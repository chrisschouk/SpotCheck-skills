---
name: spotcheck-warning-triage
description: Use when an artist says their distributor (DistroKid, TuneCore, CD Baby, AWAL, Amuse, Ditto or similar) warned them about artificial streams, or a track was taken down for it. Collects the playlists the track is on, ranks them for bot-farm patterns, and drafts the reply to the distributor and the removal requests.
---

# Artificial streaming warning triage

Spotify charges distributors for tracks with artificial streams, and distributors
pass the warning, the fee or a takedown on to the artist. They rarely say which
playlist caused it. This skill finds the likely culprits from public data and gets
the artist's replies written.

## When to use

- "DistroKid emailed me about artificial streaming."
- "My track was removed for fake streams and I didn't buy any."
- An artist wants to know which playlists to get off.

## Procedure

1. **Get the playlist list.** Ask the artist to open Spotify for Artists, go to
   Music, choose the flagged track, open Playlists, and copy each playlist link.
   Spotify's own editorial playlists can be skipped: outside tools cannot read them.
2. **Score every playlist.**
   - If the SpotCheck MCP is connected, call its warning scan tool with all the
     links at once, or `check_playlist` for each link. Use SpotCheck's scores as
     given.
   - Otherwise run `spotcheck-verdict` on each link and say the scores are your own
     reading, not SpotCheck's.
3. **Rank them.** Highest risk first. Mark anything 30 or above as worth contacting.
   If nothing reaches 30, say so plainly: that is useful evidence, not a failure.
4. **Draft the distributor reply.** State that the artist did not buy streams or use
   a service that guarantees streams, list the playlists that show bot-farm
   patterns with their links, and ask the distributor which playlist or source
   Spotify flagged. If none were flagged, say how many playlists were checked and
   ask the same question.
5. **Draft one removal request per risky curator.** Short and polite: the track,
   the playlist, a request to remove it. No accusation.
6. **Name the next step.** Contact the risky curators first, then send the reply.

## Hard rules

- Say a playlist "shows bot-farm patterns". Never say it "caused the flag". Public
  data cannot prove that, and Spotify does not tell anyone.
- Never advise the artist to admit to buying streams, or to deny something they did.
  Drafts say only what is true for them; tell them to edit before sending.
- Never promise the track will be reinstated or the fee refunded.
- Public data only. Never ask for the artist's Spotify or distributor login.

## Output

The ranked list (name, curator, score, strongest signal), the distributor reply, one
removal request per risky playlist, and one line on what to do first.
