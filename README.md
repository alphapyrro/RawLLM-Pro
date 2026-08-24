# RawLLM Pro

A modular web-based mini-application designed to run local language models directly within the Layla platform using hardware acceleration. Built with a structured asset pipeline featuring dedicated JavaScript runtime modules, styled CSS layers, and structured JSON configuration schemas.

---

**Installation & Setup**

1. Download the latest **`RawLLM-Pro-v7.6.2.zip`** package from the Releases page (`https://github.com/alphapyrro/RawLLM/releases`).
2. Open **Layla** and navigate to **Your Apps**.
3. Tap the **`+`** icon in the top right corner to open **Browse Apps**.
4. Tap **Import** in the top right corner.
5. Select **Zip File** and choose the downloaded `.zip` file.
6. Scroll down to the **Custom** section at the bottom and tap the blue **`+`** icon next to **RawLLM Pro** to finalize adding it.
7. Launch RawLLM Pro directly from the list or find it inside your **Your Apps** hub.

---

**What's New in v7.6.2**

### ✨ New Features & Enhancements
* ☕ **Official Ko-fi Support Links:** Added direct one-tap donation buttons in the Data Settings tab and the sidebar footer for users who want to support ongoing updates, new features, and local AI experiments.
* 🎙️ **Complete Voice-to-Text Architecture Overhaul:** Fully resolves speech recognition reliability by hardening silence detection, fixing native Android silence dropout reconnections, eliminating duplicate transcription echoes, and preventing accidental state desyncs.
* 📦 **SQLite Full Backup & Multi-Turn Restore:** Resolved an issue where exports only captured thread metadata; backups now query and package all message history turns, ensuring complete multi-turn conversation recovery across SQLite restores.
* 🏷️ **Custom Backup File Tagging:** Added an optional custom labeling prompt when creating system backups, enabling easy identifier tags (e.g., `_my_tag`) while supporting one-tap default exports.
* 🔇 **Zero-Feedback Acoustic Echo Guard:** Implemented synchronous suppression of STT processing while Text-to-Speech audio is actively playing, preventing the microphone from capturing the AI's voice output and causing false input loops.
* 📜 **Real-Time Dictation Auto-Scroll:** Added active auto-scroll tracking to the main input dock to automatically scroll the textarea downward as you dictate, keeping the active text horizon continuously in view for long hands-free inputs.

---

### 🛠️ Bug Fixes & Stability
* ⏳ **Queue & Voice Handoff Hardening:** Fixed a race condition where queued messages vanished into a limbo state while Text-to-Speech was speaking; queued prompts now remain visible, editable, and cancelable in the queue banner until speech concludes.
* 🛑 **Decoupled Master Stop & Send Lifecycle:** Automatically hides the master red Stop control the instant text generation completes, seamlessly restoring the interactive Send and Queue buttons during speech playback.
* 🔄 **UI Queue Reactivity:** Fixed stale button state bugs by ensuring `updateQueueUI()` fires immediately upon global audio termination or natural speech completion.
* 🧹 **Clean Bridge Event Handling:** Streamlined native bridge message passing with integrated feature flags for lightweight diagnostics.

---

**Interface & Features**

| 1. 💬 Main Chat & HUD | 2. 🗂️ Thread Manager | 3. 🧠 Samplers & Tuning | 4. 📝 Prompts & Stops |
| :---: | :---: | :---: | :---: |
| <img width="522" height="1024" alt="mainChat" src="https://github.com/user-attachments/assets/2b496ad2-9ed4-4db9-ab63-a3b70c24daaf" /> | <img width="524" height="1024" alt="chatThreads" src="https://github.com/user-attachments/assets/ff2cfd30-6cda-4cc8-b34b-f809bfc8dfd9" /> | <img width="525" height="1024" alt="Imagepipe_2" src="https://github.com/user-attachments/assets/d62e7a70-d259-439a-83d8-b858c77e1c2d" /> | <img width="525" height="1024" alt="Imagepipe_3" src="https://github.com/user-attachments/assets/4bc9da58-f97b-4d77-9741-d5d940e45637" /> |

| 5. ⚡ Web & Agents | 6. 📱 App Settings | 7. 💾 Backup & Data | 8. 🔍 Payload Inspector |
| :---: | :---: | :---: | :---: |
| <img width="525" height="1024" alt="Imagepipe_4" src="https://github.com/user-attachments/assets/6be76a55-940b-489a-9382-12a933233ddb" /> | <img width="526" height="1024" alt="appSett" src="https://github.com/user-attachments/assets/c2a43d5a-3d04-4b59-8258-3ed5142d3758" /> | <img width="525" height="1024" alt="Imagepipe_6" src="https://github.com/user-attachments/assets/9d148489-02ac-4eff-b235-cf8fe70093bd" /> | <img width="525" height="1024" alt="Imagepipe_7" src="https://github.com/user-attachments/assets/a636b3e8-f428-4bd4-93f6-cfca0da8bcce" /> |
