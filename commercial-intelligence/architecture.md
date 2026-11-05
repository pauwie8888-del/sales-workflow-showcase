# High-level architecture

```mermaid
flowchart LR
  S0["Manual research request"]
  S1["Retrieve company sources"]
  S2["Check evidence and coverage"]
  S3["Assess relevance or hold"]
  S4["Review report and research history"]
  S0 --> S1
  S1 --> S2
  S2 --> S3
  S3 --> S4
```

This is a conceptual view. It omits node configuration, API endpoints, prompts and implementation rules. The project README distinguishes live-tested stages from extensions tested with simulated providers.
