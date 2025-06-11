# otel-backend-observability

A personal OpenTelemetry backend observability stack using Docker Compose. This project provides a ready-to-use environment for collecting, processing, storing, and visualizing traces, metrics, and logs using the OpenTelemetry Collector, Prometheus, Grafana, Loki, Jaeger, and Zipkin.

## Features

- **OpenTelemetry Collector**: Receives, processes, and exports telemetry data.
- **Prometheus**: Scrapes and stores metrics.
- **Loki & Promtail**: Collects and stores logs from Docker containers.
- **Grafana**: Visualizes metrics, logs, and traces.
- **Jaeger & Zipkin**: Distributed tracing backends.

## Project Structure

```
.
├── docker-compose.yml
├── grafana/
│   └── grafana-datasources.yml
├── log/
│   ├── logs.log
│   ├── metrics.log
│   └── traces.log
├── otel-collector/
│   └── otel-config.yaml
├── prometheus/
│   └── prometheus.yml
├── promtail/
│   └── promtail.yaml
└── README.md
```

## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

### Running the Stack

1. Clone this repository:
    ```sh
    git clone https://github.com/yourusername/otel-backend-observability.git
    cd otel-backend-observability
    ```

2. Start all services:
    ```sh
    docker-compose up -d
    ```

3. Access the UIs:
    - **Grafana**: [http://localhost:3000](http://localhost:3000) (anonymous login enabled)
    - **Prometheus**: [http://localhost:9090](http://localhost:9090)
    - **Jaeger**: [http://localhost:16686](http://localhost:16686)
    - **Zipkin**: [http://localhost:9411](http://localhost:9411)
    - **Loki**: [http://localhost:3100](http://localhost:3100)

## Configuration

- **OpenTelemetry Collector**: [`otel-collector/otel-config.yaml`](otel-collector/otel-config.yaml)
- **Prometheus**: [`prometheus/prometheus.yml`](prometheus/prometheus.yml)
- **Grafana Datasources**: [`grafana/grafana-datasources.yml`](grafana/grafana-datasources.yml)
- **Promtail**: [`promtail/promtail.yaml`](promtail/promtail.yaml)

## Logs and Data

- Logs, metrics, and traces are written to the `log/` directory.
- Promtail collects Docker container logs and ships them to Loki.

## License

This project is licensed under the [GNU GPL v3](LICENSE).

---

Feel free to customize this README for your needs!
