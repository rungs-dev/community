# studio

## 0.11.3

- Complete instruction and direct tag suggestions without interrupting keyboard navigation.
- Improve Tab and arrow-key editing across nested ladder instructions, and focus the first operand after insertion.
- Sign in with a one-time code emailed to you, alongside Google and GitHub
- Scope tag actions to the operand that opened the menu, restore ladder focus after tag creation, and hide diagnostics while inline controls are active.

## 0.11.2

- Swap one ladder instruction for another in place — double-click it, then pick the new one from the list

## 0.11.1

- Stop the docs site and Studio from loading blank right after a new version ships

## 0.11.0

- Show clearer test failure messages with the failing scan's time, carried inputs, and the previous scan's value
- Add per-case `scanTime` and hold-only steps to tests — timing checks can now run finer than the 100 ms default
- Accept minute and hour units in test time values, so an hour-long wait reads `time: 1h` instead of `3600000ms`
- Fix test editor autocomplete: right suggestions at every indent and correct indentation when pressing Enter
- Explain test file mistakes better: typo suggestions, specific `advance` errors, and impossible BOOL or DINT values flagged
- Structured Text timer-reuse warning now fires only when different timer instructions share a tag, and names them

## 0.10.1

- Point deprecated ladder mnemonics at their current name, so `GEQ` now says to use `GE`, and `MOV` to use `MOVE`
- Speed up Relay replies by moving the AI tutor to GPT-5.6-Luna model
- Tell real ladder instructions rungs.dev does not support apart from names that are not instructions at all

## 0.10.0

- Add OSR and OSF one-shot instructions to the Ladder Diagram
- Add OSRI and OSFI one-shot instructions and the FBD_ONESHOT data type to Structured Text
- Pause the simulation while Studio sits in a background tab, and resume it when you come back
- Make timers keep accurate time when scans run late, modeled on measured ControlLogix® behavior
- Remove the What you'll learn section from the exercise panel
- Allow instruction mnemonics like TON or OSR as tag names and stop AOI names from shadowing built-in instructions

## 0.9.0

- New Ladder Diagram one-input math instructions: ABS, SQRT, and NEG (Math tab), with emulator-verified edge cases
- Add Ladder Logic AND, OR, XOR, NOT bitwise blocks and a Move/Logical toolbar tab
- Add Ladder Logic MVM, CLR, and BTD blocks to the Move/Logical tab
- Major faults now stop the scan: array subscript errors and negative timer presets abort at the faulting instruction
- Add NOP, AFI, and MOD ladder instructions
- Radix numeric literals in ST and Ladder: 16#, 2#, and 8# DINT bit patterns with underscore grouping
- ST AND/OR/XOR/NOT are bitwise on numeric operands, matching Control Logix®; & synonym pinned; bitwise legal in subscripts
- Stop suggesting an invalid tag type when you create a tag for the SIZE or reset (RES) instructions
- Fix DINT math to wrap at 32 bits like a real controller, including MUL overflow and mid-expression results
- Show an error when a ladder timer (TON, TOF, RTO) runs with a negative PRE or ACC
- ST no longer accepts TRUE/FALSE literals, matching Logix®: BOOL values are 1 or 0
- Fix EXIT in Structured Text to stop only the innermost loop instead of ending the whole routine
- Catch mistakes in Structured Text math functions like ABS and SIN as you type them instead of when the program runs
- ST `MOD` by zero now returns 0 and `MOD` accepts REAL operands, matching observed Logix controller behavior
- Structured Text timers and counters ignore runtime .ACC writes, matching Logix

## 0.8.5

- Show Relay's thinking while it prepares an answer, with full thoughts on click

## 0.8.4

- Improve Relay chat: explain ladder logic in plain terms, and suggest a new AOI when your goal doesn't fit the exercise

## 0.8.3

- Add `hold` to AOI unit tests — assert outputs keep their value on every scan of a step

## 0.8.2

- Fix ladder Timer Off Delay (TOF) so its output turns off exactly at the preset instead of one scan late
- Stop Relay replying with raw ladder DSL — it now describes rung changes in plain words
- Stop Relay flagging valid Ladder rungs as errors and telling you to delete semicolons
- Add Scan Cycle docs and teach Relay to explain the one-scan delay from rung and statement order
- Run Structured Text timers and counter whenever they are called; setting EnableIn to 0 no longer disables them
- Show the Timer Off Delay with Reset (TOFR) .ACC value counting up to the preset instead of down

## 0.8.1

- Rename Studio's Exercises sidebar link to Learn and point it to the new learn.rungs.dev catalog
- Patch Relay giving inaccurate guidance on Studio's simulation timing, compiler errors, and ladder edits

## 0.8.0

- Show a cookie banner so you can accept or reject product analytics
- Sort the Tags table by clicking the Name, Data Type, or Usage column header
- Sign in to Studio with your Google or GitHub account
- Groundwork for the upcoming Rungs Learn launch: exercise mode

## 0.7.2

- Add an optional Description to your AOI — shown in the print header and surfaced to Relay.
- Relay improvements.

## 0.7.1

- Warn when an OTE coil and another coil target the same tag in ladder routines.
- Fix thumbs up/down feedback on Relay replies.
- Relay chat improvements
- Flag every place a timer is reused in a routine, not just the second occurrence.

## 0.7.0

- Show errors in ladder and structured text when an array tag like `PhaseTimer.ACC` is used without an index.
- Support array index expression operands like `BoolArray[(I + 1) * 2]` in ladder instructions, with caret-preserving input and no mid-expression wrapping.
- Accept data type names like `DINT`, `BOOL`, `TIMER`, `FBD_TIMER`, `FBD_COUNTER` as tag names, matching Logix Designer®.
- Studio now shows accurate live values for ladder array indexes that use expressions, such as `DintArray[I-1]`.
- New `FBD_TIMER` and `FBD_COUNTER` tags now default `.EnableIn` to 1, matching Studio 5000 Logix Designer®.
- Model numeric semantics on Studio 5000 Logix Designer (banker rounding, destination-driven division, 32-bit REAL).
- Print AOIs from the toolbar (or Ctrl/Cmd+P): tags, ladder routines with defaults and error highlights, ST, and tests.
- Status panel logs now reset on each test or simulation run, so output reflects the latest action.
- Improve tag autocomplete in the ladder and structured text editors.
- Edit tag defaults from block instructions
- Fix the `FOR_DO` instruction example to iterate `0 to storageCount - 1`, avoiding an out-of-bounds read each scan.
- Add ladder-editor region-tier keyboard editing
- Improve Relay chat error messages so rate-limit and connectivity failures explain the cause and suggest a fix.
- Accept negative scientific REAL literals (`-1.5e1`) in ladder block operands; reject `.5e2` and `+1.5e0`
- Improve Relay agent

## 0.6.3

- Fix ladder-editor rendering issue

## 0.6.2

- Add tooltip to ladder toolbar

## 0.6.1

- Relay assistant improvements

## 0.6.0

- Add Relay AI Chat
- Add links to exercises.rungs.dev

## 0.5.1

- Minor bug fixes

## 0.5.0

- Introduce YAML-based test vectors for AOIs
- Implement quick fix functionality for tag creation
- Unify status panel into terminal-style log stream
- Add yellow color for paused state visualization in ladder-editor

## 0.4.7

- Add pause and step controls to simulation
- Change library AOI items to open on single click instead of double click
- Fix undo/redo functionality in Ladder editor
- Fix tag editor creating unnecessary undo steps when selecting rows or saving without changes
- Renaming a tag now updates its name in all editors

## 0.4.6

- Add dark mode
- Improve ladder simulation interface

## 0.4.5

- Add LIMIT to ladder-editor toolbar

## 0.4.4

- Add rung comments

## 0.4.3

- UI improvements
- Rebuilt tag editor with undo/redo and row selection

## 0.4.2

- Fix Monaco init
- Reset editor state on example AOI load
- Add LIMIT instruction
- Auto-select next element after deletion
- Implement warnings for repeated timer
- Extend LD parser syntax support
- Move ST/LD compile to a timeout-backed worker to prevent UI freezes
- Add type aware create tag dialog in ladder-editor
- Improve ladder copy-paste functionality

## 0.4.1

- Fix dragged ladder element display
  Implement undo/redo
- Add tag autocomplete
- Implement copy/paste

## 0.4.0

- Add Ladder Diagram (LD) programming language
  - Ladder editor with drag-and-drop editing, branch support, and inline parameter editing
  - Full instruction set: bit (XIC, XIO, ONS, OTE, OTL, OTU), timer (TON, TOF, RTO), counter (CTU, CTD), math (ADD, SUB, MUL, DIV), compare (EQ, NE, GT, GE, LT, LE), move (MOV), reset (RES)
  - LD compiler pipeline: lexer, parser, semantic analysis, and JS code generation
  - DSL parser/serializer for ladder diagram persistence
  - Simulation integration with runtime energization highlighting and diagnostics
  - Shared ladder UI component library
  - Example LD AOIs: MotorControl, TrafficLight, TankLevel, Cylinder

## 0.3.5

- Add Example AOIs to the library

## 0.3.4

- Replace onboarding UI with automatic AOI bootstrap
- Open AOI trend when starting simulation only for new users

## 0.3.3

- Add PostHog React error tracking
- Open AOI trend when starting simulation

## 0.3.2

- Add PostHog custom events

## 0.3.1

- Implement gate screen for mobile devices

## 0.3.0

- Implement AOI sharing functionality
- Add dialog for creating AOIs with user-defined names

## 0.2.0

- Enhance tag value parsing and validation
- Migrate state management from Redux to Zustand
- Improve AOI file import/export functionality
- Enhance AOI schema and validation
- Integrate Zod for AOI validation

## 0.1.1

- Fix trend's tooltip and markers positioning
- Add version info
- Temporarily disable the local "My AOIs"

## 0.1.0

- Initial release
