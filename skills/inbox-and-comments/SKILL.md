---
name: inbox-and-comments
description: Triage the Meta Business Suite inbox (Messenger and Instagram Direct messages, comments) and prepare draft replies. Use when the user says "check the inbox", "any messages", "reply to the comments", "unread messages", "who wrote to the page".
---

# Inbox and comments

First apply the rules of the `meta-business-suite` skill. Claude prepares, the user approves: no reply is sent without confirmation.

## Procedure

1. Open the Inbox and read the unread messages, then the recent comments on posts.
2. Classify each item: information request (prices, hours, availability, dates), collaborations/sponsors, reports or complaints, positive comments, spam/abuse.
3. Present a short summary: sender (visible name), gist, category, urgency and a proposed draft reply.
4. Write the drafts in the language of the message, with a friendly and direct tone. For practical information, point to the brand's website only if the information is there; do not invent dates, prices or rules: if you do not know them, say so and ask the user.
5. After approval, send the replies one at a time and check each was sent.

## Limits

- Do not hide or delete comments or block users without an explicit request; for serious abuse or threats, tell the user and leave the decision to them.
- Do not answer questions about safety, incidents, unofficial news or legal matters: prepare a cautious draft and hand it over.
- Do not repeat unnecessary personal data (phone numbers, addresses) in the chat.
