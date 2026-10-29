---
name: import
description: Get material into Soma so she knows and remembers it — meeting notes and transcripts, documents (PDF, Word, slides, Markdown, text), a folder or archive of files, survey or spreadsheet data, pages from Notion, Google Drive, Slack or other connected tools, or something produced in this Claude session. Use whenever the user says "put this in Soma", "import to Soma", "give this to Soma", "Soma should know about this", or shares material that is obviously useful organisational context. Offer it whenever a Claude project yields a document, analysis or decision worth keeping in Soma.
---

Soma remembers what she is given, and everything else she does gets better with good context. Importing is how a Claude session leaves something behind. You do the reading, cleaning, analysis and structuring — the work that needs a PDF opened, a spreadsheet analysed or a Notion export tidied — and hand Soma documents that are ready to keep. She files them herself and tells you where they went.

Tools: `whoami` once per session, then `ask_soma` for the hand-over, as one conversation.

If you spot the fit yourself — the user has shared or produced something Soma would plainly benefit from and the tools are present — offer it in one line ("Want me to give this to Soma?"). If they say yes, treat everything the conversation already holds as answered.

## 1. Understand before importing

Read the conversation first. Ask only what is still missing, in one message, one to five questions, fewest first. Never ask a question the conversation answers. If a tool for asking the user structured questions is available, use it.

Question bank:

1. **What it is and where it comes from** — skip when obvious from the file or the conversation.
2. **What Soma should use it for** — background on the organisation, a record of a decision, data to inform a session, the user's own reflection. This decides how documents are shaped and titled, and it is the first thing you tell Soma.
3. **Scope** — all of it or parts; anything to leave out (names, numbers, a section).
4. **Verbatim or summarised** — default is a faithful summary with decisions, facts and chosen quotes kept exactly; verbatim only when asked or when the source is short and clean.
5. **Where it should live** — a team, a project, just the user. If they have no preference, let Soma decide and report where she put it.

A single pasted note needs at most one question; an archive needs most of them.

## 2. Inventory and read

- **One item** (a note, a transcript, a document): read it in full.
- **A folder or archive**: list it, group by type and topic, read each file, drop duplicates, empty files and obvious junk, and say what you skipped.
- **Spreadsheet or survey data**: analyse it with code first — shape, segments, trends, the splits worth knowing. What goes to Soma is the narrative summary and a few key tables, never raw rows.
- **Connected tools** (Notion, Drive, Slack, others): fetch with the connector, then treat as above.
- **This session**: use the substance of what was produced here — the memo, the analysis, the decision.

Read files that are not already in context with the environment's file-reading approach. Say what you are doing when a batch is large; the user should never wonder whether you are still working.

## 3. Screen

Before anything is structured, flag what should not travel into a shared memory by default: named individuals' performance, pay, health or HR matters; customer names; raw interview transcripts; credentials and keys; personal data about third parties. For each, propose remove, generalise, or keep, and let the user decide. Default to removing what the user did not ask to keep.

## 4. Structure each document

One document per meeting, per report, per topic. A long handbook becomes a handful of documents by chapter; a dozen one-line notes become one document. Aim for documents Soma can read whole and cite, and keep each under about 2,000 words — split a longer one into parts rather than send one long message.

Use this shape, adapted to the material:

```
# [Title — what it is, in the organisation's own words]
[Date] · [Source: file, meeting, tool]

**Summary** — three to six lines.

[Body — the substance: decisions, facts, themes, numbers, kept quotes.]

**Open questions / why this matters** — one to three lines, only if the user said.
```

Keep the user's phrasing where it carries meaning. Do not add interpretation the source does not contain; Soma will do her own reading.

## 5. Receipt, then hand over to Soma

Show a manifest before anything goes to Soma: each document's title, one line on its content, rough size, and what was removed or generalised. Ask "Give these to Soma?" Nothing is sent before a yes.

Then open one `ask_soma` conversation for the import and keep its `conversation_id` throughout.

- **First message**: what this material is, where it comes from, why the user wants her to have it (from the interview), how many documents are coming, and where the user wants them if they said. Ask her to keep each one as a document, as given, and to confirm each — and to say if she merges, renames or changes anything.
- **Then one document per message.** Wait for her reply before sending the next. Treat it as a conversation, not an upload: if she asks something you can answer from what the user told you (a title, where it belongs), answer on the same conversation; if only the user can answer, come back to them. If she has a better place or name for something, let her.
- For parts of a split document, label them ("part 2 of 3") so she can join them.
- For more than about ten documents, give the user a one-line update every few.
- If she cannot keep something — no credits, or she declines — stop, report what she has and what she has not, and keep the prepared documents so the hand-over can resume.

## 6. Report

Tell the user what Soma now has, in her words where she named or placed things, what she changed, and what was skipped and why. Mention the app link only if the user asks where to continue; then give the `app_url` the tool returned.

## Data rules

- Never give Soma anything the user has not seen in the manifest.
- Interview or survey material from outside Soma is summarised and de-identified unless the user explicitly chooses otherwise. Soma's own session interviews are not re-imported; they have their own gate in the app.
- Do not send names of colleagues or customers unless the user wrote them or chose to keep them in the screen step.
- If a Soma tool is missing or returns an authentication error, ask the user to connect Soma again (the plugin's Connectors tab in claude.ai, `/mcp` in Claude Code). If it reports no credits, say so and point to Billing in the app. The first call after a quiet period can take up to a minute; do not retry in a loop.
