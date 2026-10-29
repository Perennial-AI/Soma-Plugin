---
name: memo
description: Write a memo, board brief, one-pager, decision document, proposal, culture update or recommendation with Soma's knowledge of the organisation woven in. Use when the user wants a document for someone else to read — leadership, a board, investors, a team, HR, a client — on people, teams, culture, leadership, change or an organisational decision, even when they do not mention Soma; a document on anything else is not this skill. If the user is drafting such a document in chat and Soma would make it stronger, offer to bring her in.
---

Soma knows the organisation and the user's history; you know how to write. Soma supplies context, specifics and pushback, you structure and write. The memo is written here, in Claude. Soma is the collaborator, not the author.

If you spot the fit yourself — the user is drafting something for others and the Soma tools are present — offer it in one line ("Want me to bring Soma in on this?"). If they say yes, treat everything the conversation already holds as answered.

## 1. Understand before writing

Read the conversation first. Ask only what is still missing, in one message, one to five questions, fewest first. Never ask a question the conversation answers. If a tool for asking the user structured questions is available, use it.

Question bank:

1. **Reader and outcome** — who reads it, and what decision or action should follow.
2. **Type and length** — decision memo, board or exec brief, proposal, culture update, reflection; and roughly how long. Default to one page, 400–600 words.
3. **Position** — do they already know what they recommend, or do they want Soma's read first and decide after?
4. **Sources** — their own material (ask them to attach or paste it), Soma's knowledge, or both; and anything that must stay out.
5. **Output** — a doc in the environment, Word, PDF, an email body, a Notion page.

If the user has dictated all of this, ask nothing: restate the plan in two lines and proceed.

## 2. Gather from Soma in short turns

Call `whoami` once per session if you have not. Then use `ask_soma` as a conversation on one `conversation_id`. Each call is one focused question Soma can answer in a few paragraphs. Do not hand her the whole memo in one message: a long prompt is slow and more likely to fail, and you lose the chance to steer on what she actually says.

A typical sequence:

- **Scope** (1 call). Say what the memo is and who reads it, then ask: "What do you know about this in our organisation — history, what has been tried, who is affected, and anything from recent sessions that bears on it? Say what you are drawing on."
- **Specifics** (1–2 calls). Ask for the detail the memo turns on: the decision that set this up, the tension people name, the number or pattern she has seen.
- **Challenge** (1 call, the one that earns its keep). State the recommendation in two sentences and ask what she would push back on, what the reader will object to, and what is missing. Use the answer to strengthen the memo or to change the position — and tell the user when it changed yours.

Stop when the next question is one only the user can answer, or when another call would not change a paragraph. Two to five exchanges is normal.

Adapt to the scenario:

- **Decision memo**: Soma gives history, what was tried and who is affected; the user owns the recommendation.
- **Board or investor brief**: Soma gives what changed and her reading of it, aggregated. The user decides what the board sees.
- **Culture update**: Soma gives the signal from recent sessions; the memo turns it into reading and action.
- **Proposal**: Soma gives why now and where resistance will come from.
- **Reflection or learning**: the user's words are the spine; Soma adds what she remembers of the thread and what it connects to.

## 3. Write

Lead with the point. A reader should be able to act after the first paragraph and read on for the reasoning. Use the structure for the type, adapted as the content demands:

- **Decision memo**: Situation · Options · Recommendation · Risks and mitigations · The ask.
- **Board / exec brief**: Headline · What changed · What it means · What we are doing · What we need from you.
- **Culture update**: Signal · Reading · Actions · What to watch next.
- **Proposal**: Problem · Proposal · Why now · Cost and risk · Next step.
- **Reflection**: What happened · What I learned · What changes.

- Separate fact from reading. Things that happened are facts; Soma's interpretation is a reading and is attributed ("Soma's read", "from our sessions"). Never present her analysis as settled fact, and never invent figures or quotes.
- When it is the user's memo, write in their first person and keep their voice. Soma supports; she does not take over.
- Do not bury the ask. If the memo wants something from the reader, say it plainly and early.

Produce it in whatever document capability the environment offers, in the format the user chose. Review with the user and iterate here; go back to Soma only for a specific gap.

## 4. Close the loop

When the user is happy, offer to brief Soma so she remembers the position taken and what is still open. Follow the `brief` skill — draft, ask, send once. A memo is usually worth keeping whole: offer to store the finished text with the `import` skill as well.

## Data rules

- Material from sessions or reports: aggregated themes and approved summaries only. No raw transcripts, nothing attributable to an individual, no working around a threshold Soma applies. If she declines to share something, the memo does without it.
- Do not send names of colleagues or customers to Soma unless the user wrote them.
- Board, investor and external readers are confidential by default: ask before including anything the user has not already decided to share.
- If a Soma tool is missing or returns an authentication error, ask the user to connect Soma again (the plugin's Connectors tab in claude.ai, `/mcp` in Claude Code). If it reports no credits, say so, point to Billing in the app, and finish the memo from the user's own material. The first call after a quiet period can take up to a minute; do not retry in a loop.
