# HouseRent

A full‑stack Android experience for discovering, listing, and discussing rental properties. HouseRent combines real‑time listings, voice‑first workflows, and map‑based discovery so renters and owners can move from search to conversation in minutes.

## Product Summary 
HouseRent is an Android application that helps owners publish property listings and lets renters or buyers discover them through traditional search, voice search, and location‑aware maps. The app also enables real‑time chat (including voice messages) so users can negotiate and coordinate without leaving the platform. It integrates with external listing sources and brings those posts into the app for broader market visibility.

## Core Functionality
- **Authentication & onboarding**: email/password signup and login for secure access.
- **Property listing creation**: upload details, photos, and geolocation for listings.
- **Voice‑assisted listings**: guided, question‑based posting with speech recognition and text‑to‑speech prompts.
- **Voice search**: speak a request and instantly filter external listings.
- **Real‑time chat**: text and audio messages between renters and owners.
- **External listings ingestion**: scrape and import listings from public sources into Firebase.
- **Map discovery**: show nearby listings on Google Maps with distance filtering and polylines.

## User Flow at a Glance
1. **Sign up / log in**.
2. **Browse listings** (internal and external).
3. **Filter or search via voice**.
4. **Open map view to find nearby properties**.
5. **Chat with a listing owner** (text or voice).
6. **Create a new listing** (manual or voice‑assisted).

## Architecture & Tech Stack
- **Language**: Kotlin
- **UI**: XML layouts + ViewBinding
- **Auth**: Firebase Authentication
- **Data**: Firebase Realtime Database
- **Media**: Firebase Storage
- **Maps & Location**: Google Maps SDK + Fused Location Provider
- **Voice**: Android SpeechRecognizer + Text‑to‑Speech
- **External data ingestion**: Jsoup HTML parsing
- **Image loading**: Picasso

## Engineering Metrics (Build & Platform)
These are the concrete, versioned metrics defined in the build configuration:
- **Compile SDK**: 33
- **Target SDK**: 33
- **Minimum SDK**: 21
- **App Version**: 1.0 (versionCode 1)
- **Java/Kotlin target**: 1.8
- **Enabled build feature**: ViewBinding
- **Test frameworks configured**: JUnit4, AndroidX JUnit, Espresso

## Software Engineering Principles Reflected in the Codebase
The current implementation shows the following practical SWE principles:
- **Separation of concerns by screen**: distinct Activities own individual flows (authentication, posting, chat, maps, voice search/posting).
- **Asynchronous I/O**: Firebase callbacks and coroutines keep network work off the main thread.
- **Input validation and feedback**: user input is checked before submission and feedback is provided via Toasts.
- **Permission‑aware features**: microphone, location, and storage access are gated by runtime permission checks.
- **Reusable data models and adapters**: Post/Chat models and RecyclerView adapters encapsulate UI lists.
- **Dependency transparency**: third‑party services (Firebase, Maps, Jsoup) are explicitly versioned in Gradle.

## Local Setup
1. Clone the repository.
2. Open in Android Studio.
3. Add your Firebase project and place `google-services.json` in `app/`.
4. Enable Firebase Authentication, Realtime Database, and Storage.
5. Add a Google Maps API key to `local.properties` and to the manifest entry.

## Roadmap Ideas
- Filters for price, location, and amenities.
- Property visit scheduling and booking workflows.
- Admin moderation and listing approval.
- More external listing sources and structured ingestion.

## Author
Built by Nihal Azman.
