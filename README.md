# 🎤 Real-Time Speech Translator (English ↔ Telugu)

A Python-based real-time speech recognition and translation system that listens to your voice, translates it between **English and Telugu**, and speaks the translated output.

---

## 🚀 Features

- 🎙️ Continuous speech recognition
- 🌐 Real-time translation:
  - English → Telugu
  - Telugu → English
- 🔊 Text-to-speech output
- 🔁 Voice commands to switch languages
- 🛑 Voice command to stop the program
- ⚡ Background listening (non-blocking)

---

## 🧠 How It Works

1. Captures audio from your microphone  
2. Converts speech to text using Google Speech Recognition  
3. Translates text using Google Translator  
4. Converts translated text into speech using gTTS  
5. Plays the translated audio  

---

## 🛠️ Technologies Used

- `speech_recognition`
- `deep_translator`
- `gTTS`
- `playsound`
- `pyaudio`

---

## 📦 Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-username/speech-translator.git
cd speech-translator
```

### 2. Install dependencies
```bash
pip install speechrecognition deep-translator gtts playsound pyaudio
```

> ⚠️ Note: Installing `pyaudio` may require additional setup:
- **Windows:** Install precompiled wheel
- **Linux:**  
  ```bash
  sudo apt install portaudio19-dev
  ```
- **macOS:**  
  ```bash
  brew install portaudio
  ```

---

## ▶️ Usage

Run the script:

```bash
python main.py
```

---

## 🎯 Voice Commands

| Command | Action |
|--------|--------|
| "switch to English" | Translate English → Telugu |
| "switch to Telugu" | Translate Telugu → English |
| "stop" | Exit the program |

---

## 📌 Example

**Input:**  
```
Hello, how are you?
```

**Output:**  
- Printed: Telugu translation  
- Spoken: Telugu audio  

---

## ⚠️ Known Issues

- Requires stable internet connection
- Background noise may affect accuracy
- Small bug in Telugu mode switching (see fix below)

---

## 🧩 Bug Fix

Update this part in your code:

```python
elif cmd in ["switch to telugu","స్విచ్ టు తెలుగు"]:
    language_mode = "te-IN"
```

---

## 📁 Project Structure

```
speech-translator/
│
├── main.py
├── README.md
└── temp_audio.mp3  (generated at runtime)
```

---

## 🤝 Contributing

Pull requests are welcome! Feel free to open issues for suggestions or bugs.

---

## 📜 License

This project is licensed under the MIT License.
