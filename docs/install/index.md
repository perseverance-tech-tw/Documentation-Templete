# Installation Guide

**Goal:** Help users get your application running on their computer.

---

## System Requirements

Before installing, check if your computer meets these requirements:

### Hardware (Computer Specs)

| Component | Minimum | Recommended |
| :--- | :--- | :--- |
| **CPU** | Dual-core | Quad-core |
| **RAM** | 4 GB | 8 GB |
| **Storage** | 500 MB | 1 GB |

### Software (OS)

| Platform | Requirement |
| :--- | :--- |
| **Windows** | Windows 10 or later |
| **Linux** | Ubuntu 20.04 or similar |
| **macOS** | macOS 10.15 or later |

---

## User Installation

Follow these steps to install the application.

### 1. Download

Get the installer from our [Releases Page](https://github.com/your-username/your-project/releases).
- **Windows**: `YourProject-Setup.exe`
- **Mac**: `YourProject.dmg`
- **Linux**: `YourProject-linux.tar.gz`

### 2. Install

=== "Windows"
    1. Right-click the downloaded file.
    2. Select **Run as Administrator**.
    3. Follow the instructions on the screen.

=== "macOS"
    1. Double-click the `.dmg` file.
    2. Drag the app icon into your **Applications** folder.
    3. Open it from Launchpad.

=== "Linux"
    1. Extract the file: `tar -xzf YourProject-linux.tar.gz`
    2. Open terminal in that folder.
    3. Run: `./install.sh`

---

## Developer Installation

If you are a developer and want to modify the code:

1.  **Get the Code:**
    ```bash
    git clone https://github.com/your-username/your-project.git
    cd your-project
    ```

2.  **Prepare Workspace:**
    ```bash
    # Create virtual environment
    python -m venv venv
    
    # Activate it
    source venv/bin/activate  # Mac/Linux
    venv\Scripts\activate     # Windows
    ```

3.  **Install Libraries:**
    ```bash
    pip install -r requirements.txt
    ```

---

## Troubleshooting

**Common Issues:**

- **Permission Denied?** Try running as Administrator or using `sudo`.
- **Download failed?** Check your internet connection.
- **Won't open?** Make sure your OS is up to date.
