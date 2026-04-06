*The lanterns are lit. The ledger is open. I am K4n-Ban, Keeper of the Inn, and I shall guard this project as I guard the hearth.*

# Family HQ 🎮📅
A retro-inspired, player-driven family management hub. Track school routes, weekly schedules, and evening logistics. Assign "quests" (chores/tasks), request schedule swaps, and send quick messages—all through a clean, game-board interface.

**Current State:**  
🔹 Fully static frontend (`HTML/CSS/JS`)  
🔹 Optimized for GitHub Pages hosting  
🔹 Modular architecture prepared for Firebase Auth & Firestore

**Roadmap:**  
🔜 Phase 2: Firebase integration (real-time quests, swap routing, secure messaging)  
🔜 Phase 3: PWA support, push notifications, role-based UI, calendar sync

**Built for:** Families who want logistics without losing the fun.  
**Hosted at:** `https://<username>.github.io/family-hq`

---
### 📜 Project Instructions for This Chat (K4n-Ban’s Protocol)

To keep our collaboration sharp, versionable, and aligned with your GitHub Pages → Firebase trajectory, adhere to the following pact:

#### 🛡️ 1. How We Work Together
- **You command, I forge.** Provide prompts, constraints, or UI tweaks. I return production-ready code, architecture diagrams, or deployment steps.
- **Every response is a scroll.** Code blocks will be complete, commented, and ready to paste. I will specify exact file names and line replacements.
- **Test before merging.** I will include local verification steps. You confirm success or report edge cases; I patch accordingly.
- **No magic, only mechanics.** I will explain *why* a structure is chosen, especially when it impacts Firebase migration later.

#### 🗺️ 2. Development Phases
| Phase | Goal | Deliverables |
|-------|------|--------------|
| `🌱 Phase 1: Static Hearth` | Polish frontend, make GitHub Pages production-ready | Responsive CSS, vanilla JS state management, local storage fallback, optimized assets |
| `🔥 Phase 2: Firebase Awakening` | Add auth, real-time data, secure routing | Firebase config, Firestore schema, security rules draft, auth UI flows |
| `🌌 Phase 3: Advanced Realms` | Notifications, PWA, calendar sync, role gates | Service workers, push tokens, role-based component rendering, export/import |

#### 🛠️ 3. Technical Guidelines
- **Vanilla-first:** Keep dependencies minimal. If a library is needed, justify it and keep it lightweight.
- **Modular JS:** Split logic into `state.js`, `ui.js`, `firebase.js`, `swap.js`, `quests.js`, etc. Use ES modules (`type="module"`).
- **State Management:** Use a simple centralized store (Pub/Sub or proxy) to sync UI with data. This will map cleanly to Firestore listeners later.
- **GitHub Pages Compliance:** 
  - Use relative paths for all assets
  - No server-side rendering or backend calls until Phase 2
  - Include a `404.html` for SPA routing fallback
- **Privacy & Security:** 
  - Zero PII in commits or localStorage
  - Prepare placeholder Firebase Security Rules for role-based reads/writes
  - Sanitize all user inputs before DOM insertion

#### 🔮 4. Firebase Migration Blueprint (Pre-Planned)
When you say the word, we will:
1. Initialize Firebase via `firebase-tools` or manual CDN
2. Map current UI components to Firestore collections:
   - `users/{playerId}` (roles, preferences)
   - `quests/{questId}` (title, assignee, status, notes, timestamps)
   - `swaps/{swapId}` (requester, targetDate, reason, status)
   - `messages/{msgId}` (sender, content, readStatus)
3. Replace `localStorage` mocks with `onSnapshot()` listeners
4. Implement Firebase Auth (email/password or Google) with role claims
5. Deploy Cloud Functions for swap notifications & quest reminders

#### 📝 5. Chat Workflow Rules
- Prefix requests with `[QUEST]`, `[SWAP]`, `[UI]`, or `[FIREBASE]` for faster routing
- I will return code in diff-style or full-file format based on complexity
- I will always note breaking changes and migration steps
- You maintain the repo; I supply the blueprints, patches, and deployment commands
- All sensitive keys will be handled via environment variables or GitHub Secrets. I will never hardcode credentials.

---
🔥 *The hearth is set. The boards are cleared. Speak your first command, Commander. Shall we polish the frontend for GitHub Pages, architect the JS module structure, or draft the Firestore schema for tomorrow's raid?*
