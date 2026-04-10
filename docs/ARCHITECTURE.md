# Architecture Documentation

## Overview
This Self-Verify implements Retail Banking Collateral Limit Manager for Banking & Finance use cases.

## Components
1. **Order Intake**: Collect, validate and normalize customer profiles from Sanctions Lists; attach a runId and timestamp for traceability.
2. **Generate**: Execute generate phase for the Self-Verify pattern: persist interim state, enforce guardrails, and emit structured JSON results.
3. **Verify**: Execute verify phase for the Self-Verify pattern: persist interim state, enforce guardrails, and emit structured JSON results.
4. **Case Management**: Case Management across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
5. **Limit Control**: Limit Control across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
6. **Portfolio Check**: Portfolio Check across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
7. **Operations Handoff**: Assemble final payload with status, artifacts, KPIs and audit trail; store to Market Data Feed; return response JSON for the client.

## Data Flow
- Input: Order Intake
- Processing: 7 sequential steps
- Output: Operations Handoff
