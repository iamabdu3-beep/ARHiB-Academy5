# ARHiB Academy Operations API

## Instructor
- `GET /api/v1/instructor/courses`
- `POST /api/v1/instructor/courses`
- `POST /api/v1/instructor/courses/:courseId/modules`
- `POST /api/v1/instructor/modules/:moduleId/lessons`
- `GET /api/v1/instructor/courses/:courseId/submissions`
- `PUT /api/v1/instructor/submissions/:submissionId/grade`
- `POST /api/v1/instructor/cohorts`
- `POST /api/v1/instructor/cohorts/:cohortId/sessions`

## Admin
- `GET /api/v1/admin/dashboard`
- `GET /api/v1/admin/users`
- `GET /api/v1/admin/payments`
- `PUT /api/v1/admin/payments/:id/review`
- `GET /api/v1/admin/certificates`
- `PUT /api/v1/admin/certificates/:id/status`
- `GET /api/v1/admin/audit-logs`

All instructor routes require `INSTRUCTOR` or `ADMIN`; admin routes require `ADMIN`.
