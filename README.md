# Frequency Adventure: How Often? ⏰

A free, client-side ESL learning game for first-grade learners (Pre-A1/A1).

## Files

- `index.html` — entry point
- `style.css` — visual design and responsive styles
- `script.js` — lessons, 71 activities, 5 worlds, Ticky, feedback, scores and storage

## Publish on GitHub Pages

1. Create a **public** GitHub repository, e.g. `frequency-adventure`.
2. Upload `index.html`, `style.css`, and `script.js` directly into the repository root (not inside another folder).
3. Open repository **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select **main** and **/(root)**, then **Save**.
5. Once GitHub completes deployment, open `https://YOUR-USERNAME.github.io/frequency-adventure/`.

No installation, backend, or API key is required. Some browsers have no supported English text-to-speech voice; the game still works without speech. Sound can be toggled.

## Learning experience

- 5 worlds with 14, 14, 14, 14, and 15 activities
- Modes: matching, multiple choice, fill-the-sentence, ordered sentence, story reading, spot the error, frequency calendar
- 3 illustrated mini-stories
- Frequency meter with approximate teaching percentages
- Hints, answer-specific explanations, optional Spanish assistance
- Local progress, badges, coins and stars

## Scoring

- First correct answer, no hint: 10 points
- Correct after hint/error: 5 points
- No points for incorrect attempts
- Replays award additional coins only when a new *best* world score is achieved
- Stars depend on correct first attempts: 3 (>=90%), 2 (>=70%), 1 otherwise

## Customize

Edit the `WORDS`, `ROUTINES`, `SENTENCES`, `STORIES`, `WORLDS` and activity-generation sections of `script.js`. Questions are constructed using `add(world,type,prompt,correct,options,extra)` with stable question IDs. The 71-question assertion must be updated if the number of questions changes.

## Privacy and accessibility

All progress is saved under the localStorage key `frequency_adventure_progress_v1` on the current browser/device. There are no profiles, third-party analytics, ads, or external requests. The game has tap-to-select alternatives for ordering and matching; no dragging is required. If local storage is unavailable, the game will remain playable without persistence.

## Quick manual testing

1. Check each world unlocks only after finishing the previous one.
2. Select wrong and right options on a quiz question; check feedback and progression.
3. Make and break a pair in matching mode.
4. Build and unbuild a sentence; check error and correct feedback.
5. Read each of the three stories and test multiple choice.
6. Complete a world and refresh the browser; ensure saved stars persist.
7. Replay a world without improving its score; coins must not increase.
8. Test on a narrow mobile viewport and with keyboard navigation.
9. Toggle Spanish assistance and sound, then refresh.
10. Verify links work from GitHub Pages repository subpath.

The game relies on native browser speech synthesis where available. Browser-specific audio playback should be verified on the target devices.
