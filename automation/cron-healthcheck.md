# Cron Healthcheck

## Basic

- Ověření, že cron běží a úlohy jsou nahrané.

```bash
crontab -l
systemctl status cron
```

## Troubleshooting

- Rychlá kontrola, jestli se cron joby opravdu spouští.

```bash
grep CRON /var/log/syslog
```

## Common Mistakes
- Chybí absolutní cesty v cron scriptu.
- Chybí přesměrování stdout/stderr do logu.
