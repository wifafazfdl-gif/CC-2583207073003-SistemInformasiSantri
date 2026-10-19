# Architecture v0.1

## System Overview
Sistem Informasi Santri adalah aplikasi web untuk mengelola data santri pesantren (tambah, ubah, hapus, cari, dan login pengguna). Pada M03 aplikasi baru dideploy ke satu VPS dan diakses lewat IP publik.

## Deployment View

```mermaid
flowchart TB
    I[Internet]
    F[UFW]
    C[Caddy :80]
    G[Gunicorn 127.0.0.1:8000]
    A[Flask - Sistem Informasi Santri]

    I --> F --> C --> G --> A

## Resource Constraints
- 1 vCPU
- 1 GB RAM
- 20 GB disk
- ubuntu server 24.04
- public IPv4

## Security Decisions
- non-root administration
- SSH key authentication
- password SSH disabled
- UFW enabled
- backend loopback-only
- application managed by systemd
- no secret in repository

## Current Limitations
- HTTP only( login belum terenkripsi, ditngani di m04)
- single VPS
- no database
- no container
- no CI/CD

## Planned Evolution
- M04 DNS + HTTPS
- M05 persistent data
- M06 container
- M07 IaC
- M09 CI/CD
