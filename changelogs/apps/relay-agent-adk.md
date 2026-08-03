# relay-agent-adk

## 0.0.6

- Make timers keep accurate time when scans run late, modeled on measured ControlLogix® behavior

## 0.0.4

- Tighten exercise-builder prompt: honest test names, nonzero input defaults, full-cycle tests for stateful outputs
- Count `hold` assertions toward output coverage so tests asserting an output only via `hold` are accepted
- Add `hold` to AOI unit tests — assert outputs keep their value on every scan of a step
- Run AOI tests through one shared runner everywhere — `runTestVectors` is now async with a pluggable executor

## 0.0.3

## 0.0.2

- Generate exercises whose Cfg\_ defaults, spec, and test values agree, and use time-based waits for timer tests

## 0.0.1

- Collapse the multi-agent architecture into a single agent with flat validator tools — eliminates the cross-sub-agent stale-state bug class and lets the model reason across spec/tests/code in one context.
- Internal: tighten the timer test recipe (require just-below + at-preset boundaries to pin PRE), forbid writing to timer/counter output fields (ACC, DN, EN, TT, etc.), and document the ADK DevUI mid-flight cancellation gap. No user-visible change.
