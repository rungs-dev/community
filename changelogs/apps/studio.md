# studio

## 0.4.3

### Patch Changes

- 48a83bc: UI improvements
- f71a6cf: Rebuilt tag editor with undo/redo and row selection

## 0.4.2

### Patch Changes

- ee3e1ef: Fix Monaco init
- 591e0ce: Reset editor state on example AOI load
- 377f9cc: Add LIMIT instruction
- 5862ce2: Auto-select next element after deletion
- 0af1eb4: Implement warnings for repeated timer
- f171c1f: Extend LD parser syntax support
- d1f9349: Move ST/LD compile to a timeout-backed worker to prevent UI freezes
- 30af30c: Add type aware create tag dialog in ladder-editor
- be58116: Improve ladder copy-paste functionality

## 0.4.1

### Patch Changes

- ac04f00: Fix dragged ladder element display
  Implement undo/redo
- d5f17a5: Add tag autocomplete
- 09c8ce5: Implement copy/paste

## 0.4.0

### Minor Changes

- 19a0828: Add Ladder Diagram (LD) programming language
  - Ladder editor with drag-and-drop editing, branch support, and inline parameter editing
  - Full instruction set: bit (XIC, XIO, ONS, OTE, OTL, OTU), timer (TON, TOF, RTO), counter (CTU, CTD), math (ADD, SUB, MUL, DIV), compare (EQ, NE, GT, GE, LT, LE), move (MOV), reset (RES)
  - LD compiler pipeline: lexer, parser, semantic analysis, and JS code generation
  - DSL parser/serializer for ladder diagram persistence
  - Simulation integration with runtime energization highlighting and diagnostics
  - Shared ladder UI component library
  - Example LD AOIs: MotorControl, TrafficLight, TankLevel, Cylinder

## 0.3.5

### Patch Changes

- 8a389cd: Add Example AOIs to the library

## 0.3.4

### Patch Changes

- e6091fe: Replace onboarding UI with automatic AOI bootstrap
- 1bdd209: Open AOI trend when starting simulation only for new users

## 0.3.3

### Patch Changes

- fa36f19: Add PostHog React error tracking
- 32b91ae: Open AOI trend when starting simulation

## 0.3.2

### Patch Changes

- b024152: Add PostHog custom events

## 0.3.1

### Patch Changes

- 825b75d: Implement gate screen for mobile devices

## 0.3.0

### Minor Changes

- 193da57: Implement AOI sharing functionality

### Patch Changes

- 692f1ae: Add dialog for creating AOIs with user-defined names

## 0.2.0

### Minor Changes

- 2257902: Enhance tag value parsing and validation
- f747bfa: Migrate state management from Redux to Zustand
- d213c22: Improve AOI file import/export functionality
- 5fde104: Enhance AOI schema and validation
- b71f693: Integrate Zod for AOI validation

## 0.1.1

### Patch Changes

- 0ba66c8: Fix trend's tooltip and markers positioning
- eb5bafa: Add version info
- 58d55b8: Temporarily disable the local "My AOIs"

## 0.1.0

### Minor Changes

- 8d954ba: Initial release
