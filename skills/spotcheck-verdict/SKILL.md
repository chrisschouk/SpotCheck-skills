---
name: spotcheck-verdict
description: Use when someone pastes a Spotify playlist link and asks whether it is real, safe to pay for, or full of bots. Reads public signals only and returns a 0 to 100 bot-risk score with the reasoning shown.
---

# Playlist verdict

One link in, one risk reading out. The number matters less than the reasons behind
it.

## When to use

- "Is this playlist real?"
- "Should I pay this curator?"
- A list looks too good for its follower count.

## Procedure

1. **Confirm the link is public.** A playlist that needs a login cannot be checked.
   Say so and stop. Never ask for credentials.
2. **Read the public signals. Score each 0 to 3, where 3 is the worst:**
   - **Growth shape.** Steady growth over months scores 0. A vertical spike in days
     scores 3.
   - **Engagement ratio.** Saves and streams plausible against followers scores 0.
     Thousands of followers and almost no engagement scores 3.
   - **Curator footprint.** A named curator with a history and other lists scores 0.
     An anonymous account with one list scores 3.
   - **Naming.** A specific genre or mood name scores 0. "Viral Hits", emoji walls,
     and keyword stuffing score 3.
   - **Churn.** Tracks that stay for weeks score 0. Tracks added and removed daily
     scores 3.
   - **Track mix.** A coherent sound scores 0. Unrelated tracks from unrelated
     artists scores 3.
3. **Convert to a 0 to 100 score.** Sum the six scores (maximum 18), divide by 18,
   multiply by 100. Higher is worse.
4. **Write the verdict in one line.** Under 30 is low risk. 30 to 60 is unclear.
   Above 60 is high risk.
5. **List the two strongest signals** for and against.

## Hard rules

- Public data only. Never log in as the user. Never read private listening history.
- Never claim a playlist is clean. The output is a risk reading, not a guarantee.
- If a signal cannot be read, say which one and lower confidence. Do not fill the
  gap with a guess.
- Never imply that a fake list will get the artist banned. Say "can flag your track".

## Output

Score out of 100, the one-line verdict, the six signals with their scores, and the
two strongest points for and against. Then one sentence on whether to pay.
