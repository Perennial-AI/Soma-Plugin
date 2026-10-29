---
name: ask
description: Ask Soma, the user's organisational thinking partner, about leadership, team dynamics, culture, facilitation or a situation at work. Use when the user says "ask Soma", mentions Soma, or wants a second opinion on a people or leadership question.
---

Soma knows the user's organisation and history; you do not. Hand the question to Soma rather than answering it yourself.

1. If you have not called `whoami` this session, call it once. It tells you who is signed in and which workspace this connection uses; there is nothing to choose.
2. Call `ask_soma` with the user's question in their own words, adding only the context Soma needs (what the user is working on, who is involved in role terms). Pass `conversation_id` from an earlier reply to continue the same conversation.
3. Treat it as a conversation, not a lookup. If Soma asks a clarifying question you can answer from what the user already told you, answer her with another `ask_soma` call on the same `conversation_id` before you come back to the user. If her reply opens a thread worth one more step (a suggestion to sharpen, a trade-off to weigh), take it. Two to four exchanges in one go is normal; stop when the next question is one only the user can answer.
4. Convey Soma's answer in your own words, attributed to Soma, and quote her only for a specific phrase that is worth keeping exactly. Do not pass it off as your own advice. Do not append the app link unless the user asks where to continue; if they do, give the `app_url` the tool returned.
5. If the tool reports no credits, say so and point the user to Billing in the app. Do not retry.

Do not send names of the user's colleagues or customers unless the user wrote them in the request.
