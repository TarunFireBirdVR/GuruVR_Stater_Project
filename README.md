🧭 Step-by-Step Guide: GuruVR Metaversity Starter Project

📖 Project Description
The Guru VR Metaversity Starter Project is a Unity-based template designed to kickstart development of immersive, cross-platform VR experiences. Built with scalability in mind, it supports Android, WebGL, and VR headsets like Meta Quest, and comes pre-integrated with Photon PUN2 for multiplayer networking.
Whether you're building a collaborative educational platform, a training simulation, or a multiplayer VR world, this starter kit provides a solid foundation with essential features:

🎮 Multiplayer-ready via Photon
🧍 Full-body avatars for VR users
🧪 XR Simulator for desktop testing without a headset
🧱 Scene management and onboarding tools
⚙️ Preconfigured build support for Android, WebGL, and VR

This guide will walk you through setting up the project, configuring your build targets, and deploying your experience with ease.


🗂️ 1. Download and Extract Project Files
You’ll receive a .zip file of the Guru VR project.
Steps:
Right-click the file → Extract All
Choose a destination folder on your system
Wait for extraction to complete

💻 2. Open Project in Unity
Requirements:
Unity 6000.0.25f1 (LTS) or compatible version
Unity Hub installed

Steps:
Open Unity Hub
Click "Open"
Select "Add project from disk"
Navigate to the extracted project folder and select it
Unity will import the project (this may take a few minutes)

🧪 4. Using the XR Simulator
The XR Device Simulator is enabled by default for development testing.
Controls:
T / Y keys: Simulate controller hand movement
Q / E keys: Simulate the Height of the User
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

🎮 6. Build Settings Configuration
🌐 A. WebGL Build
Go to File > Build Settings
Select WebGL → Click Switch Platform
Click Build and Run or Build

🤖 B. Android Mobile Build (Non-VR)
Go to File > Build Settings
Select Android → Click Switch Platform
In XR Plug-in Management (Android tab), Uncheck:
OpenXR
Oculus
Click Build or Build and Run

🥽 C. VR Build (Meta Quest 2/3S/3)
Switch platform to Android
Go to Edit > Project Settings > XR Plug-in Management
✅ Enable: Oculus
✅ Enable: Initialize XR on Startup

Connect Headset and Click Build and Run  and can also generate an .apk for sideloading onto Meta Quest

📌 Additional Notes
✅ Disable XR Simulator for production builds
✅ Update Room ID uniquely per game/level
🔁 Test UI scaling & interaction separately for Android, WebGL, and VR




