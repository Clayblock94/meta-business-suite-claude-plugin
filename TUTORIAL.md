# Tutorial: setting up the Meta Business Suite plugin

This guide takes you from installation to your first scheduled post. Estimated time: about 15 minutes. You do not need tokens, a developer app or any API: Claude works in the browser, using your existing Meta Business Suite login.

> The plugin is not an official Meta integration. If Meta changes the Business Suite interface, some procedures may need an update.

## 1. What you need

- A Claude account that can install plugins.
- Access to **Meta Business Suite** (business.facebook.com) with management permissions on the **Facebook page**.
- An **Instagram professional** profile (business or creator) **linked to the page**. Without the link, Instagram does not appear among a post's destinations.
- A browser Claude can use: the **built-in browser** of the Claude desktop app, or the **Claude in Chrome** extension.

To check that the page and the Instagram profile are linked, open **Settings** in Business Suite and look for the linked accounts section. Menu names may change.

## 2. Install the plugin

Choose one route.

**A. Claude app (`.plugin` file)**
1. Build the file from the repository (from the plugin folder):
   `zip -r meta-business-suite.plugin . -x ".git/*"`
   Or use a ready-made `.plugin` file if you were given one.
2. Send the file to Claude in a chat: a preview appears with a button to accept and install the plugin.

**B. Claude Code (from this repository)**
```
/plugin install meta-business-suite --marketplace Clayblock94/meta-business-suite-claude-plugin
```
This needs a recent version of Claude Code. If the command is not available, update Claude Code, or first add the marketplace with `/plugin marketplace add Clayblock94/meta-business-suite-claude-plugin` and then install `meta-business-suite`.

After installing you should see four skills: `meta-business-suite`, `schedule-post`, `inbox-and-comments`, `insights-report`.

## 3. Prepare the browser

1. Open the browser Claude will use (built-in or Claude in Chrome).
2. Go to https://business.facebook.com/latest/home and **sign in yourself**, with your own credentials. Claude never asks for or types your password.
3. Check at the top left that the right page is selected. If you manage several pages, keep the right one selected or tell Claude in your first message.
4. Stay signed in: if the session expires, Claude stops and asks you to sign in again.

If Meta shows a captcha or asks you to confirm your identity, complete it yourself: Claude does not bypass them.

## 4. Fill in the brand guidelines

The file `skills/meta-business-suite/references/brand-guidelines.md` tells Claude how to write for your profile. Edit it **before** building the `.plugin` file (step 2A) or, once the plugin is installed, ask Claude to customize it for you.

Filled-in example (fictional):

```markdown
- Language: English.
- Managed profiles: Facebook page "Rossi Bakery" and Instagram @rossibakery.
- What the brand is about: artisan bakery in Florence.
- Tone: warm and direct, at most two emoji per post.
- Hashtags: 3-5 relevant ones, never generic.
- Never write: unconfirmed prices, promises about delivery times.
- Rules on names and results: always name participants in full.
- Periods when you cannot publish live: Dec 24-26 (schedule ahead).
```

The more concrete the rules, the fewer corrections you will make to captions.

## 5. First test (read-only)

Before scheduling anything, check that everything is connected. Write to Claude:

> Open Meta Business Suite and tell me which Facebook page and which Instagram profile are selected. Do not change anything.

If Claude answers with the right names, the plugin works. Then try reading the inbox:

> Check the inbox and summarize the unread messages. Do not reply to anyone.

## 6. Use the skills

Every action that changes something (scheduling, publishing, replying, deleting) goes through a **preview** first: Claude proceeds only after your explicit go-ahead.

**Schedule a post** (`schedule-post`)
> Schedule a post on Facebook and Instagram for Friday at 6:00 pm. Topic: new opening hours. I'm attaching the photo. Give me two caption options.

Claude shows text, media, platforms and date/time. Reply "ok" to schedule it, or ask for changes. When done, check in the Planner/Calendar that the post appears at the right time.

**Handle inbox and comments** (`inbox-and-comments`)
> Check the comments on the latest posts and prepare replies. Let me approve them one by one.

**Get a report** (`insights-report`)
> Give me an Insights report for the last 28 days, Facebook and Instagram separately, with the top three content items.

Claude reports only the numbers it sees on screen, stating the period. It does not estimate or invent metrics.

## 7. What Claude does not do

- It does not publish, schedule, reply, hide or delete anything without your approval of the final preview.
- It does not ask for or store passwords.
- It does not bypass captchas, identity checks or Meta's publishing limits.
- It does not download third-party images from the internet for your posts: you provide the media.

## 8. Common problems

| Problem | What to do |
|---|---|
| Claude says a login is needed | Sign in yourself at business.facebook.com in the browser Claude uses, then try again. |
| The wrong page is selected | Change the asset from the menu at the top left of Business Suite, or give Claude the right name. |
| Instagram is missing from the destinations | Check that the profile is professional and linked to the page (see step 1). |
| A media file is rejected | Instagram feed: 4:5 or 1:1. Reels and Stories: 9:16. Claude flags unsuitable formats before uploading. |
| The scheduled time is wrong | State the time zone in your message and check the preview before confirming. |
| Claude cannot find a button | Meta may have changed the interface: Claude reads the page and looks for the item by name. If it keeps failing, describe what you see on screen. |
| Meta shows a publishing error | Claude stops and reports the message, without retrying in a loop. |

## 9. Update or remove

- **Update:** download the new version of the repository and reinstall the plugin using the same method as in step 2.
- **Remove:** uninstall the plugin from Claude's plugin settings (in Claude Code: `/plugin uninstall meta-business-suite`).
