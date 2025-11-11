## 🏠 HouseRent App

An Android application for owners, buyers, and renters to buy, rent, and sell houses. The app goes beyond basic listings by offering a real-time chat system, integration with external rental sites, and voice command support for seamless interaction.

---

## ✨ Features🔐 Authentication – Secure login & registration for all users.

🏡 Rental Listings – Post, browse, and manage house rental or sale ads.

💬 Real-Time Chat – Instant messaging(text, audio) between buyers, renters, and owners.

📡 External Integration – View rental posts fetched from other relevant sites.

🎙 Voice Commands – Perform app tasks hands-free via voice interaction.

📂 Media Upload (optional) – Add images to property listings.

⚡ Simple & Clean UI – User-friendly interface for quick navigation.

---

## 🛠 Tech Stack

Language: Kotlin

Database & Auth: Firebase Realtime Database & Firebase Authentication

Messaging: Firebase Cloud Messaging (for chat & notifications)

Storage: Firebase Storage (for media uploads)

Location/Maps: Google Maps SDK (if map features enabled)

Networking: Retrofit / OkHttp (if external API integration is used)

UI: Android XML + ViewBinding

---

## ⚙️ Installation

To set up the project locally:

Clone the repo: git clone https://github.com/wolfy01/HouseRental.git

Open the project in Android Studio

Add your Firebase project and place the google-services.json file in the app/ folder

Enable Firebase Authentication and Realtime Database (plus Storage if using media uploads)

Get a Google Maps API key (if using location features), enable Maps SDK and Directions API in Google Cloud Console, and add it to AndroidManifest.xml

---

## 📌 Roadmap

Add filters for price, location, house type, and amenities.

Implement booking and scheduling system for property visits.

Improve admin tools (moderation, post approval).

Expand external API integration for more rental platforms.

## 👨‍💻 Author

Built by Nihal Azman
