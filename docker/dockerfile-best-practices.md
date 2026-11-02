# Dockerfile Best Practices

Průvodce psaním efektivních a bezpečných Dockerfilů.

## Basic

- Build, run a základní životní cyklus kontejneru.

```bash
# Sestavení image
docker build -t myapp:latest .

# Spuštění kontejneru
docker run -d -p 8080:80 --name myapp myapp:latest

# Výpis běžících kontejnerů
docker ps

# Zastavení kontejneru
docker stop myapp

# Smazání kontejneru
docker rm myapp
```

## Advanced

- Diagnostika image a práce s build stages.

```bash
# Sestavení pouze produkční stage
docker build --target production -t myapp:prod .

# Prohlídka vrstev image
docker history myapp:latest

# Kontrola velikosti image
docker images myapp:latest
```

## Troubleshooting

- Logy, inspekce a shell uvnitř běžícího kontejneru.

```bash
# Zobrazení logů kontejneru
docker logs myapp

# Sledování logů v reálném čase
docker logs -f myapp

# Inspekce stavu kontejneru
docker inspect myapp

# Spuštění příkazu v běžícím kontejneru
docker exec -it myapp /bin/sh
```

## Common Mistakes

- Nepoužívejte `latest` v produkci, pinujte verze.
- Nespouštějte app jako root (`USER`).
- Udržujte `.dockerignore` aktuální.
- Nezahrnujte zbytečný build kontext do `COPY`.
