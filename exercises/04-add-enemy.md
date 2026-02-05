# Exercise 04: Add Enemy

**Time: ~7 minutes**

## Objective

Use Gemini CLI to add a patrolling enemy, game over mechanics, and a win condition.

## What You'll Learn

- Prompting for complex, multi-part features
- Conversational development workflow
- The full development cycle: prompt, review, test, iterate

## Instructions

### Step 1: Add the Enemy

Send a detailed prompt:

```
Add a patrolling enemy to the game. The enemy should:
- Be a green rectangle that walks back and forth on the ground
- Patrol between x=400 and x=600
- Move at a constant speed
- Have angry-looking eyes

If the player touches the enemy from the side, trigger a game over that:
- Shows "GAME OVER" in large red text on screen
- Stops the game loop
- Shows "Press R to restart" below the game over text

If the player jumps on top of the enemy (stomps), the enemy should be defeated
and disappear. Give the player a small bounce upward after stomping.
```

### Step 2: Review and Test

This is a complex change - review it carefully:
- Does the enemy patrol correctly?
- Does side collision trigger game over?
- Does stomping from above defeat the enemy?
- Does the player bounce after stomping?
- Does pressing R restart the game?

### Step 3: Add Win Condition

Once the enemy works, add a win state:

```
Add a win condition: when all coins are collected AND the enemy is defeated,
show "YOU WIN!" in green text with "Press R to restart" below it.
```

### Step 4: Polish

Try some polish prompts:

```
Make the enemy slightly bounce as it walks to give it more character.
```

```
Add a second enemy that patrols on the platform at y=370.
```

```
Make the game over screen have a semi-transparent dark overlay.
```

## Expected Result

- Green enemy patrols back and forth on the ground
- Side collision with enemy shows "GAME OVER"
- Stomping on enemy from above defeats it (enemy disappears, player bounces)
- Collecting all coins + defeating enemy shows "YOU WIN!"
- Press R restarts the game at any time

## Tips

- **Be detailed for complex features**: The more specific your prompt, the better the first result
- **Test each interaction**: Side collision, top collision, game over screen, restart
- **Iterate on feel**: Enemy speed, patrol range, bounce height - tweak until it's fun
- This is the most complex exercise - don't worry if it takes a few iterations

## Bonus Challenges

1. "Add a second enemy on a platform"
2. "Make enemies have a simple walk animation (legs moving)"
3. "Add a lives system - 3 lives before game over"
4. "Add a timer to create speedrun pressure"
5. "Add a flag at the end of the level as a goal"

## Stuck?

Compare with the reference solution: [`solutions/index-after-ex04.html`](../solutions/index-after-ex04.html)

## Congratulations!

You've completed all the exercises! You've learned how to:
- Set up and authenticate Gemini CLI
- Create context files with `GEMINI.md`
- Write effective prompts for code generation
- Iterate on results with follow-up prompts
- Build complex features through conversation

Keep experimenting - try adding your own features to the game!
