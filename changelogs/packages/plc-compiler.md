# @repo/plc-compiler

## 0.6.0

- Add OSR and OSF one-shot instructions to the Ladder Diagram
- Add OSRI and OSFI one-shot instructions and the FBD_ONESHOT data type to Structured Text
- Make timers keep accurate time when scans run late, modeled on measured ControlLogix® behavior

## 0.5.0

- New Ladder Diagram one-input math instructions: ABS, SQRT, and NEG (Math tab), with emulator-verified edge cases
- Add Ladder Logic AND, OR, XOR, NOT bitwise blocks and a Move/Logical toolbar tab
- Add Ladder Logic MVM, CLR, and BTD blocks to the Move/Logical tab
- Major faults now stop the scan: array subscript errors and negative timer presets abort at the faulting instruction
- Add NOP, AFI, and MOD ladder instructions
- Add Logix-style prescan scan mode; ONS and counter edges arm and timers reset so first-scan pulses match the controller
- ST no longer accepts TRUE/FALSE literals, matching Logix®: BOOL values are 1 or 0
- ST AND/OR/XOR/NOT are bitwise on numeric operands, matching Logix®; & synonym pinned; bitwise legal in subscripts
- CTUD baselines its edge memory on first execution, so an enable already high never counts as a rise
- Centralize data-type categories, ranges, and promotion rules in one registry
- Fix DINT math to wrap at 32 bits like a real controller, including MUL overflow and mid-expression results
- Analyzers and codegen read instruction operands from the per-language registry forms
- Show an error when a ladder timer (TON, TOF, RTO) runs with a negative PRE or ACC
- Runaway ST loops (WHILE/REPEAT/FOR) now stop after 1,000,000 iterations per scan with a clear diagnostic
- Radix numeric literals in ST and Ladder: 16#, 2#, and 8# DINT bit patterns with underscore grouping
- Derive ladder timer, counter, and coil mnemonic sets from the instruction registry
- Move timer and counter instruction semantics into one shared library used by both LD and ST
- Fix EXIT in Structured Text to stop only the innermost loop instead of ending the whole routine
- Catch mistakes in Structured Text math functions like ABS and SIN as you type them instead of when the program runs
- ST `MOD` by zero now returns 0 and `MOD` accepts REAL operands, matching observed Logix controller behavior
- Structured Text timers and counters ignore runtime .ACC writes, matching Logix
- Ladder timer negative-preset fault fires only when the timer times (TON/RTO true rung, TOF false); ACC never faults

## 0.4.2

- Fix ladder Timer Off Delay (TOF) so its output turns off exactly at the preset instead of one scan late
- Run Structured Text timers and counter whenever they are called; setting EnableIn to 0 no longer disables them
- Show the Timer Off Delay with Reset (TOFR) .ACC value counting up to the preset instead of down

## 0.4.1

## 0.4.0

- Warn when an OTE coil and another coil target the same tag in ladder routines.
- Flag every place a timer is reused in a routine, not just the second occurrence.

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
