# IELTS 30-Day Intensive Study Planner

A structured, interactive 30-day study planner designed to help IELTS
candidates achieve a strong band score from scratch with a focused
4-5 hours daily routine. Track tasks, log scores, analyze mistakes,
and time your practice sessions - all within a single, privacy-first
web page.

🌐 **Live Site:** [ielts30.nbslabs.dev](https://ielts30.nbslabs.dev)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Data & Privacy](#data--privacy)
- [Deployment](#deployment)
- [Contributing](#contributing)

## Overview

Preparing for the IELTS exam can feel overwhelming without a clear
roadmap. This planner breaks the entire preparation into a
structured 4-week, 28-day curriculum built around the official
Cambridge IELTS books (Cambridge 16-19). Each day includes
specific tasks across all four modules - Listening, Reading,
Writing, and Speaking - progressing from pattern recognition
in Week 1 to full mock tests by Week 4.

The planner is built as a single static HTML page with zero
backend dependencies. All progress is saved locally in your
browser via `localStorage`, and you can export/import your data
as JSON files to sync across devices or create backups.

## Features

- **4-Week Structured Curriculum** - 28 days of daily tasks
  organized into four progressive phases, totaling 112 checkable
  tasks across all IELTS modules
- **Interactive Task Checklist** - Check off daily tasks as you
  complete them, with visual progress tracking per day, per week,
  and overall
- **Progress Dashboard** - Real-time overall completion percentage,
  per-week mini progress indicators, and a completed days counter
- **Built-in Practice Timer** - Countdown timer with presets for
  Reading (60 min), Listening (30 min), Speaking Cue Card (2 min),
  and Full Mock Test (2h 45m), with audio notification on completion
- **Daily Score & Notes Logging** - Record your band scores and key
  takeaways for each day directly on the day card
- **Mistake Analysis Journal** - Dedicated section to log recurring
  mistakes across Reading/Listening and Writing/Speaking modules
- **Export & Import (JSON Sync)** - Download your progress as a
  `.json` backup and import it on any browser to sync across devices
- **Curated Resource Links** - Modal with hand-picked IELTS resources
  including IELTS Liz, British Council, IDP, Cambridge materials,
  BBC 6 Minute English, and more
- **Dark/Light Theme Toggle** - Full dark mode support with smooth
  theme transitions and persistent preference
- **Bulk Actions** - Toggle all tasks in the current week as
  complete/incomplete with a single click
- **Responsive Design** - Fully responsive layout optimized for
  desktop, tablet, and mobile screens
- **100% Privacy** - No server, no analytics, no cookies. All data
  stays in your browser's local storage

## Tech Stack

| Layer       | Technology                    |
| ----------- | ----------------------------- |
| Markup      | HTML5                         |
| Styling     | Tailwind CSS (CDN)            |
| Logic       | Vanilla JavaScript (ES6+)     |
| Icons       | Lucide Icons                  |
| Typography  | Inter (Google Fonts)          |
| Storage     | Browser localStorage          |
| Hosting     | GitHub Pages (custom domain)  |

## Getting Started

### Prerequisites

- Any modern web browser (Chrome, Firefox, Safari, Edge)
- No build tools, no Node.js, no package manager required

### Run Locally

1. Clone the repository:

   ```bash
   git clone git@github.com:nbslabs/ielts30.git
   cd ielts30
   ```

2. Open `index.html` directly in your browser:

   ```bash
   # Linux / macOS
   open index.html
   # or
   xdg-open index.html

   # Windows
   start index.html
   ```

   Alternatively, use any local HTTP server:

   ```bash
   # Python 3
   python3 -m http.server 8080

   # Then visit http://localhost:8080
   ```

## Usage

### Daily Study Workflow

1. **Select the current week** from the week tabs at the top of
   the study plan section
2. **Read the week's strategy** in the summary banner, including
   the target goal, action plan, and recommended Cambridge book
3. **Work through each day's tasks** - check the boxes as you
   complete Listening, Reading, Writing, Speaking, and Analysis
   activities
4. **Log your scores** in the "Score / Band" field for each day
   (e.g., `L: 33/40, R: 31/40`)
5. **Note key mistakes** in the daily takeaway field and the
   global Mistake Analysis journal
6. **Use the Practice Timer** for timed drills - select a preset
   or let it count down during your practice test

### Data Management

- **Export**: Click the "Export (Backup)" button in the header to
  download your progress as a timestamped `.json` file
- **Import**: Click "Import (Sync)" and select a previously
  exported `.json` file to restore progress on any browser
- **Reset**: Use the reset button to clear all progress (with
  confirmation prompt)

### Study Plan Structure

| Week   | Focus                                  | Cambridge Book |
| ------ | -------------------------------------- | -------------- |
| Week 1 | Pattern Recognition & Foundation       | Cambridge 16   |
| Week 2 | Building Speed & Accuracy              | Cambridge 17   |
| Week 3 | Timed Practice & Deep Mistake Analysis | Cambridge 18   |
| Week 4 | Full Mock Tests & Final Refinement     | Cambridge 19   |

## Project Structure

```
ielts30/
├── index.html    # Single-page application (HTML + CSS + JS)
├── CNAME         # Custom domain config for GitHub Pages
└── README.md     # This file
```

The entire application lives in a single `index.html` file
(~1,500 lines) containing:

- **HTML** - Semantic markup with header, main content sections,
  modals, and footer
- **Tailwind CSS** - Utility-first styling via CDN with custom
  config for Inter font family and dark mode
- **JavaScript** - ~950 lines of vanilla JS handling state
  management, UI rendering, timer logic, import/export, and
  theme toggling

## Data & Privacy

This application is **100% client-side**. There is:

- No backend server or API calls
- No analytics or tracking scripts
- No cookies
- No data sent to any third party

All study progress (completed tasks, scores, notes, theme
preference) is stored exclusively in your browser's
`localStorage` under the key `ielts30_progress`. Clearing your
browser data will remove your progress - use the Export feature
to create backups.

## Deployment

The site is deployed via **GitHub Pages** with a custom domain
(`ielts30.nbslabs.dev`). To deploy your own fork:

1. Fork the repository
2. Go to **Settings > Pages** in your GitHub repo
3. Set the source branch to `main` and folder to `/ (root)`
4. Optionally configure a custom domain via the `CNAME` file

No build step is required - GitHub Pages serves `index.html`
directly as a static file.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

Since the entire app is in a single HTML file, please keep changes
focused and test across both light and dark themes before
submitting.
