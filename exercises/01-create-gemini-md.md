# Exercise 01: Create GEMINI.md

**Time: ~5 minutes**

## Objective

Create a `GEMINI.md` context file that gives Gemini CLI persistent knowledge about your project.

## What You'll Learn

- What `GEMINI.md` is and why it matters
- How to structure a context file
- How to verify Gemini CLI reads your context
- The `/memory show` command

## Background

`GEMINI.md` is a special file that Gemini CLI automatically reads when starting a session. It gives the AI persistent context about your project - like a README specifically for your AI assistant.

This means you don't have to repeat project details in every prompt. Gemini CLI will already know:
- What your project does
- What technologies you're using
- Your coding conventions
- Important architecture details

## Instructions

### Step 1: Create the File

Create a file called `GEMINI.md` in the project root (same level as `index.html`).

You can create this manually, or ask Gemini CLI to help:

```
Create a GEMINI.md file for this project. Look at the existing code first.
```

### Step 2: Add Project Context

Your `GEMINI.md` should include these sections:

```markdown
# Gemini CLI Mario Platformer

## Project Overview
A browser-based 2D Mario-style platformer game. Single HTML file with embedded CSS and JavaScript using HTML5 Canvas.

## Tech Stack
- Pure HTML5, CSS3, JavaScript (no frameworks or build tools)
- HTML5 Canvas API for rendering
- Single file: index.html

## Architecture
- Canvas: 800x500 pixels
- Game loop: requestAnimationFrame
- Collision: AABB (Axis-Aligned Bounding Box)
- Sections marked with comment headers (e.g., // ======== PLAYER ========)

## Coding Style
- Use const for constants, let for variables
- All game objects are plain objects (not classes)
- Colors as hex strings
- Keep everything in a single index.html file

## Canvas Coordinates
- Origin (0,0) is top-left
- X increases to the right (0 to 800)
- Y increases downward (0 to 500)
- Ground is at y=460
```

### Step 3: Verify It Works

In your Gemini CLI session, run:

```
/memory show
```

You should see the contents of your `GEMINI.md` file displayed. This confirms Gemini CLI is reading your project context.

### Step 4: Test the Context

Ask Gemini CLI a question that requires project knowledge:

```
What is the canvas size for this game?
```

Gemini should answer correctly based on your `GEMINI.md` context, without needing to read the file.

## Expected Result

- A `GEMINI.md` file exists in the project root
- `/memory show` displays your context
- Gemini CLI can answer project-specific questions

## Tips

- Keep `GEMINI.md` concise - it's read on every session start
- Update it as your project evolves
- You can have both a global `~/.gemini/GEMINI.md` and a project-level one
- The project-level file takes priority for project-specific context

## Bonus Challenge

Add a "Known Issues" section to your `GEMINI.md` that mentions:
- Left/right movement is not implemented yet
- No collectibles or enemies
- No score tracking

This will help Gemini CLI understand what needs to be built!

## Next Up

[Exercise 02: Add Movement](02-add-movement.md) - Use Gemini CLI to add left/right movement to the player.
