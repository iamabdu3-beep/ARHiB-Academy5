# ARHiB Academy Mobile

Flutter Android student app foundation integrated with the NestJS API.

## Run

```bash
flutter pub get
flutter run --dart-define=API_BASE_URL=https://api.arhibacadamy.com.et/api/v1
```

For a physical Android device, use the LAN address of the development machine instead of `10.0.2.2`.

## Included

- JWT login/session persistence
- Student dashboard and enrollments
- Course/lesson browsing from the API
- Lesson progress updates
- Certificates
- Notifications and mark-read action
- Payment history
- Centralized API client

The backend remains authoritative for enrollment, payment, certificate and assessment state.


## Production Android build

Use the production API explicitly when building release artifacts:

```bash
flutter build apk --release --dart-define=API_BASE_URL=https://api.arhibacadamy.com.et/api/v1
flutter build appbundle --release --dart-define=API_BASE_URL=https://api.arhibacadamy.com.et/api/v1
```
