
# 🚀 6-Month Fitness & Study Tracker

A **local-first, automated personal dashboard** to track fitness, habits, studies, and progress over a 6-month journey — built as a **single-page static web app** with zero backend.

> Designed for consistency, low friction, and long-term tracking.

---

## ✨ Features

### 🧠 Smart Habit Tracking

* Daily **checkbox-based habit tracker**

  * Workout
  * Calories on target
  * Protein on target
  * Study
  * Sleep ≥ 7.5h
* One-click “Add Today” (auto-detects real date)
* Automatic **streak calculation**
* Data persists using `localStorage`

---

### 📅 Timetable & Schedule

* Editable **text-based schedule**
* Automatically parsed into a **responsive timetable**
* Day-wise columns (Mon–Sun)
* Live updates as you edit the schedule
* Mobile / tablet / desktop friendly

---

### 📊 Progress Dashboard

* **Weight trend chart**
* **Gym sessions per week**
* **Study hours per week**
* Real-time updates from weekly data
* Powered by Chart.js

---

### 📉 Weekly Automation

* Weekly summary **auto-generated on Sunday**
* Derived from daily habits:

  * Gym sessions count
  * Study days count
* Prevents duplicate weeks
* Manual control for:

  * Weight
  * Waist
  * Notes

---

### 🧾 Dynamic Header (Profile Card)

* Displays:

  * Name
  * Current weight
  * Starting weight
  * Goal weight
  * BMI (auto-calculated)
  * Progress bar to goal
* Updates automatically as weekly data changes
* Profile editable and stored locally

---

### 💾 Local-First & Portable

* Uses **browser `localStorage`** (no backend)
* Works fully offline
* **Export / Import** data as JSON
* Easy device migration & backups

---

## 🛠️ Tech Stack

* **HTML5** (single file)
* **Tailwind CSS** (CDN)
* **Vanilla JavaScript**
* **Chart.js** (CDN)
* **localStorage** for persistence
* **Vercel** for hosting

---

## 📁 Project Structure

```
.
├── index.html   # Entire application (no build step)
└── README.md
```

---

## 🚀 Deployment (Vercel)

### Option 1: Drag & Drop (Fastest)

1. Go to [https://vercel.com](https://vercel.com)
2. New Project → Deploy without Git
3. Upload folder containing `index.html`
4. Done ✅

### Option 2: GitHub (Recommended)

1. Push `index.html` to a GitHub repo
2. Import repo into Vercel
3. Framework preset: **Other**
4. No build command required

---

## 🧠 Data Model (High Level)

### Daily Tracker

```js
{
  date: "YYYY-MM-DD",
  workout: true,
  calories: false,
  protein: true,
  study: true,
  sleep: true
}
```

### Weekly Tracker

```js
[
  "2026-W3",
  "93.5",   // weight (manual)
  "",       // waist
  4,        // gym sessions
  3,        // study days
  "Auto-generated from daily habits"
]
```

### Profile

```js
{
  name: "Maddy",
  heightCm: 164,
  startWeightKg: 95,
  currentWeightKg: 95,
  goalWeightKg: 85
}
```

---

## ⚠️ Important Notes

* Data persists **only on the same browser & device**
* Clearing browser data will reset progress
* Always export data periodically for backup
* Weekly auto-generation runs when the app is opened on **Sunday**

---

## 🧪 Recommended Usage Flow

1. Open the app daily
2. Click **Add Today**
3. Tick completed habits
4. On Sunday → weekly row auto-generated
5. Enter weight manually
6. Track trends & stay consistent

---

## 🔮 Future Enhancements (Planned / Possible)

* PWA (installable app)
* Monthly summaries
* Goal ETA prediction
* Missed-week auto backfill
* Notifications & reminders
* Cloud sync (Supabase / Firebase)

---

## 👤 Author

**MANDAR KELKAR**
Built as a self-improvement + engineering practice project.

---

## 🏁 Final Note

This project is intentionally:

* Simple
* Local-first
* Backend-free
* Highly maintainable

It focuses on **consistency over complexity**.

> “You don’t rise to the level of your goals,
> you fall to the level of your systems.”

---

