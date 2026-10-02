# Production Readiness

## File storage
Development uploads use `FILE_UPLOAD_DIR`. Production should replace `FilesService` storage with S3-compatible object storage and signed URLs; never expose private objects directly.

## Payments
`PaymentsService` keeps provider-specific details behind a small interface. Online providers should verify webhook signatures, enforce idempotency, and update payment state transactionally. Manual payments use the same payment record plus reviewer metadata.

## Notifications
The database notification model is the source of in-app notifications. Email and push adapters can consume the same service events.

## Security
Set strong JWT secrets, HTTPS-only cookies/tokens, restrictive CORS, rate limits, object-storage policies, database backups, audit logging, and production secrets outside source control.
