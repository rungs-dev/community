# @repo/runtime

## 0.5.0

- Add the Array tab — shift registers, FIFO and LIFO buffers, and whole-array copy, fill, sort, average and search
- Add InOut parameters — arrays and structured tags like TIMER can now be passed to your instruction
- Add SINT and INT tags — 8-bit and 16-bit whole numbers for device registers and byte data

## 0.4.0

- Every AOI now has EnableIn and EnableOut as built-in parameters

## 0.3.0

- Add OSRI and OSFI one-shot instructions and the FBD_ONESHOT data type to Structured Text
- Make timers keep accurate time when scans run late, modeled on measured ControlLogix® behavior

## 0.2.0

- Run a Logix-style prescan pass before the first scan; setting EnableIn to 0 now skips Logic and clears EnableOut
- Structured Text timers and counters ignore runtime .ACC writes, matching Logix
