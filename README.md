# Meta Business Suite for Claude

A Claude plugin that manages **Facebook and Instagram from Meta Business Suite** by working in the browser, with your existing login. It uses no API and no tokens, and it never asks for your password.

> This plugin is independent and is not affiliated with, endorsed by or sponsored by Meta. Meta, Facebook, Instagram and Meta Business Suite are trademarks of their respective owners.

## Included skills

| Skill | What it does |
|---|---|
| `meta-business-suite` | Operating rules, navigation map, brand guidelines |
| `schedule-post` | Writes captions and schedules posts, reels and stories on Facebook and Instagram |
| `inbox-and-comments` | Triages messages and comments and prepares draft replies |
| `insights-report` | Reports on reach, interactions and best-performing content |

## Safety

Claude does not publish, schedule, reply or delete anything without your explicit approval of the preview. If Meta asks for verification (captcha, identity check), Claude stops and tells you.

## Installation

Full step-by-step guide: **[TUTORIAL.md](TUTORIAL.md)**.

In Claude Code:

```
/plugin install meta-business-suite --marketplace Clayblock94/meta-business-suite-claude-plugin
```

Alternatively, install the `.plugin` file. Then:

1. Fill in `skills/meta-business-suite/references/brand-guidelines.md` with the tone, profiles and rules of your brand.
2. Sign in to business.facebook.com in the browser Claude uses (built-in or Claude in Chrome).
3. Ask, for example: "schedule a post on Facebook and Instagram for Friday at 6 pm".

## Limitations

- This is not an official Meta integration: if Meta changes the Business Suite interface, some procedures may need updating.
- Slower than an API, but it can schedule on Instagram too and handle private messages.
- Works on accounts with management permissions on the page and on the linked Instagram professional profile.

## License

GNU General Public License v3.0 (GPL-3.0-only). See [LICENSE](LICENSE).
