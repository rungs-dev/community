# studio-assist

## 0.2.5

- Teach the timer transition-window idiom in test guidance so generated tests accept every correct implementation
- Show clearer test failure messages with the failing scan's time, carried inputs, and the previous scan's value
- Add per-case `scanTime` and hold-only steps to tests — timing checks can now run finer than the 100 ms default

## 0.2.4

- Speed up Relay replies by moving the AI tutor to GPT-5.6-Luna model

## 0.2.3

- Add OSR and OSF one-shot instructions to the Ladder Diagram
- Add OSRI and OSFI one-shot instructions and the FBD_ONESHOT data type to Structured Text
- Make timers keep accurate time when scans run late, modeled on measured ControlLogix® behavior

## 0.2.2

- New Ladder Diagram one-input math instructions: ABS, SQRT, and NEG (Math tab), with emulator-verified edge cases
- Add Ladder Logic AND, OR, XOR, NOT bitwise blocks and a Move/Logical toolbar tab
- Add Ladder Logic MVM, CLR, and BTD blocks to the Move/Logical tab
- Major faults now stop the scan: array subscript errors and negative timer presets abort at the faulting instruction
- Add NOP, AFI, and MOD ladder instructions
- Run a Logix-style prescan pass before the first scan; setting EnableIn to 0 now skips Logic and clears EnableOut
- Radix numeric literals in ST and Ladder: 16#, 2#, and 8# DINT bit patterns with underscore grouping
- ST no longer accepts TRUE/FALSE literals, matching Logix®: BOOL values are 1 or 0
- ST AND/OR/XOR/NOT are bitwise on numeric operands, matching Logix®; & synonym pinned; bitwise legal in subscripts

## 0.2.1

- Improve Relay's guidance on ladder timers, comparisons, and timed logic in Structured Text
- Show Relay's thinking while it prepares an answer, with full thoughts on click

## 0.2.0

- Improve Relay chat: explain ladder logic in plain terms, and suggest a new AOI when your goal doesn't fit the exercise

## 0.1.8

- Add `hold` to AOI unit tests — assert outputs keep their value on every scan of a step

## 0.1.7

- Stop Relay replying with raw ladder DSL — it now describes rung changes in plain words
- Stop Relay flagging valid Ladder rungs as errors and telling you to delete semicolons
- Add Scan Cycle docs and teach Relay to explain the one-scan delay from rung and statement order

## 0.1.6

- Patch Relay giving inaccurate guidance on Studio's simulation timing, compiler errors, and ladder edits

## 0.1.5

- Teach Relay the `Cfg_` prefix for design-time parameters like preset times and limits, separate from live `In_` inputs
- Teach Relay the real toolbar button names so it stops telling you to click `Start simulation` when you want `Test`
- Make Relay's answers more consistent — its rules now live in one stable place instead of being re-sent on every message
- Teach Relay the PlantPAx tag prefixes (In*, Out*, Sts*, Tmr*, Cnt*, Val*, Wrk\_) so it stops suggesting prefix-less names
- Add exercise mode: open a practice exercise with its brief and runnable, locked acceptance tests

## 0.1.4

- Add an optional Description to your AOI — shown in the print header and surfaced to Relay.
- Stop Relay from suggesting you delete the canned tests on seeded example AOIs.
- Move Studio context out of the system prompt into the user message via a server-rendered `<studio-context>` block.

## 0.1.3

- Relay chat improvements
- Improve how Relay explains scan order, distinguishing the logic scan from the asynchronous I/O update.

## 0.1.2

- Teach Relay the array index expression rules: which forms are allowed and which are rejected.
- Improve Relay agent

## 0.1.1

- Relay assistant improvements
