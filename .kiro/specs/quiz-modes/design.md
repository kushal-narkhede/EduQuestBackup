# Quiz Modes Design

## Correctness Properties

### CP-1: Timer Accuracy (covers AC-1)
**Property**: Lightning mode timer must count down accurately and end quiz at 0.

### CP-2: Lives Management (covers AC-2)
**Property**: Survival mode must track lives correctly and end game at 0 lives.

### CP-3: Card Matching (covers AC-3)
**Property**: Memory Master must validate matches and prevent cheating.

### CP-4: Puzzle Progress (covers AC-4)
**Property**: Puzzle pieces unlock only after correct answers.

### CP-5: Map Progression (covers AC-5)
**Property**: Treasure Hunt locations unlock sequentially.

### CP-6: FRQ Grading (covers AC-6)
**Property**: AI grading system accurately evaluates free response answers.

## Implementation

### Mode Screens
- `lib/screens/modes/lightning_mode_screen.dart`
- `lib/screens/modes/survival_mode_screen.dart`
- `lib/screens/modes/memory_master_mode_screen.dart`
- `lib/screens/modes/puzzle_quest_screen.dart`
- `lib/screens/modes/treasure_hunt_mode_screen.dart`
- `lib/helpers/frq_manager.dart` (AI grading system)

### Common Components
- Question display widget
- Answer button grid
- Score tracking
- Theme integration
