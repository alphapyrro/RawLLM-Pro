# RawLLM Pro

A modular web-based mini-application designed to run local language models directly within the Layla platform using hardware acceleration. Built with a structured asset pipeline featuring dedicated JavaScript runtime modules, styled CSS layers, and structured JSON configuration schemas.

---

**Installation & Setup**

1. Download the latest **`RawLLM-Pro-v7.5.0.zip`** package from the Releases page (`https://github.com/alphapyrro/RawLLM/releases`).
2. Open **Layla** and navigate to **Your Apps**.
3. Tap the **`+`** icon in the top right corner to open **Browse Apps**.
4. Tap **Import** in the top right corner.
5. Select **Zip File** and choose the downloaded `.zip` file.
6. Scroll down to the **Custom** section at the bottom and tap the blue **`+`** icon next to **RawLLM Pro** to finalize adding it.
7. Launch RawLLM Pro directly from the list or find it inside your **Your Apps** hub.

---

**What's New in v7.5.0**

### ✨ New Features
* 💾 **Incremental Stream Persistence:** Stream progress is now flushed to storage periodically to prevent data loss if the app is closed or interrupted mid-generation.
* 📌 **Persistent Last-Active Chat Memory:** The app now reliably reopens your exact last-active conversation across restarts and cache clears via dual-layer disk persistence.
* ❌ **Dedicated Settings Dismiss Button:** Added a fixed, quick-access close button to the top header of the settings drawer across all five tabs.
* 🔤 **Adjustable Chat Font Scale:** Customize message font size in real time via the App settings tab for improved readability and accessibility.
* 📊 **Generation Performance HUD Toggle:** Added an interface switch to easily show or hide the live generation statistics overlay (t/s, TTFT, total time, token count).
* ⏱️ **Configurable Message Timestamps:** Added optional timestamp displays supporting both 12-hour and 24-hour formats on conversation bubbles.
* 🔄 **App Preferences Factory Reset:** Added a dedicated reset control to restore interface and display preferences to factory defaults without affecting chat history or presets.
* 👆 **Click-Outside Settings Dismissal:** Tapping outside the active settings drawer now automatically closes the menu.
* ⏳ **Animated Generation Pre-loader:** Added a responsive pulsing indicator while the model initializes until the first token stream begins.

---

### 🛠️ Bug Fixes & Improvements
* ⚡ **KV Cache & Prompt Latency Optimization:** Stabilized dynamic prompt parameters to prevent full context evictions and eliminate prefill stalls across repeated turns.
* 🧠 **Context Budgeting & Static Prefix Retention:** Implemented active sliding-window budget truncation while anchoring the root message to keep memory within bounds without thrashing the KV cache.
* 🛑 **Abort State & Bubble Retention:** Fixed an issue where stopping an active stream prematurely hid or removed the message bubble, ensuring partial text is cleanly finalized.
* 🔒 **Auto-Scroll Sensitivity Calibration:** Reinforced the auto-scroll lock threshold against micro-touches and accidental drag interactions while streaming.
* 🎛️ **Factory Preset Sampler Synchronization:** Resolved an issue where selecting the factory Default environment preset failed to reset sampler controls to true out-of-the-box defaults.
* 🧹 **Code & Event Handler Cleanup:** Removed legacy, unmapped function calls from settings tab listeners to ensure clean execution with zero silent background exceptions.

---

**Interface & Features**

| 1. 💬 Main Chat & HUD | 2. 🗂️ Thread Manager | 3. 🧠 Samplers & Tuning | 4. 📝 Prompts & Stops |
| :---: | :---: | :---: | :---: |
| <img width="522" height="1024" alt="mainChat" src="https://github.com/user-attachments/assets/2b496ad2-9ed4-4db9-ab63-a3b70c24daaf" /> | <img width="520" height="1024" alt="allChats" src="https://github.com/user-attachments/assets/e7f87709-6e12-4cb0-bec9-3026f39b68e5" /> | <img width="525" height="1024" alt="Imagepipe_2" src="https://github.com/user-attachments/assets/d62e7a70-d259-439a-83d8-b858c77e1c2d" /> | <img width="525" height="1024" alt="Imagepipe_3" src="https://github.com/user-attachments/assets/4bc9da58-f97b-4d77-9741-d5d940e45637" /> |

| 5. ⚡ Web & Agents | 6. 📱 App Settings | 7. 💾 Backup & Data | 8. 🔍 Payload Inspector |
| :---: | :---: | :---: | :---: |
| <img width="525" height="1024" alt="Imagepipe_4" src="https://github.com/user-attachments/assets/6be76a55-940b-489a-9382-12a933233ddb" /> | <img width="524" height="1024" alt="appSett" src="https://github.com/user-attachments/assets/9cf2b3f8-4789-4f31-ad2a-0140d98028de" /> | <img width="525" height="1024" alt="Imagepipe_6" src="https://github.com/user-attachments/assets/9d148489-02ac-4eff-b235-cf8fe70093bd" /> | <img width="525" height="1024" alt="Imagepipe_7" src="https://github.com/user-attachments/assets/a636b3e8-f428-4bd4-93f6-cfca0da8bcce" /> |
