# REPULSE — Phase 2 Core Android MVP

A native Android starter implementation using Kotlin, Jetpack Compose, Room, and timestamp-based timer state.

## Requirements
- Android Studio Ladybug or newer
- JDK 17
- Android SDK 35
- Android device or emulator running Android 8.0 (API 26) or newer

## Open and run
1. Extract the project folder.
2. Open the `REPULSE` folder in Android Studio.
3. Allow Gradle sync to complete.
4. Select an Android emulator or connected device.
5. Press Run.

The first launch seeds five editable-in-later-phase starter activity definitions.

## Implemented in this phase
- Today screen and light theme
- Counter, checkbox, timer, and manual distance logging
- Local Room persistence
- Current and best all-habits streak calculation
- Timer state persistence using epoch timestamps
- Three-tab navigation shell

## Phase 2 scope notes
The History and Routines tabs are intentionally basic navigation shells. Full history calendar, editing, reordering, archive, and backup belong to Phase 3/4.

The Add button currently opens a name-entry dialog but does not yet persist a custom habit; full habit creation is part of Phase 3. This is deliberately not presented as a completed feature.

## Important implementation notes
- Daily logs use the device's local `LocalDate` key.
- Counter updates are clamped at zero.
- A timer's persisted start timestamp is used to reconstruct remaining time after process recreation.
- Timer UI refreshes do not determine elapsed time; timestamps do.
- The current implementation assumes the device wall clock remains reasonably accurate while the app is closed. Stronger reboot/time-change recovery and timer notification behavior are Phase 4 hardening work.

## Package
`com.repulse.app`
