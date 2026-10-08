# Student Hub Online Backend

FastAPI backend for the Student Hub global leaderboard, friend requests and learning-only 1v1 challenges.

## Render
1. Put these files in a GitHub repository.
2. On Render choose **New → Web Service** and connect the repo.
3. Use the Free plan, build command `pip install -r requirements.txt`, and start command `uvicorn main:app --host 0.0.0.0 --port $PORT`.
4. Copy the resulting `https://...onrender.com` URL.
5. In the Student Hub HTML change `YOUR-STUDENT-HUB-BACKEND.onrender.com` to your real backend hostname, or set `window.STUDENT_HUB_API_BASE` before the multiplayer script.

## Database
For a quick test, the API uses SQLite in `/tmp`. Render free web services have ephemeral files, so that database is **not persistent** across restarts/spin-downs. For persistent free testing, set `DATABASE_URL` to a PostgreSQL database such as a free Supabase Postgres project. Do not put database passwords in the HTML.

## Safety design
There is no public chat, direct messaging, phone-number field, address field, or photo sharing in this MVP. Friend requests and challenges are username-based and learning-focused.
