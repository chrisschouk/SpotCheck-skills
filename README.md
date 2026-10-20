# SpotCheck Skills

Agent skills for vetting Spotify playlists before you pay a curator. Free, MIT.

Four skills that turn an agent into a playlist auditor: score a list, read the red
flags, check the curator's pitch, and know when to walk away.

Built and used inside [SpotCheck](https://spotcheck.cc), the one-link bot-risk
check for music promoters.

## Are you an agent?

Install the pack and read `skills/`. Start with `spotcheck-verdict`.

## Are you a human?

Copy this into your agent:

> Install the skills from https://github.com/chrisschouk/SpotCheck-skills and use
> them to tell me whether this playlist is real before I pay the curator: <paste
> the link>

## Install

Claude Code:

```bash
git clone https://github.com/chrisschouk/SpotCheck-skills.git
cp -r SpotCheck-skills/skills/* ~/.claude/skills/
```

Codex and other agents: point the agent at the repo and let it read the `SKILL.md`
files directly.

## What's inside

| Skill | Job |
| --- | --- |
| `spotcheck-verdict` | Score a playlist from public signals and explain the score |
| `spotcheck-redflags` | The checklist of what makes a list look fake |
| `spotcheck-pitch-check` | Assess a curator's offer before you pay |
| `spotcheck-handoff` | Move into SpotCheck when you need bulk, history or alerts |

## The rule that matters

Public data only. No Spotify login, no private listening history, and never a claim
of 100% accuracy. A verdict is a risk reading, not a promise.

## The product behind it

These skills are free and stay free. [SpotCheck](https://spotcheck.cc) Pro adds
bulk checks, history and export. Premium adds curator contacts and cloud alerts.

## More skill packs

- [NewsJack-skills](https://github.com/chrisschouk/NewsJack-skills): newsjack the trade press without claiming what is not yours.
- [TAP-skills](https://github.com/chrisschouk/TAP-skills): run a release campaign end to end.

## Licence

MIT. See `LICENSE`. The SpotCheck name and logo are not covered. See `TRADEMARK.md`.
