## LogIQ Score - Anomaly Scoring Specification

The LogIQ Score is a unified anomaly metric designed to quantify how unusual a log sequence is relative to learned normal behavior.

### 1. Inputs
- Embeddings from the preprocessing pipeline
- Reconstruction error from the sequence model
- Temporal deviation metrics
- Service-level context features

### 2. Components
#### a. Reconstruction Error (RE)
Measures how poorly the model reconstructs a sequence.

#### b. Sequence Likelihood (SL)
Probability of the sequence under the learned distribution.

#### c. Temporal Drift (TD)
Deviation from expected timing patterns.

#### d. Service Context Deviation (SCD)
Deviation from normal behavior for the specific microservice.

### 3. Final Score
The LogIQ Score is a weighted combination:
LogIQ Score = α·RE + β·(1−SL) + γ·TD + δ·SCD

Higher scores indicate higher anomaly likelihood.

### 4. Output
- Raw score
- Normalized score (0–100)
- Severity label (Low, Medium, High, Critical)
