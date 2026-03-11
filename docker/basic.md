# Docker Základní Příkazy

## Basic
Nejběžnější příkazy pro práci s Dockerem.

* `docker --version`
* `docker run -it ubuntu /bin/bash`
* `docker ps`
* `docker stop <kontejner_id>`
* `docker rm <kontejner_id>`
* `docker images`
* `docker rmi <obraz_id>`

## Advanced
Pokročilé použití Dockeru.

* `docker build -t my_image .`
* `docker tag my_image:latest my_image:v1`
* `docker push my_image:latest`
* `docker pull my_image:latest`
* `docker exec -it <kontejner_id> /bin/bash`

## Troubleshooting
Diagnostika a debug Dockeru.

* `docker logs <kontejner_id>`
* `docker inspect <kontejner_id>`
* `docker system prune`

## Common Mistakes
Typické chyby při použití Dockeru.

* Spuštění kontejneru bez specifikace portů.
* Nepoužití `-it` při spuštění kontejneru pro interaktivní shell.
* Nesprávná konfigurace sítě kontejneru.

## Generování souboru

```bash
mkdir -p docker
cat << 'EOF' > docker/basic.md
# Docker Základní Příkazy
...
EOF
```

## Git Commit

```bash
git add docker/basic.md
git commit -m "docs: add docker basic commands"
```
