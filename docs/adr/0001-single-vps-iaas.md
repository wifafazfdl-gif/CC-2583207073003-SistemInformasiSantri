# ADR-0001: Single VPS (IaaS) untuk SISANTRI

Status: Diterima (24-10-2026)

## Konteks
SISANTRI melayani 3-10 pengguna dengan anggaran terbatas
(kredit Azure for Students).

## Keputusan
Memakai satu VM Ubuntu di Microsoft Azure (model IaaS,
public cloud), bukan PaaS atau layanan terkelola.

## Alternatif yang ditolak
- PaaS/managed: lebih mahal dan kontrol lebih sedikit.
- Manual/spreadsheet: tidak memenuhi tujuan praktikum.

## Konsekuensi
- Kontrol penuh dan biaya rendah.
- Patch, backup, dan keamanan jadi tanggung jawab sendiri.
- Single point of failure; mitigasi: backup eksternal.
