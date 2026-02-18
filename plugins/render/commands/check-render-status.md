---
name: check-render-status
description: Check the health and status of Render services using MCP tools.
---

# Check Render status

1. List services with `list_services()` and identify the target service.
2. Check the latest deploy with `list_deploys(serviceId, limit: 1)` — confirm status is `live`.
3. Scan recent error logs with `list_logs(resource: [serviceId], level: ["error"], limit: 20)`.
4. Check resource usage with `get_metrics(resourceId, metricTypes: ["cpu_usage", "memory_usage"])`.
5. Check response times with `get_metrics(resourceId, metricTypes: ["http_latency"], httpLatencyQuantile: 0.95)`.
6. Report findings: deploy status, error count, CPU/memory utilization, and p95 latency.
