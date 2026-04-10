# API Documentation

## Endpoints
### Order Intake
- **Description**: Collect, validate and normalize customer profiles from Sanctions Lists; attach a runId and timestamp for traceability.
- **Type**: Processing

### Generate
- **Description**: Execute generate phase for the Self-Verify pattern: persist interim state, enforce guardrails, and emit structured JSON results.
- **Type**: Processing

### Verify
- **Description**: Execute verify phase for the Self-Verify pattern: persist interim state, enforce guardrails, and emit structured JSON results.
- **Type**: Processing

### Case Management
- **Description**: Case Management across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Limit Control
- **Description**: Limit Control across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Portfolio Check
- **Description**: Portfolio Check across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Operations Handoff
- **Description**: Assemble final payload with status, artifacts, KPIs and audit trail; store to Market Data Feed; return response JSON for the client.
- **Type**: Processing
