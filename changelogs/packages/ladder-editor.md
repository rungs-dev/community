# @repo/ladder-editor

## 0.11.1

- Align rung numbers with their wires, reposition diagnostic badges, and improve the End rung label

## 0.11.0

- Add drag-and-drop editing for ladder branches and multi-instruction selections.
- Add a draggable branch-level tool; toolbar drags preview the real rung, branch, and level shapes
- Hold ⌥ (macOS) or Ctrl to copy instead of move while dragging ladder elements
- On touch, a long-press starts a drag when moved and opens the context menu when released in place
- Remove dead code and merge duplicated instruction editing logic; no user-visible change
- Use Studio on phones and tablets: sidebars fold into drawers and the ladder editor supports touch editing

## 0.10.1

- Complete instruction and direct tag suggestions without interrupting keyboard navigation.
- Improve Tab and arrow-key editing across nested ladder instructions, and focus the first operand after insertion.
- Scope tag actions to the operand that opened the menu, restore ladder focus after tag creation, and hide diagnostics while inline controls are active.
- Remove the F2 shortcut for single-operand editing. Use Enter or type directly to edit an operand.

## 0.10.0

- Swap one ladder instruction for another in place — double-click it, then pick the new one from the list

## 0.9.0

- StaticLadderDiagram accepts tagValues to show preset and accumulator values inside static diagrams
- Show preset and accumulator values inside the timer and counter blocks on the ladder instruction pages

## 0.8.0

- Add OSR and OSF one-shot instructions to the Ladder Diagram

## 0.7.0

- New Ladder Diagram one-input math instructions: ABS, SQRT, and NEG (Math tab), with emulator-verified edge cases
- Add Ladder Logic AND, OR, XOR, NOT bitwise blocks and a Move/Logical toolbar tab
- Add Ladder Logic MVM, CLR, and BTD blocks to the Move/Logical tab
- Add NOP, AFI, and MOD ladder instructions
- Radix numeric literals in ST and Ladder: 16#, 2#, and 8# DINT bit patterns with underscore grouping

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
