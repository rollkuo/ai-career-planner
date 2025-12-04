# AI Career Transition Planner

Personal 35-week career transition planner with daily check-ins, streak tracking, and **auto-updating** AI jobs database.

## Quick Deploy to GitHub Pages (5 minutes)

### Step 1: Create GitHub Repository
1. Go to [github.com/new](https://github.com/new)
2. Name it `ai-career-planner`
3. Keep it **Public** (required for free GitHub Pages)
4. Click "Create repository"

### Step 2: Upload Files
1. Click "uploading an existing file"
2. Drag and drop ALL files including the `.github` folder:
   - `index.html`
   - `jobs.json`
   - `README.md`
   - `.github/workflows/update-jobs.yml`
3. Click "Commit changes"

### Step 3: Enable GitHub Pages
1. Go to **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** / **root**
4. Click **Save**

### Step 4: Access Your Planner
```
https://YOUR-USERNAME.github.io/ai-career-planner/
```

---

## 🔄 Auto-Update Jobs (One-Time Setup)

### Step 1: Get Google AI API Key (FREE)
1. Go to [aistudio.google.com](https://aistudio.google.com/)
2. Sign in with Google account
3. Click **Get API Key** → **Create API key**
4. Copy the key

### Step 2: Add API Key to GitHub
1. Go to your repo → **Settings** → **Secrets and variables** → **Actions**
2. Click **New repository secret**
3. Name: `GOOGLE_API_KEY`
4. Value: Paste your API key
5. Click **Add secret**

### Step 3: Enable Actions
1. Go to your repo → **Actions** tab
2. Click "I understand my workflows, go ahead and enable them"

### Done! Now You Can:

**Option A: Click to Update**
1. Go to **Actions** tab
2. Click **Update AI Jobs** (left sidebar)
3. Click **Run workflow** → **Run workflow**
4. Wait 1-2 min, jobs.json updates automatically!

**Option B: Automatic Weekly Updates**
- Already configured! Runs every Sunday at 9am UTC
- No action needed

---

## How It Works

```
┌─────────────────┐     ┌──────────────────┐     ┌─────────────────┐
│  Click "Run     │ ──▶ │  Gemini searches │ ──▶ │  jobs.json      │
│  workflow"      │     │  job boards      │     │  auto-updates   │
└─────────────────┘     └──────────────────┘     └─────────────────┘
```

The GitHub Action:
1. Uses Gemini API with Google Search grounding
2. Searches Anthropic, OpenAI, Google, Scale AI careers pages
3. Extracts current PM/Strategy roles
4. Updates jobs.json and commits automatically

---

## Cost

- **GitHub Pages**: Free
- **GitHub Actions**: Free (2,000 mins/month)
- **Google AI Studio**: FREE (generous limits)

---

## Features

### Daily Check-In
- One specific task per day (~30 min)
- Streak tracking 🔥
- Confetti celebration

### Weekly Plan
- 35-week roadmap
- Phase-based organization
- Per-week notes

### AI Jobs Database
- Auto-updates via GitHub Actions
- Tier 1-3 companies
- Direct apply links

---

## Troubleshooting

**Jobs not updating?**
1. Check Actions tab for errors
2. Verify `GOOGLE_API_KEY` secret is set correctly
3. Make sure Actions are enabled

**Want to update immediately?**
1. Go to Actions → Update AI Jobs → Run workflow

**API key not working?**
1. Get a new key from [aistudio.google.com](https://aistudio.google.com/)
2. Make sure the secret name is exactly `GOOGLE_API_KEY`

---

## Data Storage

All progress stored in browser localStorage:
- Streak count
- Completed tasks
- Notes

Jobs stored in jobs.json (auto-updated).

---

## Manual Override

Don't want auto-updates? Just edit jobs.json directly on GitHub:
1. Click jobs.json
2. Click pencil icon
3. Edit
4. Commit

---

Good luck with your career transition! 🚀
