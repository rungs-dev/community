# @repo/plc-compiler

## 0.3.0

- Show errors in ladder and structured text when an array tag like `PhaseTimer.ACC` is used without an index.
- Studio now shows accurate live values for ladder array indexes that use expressions, such as `DintArray[I-1]`.
- Model numeric semantics on Studio 5000 Logix Designer (banker rounding, destination-driven division, 32-bit REAL precision; removes MIN/MAX).
- Unified ST/LD array subscript grammar: shared index-expression form, runtime bounds-fault
- Extract ladder syntax into dedicated package
- LD diagnostic attribution: walker-driven analysis with operand-level nodeId/span and per-rung lexer/parser gate; new compileLDProgram(ast | parseResult) API

- Align LD runtime fault messages with the editor's 0-based rung numbering. Previously `Array subscript fault` and similar runtime logs reported `Rung N+1` while the ladder editor displays the same rung as `N`, making it harder to locate the offending rung.
- Accept negative scientific REAL literals (`-1.5e1`) in ladder block operands; reject `.5e2` and `+1.5e0`

## 0.2.4

- Enforce LD rungs end with output instruction

## 0.2.3

## 0.2.2

- Add rung comments

## 0.2.1

- Add LIMIT instruction
- Implement warnings for repeated timer
- Extend LD parser syntax support
- Move ST/LD compile to a timeout-backed worker to prevent UI freezes

## 0.2.0

- Add Ladder Diagram (LD) programming language
  - Ladder editor with drag-and-drop editing, branch support, and inline parameter editing
  - Full instruction set: bit (XIC, XIO, ONS, OTE, OTL, OTU), timer (TON, TOF, RTO), counter (CTU, CTD), math (ADD, SUB, MUL, DIV), compare (EQ, NE, GT, GE, LT, LE), move (MOV), reset (RES)
  - LD compiler pipeline: lexer, parser, semantic analysis, and JS code generation
  - DSL parser/serializer for ladder diagram persistence
  - Simulation integration with runtime energization highlighting and diagnostics
  - Shared ladder UI component library
  - Example LD AOIs: MotorControl, TrafficLight, TankLevel, Cylinder

## 0.1.0

- Initial release
