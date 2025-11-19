---
inclusion: conditional
fileMatchPattern: "**/remote_api_client.dart"
---

# API Integration Guidelines

## Backend Communication

### Base URL Configuration
- Android Emulator: `http://10.0.2.2:3000`
- iOS Simulator: `http://localhost:3000`
- Physical Device: Use actual IP address
- Production: Use deployed backend URL

### Error Handling
Always wrap API calls in try-catch blocks:
```dart
try {
  final response = await http.get(Uri.parse(url));
  if (response.statusCode == 200) {
    return json.decode(response.body);
  } else {
    throw Exception('API Error: ${response.statusCode}');
  }
} catch (e) {
  print('Network error: $e');
  // Fallback to local database
  return await DatabaseHelper.instance.fallbackMethod();
}
```

### API Endpoints
- POST /auth/register
- POST /auth/login
- GET /users/:username/points
- PUT /users/:username/points
- GET /users/:username/theme
- PUT /users/:username/theme
- GET /users/:username/themes
- POST /users/:username/themes/purchase
- GET /users/:username/powerups
- POST /users/:username/powerups/purchase
- POST /users/:username/powerups/use

### Request Format
All requests should include:
- Content-Type: application/json
- Proper error handling
- Timeout configuration (10 seconds)
