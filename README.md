# Virtual Assistant (Python)

A desktop voice assistant built in Python. It listens through your mic, responds
with speech, and handles a handful of everyday commands — search Wikipedia, open
sites, tell the time, play music, and send email.

## Features

Speak any of these after it starts listening:

| Say | It does |
|-----|---------|
| "... wikipedia" | Reads a 2-sentence Wikipedia summary aloud |
| "open youtube" | Opens YouTube |
| "open google" | Opens Google |
| "open stackoverflow" | Opens Stack Overflow |
| "play music" | Plays music from a local folder |
| "the time" | Tells the current time |
| "open code" | Launches VS Code |
| "email to ..." | Sends an email via Gmail SMTP |

It greets you based on the time of day on startup.

## Requirements

```bash
pip install pyttsx3 SpeechRecognition wikipedia
```

You'll also need a working microphone and `PyAudio` for `SpeechRecognition`
(`pip install pyaudio`, or install it via your OS package manager if the pip
build fails). `pyttsx3` uses SAPI5, so text-to-speech works out of the box on
Windows.

## Usage

```bash
python Assistant.py
```

It starts listening immediately. Speak a command from the table above.

## Configuration

- **Email:** the `sendEmail()` function uses Gmail SMTP. Set your own sender
  address and an [app password](https://support.google.com/accounts/answer/185833)
  — don't use your real account password, and never commit it. Move both into
  environment variables before using this for real.
- **Music:** point the `play music` handler at your own music directory.

## License

MIT © Apoorva Verma
