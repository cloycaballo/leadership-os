# 🚀 Leadership OS

**Leadership OS** is a local-first, privacy-centric workspace designed for high-speed leadership. It consolidates daily tasks, team reliability tracking, and AI-assisted drafting into a single, secure "cockpit." Data is stored locally with optional cloud sync for cross-device backup.

---

## Key Features

**My Desk** is the personal task management board. Tasks sit in a Kanban layout with drag-and-drop columns, a calendar view for date-aware planning, and a snooze system — right-click any task to defer it and have it reappear automatically on the date you set.

**Projects** groups related tasks into a named board. TLs can share project templates across the team so recurring workflows don't need to be rebuilt from scratch each time. When a project task has a due date, it automatically surfaces as a reminder in My Desk — no manual follow-up needed.

**Evaluation Pipeline** is a structured tracker for team member evaluation cycles. It tracks status, sends automated reminders, and keeps a full history so nothing slips through.

**Team Logbook** is where TLs log issues, kudos, requests, and general notes per team member. It supports AI-assisted parsing for free-form text entry and handles mixed Tagalog/English input. The result is a searchable record of every significant interaction.

**Broadcast Tracker** handles team-wide tasks and announcements with a built-in completion tracker. Instead of chasing people down to confirm they've read or done something, the tracker shows who's done and who isn't.

**Email Drafter** uses AI to help write professional emails. Paste in context, pick a tone, get a draft. Useful for routine communication that still needs to sound considered.

**Brain Dump** is a scratchpad for capturing anything mid-thought — tasks, ideas, follow-ups. Highlight any text to convert it into a real task when you're ready.

**Local-first storage** means data lives in your browser by default. Nothing leaves the device unless you turn on cloud sync. Safe Tier is available for teams that need cloud sync fully disabled.

**Command Palette** — press Ctrl + K to get anywhere in the app without touching the mouse.

**Team Avatars** let you add profile pictures to roster members for a quick visual reference.

---

## Technology Stack

- **Frontend:** HTML5, Vanilla JavaScript, Tailwind CSS (via CDN)
- **Icons:** Lucide Icons
- **Storage:** Browser LocalStorage + Cloud Sync (Supabase) for cross-device backup
- **AI Integration:** Google Gemini API (optional)

---

## Getting Started

### Option 1: Web (Recommended)
1. Clone the repository or download the `LeadershipOS_MASTER_DO_NOT_EDIT.html` file.
2. Open it in **Chrome** or **Edge**.
3. Optionally enter your Gemini API key in Settings to enable AI features.

### Option 2: Install as Desktop App (PWA)
1. Open the hosted URL in **Microsoft Edge** or **Chrome**.
2. Click the install icon in the address bar to install as a Progressive Web App (PWA).
3. The app will run in its own window. All data remains stored locally in the browser.

---

## Privacy & Security

Leadership OS is built with a security-first approach.

- **Local-First:** Your data lives in your browser. Cloud sync is optional and under your control.
- **Data Ownership:** When using cloud sync, data is stored in your own Supabase project — not a shared server.
- **Offline-Capable:** Core task and tracking features work without an internet connection.

---

## Roadmap

- [ ] Custom Theme Engine
- [ ] Export to PDF/Excel for reporting

---

## License

Distributed under the MIT License. See `LICENSE` for more information.

---

## 🔐 GRC & Security Notes

- **Safe Tier available:** A restricted configuration that disables all cloud sync and hides sensitive data fields (PSI & Contact). Designed for compliance-sensitive deployments.
- **No SQL injection risk:** Supabase uses parameterized queries via PostgREST. Raw SQL from user input is never executed.
- **Row Level Security (RLS):** Enforced at the database level. Users can only access their own data.
- **localStorage scope:** Data is sandboxed to the app's domain in the user's browser. Other tabs, sites, or users cannot access it.
- **External API calls:** Only three services make network calls — Supabase (auth only in Safe Tier), Gemini API (user-initiated, optional), and DiceBear (avatar generation, cosmetic only).
