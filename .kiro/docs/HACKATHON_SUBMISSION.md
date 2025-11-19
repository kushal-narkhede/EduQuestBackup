# Hackathon Submission - EduQuest

## Submission Checklist

### ✅ Required Items

#### 1. Open Source Code Repository
- **URL**: https://github.com/AbhinavRaneesh/EduQuest
- **Status**: Public repository
- **License**: MIT License (OSI approved) - see LICENSE file
- **/.kiro Directory**: ✅ Present at root with specs, hooks, and steering
- **.gitignore**: ✅ Does NOT exclude .kiro directory

#### 2. Functional Application URLs
- **Flutter App**: Available for download from repository
  - Android: Build APK from source
  - iOS: Build from source (requires Mac)
  - Web: Can be deployed to Firebase Hosting or similar
- **Backend API**: Node.js server (instructions in server/README.md)
  - Local: http://localhost:3000
  - Can be deployed to Heroku, Railway, or similar

**Login Credentials** (for testing):
```
Username: demo_user
Password: demo123
```
(Or create new account - registration is open)

#### 3. Demonstration Video
- **Platform**: YouTube / Vimeo / Facebook Video
- **Duration**: 3 minutes maximum
- **Visibility**: Public
- **Content to Cover**:
  - App overview and features
  - Gamification system (themes, points, power-ups)
  - Quiz modes demonstration
  - AI-based FRQ grading system
  - Study sets management
  - AI chat assistant
  - Backend integration

**Video URL**: [TO BE ADDED]

#### 4. Category Selection
**Primary Category**: Education Technology

**Bonus Category**: Best Use of AI (AI-powered study assistant with chat interface)

#### 5. Kiro Usage Write-up
**Location**: `.kiro/KIRO_USAGE_WRITEUP.md`

**Summary**:
- **Vibe Coding**: Generated 11,500+ lines of code through conversational development
  - Most impressive: AI-based FRQ grading system with natural language processing
- **Agent Hooks**: 3 automated workflows (analyze, format, test)
  - Saved ~30 minutes/day on formatting
  - Prevented 15+ issues from reaching repository
- **Spec-Driven Development**: 4 comprehensive specs with requirements, design, and tasks
  - Better for complex features vs vibe coding for UI
- **Steering Documents**: 5 context-aware guides (2 always-included, 3 conditional)
  - Eliminated repetitive instructions
  - Ensured consistent code patterns
- **MCP**: N/A (not used in this project)

**Key Metrics**:
- Lines Generated: 11,500+
- Time Saved: 60+ hours
- Features Completed: 20+
- Kiro Contribution: ~95% of codebase

---

## Project Overview

### What is EduQuest?
EduQuest is a gamified learning platform that makes education engaging through:
- 6 customizable visual themes
- 5 unique quiz game modes
- AI-based FRQ (Free Response Question) grading
- Points and rewards system
- Power-ups for gameplay advantages
- AI-powered study assistant
- Custom and premade study sets
- Full-stack architecture (Flutter + Node.js + MongoDB)

### Technical Architecture
- **Frontend**: Flutter (Dart) - Cross-platform mobile app
- **Backend**: Node.js + Express + MongoDB
- **Database**: SQLite (local) + MongoDB Atlas (cloud sync)
- **State Management**: BLoC pattern for complex state
- **AI Integration**: Chat interface with message persistence

### Key Features
1. **Gamification System**: Themes, points, power-ups, shop
2. **Quiz Modes**: Lightning, Survival, Memory Master, Puzzle Quest, Treasure Hunt
3. **AI-Based FRQ Grading**: Automatic grading of free response questions using AI
4. **Study Management**: Create, import, browse study sets
5. **AI Assistant**: Chat-based learning support
6. **Cloud Sync**: Optional backend synchronization

---

## How Kiro Was Used

### Development Workflow
1. **Planning**: Created specs with requirements and design
2. **Implementation**: Vibe coded features with Kiro guidance
3. **Quality**: Hooks automatically formatted and analyzed code
4. **Verification**: Checked against correctness properties

### Kiro's Impact
- **Speed**: Reduced development time by ~60 hours
- **Quality**: Consistent code style and patterns
- **Complexity**: Generated sophisticated features (game physics, state management)
- **Full-Stack**: Seamlessly worked across Flutter and Node.js

### Advanced Techniques
- Spec references with #[[file:]] syntax
- Multi-file generation in single conversation
- Context-aware steering (conditional inclusion)
- Automated quality workflows with hooks

---

## Repository Structure

```
EduQuest/
├── .kiro/                    # Kiro configuration (REQUIRED FOR JUDGING)
│   ├── specs/                # Spec-driven development docs
│   ├── hooks/                # Automated workflow hooks
│   ├── steering/             # Context-aware guidance
│   ├── docs/                 # Documentation files
│   │   ├── KIRO_USAGE_WRITEUP.md # Detailed Kiro usage
│   │   ├── JUDGES_QUICK_START.md
│   │   └── ...
│   └── README.md             # Kiro config overview
├── lib/                      # Flutter app source code
├── server/                   # Node.js backend
├── assets/                   # Images, animations, content
├── LICENSE                   # MIT License (OSI approved)
├── README.md                 # Project documentation
└── HACKATHON_SUBMISSION.md   # This file
```

---

## Setup Instructions

### Flutter App
```bash
# Clone repository
git clone https://github.com/AbhinavRaneesh/EduQuest.git
cd EduQuest

# Install dependencies
flutter pub get

# Run app
flutter run
```

### Backend Server (Optional)
```bash
cd server

# Install dependencies
npm install

# Configure environment
cp .env.example .env
# Edit .env with MongoDB URI

# Run server
npm run dev
```

---

## Judges: What to Look For

### 1. Kiro Usage Excellence
- Review `.kiro/docs/KIRO_USAGE_WRITEUP.md` for comprehensive documentation
- Examine specs to see structured development process
- Check hooks for workflow automation
- Read steering docs for context-aware guidance

### 2. Code Quality
- Consistent style (thanks to format-on-save hook)
- Proper error handling
- Clean architecture (BLoC pattern, repository pattern)
- Comprehensive documentation

### 3. Feature Completeness
- 20+ major features implemented
- Full-stack integration
- Multiple game modes
- AI integration
- Cloud synchronization

### 4. Innovation
- AI-based automatic FRQ grading with natural language processing
- Gamification for learning motivation
- AI-powered study assistant
- Flexible study set management

---

## Contact Information

**Team Members**:
- Abhinav Raneesh - abhinav.raneesh@gmail.com
- Kushal Narkhede - kushalnarkhede09@gmail.com

**Repository**: https://github.com/AbhinavRaneesh/EduQuest

**Questions?** Open an issue on GitHub or email us directly.

---

## Acknowledgments

Special thanks to Kiro for enabling rapid development and maintaining code quality throughout the project. The combination of vibe coding, spec-driven development, hooks, and steering made this ambitious project achievable within hackathon timeframes.

---

**Submission Date**: [TO BE ADDED]
**Category**: Education Technology + Best Use of AI
