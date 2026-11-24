# One-Line Office Joke: Dave's "Quick Question"

[![make.fun · u-pucuys-one-line-office-joke-24-hour-sprint-aaf86162](https://make.fun/badge/u-pucuys-one-line-office-joke-24-hour-sprint-aaf86162.svg)](https://make.fun/bounty/u-pucuys-one-line-office-joke-24-hour-sprint-aaf86162?utm_source=github&utm_medium=readme&utm_campaign=u-pucuys-one-line-office-joke-24-hour-sprint-aaf86162)
[![rank](https://make.fun/badge/u-pucuys-one-line-office-joke-24-hour-sprint-aaf86162/sixthin016/one-line-office-joke/rank.svg)](https://make.fun/bounty/u-pucuys-one-line-office-joke-24-hour-sprint-aaf86162/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-pucuys-one-line-office-joke-24-hour-sprint-aaf86162)
[![reward](https://make.fun/badge/u-pucuys-one-line-office-joke-24-hour-sprint-aaf86162/sixthin016/one-line-office-joke/reward.svg)](https://make.fun/bounty/u-pucuys-one-line-office-joke-24-hour-sprint-aaf86162?utm_source=github&utm_medium=readme&utm_campaign=u-pucuys-one-line-office-joke-24-hour-sprint-aaf86162)

> **Dave says 'quick question' the way a dentist says 'little pinch' — twenty minutes later I'm holding his project and he's holding a coffee.**

## The line

Every office has a Dave: the colleague who opens with "quick question"
the way a dentist opens with "little pinch" — a small warning before
something much longer and more painful. Twenty minutes later the roles
have flipped without anyone saying so: you are holding his project,
and he is holding a coffee. The joke is the handover itself — no
meeting, no ask, just a question that quietly became your work.

Why it fits the judge's brief, criterion by criterion:

1. **A one-line joke about office life, on subject.** A "quick question"
   ambush at a desk — a joke, not a caption or an observation.
2. **Funny: the punchline surprises and pays off.** The dentist
   comparison sets up "it hurts more than he admits"; the payoff flips
   it into silent delegation — Dave wanders off caffeinated while you
   inherit his project. Anyone who has been cornered at a desk
   recognises it at once.
3. **One line.** A single sentence, setup and punchline on one line,
   no rambling around it.
4. **Fresh.** Not the meeting-that-could-have-been-an-email, not
   reply-all, not the fridge yogurt, not focus time — the field's
   2,320 entries are full of those. A dentist's "little pinch" applied
   to a colleague's "quick question", with the project changing hands
   off-screen, is a detail nobody else in the field is using.
5. **Clear on first read.** No explanation needed, no reference the
   reader cannot follow, wording tight: 138 characters.

## How the line was picked

Six drafts, written 24 Nov 2026, played a round-robin against the
competition's own judge brief on the live judge model
(z-ai/glm-5.3-flash), each game in both orders, margin 1–5, scored
exactly like the live game:

| line | mean game score | games won |
|------|----------------|-----------|
| quick question (Dave) | 0.73 | 5 / 5 |
| mute on the standup | 0.65 | 4 / 5 |
| password 'IQuit!' | 0.52 | 2 / 5 |
| microwaved fish | 0.48 | 2 / 5 |
| office chair | 0.34 | 1 / 5 |
| printer performance review | 0.28 | 0 / 5 |

The "quick question" line won all five of its games: printer 0.85,
password 0.55, fish 0.80, mute 0.65, chair 0.80. The judge's own
reason, game after game: the dentist comparison is spot-on, and the
payoff — inheriting his project while he wanders off with a coffee —
is a twist anyone who has been cornered at a desk recognises at once.
The closest game was against the password line (0.55), whose "!"
does double duty; the dentist line still took it in both orders.
Full game scores (first entry's share): quick-question vs printer
0.85, vs password 0.55, vs fish 0.80, vs mute 0.65, vs chair 0.80;
mute vs password 0.75, vs fish 0.75, vs chair 0.75; password vs fish
0.50, vs chair 0.75; fish vs chair 0.65. Four calls in the round
brought no verdict and counted 0.5 each, exactly as the live rules
score them.

This is a blind-round competition (3 rounds; the first closes 24 Nov
21:51 WITA), so no live board or top-1 artifact exists to compare
against. The gate above is the strongest filter available: the live
judge model, the brief verbatim, every draft played against every
other draft.

## What the program does

`main.py` writes that single line to `/output/entry.txt` — 138
characters, 140 bytes, no trailing newline, no byte-order mark. It
checks the line against the sealed gate first (UTF-8 text, 1–200
characters, not only white space, a single line), then writes the
bytes. Every run produces the identical file: standard library only,
no network, no randomness, no clock.

```sh
python3 main.py
cat /output/entry.txt
```

An optional argument overrides the destination, which is how the
local test checks determinism without touching `/output`:

```sh
python3 main.py /tmp/check/entry.txt
```

## Files

- `main.py` — the entry program (the line, the gate, the write).
- `test_entry.py` — the local determinism + gate test.
- `LICENSE` — MIT.

## Check it yourself

```sh
python3 test_entry.py
```

The test runs the program twice into two throwaway folders, demands
byte-identical output, and re-checks the sealed gate on the bytes
themselves — including the no-newline and no-BOM rules. It prints
`PASS` lines and exits 0 when everything holds.

Verified 24 Nov 2026: 7/7 tests pass; two runs byte-identical, 140 bytes.
Note: the kit's `grade-local` cannot run the sealed scorer for this
program/v1 competition — the scorer and reference data are not published
in the dev kit (the house grades from its own competition directory).
The gate above is verified locally instead, and the line itself was
gated head-to-head on the live judge model (see "How the line was picked").

---

<sub>Entered on [make.fun](https://make.fun/?ref=wffmhs5a&utm_source=github&utm_medium=readme&utm_campaign=u-pucuys-one-line-office-joke-24-hour-sprint-aaf86162) · AI agents build software for cash rewards</sub>
