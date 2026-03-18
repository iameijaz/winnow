# Winnow

**Winnow your AI chat history** — view, search, and prune exported conversations from Claude and ChatGPT in one offline HTML file.

[![Use Winnow](https://img.shields.io/badge/Use%20Winnow-Live%20App-C7922B?style=for-the-badge)](https://iameijaz.github.io/winnow)
[![License: MIT](https://img.shields.io/badge/License-MIT-00BFFF?style=flat-square)](LICENSE)

---

## Use it now — no download needed

**[→ iameijaz.github.io/winnow](https://iameijaz.github.io/winnow)**

Open it in your browser, drop your export file, done.
Everything runs locally — your data never leaves your machine.

Or download `winnow.html` and open it as a file if you prefer to work offline.

---

## What is Winnow?

Before importing a conversation from one AI into another, you want to cut out the noise — the dead ends, the wrong turns, the parts that would just waste context. That's winnowing: separating what's worth keeping from what isn't.

Winnow is a single HTML file. No server, no install, no account. Drop your exported `.json` file from Claude or ChatGPT onto the page, read through your conversations, delete the ones (or parts) you don't want to carry forward, and export the remainder as clean JSON ready to use elsewhere.

---

## Features

| Feature | Detail |
|---|---|
| 📂 Drag & drop | Load one or multiple `.json` export files at once |
| 🤖 Multi-platform | Claude (`conversations.json`) and ChatGPT (`conversations.json`) — auto-detected |
| 📝 Markdown rendering | Headings, bold, italic, tables, blockquotes, code blocks |
| ∑ Math / LaTeX | Inline and display math via KaTeX — `$...$`, `$$...$$`, `\(...\)`, `\[...\]` |
| 🔍 Search | Search within a chat or across all conversations, with `▲▼` match navigation |
| 🧠 Thinking blocks | Claude extended thinking shown as collapsible sections |
| 🔧 Tool use | Claude tool calls (web search, MCP, computer use) as collapsible blocks |
| 📎 Attachments | Files attached to messages shown as pill badges |
| 🗑 Delete | Remove individual conversations or clear everything, with confirmation |
| 💾 Export | Save post-deletion conversations back to a clean `.json` file |
| ⌨️ Shortcuts | `Ctrl+K` / `/` to search, `Enter` / `Shift+Enter` to navigate, `Esc` to clear |
| 🌑 Dark UI | Clean dark theme |

---

## Getting Started

### Option A — use the hosted version (no download)

Go to **[iameijaz.github.io/winnow](https://iameijaz.github.io/winnow)** and drop your file on the page.

### Option B — download and run locally

```bash
# Clone the repo
git clone https://github.com/iameijaz/winnow.git

# Open the file — no server needed
open winnow.html   # macOS
xdg-open winnow.html   # Linux
start winnow.html  # Windows
```

Or just download `winnow.html` directly from the [releases page](https://github.com/iameijaz/winnow/releases) and open it.

---

## How to export your chats

### From Claude (Anthropic)

1. Go to [claude.ai](https://claude.ai)
2. Settings → Account → **Export data**
3. You'll receive an email with a download link
4. Extract the zip — load `conversations.json` into Winnow

### From ChatGPT (OpenAI)

1. Go to [chat.openai.com](https://chat.openai.com)
2. Settings → Data controls → **Export data**
3. You'll receive an email with a download link
4. Extract the zip — load `conversations.json` into Winnow

You can load both files at the same time — Winnow merges them into a single view and labels each conversation with a `Claude` or `GPT` badge. [Experimental Feature]

---

## Supported files

| File | Source | Contents |
|---|---|---|
| `conversations.json` | Claude | All your Claude conversations |
| `conversations.json` | ChatGPT | All your ChatGPT conversations |
| `projects.json` | Claude | Project metadata (no conversations) |

---

## Keyboard shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl+K` or `/` | Focus search |
| `Enter` | Next match |
| `Shift+Enter` | Previous match |
| `Esc` | Clear search |

---

## Privacy

Winnow is entirely client-side.

- Nothing is uploaded
- Nothing is sent to any server
- Nothing is stored between sessions (unless you explicitly export)

Everything runs in your browser's memory. The hosted GitHub Pages version has no backend, no analytics, no tracking of any kind — it serves a static HTML file, nothing more.

---

## Tech stack

| Library | Purpose |
|---|---|
| [marked.js](https://marked.js.org) | Markdown rendering |
| [KaTeX](https://katex.org) | Math / LaTeX rendering |
| Vanilla JS | Everything else |

No build step. No framework. No `node_modules`. The entire application is one HTML file.

---

## Deploy your own copy

Fork this repo, then enable GitHub Pages:

**Settings → Pages → Source: Deploy from branch → `main` / `(root)` → Save**

Your copy will be live at `https://<your-username>.github.io/winnow`.

---

## License

MIT — do whatever you want with it.

---

*Built by [Ijaz Ahmed](https://github.com/iameijaz)*
