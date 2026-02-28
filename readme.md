<div align="center">
  <h1>Christopher Dickinson</h1>
  <br>
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

<p align="center">
Army vet. Cybersecurity student. Solo builder.<br><br>
I spent years inside classified networks — SIPRnet, compartmented systems, environments where bad configuration isn't a learning opportunity, it's an incident. That background made me obsessive about how things actually work under the hood, and impatient with software that cuts corners on security.<br><br>
Now I channel that into building: production-grade tools I maintain myself, open-source utilities that scratch real itches, and contributions to projects I actually use. Most of what I ship lives at the intersection of AI, audio, and security tooling.
</p>

<p align="center">
  <a href="https://github.com/theelderemo/Resume">
    <img src="https://img.shields.io/badge/My_Resume-brightgreen?style=for-the-badge&logo=github&logoColor=white" alt="My Resume">
  </a>
  &nbsp;
  <a href="https://www.credly.com/users/chrismdickinson">
    <img src="https://img.shields.io/badge/Credly_Certs-FF6B00?style=for-the-badge&logo=credly&logoColor=white" alt="Credly Badge">
  </a>
</p>

---

<div id="user-content-toc">
  <ul align="center" style="list-style: none;">
    <summary>
      <h1>What I'm Building</h1>
    </summary>
  </ul>
</div>

## [VRS/A — Lyric + Music Workstation](https://vrsa.app)

![React](https://img.shields.io/badge/React_19-20232A?style=flat&logo=react&logoColor=61DAFB)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat&logo=supabase&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat&logo=pwa&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white)

Bootstrapped, solo-dev AI workstation for lyric writing and music production. Built for myself, at first, then made public and added features.

In roughly three months it's gone from zero to a meaningful number of daily active users, an impressive amount of total userss, and paying subscribers on the Studio Pass tier, with absolutely no advertising or marketing. 

**What's under the hood:**
- **Ghostwriter** — chat-based lyric generation with session memory, multi-model A/B mode, take history, and album-context awareness
- **Canvas** — Notion inspired editor with inline AI edits, syllable counter, rhyme heatmap, and MP3 transcription
- **Suno Bridge** — Chrome + Firefox extensions that capture auth tokens and route lyrics directly to the Suno API with version picker (v4 → v5)
- **Audio Analyzer** — BPM + key/scale detection via a custom VM audio engine running Essentia.js WASM
- **Album Art** — Flux 1.1 Pro, Flux 2, and Sora via Azure OpenAI deployments
- **Multi-model routing** — GPT, Claude, DeepSeek, Gemini, Grok, Kimi K2, MiniMax, Mistral across OpenAI, Bedrock, OpenRouter, and Google APIs
- **Rights Management** — proof-of-creation certificate generator (printable PDF)
- **Mobile** — Capacitor 8 Android build + full PWA support

> App: **[vrsa.app](https://vrsa.app)** · Studio: **[studio.vrsa.app](https://studio.vrsa.app)**

<br>

---

<div id="user-content-toc">
  <ul align="center" style="list-style: none;">
    <summary>
      <h1>Other Work</h1>
    </summary>
  </ul>
</div>

## Google Colab

**[HeartLib Script](https://github.com/theelderemo/HeartLib-Google-Colab)**

<a target="_blank" href="https://colab.research.google.com/github/theelderemo/HeartLib-Google-Colab/blob/main/HeartLib.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

Optimized scripts for running [HeartMuLa](https://github.com/HeartMuLa/heartlib) music generation with maximum performance on NVIDIA GPUs, especially A100.

---

**[Ollama Stack](https://github.com/theelderemo/ollama-google-colab)**

<a target="_blank" href="https://colab.research.google.com/github/theelderemo/ollama-google-colab/blob/main/ollamacolab.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

Full Ollama stack running on Google Colab with Gradio as a UI — spin up a local LLM in your browser with zero local setup.

---

**[Wan 2.2 Video](https://github.com/theelderemo/wan2.2-google-colab)**

<a target="_blank" href="https://colab.research.google.com/github/theelderemo/wan2.2-google-colab/blob/main/wan2_2.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

![GitHub Repo stars](https://img.shields.io/github/stars/theelderemo/wan2.2-google-colab)

Plug-and-play Colab notebook for Wan 2.2 — an advanced image-to-video model — stripped down to just work.

<br>

## [CortexAI](https://github.com/theelderemo/cortexai)

![GitHub package.json dynamic](https://img.shields.io/github/package-json/version/theelderemo/cortexai)
![GitHub last commit](https://img.shields.io/github/last-commit/theelderemo/cortexai)
![GitHub contributors](https://img.shields.io/github/contributors-anon/theelderemo/cortexai)
![GitHub License](https://img.shields.io/github/license/theelderemo/cortexai)

Open-source AI-powered penetration testing agent that automates reconnaissance, vulnerability discovery, and analysis. Executes authorized security tests using installed tools, maintains immutable audit trails, and delivers findings with OWASP mapping and remediation guidance.

<br>

## [Epstein Index](https://github.com/theelderemo/FULL_EPSTEIN_INDEX)  
![GitHub Repo stars](https://img.shields.io/github/stars/theelderemo/FULL_EPSTEIN_INDEX)


FULL_EPSTEIN_INDEX is a comprehensive, unified research archive aggregating public releases related to the Jeffrey Epstein estate and associated investigations. 

<br>

## [Epstein Estate Dataset + Gradio Analyzer](https://github.com/theelderemo/Epstein-files) 

When the U.S. House Oversight Committee released 20,000+ pages of unstructured documents, the data was technically public but practically inaccessible. I built a forensic analysis tool to change that.

<dl>
  <dt>Search Engine:</dt>
  <dd>— Local RAG-ready search interface via Gradio for rapid keyword and passage analysis across the full corpus.</dd>
  <dt>Governance:</dt>
  <dd>— Established a Responsible Use Framework to prevent misuse while keeping the tool genuinely open for researchers and journalists.</dd>
</dl>

<br>

## [eDEX-UI Security Patch](https://github.com/theelderemo/Edex-UI-android)

![Patched](https://img.shields.io/badge/Security_Patch-%23FF2D20.svg)  ![GitHub Repo stars](https://img.shields.io/github/stars/theelderemo/eDEX-UI-security-patched)



The original `eDEX-UI` — a well-known sci-fi terminal emulator — was archived with an unresolved security vulnerability. I forked it, patched the flaw, modernized the codebase, removed all deprecated dependencies, and cut a clean release.

> All legacy code has been replaced, minor additional vulns remediated, and the dependency tree is fully up to date.

<br>

## [CorgiDB](https://github.com/roman-corgi/corgidb)

Contributed a `get_optimal_sql_datatypes` helper function to automate efficient SQL datatype selection for pandas DataFrames — reducing manual overhead and ensuring optimal storage across schema generation workflows.

<br>

## [Simple Chat](https://github.com/theelderemo/simple-chat-ui)

Local AI chat workbench with multi-provider support (AWS Bedrock, OpenAI, Azure, Gemini) - Deno-powered server with browser-based UI

---

<div align="center">
  <a href="https://spotify-github-profile.kittinanx.com/api/view?uid=31ezhpiqjkem4fugshj4krrs7a7m&redirect=true">
    <img src="https://spotify-github-profile.kittinanx.com/api/view?uid=31ezhpiqjkem4fugshj4krrs7a7m&cover_image=true&theme=spotify-embed&show_offline=false&background_color=0d1117&interchange=false&profanity=false&mode=dark&bar_color=53b14f&bar_color_cover=false" 
         alt="Spotify GitHub profile">
  </a>
</div>

<img width="1408" height="768" alt="Generated image 2 (1)" src="https://github.com/user-attachments/assets/b96cfa29-d6a0-4eca-a03e-e28635d0ffad" />
