---
name: brief
description: Send Soma an update on the user's behalf so Soma remembers it. Use when the user says "tell Soma", "brief Soma", "let Soma know", or wants Soma to have context on what they shipped, decided, or are struggling with.
---

A brief is a short, dated note Soma reads now and remembers later. It appears as a conversation in the app, where the user can read Soma's reply or continue.

1. Call `whoami` once per session if you have not.
2. Draft the update in two to five sentences, first person as the user: what happened, why it matters, what is open. Write it from what the user told you or what you did together in this session. Leave out file paths, code and anything that reads as confidential (customer names, salaries, health, HR matters) unless the user asked for it.
3. Show the draft and ask "Send this to Soma?" unless the user already dictated the exact text.
4. Call `brief_soma` once with the agreed text. Soma knows the message comes from you on the user's behalf. Report Soma's short reply in a sentence; mention the app link only if the user asks.

Never call `brief_soma` more than once per update, and never on your own initiative.
