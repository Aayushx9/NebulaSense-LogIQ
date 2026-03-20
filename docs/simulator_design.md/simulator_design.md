## LogIQ Sim — Microservice Simulator Design

LogIQ Sim generates realistic microservice logs with controllable anomalies to test the full NebulaSense LogIQ pipeline.

### 1. Architecture
The simulator consists of three microservices:
- microservice_a
- microservice_b
- microservice_c

Each service:
- Generates logs at configurable rates
- Emits structured JSON logs
- Includes latency, status codes, payload sizes, and trace IDs

### 2. Anomaly Types
- Latency spikes
- Error bursts (4xx/5xx)
- Payload anomalies
- Sequence disruptions
- Service outages

### 3. Anomaly Injector
The `anomaly_injector.py` module:
- Injects anomalies at random or scheduled intervals
- Supports severity levels
- Ensures reproducibility via seeds

### 4. Log Generator
`generator.py` orchestrates:
- Multi-service log generation
- Trace propagation
- Anomaly scheduling
- Output to file, API, or stream

### 5. Output Format
All logs follow a consistent schema:
- timestamp
- service_name
- trace_id
- latency_ms
- status_code
- payload_size
- anomaly_flag
