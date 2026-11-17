---
name: meta-business-suite
description: Operating rules for working in Meta Business Suite (business.facebook.com) through the browser. Use when the user mentions "Meta Business Suite", "Business Suite", "Facebook page", "Instagram business profile", or asks to manage, check or publish on their Meta social profiles.
---

# Meta Business Suite - operating rules

## Using the browser

Meta Business Suite has no official connector: work through the browser (prefer the built-in browser, otherwise Claude in Chrome) at https://business.facebook.com/latest/home. Never ask for or type credentials: if a login is needed, open the page and ask the user to sign in themselves.

## Before starting

1. Read `references/brand-guidelines.md` for tone, language and caption rules.
2. Load the browser tools (tabs_context, navigate, read_page/get_page_text, computer, find, form_input) in a single search.
3. Open Business Suite and check that the selected asset (menu at the top left) is the right one: the one named in `brand-guidelines.md`. If there are several assets, confirm which one to use.

## Navigation map

- Home: overview, recent activity, suggestions
- Inbox: Messenger/Instagram Direct messages, comments, story replies
- Planner / Calendar: scheduled posts and stories
- Create post / Create story / Create reel: single composer for Facebook and Instagram
- Insights (Results): reach, views, interactions, followers, content
- Content: all published posts, scheduled posts, drafts
- Settings: roles, publishing tools, linked accounts

Labels may change, and may appear in another language depending on the user's account: if you cannot find an item, use `find` or read the page instead of guessing coordinates.

## Non-negotiable rules

- Do not publish, schedule, send messages, reply to comments, delete or hide anything without the user's explicit approval of the final text, media, destinations and time.
- Always show the preview first (full text + platforms + date/time) and wait for the go-ahead.
- Do not bypass errors, blocks or verification requests from Meta (captcha, identity check, publishing limits): stop and report.
- Never write third parties' sensitive data in reports; do not invent metrics: report only the numbers read on screen, with period and source.
- If an action is irreversible (deleting, blocking a user), ask for confirmation even if the user mentioned it in general terms.

## Final check

After every action, confirm on the page (success message, entry in the Planner, inbox counter) and tell the user what actually shows as done.

## Other skills in the plugin

- `schedule-post`: create and schedule posts/reels/stories
- `inbox-and-comments`: triage messages and comments and prepare draft replies
- `insights-report`: reports on results and trends
