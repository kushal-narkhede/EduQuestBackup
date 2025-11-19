# EduQuest

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Project Description

EduQuest is a user-friendly learning app designed to make education more engaging and enjoyable. By incorporating gamified features such as theme changes, power-ups, and inbuilt games, EduQuest encourages users to learn in a fun and interactive way.

> **🏆 Hackathon Submission**: See [HACKATHON_SUBMISSION.md](HACKATHON_SUBMISSION.md) for submission details and [.kiro/docs/KIRO_USAGE_WRITEUP.md](.kiro/docs/KIRO_USAGE_WRITEUP.md) for how Kiro was used to build this project.

## Table of Contents

1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Database](#database)
4. [Requirements](#requirements)
5. [Installation Instructions](#installation-instructions)
6. [Usage Instructions](#usage-instructions)
7. [Kiro Development](#kiro-development)
8. [License](#license)
9. [Support Information](#support-information)

## Features

### 🎮 Gamification System
- **6 Visual Themes**: Space, Beach, Forest, Arctic, Crystal, Volcano
- **Points & Rewards**: Earn points by learning, spend on themes and power-ups
- **Power-ups**: Skip questions, 50/50, time freeze, double points
- **Shop System**: Purchase themes and power-ups with earned points

### 📚 Quiz Modes
- **Lightning Mode**: Fast-paced timed challenges
- **Survival Mode**: Three lives, progressive difficulty
- **Memory Master**: Card matching with educational content
- **Puzzle Quest**: Unlock puzzle pieces by answering correctly
- **Treasure Hunt**: Map-based progression system

### 🤖 AI-Powered Features
- **FRQ Grading**: Automatic grading of free response questions using AI
- **Study Assistant**: Chat-based learning support with context-aware responses
- Message history persistence
- Educational content focus

### 📖 Study Sets Management
- Create custom study sets
- Import from Excel/CSV files
- Browse premade content (AP Computer Science, SAT prep)
- Search and filter functionality
- Cloud synchronization (optional)

### ☁️ Full-Stack Architecture
- Flutter frontend (cross-platform)
- Node.js + Express backend
- SQLite local database
- MongoDB cloud sync
- RESTful API integration

## Technologies Used

EduQuest is developed using the Flutter framework to ensure a smooth and efficient cross-platform experience.

## Database

EduQuest uses SQLite as the database for storing user progress, game data, and other essential information. SQLite ensures efficient data management and retrieval for a seamless learning experience.

## Requirements

- Flutter SDK installed
- A compatible device or emulator to run the app
- Internet connection for downloading dependencies

## Installation Instructions

1. Clone the repository from GitHub:
   ```bash
   git clone https://github.com/AbhinavRaneesh/EduQuest.git
   ```
2. Navigate to the project directory:
   ```bash
   cd eduquest
   ```
3. Install dependencies:
   ```bash
   flutter pub get
   ```
4. Run the application:
   ```bash
   flutter run
   ```

> **Note:** The app is not yet published on the App Store or Play Store due to developer age restrictions.

## Usage Instructions

- Open the app and create an account.
- Customize themes according to your preference.
- Earn power-ups and rewards through interactive learning activities.
- Explore built-in games that reinforce learning.

## Kiro Development

This project was developed using **Kiro**, an AI-powered development assistant. We leveraged advanced Kiro features including:

- **Vibe Coding**: Generated 11,500+ lines of code through conversational development
- **Spec-Driven Development**: 4 comprehensive specs with structured requirements and tasks
- **Agent Hooks**: Automated code formatting, analysis, and testing
- **Steering Documents**: Context-aware guidance for consistent code patterns

**📖 Full Kiro Usage Documentation**: See [.kiro/docs/KIRO_USAGE_WRITEUP.md](.kiro/docs/KIRO_USAGE_WRITEUP.md)

### .kiro/ Directory Structure

```
.kiro/
├── specs/                      # Spec-driven development documentation
│   ├── gamification-system/    # Points, themes, power-ups
│   ├── quiz-modes/             # 5 game modes + FRQ grading
│   ├── ai-integration/         # AI chat with BLoC pattern
│   └── study-sets/             # Custom and premade study content
├── hooks/                      # Automated workflow hooks
│   ├── analyze-on-commit.json  # Pre-commit Flutter analysis
│   ├── format-on-save.json     # Auto-format Dart code
│   └── test-on-save.json       # Run tests on file save
├── steering/                   # Context-aware guidance
│   ├── flutter-best-practices.md (always included)
│   ├── project-structure.md (always included)
│   ├── database-patterns.md (conditional)
│   ├── theme-system.md (conditional)
│   └── api-integration.md (conditional)
└── docs/                       # Documentation
    ├── KIRO_USAGE_WRITEUP.md   # Comprehensive Kiro documentation
    ├── JUDGES_QUICK_START.md   # Quick reference for judges
    └── QUICK_REFERENCE.md      # Quick facts
```

### Kiro Features Demonstrated

✅ **Vibe Coding**: Conversational feature development  
✅ **Spec-Driven Development**: 4 specs with requirements, design, and tasks  
✅ **Agent Hooks**: 3 automated workflows (analyze, format, test)  
✅ **Steering Documents**: 5 context-aware guides (2 always + 3 conditional)  
✅ **Full-Stack Development**: Flutter + Node.js + MongoDB  
✅ **Complex Code Generation**: AI grading system, state management, API integration

### Key Metrics

- **Lines Generated**: 11,500+
- **Time Saved**: 60+ hours
- **Features Completed**: 20+
- **Specs Created**: 4
- **Hooks Configured**: 3
- **Steering Docs**: 5

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support Information

For any queries or support, please contact:
- **Email:** [abhinav.raneesh@gmail.com](mailto:abhinav.raneesh@gmail.com)
- **Email:** [kushalnarkhede09@gmail.com](mailto:kushalnarkhede09@gmail.com)
- **GitHub Issues:** [Open an issue](https://github.com/AbhinavRaneesh/EduQuest/issues)
