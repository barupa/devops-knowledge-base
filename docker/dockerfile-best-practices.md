# Dockerfile Best Practices

Průvodce psaním efektivních a bezpečných Dockerfilů.

## Basic

Základní Docker příkazy:

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

Multi-stage build pro menší image:

```bash
# Sestavení pouze produkční stage
docker build --target production -t myapp:prod .

# Prohlídka vrstev image
docker history myapp:latest

# Kontrola velikosti image
docker images myapp:latest
```

## Troubleshooting

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

- Používání tagu `latest` v produkci — vždy pinujte konkrétní verze.
- Spouštění jako root uvnitř kontejnerů — použijte direktivu `USER`.
- Neuvedení `.dockerignore` — vždy vylučte `node_modules`, `.git` atd.
- Kopírování celého kontextu — používejte specifické cesty v `COPY`.
