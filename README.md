# ⚡ Grid — Autonomous Academic & Life Scheduling Engine
> **Semester 3 IT Workshop III (Python) Project**  
> *A heuristic-driven, retro-inspired autonomous scheduling engine built with pure Python, Flask, SQLite3, and Matplotlib.*

---

## 🌐 Quick Links
- **Live Deployment:** [https://grid-planner-jmz0.onrender.com/](https://grid-planner-jmz0.onrender.com/)
- **Repository:** [https://github.com/scrymgeor/Grid_Planner](https://github.com/scrymgeor/Grid_Planner)

---

## 📖 What is GRID?
Traditional calendars are passive—you still have to figure out *when* to study. **Grid** automates time management:
1. You set your weekly free hours and input tasks with deadlines and priorities.
2. Our **Greedy Heuristic Algorithm** calculates dynamic task urgency:
   $$\text{Urgency} = \frac{\text{Priority (1–5)} \times 100}{\text{Hours Remaining to Deadline}}$$
3. It breaks tasks into **1.5-hour burnout-prevention blocks** and slots them into your free time automatically.

---

##  Features
- **Heuristic Auto-Scheduler:** Computes dynamic urgency and auto-allocates study blocks.
- **Retro UI:** Nostalgic pastel grid paper and windowed aesthetic.
- **Full Relational CRUD:** Multi-user SQLite3 database with SHA-256 password hashing.
- **Network Services (SMTP):** Welcome emails on signup and 6-digit OTP verification for password resets.
- **Habit & Streak Tracker:** Daily habit checklist with active streak counters.
- **Data Analytics:** Real-time workload distribution bar charts powered by **Matplotlib**.
- **File I/O & Undo Stack:** Batch import/export via CSV, system activity logging, and an in-memory `ActionStack` (LIFO) for undo operations.

---

## Implementation
- **OOP & Polymorphism:** `Task` base class overridden by `AcademicTask`, `FitnessHabitTask`, and `WorkProjectTask`.
- **Database Processing:** SQLite3 relational schema (`users`, `tasks`, `free_slots`, `schedule`, `habits`).
- **Data Structures:** Custom `ActionStack` class with `.push()` and `.pop()`.
- **Networking:** Client-server email dispatching using Python's native `smtplib`.
- **Concurrency:** Background `threading.Thread` daemon monitoring deadlines.
- **File Processing:** CSV parsing (`csv.DictReader`, `csv.writer`) and text append logging (`system_activity.log`).
-Grid integrates production-grade email services using Python's native `smtplib` and `email.mime` over authenticated TLS/SSL ports:
  **Automated Onboarding:** Sends an official **Welcome Email** immediately upon user registration.
  **Secure Password Recovery:** Generates and dispatches a dynamic **6-digit verification OTP** when a user clicks *"Forgot Password"*.
---

## 🚀 Quickstart & Setup

```bash
# 1. Clone the repository
git clone https://github.com/scrymgeor/Grid_Planner.git
cd YOUR_REPO_NAME

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the application
python app.py
Open http://127.0.0.1:5000 in your browser.
👨‍💻 Author
Student Name: Keerthana A E
Course: IT Workshop III
