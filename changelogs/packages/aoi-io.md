# @repo/aoi-io

## 0.5.0

- Add the Array tab — shift registers, FIFO and LIFO buffers, and whole-array copy, fill, sort, average and search
- Add CPT and CMP — write a whole formula in one ladder box instead of chaining math instructions
- Say why a file will not open instead of loading an empty AOI named ParseError
- Add InOut parameters — arrays and structured tags like TIMER can now be passed to your instruction
- Add SINT and INT tags — 8-bit and 16-bit whole numbers for device registers and byte data
- Timer and counter rungs now read `TON(MyTimer,?,?)`, not `TON(MyTimer)`, matching Logix Designer®
- Fix importing an AOI text file: keep descriptions intact and name the real problem when a tag is rejected
- Fix exported REAL values under the Exponential style to match the value a controller stores

## 0.4.0

- Save an AOI as an .L5X file you can import into Logix Designer®
- Every AOI now has EnableIn and EnableOut as built-in parameters

## 0.3.4

- Allow instruction mnemonics like TON or OSR as tag names and stop AOI names from shadowing built-in instructions

## 0.3.0

- Introduce YAML-based test vectors foir AOIs

## 0.2.2

- Add rung comments

## 0.2.0

- Enhance tag value parsing and validation
- Improve AOI file import/export functionality
- Enhance AOI schema and validation

## 0.1.1

- Fix AOI import/export parser and serializer to support default values for local tags and array elements
- Fix DSL parser logic indentation handling
- Fix DSL import for local tags and numeric defaults

## 0.1.0

- Initial release
