# CHAOS_AI

**CHAOS_AI** is an advanced AI-powered desktop assistant for Windows, offering conversational intelligence, voice control, music playback, app and system automation, and more. Powered by Google Gemini, CHAOS_AI brings together a rich suite of features for productivity, entertainment, and desktop management—all configurable via a single `config.py` file.

---

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Example Commands](#example-commands)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Future Enhancements](#future-enhancements)

---

## Features

- **AI-Powered Chat:** Context-aware conversations using Google Gemini (Generative AI). Keeps persistent memory for natural, ongoing dialogue.
- **Voice Commands:** Hands-free interaction using speech recognition. Configurable timeout for audio input.
- **Text-to-Speech (TTS):** Natural voice responses powered by pyttsx3. Fully customizable voice, rate, and volume.
- **Spotify Music Control:** Play songs directly on your Spotify account and devices. Quick search and playback with error handling.
- **Web Automation:** Opens websites and performs Google searches from voice or text commands.
- **App Launcher:** Launch any installed application via Start Menu or directly using executable name.
- **App Closer:** Close running applications by name using process management.
- **System Control:** Shutdown, restart, log off, mute, and control system volume—all via simple commands.
- **Real-time Clock:** Announces the current time on request.
- **Conversation Logging:** All interactions are logged to a configurable file.
- **Persistent Chat Memory:** Chat history is stored in a JSON file for recall and context.
- **Multithreading:** Non-blocking voice and system operations for smooth, responsive experience.
- **Robust Error Handling:** Notifies user of missing configurations, API issues, and runtime errors.

---

## Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Aestheticfrog/CHAOS_AI.git
   cd CHAOS_AI
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Your Settings**
   - Copy `config_template.py` to `config.py`.
   - Fill out all API keys and preferences required (see [Configuration](#configuration) below).

---

## Configuration

All settings are managed via `config.py`. You'll need to provide API keys and set preferences for your environment.

### Example `config.py` Fields

```python
# Google Gemini API Key
apikey = "YOUR_GEMINI_API_KEY"

# Spotify API Credentials
SPOTIFY_CLIENT_ID = "your_spotify_client_id"
SPOTIFY_CLIENT_SECRET = "your_spotify_client_secret"
SPOTIFY_REDIRECT_URI = "http://localhost:8888/callback"
SPOTIFY_SCOPE = "user-library-read user-read-playback-state user-modify-playback-state"

# TTS (Text-to-Speech) Settings
TTS_VOICE_INDEX = 1       # Index of the voice in pyttsx3 (0 or 1)
TTS_RATE = 150            # Speech rate
TTS_VOLUME = 1.0          # Volume (0.0 to 1.0)

# Audio Input
AUDIO_TIMEOUT = 5         # Seconds to wait for audio input

# File Paths
CHAT_MEMORY_FILE = "chat_memory.json"         # Persistent memory
CONVERSATION_LOG_FILE = "conversation_log.txt" # Log file
```

**If `config.py` is missing or incomplete, CHAOS_AI will notify you and exit.**

---

## Usage

Start the assistant from your terminal:

```bash
python chaos.py
```

You’ll see a prompt:
```
Welcome to CHAOS AI! Type 'exit' to quit or say 'exit' during audio input.
Type your command or say 'audio' for voice input:
```

- **Type commands directly** or type `audio` to use voice input.
- **Type `exit`** or say "exit" to quit.

---

## Example Commands

- **General AI Chat:**  
  `What's the weather today?`  
  `Tell me a joke.`

- **Voice Interaction:**  
  Type `audio` and speak:  
  "Play Imagine Dragons song"  
  "Open github.com"  
  "Shutdown the computer"

- **Music Control:**  
  `play Bohemian Rhapsody song`  
  `play Shape of You`

- **Web Automation:**  
  `open wikipedia.org`  
  `search for Python tutorials on the browser`

- **App Automation:**  
  `launch Calculator`  
  `open Notepad`  
  `close Chrome`

- **System Control:**  
  `shutdown`  
  `restart`  
  `log off`  
  `increase volume`  
  `decrease volume`  
  `mute`

- **Time:**  
  `what's the time?`

---

## Troubleshooting

- **Missing `config.py`:**  
  Copy `config_template.py` to `config.py` and fill in your credentials.
- **API Key Issues:**  
  Double-check your Gemini and Spotify keys.
- **Voice Not Working:**  
  Check your pyttsx3 installation and device audio settings.
- **Spotify Device Not Found:**  
  Ensure Spotify is open and active on a device with your account.
- **Speech Recognition Fails:**  
  Make sure your microphone is connected and working.

---

## Contributing

Pull requests are welcome!  
- Please fork the repository and submit your improvements.
- For bug reports or feature requests, open an issue on [GitHub Issues](https://github.com/Aestheticfrog/CHAOS_AI/issues).

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Future Enhancements

- **Email and Calendar Integration**
- **Smart Home Control (IoT devices)**
- **Enhanced NLP for improved conversation flow**
- **Cross-platform support (Linux, macOS)**
- **User profiles and personalization**

---

**Enjoy CHAOS_AI – your intelligent, customizable desktop assistant!**
