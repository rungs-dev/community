# studio

## 0.4.0

### Minor Changes

- 19a0828: Add Ladder Diagram (LD) programming language
  - Ladder editor with drag-and-drop editing, branch support, and inline parameter editing
  - Full instruction set: bit (XIC, XIO, ONS, OTE, OTL, OTU), timer (TON, TOF, RTO), counter (CTU, CTD), math (ADD, SUB, MUL, DIV), compare (EQ, NE, GT, GE, LT, LE), move (MOV), reset (RES)
  - LD compiler pipeline: lexer, parser, semantic analysis, and JS code generation
  - DSL parser/serializer for ladder diagram persistence
  - Simulation integration with runtime energization highlighting and diagnostics
  - Shared ladder UI component library
  - Example LD AOIs: MotorControl, TrafficLight, TankLevel, Cylinder

### Patch Changes

- Updated dependencies [19a0828]
  - @repo/ladder-editor@0.2.0
  - @repo/plc-compiler@0.2.0
  - @repo/plc-core@0.3.0
  - @repo/aoi-io@0.2.1

## 0.3.5

### Patch Changes

- 8a389cd: Add Example AOIs to the library

## 0.3.4

### Patch Changes

- e6091fe: Replace onboarding UI with automatic AOI bootstrap
- 1bdd209: Open AOI trend when starting simulation only for new users

## 0.3.3

### Patch Changes

- fa36f19: Add PostHog React error tracking
- 32b91ae: Open AOI trend when starting simulation

## 0.3.2

### Patch Changes

- b024152: Add PostHog custom events

## 0.3.1

### Patch Changes

- 825b75d: Implement gate screen for mobile devices

## 0.3.0

### Minor Changes

- 193da57: Implement AOI sharing functionality

### Patch Changes

- 692f1ae: Add dialog for creating AOIs with user-defined names

## 0.2.0

### Minor Changes

- 2257902: Enhance tag value parsing and validation
- f747bfa: Migrate state management from Redux to Zustand
- d213c22: Improve AOI file import/export functionality
- 5fde104: Enhance AOI schema and validation
- b71f693: Integrate Zod for AOI validation

### Patch Changes

- Updated dependencies [2257902]
- Updated dependencies [d213c22]
- Updated dependencies [5fde104]
- Updated dependencies [b71f693]
  - @repo/plc-core@0.2.0
  - @repo/aoi-io@0.2.0

## 0.1.1

### Patch Changes

- 0ba66c8: Fix trend's tooltip and markers positioning
- eb5bafa: Add version info
- 58d55b8: Temporarily disable the local "My AOIs"
- Updated dependencies [0f5dc05]
- Updated dependencies [a8ae6a7]
- Updated dependencies [e5c8289]
  - @repo/plc-core@0.1.1
  - @repo/aoi-io@0.1.1

## 0.1.0

### Minor Changes

- 8d954ba: Initial release

### Patch Changes

- Updated dependencies [8d954ba]
  - @repo/plc-core@0.1.0
  - @repo/aoi-io@0.1.0
  - @repo/ladder-ui@0.1.0
  - @repo/plc-compiler@0.1.0
