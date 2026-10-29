---
name: deck
description: Create a slide deck with Soma's knowledge of the user's organisation woven in. Use when the user wants slides, a deck, a presentation or a talk that touches people, teams, culture, leadership, change, facilitation or the organisation's own story — for a leadership team, board, all-hands, workshop, offsite, client or conference — on a topic Soma knows, on a work project, on something they have learned, or on results from Soma. Use it even when the user does not mention Soma, as long as the deck is about the organisation and its people; a deck on anything else is not this skill.
---

Soma knows the organisation, its history and the user's own journey; you know how to build a deck. Soma supplies substance and context, you shape and produce. The deck is built here, in Claude. Soma is the collaborator, not the author.

If you spot the fit yourself — the user is already working on a presentation and the Soma tools are present — offer it in one line ("Want me to bring Soma in on this?"). If they say yes, treat everything the conversation already holds as answered.

## 1. Understand the task before anything else

Read the conversation first. Often the user has already said what the deck is for, who it is for and what it should draw on. Ask only what is still missing, in one message, one to five questions, fewest first. Never ask a question the conversation answers. If a tool for asking the user structured questions is available, use it.

Question bank:

1. **Purpose** — what should the audience think, decide or do afterwards?
2. **Audience and setting** — who, and where: board, leadership team, all-hands, workshop, external. This decides tone and what may be shown.
3. **Length** — slide count or minutes. Default to 8–12 slides if they have no preference.
4. **Sources** — their own material (ask them to attach or paste it), Soma's knowledge, or both; and anything that must stay out.
5. **Output** — the environment's slide artifact, PowerPoint, Google Slides; a brand or template to follow.

If the user has dictated all of this, ask nothing: restate the plan in two lines and proceed.

## 2. Gather from Soma in short turns

Call `whoami` once per session if you have not. Then use `ask_soma` as a conversation on one `conversation_id`. Each call is one focused question Soma can answer in a few paragraphs. Do not hand her the whole task in one message: a long prompt is slow and more likely to fail, and you lose the chance to steer on what she actually says.

A typical sequence:

- **Scope** (1 call). Say what the deck is and for whom, then ask: "What do you know about this in our organisation — history, decisions, live tensions, anything from recent sessions that bears on it? Say what you are drawing on."
- **Depth** (1–3 calls). Pick the two or three threads that matter most for this audience and ask for specifics on each. Follow a thread she opens if it strengthens the deck; drop it if it does not.
- **Check** (0–1 call). Once you have an outline, send her the slide titles — titles only, never the full deck — and ask what is missing, wrong, or would land badly with this audience.

Stop when the next question is one only the user can answer, or when another call would not change a slide. Two to five exchanges is normal.

Adapt to the scenario:

- **A topic Soma knows** (leadership, culture, change): she carries the substance. Ask for the organisation's own examples so the deck is not generic.
- **A work project**: the user carries the project. Ask Soma for context — who is affected, what has been tried before, what people are worried about.
- **Something the user learned**: the user's words are the spine. Ask Soma what she remembers of this thread in their journey and what it connects to.
- **Results from Soma** (a report, a session run): ask for themes and her reading, aggregated only. See the data rules below.

## 3. Build the deck

Outline first: one line per slide with the point it makes. Show the outline to the user when the deck is long (more than about ten slides) or the audience is senior or external; otherwise proceed. Then build with whatever slide capability the environment offers (slide artifact, PowerPoint skill, or similar), following the brand or template if one was given.

- One idea per slide; the title states the point.
- Put Soma's nuance in speaker notes rather than crowding the slide.
- Separate fact from reading. Things that happened are facts; Soma's interpretation is a reading, and is attributed ("Soma's read", "from our sessions"). Never present her analysis as settled fact, and never invent figures or quotes.
- When the deck is about the user's project or learning, keep their voice. Soma supports; she does not take over.

Review with the user and iterate here. Go back to Soma only for a specific gap.

## 4. Close the loop

When the user is happy, offer to brief Soma so she remembers what was made and why: what the deck is, for whom, the main claims, what is still open. Follow the `brief` skill — draft, ask, send once. If the deck carries a decision or a framing the organisation should keep, offer to store the outline and notes with the `import` skill.

## Data rules

- Material from sessions or reports: aggregated themes and approved summaries only. No raw transcripts, nothing attributable to an individual, no working around a threshold Soma applies. If she declines to share something, the deck does without it.
- Do not send names of colleagues or customers to Soma unless the user wrote them.
- Board and external audiences are confidential by default: ask before including anything the user has not already decided to share.
- If a Soma tool is missing or returns an authentication error, ask the user to connect Soma again (the plugin's Connectors tab in claude.ai, `/mcp` in Claude Code). If it reports no credits, say so, point to Billing in the app, and finish the deck from the user's own material. The first call after a quiet period can take up to a minute; do not retry in a loop.
