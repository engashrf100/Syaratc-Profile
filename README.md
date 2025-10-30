<div align="center">

  <img src="assets/images/app_icon.jpg" alt="Syaratc Online" width="140" height="140" />

  <h1>Syaratc Online</h1>

  <p>
    Find, finance, and manage cars with a modern, high‑performance Flutter app powered by clean architecture.
  </p>

  <p>
    <a href="https://syaratc.online/en"><img alt="Website" src="https://img.shields.io/badge/Website-syaratc.online-success?logo=google-chrome&logoColor=white"></a>
    <a href="https://play.google.com/store/apps/details?id=com.syatric.app"><img alt="Google Play" src="https://img.shields.io/badge/Google%20Play-com.syatric.app-3DDC84?logo=google-play&logoColor=white"></a>
  </p>

</div>

## Overview

Syaratc Online is a car marketplace and financing companion. The app connects users with curated car offers, financing partners, and company programs while delivering a smooth, localized experience. It mirrors the core capabilities available on the website (`https://syaratc.online/en`) and adds mobile‑first features like push notifications, offline‑first storage, and background token refresh.

### Project Pref

This repository hosts the app profile and demos only (no source code). Use this README on GitHub as a portfolio page to showcase product scope, technology choices, and videos.

## Technologies

| Layer | Technology |
|---|---|
| Language | Flutter, Dart |
| State | BLoC (Cubit) |
| Storage | Hive for local persistence |
| Architecture | Clean Architecture (domain, data, presentation) |
| Networking | API handler with interceptors, pagination, and error mapping |
| Auth | Token auth with OTP; secure refresh token in background; guest and authenticated flows |
| UI/UX | Slivers for performant lists, skeleton loading, onboarding game/flow |
| i18n | Double localization (e.g., Arabic/English) |
| Notifications | Firebase Cloud Messaging + local notifications |
| Web Content | In‑app WebView for Terms and Conditions, Privacy |

## Screens & Features

- **Splash**: cold‑start bootstrap, env/config probing, auth state restore
- **Auth**: login and signup, OTP verification, resend/refresh OTP
- **Forgot Password**: password reset with secure flows
- **Background Token Refresh**: silent refresh for both guest and authenticated sessions
- **Home**: brand search, featured products, performant sliver lists, skeleton loading
- **Offers**: special/featured offers, filters, pagination
- **Order/Form**: guided purchase order form with validation and autosave
- **Companies Offers**: tailored programs for businesses
- **User Profile**: profile view/edit, saved cars, preferences
- **Drawer**: links to Terms & Conditions and Privacy via WebView

## Visual Architecture

```
App (Flutter)
├─ presentation/        # Widgets, pages, BLoC cubits, UI state
├─ domain/              # Entities, repositories (abstract), use‑cases
└─ data/                # DTOs, mappers, Hive boxes, API clients/interceptors

Cross‑cutting: localization, error handling, analytics, notifications
```

## Demo Videos

> All videos are stored locally in this repo under `assets/`. GitHub supports inline playback of `.mov`.

### Home
<video src="assets/home.mov" controls width="720"></video>

### Offers
<video src="assets/OFFERS.mov" controls width="720"></video>

### Onboarding & Auth
<video src="assets/onboarding+auth.mov" controls width="720"></video>

### Form & Drawer
<video src="assets/FORM+DRAWER.mov" controls width="720"></video>

If inline playback doesn’t appear, use these direct links:

- `assets/home.mov`
- `assets/OFFERS.mov`
- `assets/onboarding+auth.mov`
- `assets/FORM+DRAWER.mov`

## Why Syaratc Online?

- **End‑to‑end flow** from discovery to financing
- **Reliable performance** with slivers, pagination, and skeleton loading
- **Production‑ready architecture** (testable, scalable)
- **Localization‑first** experience
- **Engagement** via FCM + local notifications

## Suggestions to Elevate Further

- **Deep Links & App Links** for campaign and offer landing
- **Performance Monitoring** with Firebase Performance and Crashlytics
- **A/B Testing** for onboarding flow and conversion levers
- **Offline‑first Caching** for offers and catalogs
- **Accessibility** pass (text scaling, semantics, contrast)
- **CI/CD** with automated build and store metadata sync

## Open Questions (for kickoff)

1. Do we need Apple App Store targets and review assets now or later?
2. Preferred analytics stack (Firebase Analytics vs. alternative)? Events to track?
3. Exact OTP provider and rate‑limit requirements?
4. Supported locales beyond Arabic/English?
5. API SLA and pagination window sizes for offers/catalogs?

## Getting Started (Profile Repo)

This is a profile/portfolio repository containing assets and documentation only. If you want the full source code or a custom build, please reach out.

---

Made with Flutter • © Syaratc Online


