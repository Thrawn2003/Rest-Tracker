# Rest Tracker (Lull)

A personal sleep tracker that runs as a single static page. Log each morning in about 20 seconds, and Lull works out your bedtime, picks one habit to focus on each week, scores your nights, and explains your patterns in plain words.

## What it does

- **Home**: a quick log, tonight's bedtime with a countdown, this week's habit, and one key number tied to your goal.
- **Setup in 30 seconds**: your goal, wake time, how much sleep you need, and a few habits. These choose your first habit and what Lull highlights.
- **One habit a week**: Lull picks the habit most likely to help you (from your answers, then from your own nights). Most habits are checked automatically from your log, and at the end of the week it compares your sleep with the week before.
- **Insights**: a plain-language summary, a sleep score chart, what helps and what hurts (with a confidence label), your body clock (chronotype, regularity, social jet lag) and an AI sleep coach.
- **Tools**: energy forecast, caffeine tracker, nap planner with timer, jet lag planner, guided breathing and a bedroom check.
- **Me**: your profile, schedule, clock and unit preferences, your nights, and export or backup.

## Run it

Open `index.html` in a browser, or serve the folder with any static server:

```bash
python3 -m http.server 8000
```

Your nights are stored in the browser (`localStorage`). Use **Me > Your data** to save a backup file or copy backup text.

## Notes

- Syncing to an account, saving files through the app, and the AI coach only work when the page is opened inside claude.ai as an artifact. Opened on its own, the page works fully offline from your browser's storage and hides the coach.
- The sleep score, energy forecast and light timing for jet lag are estimates from published models, not medical measurements.
- Lull gives general sleep guidance and is not medical advice. Persistent insomnia, loud snoring with gasping, or sleepiness that makes driving unsafe are reasons to see a doctor.
