# Manual Deployment M03

## Application
Sistem Informasi Santri (Flask + Gunicorn), repo: `CC-2583207073003-SistemInformasiSantri`

## Application Path
`/srv/cc-m03`

## Service
`cc-m03.service`

## Backend
`127.0.0.1:8000` (loopback-only, tidak bisa diakses langsung dari internet)

## Public Endpoint
`http://<PUBLIC_IP>/`

## Update Procedure

```bash
cd /srv/cc-m03
git pull
source .venv/bin/activate
python -m pip install -r requirements.txt
sudo systemctl restart cc-m03
sudo systemctl status cc-m03 --no-pager
curl -fsS http://127.0.0.1:8000/health
curl -fsS http://127.0.0.1/health
```

## Verification
- `systemctl status` menunjukkan `active (running)`
- `/health` di Gunicorn (port 8000) dan di Caddy (port 80) sama-sama merespons
- Halaman utama bisa dibuka dari browser lewat `http://<PUBLIC_IP>/`
