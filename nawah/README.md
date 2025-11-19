<div align="center">

  <img src="assets/images/logo.png" alt="Nawah Healthcare" width="140" height="140" />

  <h1>Nawah Healthcare</h1>

  <p>
    A modern Flutter healthcare platform for consultations, branch discovery, and service booking across MENA.
  </p>

  <p>
    <strong>Status:</strong> 75% complete · QA & regression testing · Booking with multi-payment + social auth in progress
  </p>

  <p>
    <img src="https://img.shields.io/badge/Flutter-3.8+-02569B?logo=flutter&logoColor=white" alt="Flutter" />
    <img src="https://img.shields.io/badge/Dart-3.8+-0175C2?logo=dart&logoColor=white" alt="Dart" />
    <img src="https://img.shields.io/badge/Platforms-Android%20%7C%20iOS-lightgrey" alt="Platforms" />
    <img src="https://img.shields.io/badge/Architecture-Clean-blue" alt="Architecture" />
    <img src="https://img.shields.io/badge/State-BLoC-green" alt="State" />
  </p>

</div>

## Overview

Nawah is a healthcare consultation companion that connects patients with clinics, branches, and specialists. The app delivers bilingual (Arabic/English) experiences, secure consultations with media attachments, dynamic branch/doctor availability, and targeted notifications for offers or follow-ups. The current build mirrors real production scope while we finish QA, add "Book Now" with multi-payment environments, and enable social authentication for faster onboarding.

- Target markets: Egypt · Saudi Arabia · GCC
- Deployment: Android first, iOS build under the same codebase
- Coverage: Consultations, services, branch locator, history, profile, notifications, settings

## Status & Roadmap

- ✅ Core flows: authentication, consultations, services, branches, notifications, localization
- ✅ Internal QA + beta testing (75% of backlog closed)
- 🚧 In progress: Booking & payments (multiple PSP environments), social auth, analytics events
- 🔜 Next: Rich booking summary, Apple Sign-In, provider-side messaging, App Store submission

## Technologies

| Layer | Stack |
|---|---|
| Language | Flutter, Dart |
| State | BLoC (flutter_bloc), Cubits, rxdart |
| Architecture | Clean Architecture (presentation · domain · data) |
| Networking | dio + retrofit + interceptors, connectivity_plus |
| Serialization | freezed, json_serializable, build_runner |
| Storage & Security | flutter_secure_storage, shared_preferences |
| UI/UX | Material 3 theming, flutter_screenutil, shimmer, cached_network_image, custom hero flows |
| Notifications | Firebase Cloud Messaging, flutter_local_notifications, timezone |
| Localization | easy_localization (AR/EN, RTL) |
| Analytics & Logging | Firebase Analytics events, pretty_dio_logger |
| Dependency Injection | get_it / injectable style service locator |

## Screens & Features

- **Splash & Session Restore**: Fast boot, env detection, token refresh, biometric resume
- **Auth**: OTP login/signup, password reset, biometric unlock, (Social auth coming in QA sprint)
- **Consultations**: Attach medical notes/photos, track status, receive responses
- **Services Catalog**: Filtered services with pricing, duration, and prerequisites
- **Branch Finder**: Live branch availability, working hours, map & directions
- **Booking (WIP)**: Pay-now & pay-later options, multi PSP environments, promo codes
- **Notifications**: Deep-linked push topics for offers, consultation updates, system alerts
- **Profile & Settings**: Preferences, language switch (instant RTL), security controls
- **System Reliability**: Offline awareness, retry logic, structured error surfaces

## Highlights

- Clean Architecture separation + feature-first folders for scalability
- Enterprise-grade session & token management with auto-refresh + secure storage
- Modern UX touches: hero motions, skeleton states, shimmer, custom loaders
- Deep localization: Arabic-first typography, mirrored layouts, localized notifications
- QA-ready: logging, analytics hooks, remote config toggles for staged rollouts

## Visual Architecture

```
App (Flutter) — Clean Architecture (presentation · domain · data)
├─ presentation/   # widgets, pages, cubits, UI logic
├─ domain/         # entities, repositories contracts, use-cases
└─ data/           # DTOs, retrofit clients, mappers, local persistence

Cross-cutting: localization, analytics, notifications, payments, error handling
```

## Project Structure (planned)

```
lib/
├─ core/
│  ├─ di/                   # dependency injection (GetIt registrations)
│  ├─ network/              # dio factory, interceptors, retrofit services
│  ├─ localization/         # easy_localization config, translation keys
│  ├─ services/             # firebase, notifications, secure storage
│  ├─ theme/                # colors, typography, Material 3 themes
│  ├─ utils/                # formatters, validators, helpers
│  └─ widgets/              # reusable UI components
├─ features/
│  ├─ auth/                 # login, signup, OTP, biometric, social
│  ├─ onboarding/           # first-run flow
│  ├─ consultations/        # submit, track, history
│  ├─ services/             # catalog, filters, booking hooks
│  ├─ branches/             # branch info, maps, availability
│  ├─ notifications/        # push center & topics
│  ├─ profile/              # user profile, settings, preferences
│  └─ main/                 # navigation shell, tabs
├─ data/                    # static configs, mock payloads
├─ injection_container.dart # GetIt bootstrapping
└─ main.dart                # entry point
```

## Hero Imagery

<table>
  <tr>
    <td><img src="assets/images/headers/header-1.png" alt="Hero 1" width="220" /></td>
    <td><img src="assets/images/headers/header-2.png" alt="Hero 2" width="220" /></td>
    <td><img src="assets/images/headers/header-3.png" alt="Hero 3" width="220" /></td>
  </tr>
  <tr>
    <td><img src="assets/images/headers/header-4.png" alt="Hero 4" width="220" /></td>
    <td><img src="assets/images/headers/header-5.png" alt="Hero 5" width="220" /></td>
    <td></td>
  </tr>
</table>

## Screenshots

<table>
  <tr>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.54.21pm.png" width="210" alt="Screen 1" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.54.35pm.png" width="210" alt="Screen 2" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.54.42pm.png" width="210" alt="Screen 3" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.55.01pm.png" width="210" alt="Screen 4" /></td>
  </tr>
  <tr>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.55.19pm.png" width="210" alt="Screen 5" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.55.27pm.png" width="210" alt="Screen 6" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.55.34pm.png" width="210" alt="Screen 7" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.55.40pm.png" width="210" alt="Screen 8" /></td>
  </tr>
  <tr>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.55.47pm.png" width="210" alt="Screen 9" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.55.59pm.png" width="210" alt="Screen 10" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.56.06pm.png" width="210" alt="Screen 11" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.56.13pm.png" width="210" alt="Screen 12" /></td>
  </tr>
  <tr>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.56.17pm.png" width="210" alt="Screen 13" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.56.22pm.png" width="210" alt="Screen 14" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.57.14pm.png" width="210" alt="Screen 15" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.57.20pm.png" width="210" alt="Screen 16" /></td>
  </tr>
  <tr>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.57.33pm.png" width="210" alt="Screen 17" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.57.44pm.png" width="210" alt="Screen 18" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.57.49pm.png" width="210" alt="Screen 19" /></td>
    <td><img src="assets/images/screenshots/screenshot-2025-11-19-2.57.56pm.png" width="210" alt="Screen 20" /></td>
  </tr>
</table>

## Demos (GIF Previews)

> Tip: GIFs may take a moment to load. If playback is slow, open them directly from the repo under `assets/demos/gifs/`.

### Onboarding
<img src="assets/demos/gifs/onboarding.gif" alt="Onboarding demo" width="360" />

### Main Navigation
<img src="assets/demos/gifs/main-screens.gif" alt="Main screens demo" width="360" />

### Consultations & Services
<img src="assets/demos/gifs/consultant.gif" alt="Consultation demo" width="360" />

### Branches & Services
<img src="assets/demos/gifs/branches-and-branch.gif" alt="Branches demo" width="360" />

### Auth Flow
<img src="assets/demos/gifs/auth.gif" alt="Auth demo" width="360" />

### Settings & Localization
<img src="assets/demos/gifs/settings.gif" alt="Settings demo" width="360" />

### Services Carousel
<img src="assets/demos/gifs/services.gif" alt="Services demo" width="360" />

## Contact

- Email: <a href="mailto:eng.ashrf100@gmail.com?subject=Nawah%20Inquiry">eng.ashrf100@gmail.com</a>
- WhatsApp: <a href="https://wa.me/201287200535" target="_blank">+20 128 720 0535</a>
- Phone: <a href="tel:+201287200535">+20 128 720 0535</a>

---

Nawah sits alongside other Flutter portfolio entries in this repository. Add new assets or update screenshots by dropping media into `assets/` and referencing them here for a clean, repeatable presentation.
