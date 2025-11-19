---
inclusion: conditional
fileMatchPattern: "**/database_helper.dart"
---

# Database Patterns and Best Practices

## SQLite Schema

### Users Table
```sql
CREATE TABLE users (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  username TEXT UNIQUE NOT NULL,
  password TEXT NOT NULL,
  points INTEGER DEFAULT 0,
  current_theme TEXT DEFAULT 'space'
)
```

### Common Patterns

#### Singleton Pattern
```dart
class DatabaseHelper {
  static final DatabaseHelper instance = DatabaseHelper._init();
  static Database? _database;
  
  DatabaseHelper._init();
  
  Future<Database> get database async {
    if (_database != null) return _database!;
    _database = await _initDB('eduquest.db');
    return _database!;
  }
}
```

#### CRUD Operations
- Always use parameterized queries to prevent SQL injection
- Handle null values appropriately
- Return meaningful error messages
- Use transactions for related operations

#### Error Handling
```dart
try {
  final db = await database;
  await db.insert('users', user.toMap());
} on DatabaseException catch (e) {
  if (e.isUniqueConstraintError()) {
    throw Exception('Username already exists');
  }
  throw Exception('Database error: $e');
}
```

## Migration Strategy
When adding new columns:
1. Check if column exists
2. Use ALTER TABLE if needed
3. Provide default values
4. Test with existing data
