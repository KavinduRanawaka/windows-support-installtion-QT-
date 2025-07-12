

### 2. 🛠️ Build Instructions

#### ▶️ Option A: Using Qt Creator

1. Open `qt-usb-serial-graph.pro` in Qt Creator.
2. Configure a **Windows kit** (MSVC or MinGW).
3. Click **Build** → **Run**.

#### ▶️ Option B: Manual Build

```bash
git clone https://github.com/yourname/usb-serial-3d-graph.git
cd usb-serial-3d-graph
qmake
make
```

---

## 📦 Creating a Windows Installer

### ✅ Step 1: Build & Deploy

Build your project in **Release Mode**, then use:

```bash
windeployqt release/YourApp.exe
```

> This gathers all required Qt DLLs into your build folder.

---

### ✅ Step 2: Create `.exe` Installer

1. Install [Inno Setup](https://jrsoftware.org/isinfo.php).
2. Use this script (`installer.iss`):

```ini
[Setup]
AppName=USB Serial Visualizer
AppVersion=1.0
DefaultDirName={pf}\USBVisualizer
DefaultGroupName=USBVisualizer
OutputDir=output
OutputBaseFilename=USBVisualizerInstaller

[Files]
Source: "release\*"; DestDir: "{app}"; Flags: ignoreversion recursesubdirs

[Icons]
Name: "{group}\USBVisualizer"; Filename: "{app}\YourApp.exe"
```

3. Open `installer.iss` in Inno Setup Compiler → Click **Build**.

✅ Done! You now have an installer:
`output/USBVisualizerInstaller.exe`

---

## 📁 Project Structure

```bash
.
├── src/
│   ├── main.cpp
│   ├── mainwindow.cpp/.h
│   ├── serialhandler.cpp/.h
│   ├── graphrenderer.cpp/.h
│   ├── threedwindow.cpp/.h
│   └── mainwindow.ui
├── release/
├── screenshots/
├── qt-usb-serial-graph.pro
└── installer.iss
```

---

## ⚖️ License

This project is licensed under the **MIT License**.
Feel free to use, modify, and distribute.

---

## 🙌 Contribution

Have ideas or improvements?
Fork the repo, open a PR, or submit issues.

---

## 👨‍💻 Author

**\[Your Name]**
GitHub: [@yourusername](https://github.com/yourusername)

---

> 💬 *“Simple and effective data visualization for your embedded devices.”*

```

---

Would you like me to save this as a `README.md` file or include example screenshots?
```
