<p align="center">
  <img src="docs/assets/images/ui/logo.png" alt="Perseverance Technology" width="200">
</p>

<h1 align="center">MkDocs Documentation Template</h1>

<p align="center">
  <strong>Professional documentation template powered by MkDocs Material</strong>
</p>

<p align="center">
  <a href="#about">About</a> •
  <a href="#features">Features</a> •
  <a href="#quick-start">Quick Start</a> •
  <a href="#configuration">Configuration</a> •
  <a href="#deployment">Deployment</a> •
  <a href="#license">License</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/MkDocs-Material-526CFE?style=for-the-badge&logo=MaterialForMkDocs&logoColor=white" alt="MkDocs Material">
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License">
</p>

---

## About

This is a **professional documentation template** built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) by **Perseverance Technology Co., Ltd.**

We designed this template to help you create **beautiful, comprehensive, and versioned documentation** without starting from scratch. Whether you are a developer, technical writer, or project manager, you can easily adapt this template to your needs.

**Why use this template?**
- **Professional Look:** Ready-to-use corporate-grade design.
- **Multi-Version Support:** Manage different versions of your product documentation (e.g., v1.x, v2.x).
- **Responsive:** Looks great on desktops, tablets, and mobile phones.
- **Searchable:** Powerful built-in search to help users find information instantly.

---

## Features

| Feature | Description |
|---------|-------------|
| **Modern Design** | Clean, professional UI driven by the Material theme |
| **Dark/Light Mode** | Users can toggle between dark and light themes |
| **Responsive** | Fully optimized for all screen sizes |
| **Fast Search** | Instant, client-side search functionality |
| **Code Highlighting** | Syntax highlighting for 100+ programming languages |
| **Diagrams** | Built-in Mermaid diagram support for flowcharts and graphs |
| **Versioning** | Support for multiple documentation versions (Powered by Mike) |
| **Auto Deploy** | Integrated GitHub Actions for automated deployment |

---

## Quick Start

This section guides you through setting up the project on your local machine.

### Prerequisites

Before you begin, ensure you have the following installed:
- **Python** (3.8 or higher): The programming language required to run MkDocs.
- **Git**: Version control system to manage the project code.

### Installation

Follow these steps to get your documentation running locally:

```bash
# 1. Download the project
# Clone this repository to your computer
git clone https://github.com/perseverance-tech-tw/Documentation-Template.git
cd Documentation-Template

# 2. Create a secure workspace (Virtual Environment)
# This keeps the project dependencies isolated from your system
python -m venv .venv

# 3. Activate the workspace
# Mac/Linux:
source .venv/bin/activate
# Windows:
.venv\Scripts\activate

# 4. Install required tools
# Installs MkDocs, Material theme, and Mike version manager
pip install -r requirements.txt

# 5. Start the preview server
# This will launch a local website where you can see your changes live
mkdocs serve
```

Once started, open your web browser and go to: **http://localhost:8000**

---

## Configuration

Everything can be customized to fit your brand.

### Step 1: Update Project Settings
The file `mkdocs.yml` is the "control center" for your documentation. Open it and change the following settings:

```yaml
site_name: Your Project Name
site_url: https://your-username.github.io/your-project/
repo_url: https://github.com/your-username/your-project
repo_name: Your Project
copyright: "&copy; 2026 Your Company. All rights reserved."
```

### Step 2: Branding (Logo & Favicon)
Replace the default images with your company branding:

| File | Location | Description |
|------|----------|-------------|
| **Logo** | `docs/assets/images/ui/logo.png` | Appears in header and footer |
| **Favicon** | `docs/favicon.ico` | Appears in the browser tab |

### Step 3: Color Theme
Customize the look and feel in `mkdocs.yml`:

```yaml
theme:
  palette:
    - scheme: default
      primary: blue      # Main brand color
      accent: amber      # Highlight color
```
*Colors available: red, pink, purple, deep purple, indigo, blue, light blue, cyan, teal, green, light green, lime, yellow, amber, orange, deep orange, brown, grey.*

---

## Deployment

We support standard deployment and versioned deployment.

### Option 1: Standard Deployment
Great for simple projects with a single version.

```bash
mkdocs gh-deploy
```

### Option 2: Versioned Deployment (Recommended)
This uses **Mike** to manage multiple versions (e.g., v1.x, v2.x). Perfect for releasing software updates while keeping old documentation accessible.

```bash
# 1. Deploy your first version (e.g., v1.0)
mike deploy --push 1.0 latest

# 2. Set it as the default version users see first
mike set-default --push latest

# 3. When you release a new version (e.g., v2.0)
mike deploy --push --update-aliases 2.0 latest
```

> **Note:** The `latest` alias ensures users always land on the newest documentation.

---

## Project Structure

Here is how the project files are organized:

```
Documentation-Template/
│
├── .github/              # Automation scripts (GitHub Actions)
├── docs/                 # YOUR CONTENT GOES HERE
│   ├── assets/           # Images and logos
│   ├── definition/       # Overview pages
│   ├── features/         # Feature details
│   ├── install/          # Installation guides
│   ├── usage/            # Usage instructions
│   ├── index.md          # The Homepage
│   └── ...
├── overrides/            # Custom HTML templates (Footer, etc.)
├── mkdocs.yml            # Main Configuration File
└── requirements.txt      # List of software dependencies
```

---

## Development Commands

Reference for common commands you will use:

| Command | Description |
|---------|-------------|
| `mkdocs serve` | **Preview** your site locally |
| `mkdocs build` | **Build** the site into static HTML files |
| `mike serve` | **Preview versions** locally (with dropdown selector) |
| `mike list` | **See all versions** currently deployed |

---

## Contributing

We welcome contributions! Please follow these steps:

1. **Fork** this repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add amazing feature'`
4. **Push** to the branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request

---

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## About Perseverance Technology

<p align="center">
  <img src="docs/assets/images/ui/logo.png" alt="Perseverance Technology Co., Ltd." width="120">
</p>

<p align="center">
  <strong>Perseverance Technology Co., Ltd.</strong><br>
  Building innovative solutions for tomorrow
</p>

<p align="center">
  <a href="https://github.com/perseverance-tech-tw">
    <img src="https://img.shields.io/badge/GitHub-perseverance--tech--tw-181717?style=flat-square&logo=github" alt="GitHub">
  </a>
</p>

---

<p align="center">
  Made with passion by <strong>Perseverance Technology Co., Ltd.</strong>
</p>

<p align="center">
  Copyright 2026 Perseverance Technology Co., Ltd. All rights reserved.
</p>
