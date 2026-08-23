# RawLLM Pro

A modular web-based mini-application designed to run local language models directly within the Layla platform using hardware acceleration. Built with a structured asset pipeline featuring dedicated JavaScript runtime modules, styled CSS layers, and structured JSON configuration schemas.

---

**Installation & Setup**

1. Download the latest **`RawLLM-Pro-v7.6.0.zip`** package from the Releases page (`https://github.com/alphapyrro/RawLLM/releases`).
2. Open **Layla** and navigate to **Your Apps**.
3. Tap the **`+`** icon in the top right corner to open **Browse Apps**.
4. Tap **Import** in the top right corner.
5. Select **Zip File** and choose the downloaded `.zip` file.
6. Scroll down to the **Custom** section at the bottom and tap the blue **`+`** icon next to **RawLLM Pro** to finalize adding it.
7. Launch RawLLM Pro directly from the list or find it inside your **Your Apps** hub.

---

**What's New in v7.6.0**

### ✨ New Features
* 🎙️ **Voice & Speech Controls (Beta):** Adds hands-free voice chat with automatic text-to-speech playback, customizable dictation modes (pause detection, push-to-talk, manual), voice engine selection, and dedicated audio playback stop controls.
* ✂️ **Context Pruning & Memory Horizon Visualizer:** Real-time token budgeting visualizer dims pruned messages that exceed the context budget, labels trimmed history with a `✂️ Pruned` badge, and renders an active memory horizon divider in the chat viewport.
* ⏳ **Smart Message Queueing & Draft Protection:** Queue a follow-up message while generation is actively running via the dynamic `⏳` button. Includes single-slot queue buffering, cross-thread handoff upon completion, Master Halt (`⏹`) draft preservation, and non-destructive unqueueing (`✕`) that merges safely with in-progress text.
* 📥 **Single-Thread Import & Dual-Format Export:** Adds a dedicated sidebar button to import individual `.json`, `.md`, or `.txt` conversations, alongside per-message `💾 Export JSON` (full backup) and `📄 Export MD` (formatted document) export options.
* 🧠 **Floating Sampler Preset Quick-Menu:** Quick-access floating `🧠` button allows instant switching between saved sampler presets from anywhere in the app without opening the settings drawer (toggleable in App Settings).
* 💾 **SQLite Database Auto-Migration:** Automatically migrates conversation storage from individual flat JSON files to a unified SQLite database (`app.db`) for improved performance, data integrity, and instant thread loading.
* 📦 **Updated Core SDK Bridge:** Upgraded internal Layla SDK and bridge integration layers to the latest version.

---

### 🛠️ Bug Fixes & Improvements
* ⚡ **Non-Blocking Thread Navigation & Streaming:** Upgraded bridge architecture to allow instant new chat creation (`+ New Chat`), uninterrupted thread switching, and sidebar navigation while streaming continues in the background.
* 🚀 **Engine Performance & Latency Optimization:** Eliminated internal bridge bottlenecks to drastically reduce Time-to-First-Token (TTFT), resolve long loading times, and improve tokens-per-second throughput.
* 🛑 **Token Limit Enforcement:** Fixed an issue where text generation continued streaming past the client-side configured maximum token ceiling.
* 🔀 **True Conversation Forking:** Fixed a critical issue where editing a prior message deleted or overwrote the original conversation thread instead of branching a new fork.
* 🛡️ **Stream Thread Deletion Safeguards:** Prevented chat thread deletions while a generation is actively running to prevent database desynchronization and ghost threads.
* 🔄 **Dynamic Retry Button Visibility:** Corrected retry button persistence so it appears exclusively on the single latest assistant response and disappears immediately once a new user message is submitted.
* 💡 **Hardware Engine Allocation Guidance:** Added an in-app notice clarifying that Max Tokens and Context Window settings in RawLLM Pro cannot exceed the allocations configured in Layla's native model settings.

---

**Interface & Features**

| 1. 💬 Main Chat & HUD | 2. 🗂️ Thread Manager | 3. 🧠 Samplers & Tuning | 4. 📝 Prompts & Stops |
| :---: | :---: | :---: | :---: |
| <img width="522" height="1024" alt="mainChat" src="https://github.com/user-attachments/assets/2b496ad2-9ed4-4db9-ab63-a3b70c24daaf" /> | <img width="524" height="1024" alt="chatThreads" src="https://github.com/user-attachments/assets/ff2cfd30-6cda-4cc8-b34b-f809bfc8dfd9" /> | <img width="525" height="1024" alt="Imagepipe_2" src="https://github.com/user-attachments/assets/d62e7a70-d259-439a-83d8-b858c77e1c2d" /> | <img width="525" height="1024" alt="Imagepipe_3" src="https://github.com/user-attachments/assets/4bc9da58-f97b-4d77-9741-d5d940e45637" /> |

| 5. ⚡ Web & Agents | 6. 📱 App Settings | 7. 💾 Backup & Data | 8. 🔍 Payload Inspector |
| :---: | :---: | :---: | :---: |
| <img width="525" height="1024" alt="Imagepipe_4" src="https://github.com/user-attachments/assets/6be76a55-940b-489a-9382-12a933233ddb" /> | <img width="526" height="1024" alt="appSett" src="https://github.com/user-attachments/assets/c2a43d5a-3d04-4b59-8258-3ed5142d3758" /> | <img width="525" height="1024" alt="Imagepipe_6" src="https://github.com/user-attachments/assets/9d148489-02ac-4eff-b235-cf8fe70093bd" /> | <img width="525" height="1024" alt="Imagepipe_7" src="https://github.com/user-attachments/assets/a636b3e8-f428-4bd4-93f6-cfca0da8bcce" /> |
