# Learn Gemini CLI - Mario Platformer

Build a Mario-style platformer game while learning how to use **Gemini CLI** - Google's AI-powered command-line coding assistant.

You'll start with a partially working game (jumping works, but you can't move left or right!) and use Gemini CLI to add features through guided exercises.

## What You'll Build

A browser-based 2D platformer with:
- Player movement and physics
- Collectible coins with animations
- Score display
- Patrolling enemies
- Game over and win conditions

## What You'll Learn

| Concept | Exercise |
|---------|----------|
| Installing and authenticating Gemini CLI | Exercise 00 |
| Creating `GEMINI.md` context files | Exercise 01 |
| Natural language prompting & file editing | Exercise 02 |
| Multi-step prompting & iteration | Exercise 03 |
| Complex feature development | Exercise 04 |

## Prerequisites

- **Google Account** (for Gemini CLI authentication)
- **Node.js 20+** ([download](https://nodejs.org/))
- **A modern browser** (Chrome, Firefox, Edge)
- **A terminal** (Terminal.app, iTerm2, Windows Terminal, etc.)

## Quick Start

### 1. Install Gemini CLI

```bash
npm install -g @anthropic-ai/gemini-cli
```

### 2. Clone This Repo

```bash
git clone <repo-url>
cd gemini-cli-tes
```

### 3. Open the Game

Open `index.html` in your browser. You should see a character that can jump but can't move left or right.

### 4. Start the Exercises

| # | Exercise | Time | What You'll Learn |
|---|----------|------|-------------------|
| 00 | [Setup Gemini CLI](exercises/00-setup-gemini-cli.md) | 5 min | Install, authenticate, first prompt |
| 01 | [Create GEMINI.md](exercises/01-create-gemini-md.md) | 5 min | Context files, project memory |
| 02 | [Add Movement](exercises/02-add-movement.md) | 7 min | Prompting, file editing, iteration |
| 03 | [Add Coins & Score](exercises/03-add-coins.md) | 7 min | Multi-step prompts, refinement |
| 04 | [Add Enemy](exercises/04-add-enemy.md) | 7 min | Complex features, full dev cycle |

**Total time: ~30 minutes**

## Useful Gemini CLI Commands

| Command | Description |
|---------|-------------|
| `gemini` | Start interactive session in current directory |
| `gemini -p "prompt"` | One-shot prompt (non-interactive) |
| `/memory show` | Show active GEMINI.md context |
| `/tools` | List available tools |
| `/compress` | Compress conversation to save context |
| `/stats` | Show token usage statistics |
| `Ctrl+C` | Cancel current generation |
| `exit` or `Ctrl+D` | Exit Gemini CLI |

## Troubleshooting

### "command not found: gemini"
Make sure Node.js 20+ is installed and run:
```bash
npm install -g @anthropic-ai/gemini-cli
```

### Authentication issues
Run `gemini` and follow the OAuth prompts. Make sure you're signed into your Google account in the browser.

### Game doesn't load
- Make sure you're opening `index.html` directly in the browser (File > Open)
- Check the browser console (F12) for errors

### Gemini CLI doesn't see my files
Make sure you're running `gemini` from the project root directory (`gemini-cli-tes/`).

## Resources

- [Gemini CLI Documentation](https://github.com/google-gemini/gemini-cli)
- [Gemini CLI Blog Post](https://blog.google/technology/developers/gemini-cli/)
- [HTML5 Canvas MDN Docs](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)

## Solutions

If you get stuck, reference solutions are available in the [`solutions/`](solutions/) directory. Try to use Gemini CLI first though - that's the whole point!
