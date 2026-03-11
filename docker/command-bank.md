# Docker Command Bank

Automaticky generovaná banka příkazů z LLM odpovědí (AnythingLLM/Gemini).
Agent deduplikuje příkazy napříč celou knowledge base.

## Basic

<!-- Příkazy pro běžné použití -->

```bash
docker-compose up -d
docker --version
docker run -it ubuntu /bin/bash
docker ps
docker stop <kontejner_id>
docker rm <kontejner_id>
docker images
docker rmi <obraz_id>
docker build -t my_image .
docker tag my_image:latest my_image:v1
docker push my_image:latest
docker pull my_image:latest
docker exec -it <kontejner_id> /bin/bash
docker logs <kontejner_id>
docker inspect <kontejner_id>
docker system prune
```
## Advanced

<!-- Volitelné pokročilé příkazy -->

## Troubleshooting

<!-- Diagnostické a opravné kroky -->

## Common Mistakes

<!-- Časté chyby a anti-patterny -->
