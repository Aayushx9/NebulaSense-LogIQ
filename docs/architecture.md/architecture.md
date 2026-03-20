# NebulaSense LogIQ — System Architecture
logs → stream → model → score → API → dashboard


```text
        ┌──────────────┐
        │  LogIQ Sim   │
        └──────┬───────┘
               │ logs
               ▼
        ┌──────────────┐
        │ LogIQ Stream │
        └──────┬───────┘
               │ batches
               ▼
        ┌──────────────┐
        │  LogIQ Core  │
        └──────┬───────┘
               │ scores
               ▼
        ┌──────────────┐
        │  LogIQ API   │
        └──────┬───────┘
               │ JSON
               ▼
        ┌──────────────┐
        │ LogIQ View   │
        └──────────────┘
```
