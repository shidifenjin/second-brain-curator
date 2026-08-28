# Card Schema

## Raw capture

Store the full source unchanged. Recommended frontmatter:

```yaml
capture_id: CAP-20260101-001
captured_at: 2026-01-01T09:00:00Z
source_type: reading_export
source_message_id: optional-stable-id
source_url: optional-canonical-url
content_hash: sha256:optional
status: captured
needs_split: false
```

Recommended body sections:

```markdown
## Original content

Complete source text.

## User annotations

Only text confidently identified as the user's own annotation.
```

If authorship is unclear, preserve the content in its original order and set `needs_split: true`.

## Candidate card

```yaml
card_id: C-0001
status: draft
created: 2026-01-01
source_records:
  - CAP-20260101-001
review_stage: new
privacy: normal
```

Required sections:

```markdown
# One independently understandable claim

## My view

The user's current view, without inventing certainty.

## Source index

Links or precise pointers to supporting raw records.

## AI interpretation

A concise interpretation, clearly labeled as AI-generated.

## Question for review

One question that could clarify, challenge, or extend the idea.

## Possible connections

- proposed · extends · [[Another card]] — one-sentence rationale

## Conversation log

Append meaningful decisions and new thoughts.

## Review decision

- [ ] Approve
- [ ] Revise
- [ ] Continue discussion
- [ ] Find connections
- [ ] Stop here
- [ ] Discard
```

The title should be a claim, not a broad topic label. A card must remain understandable when read outside its original conversation.
