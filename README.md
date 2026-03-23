# New Relic Power for Kiro

Production observability power for investigating incidents, debugging performance, and analyzing telemetry in real time. This power enables Kiro AI agents to query New Relic data using NRQL and MCP tools.

## About New Relic

[New Relic](https://newrelic.com/) is an observability platform for monitoring applications, infrastructure, logs, traces, and alerts.

With this power, Kiro can investigate production behavior directly from your IDE by querying New Relic telemetry through an OAuth-based MCP server.

> Note: The New Relic MCP server is currently in preview. Access may require requesting enablement at [mcp.newrelic.com](https://mcp.newrelic.com/).

## Features

- **NRQL-Powered Analysis**: Run flexible NRQL queries over logs, metrics, traces, and events
- **Golden Signals Monitoring**: Analyze latency, traffic, errors, and saturation quickly
- **Incident Investigation Workflows**: Investigate production errors, regressions, and alert spikes
- **Entity-Aware Troubleshooting**: Scope by application, service, host, or entity GUID
- **Alert & Change Correlation**: Connect incidents with deployments and related events
- **AI-First Experience**: Ask natural language questions and let Kiro choose the right tools

## Installation

### Prerequisites

1. **New Relic Account**: Access to a New Relic account
2. **New Relic API Key**: User API key and account ID
3. **MCP Access**: OAuth access to the New Relic MCP server

### Kiro Power Setup

1. Open the Powers panel in Kiro
2. Click **Add power from GitHub**
3. Add this repository
4. Complete OAuth authorization for `https://mcp.newrelic.com/mcp/`

## What can you do with New Relic and Kiro?

### 1 - Investigate Production Errors
Use prompts like:
- Why is `checkout-api` error rate increasing in the last hour?
- Show top `TransactionError` classes affecting production
- Find related logs and traces for timeout errors

### 2 - Analyze Performance Regressions
Use prompts like:
- What endpoints got slower after today’s deployment?
- Compare p95 latency now vs yesterday for `api-service`
- Identify the slowest datastore spans in the last 4 hours

### 3 - Investigate Alerts and Incidents
Use prompts like:
- What critical issues are currently open?
- Summarize likely root cause for this incident
- Correlate recent change events with alert start time

### 4 - Validate Service Health with Golden Signals
Use prompts like:
- Show latency, traffic, errors, and saturation for `checkout-api`
- Which service has the highest error rate right now?
- Trend CPU and memory for hosts behind this service

## Steering Files

The power includes structured steering content in [steering/observability-steering-index.md](steering/observability-steering-index.md), with supporting guides:

- [steering/nrql-guide.md](steering/nrql-guide.md)
- [steering/query-patterns.md](steering/query-patterns.md)
- [steering/troubleshooting-workflows.md](steering/troubleshooting-workflows.md)

## Resources

- **New Relic Docs**: [docs.newrelic.com](https://docs.newrelic.com/docs/agentic-ai/mcp/overview/)
- **MCP Entry Point**: [mcp.newrelic.com](https://mcp.newrelic.com/)
- **NRQL Reference**: [NRQL docs](https://docs.newrelic.com/docs/nrql/get-started/introduction-nrql-new-relics-query-language/)