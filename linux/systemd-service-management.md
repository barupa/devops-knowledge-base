# Systemd Service Management

Správa Linux služeb pomocí `systemctl` a `journalctl`.

## Basic

- Start/stop, enable/disable a reload systemd konfigurace.

```bash
# Zobrazení stavu služby
systemctl status nginx

# Spuštění služby
systemctl start nginx

# Zastavení služby
systemctl stop nginx

# Povolení služby při bootu
systemctl enable nginx

# Zakázání služby při bootu
systemctl disable nginx

# Reload systemd daemon po změně unit souboru
systemctl daemon-reload
```

## Advanced

- Výpis aktivních služeb, závislostí a živých logů.

```bash
# Výpis všech aktivních služeb
systemctl list-units --type=service --state=active

# Zobrazení závislostí služby
systemctl list-dependencies nginx

# Sledování logů služby
journalctl -u nginx -f

# Logy od posledního bootu
journalctl -u nginx -b
```

## Troubleshooting

- Diagnostika failnutých služeb a validace unit souborů.

```bash
# Zobrazení neúspěšných služeb
systemctl --failed

# Detailní stav služby
systemctl status nginx -l

# Validace syntaxe unit souboru
systemd-analyze verify /etc/systemd/system/myapp.service
```

## Common Mistakes

- Po změně unit souboru chybí `daemon-reload`.
- `Restart=always` bez `RestartSec` může vytvořit restart smyčku.
- Pro síťové služby často chybí `After=network.target`.
