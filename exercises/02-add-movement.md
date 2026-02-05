# Exercise 02: Add Movement

**Time: ~7 minutes**

## Objective

Use Gemini CLI to add left/right arrow key movement to the player character.

## What You'll Learn

- Writing effective natural language prompts
- Reviewing and approving file edits
- Testing changes in the browser
- Iterating on results with follow-up prompts

## Background

Open `index.html` in your browser. Notice that:
- Jumping works (Space / ArrowUp)
- The player **cannot** move left or right

Look at the code: `player.velX`, `player.speed`, and `FRICTION` already exist but aren't being used. There's a `// TODO` comment in the `update()` function marking where movement code should go.

## Instructions

### Step 1: Write Your Prompt

In your Gemini CLI session, type a prompt like:

```
Add left/right arrow key movement to the player character. The player.speed,
player.velX, and FRICTION constants already exist. Use the keys object to
check for ArrowLeft and ArrowRight. Add the code where the TODO comment is
in the update function.
```

### Step 2: Review the Changes

Gemini CLI will propose changes to `index.html`. Before accepting:
- Read through the proposed code
- Make sure it uses the existing `player.speed` and `FRICTION` values
- Check that it modifies `player.velX` based on arrow key input
- Verify it applies friction when no keys are pressed

**Approve the file write** when you're satisfied with the changes.

### Step 3: Test in Browser

Refresh `index.html` in your browser. Try:
- Press ArrowLeft - player should move left
- Press ArrowRight - player should move right
- Release keys - player should slow down (friction)
- Jump while moving - should maintain momentum

### Step 4: Iterate

If something isn't right, ask Gemini CLI to fix it:

```
The player can walk off the left edge of the screen. Add boundary checking
so the player stays within the canvas (0 to 800).
```

Or if the movement feels off:

```
The movement feels too slippery. Increase the friction so the player stops faster.
```

## Expected Result

- Arrow keys move the player left and right
- Player slows down when keys are released (friction)
- Player stays within canvas boundaries
- Jumping while moving works smoothly

## Tips

- **Be specific**: Mention the exact variable names and where to add code
- **Reference existing code**: "Use the existing `player.speed` constant" is better than "add movement with speed 5"
- **One thing at a time**: If the first change isn't perfect, iterate with a follow-up prompt rather than starting over
- The `keys` object already tracks `ArrowLeft` and `ArrowRight` from the event listeners

## Bonus Challenges

Try these follow-up prompts:

1. "Make the player face the direction they're moving" (flip the eyes)
2. "Add a slight acceleration curve so movement feels more natural"
3. "Add a dust particle effect when the player changes direction"

## Stuck?

If your game isn't working, you can compare with the reference solution: [`solutions/index-after-ex02.html`](../solutions/index-after-ex02.html)

## Next Up

[Exercise 03: Add Coins & Score](03-add-coins.md) - Add collectible coins and a score display.
