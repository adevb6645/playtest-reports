# Playtest reports

A log of bugs found during playtesting, written up the way a QA tester would
document them on the job: clear repro steps, severity, type, and expected
versus actual behavior.

## Games covered

- **Crater Command** - browser-based multiplayer artillery game
- **Adrift** - Godot 4.7 top-down ship survival sim
- Other non-NDA titles found during independent play

## How reports are organized

Every bug is its own issue. Labels carry the metadata:

- `game:*` which game the bug was found in
- `severity:*` how much it affects the player
- `type:*` what kind of bug it is (logic, visual, audio, performance)
- `status:*` where it stands (open, confirmed, fixed, wontfix)

See [LABELS.md](./LABELS.md) for the full label reference.

## Filing a new report

Click "New issue" on this repo. The bug report template will prompt for
everything needed: game, severity, type, a summary, numbered repro steps,
expected versus actual behavior, and optional screenshots or video.

## Why this exists

This started as a way to track feedback on two games in active development,
and turned into a record of testing practice: writing reports that someone
else (a developer, or another tester) could act on without needing to ask
follow-up questions.
