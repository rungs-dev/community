# @repo/runtime

## 0.3.0

- Add OSRI and OSFI one-shot instructions and the FBD_ONESHOT data type to Structured Text
- Make timers keep accurate time when scans run late, modeled on measured ControlLogix® behavior

## 0.2.0

- Run a Logix-style prescan pass before the first scan; setting EnableIn to 0 now skips Logic and clears EnableOut
- Structured Text timers and counters ignore runtime .ACC writes, matching Logix
