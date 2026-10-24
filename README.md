# Voice Ladder

A daily beginner singing routine that runs in the browser, 5 to 20 minutes a day, with live mic feedback and a coach that adapts to your voice.

**Live app:** https://justtylerss.github.io/Voice-Ladder/

## The routine

| Step | What you do | What the mic shows |
|------|-------------|--------------------|
| do · Breathe | A 4-count inhale, then a steady "sss" | A hiss loudness bar with a steady zone; it stops the timer automatically and scores steadiness |
| re · Warm up | Lip trills, straw phonation, or hums sliding up and down (an octave from Level 3) | Follow-the-dot graph: your pitch traced against the slide |
| mi · Match the note | Play a note, sing it back, hold it (a full octave of notes from Level 2) | A tuner bar (flat ← on pitch → sharp); hold in the green to match |
| fa · Scales & arpeggios | 1-2-3-2-1, the 5-note scale, arpeggios, octave arpeggios, and the 9-note scale as you level up | Sing it back: the app plays one note, waits for you to land it, and checks it off ✓ / ~ / ✗ |
| sol · Cool down | Quiet hums sliding down | Follow-the-dot graph plus a check that you're singing softly |

## Coach

- **Levels 1–5** (Foundations → Pitch control → Range & registers → Agility → Polish). They follow the progression voice clinics use: glides and short scales, then arpeggios, wider leaps, sustained dynamics, and agility. The pitch target tightens from ±40¢ to ±15¢. Three strong sessions on different days unlock the next level.
- **Weak-spot coaching:** every note you sing is logged by pitch (average cents off and flat/sharp tendency), along with whether you go flat on rising notes, scoop into notes, or wobble on held notes. **Today's focus** turns that into plain advice and a drill on your weakest notes.
- **Coach tips** after each sing-back round, based on what the mic heard.
- **Level drills:** Hold & swell (*messa di voce*) from Level 3, and agility runs from Level 4.
- **Ear training mode** hides the needle until each note is done.

## Your plan

Session length (5 / 11 / 20 min), warm-up style (lip trills, straw, or hum), vowel (ah, ee, oo, or rotating daily), goal (pop, R&B, rock, musical theater, choir, or just for fun), which steps to include, and your level.

## Voice type test

You sing your lowest clear note, then your highest comfortable note, then (optionally) one slow slide so the app can find where your voice flips (your register break, or passaggio). It combines range and break to estimate bass, baritone, tenor, alto, mezzo-soprano, or soprano, then fits every exercise to that range: slides stay inside it, scales stop at your comfortable top, and the tuner warns you near the top.

## Progress

The **Your progress** section tracks each metric per day (pitch accuracy in cents, time on pitch, sing-back notes landed, slide following, breath length, breath steadiness, hold & swell control, and range). Each metric gets a chart with a least-squares trend line and a plain verdict: improving, holding steady, or dipping.

## Roadmap

Day 1, Week 1, Week 2, Month 1, Month 3, Month 6, and Year 1. Each milestone covers what to expect at roughly 15 minutes a day, 5–6 days a week, plus goals that check off automatically from your log.

## Pitch tracking

- **Live mic:** wear headphones for the best results. Without headphones, the mic pauses while the app's own tones play.
- **Upload a take:** a voice memo or video gets graphed against the target notes.

Pitch detection uses the YIN algorithm, running entirely in the browser. No audio leaves your device.

## Saving and sync

Your practice log (streak, breath times, accuracy) is saved in the browser's local storage. To share it across your phone and computer, connect each device under **Sync your phone and computer** with a GitHub token that has only `gist` scope. The app keeps the log in a private gist (`voice-ladder-log.json`) and merges by day, keeping whichever device's change is newest. It syncs when the app opens, after each change, and when you come back to the tab.

The token is stored only in each device's local storage. You can revoke it anytime at github.com/settings/tokens.

## Files

`index.html` is the entire app: HTML, CSS, and JavaScript in one file, with no build step.
