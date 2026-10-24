# Voice Ladder

A daily beginner singing routine that runs in the browser, about 11 minutes a day, with live mic feedback.

**Live app:** https://justtylerss.github.io/Voice-Ladder/

## The routine

| Step | What you do | What the mic shows |
|------|-------------|--------------------|
| do · Breathe | A 4-count inhale, then a steady "sss" | A hiss loudness bar with a steady zone; it stops the timer automatically and scores steadiness |
| re · Warm up | Lip trills or hums sliding up and down | Follow-the-dot graph: your pitch traced against the slide |
| mi · Match the note | Play a note, sing it back, hold it | A tuner bar (flat ← on pitch → sharp); hold in the green for 3 s to match |
| fa · Five-note scale | do re mi fa sol fa mi re do, moving up a half step each round | Sing it back: each note lights up ✓ / ~ / ✗ as you land it |
| sol · Cool down | Quiet hums sliding down | Follow-the-dot graph plus a check that you're singing softly |

## Voice type test

You sing your lowest clear note, then your highest comfortable note. The app charts your range against bass, baritone, tenor, alto, mezzo-soprano, and soprano, then suggests a starting note that fits your voice.

## Progress

The **Your progress** section tracks each metric per day (pitch accuracy in cents, time on pitch, scale notes hit, slide following, breath length, breath steadiness, and range). Each metric gets a chart with a least-squares trend line and a plain verdict: improving, holding steady, or dipping.

## Pitch tracking

- **Live mic:** wear headphones for the best results. Without headphones, the mic pauses while the app's own tones play.
- **Upload a take:** a voice memo or video gets graphed against the target notes.

Pitch detection uses the YIN algorithm, running entirely in the browser. No audio leaves your device.

## Saving and sync

Your practice log (streak, breath times, accuracy) is saved in the browser's local storage. To share it across your phone and computer, connect each device under **Sync your phone and computer** with a GitHub token that has only `gist` scope. The app keeps the log in a private gist (`voice-ladder-log.json`) and merges by day, keeping whichever device's change is newest. It syncs when the app opens, after each change, and when you come back to the tab.

The token is stored only in each device's local storage. You can revoke it anytime at github.com/settings/tokens.

## Files

`index.html` is the entire app: HTML, CSS, and JavaScript in one file, with no build step.
