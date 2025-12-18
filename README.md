# Stock Market Platform — Fintech Market Dashboard

A lightweight stock-market dashboard built with React (Vite) frontend and a small Flask backend. It visualizes market data, sentiment samples and portfolio information from CSV files and provides analytics components such as heatmaps, movers, charts and investor summaries.

## Key features
- Interactive dashboard with market overview, heatmap, market movers and charts
- Portfolio table and simple investment analysis components
- DSFM analytics page and visual components for tracking market trends
- Backend API (Flask) serving CSV data for the frontend

## Tech stack
- Frontend: React + Vite
- Styling: Tailwind CSS
- Backend: Python Flask (located in `backend/app.py`)
- Data: CSV files in `backend/data/` (e.g. `market_data.csv`, `sentiment_sample.csv`)

## Repository structure (high level)
- public/ — static public assets
- src/ — React app source
  - components/ — dashboard components and pages
  - pages/ — route pages
- backend/ — Flask API and data
  - data/ — CSV datasets used by the app
- README.md — this file

## Getting started (development)
### Prerequisites
- Node.js (v16+ recommended) and npm or yarn
- Python 3.8+ and virtualenv

1) Install frontend dependencies

```bash
# from repository root
npm install
```

2) Start frontend dev server

```bash
npm run dev
# or with yarn: yarn dev
```

This runs the Vite dev server (usually at http://localhost:5173). The frontend expects the backend API to be available for data requests.

3) Setup and run the backend (Flask)

```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate   # macOS / Linux
pip install -r requirements.txt
python app.py               # or `flask run` if configured`
```

By default the backend serves CSV data from `backend/data/`. Check `backend/app.py` for endpoints and configuration.

### Data
- Sample datasets are located in `backend/data/`.
- To add your own data, place CSV files in that folder and update the backend endpoints or frontend data paths as needed.

### Build & deploy
- Build frontend for production:

```bash
npm run build
# serve the build from a static host or integrate with the backend
```

- Production backend: run the Flask app behind a WSGI server (gunicorn/uvicorn) and serve the static `dist/` files produced by the frontend build.

### Environment & configuration
- There are no secret keys in this repository by default. If you add API keys or secrets, store them in environment variables and do not commit them.

## Contributing
- Feel free to open issues or create pull requests.
- Suggested improvements: add unit tests, improve error handling in the backend, add CI, support real-time market data streaming.

## License
- This repository does not include a license file. Add a LICENSE if you want to define terms for reuse.

## Acknowledgements
- Built with Vite, React and Tailwind CSS.

If you want, I can:
- Add a quickstart bash script to automate setup
- Add a LICENSE file and a CONTRIBUTING guide
- Generate API docs for the Flask backend
