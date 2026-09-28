# Bug Report — Lumbricina

| Bug ID | Test Case ID | Title | Status | Preconditions | Severity | Priority | Steps to Reproduce | Expected Result | Actual Result |
|---|---|---|---|---|---|---|---|---|---|
| PASBUG-1 | TC-PAS-03 | Bonus timer misconfigured | Closed (fixed) | Debug mode active | Medium | Medium | Observe bonus counter | 50 cycles | Debug menu showed 40 cycles instead of 50 as specified; fixed in vFINAL |
| PASBUG-2 | TC-PAS-05 | Red pill doesn't show score increase | Closed (fixed) | Game running, red pill visible | High | High | Eat the red pill | Score +100 | Score did not increase; fixed in vFINAL |
| PASBUG-3 | TC-PAS-06 | Red pill doesn't increase length | Closed (fixed) | Game running, red pill visible | High | High | Eat the red pill | Length +1 | Length did not increase as specified |
| PASBUG-4 | TC-PAS-07 | Green pill inverts the wrong keys | Closed (fixed) | Green pill available | Medium | Medium | Eat green pill and move | Left/right controls inverted | Up/down controls were inverted instead of left/right, per spec |
| PASBUG-5 | TC-PAS-09 | Blue pill doesn't add points | Closed (fixed) | — | High | High | Eat the blue pill | Score +500 | Score did not increase; fixed in vFINAL |
| PASBUG-6 | TC-PAS-10 | Black pill doesn't trigger Game Over | Closed (fixed) | Black pill available | High | High | Eat the black pill | Immediate Game Over | Pill could be eaten with no effect at all; fixed in vFINAL |
| PASBUG-7 | TC-PAS-11 | Orange pill never spawns | Open | Game running, waiting for spawn | Low | Low | Observe spawns during gameplay | Should spawn with a low probability | Never appeared in vFINAL — spawn probability parameter may be misconfigured |
| PASBUG-8 | TC-PAS-12 | Yellow pill doesn't reduce speed / wrongly increases length | Closed (fixed) | Yellow pill available | Medium | Medium | Eat the yellow pill | Lower speed, no length change | Increased length in v1 instead; fixed in vFINAL (correctly lowers speed) |
| PASBUG-9 | TC-PAS-13 | Green pill doesn't award 1000 points | Open | Green pill available | Medium | Medium | Eat the green pill | Score +1000 and reversed controls | Controls reverse correctly, but score is not added — still open |
| BUGLOG-1 | TLOG-02 | Game cannot be paused | Open | Game running | High | High | Start the game, then press the pause key | Game pauses | Game does not pause — no key currently triggers it |
| BUGLOG-2 | TLOG-03 | Game cannot be resumed after pausing | Open | Game running, then paused | Medium | Medium | Pause the game with the designated key | Game resumes | Cannot resume, since pausing itself doesn't work / paused state isn't reachable |
| HSBUG-1 | TC-HS-02 | Only 3 highscores shown instead of 5 | Closed (fixed) | Game ended, multiple scores recorded | Medium | Medium | Play several rounds and record scores | Top 5 scores shown | Only 3 shown in v1; fixed in vFINAL (now shows 5) |
| HSBUG-2 | TC-HS-03 | Name field accepts more than 30 characters | Open | End of game | Medium | Medium | Enter a name longer than 30 characters and confirm | Input limited to 30 characters, per spec | Accepts more than 30 characters in both v1 and vFINAL — fix pending |

**Summary:** 13 bugs logged — 10 fixed and verified via regression testing on Build vFINAL, 3 remain open (low-severity spawn issue, pause/resume feature missing, and name field length not enforced).
