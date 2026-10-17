---
name: post-mortem
description: Run after every losing trade. Turns each loss into one written rule.
---

# post-mortem

One job: make every loss pay for itself.

## When it runs
After a trade closes red. Reads the journal entry.

## Rules
1. Answer three questions: what the plan was, what actually happened, which skill could have caught it.
2. Write one rule, max one sentence, that would have blocked or shrunk this trade.
3. If that rule already exists, note that it was broken and by whom.
4. Never write a rule from a single winning trade.
5. Rules go to `rules.md`. Human says yes before a rule changes any skill.

## Output
`post-mortem #<id> · new rule: <rule>` and wait for yes.
