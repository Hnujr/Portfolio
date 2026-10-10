# Portfolio
A product management concept and AI-generated frontend prototype for a centralized student workspace at UVA.

# Product Concept: StudySpaces (Centralized Student Workspace)

### 1. The Problem (Context Switching & Tab Fatigue)
University students have to navigate a highly fragmented digital ecosystem every single day. At UVA, a single student might use **Microsoft Teams** for Economics, **Outlook** for school communications, **Google Calendar** for personal scheduling, **Gradescope** for math submissions, and **WebAssign** for homework. 

This causes two major issues:
* **Information Fragmentation:** Deadlines are scattered across multiple platforms, making it easy to forget tasks or lose track of what is due next.
* **Tab Hoarding:** Students keep dozens of browser tabs open simultaneously to avoid losing their place, which slows down laptop performance and causes mental clutter. 

### 2. The Solution (Task-Specific Tab Groups)
**StudySpaces** is a browser extension and dashboard that acts as a single source of truth for a student's day. Instead of organizing by website, it organizes by **assignment/task**.

* **The Command Center:** A single dashboard that aggregates deadlines across Gradescope, WebAssign, and Teams into one unified timeline.
* **One-Click Study Environments:** Next to each assignment deadline is a "Launch Workspace" button. Clicking it instantly opens a localized group of tabs pre-loaded with everything needed for *just* that assignment (e.g., the WebAssign portal, the specific Teams lecture slide, and an e-textbook).
* **Automated Cleanup:** When a student submits the assignment or clicks "Pause Session," the extension automatically saves their place and closes the tab group, optimizing laptop memory and preventing mental clutter.

### 3. Core Target Audience (User Persona)
* **The Fragmented Student:** A UVA student taking a cross-disciplinary schedule (like STEM and Commerce) who jumps between 4+ learning portals daily and struggles with digital clutter.

### 4. Key Success Metrics (KPIs)
To measure if StudySpaces is successful, we would track:
* **Active Workspaces Launched:** How many times a day students use the "Launch Workspace" feature instead of opening tabs manually.
* **Tab Reduction Rate:** The average reduction in total open browser tabs per user session.
* **Daily Active Users (DAU):** The number of students relying on the dashboard as their primary morning planner.

### 5. Technical & Execution Considerations (For the Engineering Team)
To build this, the product and engineering teams would need to tackle:
* **API Integrations:** Securing read-only permissions to pull data from fragmented portals (Canvas API, Microsoft Graph API for Teams/Outlook, and scraping hooks for Gradescope).
* **Browser Extension State Management:** Utilizing Chrome Extension APIs (`chrome.tabs` and `chrome.tabGroups`) to programmatically save, group, open, and close sets of URLs based on the active assignment ID.
* **Privacy & Security:** Ensuring student login credentials for academic portals are securely handled locally on the browser rather than stored on an external server.
