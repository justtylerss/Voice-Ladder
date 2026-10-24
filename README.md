# Voice Ladder

A daily beginner singing routine that runs in the browser, about 11 minutes a day.

**Live app:** https://justtylerss.github.io/Voice-Ladder/

## The routine

| Step | What you do |
|------|-------------|
| do · Breathe | A 4-count inhale, then a steady hiss, with a timer and a personal best |
| re · Warm up | Lip trills or hums sliding along with a reference tone |
| mi · Match the note | Play a note, sing it back, hold it |
| fa · Five-note scale | do re mi fa sol fa mi re do, moving up a half step each round |
| sol · Cool down | Quiet hums sliding down |

## Pitch tracking

- **Live mic:** wear headphones, tap *Live mic*, and sing. The readout shows the nearest target note, how many cents off you are, and whether to go higher or lower.
- **Upload a take:** a voice memo or video gets graphed against the target notes.

Pitch detection uses the YIN algorithm, running entirely in the browser. No audio leaves your device.

## Saving and sync

Your practice log (streak, breath times, accuracy) is saved in the browser's local storage. To share it across your phone and computer, connect each device under **Sync your phone and computer** with a GitHub token that has only `gist` scope. The app keeps the log in a private gist (`voice-ladder-log.json`) and merges by day, keeping whichever device's change is newest. It syncs when the app opens, after each change, and when you come back to the tab.

The token is stored only in each device's local storage. You can revoke it anytime at github.com/settings/tokens.

## Files

`index.html` is the entire app: HTML, CSS, and JavaScript in one file, with no build step.
