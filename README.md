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

# 🚀 RawLLM Pro v7.5.0

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
| <img width="465" height="1024" alt="1mainChat" src="https://github.com/user-attachments/assets/0c9e84b4-3022-42ae-bd2c-9b21660397cb" /> | <img width="465" height="1024" alt="2chatManifest" src="https://github.com/user-attachments/assets/e1717288-85c2-4493-a650-714c4536797e" /> | <img width="465" height="1024" alt="3samplers" src="https://github.com/user-attachments/assets/82b23c6e-925b-47ef-ac64-a3cc199a72db" /> | <img width="465" height="1024" alt="4prompts" src="https://github.com/user-attachments/assets/a42a4701-11d0-4280-a1c0-c25fc18b990a" /> |

| 5. ⚡ Web & Agents | 6. 📱 App Settings | 7. 💾 Backup & Data | 8. 🔍 Payload Inspector |
| :---: | :---: | :---: | :---: |
| <img width="465" height="1024" alt="5agents" src="https://github.com/user-attachments/assets/a5433552-297e-4ac7-813a-5a34aed423df" /> | <img width="465" height="1024" alt="6appSettings" src="https://github.com/user-attachments/assets/e917759c-91e7-42e9-9b78-528c876d2b38" /> | <img width="465" height="1024" alt="7dataTab" src="https://github.com/user-attachments/assets/1cb99992-2b6e-497b-abab-0940e081120e" /> | <img width="465" height="1024" alt="8apiInspector" src="https://github.com/user-attachments/assets/440f6034-0487-4e8e-b41e-1644c24f8624" /> |
