# @repo/ladder-syntax

## 0.2.2

- New Ladder Diagram one-input math instructions: ABS, SQRT, and NEG (Math tab), with emulator-verified edge cases
- Add Ladder Logic AND, OR, XOR, NOT bitwise blocks and a Move/Logical toolbar tab
- Add NOP, AFI, and MOD ladder instructions
- Radix numeric literals in ST and Ladder: 16#, 2#, and 8# DINT bit patterns with underscore grouping

## 0.2.1

## 0.2.0

- Unified ST/LD array subscript grammar: shared index-expression form, runtime bounds-fault
- Accept negative scientific REAL literals (`-1.5e1`) in ladder block operands; reject `.5e2` and `+1.5e0`
