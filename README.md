# RawLLM Pro

A modular web-based mini-application designed to run local language models directly within the Layla platform using hardware acceleration. Built with a structured asset pipeline featuring dedicated JavaScript runtime modules, styled CSS layers, and structured JSON configuration schemas.

---

**Installation & Setup**

1. Download the latest **`RawLLM-Pro-v7.4.0.zip`** package from the Releases page (`https://github.com/alphapyrro/RawLLM/releases`).
2. Open **Layla** and navigate to **Your Apps**.
3. Tap the **`+`** icon in the top right corner to open **Browse Apps**.
4. Tap **Import** in the top right corner.
5. Select **Zip File** and choose the downloaded `.zip` file.
6. Scroll down to the **Custom** section at the bottom and tap the blue **`+`** icon next to **RawLLM Pro** to finalize adding it.
7. Launch RawLLM Pro directly from the list or find it inside your **Your Apps** hub.

---

**What's New in v7.4.0**

* **Dedicated App Settings Tab:** Added a new 5-tab settings layout featuring persistent global controls for keyboard dismissal on send, auto-titling conversations on first send, default auto-scroll behavior, and stats HUD visibility.
* **Live Streaming & Stats HUD Stability:** Refactored streaming DOM updates so toggling stats mid-stream no longer interrupts or unmounts active assistant response bubbles.
* **Two-Way Auto-Scroll Sync:** Synchronized the chat dock's quick-lock toggle with global settings while preserving intuitive upward-drag disengagement.
* **Multi-Tab Preset Preservation:** Resolved an unmounted DOM issue ensuring active agent states are preserved when saving environment presets across different settings tabs.
* **Standardized Token Limit Defaults:** Harmonized default limits across HTML elements, runtime parameters, and fallback resets to 512 Max Tokens and a 2,048 Context Window.
* **Clean Boot Rendering:** Updated static HTML placeholders to eliminate layout shifts and context bar token count flicker during initial launch.

---

**Interface & Features**

| 1. 💬 Main Chat & HUD | 2. 🗂️ Thread Manager | 3. 🧠 Samplers & Tuning | 4. 📝 Prompts & Stops |
| :---: | :---: | :---: | :---: |
| <img width="465" height="1024" alt="1mainChat" src="https://github.com/user-attachments/assets/0c9e84b4-3022-42ae-bd2c-9b21660397cb" /> | <img width="465" height="1024" alt="2chatManifest" src="https://github.com/user-attachments/assets/e1717288-85c2-4493-a650-714c4536797e" /> | <img width="465" height="1024" alt="3samplers" src="https://github.com/user-attachments/assets/82b23c6e-925b-47ef-ac64-a3cc199a72db" /> | <img width="465" height="1024" alt="4prompts" src="https://github.com/user-attachments/assets/a42a4701-11d0-4280-a1c0-c25fc18b990a" /> |

| 5. ⚡ Web & Agents | 6. 📱 App Settings | 7. 💾 Backup & Data | 8. 🔍 Payload Inspector |
| :---: | :---: | :---: | :---: |
| <img width="465" height="1024" alt="5agents" src="https://github.com/user-attachments/assets/a5433552-297e-4ac7-813a-5a34aed423df" /> | <img width="465" height="1024" alt="6appSettings" src="https://github.com/user-attachments/assets/e917759c-91e7-42e9-9b78-528c876d2b38" /> | <img width="465" height="1024" alt="7dataTab" src="https://github.com/user-attachments/assets/1cb99992-2b6e-497b-abab-0940e081120e" /> | <img width="465" height="1024" alt="8apiInspector" src="https://github.com/user-attachments/assets/440f6034-0487-4e8e-b41e-1644c24f8624" /> |
