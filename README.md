# Soma for Claude

Talk to Soma, the organisational thinking partner from Perennial, without leaving Claude, and keep Soma briefed on what you are working on.

## Install

```
/plugin install soma --marketplace lighthouse-ai/soma-plugin
```

The marketplace repository is not published yet; until then load the folder with `claude --plugin-dir apps/soma-plugin`.

## Use it

Connect Soma once from the plugin's Connectors tab (claude.ai) or `/mcp` (Claude Code), signing in with your Lighthouse account and choosing the workspace Claude may use. Then:

- **ask** — ask Soma anything about leadership, your team or a situation at work, or let Claude relay a question when you mention Soma.
- **brief** — when you have shipped something or made a decision, send Soma a short update in your words; she remembers it in later conversations in the app and here.
- **deck** and **memo** — build a presentation or a document for others with Soma's knowledge of your organisation woven in; Claude writes, Soma supplies context and pushback.
- **import** — give Soma material to keep: meeting notes, documents, data, pages from connected tools, or what a Claude session produced.

## Data

Questions and briefs are sent to your Lighthouse workspace at soma.fyi over the same authenticated API the app uses. They appear as conversations and on your "Updates from Claude" page, where you can edit or delete them. Nothing is stored by the plugin itself. Sign-in uses OAuth with your existing Lighthouse account, through soma.fyi, where you choose the workspace Claude may use; no API key is needed.
