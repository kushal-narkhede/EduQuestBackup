# Gamification System Design

## Architecture

### Database Schema

#### Users Table
```sql
CREATE TABLE users (
  id INTEGER PRIMARY KEY,
  username TEXT UNIQUE NOT NULL,
  password TEXT NOT NULL,
  points INTEGER DEFAULT 0,
  current_theme TEXT DEFAULT 'space'
);
```

#### Themes Table
```sql
CREATE TABLE user_themes (
  user_id INTEGER,
  theme_name TEXT,
  FOREIGN KEY (user_id) REFERENCES users(id)
);
```

#### Power-ups Table
```sql
CREATE TABLE user_powerups (
  user_id INTEGER,
  powerup_id TEXT,
  count INTEGER DEFAULT 0,
  FOREIGN KEY (user_id) REFERENCES users(id)
);
```

## Correctness Properties

### CP-1: Theme Persistence (covers AC-1)
**Property**: When a user selects a theme, it must be saved to the database and restored on next login.

**Verification**: 
- User selects beach theme
- App restarts
- Beach theme is still active

### CP-2: Points Integrity (covers AC-2)
**Property**: Points can only increase through earning or decrease through spending. Points cannot go negative.

**Verification**:
- User earns 10 points → balance increases by 10
- User spends 5 points → balance decreases by 5
- User attempts to spend more than balance → transaction rejected

### CP-3: Power-up Inventory (covers AC-3)
**Property**: Power-up count must accurately reflect purchases and usage.

**Verification**:
- User purchases 3 skip power-ups → inventory shows 3
- User uses 1 skip → inventory shows 2
- User cannot use power-up when count is 0

### CP-4: Shop Transactions (covers AC-4)
**Property**: All shop purchases must be atomic - either both point deduction and item grant succeed, or neither happens.

**Verification**:
- User with 100 points buys 50-point theme → points become 50, theme unlocked
- If database error occurs → points unchanged, theme not unlocked

### CP-5: Data Sync (covers AC-5)
**Property**: Local and remote data stores must maintain consistency when sync is enabled.

**Verification**:
- User earns points locally → synced to MongoDB
- User purchases theme remotely → reflected in local SQLite

## Implementation Notes

### Theme System
- Use `ThemeColors` helper class for consistent color schemes
- Background widgets: `SpaceBackground`, `BeachBackground`, `_ImageBackground`
- Store theme preference in SharedPreferences for quick access

### Points System
- DatabaseHelper methods: `getUserPoints()`, `updateUserPoints()`
- RemoteApiClient methods: `getUserPoints()`, `updateUserPoints()`
- UI updates via setState after point changes

### Power-ups System
- Power-up IDs: 'skip', 'fifty_fifty', 'time_freeze', 'double_points'
- Shop prices defined in ShopTab widget
- Usage logic in quiz screens

## API Endpoints (Backend)

```
POST /auth/register
POST /auth/login
GET /users/:username/points
PUT /users/:username/points
GET /users/:username/theme
PUT /users/:username/theme
GET /users/:username/themes
POST /users/:username/themes/purchase
GET /users/:username/powerups
POST /users/:username/powerups/purchase
POST /users/:username/powerups/use
```
