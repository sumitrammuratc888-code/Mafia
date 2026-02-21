# AI Resume & Portfolio

A modern AI-powered resume and portfolio website built with **Next.js** (frontend) and **Python FastAPI** (backend) in a single directory.

## Features

- **Resume & Portfolio Display** – Hero, About, Skills, Experience, Projects, and Contact sections
- **AI Resume Assistant** – Paste a job description to get AI-powered resume improvement suggestions
- **Modern UI** – Dark theme with green accents, responsive design, smooth animations
- **Tech Stack** – Next.js 15, TypeScript, Tailwind CSS, FastAPI, OpenAI (optional)

## Project Structure

```
Ai-Resume-Portfolio/
├── src/                 # Next.js frontend
│   ├── app/             # App Router pages
│   └── components/      # React components
├── api/                 # Python FastAPI backend
│   ├── main.py          # API routes
│   └── requirements.txt
├── package.json
└── README.md
```

## Getting Started

### Prerequisites

- Node.js 18+
- Python 3.9+
- npm or pnpm

### 1. Install Frontend Dependencies

```bash
cd Ai-Resume-Portfolio
npm install
```

### 2. Install Python Dependencies

```bash
cd api
python -m venv venv

# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate

pip install -r requirements.txt
```

### 3. Environment Variables (Optional)

Copy `api/.env.example` to `api/.env` and add your OpenAI API key for AI-powered suggestions:

```
OPENAI_API_KEY=sk-...
```

Without an API key, the app uses rule-based fallback suggestions.

### 4. Run the Application

**Terminal 1 – Next.js frontend:**
```bash
npm run dev
```

**Terminal 2 – Python API:**
```bash
cd api
uvicorn main:app --reload
```

- Frontend: [http://localhost:3000](http://localhost:3000)
- API: [http://localhost:8000](http://localhost:8000)

### 5. Customize Your Content

Edit these files to add your own information:

- `src/components/Hero.tsx` – Name, title, intro
- `src/components/About.tsx` – Bio and quick facts
- `src/components/Skills.tsx` – Tech stack
- `src/components/Experience.tsx` – Work history
- `src/components/Projects.tsx` – Projects
- `src/components/Footer.tsx` – Social links

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | API info |
| GET | `/health` | Health check |
| POST | `/suggest` | Get resume suggestions (body: `{"job_description": "..."}`) |

## Build for Production

```bash
npm run build
npm start
```

## License

MIT
