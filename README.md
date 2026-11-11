# Rest Tracker (Lull)

A personal sleep tracker that runs as a single static page. Log each morning in about 20 seconds, and Lull works out your bedtime, picks one habit to focus on each week, scores your nights, and explains your patterns in plain words.

## What it does

- **Home**: a quick log, tonight's bedtime with a countdown, this week's habit, and one key number tied to your goal. After you log, Luna offers a morning readout.
- **Luna, the coach**: a chatbot with its own tab. She knows your logged nights, your goal and the patterns Lull found, remembers the conversation, and - when the page runs inside claude.ai with Claude available - can act for you: log a night, log caffeine, change your schedule settings or set your weekly habit, but only when you ask, with a visible receipt in the chat for every change.
- **Setup in 30 seconds**: your goal, wake time, how much sleep you need, and a few habits. These choose your first habit and what Lull highlights.
- **One habit a week**: Lull picks the habit most likely to help you (from your answers, then from your own nights). Most habits are checked automatically from your log, and at the end of the week it compares your sleep with the week before.
- **Insights**: a plain-language summary, a sleep score chart, what helps and what hurts (with a confidence label), your body clock (chronotype, regularity, social jet lag) and a sleep coach.
- **Tools**: energy forecast, caffeine tracker, nap planner with timer, jet lag planner, guided breathing and a bedroom check.
- **Me**: your profile, schedule, clock and unit preferences, your nights, and export or backup.

## Run it

Open `index.html` in a browser, or serve the folder with any static server:

```bash
python3 -m http.server 8000
```

Your nights are stored in the browser (`localStorage`). Use **Me > Your data** to save a backup file or copy backup text.

## Notes

- Everything shown comes from the nights you log. There is no sample or placeholder data.
- Luna answers with Claude when the page is opened inside claude.ai, and that is also when she can make changes for you (each change needs your request and shows a receipt). Opened on its own, or if Claude can't be reached, she answers from Lull's built-in analysis of your logged nights, so the coach always works - she just can't act for you there.
- Syncing to an account and saving files through the app also need claude.ai. Opened on its own, the page works fully from your browser's storage.
- The sleep score, energy forecast and light timing for jet lag are estimates from published models, not medical measurements.
- Lull gives general sleep guidance and is not medical advice. Persistent insomnia, loud snoring with gasping, or sleepiness that makes driving unsafe are reasons to see a doctor.
