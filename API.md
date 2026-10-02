# API Starter Contract

Base path: `/api/v1`

## Auth

- `POST /auth/register`
- `POST /auth/login`
- `POST /auth/refresh`
- `POST /auth/logout`

## User

- `GET /users/me`

## Courses

- `GET /courses?language=en`
- `GET /courses/:id?language=en`

## Enrollment

- `POST /enrollments` with `{ "courseId": "uuid" }`
- `GET /enrollments/me`

## Progress

- `GET /progress/me`
- `PUT /progress/lessons/:lessonId` with `{ "progressPct": 0..100 }`

Swagger is the executable API reference once the backend is running.

## Student learning APIs

- `GET /api/v1/enrollments/me` — current student's enrollments
- `POST /api/v1/enrollments` — enroll in a published course (`courseId`)
- `GET /api/v1/progress/me` — current student's lesson progress
- `PUT /api/v1/progress/lessons/:lessonId` — save progress (`progressPct`: 0–100)
- `GET /api/v1/assessments/course/:courseId` — assessments available in an enrolled course
- `GET /api/v1/assessments/:id` — assessment questions/options
- `POST /api/v1/assessments/:id/attempts` — start an assessment attempt
- `POST /api/v1/assessments/attempts/:attemptId/answers` — save an answer
- `POST /api/v1/assessments/attempts/:attemptId/submit` — submit and score an attempt
- `GET /api/v1/certificates/me` — current student's certificates
- `GET /api/v1/certificates/verify/:code` — public certificate verification
