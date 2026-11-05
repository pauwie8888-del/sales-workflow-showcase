# High-level architecture

```mermaid
flowchart LR
  S0["Call notes or transcript"]
  S1["Extract and review editable notes"]
  S2["Draft and validate proposal"]
  S3["Create seven-slide presentation"]
  S4["Salesperson reviews before sharing"]
  S0 --> S1
  S1 --> S2
  S2 --> S3
  S3 --> S4
```

This is a conceptual view. It omits node configuration, API endpoints, prompts and implementation rules. The project README distinguishes live-tested stages from extensions tested with simulated providers.
