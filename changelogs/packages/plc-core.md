# @repo/plc-core

## 0.5.0

- Show errors in ladder and structured text when an array tag like `PhaseTimer.ACC` is used without an index.
- Edit tag defaults from block instructions
- Accept negative scientific REAL literals (`-1.5e1`) in ladder block operands; reject `.5e2` and `+1.5e0`
- Improve tag autocomplete in the ladder and structured text editors.

- Accept data type names like `DINT`, `BOOL`, `TIMER`, `FBD_TIMER`, and `FBD_COUNTER` as tag names, matching Studio 5000 Logix Designer®.
- New `FBD_TIMER` and `FBD_COUNTER` tags now default `.EnableIn` to 1, matching Studio 5000 Logix Designer®.

## 0.4.0

- Introduce YAML-based test vectors for AOIs

## 0.3.0

- Add Ladder Diagram (LD) programming language
  - Ladder editor with drag-and-drop editing, branch support, and inline parameter editing
  - Full instruction set: bit (XIC, XIO, ONS, OTE, OTL, OTU), timer (TON, TOF, RTO), counter (CTU, CTD), math (ADD, SUB, MUL, DIV), compare (EQ, NE, GT, GE, LT, LE), move (MOV), reset (RES)
  - LD compiler pipeline: lexer, parser, semantic analysis, and JS code generation
  - DSL parser/serializer for ladder diagram persistence
  - Simulation integration with runtime energization highlighting and diagnostics
  - Shared ladder UI component library
  - Example LD AOIs: MotorControl, TrafficLight, TankLevel, Cylinder

## 0.2.0

- Enhance tag value parsing and validation
- Enhance AOI schema and validation
- Integrate Zod for AOI validation

## 0.1.1

- Fix AOI import/export parser and serializer to support default values for local tags and array elements

## 0.1.0

- Initial release
