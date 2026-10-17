---
name: your-skill-name
description: One line. What this skill does and when it runs.
---

# your-skill-name

Every bot skill that works has the same shape: READ, CHECK, APPLY RULE, DRAFT, then a human says yes.
Fill in the brackets, delete these two lines, send it to your Grok Bot.

## 01 READ
What data the bot pulls before it does anything.
- [source 1, e.g. price]
- [source 2, e.g. order book]
- [source 3, e.g. news calendar]

## 02 CHECK
Is the data good enough to act on? If any check fails, stop and log `CHECK BLOCKED · <reason>`.
- Data is fresh: [max age, e.g. under 30 seconds]
- Nothing missing: [required fields]

## 03 APPLY RULE
The hard rule. Written so a stranger could check it. If it fails, stop and log `RULE BLOCKED · <reason>`.
- [rule 1, e.g. risk exactly 1% of balance]
- [rule 2, e.g. reward at least 2x risk]
- Never bend a number to make the rule pass.

## 04 DRAFT
What the bot prepares. It does not send anything.
- [the draft, e.g. order: pair, side, entry, stop, target, size]
- One line on why it passed.

## YOU
The bot waits for a human yes or no. No answer means no.
Log every yes, every no, every block.
