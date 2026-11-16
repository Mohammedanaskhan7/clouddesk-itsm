<div align="center">

# CloudDesk ITSM — IT Help Desk & Ticket Management System

**A zero-dependency, role-based IT service desk web application with real-time ticket tracking, multi-criteria filtering, and an integrated security-rule test runner.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Firebase Ready](https://img.shields.io/badge/Firebase_Schema-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)

[Features](#-key-features) • [Screenshots](#-screenshots) • [Quick Start](#-quick-start) • [Architecture](#-architecture--data-model) • [Roadmap](#-roadmap)

</div>

---

## Overview

**CloudDesk ITSM** streamlines internal IT support operations by replacing fragmented email and chat requests with a structured, auditable ticket lifecycle. Built for fast deployment and zero-setup browser execution, the current release runs entirely client-side with `localStorage` persistence and an interactive 12-scenario verification suite, alongside a documented schema and security ruleset for Cloud Firestore migration.

---

## ✨ Key Features

| Capability | Employee Role | IT Support Admin Role |
| :--- | :--- | :--- |
| **Ticket Submission** | Create tickets with auto-generated `TKT-YYYY-NNNN` IDs | View all department queues |
| **Ownership Isolation** | View and search only self-submitted tickets | Access full organization ticket register |
| **Search & Filtering** | Filter by Ticket ID, Category, Priority, and Status | Filter by Employee Name + all ticket attributes |
| **Triage & Resolution** | Track live status (`Open`, `In Progress`, `Resolved`) | Update Priority, Status, and Resolution Notes |
| **Diagnostics & QA** | Inspect local JSON store | Run built-in 12-scenario RBAC verification suite |

---

## 📸 Screenshots

### Employee Dashboard & Ticket Inspector
![Employee Dashboard]screenshots/README.md/dashboard.png

### Built-in 12-Scenario Verification Runner
![Verification Runner]screenshots/README.md/test_runner.png

---

## 🚀 Quick Start

No build step, package manager, or backend server is required to run the prototype:

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/clouddesk-itsm.git

# 2. Navigate into the project directory
cd clouddesk-itsm

# 3. Open index.html in any modern browser
```

Or enable **GitHub Pages** (`Settings → Pages → Deploy from branch: main`) to host the application immediately.

---

## 🏗 Architecture & Data Model

### Current Prototype (`index.html`)
- **UI Layer:** Responsive interface built with semantic HTML5 and Tailwind CSS utility classes.
- **State & Persistence:** Browser `localStorage` (`ou_mca_helpdesk_users_v3`, `ou_mca_helpdesk_tickets_v3`, `ou_mca_helpdesk_session_v3`).
- **Access Simulation:** Client-side role evaluator (`evaluateFirestoreRule`) modeling row-level ownership and admin-only mutations.

### Project Structure

```text
clouddesk-itsm/
├── index.html                              # Standalone web application
├── README.md                               # Project documentation
├── CONTRIBUTING.md                         # Contribution guidelines
├── LICENSE                                 # MIT License
├── .gitignore                              # Standard ignore rules
├── docs/
│   └── IT_Help_Desk_System_Documentation.pdf
└── screenshots/
    ├── dashboard.png                       # Employee workspace UI
    └── test_runner.png                     # 12-scenario test runner UI
```

---

## 🗺 Roadmap

- [x] Standalone HTML5/JS prototype with Employee & Admin workflows
- [x] Multi-attribute search, filtering, and KPI summary cards
- [x] Built-in 12-scenario rule-simulation test runner
- [ ] Connect live Firebase Authentication (Email/Password & Google OAuth)
- [ ] Migrate `localStorage` collections to Cloud Firestore with deployed `firestore.rules`
- [ ] Add transaction-safe server-side ticket ID counter & audit log

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for more information.

**Author:** Mohammed Anas Ullah Khan
