# AI Career Transition Planner

Personal 35-week career transition planner with daily check-ins, streak tracking, and AI jobs database.

## Quick Deploy to GitHub Pages (5 minutes)

### Step 1: Create GitHub Repository
1. Go to [github.com/new](https://github.com/new)
2. Name it `ai-career-planner` (or anything you want)
3. Keep it **Private** (for personal use)
4. Click "Create repository"

### Step 2: Upload Files
1. Click "uploading an existing file"
2. Drag and drop both files:
   - `index.html`
   - `jobs.json`
3. Click "Commit changes"

### Step 3: Enable GitHub Pages
1. Go to repository **Settings** → **Pages**
2. Under "Source", select **Deploy from a branch**
3. Select **main** branch and **/ (root)** folder
4. Click **Save**
5. Wait 1-2 minutes

### Step 4: Access Your Planner
Your planner will be live at:
```
https://YOUR-USERNAME.github.io/ai-career-planner/
```

---

## Updating Jobs

### Manual Update (Recommended - Most Reliable)
1. Go to your repository on GitHub
2. Click on `jobs.json`
3. Click the pencil icon (Edit)
4. Update job listings
5. Click "Commit changes"

### Jobs JSON Format
```json
{
  "lastUpdated": "2025-12-03",
  "jobs": [
    {
      "company": "Anthropic",
      "role": "Strategic PM",
      "salary": "$260-325K",
      "requirements": ["10+ yrs PM", "SQL required"],
      "tier": 1,
      "url": "https://job-boards.greenhouse.io/anthropic/jobs/...",
      "active": true
    }
  ]
}
```

### Where to Find Jobs
- **Anthropic**: https://www.anthropic.com/careers
- **OpenAI**: https://openai.com/careers
- **Google AI**: https://www.google.com/about/careers/applications/jobs/results?q=AI
- **Microsoft**: https://careers.microsoft.com/us/en/search-results?keywords=AI

### Weekly Job Check Reminder
Add to your calendar: **Every Sunday, 10 min**
- Check job boards above
- Update `jobs.json` if roles changed
- Mark closed roles as `"active": false`

---

## Features

### Daily Check-In
- One specific task per day (~30 min)
- Streak tracking (resets after 2 consecutive skips)
- Confetti celebration on completion 🎉

### Weekly Plan
- 35-week roadmap
- Phase-based organization
- Per-week notes
- Progress tracking

### AI Jobs Database
- Tier 1-3 companies
- Salary ranges
- Key requirements
- Direct apply links

---

## Data Storage

All your progress is stored in your browser's localStorage:
- Streak count
- Completed tasks
- Week notes
- General notes

**To backup**: Open browser console, run:
```javascript
console.log(localStorage.getItem('ai-career-planner-v6'));
```

**To restore**: 
```javascript
localStorage.setItem('ai-career-planner-v6', 'YOUR_BACKUP_STRING');
```

---

## Customization

### Change Start Date
In `index.html`, find and update:
```javascript
const START_DATE = new Date('2025-12-02');
```

### Add More Tasks
Find the `dailyTasks` object and add entries:
```javascript
const dailyTasks = {
    1: [
        { task: "Your task here", duration: "30 min" },
        // ...
    ],
    // ...
};
```

---

## FAQ

**Q: Can I use this on mobile?**
A: Yes, it's responsive. Works on any browser.

**Q: Does my data sync across devices?**
A: No, localStorage is per-browser. Use the backup/restore method if needed.

**Q: Can others see my planner?**
A: Only if you make the repo public. Private repos + GitHub Pages = only you can access.

---

## Support

This is a personal tool. If you want to improve it:
- Fork the repo
- Make changes
- Commit to your version

Good luck with your career transition! 🚀
