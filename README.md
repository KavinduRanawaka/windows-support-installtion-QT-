
````markdown
# 🚀 USB/Serial Port Data Visualizer with 3D Display

![Qt](https://img.shields.io/badge/Framework-Qt5%2F6-blue)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Build-Stable-brightgreen)

A modern Qt-based C++ desktop application that reads data from USB or serial ports, plots it in real-time, and visualizes a dynamic 3D rectangle in a separate subwindow.

---

## 🎯 Features

✅ Read data from USB or Serial Ports  
📈 Real-time graphing using **QtCharts**  
🧊 3D subwindow using **Qt3D**  
⚡ Lightweight, fast, and responsive  
📦 Generates a Windows auto-installer (.exe) with all dependencies  
🛠 Clean, modular C++ architecture using **Qt Widgets**

---

## 🖼️ Demo Preview

<img src="screenshots/main_ui.png" alt="Main UI" width="600"/>
<img src="screenshots/3d_window.png" alt="3D Window" width="400"/>

---

## 🧱 Technology Stack

- **Qt Widgets** – UI & layout
- **Qt Serial Port** – USB/COM port communication
- **Qt Charts** – Real-time graph plotting
- **Qt 3D Extras** – 3D rendering of rectangle/cube
- **C++** – Core logic and performance
- **Inno Setup** – Windows installer creation

---

## 🔧 Getting Started

### 1. 🧰 Requirements

Install Qt (5 or 6) using [Qt Online Installer](https://www.qt.io/download).  
Ensure these modules are installed:

```text
✔ Qt Widgets
✔ Qt Serial Port
✔ Qt Charts
✔ Qt 3D (core, extras, render, input)
````

---

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
