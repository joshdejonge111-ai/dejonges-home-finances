
# DeJonge Home Finances — Premium Forest Edition

A multi-user financial dashboard for home finances, featuring automatic ingest, paystub upload, and beautiful forest-green design inspired by the Oregon coastline.

![App Screenshot](https://via.placeholder.com/900x400?text=Demo+Screenshot) <!-- Replace with your real screenshot -->

## Features

- Secure multi-user login
- Financial dashboard with charts, widgets, swipe cards
- Paystub upload (CSV/QFX/PDF) with auto-net detection
- Nightly ingest & projections
- Export to ICS & CSV
- Forest-green, calming UI (Apple/Nike-inspired)
- Ready for deployment with Render, Heroku, Fly.io

---

## Quick Demo Launch

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy)

---

## Getting Started

### 1. Local Setup

```bash
git clone https://github.com/joshdejonge111-ai/dejonges-home-finances.git
cd dejonges-home-finances
# Create and activate a virtualenv if desired
pip install -r requirements.txt
python app.py
```
Visit [http://localhost:5000](http://localhost:5000)

### 2. Deployment (Render Recommended)

- Go to [Render.com](https://render.com)
- Click "New Web Service" → "Connect GitHub"
- Select your repo: dejonges-home-finances
- Use `render.yaml` for auto config
- Set environment variables:
  - `FLASK_SECRET_KEY`
  - `ADMIN_EMAIL`
  - `ADMIN_PASSWORD_HASH` (generate with: `python -c "from werkzeug.security import generate_password_hash as g; print(g('YourStrongPassword'))"`)
  - `SCHEDULER_DAILY_HHMM` (optional, e.g., `03:00`)
- Click Deploy!

### 3. Fly.io / Heroku Deployment

See `fly.toml`, `Procfile`, and instructions below for alternate platforms.

---

## Tech Stack

- **Backend:** Flask (Python)
- **Frontend:** HTML, CSS, JS, React (landing page in `/client`)
- **Deployment:** Docker, Render, Fly.io, Heroku

## Folder Structure

```
/
├── app.py
├── requirements.txt
├── Procfile
├── render.yaml
├── runtime.txt
├── static/
├── templates/
├── client/              # React landing page
└── README.md
```

## License

MIT

---

## Contact

For questions, support, or demo requests: [joshdejonge111@gmail.com](mailto:joshdejonge111@gmail.com)
