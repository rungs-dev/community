# @repo/exercise-catalog

## 0.8.0

- Add Boiler Interlocks and Burner Control exercises

## 0.7.1

- Strengthen exercise vectors so invalid shortcut logic no longer passes

## 0.7.0

- Browse the exercises as ordered courses at rungs.dev/courses, each with its own page, progress and starting point
- The free tier is now the Boolean Logic course
- Add 10 new exercises to the catalog

## 0.6.0

- Fix timed exercise tests rejecting correct solutions; a second scan cadence now catches scan-counted timing
- Add per-case `scanTime` and hold-only steps to tests — timing checks can now run finer than the 100 ms default

## 0.5.0

- Add 20 playable exercises — math, bit logic, masked moves, filters, and sequencers — bringing the catalog to 60
- Reorder the catalog easiest-first and update which 20 exercises are free
- Tighten tests, reference solutions, and behavior notes across existing exercises, with worked binary examples
- Make timers keep accurate time when scans run late, modeled on measured ControlLogix® behavior

## 0.4.1

- CTUD exercise tests observe the enable low before expecting a count, matching controller prescan behavior

## 0.4.0

- Add ten exercises and reorder the catalog so concepts build on each other — 40 exercises now playable
- Add nine exercises spanning XOR logic, edge detection, timer patterns, run-time tracking, and configurable scaling
- Remove unused exercise test-hash helpers; no user-visible change
- Strengthen ten timed exercises with `hold` assertions — outputs must now stay steady through every scan of a phase
- Add `hold` to AOI unit tests — assert outputs keep their value on every scan of a step

## 0.3.0

- Add the One-Scan Delay exercise: one lamp follows a button instantly, another follows it one scan later
- Fix the Hysteresis exercise example to match its behavior: output turns on at the high limit and off at the low limit
- Move Press-Toggle Lamp after Rising Edge, raise it to medium difficulty, and clarify what it teaches

## 0.2.0

- Internal: move the PLC exercise specs into a shared catalog package with runtime validation
- Solve exercises in Ladder Diagram or Structured Text, with progress tracked independently per language
- Add exercise mode: open a practice exercise with its brief and runnable, locked acceptance tests
