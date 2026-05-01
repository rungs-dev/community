# studio

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
