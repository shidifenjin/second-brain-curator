# Review Sessions

## Daily five-card queue

Select up to five cards using this order:

1. cards whose `next_review` is due;
2. cards not shown during the previous seven days;
3. candidates containing a personal view but an unresolved question or proposed link;
4. a useful mix of two recent candidates, two older permanent cards, and one card that may connect them, when available.

Exclude discarded, closed, channel-inappropriate, or explicitly suppressed cards. Do not add weak cards merely to reach five.

Send a compact menu containing the number, card ID, claim/title, and one short review cue. Offer: choose 1–5, start sequentially, another set, or skip today. Store delivery and outcomes in a separate review-state file instead of modifying source material.

## On-demand routing

- No target: use today's queue or build one immediately.
- Card ID: exact-match across permanent and candidate cards.
- Book title: search source records, import reports, provenance fields, and body text; then include explicitly linked cards.
- Topic: compare claims and contexts semantically rather than relying only on filenames or tags.

If no card exists, say so and offer to create candidates from the relevant raw sources. Do not invent matches.

## One-card dialogue

Show the claim, the user's existing view, and source pointers. Ask one question that tests understanding, boundaries, counterexamples, connections, or action. After the reply, offer to continue, update, branch into a candidate, find links, move to the next card, stop, or discard.

Suggested external review state fields: `last_reviewed_at`, `last_outcome`, `next_review_at`, and `times_reviewed`.
