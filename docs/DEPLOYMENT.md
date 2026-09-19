# Deployment & Operations Guide: FinTech Core Ledger

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-fintech-core-ledger-45eae2/](/preview/prod-fintech-core-ledger-45eae2/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-19T16:14:48.941749+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=FinTech Core Ledger Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/pytest-of-root/pytest-0/test_products_api_crud_lifecyc0/repo/workspaces/prod-fintech-core-ledger-45eae2
ExecStart=/usr/bin/python3 /tmp/pytest-of-root/pytest-0/test_products_api_crud_lifecyc0/repo/workspaces/prod-fintech-core-ledger-45eae2/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.
