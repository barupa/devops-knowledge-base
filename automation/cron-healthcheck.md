# Cron Healthcheck

## Basic
```bash
crontab -l
systemctl status cron
```

## Troubleshooting
```bash
grep CRON /var/log/syslog
```

## Common Mistakes
- Zapomenuté absolutní cesty v cron úlohách.
