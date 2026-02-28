# Musicon - Automated Mashup Generator

Musicon is a Flask-based web application that generates custom audio mashups and delivers them directly to the user via email as a ZIP file.
This project demonstrates backend automation, audio processing, file handling, email integration, and cloud deployment.

---

## UI Preview

![UI Preview](static/UI.png)

## Features

- Generate mashups from multiple songs
- Custom duration selection
- Automatic ZIP file creation
- Email delivery of mashup file
- Modern glassmorphism UI
- Cloud deployment support

---

## Tech Stack

### Backend
- Python
- Flask
- MoviePy
- yt-dlp
- SMTP (Gmail)

### Frontend
- HTML
- CSS (Glassmorphism design)

### Deployment
- Render
- Gunicorn

---

## Methodology

### 1. Input Collection

The user provides:
- Singer name
- Number of songs
- Duration (in seconds)
- Email address

The system validates inputs and email format before processing.

---

### 2. Audio Processing

- Songs are downloaded or processed.
- Each audio clip is trimmed to the specified duration.
- Clips are merged using MoviePy.
- Final mashup is generated in `.mp3` format.

---

### 3. File Packaging

- The generated MP3 file is compressed into a ZIP file.
- The file name is dynamically generated using the singer's name.

Example:

```
Arijit_Singh_mashup.zip
```

---

### 4. Email Automation

- Secure SMTP connection is established using Gmail App Password.
- ZIP file is attached automatically.
- Mashup is delivered to the user's email.

---

### 5. Deployment Workflow

- Code pushed to GitHub.
- Connected to Render.
- Gunicorn used as WSGI server.
- Environment variables configured securely.

---

## Environment Variables

The following environment variables must be configured:

```
SENDER_EMAIL=your_email@gmail.com
APP_PASSWORD=your_app_password
```

---

## Learning Outcomes

This project demonstrates:
- Backend application development
- Audio file processing
- Email automation using SMTP
- Secure environment variable handling
- Git and GitHub workflow
- Cloud deployment using Render

---

## Author

**Arushi Khanna**
Roll No: 102317147
