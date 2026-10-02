# ARHiB Academy Portal Layer

## Instructor
- `/instructor` lists assigned courses and supports course creation.
- `/instructor/courses/[courseId]` supports module/lesson authoring and submission review.
- Requires an access token stored by the login flow and an `INSTRUCTOR` or `ADMIN` role.

## Admin
- `/admin` shows operational dashboard data, users, payments, certificates, and audit-log counts.
- Backend routes are protected by the `ADMIN` role.

## Next integration
1. Add role-aware post-login routing.
2. Add full CRUD editing and publication controls.
3. Add payment/certificate review actions to the admin UI.
4. Add cohort/session scheduling screens.
5. Add file upload UI backed by signed object-storage URLs.
