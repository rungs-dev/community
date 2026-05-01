# @repo/ladder-editor

## 0.6.0

- Support array index expression operands like `BoolArray[(I + 1) * 2]` in ladder instructions, with caret-preserving input and no mid-expression wrapping.
- Edit tag defaults from block instructions
- Improve tag autocomplete in the ladder and structured text editors.

- Add ladder-editor region-tier keyboard editing
- Internal cleanup of ladder context menu and instruction tooltip components; no user-visible change.
- Print AOIs from the toolbar (or Ctrl/Cmd+P): tags, ladder routines with defaults and error highlights, ST, and tests.
- Accept negative scientific REAL literals (`-1.5e1`) in ladder block operands; reject `.5e2` and `+1.5e0`

## 0.5.0

- Add tooltip to toolbar instructions

## 0.4.0

- Introduce YAML-based test vectors foir AOIs

- Add yellow color for paused state visualization in ladder-editor

## 0.3.1

- Fix undo/redo functionality in Ladder editor

## 0.3.0

- Implement theme support
- Add static ladder diagram components
- Improve ladder simulation interface

## 0.2.4

- Add LIMIT to ladder-editor toolbar

## 0.2.3

- Add rung comments

## 0.2.2

- Add LIMIT instruction
- Auto-select next element after deletion
- Extend LD parser syntax support
- Add type aware create tag dialog in ladder-editor
- Improve ladder copy-paste functionality

## 0.2.1

- Fix dragged ladder element display
  Implement undo/redo
- Add tag autocomplete
- Implement copy/paste

## 0.2.0

- Add Ladder Diagram (LD) programming language
  - Ladder editor with drag-and-drop editing, branch support, and inline parameter editing
  - Full instruction set: bit (XIC, XIO, ONS, OTE, OTL, OTU), timer (TON, TOF, RTO), counter (CTU, CTD), math (ADD, SUB, MUL, DIV), compare (EQ, NE, GT, GE, LT, LE), move (MOV), reset (RES)
  - LD compiler pipeline: lexer, parser, semantic analysis, and JS code generation
  - DSL parser/serializer for ladder diagram persistence
  - Simulation integration with runtime energization highlighting and diagnostics
  - Shared ladder UI component library
  - Example LD AOIs: MotorControl, TrafficLight, TankLevel, Cylinder
