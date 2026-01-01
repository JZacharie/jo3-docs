# Observability Applications

This section outlines the observability stack deployed on the **Jo3** cluster.

## Grafana SBX
- **URL**: `grafana-sbx.p.zacharie.org`
- **Description**: Central dashboarding platform for visualizing metrics and logs.
- **Data Sources**:
    - Prometheus (Metrics)
    - InfluxDB (Sensor data)
    - Loki (Logs)
    - OpenObserve (Alternative Logs)
    - PostgreSQL (Application performance data)

## InfluxDB 2
- **Internal URL**: `192.168.0.115:8086`
- **Description**: Time-series database primarily used for IoT and sensor data storage.

## OpenObserve (Zinc)
- **URL**: `o2-openobserve.p.zacharie.org`
- **Description**: Lightweight observability platform for logs, metrics, and traces.
- **Dependencies**: 
    - PostgreSQL (Metadata)
    - S3 (Data Storage)

## Gatus
- **URL**: `gatus.p.zacharie.org`
- **Description**: Automated service health dashboard. Performs periodic HTTP/TCP health checks against internal and external endpoints.
