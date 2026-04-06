# Synthetic_Monitoring
Synthetic monitoring is a proactive way of monitoring systems where you simulate user actions (like login, API calls, page loads) using scripts or bots—even when no real users are active.

# Project Layout

## Project Structure

```text
synthetic-monitor/
├── config/
│   └── checks.yaml          # check definitions
├── synmon/
│   ├── __init__.py
│   ├── scheduler.py         # APScheduler-based runner
│   ├── checks/
│   │   ├── http_check.py
│   │   ├── dns_check.py
│   │   ├── tcp_check.py
│   │   └── browser_check.py # Playwright
│   ├── aggregator.py        # normalize + tag results
│   ├── exporter.py          # Prometheus /metrics server
│   ├── alerting.py          # Alertmanager webhook
│   └── state.py             # SQLite result store
├── dashboards/
│   └── grafana.json         # pre-built Grafana dashboard
├── requirements.txt
└── main.py
 
