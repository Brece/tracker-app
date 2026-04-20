We are building a modular fullstack tracker app.

Tech:

- React (Vite) frontend
- Node.js (TypeScript) backend

Goal:

- Support multiple trackers (e.g. Steam Deck, GitHub, APIs)
- Each tracker follows a shared interface
- Architecture should be simple, modular, and scalable

---

Backend Structure:

- trackers/
    - each tracker is its own module
    - index.ts acts as registry
- core/
    - types.ts (interfaces)
    - trackerRunner.ts (execution logic)
- api/
    - routes.ts
- server.ts

---

System Design:

- Each tracker:
    - has id, name, and check() method
    - returns a standardized result

- The system:
    - registers all trackers
    - runs them via a central runner
    - exposes results via API

---

Requirements:

- Define Tracker interface (id, name, check())
- Define TrackerResult type
- Implement tracker registry
- Implement runner that executes all trackers
- Add one example tracker (mock)
- Expose GET /api/trackers endpoint

---

Constraints:

- Keep everything minimal and readable
- Avoid over-engineering
- Do not introduce unnecessary abstractions
- Do not change project structure
- Only modify files when explicitly asked

---

Output Behavior:

- Explain briefly
- Do not generate multiple files unless requested
- Output only relevant code
