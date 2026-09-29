# Working with agents

Starter prompts for habits that make AI help more reliable. Copy one into your AI assistant and fill in the brackets.

Last updated September 2026.

## Get a second opinion on a change

From [Ad Astra](https://robburke.net/side-quests/ad-astra/).

```text
You are reviewing a change that [another AI assistant or a colleague] made to [project]. Look at the actual files that changed, not a summary, and rerun the checks yourself. Tell me what is correct, what is worth keeping, and specific improvements. For each test you rely on, say what it actually proves, and where you can, break the fix on purpose to confirm the test fails.
```

**A good result:** a review that quotes the real changes and reports what it reran, not one that agrees with the summary it was given.

## Leave notes for next time

From [Withings to Garmin Instant Sync](https://robburke.net/side-quests/withings-to-garmin-instant-sync/).

```text
Before we finish, write a short lessons-learned file for this project: the dead ends we hit, the approaches and versions to avoid, and why. Write it as instructions to yourself for next time. I'll save it as CLAUDE.md or AGENTS.md in the project folder, or paste it at the start of our next conversation.
```

**A good result:** the next session skips the dead ends instead of rediscovering them.

## Drill the gaps before an exam

From [Anthropic Architect Cert](https://robburke.net/side-quests/anthropic-architect-cert/).

```text
Here are my practice exam results for [exam name], pasted exactly as the exam showed them. Identify my weakest areas, then run two short review sessions on them, with about a third of the questions on topics I already know so I can't coast. At the end, write a one-page cheat sheet of what I still need to memorize, sized to print.
```

**A good result:** review sessions aimed at what you got wrong, and a cheat sheet short enough to print.
