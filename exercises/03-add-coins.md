# Exercise 03: Add Coins & Score

**Time: ~7 minutes**

## Objective

Use Gemini CLI to add collectible coins on platforms and a score HUD.

## What You'll Learn

- Multi-step prompting (building features incrementally)
- Iterative refinement of visual elements
- Using `/compress` to manage long conversations

## Instructions

### Step 1: Add Coins

Send this prompt to Gemini CLI:

```
Add 5 collectible coins to the game. Place them floating above the platforms.
Each coin should be a yellow circle that bobs up and down with a gentle
animation. When the player touches a coin, it should disappear. Use the
existing checkCollision function for detection.
```

Review and approve the changes. Test in your browser - you should see yellow coins floating above platforms.

### Step 2: Add Score Display

Now add the score HUD:

```
Add a score display in the top-right corner showing "Coins: X/5" where X
is the number of coins collected. Use a retro pixel-style font. Make the
text white with a dark shadow for readability.
```

### Step 3: Iterate on the Visuals

Try refining the experience:

```
Add a small sparkle/particle effect when a coin is collected.
```

Or:

```
Make the coins rotate by drawing them as an ellipse that changes width over time.
```

### Step 4: Compress if Needed

If your conversation is getting long, use:

```
/compress
```

This summarizes the conversation history to free up context space while preserving important details.

## Expected Result

- 5 coins visible on platforms, gently bobbing up and down
- Coins disappear when the player touches them
- Score display in the top-right showing "Coins: X/5"
- Score updates when coins are collected

## Tips

- **Build incrementally**: Add coins first, then the HUD. Don't try to do everything in one prompt.
- **Be visual**: Describe what you want to *see*, not just the code structure
- **Iterate on feel**: If the bobbing is too fast or coins are too small, say so in a follow-up prompt
- If you notice Gemini CLI losing track of earlier changes, use `/compress` to refresh context

## Bonus Challenges

1. "Add a sound effect when collecting a coin" (using Web Audio API)
2. "Make coins have a golden glow effect"
3. "Show a floating +1 text that fades upward when a coin is collected"
4. "Add a celebration effect when all 5 coins are collected"

## Stuck?

Compare with the reference solution: [`solutions/index-after-ex03.html`](../solutions/index-after-ex03.html)

## Next Up

[Exercise 04: Add Enemy](04-add-enemy.md) - Add a patrolling enemy with game over and win conditions.
