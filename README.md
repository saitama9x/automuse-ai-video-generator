# 🎬 AutoMuse — Batch AI Video & Image Generator Studio

<div align="center">

[![Live Web App](https://img.shields.io/badge/Web%20App-automuse.site-4F46E5?style=for-the-badge&logo=googlechrome&logoColor=white)](https://automuse.site/)
[![Status](https://img.shields.io/badge/Status-Online%20%26%20Active-brightgreen?style=for-the-badge)](https://automuse.site/)
[![Aspect Ratios](https://img.shields.io/badge/Aspect%20Ratios-16%3A9%20%7C%209%3A16-orange?style=for-the-badge)](https://automuse.site/)
[![Supported Languages](https://img.shields.io/badge/Languages-EN%20%7C%20VI%20%7C%20HI%20%7C%20RU%20%7C%20ZH-blue?style=for-the-badge)](https://automuse.site/)

<br />

<p align="center">
  <b>A high-speed, automated web platform for batch AI video and image creation. Convert text to video, animate images into cinematic clips, and produce high-resolution content at scale.</b>
</p>

### 🚀 [Open Studio in Your Browser » https://automuse.site/](https://automuse.site/)

[Overview](#-overview) •
[Key Features](#-key-features) •
[AI Generation Modes](#-supported-ai-generation-modes) •
[User Guide](#-how-to-use-automuse) •
[Workflow & Capabilities](#-smart-workflow--creative-controls) •
[FAQ](#-frequently-asked-questions-faq)

</div>

---

## 🌟 Overview

<img width="1895" height="1065" alt="image" src="https://github.com/user-attachments/assets/bec81e24-069c-4bfe-b26b-3a8f9b891a9b" />

**[AutoMuse](https://automuse.site/)** is an all-in-one web-based studio built to automate and supercharge generative AI workflows. Instead of manually entering prompts one by one, AutoMuse empowers creators, marketers, video editors, and digital artists to generate dozens or hundreds of high-definition AI videos and images in parallel.

Running entirely in your browser with zero software installation, AutoMuse connects directly with Muse AI to deliver an industrial-grade batch generation pipeline with real-time tracking and fast streaming exports.

---

## ✨ Key Features

- **⚡ High-Throughput Batch Generation**: Input hundreds of prompts at once (one per line) or import entire prompt lists from `.txt` files in a single click.
- **🚀 Multi-Threaded Parallel Execution**: Customize your worker concurrency (from 1 to 5 threads) to maximize processing speed while maintaining seamless queue stability.
- **🎬 Full Multi-Modal AI Capabilities**:
  - **Text to Video**: Transform detailed textual scene descriptions into smooth, cinematic video clips.
  - **Image to Video**: Animate static photos, portraits, and concept artwork into realistic motion video.
  - **Text to Image**: Rapidly produce visual concepts, wallpapers, and thumbnail art from text.
- **📐 Dual Aspect Ratios (16:9 & 9:16)**:
  - **16:9 Landscape**: Perfect for YouTube, presentations, TV, and widescreen desktop monitors.
  - **9:16 Portrait**: Optimized for TikTok, Instagram Reels, YouTube Shorts, and mobile stories.
- **🖼️ Intelligent Reference Asset Dock**:
  - **Shared / All Mode**: Reference images supply consistent aesthetic guidelines across all prompts.
  - **Paired (1-to-1) Mode**: Automatically pairs Line $i$ with Image $i$ for precise multi-scene storyboard generation.
  - **Built-in Image Cropper**: Easily adjust aspect ratio and frame your reference assets inside the tool.
- **📁 Multi-Project Organization & Multi-Account Support**:
  - Keep campaigns, brands, or topics neatly structured into separate project workspaces.
  - Use a global shared cookie or set independent cookies per project to run multiple accounts simultaneously.
- **📦 Zero-Buffer Streamed ZIP Export**:
  - Preview completed videos with a responsive in-browser video player.
  - Download individual files immediately or export the entire project’s assets in a single, memory-safe streamed ZIP package.
- **🌐 5 Built-in Languages (i18n)**: Native UI translation for **English**, **Tiếng Việt**, **हिन्दी (Hindi)**, **Русский (Russian)**, and **中文 (Chinese)**.
- **🛡️ 100% Client-Side Privacy**: Prompts, projects, and credentials are saved strictly in your browser (`localStorage`). No private prompts or databases are held on external servers.

---

## 🎯 Supported AI Generation Modes

| Mode | Input | Output | Best Used For |
| :--- | :--- | :--- | :--- |
| **Text-to-Video** | Descriptive Text Prompt | HD Video Clip (`.mp4`) | Cinematic b-roll, storytelling clips, nature/sci-fi scenes, commercial concepts |
| **Image-to-Video** | Image + Motion Prompt | Animated Video (`.mp4`) | Bringing character art to life, product motion showcases, photo animation |
| **Text-to-Image** | Descriptive Text Prompt | High-Res Image (`.png`/`.jpg`) | Concept design, social media assets, visual inspiration, digital artwork |

---

## 📖 How to Use AutoMuse

Creating media in bulk with AutoMuse takes only a few simple steps:

### 1. Access the Studio
Open **[https://automuse.site/](https://automuse.site/)** on your desktop, tablet, or mobile browser.

### 2. Configure Your Authentication
- Click the **Key / Cookie** icon in the top navigation bar.
- Paste your `muse.ai` session cookie into the **Shared Cookie** field (or assign a custom cookie to a specific project).

### 3. Create a Project & Set Dimensions
- In the sidebar, click **New Project** to keep your work organized.
- Choose your preferred output ratio:
  - **Landscape (16:9)** for wide-format videos.
  - **Portrait (9:16)** for vertical social videos.

### 4. Compose Prompts & Add References
- Type or paste your prompt list directly into the composer. Each line automatically becomes an individual generation job.
- Or click **Load TXT** to upload a prompt file from your computer.
- *(Optional)* Upload reference images to the asset dock and choose your mapping scheme (**All** or **Paired**).

### 5. Start the Queue & Monitor Progress
- Choose your concurrency limit (1 to 5 threads).
- Click **Run**. AutoMuse will process jobs automatically with real-time status tracking, estimated time remaining (ETA), and progress indicators.
- Need to step away? AutoMuse maintains queue state and lets you pause, resume, or retry failed items at any time.

### 6. Preview & Download
- Watch your generated videos directly inside the interactive player.
- Click **Download** on any result or hit **Download ZIP** to pack all finished assets from your project into a single archive.

---

## 💡 Smart Workflow & Creative Controls

### 🔹 Paired Storyboard Generation
When creating sequential stories, upload multiple character poses or concept shots. By selecting **Paired (1-to-1)** mode:
- **Line 1** will animate **Image 1**
- **Line 2** will animate **Image 2**
- **Line 3** will animate **Image 3**

This allows seamless scene-by-scene consistency without having to configure each video individually.

### 🔹 Safe Queue Controls
- **Anti-Spam Cooldown**: Built-in safeguards protect against accidental double-clicks or erratic queue stops.
- **Selective Retry**: Re-run specific failed prompts or batch-retry all unsuccessful jobs with one click.
- **Diagnostic Log**: View real-time background logs to instantly pinpoint any token expiration or network disruptions.

---

## ❓ Frequently Asked Questions (FAQ)

<details>
<summary><b>1. What is AutoMuse?</b></summary>
AutoMuse is a specialized web studio hosted at <a href="https://automuse.site/">automuse.site</a> designed to automate batch generation of AI videos and images using Muse AI.
</details>

<details>
<summary><b>2. Is there any software to install?</b></summary>
No. AutoMuse is 100% web-based. You can use it directly in modern web browsers (Chrome, Edge, Safari, Firefox) on desktop, tablet, or smartphone.
</details>

<details>
<summary><b>3. Are my cookies and prompts private?</b></summary>
Yes. AutoMuse employs a client-first security philosophy. Your projects, prompt batches, and cookies are stored solely in your browser's local storage (<code>localStorage</code>) and are never kept in a remote database.
</details>

<details>
<summary><b>4. Does AutoMuse support vertical videos for TikTok and Shorts?</b></summary>
Yes! You can toggle between <b>Portrait (9:16)</b> and <b>Landscape (16:9)</b> for both video and image generation with a single click.
</details>

<details>
<summary><b>5. Can I use multiple accounts at the same time?</b></summary>
Yes. AutoMuse features project-level cookie scoping. You can assign different cookies to different projects to run concurrent campaigns across multiple accounts simultaneously.
</details>

<details>
<summary><b>6. How many prompts can I run at once?</b></summary>
You can paste hundreds of prompts in one go. AutoMuse queues them efficiently and processes them according to your selected thread limit (1–5 concurrent workers).
</details>

<details>
<summary><b>7. How does the ZIP download work for large projects?</b></summary>
AutoMuse streams finished files directly from the CDN into a single ZIP archive on the fly without loading all files into browser memory first, ensuring smooth downloads even for multi-gigabyte collections.
</details>

---

## 🌐 Try AutoMuse Today

Supercharge your AI content creation pipeline:

👉 **[Launch AutoMuse Studio at automuse.site](https://automuse.site/)**

---

<div align="center">
  <sub>Built for content creators, filmmakers, and digital artists. Powered by AutoMuse.</sub>
</div>
