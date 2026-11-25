# 🐍 Python Internship – 5 Projects (Beginner + Advanced)

Five Python projects built during my Python Programming internship. Every project has two levels:
a **Beginner** version (core features) and an **Advanced** version (GUI, database, APIs and extra features).

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Projects](https://img.shields.io/badge/Projects-5-green)
![Levels](https://img.shields.io/badge/Levels-Beginner%20%2B%20Advanced-orange)

---

## 📁 Projects

| # | Project | Beginner | Advanced |
|---|---------|----------|----------|
| 1 | **Voice Assistant** | Voice input, greeting, time/date, web search, text-to-speech | Intent understanding, voice email, reminders, live weather, Q&A, custom commands |
| 2 | **BMI Calculator** | Command-line BMI with category and input validation | tkinter GUI, colour-coded result, multi-user records (SQLite), BMI trend graph |
| 3 | **Password Generator** | Command-line, custom length and character types | tkinter GUI, `secrets` module, strength meter, auto-copy, last-5 history |
| 4 | **Weather App** | City/ZIP lookup, °C/°F, humidity, wind, error handling | tkinter GUI, 5-day forecast, weather icons, °C/°F toggle |
| 5 | **Chat Application** | Two-user socket chat with timestamps | GUI chat with login, multiple rooms, message history (SQLite) |

## 🗂️ Folder Structure

```
python_internship/
├── README.md
├── requirements.txt
├── task1_voice_assistant/
│   ├── beginner.py
│   ├── advanced.py
│   ├── custom_commands.json
│   └── knowledge_base.json
├── task2_bmi_calculator/
│   ├── beginner.py
│   └── advanced.py
├── task3_password_generator/
│   ├── beginner.py
│   └── advanced.py
├── task4_weather_app/
│   ├── beginner.py
│   └── advanced.py
└── task5_chat_app/
    ├── beginner_server.py
    ├── beginner_client.py
    ├── advanced_server.py
    └── advanced_client.py
```

## ⚙️ Installation

```bash
git clone https://github.com/<your-username>/python-internship-5-projects.git
cd python-internship-5-projects
pip install -r requirements.txt
```

> **Linux:** `sudo apt install python3-tk portaudio19-dev`
> **Windows/Mac:** tkinter comes with Python. If `PyAudio` fails to install, try `pip install pipwin && pipwin install pyaudio` (Windows).

## ▶️ How to Run

### Task 1 – Voice Assistant
```bash
cd task1_voice_assistant
python beginner.py
python advanced.py            # voice mode
python advanced.py --text     # type instead of speaking (no microphone needed)
```
Try: *"hello"*, *"what is the time"*, *"search for Python tutorials"*, *"remind me in 2 minutes"*, *"weather in Delhi"*.

### Task 2 – BMI Calculator
```bash
cd task2_bmi_calculator
python beginner.py
python advanced.py
```

### Task 3 – Password Generator
```bash
cd task3_password_generator
python beginner.py
python advanced.py
```

### Task 4 – Weather App
Get a free API key from [openweathermap.org](https://openweathermap.org/api) and set it:
```bash
# Windows (CMD)
set OPENWEATHER_API_KEY=your_key_here
# Linux / Mac
export OPENWEATHER_API_KEY=your_key_here

cd task4_weather_app
python beginner.py
python advanced.py
```
> New API keys can take 1–2 hours to activate.

### Task 5 – Chat Application
Start the **server first**, then open two (or more) client windows.
```bash
cd task5_chat_app

# Beginner
python beginner_server.py
python beginner_client.py      # run in 2 terminals

# Advanced
python advanced_server.py
python advanced_client.py      # run in 2+ windows: Register -> Login -> pick a room
```

## ✨ Key Features

- **Input validation** and graceful error handling in every project
- **SQLite** database for BMI records and chat history
- **Secure password generation** with the `secrets` module and guaranteed character types
- **Threaded socket server** with real-time messaging, rooms and disconnect notifications
- **PBKDF2-hashed passwords** for chat login (never stored in plain text)
- **API keys via environment variables**, never hard-coded

## 🔒 Privacy Note (Voice Assistant)

- Audio is recorded only while the assistant shows "Listening..." and is sent to Google's free Web Speech API
  (`recognize_google`) to convert it to text. No audio is saved on disk.
- Weather requests send only the city name to OpenWeatherMap; Q&A fallback sends the topic to Wikipedia.
- Email uses a test account; credentials are read from environment variables (`SMTP_USER`, `SMTP_PASS`).
- `custom_commands.json` is stored locally and contains only the phrases you add.

## 🛠️ Tech Stack

Python · tkinter · SQLite3 · socket & threading · requests · speech_recognition · pyttsx3 · matplotlib · Pillow · pyperclip · OpenWeatherMap API

## 👨‍💻 Author

**Rahul Pal** – BCA Student
🔗 LinkedIn: `<add your LinkedIn link>`
🐙 GitHub: `<add your GitHub link>`

## 📜 License

This project is for educational purposes (internship submission).

