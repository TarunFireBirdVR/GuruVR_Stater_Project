🧭 Step-by-Step Guide: Guru VR Metaversity Starter Project
🗂️ 1. Extract Project Files
You’ll receive a .zip file of the Guru VR project.

Steps:
Right-click the file → Extract All

Choose a destination folder on your system

Wait for extraction to complete

💻 2. Open Project in Unity
Requirements:
Unity 2023.3.0f1 (LTS) or compatible version

Unity Hub installed

Steps:
Open Unity Hub

Click "Open"

Select "Add project from disk"

Navigate to the extracted project folder and select it

Unity will import the project (this may take a few minutes)

🏗️ 3. Project Overview
This template is ready-to-use with the following pre-configured features:

Feature	Description
✅ Multiplayer Support	Photon integration is pre-set for cross-platform networking
✅ XR Simulator	Simulate VR inputs using keyboard/mouse
✅ Avatar System	Includes VR full-body avatars and third-person controls
✅ VR-ready Scene	Optimized for Android VR and PC-based XR

No need to import additional packages unless extending functionality.

🧪 4. Using the XR Simulator
The XR Device Simulator is enabled by default for development testing.

Controls:
T / Y keys: Simulate controller hand movement

Mouse + WASD: Move and look around

Toggle Simulator:
Enable during development

Disable before production to show full VR avatars

To toggle:

Locate XR Device Simulator GameObject in the hierarchy

Enable/Disable as needed

📝 5. Set Unique Room Name (Multiplayer)
To avoid collisions between multiplayer sessions:

Find the Room Name input field in your Lobby UI or script (e.g., JoinRoom.cs)

Set a unique room ID, such as:

GameSession_101

MysteryIsland_Level3

Ensure all participants use the same ID to connect in Photon

🎮 6. Build Settings Configuration
🌐 A. WebGL Build
Go to File > Build Settings

Select WebGL → Click Switch Platform

Disable XR:

Edit > Project Settings > XR Plug-in Management

Uncheck Initialize XR on Startup and other plugins

Ensure XR Simulator is OFF

Click Build and Run or Build

🤖 B. Android Build (Non-VR)
Go to File > Build Settings

Select Android → Click Switch Platform

In XR Plug-in Management (Android tab), Uncheck:

OpenXR

Oculus

In Player Settings > Resolution and Presentation, configure:

Company Name

Package Name (e.g., com.guruvr.project)

Click Build or Build and Run

🥽 C. VR Build (Meta Quest / Android VR)
Switch platform to Android

Go to Edit > Project Settings > XR Plug-in Management

✅ Enable: OpenXR

✅ Enable: Initialize XR on Startup

Under OpenXR settings: Set Oculus as runtime

Go to Player Settings > Other Settings:

Set Minimum API Level to Android 10+

Use Graphics API: Vulkan or OpenGLES3

Click Build to generate an .apk for sideloading onto Meta Quest

📌 Additional Notes
✅ Disable XR Simulator for production builds
✅ Update Room ID uniquely per game/level
🔁 Test UI scaling & interaction separately for Android, WebGL, and VR
📦 Optimize build size:

Remove unused assets

Strip debug symbols

Use LZ4HC compression in Player Settings

📂 Recommended Folder Structure (Optional)
Copy
Edit
GuruVRProject/
├── Assets/
│   ├── Photon/
│   ├── XR/
│   ├── UI/
│   ├── Scripts/
│   └── Scenes/
├── ProjectSettings/
├── Packages/
└── README.md
