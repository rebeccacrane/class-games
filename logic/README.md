Formal Logic games

### Pixel Art Review Games

Self-checking pixel-art practice for Formal Logic. Each question a student gets right colors in part of a mystery picture. When the picture is done, they type their name and screenshot the score box for Teams.

### Files

| File | What it is |
|---|---|
| `pixel-art-template.html` | The game. Copy it for each new game and edit only the content block. The sample game is "A, E, I or O?" (20 propositions). |
| `picture-maker.html` | A drawing tool for new pictures. Start from a blank grid or drop in a photo: it averages the photo into the grid and reduces it to 2–12 colors (crop to fit, or show the whole photo with a white margin), then you can touch it up. Draw, copy the code, paste it over the `PICTURE` block in a game. To edit an existing picture, paste its `PICTURE` block into the code box and press **Load**. |

### Making a new game

1. Copy `pixel-art-template.html` and rename it (for example `square-of-opposition.html`).
2. Open it in a text editor and find the block marked **GAME CONTENT: EDIT ONLY THIS BLOCK**.
3. Change `TITLE`, `SUBTITLE` and `CHOICES`.
   - Buttons: `CHOICES = ["Valid","Invalid"]`, `["True","False","Unknown"]`, etc.
   - A single question can use its own buttons: `{x:"…", c:["Contraries","Subcontraries"], a:"Contraries", why:"…"}`
   - Typed answers: `CHOICES = []` (or `c:[]` on one question), and list the accepted spellings: `a:["middle term","the middle term"]`. Capitals and extra spaces are ignored.
4. Replace the `QUESTIONS` list. `x` is the question, `a` the answer (spelled exactly like its button), `why` one sentence shown after a right answer. Use `\n` inside `x` to stack lines, such as a syllogism.
5. Optional: draw a new picture in `picture-maker.html` and paste it over `PICTURE`.
6. Commit and push. With GitHub Pages turned on, the game is at `https://rebeccacrane.github.io/class-games/logic/<file>.html`.

### How it plays

- Any number of questions and any grid size works; the picture's pixels are split evenly among the questions in a fixed scattered pattern.
- Wrong answers can be retried (the wrong button is crossed out), so every student finishes the picture. The score counts answers right on the **first try**.
- Works on laptop, tablet and phone, in light and dark mode. No login, nothing is saved.

### Heads-up

Answers sit in the page's source code, so a determined student could find them with View Source. The same is true of the Google Sheets version's hidden answer tab.
