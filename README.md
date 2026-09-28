# 🐛 Lumbricina — Manual QA Testing Project

Manual black-box functional testing project for **Lumbricina**, a Snake-style browser game, developed as a team final assignment for a Manual QA course.

## 👥 Team & My Role

This was a **group project** with three testers:

| Role | Person |
|---|---|
| QA Lead | Ema |
| Test Report | **Leandro Martín Pereyra** (me) |
| Bug Report | Germán |

All three contributed to writing and executing test cases across modules. My focus was on the **Test Report** and on writing/executing test cases for the **Movement** and **Collision** modules.

## 🎯 Testing Objective

🎮 **Play the game:** [v1](https://nahual.github.io/qc-lumbricina/?v=1) | [vFINAL](https://nahual.github.io/qc-lumbricina/)

Validate the core functionality of the game, including:
- Snake movement in response to arrow keys (with reversed controls under one power-up effect)
- Power-up ("pill") spawn behavior and effects
- Collision detection (walls, obstacles, self-collision) triggering Game Over
- Scoring and level progression (every 500 points)
- Highscore system (top 5, sorted, tie-breaking, 30-character name field, default name)
- Debug info panel (length, speed, bonus timer)

## 🔍 Scope

**In scope:** movement & controls, collisions, pill spawning/effects/duration, scoring & levels, highscore logic, debug panel — tested manually on Desktop web (Firefox, Edge, Chrome) on Windows 10/11 and Linux, using a physical keyboard.

**Out of scope:** performance testing, multi-device/mobile, automated testing, accessibility testing, visual/art design.

## 🧪 Methodology

- **Type:** Manual black-box functional testing (functional, negative, exploratory, and regression testing)
- **Evidence:** Screenshots for each test execution
- **Two test cycles:** an initial run (**Build v1**) and a regression run after fixes (**Build vFINAL**), to verify that reported bugs were actually resolved

## 📊 Results

- **40 test cases** written and organized by module (Movement, Collisions, Pills, Highscore, Debug info)
- **13 bugs** logged with severity, priority, reproduction steps, expected vs. actual result
- Of those, **10 bugs were fixed and re-verified** in the regression cycle (Build vFINAL); 3 remained open at the end of the cycle
- Full regression suite re-executed on vFINAL to confirm fixes didn't break existing functionality

See [`bug_report.md`](./bug_report.md) for the full bug list (translated to English).

## 🛠️ Tools Used

- Spreadsheet (Excel/Sheets) for test case design and bug tracking
- Screenshots for evidence
- No automation tools were used — this was a fully manual testing exercise

## 📄 Full Documentation

The complete Test Plan, Test Report and test case spreadsheet (in Spanish, the language of the original course) are available on request — this repo includes the English summary and translated bug report for portfolio purposes.

## 💡 What I Took Away

This project gave me hands-on experience with the full manual QA cycle: turning specs into testable cases, executing them, documenting defects clearly enough for a developer to reproduce them without guesswork, and re-validating fixes through regression testing — not just finding bugs once, but confirming they stay fixed.
