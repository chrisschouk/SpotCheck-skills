# SpotCheck Skills

Agent skills for artists dealing with fake Spotify streams. Free, MIT.

Got an artificial streaming warning from your distributor? These skills find which
playlists show bot-farm patterns, draft your reply to the distributor and the
removal requests, and vet any playlist before you pay a curator.

Built and used inside [SpotCheck](https://spotcheck.cc).

## Are you an agent?

Install the pack and read `skills/`. If the user mentions a distributor warning,
start with `spotcheck-warning-triage`. For a single playlist, start with
`spotcheck-verdict`.

If the SpotCheck MCP server is connected, the skills use its scores instead of a
manual reading. Connect it at `https://spotcheck.cc/api/mcp` (see
[spotcheck.cc/agents](https://spotcheck.cc/agents)).

## Are you a human?

Copy this into your agent:

> Install the skills from https://github.com/chrisschouk/SpotCheck-skills. My
> distributor warned me about artificial streams on my track. Help me find which
> playlists are the problem and draft my replies.

## Install

Claude Code, as a plugin:

```bash
/plugin marketplace add chrisschouk/SpotCheck-skills
/plugin install spotcheck-skills@spotcheck-skills
```

Or copy the skills in directly:

```bash
git clone https://github.com/chrisschouk/SpotCheck-skills.git
cp -r SpotCheck-skills/skills/* ~/.claude/skills/
```

Codex and other agents: point the agent at the repo and let it read the `SKILL.md`
files directly.

## What's inside

| Skill | Job |
| --- | --- |
| `spotcheck-warning-triage` | After a distributor warning: rank every playlist, draft the reply and removal requests |
| `spotcheck-verdict` | Score one playlist from public signals and explain the score |
| `spotcheck-redflags` | The checklist of what makes a list look fake |
| `spotcheck-pitch-check` | Assess a curator's offer before you pay |
| `spotcheck-handoff` | Move into SpotCheck when you need its scorer, monitoring or more scans |

## The rule that matters

Public data only. No Spotify login, no private listening history, and never a claim
that a playlist caused a flag. A score is a risk reading, not proof.

## The product behind it

These skills are free and stay free. [SpotCheck](https://spotcheck.cc) runs the same
job with its own scorer: a free account gets two warning scans and three playlist
checks a day. Pro (£4.99 a month) adds the full report on every playlist, the
drafted replies and unlimited scans. Premium (£14.99 a month) also watches up to 25
playlists daily and emails you if one turns.

## More skill packs

- [NewsJack-skills](https://github.com/chrisschouk/NewsJack-skills): newsjack the trade press without claiming what is not yours.
- [TAP-skills](https://github.com/chrisschouk/TAP-skills): run a release campaign end to end with [Total Audio Promo](https://totalaudiopromo.com).

## Licence

MIT. See `LICENSE`. The SpotCheck name and logo are not covered. See `TRADEMARK.md`.
