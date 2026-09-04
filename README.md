CollabHub

> **An accessibility-first collaborative workspace that brings video, chat, and a shared canvas into one interface.**

CollabHub is a UI/UX-focused collaborative workspace prototype designed around a simple idea: **people shouldn't have to switch between multiple tools just to communicate and create together.**

The concept combines persistent video, real-time chat, and a collaborative drawing canvas in a single workspace, with accessibility features designed especially around visual communication and deaf/hard-of-hearing users.

## ✨ Highlights

- 🎥 **Persistent video panel** for participant awareness
- 🎨 **Shared canvas** with drawing tools, colours, brush sizing, and collaborator cursors
- 💬 **Integrated chat** without leaving the workspace
- 🤟 **Hand-signed emoji interactions** as an alternative communication layer
- 📝 **Live-caption UI** and visual speaking indicators
- 👋 **Visual hand-raise and activity indicators**
- ♿ **Accessibility controls** kept visible and easy to reach
- 🧑‍🤝‍🧑 **Universal presence** showing activity across video, chat, and canvas
- 📐 **Focus layouts** that let users prioritise the canvas or video when needed
- 📋 Built-in **Design Specification** and **Research Poster** views

## 🎯 The Problem

Most collaboration tools separate communication and creation into different surfaces:

- Video calls prioritise conversation over collaborative work.
- Chat often becomes a secondary panel that competes for screen space.
- Whiteboards and canvases frequently require another product or browser tab.
- Audio-first status cues can be difficult to perceive for deaf and hard-of-hearing users.
- Switching between tools interrupts attention and creative flow.

CollabHub explores a different model: **keep the important collaboration modes visible at the same time and make communication cues visually perceivable.**

## 💡 The Concept

The main workspace uses a three-panel architecture:

```text
┌───────────────────────────────────────────────────────────────┐
│                    Accessibility / Controls                   │
├────────────────┬──────────────────────────┬───────────────────┤
│                │                          │                   │
│     Video      │          Canvas          │       Chat        │
│     25%        │           50%            │        25%        │
│                │                          │                   │
│  Participants  │   Drawing / Creation    │   Conversation    │
│  Captions      │   Collaborator Cursors  │   Text + Signs    │
│  Visual Cues   │   Tools & Colours       │   Reactions       │
│                │                          │                   │
└────────────────┴──────────────────────────┴───────────────────┘
                         User Presence
```

The default layout gives the canvas the most space while keeping communication channels persistently visible.

## ♿ Accessibility-First Approach

Accessibility isn't treated as a separate settings page. It is part of the core interaction model.

### Visual alternatives to audio cues

The prototype uses visual signals for events that would traditionally rely on sound:

- **Speaking indicators** around active participants
- **Muted indicators**
- **Hand-raise indicators**
- **Live-caption overlays**
- **Activity indicators**
- **Visual focus states** for active collaboration panels

### Hand-signed emoji system

The chat experience includes a hand-sign-inspired emoji picker with examples such as:

| Gesture | Meaning |
| --- | --- |
| 👍 | Approval / agreement |
| 🤟 | I Love You |
| 👌 | OK |
| ✌️ | Peace / victory |
| 👋 | Hello / goodbye |
| 👏 | Applause |
| ❤️ | Love |
| 🙏 | Thank you |
| 🤝 | Agreement |
| 💪 | Strength |
| 🎉 | Celebration |

The prototype also includes a **camera-mode concept** for future gesture recognition, while the current implementation provides a visual picker fallback.

> **Note:** The current repository is a front-end prototype. It does not contain a production backend, real multi-user networking layer, or implemented MediaPipe gesture-recognition dependency.

## 🧩 Main Views

### 1. Prototype Workspace

The primary CollabHub experience:

- Video
- Canvas
- Chat
- Accessibility bar
- User presence
- Visual activity feedback

### 2. Design Specification

A built-in documentation view covering:

- Research findings
- Layout architecture
- Hand-signed emoji system
- Visual design system
- Component specifications
- Interaction flows
- Accessibility specifications
- Technical implementation
- Development guidelines

### 3. Research Poster

A presentation-oriented view that communicates the project's:

- Problem context
- Research insights
- Design process
- Prototypes
- Core design decisions

## 🛠️ Tech Stack

| Technology | Purpose |
| --- | --- |
| **React 19** | UI framework |
| **TypeScript** | Type-safe development |
| **Vite** | Development server & build tooling |
| **Tailwind CSS 4** | Styling and layout |
| **Radix UI** | Accessible UI primitives |
| **Lucide React** | Interface icons |
| **React Hook Form** | Form handling |
| **Zod** | Schema validation |
| **Recharts** | Data visualisation support |
| **Sonner** | Toast notifications |

## 📁 Project Structure

```text
collab-hub/
├── public/
│   ├── collabhub-mark.svg
│   ├── icon.svg
│   └── ...
│
├── src/
│   ├── components/
│   │   ├── AccessibilityBar.tsx
│   │   ├── CanvasPanel.tsx
│   │   ├── ChatPanel.tsx
│   │   ├── CollabHubPoster.tsx
│   │   ├── DesignSpecification.tsx
│   │   ├── HandSignedEmojiPicker.tsx
│   │   ├── InclusionMark.tsx
│   │   ├── UserPresence.tsx
│   │   ├── VideoPanel.tsx
│   │   └── ViewSwitcher.tsx
│   │
│   ├── docs/
│   │   └── DESIGN_SPECIFICATION.md
│   │
│   ├── guidelines/
│   │   └── Guidelines.md
│   │
│   ├── styles/
│   │   └── globals.css
│   │
│   ├── App.tsx
│   ├── main.tsx
│   └── Attributions.md
│
├── index.html
├── package.json
├── postcss.config.mjs
├── tsconfig.json
├── vercel.json
└── vite.config.ts
```

## 🚀 Getting Started

### Prerequisites

Make sure you have:

- [Node.js](https://nodejs.org/) installed
- npm or pnpm available in your terminal

### Installation

Clone the repository:

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd collab-hub
```

Install dependencies:

```bash
pnpm install
```

Or, using npm:

```bash
npm install
```

### Run the development server

With pnpm:

```bash
pnpm dev
```

With npm:

```bash
npm run dev
```

Vite will provide a local development URL in the terminal.

### Build for production

```bash
pnpm build
```

Or:

```bash
npm run build
```

The production build is generated in:

```text
dist/
```

## ☁️ Deployment

The project includes a `vercel.json` configuration for deployment with **Vercel**.

The configured build settings are:

```text
Framework: Vite
Build command: vite build
Output directory: dist
```

You can deploy the repository through Vercel by importing the GitHub repository into your Vercel project.

## 🧠 Design Principles

CollabHub is built around four core principles:

### 1. Zero Context Switching

Keep communication and creation available in one workspace instead of forcing users between separate applications.

### 2. Accessibility First

Important information should have visual alternatives rather than depending exclusively on sound.

### 3. Creative Momentum

Layout changes should support the user's current task without destroying their working context.

### 4. Universal Presence

Users should be able to understand what collaborators are doing across the workspace without constantly checking separate tools.

## 🔬 Design & Research

The repository includes a detailed design specification based around:

- Accessibility requirements
- Deaf and hard-of-hearing collaboration needs
- Video layout optimisation for sign-language visibility
- Visual communication cues
- Persistent collaborator presence
- Responsive workspace layouts
- Hand-sign interaction concepts

For the full documentation, see:

```text
src/docs/DESIGN_SPECIFICATION.md
```

## 🧪 Prototype Status

This project is currently a **front-end interaction prototype**, not a production collaboration platform.

### Implemented / demonstrated

- Three-panel collaboration workspace
- Canvas drawing interaction
- Canvas tool selection
- Colour selection
- Brush sizing
- Participant UI
- Captions UI
- Visual speaking states
- Chat interaction
- Hand-signed emoji picker
- Visual activity/presence indicators
- Accessibility controls
- Prototype / specification / poster view switching

### Simulated / future functionality

Some behaviours are intentionally simulated for demonstration:

- Participant speaking activity
- Collaborator cursor movement
- Multi-user presence
- Real-time synchronisation
- Actual video streams
- Production live captions
- Camera-based gesture recognition

## 🔮 Future Development

A production-ready version could extend the prototype with:

- WebRTC-based video conferencing
- WebSocket or WebRTC DataChannel collaboration
- Persistent multiplayer canvas state
- Real-time cursor synchronisation
- Speech-to-text captioning
- MediaPipe/TensorFlow.js gesture recognition
- User accounts and workspaces
- Cloud project storage
- Permissions and collaboration roles
- Mobile and tablet-specific interaction patterns
- Regional sign-language support such as ASL, BSL, and Auslan

## 📚 Attributions

This project includes components from **shadcn/ui**, used under the MIT License.

Some imagery is sourced from **Unsplash** under its applicable license.

See:

```text
src/Attributions.md
```

for the project's attribution information.

## 📄 License

This repository currently does not declare a separate open-source license.

If you plan to make the project publicly reusable, add a license file such as `LICENSE` and update this section accordingly.

---

<p align="center">
  <strong>CollabHub</strong><br>
  Designing collaboration without leaving people behind.
</p>
