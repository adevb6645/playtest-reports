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
- `severity:*` how much it affects the player (high, medium, low)
- `type:*` what kind of bug it is (logic, visual, audio, performance,
  other). A bug can have more than one type if it has more than one
  root cause, for example a logic error that also causes a visual glitch.
- `status:*` where it stands (open, confirmed, fixed, wontfix)

See [LABELS.md](./LABELS.md) for the full label reference.

Labels do not get applied automatically just by filling out the issue
form. After submitting a report, open the issue and apply the matching
labels yourself using the gear icon next to "Labels" in the sidebar.

## Filing a new report

Click "New issue" on this repo. The bug report template will prompt for
everything needed: game, severity, type, a summary, numbered repro steps,
expected versus actual behavior, and optional screenshots or video.

After submitting, apply labels to the issue so it shows up correctly on
the dashboard (see below).

## Live dashboard

`playtest-dashboard.html` is a standalone page that pulls live data
straight from this repo's GitHub Issues using the public GitHub API. No
login or setup needed to view it, just a GitHub username and repo name.

It shows total/open/resolved counts, a breakdown by game, severity, type,
and status, and a list of recent reports. If this repo has GitHub Pages
enabled (Settings > Pages > Source: main branch, root folder), the
dashboard is reachable at a public URL without needing to download
anything.

## Why this exists

This started as a way to track feedback on two games in active development,
and turned into a record of testing practice: writing reports that someone
else (a developer, or another tester) could act on without needing to ask
follow-up questions.
