---
inclusion: conditional
fileMatchPattern: "**/*screen.dart"
---

# Theme System Integration

## Available Themes
1. **space** (default) - Dark space theme with gradient
2. **beach** - Bright beach background with warm colors
3. **forest** - Nature-themed with green tones
4. **arctic** - Cool blue/white ice theme
5. **crystal** - Glass/transparent aesthetic
6. **volcano** - Fiery red/orange theme

## Theme Integration in Screens

### Background Widget
Always use the helper function:
```dart
Stack(
  children: [
    getBackgroundForTheme(currentTheme),
    // Your content here
  ],
)
```

### Color Scheme
Use ThemeColors helper:
```dart
// Primary color (background accent)
ThemeColors.getPrimaryColor(currentTheme)

// Secondary color (cards, dialogs)
ThemeColors.getSecondaryColor(currentTheme)

// Button color
ThemeColors.getButtonColor(currentTheme)

// Text color (auto-adjusts for readability)
ThemeColors.getTextColor(currentTheme)
```

### Text Readability
Beach theme uses dark text, others use light text:
```dart
TextStyle(
  color: currentTheme == 'beach' 
    ? Colors.brown.shade800 
    : Colors.white,
)
```

### Overlay Styles
Set status bar colors appropriately:
```dart
SystemChrome.setSystemUIOverlayStyle(
  ThemeColors.getOverlayStyle(currentTheme)
);
```

## Theme Persistence
Themes are stored in:
- Local: SQLite users table (current_theme column)
- Remote: MongoDB User model (currentTheme field)
- Cache: SharedPreferences for quick access
