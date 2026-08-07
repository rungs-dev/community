# @repo/test-runner

## 0.5.0

- Show clearer test failure messages with the failing scan's time, carried inputs, and the previous scan's value
- Add per-case `scanTime` and hold-only steps to tests — timing checks can now run finer than the 100 ms default
- Accept minute and hour units in test time values, so an hour-long wait reads `time: 1h` instead of `3600000ms`
- Explain test file mistakes better: typo suggestions, specific `advance` errors, and impossible BOOL or DINT values flagged

## 0.4.1

## 0.4.0

- Make timers keep accurate time when scans run late, modeled on measured ControlLogix® behavior
- Add OSRI and OSFI one-shot instructions and the FBD_ONESHOT data type to Structured Text

## 0.3.0

- Run a Logix-style prescan pass before the first scan; setting EnableIn to 0 now skips Logic and clears EnableOut

## 0.2.0

- Add `hold` to AOI unit tests — assert outputs keep their value on every scan of a step
- Run AOI tests through one shared runner everywhere — `runTestVectors` is now async with a pluggable executor

## 0.1.5

## 0.1.4

- Internal: move the PLC exercise specs into a shared catalog package with runtime validation

## 0.1.3

## 0.1.2

## 0.1.1

- @repo/runtime@0.1.1
