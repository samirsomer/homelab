# 🏠 Homelab 

> A modular, production‑inspired homelab built using **Docker**
> Designed for learning real‑world DevOps, SRE, and infrastructure
> patterns.



------------------------------------------------------------------------

# 🧱 Architecture Overview

## Layered Model

``` mermaid
flowchart TD
    Shared[(Shared
Data Plane)]
    Infra[(Infra
Control Plane)]
    Obs[(Observability
Passive Plane)]
    Apps[(Applications
Workloads)]

    Infra --> Shared
    Apps --> Shared
    Apps --> Infra

    Obs -. Observes .-> Shared
    Obs -. Observes .-> Infra
    Obs -. Observes .-> Apps
```

### Mental Model

  Layer               Responsibility
  ------------------- ---------------------------
  **Shared**          Owns persistent state
  **Infra**           Controls, secures, routes
  **Observability**   Observes everything
  **Applications**    Business workloads

---------------------------------------------------------


# 🛠 Future Roadmap

-   Dynamic DB credentials via Vault
-   Grafana using Postgres backend
-   Centralized log aggregation
-   OpenTelemetry instrumentation
-   CI/CD integration
-   TLS everywhere


