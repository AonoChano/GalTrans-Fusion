# GalTrans-Fusion 

**[Author]**   AonoChano  
**[Version]**  v2.2  
**[GitHub]**   [github.com/AonoChano](https://github.com/AonoChano)

A real-time OCR translation tool for Galgames and Visual Novels, powered by local Ollama vision models and the DeepSeek API. It allows you to select any part of your screen, recognize Japanese text, and translate it into Chinese on the fly.

![demo_image_placeholder.png](https://user-images.githubusercontent.com/AonoChano/GalTrans-Fusion/assets/placeholder.png)  <!-- It's recommended to add a GIF or screenshot of the tool in action -->

---

### Core Features

-   **On-the-fly Translation**: Press a hotkey to instantly OCR and translate text within a selected area.
-   **Persistent & Adjustable Selection**: Select the game's text box once. The selection area remains on screen and can be moved or resized at any time.
-   **High-Quality AI Services**:
    -   **OCR**: Utilizes any [Ollama](https://ollama.com/) compatible multimodal model (e.g., LLaVA) running locally for privacy and control.
    -   **Translation**: Leverages the powerful [DeepSeek API](https://www.deepseek.com/) for accurate, context-aware translations tailored for games.
-   **Customizable Hotkeys**: Set any keyboard combination or even extra mouse buttons (side buttons) as the translation trigger.
-   **Interactive UI**:
    -   A simple control panel for initial setup.
    -   A draggable result window to display translations.
    -   An "Area Edit" mode to toggle between adjusting the capture zone and clicking through it to interact with the game.
-   **User-Friendly Configuration**: All settings, including API keys and hotkeys, are managed through a clean GUI and saved locally.

### Prerequisites

1.  **Python**: Python 3.8 or newer.
2.  **Ollama**: You must have [Ollama](https://ollama.com/) installed and running on your local machine.
3.  **Ollama Vision Model**: You need a multimodal vision model pulled in Ollama. The default is `llava:7b`. You can get it by running:
    ```bash
    ollama pull llava:7b
    ```
4.  **DeepSeek API Key**: A valid API key from [DeepSeek](https://platform.deepseek.com/).

### Installation & Usage

1.  **Download**: Clone or download the repository ZIP file and extract it.
    ```bash
    git clone https://github.com/AonoChano/GalTrans-Fusion.git
    cd GalTrans-Fusion
    ```
2.  **Run the Application**: Double-click the `main.py` or run it from your terminal. The script will automatically detect and install any missing Python libraries.
    ```bash
    python main.py
    ```
3.  **Initial Setup**:
    -   The main window will appear. Click the **"Settings"** button.
    -   Enter your **DeepSeek API Key**.
    -   Verify the **Ollama API URL** and **Model Name** are correct.
    -   Click **"Set"** to define a new hotkey for triggering translations. Press your desired key combination or click a mouse side-button in the pop-up dialog.
    -   Save your settings.

4.  **Select Translation Area**:
    -   Click the **"Select Translation Area"** button.
    -   Your screen will dim. Click and drag to draw a box around the area where game text appears.
    -   A blue dashed overlay will now persistently mark this area.

5.  **Translate!**:
    -   A result window will appear. Drag it to a convenient, non-overlapping location.
    -   Start your game. Whenever new text appears, press your configured **hotkey**. The translation will show up in the result window.
    -   Alternatively, you can click the "Translate" button inside the result window (if enabled).

6.  **Adjusting the Area**:
    -   In the result window, check the **"Area Edit"** checkbox.
    -   You can now click and drag the blue overlay's borders or corners to resize it, or drag its center to move it.
    -   Uncheck "Area Edit" to allow mouse clicks to pass through the overlay to the game.

### For Developers

Enable **"Developer Mode"** in the settings to print detailed debug logs to the console. This is useful for troubleshooting issues with API connections or the OCR/translation process.

### License

This project is licensed under the [Apache-2.0 License](LICENSE).

