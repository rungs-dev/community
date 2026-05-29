# studio-assist

## 0.1.5

- Teach Relay the `Cfg_` prefix for design-time parameters like preset times and limits, separate from live `In_` inputs
- Teach Relay the real toolbar button names so it stops telling you to click `Start simulation` when you want `Test`
- Make Relay's answers more consistent — its rules now live in one stable place instead of being re-sent on every message
- Teach Relay the PlantPAx tag prefixes (In*, Out*, Sts*, Tmr*, Cnt*, Val*, Wrk\_) so it stops suggesting prefix-less names
- Add exercise mode: open a practice exercise with its brief and runnable, locked acceptance tests

## 0.1.4

- Add an optional Description to your AOI — shown in the print header and surfaced to Relay.
- Stop Relay from suggesting you delete the canned tests on seeded example AOIs.
- Move Studio context out of the system prompt into the user message via a server-rendered `<studio-context>` block.

## 0.1.3

- Relay chat improvements
- Improve how Relay explains scan order, distinguishing the logic scan from the asynchronous I/O update.

## 0.1.2

- Teach Relay the array index expression rules: which forms are allowed and which are rejected.
- Improve Relay agent

## 0.1.1

- Relay assistant improvements
