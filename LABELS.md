# Labels for playtest-reports

Create these labels in the repo under Settings > Labels. GitHub starts you
with a few default labels (bug, enhancement, etc.) — you can delete those or
leave them, they will not interfere.

## Game labels

| Label | Color (hex) | Description |
|---|---|---|
| game:crater-command | 1D9E75 | Bug found in Crater Command |
| game:adrift | 7F77DD | Bug found in Adrift |
| game:other-indie | D85A30 | Bug found in another non-NDA title |

## Severity labels

| Label | Color (hex) | Description |
|---|---|---|
| severity:high | E24B4A | Breaks the game or blocks progress |
| severity:medium | EF9F27 | Noticeable, workaround exists |
| severity:low | B4B2A9 | Cosmetic or minor annoyance |

## Type labels

| Label | Color (hex) | Description |
|---|---|---|
| type:logic | 378ADD | Game behaves incorrectly |
| type:visual | D4537E | Rendering, UI, animation |
| type:audio | 5DCAA5 | Sound or music issue |
| type:performance | 854F0B | Lag, crash, freeze |
| type:other | 888780 | Does not fit the above |

## Status labels

| Label | Color (hex) | Description |
|---|---|---|
| status:open | C0DD97 | New, not yet looked at |
| status:confirmed | 639922 | Reproduced, confirmed real |
| status:fixed | 085041 | Fixed, close the issue when applying this |
| status:wontfix | 444441 | Will not be addressed, with a reason in a comment |

## How to set these up fast

Instead of clicking "new label" fourteen times, you can use the GitHub CLI
if it is installed:

```
gh label create "game:crater-command" --color 1D9E75 --description "Bug found in Crater Command"
gh label create "game:adrift" --color 7F77DD --description "Bug found in Adrift"
gh label create "game:other-indie" --color D85A30 --description "Bug found in another non-NDA title"
gh label create "severity:high" --color E24B4A --description "Breaks the game or blocks progress"
gh label create "severity:medium" --color EF9F27 --description "Noticeable, workaround exists"
gh label create "severity:low" --color B4B2A9 --description "Cosmetic or minor annoyance"
gh label create "type:logic" --color 378ADD --description "Game behaves incorrectly"
gh label create "type:visual" --color D4537E --description "Rendering, UI, animation"
gh label create "type:audio" --color 5DCAA5 --description "Sound or music issue"
gh label create "type:performance" --color 854F0B --description "Lag, crash, freeze"
gh label create "type:other" --color 888780 --description "Does not fit the above"
gh label create "status:open" --color C0DD97 --description "New, not yet looked at"
gh label create "status:confirmed" --color 639922 --description "Reproduced, confirmed real"
gh label create "status:fixed" --color 085041 --description "Fixed, close the issue when applying this"
gh label create "status:wontfix" --color 444441 --description "Will not be addressed, with a reason in a comment"
```

Run these from inside the cloned repo folder, after `gh auth login`.
