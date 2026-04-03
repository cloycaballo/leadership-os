# 🚀 Leadership OS

**Leadership OS** is a local-first, privacy-centric workspace designed for high-speed leadership. It consolidates daily tasks, team reliability tracking, and AI-assisted drafting into a single, secure "cockpit." Data is stored locally with optional cloud sync for cross-device backup.

---

## Key Features

- **Brain Dump:** Clear your mental RAM instantly. Type anything, convert to tasks later.
- **Reliability Matrix:** A visual heatmap for team accountability and attendance tracking.
- **Snooze & Boomerang:** Right-click tasks to hide them until you're ready to follow up.
- **Command Palette:** Use `Ctrl + K` to navigate the entire app without a mouse.
- **Local-First with Cloud Sync:** Data is stored locally in your browser and optionally synced to the cloud. Work offline and sync when connected.
- **Team Avatars:** Add profile pictures to team members for a personalized roster view.
- **Project Task Notifications:** Get notified when project tasks are due — scheduled reminders right in My Desk.

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
