# 🧭 GuruVR Metaversity Starter Project

## 📖 Project Description

The **GuruVR Metaversity Starter Project** is a Unity-based template designed to jumpstart development of immersive, cross-platform VR experiences. Built with scalability and ease-of-use in mind, it supports **Android**, **WebGL**, and **VR headsets like Meta Quest**, and comes pre-integrated with **Photon PUN2** for multiplayer networking.

Whether you're building a collaborative educational platform, a training simulation, or a social multiplayer VR world, this starter kit offers a strong foundation with:

- 🎮 Multiplayer-ready setup via Photon PUN2  
- 🧍 Full-body avatars for immersive VR  
- 🧪 XR Simulator for desktop testing without a headset  
- 🧱 Scene management and onboarding UI  
- ⚙️ Preconfigured build support for Android, WebGL, and VR  

---

## 🗂️ 1. Download & Extract Project Files

You will receive the project in `.zip` format.

### Steps:
- Right-click the file → **Extract All**
- Choose a destination folder
- Wait for extraction to complete

---

## 💻 2. Open Project in Unity

### Requirements:
- Unity **6000.0.25f1 (LTS)** or compatible version
- Unity Hub

### Steps:
1. Open **Unity Hub**
2. Click **"Open"**
3. Select **"Add project from disk"**
4. Navigate to the extracted project folder
5. Unity will import the project (may take a few minutes)

---

## 🧪 3. Using the XR Simulator

The XR Device Simulator is enabled by default for development.

### Controls:
- `T / Y` keys → Simulate hand/controller movement  
- `Q / E` keys → Simulate height  
- `WASD + Mouse` → Move around and look

### Toggle XR Simulator:
- Enabled by default for development
- **Disable for production builds** to show full VR avatars

To toggle manually:
- Locate the **XR Device Simulator** GameObject in the Hierarchy
- Enable or disable it as needed

---

## 📝 4. Set Unique Room Name (Multiplayer)

To prevent multiplayer session overlap:

1. Locate the **Room Name** field in your UI or `JoinRoom.cs`
2. Set a **unique room ID**, e.g.:
   - `GameSession_101`
   - `MysteryIsland_Level3`

---

## 🎮 5. Build Settings Configuration

### 🌐 A. WebGL Build
1. Go to `File > Build Settings`
2. Select **WebGL** → Click **Switch Platform**
3. Click **Build and Run** or **Build**

> No XR or simulator plugins needed for WebGL.

---

### 🤖 B. Android Mobile Build (Non-VR)
1. `File > Build Settings` → Select **Android** → **Switch Platform**
2. Go to `Edit > Project Settings > XR Plug-in Management (Android)`
   - ❌ Uncheck **OpenXR**
   - ❌ Uncheck **Oculus**
3. Click **Build and Run** or **Build**

---

### 🥽 C. VR Build (Meta Quest 2/3S/3)
1. Switch platform to **Android**
2. Go to `Edit > Project Settings > XR Plug-in Management`
   - ✅ Enable **Oculus**
   - ✅ Enable **Initialize XR on Startup**
3. Connect your **Meta Quest** headset
4. Click **Build and Run**, or generate `.apk` for sideloading

---

## 📌 Additional Notes

- ✅ **Disable XR Simulator** before final builds  
- ✅ **Update Room ID** for each game/level to isolate multiplayer sessions  
- 🔁 **Test UI and interaction scaling** separately for Android, WebGL, and VR  
- 📦 To **optimize build size**:
  - Remove unused assets
  - Strip debug symbols
  - Use **LZ4HC compression** (Player Settings → Publishing Settings)

---

## 📂 Recommended Folder Structure (Optional)

