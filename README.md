# Tara Suleiman — Portfolio Site

## Setup Instructions

### 1. Replace placeholder text
Before deploying, do a find-and-replace across all HTML files:
- `YOURUSERNAME` → your actual GitHub username
- `assets/Tara_Suleiman_Resume.pdf` → add your actual resume PDF to assets/

### 2. Add your screenshots
Place your dashboard screenshots in `assets/images/` with these exact filenames:

| File | What it is |
|---|---|
| `p1-overview.png` | Project 1 — Page 1 Executive Overview |
| `p1-response.png` | Project 1 — Page 2 Response Time |
| `p1-scoring.png` | Project 1 — Page 3 Lead Quality |
| `p2-overview.png` | Project 2 — Page 1 Segment Overview |
| `p2-deep-dive.png` | Project 2 — Page 2 Segment Deep Dive |
| `p3-current-state.png` | Project 3 — Lucidchart current state diagram |
| `p3-future-state.png` | Project 3 — Lucidchart future state diagram |
| `p3-makecom.png` | Project 3 — Make.com scenario screenshot |
| `p3-airtable.png` | Project 3 — Airtable base screenshot |
| `p4-evaluation.png` | Project 4 — ROC curves + confusion matrices |
| `p4-importance.png` | Project 4 — Feature importance chart |

### 3. Deploy to GitHub Pages

1. Create a new GitHub repo named exactly: `[yourusername].github.io`
2. Push all files from this folder into the root of that repo
3. Go to repo Settings → Pages → Source: Deploy from branch → main → / (root)
4. Your site will be live at `https://[yourusername].github.io` in ~2 minutes

### 4. Connect your custom domain

In your GitHub repo:
1. Go to Settings → Pages → Custom domain
2. Type your domain (e.g., `tarasuleiman.com`) → Save
3. Check "Enforce HTTPS" once it verifies

In your domain registrar (Namecheap / GoDaddy etc.):
Add these DNS records:

**A records (point to GitHub's IPs):**
```
@ → 185.199.108.153
@ → 185.199.109.153
@ → 185.199.110.153
@ → 185.199.111.153
```

**CNAME record:**
```
www → [yourusername].github.io
```

DNS changes take 10 minutes to 48 hours to propagate.
GitHub will automatically provision an SSL certificate once DNS verifies.

### 5. File structure
```
portfolio-site/
├── index.html          (homepage)
├── project1.html       (SentinelSec)
├── project2.html       (FinSight)
├── project3.html       (Support Tickets)
├── project4.html       (Lead Prediction)
├── about.html          (About + Resume)
├── CNAME               (create this file with just your domain inside)
├── assets/
│   ├── css/style.css
│   ├── js/main.js
│   └── images/         (add all screenshots here)
└── README.md
```

### 6. CNAME file
Create a file called `CNAME` (no extension) in the root folder.
Inside it, put just your domain on one line:
```
tarasuleiman.com
```
This tells GitHub Pages to serve your site at your custom domain.
