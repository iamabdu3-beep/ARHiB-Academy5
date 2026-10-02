# ARHiB Academy Architecture

## Applications

- `backend`: NestJS REST API, Prisma, PostgreSQL, Redis integration point.
- `web`: Next.js public website and authenticated student portal.
- `mobile`: Flutter Android application.
- `docs`: API, architecture, product and operational documentation.
- `docker`: local/staging infrastructure definitions.

## API principles

- Versioned REST API under `/api/v1`.
- OpenAPI documentation under `/docs`.
- PostgreSQL is the system of record.
- Object storage is used for large/private learning files.
- Access tokens are short-lived; refresh tokens are hashed and rotated.
- Server remains authoritative for enrollment, payment, assessment results and certificates.
- Localized content uses translation tables with language fallback.

## Delivery phases

1. Foundation, authentication and RBAC
2. Course/catalog/content management
3. Enrollment and learning progress
4. Cohorts and instructor workflows
5. Assessments, assignments and exams
6. Online/manual payments
7. Certificates and verification
8. Notifications, reporting and audit
9. Web portal
10. Android app
11. Security/performance/UAT
12. Production deployment
