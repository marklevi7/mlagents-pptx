# Project rules — mlagents-pptx

## Versioning rule (MANDATORY)

Every change the user requests bumps an internal **collaboration version number**.

- The current state — the initial import of the deck — is **version 0**.
- The next requested change becomes **version 1**, the one after **version 2**,
  and so on. The number only ever goes up, by one, per requested change.
- Always refer to the work by its current version number in replies
  ("this is version N", "shipping version N+1", etc.).
- Track and increment this number for every change, without being reminded.

> Note: this collaboration version number is separate from the deck's own
> in-content tag (currently `v122` on the cover and in the README). Unless the
> user says otherwise, do not assume bumping the collaboration version also
> changes that visible tag.

## Preview-link rule (MANDATORY)

Before giving the user any preview link, ALWAYS open/fetch that exact link and
verify its contents match the latest change. Only hand over a link after
confirming it serves the current version. Never give an unverified link.

- Use **commit-pinned** links to avoid stale CDN caches:
  `https://rawcdn.githack.com/marklevi7/mlagents-pptx/<FULL_COMMIT_SHA>/index.html`
  (the `<SHA>` is immutable, so each link is freshly cached and never stale).
- Do NOT hand out `raw.githack.com/.../<branch>/index.html` branch links — they
  cache aggressively and serve outdated content.
- Verification step: `curl` the link and grep for text from the newest edit;
  confirm it appears before sending.

## Project

Single-file HTML presentation. `index.html` is the live deck. See `README.md`.
