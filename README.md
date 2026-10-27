# Secure Login System — Mini Project

A Flask web application demonstrating user registration, secure password hashing, input validation, parameterized SQL queries, session-based authentication, protected dashboard access, and logout.

## Requirements
- Python 3.9+
- Flask (installed from `requirements.txt`)

## Run on Windows
1. Extract this ZIP.
2. Open Command Prompt in the project folder.
3. Run:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   pip install -r requirements.txt
   python app.py
   ```
4. Open `http://127.0.0.1:5000` in your browser.
5. Create an account, log in, and test the protected dashboard and logout.

## Run on macOS/Linux
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python3 app.py
```
Then open `http://127.0.0.1:5000`.

## Security notes
- Passwords are hashed with Werkzeug's scrypt password hashing.
- SQL statements use placeholders (parameterized queries).
- Flask session cookies are HttpOnly and SameSite=Lax.
- For production deployment, set a strong `SECRET_KEY`, enable HTTPS, set `COOKIE_SECURE=1`, use CSRF protection and rate limiting, and deploy with a production WSGI server. This educational demo does not implement 2FA or a full CSRF defense.
- Do not use the built-in Flask development server for production.
