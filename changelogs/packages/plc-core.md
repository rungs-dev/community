# @repo/plc-core

## 0.11.0

- Reject AOI names that clash with a Logix data type such as `TIMER`, which a controller would refuse
- Every AOI now has EnableIn and EnableOut as built-in parameters

## 0.10.0

- Swap one ladder instruction for another in place — double-click it, then pick the new one from the list

## 0.9.0

- Point deprecated ladder mnemonics at their current name, so `GEQ` now says to use `GE`, and `MOV` to use `MOVE`
- Tell real ladder instructions rungs.dev does not support apart from names that are not instructions at all

## 0.8.0

- Add OSR and OSF one-shot instructions to the Ladder Diagram
- Add OSRI and OSFI one-shot instructions and the FBD_ONESHOT data type to Structured Text
- Allow instruction mnemonics like TON or OSR as tag names and stop AOI names from shadowing built-in instructions

## 0.7.0

- Centralize data-type categories, ranges, and promotion rules in one registry
- Instruction registry rows now carry per-language forms (st/ld), each with its own operands and docs link
- New Ladder Diagram one-input math instructions: ABS, SQRT, and NEG (Math tab), with emulator-verified edge cases
- Add Ladder Logic AND, OR, XOR, NOT bitwise blocks and a Move/Logical toolbar tab
- Add Ladder Logic MVM, CLR, and BTD blocks to the Move/Logical tab
- Add NOP, AFI, and MOD ladder instructions
- Radix numeric literals in ST and Ladder: 16#, 2#, and 8# DINT bit patterns with underscore grouping
- Derive ladder timer, counter, and coil mnemonic sets from the instruction registry
- Catch mistakes in Structured Text math functions like ABS and SIN as you type them instead of when the program runs

## 0.6.0

- Add exercise mode: open a practice exercise with its brief and runnable, locked acceptance tests

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
