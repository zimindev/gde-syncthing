## 🧭 Syncthing Setup Guide

### ✅ What is Syncthing?
Syncthing is a free, decentralized file synchronization tool that lets you sync files between devices securely — no cloud involved.

---

### 🖥️ Step 1: Install Syncthing

#### **Linux (Debian/Ubuntu):**
```bash
sudo apt install syncthing
```

#### **Arch Linux:**
```bash
sudo pacman -S syncthing
```

#### **Windows:**
- Download the installer from: https://syncthing.net/downloads/
- Extract the folder and run `syncthing.exe`.

#### **macOS:**
```bash
brew install syncthing
```

---

### 🚀 Step 2: Start Syncthing

#### **Linux:**
```bash
syncthing
```

Or run it as a systemd service:
```bash
systemctl --user enable syncthing
systemctl --user start syncthing
```

#### **Windows/macOS:**
Just run `syncthing.exe` or use the app shortcut.

---

### 🌐 Step 3: Access the Web Interface

- Open your browser and go to:
  ```
  http://localhost:8384
  ```

---

### 🔗 Step 4: Link Devices

1. On Device A, go to the **Web UI > Actions > Show ID** — copy this **Device ID**.
2. On Device B, open Syncthing and click **“Add Remote Device”**.
3. Paste the Device ID from Device A.
4. Set a name and optional folder sharing preferences.
5. Accept the pairing on the other device.

---

### 📁 Step 5: Share Folders

1. In Syncthing, click **“Add Folder”**.
2. Set a **Folder Label** and **Folder Path**.
3. Choose which **Remote Devices** to share with.
4. On the other device, accept the folder share and set its local path.

---

### 🔒 Optional: Enable GUI Authentication

Go to **Settings > GUI**:
- Enable `GUI Authentication`
- Set a **username and password**

---

### 🔄 Optional: Auto-start Syncthing on Boot

**Linux (Systemd user service):**
```bash
systemctl --user enable syncthing
```

**Windows:**
- Add Syncthing shortcut to Startup folder.

---

### 📦 Bonus: Sync over LAN only
- Go to **Settings > Connections**:
  - Disable “Global Discovery” and “Relay”.
  - Keep only “Local Discovery” checked if you want LAN-only syncing.

---

### 📱 Mobile
- Install the **Syncthing app** from Google Play or F-Droid.
- Pair your phone like any other device.
