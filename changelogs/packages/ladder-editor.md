# @repo/ladder-editor

## 0.2.2

### Patch Changes

- 377f9cc: Add LIMIT instruction
- 5862ce2: Auto-select next element after deletion
- f171c1f: Extend LD parser syntax support
- 30af30c: Add type aware create tag dialog in ladder-editor
- be58116: Improve ladder copy-paste functionality

## 0.2.1

### Patch Changes

- ac04f00: Fix dragged ladder element display
  Implement undo/redo
- d5f17a5: Add tag autocomplete
- 09c8ce5: Implement copy/paste

## 0.2.0

### Minor Changes

- 19a0828: Add Ladder Diagram (LD) programming language
  - Ladder editor with drag-and-drop editing, branch support, and inline parameter editing
  - Full instruction set: bit (XIC, XIO, ONS, OTE, OTL, OTU), timer (TON, TOF, RTO), counter (CTU, CTD), math (ADD, SUB, MUL, DIV), compare (EQ, NE, GT, GE, LT, LE), move (MOV), reset (RES)
  - LD compiler pipeline: lexer, parser, semantic analysis, and JS code generation
  - DSL parser/serializer for ladder diagram persistence
  - Simulation integration with runtime energization highlighting and diagnostics
  - Shared ladder UI component library
  - Example LD AOIs: MotorControl, TrafficLight, TankLevel, Cylinder
