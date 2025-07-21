# 🌪️ SankatMochak - Disaster Management App

**SankatMochak** is a mobile application built using **Kotlin**, **XML**, and **Firebase** that empowers users and authorities to efficiently report and respond to disaster incidents. It facilitates real-time communication, secure user authentication, and centralized incident management to improve disaster response times and coordination.

---

## 📱 Features

* ✅ **User Registration & Login** (Firebase Authentication)
* 🚘 **Incident Reporting** with disaster type, severity, and description
* 📍 **Location-Based Reports** (GPS tagging)
* 🔔 **Real-Time Alerts & Notifications**
* 🗂️ **Admin Dashboard** to monitor and manage incidents
* ☁️ **Cloud Data Storage** using Firebase Realtime Database
* 📷 **Image Uploads** for visual evidence (Firebase Storage)

---

## 🧱 Tech Stack

| Layer       | Technology                       |
| ----------- | -------------------------------- |
| Frontend UI | XML, Kotlin (Android SDK)        |
| Backend     | Firebase Realtime Database       |
| Auth        | Firebase Authentication          |
| Storage     | Firebase Storage                 |
| Push Alerts | Firebase Cloud Messaging (FCM)\* |

> \*If enabled, FCM can be used to send regional alerts.

---

## 📂 Project Structure (Simplified)

```plaintext
SankatMochak/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/sankatmochak/
│   │   │   │   ├── activities/         # Login, Signup, Dashboard
│   │   │   │   ├── adapters/           # Custom adapters for RecyclerViews
│   │   │   │   ├── models/             # Data classes (e.g., User, Incident)
│   │   │   │   ├── utils/              # Firebase helpers, validation
│   │   │   ├── res/
│   │   │   │   ├── layout/             # XML layout files
│   │   │   │   ├── drawable/           # Icons, backgrounds
│   │   │   │   ├── values/             # Colors, styles
├── build.gradle
├── google-services.json               # Firebase config
```

---

## 🚀 Getting Started

### Prerequisites

* Android Studio Arctic Fox or later
* Firebase Project ([https://console.firebase.google.com/](https://console.firebase.google.com/))
* `google-services.json` file added to `/app` directory

### Installation Steps

1. **Clone the repo**

   ```bash
   git clone https://github.com/Vikas9kumargupta/SankatMochak.git
   cd SankatMochak
   ```

2. **Open in Android Studio**

   * File → Open → Select `SankatMochak` directory

3. **Set up Firebase**

   * Enable Email/Phone authentication
   * Create `Incident`, `Users`, and `Reports` collections in Realtime DB
   * Configure Firebase Storage and FCM (optional)

4. **Build & Run the App**

   * Connect your device or emulator
   * Click ▶️ to run the app

---


## 🔒 Firebase Security Rules (Suggested)

```json
{
  "rules": {
    "users": {
      "$uid": {
        ".read": "$uid === auth.uid",
        ".write": "$uid === auth.uid"
      }
    },
    "incidents": {
      ".read": "auth != null",
      ".write": "auth != null"
    }
  }
}
```

---

## 🧑‍💻 Author

**Vikas Kumar Gupta**
💼 [LinkedIn](https://www.linkedin.com/in/work-with-vikas/) | 📂 [GitHub](https://github.com/Vikas9kumargupta)

---

## 📃 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙌 Contributions

Want to improve or contribute? Feel free to fork the repo, open issues, or submit pull requests.
