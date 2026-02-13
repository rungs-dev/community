# @repo/plc-compiler

## 0.2.1

### Patch Changes

- 377f9cc: Add LIMIT instruction
- 0af1eb4: Implement warnings for repeated timer
- f171c1f: Extend LD parser syntax support
- d1f9349: Move ST/LD compile to a timeout-backed worker to prevent UI freezes

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

## 0.1.0

### Minor Changes

- 8d954ba: Initial release
