# CC-2583207073003-SistemInformasiSantri

# Sistem Informasi Santri

Cloud Computing — PTI 2802  
Pertemuan 3 — Project Inception

## Author
<Wifa Fazriyatul fadhla> / 2583207073003 / <2A>

## Problem
Pengelolaan data santri di pesantren masih manual sehingga data sulit dicari, rawan salah catat, dan tidak mudah diakses pengurus.

## Target Users
- Admin pesantren
- Ustadz/pengurus

## Features M03
- baseline application
- health endpoint
- VPS deployment

## Architecture

```mermaid
flowchart LR
    U[User] --> C[Caddy]
    C --> G[Gunicorn]
    G --> F[Flask]
```

## Documentation
- [Requirements](docs/requirements.md)
- [Architecture](docs/architecture.md)
- [Manual Deployment](docs/manual-deployment.md)
