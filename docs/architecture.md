# Architecture

This section details the high-level architecture and service dependencies of the **Jo3** cluster.

## Service Dependency Map

The following diagram illustrates the relationships between the core infrastructure, observability stack, productivity tools, and AI services.

```mermaid
graph TD
    %% Core Infrastructure
    Ingress[Traefik Ingress] --> Apps
    Vault[Vault] -->|Secrets| Apps
    PostgresPrd[(Postgres PRD)] --> Keycloak
    PostgresPrd --> Docspell
    PostgresPrd --> Outline
    PostgresPrd --> Grafana
    
    %% Observability
    InfluxDB[(InfluxDB)] --> GrafanaSBX
    Prometheus[Prometheus] --> GrafanaSBX
    Loki[Loki] --> GrafanaSBX
    OpenObserve[OpenObserve/Zinc] --> GrafanaSBX
    
    %% AI Stack
    Ollama[Ollama] --> OpenWebUI
    Ollama --> LobeChat
    
    %% Productivity
    Redis[(Redis)] --> Paperless
    Redis --> Outline
    
    subgraph "Observability"
        GrafanaSBX[Grafana SBX]
        InfluxDB
        Prometheus
        Loki
        OpenObserve
        Gatus
    end
    
    subgraph "Productivity"
        Paperless
        Docspell
        Outline
        Planka
    end

    subgraph "Security"
        Keycloak
        Vault
    end
```

## Infrastructure Components

- **Traefik Ingress**: Entry point for all HTTP/HTTPS traffic.
- **HashiCorp Vault**: Central secret management.
- **PostgreSQL**: Primary relational database for most applications.
- **Redis**: Caching layer for Paperless and Outline.
