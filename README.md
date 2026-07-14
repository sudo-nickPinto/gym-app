# Gym App

Private social fitness app MVP for iOS/Android.

## What This Project Is

Gym App is a friends-first workout sharing app for a private beta (20-50 users).

MVP focus:

- account auth and profiles
- friend requests and private social graph
- workout posts (caption + structured workout, optional media)
- feed, likes, comments, mentions
- device push notifications + in-app notification history
- self-service data export and account deletion

## Current Status

Architecture is approved and committed.
Implementation has not started yet.

## Source-of-Truth Docs

- [docs/SYSTEM_ARCHITECTURE.md](docs/SYSTEM_ARCHITECTURE.md) - implementation architecture authority

## Technical Direction (MVP)

- Mobile: Expo (React Native)
- Backend: NestJS (TypeScript), modular monolith
- Data: PostgreSQL
- Cache/rate limiting: Redis
- Media storage: AWS S3
- Push delivery: Expo Push -> APNs/FCM
- Environments: dev, staging, prod

## What Comes Next

1. Scaffold backend foundation (NestJS app, config, DB connection, migrations).
2. Scaffold mobile foundation (Expo app shell + API client baseline).
3. Implement first vertical slice: Auth + Profile.
4. Add tests (unit/integration/critical-path E2E) and CI checks.
5. Deploy staging baseline and run smoke tests.

## Notes

- Shares are deferred (not MVP).
- Per-account post notifications are included in MVP.
- No commit or push should happen without explicit founder approval.