# Systemd Service Management

Správa Linux služeb pomocí systemctl.

## Basic

Nejpoužívanější systemctl příkazy:

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

```bash
# Zobrazení neúspěšných služeb
systemctl --failed

# Detailní stav služby
systemctl status nginx -l

# Validace syntaxe unit souboru
systemd-analyze verify /etc/systemd/system/myapp.service
```

## Common Mistakes

- Zapomenutí `daemon-reload` po editaci unit souborů.
- Nastavení `Restart=always` bez `RestartSec` — může způsobit restart smyčku.
- Neuvedení `After=network.target` pro síťově závislé služby.
