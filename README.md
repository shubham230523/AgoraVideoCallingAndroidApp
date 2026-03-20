# AgoraVideoCallingAndroidApp 📹📱

A high-performance Android application that enables real-time 1-on-1 and group video communication. Built using the **Agora Video SDK**, this project demonstrates how to implement low-latency video streaming, handle dynamic permissions, and manage real-time event listeners in a mobile environment.

---

## 🎯 Project Overview

This app serves as a reference implementation for integrating **Real-Time Engagement (RTE)** features into Android. It focuses on:
* **Low Latency:** Leveraging Agora's SD-RTN™ (Software Defined Real-time Network) for global connectivity.
* **Scalability:** Transitioning from 1-on-1 chats to group conferencing with minimal overhead.
* **Security:** Using App IDs and Token-based authentication to secure communication channels.

---

## 🌟 Key Features

* **Instant Video Calling:** Join channels by entering a unique string name to start a video session.
* **Real-time Event Handling:** Automatic UI updates when users join or leave a channel.
* **Camera & Audio Controls:** Toggle microphone (mute/unmute) and switch between front and rear cameras mid-call.
* **Local & Remote Previews:** Dynamic rendering of the local user's camera feed and remote participants' streams.
* **Permission Management:** Robust handling of Android runtime permissions for Camera and Microphone.

---

## 🛠 Tech Stack

| Category | Technology |
| :--- | :--- |
| **Language** | Kotlin / Java |
| **Video SDK** | Agora Video SDK (RTC Engine) |
| **Architecture** | MVC / MVVM |
| **UI Components** | SurfaceView / TextureView for Video Rendering |
| **Build Tool** | Gradle |

---

## 🚀 Setup & Installation

### Prerequisites
1.  **Agora Developer Account:** Sign up at [agora.io](https://console.agora.io/) and create a project to get your **App ID**.
2.  **Android Studio:** Version 3.3 or higher.
3.  **Physical Device:** Real Android device is recommended for testing camera/mic functionality.

### Steps to Run
1.  **Clone the repo:**
    ```bash
    git clone https://github.com/shubham230523/AgoraVideoCallingAndroidApp.git
    ```
2.  **Add your Credentials:**
    Open `strings.xml` or your configuration file and replace the placeholders:
    ```xml
    <string name="agora_app_id">YOUR_APP_ID_HERE</string>
    <string name="agora_access_token">YOUR_TEMP_TOKEN_HERE</string>
    ```
3.  **Build and Deploy:**
    Sync Gradle and run the app on your physical device.

---

## 🏗 Implementation Details

The core logic follows the standard Agora lifecycle:
1.  **Initialize:** Create the `RtcEngine` instance with your App ID.
2.  **Setup Video:** Enable the video module and configure the `VideoEncoderConfiguration`.
3.  **Join:** Call `joinChannel()` with a token and channel name.
4.  **Render:** Use `setupLocalVideo()` and `setupRemoteVideo(uid)` to bind video streams to UI containers.
5.  **Leave:** Clean up resources by calling `leaveChannel()` and `RtcEngine.destroy()`.

---

## 🤝 Contributing

Contributions to enhance the UI or add features like Screen Sharing or Chat are welcome! Please open an issue first to discuss your ideas.

---

### 👨‍💻 Author
**Shubham**
* [GitHub](https://github.com/shubham230523)
