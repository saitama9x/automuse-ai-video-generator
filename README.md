# 🎬 AutoMuse — Batch AI Video & Image Generator Studio

<div align="center">

[![Live Web App](https://img.shields.io/badge/Live%20Website-automuse.site-4F46E5?style=for-the-badge&logo=googlechrome&logoColor=white)](https://automuse.site/)
[![Next.js 14](https://img.shields.io/badge/Next.js-14.2-black?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![React 18](https://img.shields.io/badge/React-18.3-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.6-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-3.4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![GitHub Stars](https://img.shields.io/github/stars/saitama9x/automuse-ai-video-generator?style=for-the-badge&color=ffd700)](https://github.com/saitama9x/automuse-ai-video-generator)

<p align="center">
  <b>High-throughput web studio for automated batch AI video and image generation. Convert text to video, animate images into videos, and synthesize high-resolution media at scale.</b>
</p>

### 🌐 [Launch Web App » automuse.site](https://automuse.site/)

[Overview](#-overview) •
[Key Features](#-key-features) •
[Supported AI Modes](#-supported-ai-generation-modes) •
[Quick Start](#-quick-start-guide) •
[Architecture](#-architecture--security) •
[Tech Stack](#-tech-stack) •
[FAQ](#-frequently-asked-questions-faq)

</div>

---

## 🌟 Overview

**[AutoMuse](https://automuse.site/)** is an open-access, high-performance web platform built to automate **AI video generation** and **AI image synthesis**. Designed for content creators, digital marketers, TikTok/Reels/Shorts producers, and AI developers, AutoMuse eliminates the friction of one-by-one manual prompting by introducing an industrial-grade **batch processing pipeline** powered by Muse AI.

With AutoMuse at [automuse.site](https://automuse.site/), you can input hundreds of prompts at once, pair them with reference assets, configure concurrent worker threads, and stream finished high-definition media directly to your machine or export entire campaigns as memory-efficient ZIP archives.

---

## ✨ Key Features

- **🚀 High-Speed Batch Generation**: Paste unlimited prompts (one per line) or import `.txt` prompt files. Process multiple video and image tasks simultaneously.
- **⚡ Multi-Threaded Concurrency**: Configurable execution threads (1 to 5 parallel workers) for optimal job throughput without account rate-limiting.
- **🎬 Full Multi-Modal AI Suite**: Native support for **Text-to-Video**, **Image-to-Video**, and **Text-to-Image**.
- **📐 Dual Aspect Ratio Presets**: Switch between **16:9 Landscape** (YouTube, Desktop) and **9:16 Portrait** (TikTok, Instagram Reels, YouTube Shorts).
- **🖼️ Advanced Reference Image Mapping**:
  - **Shared / All Mode**: Reference assets provide universal stylistic context across all prompts.
  - **Paired (1-to-1) Mode**: Automatically pairs Line $i$ with Image $i$ for precise storyboard and multi-scene continuity.
  - **Built-in Image Editor**: Real-time cropping and ratio alignment directly in the browser.
- **📁 Multi-Project Organization & Multi-Account Cookies**: Isolate projects into dedicated workspaces with individual cookie authentication or use a global shared cookie.
- **📦 Zero-Buffer Streamed ZIP Export**: Download individual files on the fly or export entire multi-gigabyte project outputs in a single, memory-safe streamed ZIP archive (ZIP64 compliant).
- **🌐 5 Built-in Languages (i18n)**: Fully translated in **English**, **Tiếng Việt**, **हिन्दी (Hindi)**, **Русский (Russian)**, and **中文 (Chinese)**.
- **🛡️ Privacy & Client-First Security**: Zero server database retention. Session tokens and projects reside safely in client `localStorage`, shielded by an HMAC-signed, SSRF-protected proxy layer.

---

## 🎯 Supported AI Generation Modes

| Mode | Input | Output | Best Used For |
| :--- | :--- | :--- | :--- |
| **Text-to-Video** | Descriptive Text Prompt | HD Video Clip (`.mp4`) | AI storytelling, B-roll generation, abstract scenes, background visuals |
| **Image-to-Video** | Reference Image + Motion Prompt | Animated Video (`.mp4`) | Bringing portraits to life, product animation, photo animation, scene transitions |
| **Text-to-Image** | Text Description | High-Res Visual (`.png`/`.jpg`) | Concept design, thumbnails, character concepting, wallpaper creation |

---

## 🚀 Quick Start Guide

Experience the full studio live at **[https://automuse.site/](https://automuse.site/)**:

### Step 1: Set Your Authentication Cookie
Click the **Cookie** key icon in the navigation bar. Paste your session cookie into the **Shared Cookie** field (or set a unique cookie for a specific project).

### Step 2: Create a Project & Pick Aspect Ratio
Create a project workspace in the sidebar. Select your target aspect ratio:
- `Landscape (16:9)` for YouTube / Widescreen.
- `Portrait (9:16)` for TikTok / Reels / Shorts.

### Step 3: Input Prompts & Reference Images
- Type or paste your prompt batch into the composer (each line represents a separate generation job).
- Click **Load TXT** to upload pre-written prompt lists.
- (Optional) Upload reference pictures to the asset tray and choose between **All** or **Paired** mapping.

### Step 4: Run Queue & Monitor Progress
- Select your desired thread count (e.g., 2–4 concurrent jobs) and click **Run**.
- Follow live job statuses (`pending`, `running`, `success`, `failed`), real-time progress bars, and ETA indicators.

### Step 5: Preview & Export
- Inspect outputs directly in the built-in media viewer.
- Click **Download** for individual assets or **Download ZIP** to stream all completed results into a single archive.

---

## 🏗️ Architecture & Security

AutoMuse operates on a secure, lightweight architecture that isolates sensitive credentials from external exposure while ensuring lightning-fast streaming speeds:

```
[Browser Client]
  │  Zustand + LocalStorage (Zero server-side prompt storage)
  │  Cryptographic token signing (HMAC-SHA256, AES-256 sealed sessions)
  ▼
[Next.js API Gateway / Proxy Layer]
  ├─ /api/muse/*             → Signs X-Device-ID & validates tokens → Upstream AI engine
  ├─ /api/download           → SSRF-hardened CDN validation → Client stream
  └─ /api/download-project   → Single-use ticket authentication → O(1) memory ZIP64 stream
```

### Security & Privacy Highlights
- **Client-Side Data Ownership**: Projects, cookies, and prompt logs remain strictly in the user's browser.
- **SSRF Prevention**: All media downloads strictly enforce host allowlists (`*.fbcdn.net`) with redirect verification.
- **Memory Bounded Streaming**: Project ZIP packaging consumes minimal RAM regardless of total media size.

---

## 🛠️ Tech Stack

- **Framework**: [Next.js 14](https://nextjs.org/) (Pages Router)
- **Frontend**: [React 18](https://react.dev/), [TypeScript 5.6](https://www.typescriptlang.org/)
- **Styling**: [Tailwind CSS 3.4](https://tailwindcss.com/)
- **State Management**: [Zustand](https://github.com/pmndrs/zustand) with client-side persistence
- **Virtualization**: [@tanstack/react-virtual](https://tanstack.com/virtual) (Smooth 60 FPS table rendering with 1,000+ jobs)
- **Localization**: [i18next](https://www.i18next.com/)
- **Deployment**: Docker, Docker Compose, Caddy Reverse Proxy, Cloudflare Tunnel

---

## 💻 Local Development & Installation

### Requirements
- **Node.js**: `v20.0.0+`
- **pnpm**: `v10.0.0+`

```bash
# 1. Clone the repository
git clone https://github.com/saitama9x/automuse-ai-video-generator.git
cd automuse-ai-video-generator

# 2. Install dependencies
pnpm install

# 3. Configure environment
cp .env.example .env.local

# 4. Start local development server
pnpm dev
```

Visit `http://localhost:3000` to preview your local instance.

### Run Tests & Validation
```bash
pnpm typecheck   # TypeScript static typechecking
pnpm test        # Vitest test suite
```

---

## 🐳 Docker Deployment

Run AutoMuse in an isolated production container:

```bash
# Build & start container
docker compose up -d --build
```

For custom domain configuration, SSL termination, and automated deployment pipelines, check the **[DEPLOY.md](DEPLOY.md)** guide.

---

## ❓ Frequently Asked Questions (FAQ)

<details>
<summary><b>1. Is AutoMuse free to use?</b></summary>
Yes, the AutoMuse web application at <a href="https://automuse.site/">automuse.site</a> is free to access. You only need your own Muse account credentials/cookie to run generations.
</details>

<details>
<summary><b>2. Are my prompts and cookies stored on your server?</b></summary>
No. AutoMuse uses a client-first security model. Your prompts, projects, and cookies are stored solely in your browser's <code>localStorage</code>. Requests are proxied solely for HMAC signing and CORS/SSRF-compliant media retrieval.
</details>

<details>
<summary><b>3. Can I generate videos in 9:16 vertical format for TikTok and Shorts?</b></summary>
Yes! AutoMuse natively supports both <code>Portrait (9:16)</code> and <code>Landscape (16:9)</code> aspect ratios for all video and image generation modes.
</details>

<details>
<summary><b>4. What is the difference between "Shared" and "Paired" reference mode?</b></summary>
In <b>Shared</b> mode, all prompts in your batch use all uploaded reference images. In <b>Paired</b> mode, Prompt Line 1 uses Image 1, Prompt Line 2 uses Image 2, and so on—perfect for animating a sequential series of images.
</details>

<details>
<summary><b>5. How does the ZIP download handle large multi-gigabyte projects?</b></summary>
AutoMuse uses an asynchronous server-side streaming engine with ZIP64 support. Files are streamed sequentially from the CDN directly into the user's download stream with $O(1)$ RAM utilization, preventing server crashes or browser memory overflow.
</details>

---

## 📜 License & Disclaimer

This project is maintained for creative and automation workflows. Please ensure your usage complies with the terms of service of the respective third-party AI models and providers.

---

<div align="center">
  <sub>Designed & Developed for AI creators worldwide. Visit <b><a href="https://automuse.site/">AutoMuse Studio</a></b>.</sub>
</div>
