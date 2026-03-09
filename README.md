# CodeMentor AI

CodeMentor AI is an intelligent full-stack web application that helps users learn, practice, and improve their coding skills using advanced AI tools. It includes an AI-powered code editor, voice-to-code functionality, coding challenges, progress tracking, and user profile management.

---
## Features

- **AI Code Editor**  
  Write, debug, and improve code with real-time AI assistance. Supports Python, JavaScript, Java, C++, and C.

- **Voice-to-Code**  
  Generate code or prompts using your voice with speech-to-text technology.

- **Coding Challenges**  
  Practice coding problems with different difficulty levels and get instant feedback.

- **User Profiles**  
  Save code snippets, track solved challenges, and manage preferences such as dark mode.

- **Progress Dashboard**  
  Visualize coding progress and performance statistics.

- **Authentication System**  
  Secure registration, login, and password reset through email verification.

- **Modern User Interface**  
  Responsive design with light and dark theme support.

---

## Tech Stack

**Backend**
- Python
- Flask
- Flask-SQLAlchemy
- Flask-Login

**Frontend**
- HTML
- CSS
- Bootstrap
- Jinja2 Templates
- CodeMirror
- Chart.js

**AI / ML**
- Google Gemini API
- OpenAI Whisper (Speech-to-text)

**Database**
- PostgreSQL (or any SQLAlchemy compatible database)

**Other Tools**
- dotenv
- SMTP (for email services)

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd codementor_ai
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure Environment Variables

Create a `.env` file in the project root directory and add:

```bash
DATABASE_URL=postgresql://user:password@localhost:5432/codementor_ai
GOOGLE_API_KEY=your_google_gemini_api_key
SMTP_SERVER=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASSWORD=your_email_password
FROM_EMAIL=your_email@gmail.com
```

### 4. Database Setup

Create the database and tables:

```bash
psql -d codementor_ai -f create_tables.sql
```

### 5. Seed Coding Challenges

```bash
python seed.py
```

### 6. Run the Application

```bash
python -m app.run
```

Open your browser and visit:

```
http://localhost:5000
```

---

## Usage

1. Register a new account or log in.
2. Use the **AI Code Editor** to write and improve your code.
3. Generate code using **voice commands**.
4. Solve **coding challenges** and track your progress.
5. Save useful **code snippets** in your profile.
6. Switch between **light and dark themes**.

---

## Project Structure

```
codementor_ai/
│
├── app/
│   ├── __init__.py
│   ├── run.py
│   ├── models.py
│   ├── seed_challenges.py
│   ├── static/
│   └── templates/
│
├── config.py
├── create_tables.sql
├── requirements.txt
└── seed.py
```

---

## Data Models

- **User_details**  
  Stores user information, email, password (hashed), preferences, and saved snippets.

- **Snippet**  
  Stores saved code snippets for each user.

- **Challenge**  
  Contains coding challenges with starter code and test cases.

- **UserChallengeProgress**  
  Tracks attempts, solutions, and feedback for each challenge.

---

## Important Files

- `app/run.py` → Main Flask application and routes  
- `app/models.py` → Database models  
- `app/seed_challenges.py` → Challenge data seeding  
- `app/templates/` → HTML templates  
- `app/static/` → CSS and static resources  
- `create_tables.sql` → Database schema  
- `requirements.txt` → Project dependencies  

---

## AI & Voice Features

**AI Code Assistance**
- Uses Google Gemini API for:
  - Code explanation
  - Bug detection
  - Code improvements

**Voice-to-Code**
- Uses OpenAI Whisper to convert speech into text for generating coding prompts.

---

## Security

- Password hashing using Werkzeug
- Secure session management with Flask-Login
- Password reset using secure email tokens

---

## Customization

You can extend the project by:

- Adding more coding challenges in `app/seed_challenges.py`
- Editing the UI in `templates/` and `static/`
- Integrating additional AI APIs

---

## License

Add your preferred license such as **MIT License** or **GPL License**.

---

## Credits

- Flask  
- Google Gemini API  
- OpenAI Whisper  
- CodeMirror  
- Bootstrap  
- Chart.js  

---

## Troubleshooting

- Install **ffmpeg** for audio conversion required by Whisper.
- Ensure your **API keys** and **database credentials** are correct in `.env`.
- If using Gmail for email features, enable **App Passwords** when using 2FA.

  ---

## Author

**K. Krishnaveni**
