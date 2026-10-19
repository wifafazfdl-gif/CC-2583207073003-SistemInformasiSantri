# Requirements

## Problem Statement
Pengelolaan data santri di pesantren masih dilakukan secara manual sehingga data sulit dicari, rawan salah catat, dan tidak mudah diakses oleh pengurus. Sistem Informasi Santri dibutuhkan untuk menyimpan dan mengelola data santri secara terpusat melalui aplikasi web yang dapat diakses lewat internet.

## Target Users
- Admin pesantren
- Ustadz/pengurus

## Functional Requirements
- FR-01 admin dapat menambah data santri
- FR-02 admin dapat mengubah dan menghapus data santri
- FR-03 pengguna harus login akun/email terlebih dahulu
- FR-04 pengguna dapat melihat daftar santri
- FR-05 pengguna dapat mencari santri berdasarkan nama atau NIS
- FR-06 sistem menyediakan endpoint /health untuk pengecekan status aplikasi

## Non-Functional Requirements
- NFR-01 backend loopback-only
- NFR-02 application managed by systemd
- NFR-03 public request through reverse proxy
- NFR-04 no secret in repository

## Constraints
- 1 vCPU
- 1 GB RAM
- 20 GB disk
- Ubuntu Server 24.04
- public IPv4

## Acceptance Criteria M03
- [ ] first deployment accessible
- [ ] health endpoint works
