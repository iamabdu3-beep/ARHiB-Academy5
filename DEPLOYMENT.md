# ARHiB Academy — Deployment Guide

## Staging

1. Copy `docker/.env.staging.example` to `docker/.env.staging`.
2. Replace every placeholder secret and domain.
3. Start the stack:

```bash
docker compose --env-file docker/.env.staging -f docker/docker-compose.staging.yml up -d --build
```

4. Apply Prisma migrations from the backend container using the project's migration workflow.
5. Check `GET /api/v1/health/live` and `GET /api/v1/health/ready`.

## Production requirements

- Terminate TLS at a reverse proxy/load balancer.
- Keep PostgreSQL and Redis private; expose only the web/API entry points.
- Use managed object storage for uploaded learning files and signed URLs for private resources.
- Store secrets in a secret manager rather than Git or compose files.
- Configure database backups and test restoration regularly.
- Configure log aggregation and alerting for readiness failures, payment webhook failures, and authentication anomalies.
- Run migrations as an explicit deployment step; do not silently mutate production schema at application startup.
- Set restrictive CORS origins and review upload MIME/size limits for the actual curriculum.
