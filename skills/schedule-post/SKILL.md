---
name: schedule-post
description: Create and schedule posts, reels and stories on Facebook and Instagram from Meta Business Suite. Use when the user says "schedule a post", "post on Facebook and Instagram", "put it on the calendar", "write and schedule the caption", "draft a post".
---

# Scheduling a post in Meta Business Suite

First apply the rules of the `meta-business-suite` skill (mandatory preview, nothing published without approval).

## Procedure

1. Collect: topic/event, media (files or links), platforms (Facebook, Instagram or both), date and time, optional link.
2. If media is missing, ask the user to attach it. If the files are on their computer, use the device tools to prepare them; do not download third-party images from the internet.
3. Write the caption following `references/brand-guidelines.md` (language, tone, hashtags and brand rules). Offer at most two variants.
4. Check the requirements: Instagram feed 4:5 or 1:1, Reels/Stories 9:16; Facebook accepts more formats. Flag media that is not suitable.
5. Show the user the preview: text, media, platforms, date/time (state the time zone). Wait for confirmation.
6. In the browser: Create post → choose the pages/profiles (Facebook, Instagram or both) → upload media → paste text → set "Schedule" with date and time → confirm.
7. Check in the Planner/Calendar that the post appears at the right time and report the result.

## Notes

- For multi-day events, propose a sequence (announcement, countdown, event day, results) and schedule it only after the user approves the whole sequence.
- If Meta reports errors (format, limit, content), do not retry in a loop: report the message and suggest a fix.
- Save as a draft if the user has not yet approved the time/date.
