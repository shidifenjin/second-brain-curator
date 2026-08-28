# Local Configuration Example

Copy this file to `local-config.md` and keep that copy private.

## Storage

- Raw archive: `/path/to/second-brain/raw`
- New captures: `/path/to/second-brain/raw/inbox`
- Source index: `/path/to/second-brain/raw/index`
- Card vault: `/path/to/second-brain/cards`
- Candidate cards: `/path/to/second-brain/cards/review`
- Processing state: `/path/to/private/state.json`

## Input channel

- Type: `folder`, `feishu`, `slack`, `email`, or another supported source
- Conversation or inbox identifier: `<private value>`
- Authorized sender identifiers: `<private values>`
- Reply identity: `<private value>`

## Review preferences

- Review language: English or Chinese
- Questions per turn: 1
- Automatic permanent-card promotion: disabled
- Allowed relationship types: supports, counterexample, extends, applies, alternative

## Safety

Keep this file, credentials, account identifiers, and processing cursors outside version control.
