# Prometheus

Metrics collection and time-series database for platform monitoring.

**URL:** https://prometheus.agnxxt.com

## Features

- Scrapes metrics from all platform services
- 15-day data retention
- PromQL query language
- Service discovery via Docker labels

## Configuration

- Config: `/home/ubuntu/platform/monitoring/prometheus.yml`
- Storage: `/prometheus` volume
- Retention: 15 days
- Port: 9090

## Source

- Upstream: [prometheus/prometheus](https://github.com/prometheus/prometheus)
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
