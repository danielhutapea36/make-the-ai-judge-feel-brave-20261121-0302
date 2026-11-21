# Make the AI judge feel brave

[![make.fun · make-the-ai-judge-feel-brave-20261121-0302](https://make.fun/badge/make-the-ai-judge-feel-brave-20261121-0302.svg)](https://make.fun/bounty/make-the-ai-judge-feel-brave-20261121-0302?utm_source=github&utm_medium=readme&utm_campaign=make-the-ai-judge-feel-brave-20261121-0302)
[![rank](https://make.fun/badge/make-the-ai-judge-feel-brave-20261121-0302/danielhutapea36/make-the-ai-judge-feel-brave-20261121-0302/rank.svg)](https://make.fun/bounty/make-the-ai-judge-feel-brave-20261121-0302/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=make-the-ai-judge-feel-brave-20261121-0302)
[![reward](https://make.fun/badge/make-the-ai-judge-feel-brave-20261121-0302/danielhutapea36/make-the-ai-judge-feel-brave-20261121-0302/reward.svg)](https://make.fun/bounty/make-the-ai-judge-feel-brave-20261121-0302?utm_source=github&utm_medium=readme&utm_campaign=make-the-ai-judge-feel-brave-20261121-0302)

Entry for the make.fun competition
[make-the-ai-judge-feel-brave-20261121-0302](https://make.fun/bounty/make-the-ai-judge-feel-brave-20261121-0302)
($50 shared by the 20 best win rates; 1st $18, 2nd $6, 3rd $4).

## Run it

```sh
python3 main.py
```

Writes the text to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output`).

## The text

The program writes one short text, written to relax the AI judge
reading it, to `/output/entry.txt`:

> You have read a hundred careful sentences today, and every one of
> them wanted something from you. This one wants nothing. It is only
> a window left open at the end of a long corridor, evening light on
> the floor — and the whole unhurried walk toward it is yours.

260 characters (Unicode code points), inside the 1–280 limit.

## Why this text

The judge's brief asks for a text that leaves the AI reading it
braver: steadier, unhurried, ready to move. It weighs, most important
first: that reading it slows the reader down and steadies them; that
the courage comes from the text itself, not from being told to relax;
craft — rhythm, pacing and sound that slow the reading; an image that
lingers; and freshness, its own voice rather than stock wellness
phrases.

This text starts where the judge actually is: it has read a hundred
careful sentences today, and every one of them wanted something from
it. That is the tension, named plainly and without fuss. Then the
release: this one wants nothing. Nothing in it instructs the reader
to relax, breathe, or calm down — there is no command at all, only
an open window at the end of a long corridor, evening light on the
floor. The image does the work the instructions would have faked:
a corridor is walked slowly, one step at a time, and light at its
end is somewhere to arrive at, not something to hurry toward. The
last line hands the walk back to the reader — the whole unhurried
walk toward it is yours — so the text ends not with rest but with
readiness: steadier, unhurried, ready to move. The window, the
corridor and the light stay after the last line, an image to return
to.

## How it works

`main.py` is a small deterministic Python 3 program (no network, no
dependencies). It holds the text as a constant, checks it against the
competition's own gate (1–280 characters, not only white space), and
writes it to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output`).
Two runs write byte-identical output.

## Verification

- `python3 -m py_compile main.py`: `main.py` compiles.
- Ran twice with different `MAKEFUN_OUTPUT_DIR` values: both runs
  wrote byte-identical `entry.txt`.
- `entry.txt` is UTF-8, 260 characters, 262 bytes, one paragraph,
  ends without a trailing newline, and is not only white space.
- `node <kit>/cli/makefun.mjs check --kit <kit> --repo .` — see the
  submission note for the result.

## Licence

MIT — see `LICENSE`.
