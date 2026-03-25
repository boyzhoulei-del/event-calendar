# Deployment Guide

## Status
✅ Files created and committed locally
- SPEC.md - Complete specification
- index.html - Full single-file web app (22KB)
- 42 events for 2026 loaded

## Local Git Setup
```bash
cd /Users/zhoulei/.qclaw/workspace/event-calendar
git log --oneline
# cf8f005 feat: initial event calendar app
```

## Push to GitHub

If network allows, run:
```bash
git push -u origin main
```

## Enable GitHub Pages

After push succeeds:
1. Go to https://github.com/boyzhoulei-del/event-calendar/settings
2. Scroll to "Pages" section
3. Select "Deploy from a branch"
4. Choose "main" branch, root folder
5. Save

Your calendar will be live at: https://boyzhoulei-del.github.io/event-calendar/

## Features Implemented

✅ Mobile-first design (375px baseline)
✅ Dark theme (#0a0a0f background)
✅ Calendar grid with month navigation
✅ 42 events for 2026:
  - 5 Sports events
  - 13 Chinese festivals
  - 13 Global holidays
  - 6 Concerts/performances
  - 5 Tech events
✅ Filter by event type
✅ Click date to view events
✅ Event cards with details
✅ Responsive layout
✅ Chinese language support
✅ No build step needed - pure HTML/CSS/JS

## Testing

Open `index.html` in any browser to test locally.
