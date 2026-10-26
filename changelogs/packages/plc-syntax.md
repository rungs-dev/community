# @repo/plc-syntax

## 0.3.3

- Renaming a tag changes only its uses in ST, LD and tests, never the same word in a comment or quoted text
- Structured Text reports each syntax error once, and explains a `VAR` block, a time literal such as `T#5s` or a named argument
- Add `STRING` tags, text in quotes, and the string instructions, such as `CONCAT`, `FIND`, `MID`, `DTOS` and `STOD`
- Add `SWPB`, which puts the bytes of an `INT` or `DINT` in a new order, in Ladder and Structured Text
- The Status panel shows each ladder rung Studio cannot read, by its number and with its text

## 0.3.2

- Errors for instructions Studio doesn't have, such as `R_TRIG`, `MAX` or `ATN`, now say what to use instead

## 0.3.1

- Ladder error messages name the tag or instruction at fault and say how to fix it

## 0.3.0

- Add CPT and CMP — write a whole formula in one ladder box instead of chaining math instructions
- Add IsINF and IsNAN to the Compare tab — catch a REAL that has turned into infinity or "not a number"

## 0.2.4

- Point deprecated ladder mnemonics at their current name, so `GEQ` now says to use `GE`, and `MOV` to use `MOVE`
- Tell real ladder instructions rungs.dev does not support apart from names that are not instructions at all

## 0.2.2

- New Ladder Diagram one-input math instructions: ABS, SQRT, and NEG (Math tab), with emulator-verified edge cases
- Add Ladder Logic AND, OR, XOR, NOT bitwise blocks and a Move/Logical toolbar tab
- Add NOP, AFI, and MOD ladder instructions
- Radix numeric literals in ST and Ladder: 16#, 2#, and 8# DINT bit patterns with underscore grouping

## 0.2.0

- Unified ST/LD array subscript grammar: shared index-expression form, runtime bounds-fault
- Accept negative scientific REAL literals (`-1.5e1`) in ladder block operands; reject `.5e2` and `+1.5e0`
