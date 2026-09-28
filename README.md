# Ludo Buddy - Flutter source

A polished, offline, pass-and-play Ludo game for 2-4 players on one Android device.

## What is included

- `lib/main.dart` - app entry point and theme wiring
- `lib/theme.dart` - the colour system
- `lib/game/board_data.dart` - board geometry (52 ring squares, home columns, yards, safe squares)
- `lib/game/ludo_game.dart` - the complete, framework-free rules engine
- `lib/widgets/dice.dart` - a pips-based animated dice face
- `lib/widgets/ludo_board.dart` - the board painter + animated tokens
- `lib/screens/setup_screen.dart` - player selection screen
- `lib/screens/game_screen.dart` - the game screen (roll, move, win)
- `test/ludo_game_test.dart` - unit tests for the rules

## Rules implemented

- 2, 3 or 4 local players, classic board layout
- Roll a 6 to leave the yard
- Rolling a 6 grants another turn
- Exact count required to reach the finish
- Capture an opponent on a non-safe ring square
- Safe squares: the four start squares and the four star squares
- Win when all four tokens are finished

## How to run

```bash
flutter pub get
flutter test        # optional: checks the rules
flutter run
```

## How to build release files

```bash
flutter build apk --release        # build/app/outputs/flutter-apk/app-release.apk
flutter build appbundle --release  # build/app/outputs/bundle/release/app-release.aab
```

The APK is for sharing/sideloading. The AAB is what Google Play requires for upload.
