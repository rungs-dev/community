# @repo/plc-core

## 0.3.0

### Minor Changes

- 19a0828: Add Ladder Diagram (LD) programming language
  - Ladder editor with drag-and-drop editing, branch support, and inline parameter editing
  - Full instruction set: bit (XIC, XIO, ONS, OTE, OTL, OTU), timer (TON, TOF, RTO), counter (CTU, CTD), math (ADD, SUB, MUL, DIV), compare (EQ, NE, GT, GE, LT, LE), move (MOV), reset (RES)
  - LD compiler pipeline: lexer, parser, semantic analysis, and JS code generation
  - DSL parser/serializer for ladder diagram persistence
  - Simulation integration with runtime energization highlighting and diagnostics
  - Shared ladder UI component library
  - Example LD AOIs: MotorControl, TrafficLight, TankLevel, Cylinder

## 0.2.0

### Minor Changes

- 2257902: Enhance tag value parsing and validation
- 5fde104: Enhance AOI schema and validation
- b71f693: Integrate Zod for AOI validation

## 0.1.1

### Patch Changes

- 0f5dc05: Fix AOI import/export parser and serializer to support default values for local tags and array elements

## 0.1.0

### Minor Changes

- 8d954ba: Initial release
