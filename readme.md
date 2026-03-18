<img width="100%" src="https://capsule-render.vercel.app/api?type=blur&color=0:0d1117,20:150a2e,40:2e0a5c,55:5c006e,70:7a0040,85:600010,100:420808&height=200&section=header&text=Chris%20Dickinson&desc=theelderemo&fontSize=42&fontColor=58A6FF&animation=fadeIn&fontAlignY=36&descAlignY=60&descSize=18&descColor=8b949e" />

<div align="center">
  <img src="https://img.shields.io/badge/Cybersecurity_Student-navy">
  <img src="https://img.shields.io/badge/U.S.%20Army%20Veteran-forestgreen?style=flat&logo=army">
  <img src="https://img.shields.io/badge/Top%20Secret_Clearance-firebrick?style=flat&logo=lock&logoColor=white">
</div>

<div align="center">
  <a href="https://github.com/theelderemo">
    <img src="http://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=theelderemo&theme=github_dark" 
         alt="My GitHub stats">
  </a>
  <a href="https://github.com/theelderemo">
    <img src="http://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=theelderemo&theme=github_dark" 
         alt="Repos per language">
  </a>
  <a href="https://github.com/theelderemo">
    <img src="http://github-profile-summary-cards.vercel.app/api/cards/stats?username=theelderemo&theme=github_dark">
  </a>
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=58A6FF&center=true&vCenter=true&width=650&lines=Army+Vet.+Cybersecurity+Student.+Solo+Builder.;ML+%2B+Audio+%2B+Security;chmod+000+/impostor_syndrome" alt="Typing SVG" />
</div>
<div
<p align="center">
I spent years inside classified networks, SIPRnet, compartmented systems, environments where bad configuration isn't a learning opportunity, it's an incident. That background made me obsessive about how things actually work under the hood, and impatient with software that cuts corners on security.<br><br>
Now I channel that into building: production-grade tools I maintain myself, open-source utilities that scratch real itches, and contributions to projects I actually use. Most of what I ship lives at the intersection of AI, audio/music, and security tooling.
</p>

<p align="center">
  <img src="assets/projects-banner.svg" alt="Contributions & Projects" width="100%">
</p>


<p align="center">
  <a href="https://vrsa.app">
    <img src="assets/vrsa-banner.svg" alt="VRSA" width="100%">
  </a>
</p>

Bootstrapped, solo-dev AI workstation for lyric writing and music production — now a **multi-app platform spanning 3 deployments, 3 separate codebases, and 9 proprietary model variants**. Grew from a personal tool to daily active users and paying subscribers with zero advertising.
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 24">
  <path d="M0 12h450 l5 -5 l10 14 l10 -18 l10 14 l5 -5 h450" stroke="#8B5CF6" stroke-width="1.2" fill="none" stroke-linejoin="round"/>
  <line x1="0" y1="12" x2="445" y2="12" stroke="#30363D" stroke-width="1"/>
  <line x1="555" y1="12" x2="1000" y2="12" stroke="#30363D" stroke-width="1"/>
</svg>

#### **Platform surfaces:**

| App | Stack | Status |
|---|---|---|
| [vrsa.app](https://vrsa.app) | React + Vite + Capacitor 8 | Live |
| [studio.vrsa.app](https://studio.vrsa.app) | Next.js 16 + TypeScript + Docker | Live |
| [generate.vrsa.app](https://generate.vrsa.app) | Next.js + React + Zustand + WaveSurfer.js | WIP |

<details>
<summary>Platform Architecture</summary>

```mermaid
graph TB
    subgraph USER [" "]
        direction LR
        Web["🌐 Web"]
        PWA["📱 PWA"]
        Android["🤖 Android"]
    end

    Web & PWA & Android --> A

    subgraph APPS ["Three Deployments"]
        A["<b>vrsa.app</b> React · Vite · Capacitor · 32 routes · 50 components · 9 hooks · Ghostwriter · Canvas · Audio Analyzer · Suno Bridge · Album Art · Rights Mgmt"]

        B["<b>studio.vrsa.app</b> Next.js · TypeScript · Tone.js · Browser DAW — 16 tracks · 64 clips · Piano Roll · Drum Sequencer · Waveform Editor · 1,300 lines of synth presets · MIDI I/O"]

        C["<b>generate.vrsa.app</b> Next.js · TypeScript · Zustand · 11 pages · 8 stores · ~120 components · 7 gen modes · AI Radio · AI DJ · LoRA Training · WaveSurfer.js"]
    end

    Web --> B & C

    subgraph AUTH ["Shared Auth Layer"]
        D[("Supabase · .vrsa.app cookies · RLS · Edge Functions · RPCs · Storage")]
    end

    A & B & C --> D

    subgraph GPU ["Modal Backend — H100 GPU"]
        E["Async Spawn/Poll · 600s Timeout · Persistent Weight Volume"]
        E --> F["<b>6 DiT Models</b> v1.5 · v1.5-stream · v1.5-craft · v1.5-core · v1.5-shift3 · v1.5-shift1"]
        E --> G["<b>3 LM Models</b> pulse-nano 0.6B · pulse 1.7B · pulse-pro 4B"]
    end

    D --> E

    subgraph LLM ["Multi-Provider LLM Routing"]
        H["GPT · Claude · DeepSeek · Gemini · Grok · Kimi K2 · MiniMax · Mistral"]
    end

    A --> H

    subgraph MEDIA ["Media Generation"]
        I["Flux 1.1 Pro · Flux 2 · Sora via Azure OpenAI"]
    end

    A --> I

    subgraph INFRA ["Infrastructure"]
        J["107 API Endpoints · Vercel · Docker · Sentry · Honeybadger · Amplitude · Intercom · Cloudflare Turnstile · FingerprintJS · Crowdin i18n"]
    end

    style USER fill:transparent,stroke:#58A6FF,stroke-width:2px,color:#58A6FF
    style APPS fill:transparent,stroke:#8B5CF6,stroke-width:2px,color:#8B5CF6
    style AUTH fill:transparent,stroke:#3ECF8E,stroke-width:2px,color:#3ECF8E
    style GPU fill:transparent,stroke:#F97316,stroke-width:2px,color:#F97316
    style LLM fill:transparent,stroke:#EC4899,stroke-width:2px,color:#EC4899
    style MEDIA fill:transparent,stroke:#EAB308,stroke-width:2px,color:#EAB308
    style INFRA fill:transparent,stroke:#6B7280,stroke-width:2px,color:#6B7280
```

</details>  

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 20">
  <path d="M435 10h15 M460 10h5 M475 10h25 M510 10h5 M525 10h15 M550 10h5" stroke="#58A6FF" stroke-width="1.5"/>
</svg>

#### **VRSA v1.5 — AI Music Generation Engine:**
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 24">
  <path d="M0 12h470 M530 12h470" stroke="#30363D" stroke-width="1"/>
  <path d="M480 8v8 M490 4v16 M500 10v4 M510 6v12 M520 8v8" stroke="#8b949e" stroke-width="2.5" stroke-linecap="round"/>
</svg>

Custom cloud inference backend running **6 DiT plus 3 LM model variants** on H100 GPUs, all served from a persistent weight volume with async spawn/poll architecture:

| VRSA Name | Type | Description |
|---|---|---|
| vrsa v1.5 | DiT (default) | Turbo — balanced speed + quality |
| vrsa v1.5-stream | DiT | Continuous generation mode |
| vrsa v1.5-craft | DiT | SFT — higher fidelity |
| vrsa v1.5-core | DiT | Base model |
| vrsa v1.5-shift3 / shift1 | DiT | Flow-shift variants |
| vrsa-pulse-nano | LM 0.6B | Fast token-level generation |
| vrsa-pulse | LM 1.7B | Balanced LM |
| vrsa-pulse-pro | LM 4B (default) | Full reasoning + CoT metadata |

#### **7 task types:**

| | | | | | | |
|---|---|---|---|---|---|---|
| Text to Music | Music to Music | Cover | Repainting | Extracting | Section by Section Build | Complete |

#### **Output formats:**  
mp3 · flac · wav · wav32 · opus · aac   
#### **Generation surface:**    
BPM, key/scale, time signature, guidance scale, ODE/SDE sampling, CFG interval, latent shift/rescale, batch size up to 8

#### **30+ page modules in vrsa.app:**

| Module | Description |
|---|---|
| **Ghostwriter** | Chat-based lyric generation with session memory, multi-model A/B mode, take history, and album-context awareness |
| **Canvas** | Notion-inspired editor with inline AI edits, syllable counter, rhyme heatmap, and MP3 transcription |
| **Suno Bridge** | Chrome + Firefox extensions that capture auth tokens and route lyrics directly to the Suno with version picker (v4 → v5) |
| **Audio Analyzer** | BPM + key/scale detection via custom VM audio engine running Essentia.js WASM |
| **Album Art** | Flux 1.1 Pro, Flux 2, and Sora via Azure OpenAI deployments |
| **Multi-model routing** | GPT, Claude, DeepSeek, Gemini, Grok, Kimi K2, MiniMax, Mistral across OpenAI, Bedrock, OpenRouter, and Google APIs |
| **Rights Management** | Proof-of-creation PDF certificate generator |
| **MyMusic / Projects / AlbumWorkspace** | Full library, project, and album management |
| **Admin Panel** | Platform administration, really just a view only style cms for me to see stats |
| **Studio Pass** | Subscription and billing management |
| **Mobile** | Capacitor 8 Android build + full PWA support |

#### **Infrastructure:**

| | |
|---|---|
| **Auth** | Cross-subdomain cookies scoped to `.vrsa.app`, shared across all three apps |
| **Compute** | Modal async generation pipeline, H100 GPU, 600s timeout, persistent weights volume |
| **API** | 107 endpoints mapped and routed |
| **DevOps** | Crowdin i18n workflow, Docker + docker-compose, multi-project deployment |

> App: **[vrsa.app](https://vrsa.app)** · Studio: **[studio.vrsa.app](https://studio.vrsa.app)** · Generate *(WIP)*: **[generate.vrsa.app](https://generate.vrsa.app)**

<br>

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 24">
  <path d="M0 12h470 M530 12h470" stroke="#30363D" stroke-width="1"/>
  <path d="M480 8v8 M490 4v16 M500 10v4 M510 6v12 M520 8v8" stroke="#8b949e" stroke-width="2.5" stroke-linecap="round"/>
</svg>

<br>

<p align="center">
  <a href="https://github.com/theelderemo/ai-audio-tools">
    <img src="assets/ai-audio-tools-banner.svg" alt="AI Audio Tools" width="100%">
  </a>
</p>

#### A curated list of 100+ AI-powered audio tools across 16 categories:  
music creation, voice cloning, stem separation, TTS, transcription, sound detection, and more. 

<p align="center">
  <img src="assets/other-work-banner.svg" alt="Other Work & Contributions" width="100%">
</p>

<br>

<p align="center">
    <img src="assets/colab-banner.svg" alt="Colab Scripts" width="100%">
</p>

<br>

**[HeartLib Script](https://github.com/theelderemo/HeartLib-Google-Colab)**

<a target="_blank" href="https://colab.research.google.com/github/theelderemo/HeartLib-Google-Colab/blob/main/HeartLib.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

Optimized scripts for running [HeartMuLa](https://github.com/HeartMuLa/heartlib) music generation with maximum performance on NVIDIA GPUs, especially A100.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 20">
  <path d="M0 10h475 M525 10h475" stroke="#30363D" stroke-width="1"/>
  <path d="M485 5v10h5 M515 5v10h-5" stroke="#58A6FF" stroke-width="1.5" fill="none"/>
  <rect x="495" y="8" width="10" height="4" fill="#6B7280"/>
</svg>

**[Ollama Stack](https://github.com/theelderemo/ollama-google-colab)**

<a target="_blank" href="https://colab.research.google.com/github/theelderemo/ollama-google-colab/blob/main/ollamacolab.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

Full Ollama stack running on Google Colab with Gradio as a UI — spin up a local LLM in your browser with zero local setup.


<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 20">
  <path d="M0 10h475 M525 10h475" stroke="#30363D" stroke-width="1"/>
  <path d="M485 5v10h5 M515 5v10h-5" stroke="#58A6FF" stroke-width="1.5" fill="none"/>
  <rect x="495" y="8" width="10" height="4" fill="#6B7280"/>
</svg>

**[Wan 2.2 Video](https://github.com/theelderemo/wan2.2-google-colab)**

<a target="_blank" href="https://colab.research.google.com/github/theelderemo/wan2.2-google-colab/blob/main/wan2_2.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

<br>

Plug-and-play Colab notebook for Wan 2.2 — an advanced image-to-video model — stripped down to just work.

<br>

<p align="center">
  <a href="https://github.com/theelderemo/cortexai">
    <img src="assets/cortexai-banner.svg" alt="CortexAI" width="100%">
  </a>
</p>

This was a proof of concept project for myself. Open-source AI-powered penetration testing agent that automates reconnaissance, vulnerability discovery, and analysis. Executes authorized security tests using installed tools, maintains immutable audit trails, and delivers findings with OWASP mapping and remediation guidance. Fair warning, it's a monorepo.

<br>

<p align="center">
  <a href="https://github.com/theelderemo/FULL_EPSTEIN_INDEX">
    <img src="assets/epstein-index-banner.svg" alt="Epstein Index" width="100%">
  </a>
</p>

A comprehensive, unified research archive aggregating public releases related to the Jeffrey Epstein estate and associated investigations. 

<br>

<p align="center">
  <a href="https://github.com/theelderemo/Epstein-files">
    <img src="assets/epstein-files-banner.svg" alt="Epstein Files" width="100%">
  </a>
</p>

When the U.S. House Oversight Committee released 20,000+ pages of unstructured documents, the data was technically public but practically inaccessible. I built a forensic analysis tool to change that.

<dl>
  <dt>Search Engine:</dt>
  <dd>— Local RAG-ready search interface via Gradio for rapid keyword and passage analysis across the full corpus.</dd>
  <dt>Governance:</dt>
  <dd>— Established a Responsible Use Framework to prevent misuse while keeping the tool genuinely open for researchers and journalists.</dd>
</dl>

<br>

<p align="center">
  <a href="https://github.com/theelderemo/eDEX-UI-security-patched">
    <img src="assets/edex-ui-banner.svg" alt="Edex UI" width="100%">
  </a>
</p>


The original `eDEX-UI` — a well-known sci-fi terminal emulator — was archived with an unresolved security vulnerability. I forked it, patched the flaw, modernized the codebase, removed all deprecated dependencies, and cut a clean release. 

> All legacy code has been replaced, minor additional vulns remediated, and the dependency tree is fully up to date.

<br>

<p align="center">
  <a href="https://github.com/roman-corgi/corgidb">
    <img src="assets/corgidb-banner.svg" alt="CorgiDB" width="100%">
  </a>
</p>

Contributed a helper function to automate efficient SQL datatype selection for pandas DataFrames — reducing manual overhead and ensuring optimal storage across schema generation workflows.

<br>

<p align="center">
  <a href="https://github.com/theelderemo/simple-chat-ui">
    <img src="assets/simple-chat-banner.svg" alt="Simple Chat" width="100%">
  </a>
</p>

Local AI chat workbench with multi-provider support (AWS Bedrock, OpenAI, Azure, Gemini) - Deno-powered server with browser-based UI  

<br>

<details>
<summary>Certifications</summary>

<div align="center">
  <a href="https://www.credly.com/users/chrismdickinson">
    <img src="https://img.shields.io/badge/Credly_Profile-FF6B00?style=for-the-badge&logo=credly&logoColor=white" alt="Credly Profile">
  </a>
</div>
<br>

<!--START_SECTION:badges-->
<a href="https://www.credly.com/badges/da05cb1e-13b8-4e2a-b983-200a09dd5dd6" title="Google Cybersecurity Professional Certificate V2"><img src="https://images.credly.com/size/80x80/images/0bf0f2da-a699-4c82-82e2-56dcf1f2e1c7/image.png" alt="Google Cybersecurity Professional Certificate V2" width="80" height="80"></a>
<a href="https://www.credly.com/badges/e7e90b67-7c5f-4531-8515-c38ff1f7b4e9" title="Google Project Management Professional Certificate"><img src="https://images.credly.com/size/80x80/images/51dff787-71ae-4d9d-9ca7-ef9342914d75/GCC_badge_PGM_1000x1000.png" alt="Google Project Management Professional Certificate" width="80" height="80"></a>
<a href="https://www.credly.com/badges/21b90465-9cbb-48dd-a2fd-f4427bfbdf9c" title="Introduction to Cybersecurity"><img src="https://images.credly.com/size/80x80/images/af8c6b4e-fc31-47c4-8dcb-eb7a2065dc5b/I2CS__1_.png" alt="Introduction to Cybersecurity" width="80" height="80"></a>
<a href="https://www.credly.com/badges/2ddd8243-42ba-45e7-992a-e09a5fcd9333" title="LFC108: Cybersecurity Essentials"><img src="https://images.credly.com/size/80x80/images/e79f9317-b3f7-4b57-a859-f24d5f25fe36/blob" alt="LFC108: Cybersecurity Essentials" width="80" height="80"></a>
<a href="https://www.credly.com/badges/db11d6a9-5a71-4fac-9ae6-2285f4690838" title="Networking Basics"><img src="https://images.credly.com/size/80x80/images/5bdd6a39-3e03-4444-9510-ecff80c9ce79/image.png" alt="Networking Basics" width="80" height="80"></a>
<a href="https://www.credly.com/badges/321f3b1b-3aa4-46aa-94b5-1308746afee9" title="Network Addressing and Basic Troubleshooting"><img src="https://images.credly.com/size/80x80/images/49c099bd-8542-4f48-8c03-f21799dcaf51/image.png" alt="Network Addressing and Basic Troubleshooting" width="80" height="80"></a>
<a href="https://www.credly.com/badges/114b088c-90db-4d7d-8aaf-2f3d6f020a4f" title="Introduction to Cybersecurity Tools and Cyberattacks V3"><img src="https://images.credly.com/size/80x80/images/4ccd9157-c68a-4797-b23c-506601198991/blob" alt="Introduction to Cybersecurity Tools and Cyberattacks V3" width="80" height="80"></a>
<a href="https://www.credly.com/badges/f01e68f8-dcf3-407f-80a7-ad81424efaf0" title="Cybersecurity Roles, Processes & Operating System Security"><img src="https://images.credly.com/size/80x80/images/c617d37c-9c45-4617-aabf-e11954e188ec/blob" alt="Cybersecurity Roles, Processes & Operating System Security" width="80" height="80"></a>
<a href="https://www.credly.com/badges/830e0e75-ba79-41f2-bd40-aef61e3805f8" title="Project Management Essentials"><img src="https://images.credly.com/size/80x80/images/4d7038ef-658b-4ef8-8627-e0af45963c7e/image.png" alt="Project Management Essentials" width="80" height="80"></a>
<a href="https://www.credly.com/badges/b0e33980-7b53-4c28-ab9c-a7c2931eaf60" title="Cyber Threat Management"><img src="https://images.credly.com/size/80x80/images/5d5ac32b-d239-42b8-9665-8a921dc3ab47/image.png" alt="Cyber Threat Management" width="80" height="80"></a>
<a href="https://www.credly.com/badges/c3cacfb4-a6c9-42b9-ac33-0c08d0fb8364" title="Meta Data Analyst Professional Certificate"><img src="https://images.credly.com/size/80x80/images/4dd82f2c-e7eb-4b64-bb24-f4351f596220/image.png" alt="Meta Data Analyst Professional Certificate" width="80" height="80"></a>
<a href="https://www.credly.com/badges/6bef95d0-e030-4ded-8cec-205c91f781ad" title="Cybersecurity Essentials"><img src="https://images.credly.com/size/80x80/images/c1426860-8205-4220-a0d5-5e6d4f07db17/blob" alt="Cybersecurity Essentials" width="80" height="80"></a>
<a href="https://www.credly.com/badges/b15b4041-c7ad-4f8f-84fa-567db7e07b38" title="IBM Cybersecurity Analyst Assessment"><img src="https://images.credly.com/size/80x80/images/3870a682-efd0-4a47-851c-287ba4397677/blob" alt="IBM Cybersecurity Analyst Assessment" width="80" height="80"></a>
<!--END_SECTION:badges-->

</details>

<br>

<div align="center">
  <a href="https://spotify-github-profile.kittinanx.com/api/view?uid=31ezhpiqjkem4fugshj4krrs7a7m&redirect=true">
    <img src="https://spotify-github-profile.kittinanx.com/api/view?uid=31ezhpiqjkem4fugshj4krrs7a7m&cover_image=true&theme=spotify-embed&show_offline=false&background_color=0d1117&interchange=false&profanity=false&mode=dark&bar_color=53b14f&bar_color_cover=false" 
         alt="Spotify GitHub profile">
  </a>
</div>

<br>

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 24">
  <path d="M0 12h480 M520 12h480" stroke="#30363D" stroke-width="1"/>
  <path d="M488 8l5 4-5 4 M498 16h8" stroke="#58A6FF" stroke-width="1.5" fill="none" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

<p align="center">
  <img src="assets/dust.svg" alt="dust" width="100%">
</p>

<!-- 
  49 66 20 79 6f 75 27 72 65 20 72 65 61 64 69 6e 67 20 74 68 69 73 2c 
  79 6f 75 20 61 6c 72 65 61 64 79 20 6b 6e 6f 77 20 77 68 61 74 20 69 74 20 73 61 79 73 2e
-->
