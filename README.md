# Step Counter Monitoring System

A simple system that collects step counter data from a mobile app, stores it in a Firebase Firestore cloud database, and visualizes it via a web dashboard using Chart.js.

---

## 📱 1. How to Set Up and Run the Mobile Application

### Prerequisites
- Android Studio installed
- Firebase project created

### Steps
1. Clone or download this repo.
2. Open the `mobile-app/` folder in Android Studio.
3. Add your `google-services.json` file from Firebase to `mobile-app/app/`.
4. Make sure the following dependencies are in `build.gradle`:

```gradle
implementation platform('com.google.firebase:firebase-bom:31.0.1')
implementation 'com.google.firebase:firebase-firestore-ktx'
implementation 'com.google.firebase:firebase-analytics-ktx'
