# distributed-log-analyzer

![Build Status](https://github.com/rainel-projects/distributed-log-analyzer/workflows/CI/badge.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

Kafka-based distributed log analyzer with real-time processing and visualization.

## Architecture

Consumes log events from Kafka topics, processes them for anomalies and patterns, and exposes metrics to Prometheus for Grafana visualization.

## Tech Stack

- **Message Queue**: Apache Kafka
- **Monitoring**: Grafana + Prometheus
- **Processing**: Python consumer
- **Load Testing**: kafkacat, wrk

## Quick Start

### Using Docker Compose (Recommended)

```bash
# Clone the repository
git clone https://github.com/rainel-projects/distributed-log-analyzer.git
cd distributed-log-analyzer

# Start services
docker-compose up -d

# View logs
docker-compose logs -f
```

### View Dashboards
Grafana: http://localhost:3000 (admin/admin)

## Project Structure

```
distributed-log-analyzer/
├── src/              # Source code
├── benchmarks/       # Performance benchmarks
├── docs/             # Documentation
├── Dockerfile        # Container image
├── docker-compose.yml
└── .github/workflows/ # CI/CD pipelines
```

## Benchmarks

Run performance benchmarks:

```bash
cd benchmarks
./bench.sh
```

## Contributing

Contributions welcome! Please open an issue or submit a PR.

## License

MIT License - see LICENSE file for details.
