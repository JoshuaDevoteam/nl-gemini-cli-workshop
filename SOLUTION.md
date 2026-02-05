# Facilitator Guide

Notes for running the Gemini CLI Mario Platformer workshop.

## Timing

| Exercise | Estimated | Buffer | Notes |
|----------|-----------|--------|-------|
| 00 - Setup | 5 min | +3 min | Auth can be slow on restricted networks |
| 01 - GEMINI.md | 5 min | +2 min | Some participants may overthink the content |
| 02 - Movement | 7 min | +3 min | First real interaction, expect questions |
| 03 - Coins | 7 min | +3 min | Multi-step prompting is new for most |
| 04 - Enemy | 7 min | +5 min | Most complex, iterations take time |
| **Total** | **31 min** | **+16 min** | **~45 min with buffer** |

## Before the Workshop

1. **Test Gemini CLI access** - Make sure participants can install npm packages and authenticate with Google
2. **Pre-clone the repo** if network is unreliable
3. **Have `index.html` open** in a browser tab to demo the starting state
4. **Have the final solution open** in another tab to show what they'll build

## Common Issues

### Exercise 00 - Setup
- **npm permission errors**: Use `npx @google/gemini-cli` as alternative
- **Auth fails in corporate browser**: Try incognito/private window
- **"command not found"**: PATH not configured for npm global bin. Run `npm config get prefix` and add `/bin` to PATH

### Exercise 01 - GEMINI.md
- **Participants copy GEMINI.md verbatim**: Encourage them to ask Gemini CLI to help create it by reading the code first
- **File not detected**: Must be in the project root, named exactly `GEMINI.md`

### Exercise 02 - Movement
- **Player moves but clips through platforms**: The existing collision detection only handles vertical collisions. This is fine for the tutorial scope.
- **Movement too fast/slow**: Encourage iteration - "Make the player move slower" is a valid follow-up prompt
- **Player walks off screen**: Boundary checking might be missed. Prompt: "The player can walk off the edge of the screen, add boundary checking"

### Exercise 03 - Coins
- **Coins placed inside platforms**: Ask Gemini CLI to reposition them above platforms
- **Score doesn't update**: Check that the `score` variable is being incremented in the collision check
- **Too many coins**: Participants might ask for more than 5 - that's fine, but remind them to update the HUD denominator

### Exercise 04 - Enemy
- **Stomp detection unreliable**: The velocity-based check can be finicky. If participants struggle, suggest: "Make the stomp detection more generous - check if the player's bottom half overlaps the enemy's top half"
- **Game over triggers immediately**: Enemy might spawn too close to player start position. Adjust patrol range
- **R key doesn't restart**: Make sure the keydown listener checks for `KeyR` (not `r`)

## Alternative Prompts That Work Well

### Exercise 02
- "Look at the update function. There's a TODO comment about movement. Implement it using the existing player.speed and FRICTION values."
- "The arrow keys are already tracked in the keys object. Add code to move the player left and right with acceleration and friction."

### Exercise 03
- "Add golden coins that float above each platform. Make them bob up and down gently."
- "Now add a score counter. Show it in the top-right. When I collect all coins, show a message."

### Exercise 04
- "Add a bad guy that walks back and forth on the ground. If I touch it from the side, game over. If I jump on it, it dies."
- "I want an enemy, game over screen, and a win condition. The win condition is: all coins collected and enemy defeated."

## Tips for Running the Workshop

- **Demo first**: Show the starting game and the finished game side by side before starting
- **Encourage experimentation**: The exact prompts don't matter - participants should learn to iterate
- **Celebrate variations**: Different participants will get different results - that's the point
- **Don't rush**: If someone is stuck on Exercise 02, it's better to get that working well than to rush through all 4
- **Use the solutions**: If someone falls behind, they can copy a solution file and continue from there
- **Pair programming**: Encourage participants to work in pairs - one types prompts, one reviews changes

## Post-Workshop

- Ask participants what surprised them about using Gemini CLI
- Discuss: When would you use AI CLI tools vs. a regular IDE?
- Challenge: "Add one more feature to the game on your own using Gemini CLI"
