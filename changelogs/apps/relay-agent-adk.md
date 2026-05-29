# relay-agent-adk

## 0.0.1

- Collapse the multi-agent architecture into a single agent with flat validator tools — eliminates the cross-sub-agent stale-state bug class and lets the model reason across spec/tests/code in one context.
- Internal: tighten the timer test recipe (require just-below + at-preset boundaries to pin PRE), forbid writing to timer/counter output fields (ACC, DN, EN, TT, etc.), and document the ADK DevUI mid-flight cancellation gap. No user-visible change.
