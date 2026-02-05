# Exercise 00: Setup Gemini CLI

**Time: ~5 minutes**

## Objective

Install Gemini CLI, authenticate with your Google account, and run your first prompt.

## What You'll Learn

- How to install Gemini CLI via npm
- How to authenticate with Google OAuth
- How to run a one-shot prompt
- How to start an interactive session

## Instructions

### Step 1: Install Gemini CLI

Open your terminal and run:

```bash
npm install -g @google/gemini-cli
```

Verify the installation:

```bash
gemini --version
```

### Step 2: Authenticate

Start Gemini CLI for the first time:

```bash
gemini
```

This will open your browser for Google OAuth authentication. Sign in with your Google account and authorize the CLI.

### Step 3: Test with a One-Shot Prompt

Try a quick one-shot prompt to verify everything works:

```bash
gemini -p "What is 2 + 2?"
```

You should see Gemini respond with the answer.

### Step 4: Start an Interactive Session

Navigate to the project directory and start an interactive session:

```bash
cd gemini-cli-tes
gemini
```

You're now in an interactive Gemini CLI session! Type your prompts and press Enter to send them.

## Expected Result

- Gemini CLI is installed and accessible from your terminal
- You've authenticated with your Google account
- You can run prompts and get responses
- You have an interactive session running in the project directory

## Tips

- If `gemini` is not found, make sure your npm global bin directory is in your PATH
- You can exit the interactive session with `exit` or `Ctrl+D`
- Use `Ctrl+C` to cancel a generation in progress

## Next Up

[Exercise 01: Create GEMINI.md](01-create-gemini-md.md) - Give Gemini CLI context about your project.
