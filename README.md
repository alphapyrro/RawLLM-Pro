# RawLLM Pro

A modular web-based mini-application designed to run local language models directly within the Layla platform using hardware acceleration. Built with a structured asset pipeline featuring dedicated JavaScript runtime modules, styled CSS layers, and structured JSON configuration schemas.

---

**Installation & Setup**

1. Download the latest **`RawLLM-Pro-v7.6.3.zip`** package from the Releases page (`https://github.com/alphapyrro/RawLLM/releases`).
2. Open **Layla** and navigate to **Your Apps**.
3. Tap the **`+`** icon in the top right corner to open **Browse Apps**.
4. Tap **Import** in the top right corner.
5. Select **Zip File** and choose the downloaded `.zip` file.
6. Scroll down to the **Custom** section at the bottom and tap the blue **`+`** icon next to **RawLLM Pro** to finalize adding it.
7. Launch RawLLM Pro directly from the list or find it inside your **Your Apps** hub.

---

**What's New in v7.6.3**

### ✨ New Features & Enhancements
* 🎙️ **Concurrent Real-Time TTS Streaming:** Overhauled audio delivery from an end-of-turn blocker into an asynchronous clause-level stream dispatcher that speaks text in real time as tokens generate.
* 📦 **Speech Delivery Timing Selector:** Added a dedicated mode toggle inside the Voice panel between low-latency clause streaming (ideal for system voices) and batch delivery on completion (ideal for neural Kokoro models).
* 🧠 **Intelligent Voice Profiling & Metadata Parsing:** Added regex-based decoding for serialized JSON Kokoro models and system voices to automatically detect and display gender, nationality/dialect, and online/offline availability in the voice picker.
* 💾 **Automatic SQLite Schema Migrations:** Implemented safe runtime `ALTER TABLE` schema updates on boot to automatically register missing columns (`is_streaming`, `is_forked`, `is_pinned`, `sys_prompt_preset_name`) without wiping existing user databases.
* ⚡ **Session Anchor for Warm KV Caches:** Binds startup to a persistent host session contract (`rawllm_session_main`) to keep local llama.cpp KV prefixes warm across conversational turns.
* 📊 **Dynamic Ingestion Calibration:** Added real-time tracking of measured prefill tokens per second (`measuredPrefillTps`) to provide accurate prompt ingestion estimates across mobile NPUs and CPUs.

---

### 🛠️ Bug Fixes & Stability
* 🛡️ **Cross-Platform Safe-Area Inset Scoping:** Replaced brittle global inset padding with scoped WebKit checks (`@supports (-webkit-touch-callout: none)`) across headers, sidebars, and input docks to prevent dead space on Android while preserving notch clearance on iOS.
* 📱 **Visual Viewport Keyboard Anchoring:** Attached active resize listeners to `window.visualViewport` to smoothly track and preserve chat scroll positions when the virtual keyboard opens.
* 🎤 **Native Audio Hardware Unclamping:** Added explicit host audio session cleanup (`releaseHostAudioSession`) to release micro-level microphone session locks when toggling speech recognition.
* 🗄️ **Synchronous In-Memory Thread Cache:** Integrated a dedicated thread cache map (`threadsCache`) to eliminate redundant disk and database reads during rapid UI switches and message operations.
* 📐 **Calibrated Token Estimation Ratio:** Updated token estimation heuristics to `Math.ceil(length / 3.4)` to better match modern BPE tokenizer distributions and avoid context clipping.
* ✂️ **Strict Append-Only Memory Horizon:** Fixed context-pruning behavior to strictly trim from turn 0 only when exceeding context budgets, preventing prefix invalidation during ongoing turns.

---

**Interface & Features**

| 1. 💬 Main Chat | 2. 🗂️ Threads | 3. 🧠 Samplers | 4. 📝 Prompts |
| :---: | :---: | :---: | :---: |
| <img src="https://github.com/user-attachments/assets/511c6573-b91e-4cb8-ac9e-ce428757d65b" width="525" alt="Main Chat" /> | <img src="https://github.com/user-attachments/assets/055f47ca-8874-4028-8af2-1701cd467368" width="525" alt="Threads" /> | <img src="https://github.com/user-attachments/assets/794364b7-c0d8-47b2-a057-9012f9f5a8ca" width="525" alt="Samplers" /> | <img src="https://github.com/user-attachments/assets/ec6da647-efef-4110-bb54-b6fa9347f988" width="525" alt="Prompts" /> |

| 5. ⚡ Agents | 6. 📱 App Settings | 7. 💾 Backup & Data | 8. 🔍 Inspector |
| :---: | :---: | :---: | :---: |
| <img src="https://github.com/user-attachments/assets/75a9b663-a3cb-4b51-a6b5-85cc1522bd93" width="525" alt="Agents" /> | <img src="https://github.com/user-attachments/assets/ed8a7a5d-a813-457c-ae89-6636d4fd88ba" width="525" alt="App Settings" /> | <img src="https://github.com/user-attachments/assets/27d0f919-3545-439a-904a-b7c4e1ce44c8" width="525" alt="Backup & Data" /> | <img src="https://github.com/user-attachments/assets/05744536-c7e7-480f-ad18-ffe3480da988" width="525" alt="Payload Inspector" /> |
