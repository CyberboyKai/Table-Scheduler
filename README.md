# 🍽️ Table Scheduler

A party-assignment tool for restaurant hosts. Suggests which server should take each incoming party, keeping guest counts balanced across servers.

**▶ Live app:** https://cyberboykai.github.io/Table-Scheduler/

## Assignment Rules

1. **Clock-in order first** — servers who haven't received a party yet today go first, in the order they clocked in.
2. **Headcount balancing** — after that, the next party goes to the server with the fewest seated guests.
3. **No idle servers** — ties go to whoever has waited longest since their last seating.

## Features

- ⚡ **One-tap seating** — type the party size and hit Enter to seat with the suggested server
- ☕ **Breaks** — servers on break are excluded from suggestions (manual assignment still possible)
- ⭐ **Override seating** — host can hand-pick a server, e.g. for a regular's request
- 📋 **Seating log sidebar** — cancel a mistaken seating or undo a departure
- 🌐 **Korean / English** language toggle
- 💾 No install, no server — saves automatically to the browser (localStorage)

## How to Use

1. Add your staff in the **Settings** tab
2. Each morning, clock servers in on the **Floor** tab in arrival order
3. When a party arrives, enter the size → seat with the suggested server (Enter)
4. When a party leaves, tap the green chip on the server's card to mark them departed
5. At the end of the day, reset via **Settings → Start New Day**

## Tech

A single `index.html` — no framework, no build step, no backend. Data lives in the browser's localStorage (per-device, no sync).
