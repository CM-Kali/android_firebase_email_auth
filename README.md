🔥 Firebase Authentication App (Java Android)

A simple Android app that demonstrates Firebase Email & Password Authentication using Java.
The app includes:

A Registration Screen for new users

A Login Screen for existing users

A Main Page that users reach after successful authentication

Optional Splash Screen for startup animation

📱 Features

✅ User Registration (with Firebase Authentication)
✅ User Login (email & password)
✅ Auto-login if user already signed in
✅ Simple & clean UI using XML layouts
✅ Toast messages and progress bar feedback
✅ Firebase integration through google-services.json

🧰 Tech Stack
Component	Description
Language	Java
Framework	Android SDK
Backend	Firebase Authentication
IDE	Android Studio
Min SDK	26
Target SDK	34
📂 Project Structure
app/
├── java/com/example/firebase_auth/
│   ├── registration.java     # Handles user signup
│   ├── login.java            # Handles user login
│   ├── MainActivity.java     # Landing page after login
│   └── SplashActivity.java   # (Optional) Splash screen
│
├── res/layout/
│   ├── activity_registration.xml
│   ├── activity_login.xml
│   ├── activity_main.xml
│   └── activity_splash.xml
│
├── AndroidManifest.xml
└── google-services.json       # Firebase configuration file

⚙️ Setup Instructions
1️⃣ Prerequisites

Android Studio installed

Google account

Internet connection

2️⃣ Create Firebase Project

Go to Firebase Console

Click Add Project → Give it a name → Continue

Click Add App → Android

Enter your package name (e.g., com.example.firebase_auth)

Download the google-services.json file

Place it in your project under:

app/google-services.json


Enable Email/Password Authentication:

Go to Firebase Console → Authentication → Sign-in method

Enable Email/Password

3️⃣ Add Dependencies

In your app/build.gradle:

plugins {
    id 'com.android.application'
    id 'com.google.gms.google-services'
}

android {
    compileSdk 34
    defaultConfig {
        applicationId "com.example.firebase_auth"
        minSdk 26
        targetSdk 34
        versionCode 1
        versionName "1.0"
    }
}

dependencies {
    implementation 'com.google.firebase:firebase-auth:22.3.0'
    implementation 'com.google.android.gms:play-services-auth:21.1.0'
}


In your project-level build.gradle:

classpath 'com.google.gms:google-services:4.4.2'

4️⃣ Add Internet Permission

In AndroidManifest.xml, add before <application>:

<uses-permission android:name="android.permission.INTERNET" />

5️⃣ Run the App

Connect an emulator or physical device

Click ▶️ Run in Android Studio

Register a new account → Login → Enjoy 🎉

🚀 Screens Flow
Screen	Function
SplashActivity	Shows app logo briefly on launch
registration.java	Register a new Firebase user
login.java	Log in existing users
MainActivity.java	Welcome screen for logged-in users
🐞 Troubleshooting

App crashes on start:
→ Ensure mAuth = FirebaseAuth.getInstance(); is initialized before using getCurrentUser()

Authentication failed:
→ Check if Email/Password sign-in is enabled in Firebase Console

No network:
→ Verify <uses-permission android:name="android.permission.INTERNET" />

google-services.json missing:
→ Re-download from Firebase Console and place it in /app

👨‍💻 Author

CMADEEL
📧 Email: madeel466466@gmail.com
]
💻 GitHub: https://github.com/CM-Kali

🧡 License

This project is open-source and free to use for learning or personal projects.
