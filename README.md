# Step Counter Monitoring System

A simple system that collects step counter data from a mobile app, stores it in a Firebase Firestore cloud database, and visualises it via a web dashboard using Chart.js.

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
    ```

5. Connect your physical Android device or emulator.
   ### How to Connect a Physical Android Device

a. **Enable Developer Options on your Android device:**
   - Go to **Settings** > **About phone**.
   - Find **Build number** and tap it **7 times** until you see a message "You are now a developer!"

b. **Enable USB Debugging:**
   - Go back to **Settings**.
   - Open **Developer options** (usually under System or Additional settings).
   - Toggle **USB debugging** to **ON**.

c. **Connect your Android device to your computer:**
   - Use a USB cable to connect the device.

d. **Authorise USB debugging:**
   - When prompted on your phone, tap **Allow** to authorise your computer.

e. **Verify device connection in Android Studio:**
   - Open Android Studio.
   - Click the **Run** button or select **Run > Run 'app'**.
   - In the **Select Deployment Target** window, your device should appear.
   - Select your device and click **OK**.

e. **Run the app:**
   - Android Studio will build and install the app on your physical device.
   - The app will launch automatically on your device.

---

**Troubleshooting:**

- Make sure your device drivers are installed on your computer.
- Try using a different USB cable or USB port if your device is not detected.
- Restart Android Studio or your device if connection issues persist.

---

## ☁️ 2. How to Deploy the Backend API

Backend API is **not used**.

Instead, Firebase Firestore is accessed directly from the mobile app and the web dashboard using Firebase SDK.

No server or backend code is needed for this prototype.

---

## 🌐 3. How to Run the Web Application

### Option 1: Local
- Open `web-app/index.html` in any modern browser.
- Ensure your Firebase config is added correctly in the script tag.
- You will see a live chart of steps pulled from Firestore.

### Option 2: Live Hosting
You can deploy the HTML file using:
- GitHub Pages
- Netlify
- Vercel

Example (Netlify):
1. Go to https://app.netlify.com/
2. Drag and drop `index.html` from `web-app/`
3. Click Publish to go live!

---

## 📦 4. Dependencies & Libraries Used

### Mobile App
- Kotlin
- Android Sensor API
- Firebase Firestore SDK (KTX)

### Web App
- Firebase JS SDK
- Chart.js (via CDN)

---

## 💡 5. Design Choices

- Firebase was selected to simplify cloud setup with native Android and JS SDKs.
- The mobile app uses `Sensor.TYPE_STEP_COUNTER` for accurate step tracking.
- Firestore is used to store step count data with timestamps.
- The web dashboard is a lightweight static app using Chart.js for visualization.
- Added UI/UX features:
  - Total step summary
  - Filtering (all, last 24h, last 7 entries)
  - Responsive and clean layout

---

## 👨‍💻 Developer

Noor Hannani Syamimi binti Mohd Suffian
📧 noorhannanisyamimi@graduate.utm.my
