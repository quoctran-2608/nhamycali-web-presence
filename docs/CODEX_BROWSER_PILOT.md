# Codex Browser Pilot — Current Task

This is the current browser-execution entry point.

## Current live task

**Run only the Substack pilot. Bluesky is completed. Do not run Blogger in the same task.**

Bluesky canonical profile:
- https://bsky.app/profile/nhamycali.bsky.social
- status: completed
- do not recreate or re-run signup

## Required reading

1. `AGENTS.md`
2. `brand/BRAND_ENTITY.yaml`
3. `brand/OFFICIAL_LINKS.yaml`
4. `brand/BRAND_DNA.md`
5. `brand/COPY_LIBRARY.md`
6. `assets/ASSET_MANIFEST.yaml`
7. `assets/PLATFORM_ASSET_POLICY.yaml`
8. `docs/REGISTRATION_POLICY.md`
9. `research/WAVE_1_DECISIONS.yaml`
10. `playbooks/PILOT_SEQUENCE.yaml`
11. `playbooks/SUBSTACK.md`
12. `content/seed/SUBSTACK_WELCOME.md`
13. `state/accounts.csv`
14. `state/manual_actions.md`

## Instruction to Codex

Use this task wording:

> Execute the NHÀ MỸ CALI **Substack pilot only** according to the repository rules and `playbooks/SUBSTACK.md`.
>
> Operate autonomously for routine reversible browser work. Do not ask me before ordinary actions such as Next, Continue, Save, Edit, Upload, Skip, Create, Publish, Post, navigation, reasonable field selection, copy fitting, or public QA when the intended result is already defined by the repo.
>
> If an ordinary UI action does not respond, retry it up to 3 times using normal browser actions, reload, or direct navigation to the official page. If browser tooling still cannot activate the control, ask me for one manual click only, then continue from the resulting page without restarting the workflow.
>
> Perform one reasonable existing-account check. Prior research found no clear NHÀ MỸ CALI Substack property. If a strong likely official account is found, stop for ownership confirmation. If no strong match is found, or logged-out search is unavailable and signup does not reveal an ownership conflict, proceed with signup rather than looping on discovery.
>
> Preferred public architecture:
> - publication/brand: NHÀ MỸ CALI
> - author/person identity, only where Substack exposes a distinct author field: Helen Hà Nguyễn
> - canonical website: https://nhamycali.com/
> - preferred handle: nhamycali
> - publication avatar: assets/avatar/nhamycali-avatar-square.png
> - Helen portrait only for a distinct author/person identity
>
> Adapt non-canonical bio/About/description/title copy autonomously to fit live field limits while preserving canonical facts and brand meaning. You may choose reasonable categories, navigation order, visibility defaults and other non-sensitive settings without asking me.
>
> Use the approved welcome issue from `content/seed/SUBSTACK_WELCOME.md`. Publish only the first approved welcome issue during this pilot; do not bulk-import the website archive.
>
> Do not purchase a custom domain, enable paid subscriptions, connect Stripe, or make any payment.
>
> Stop only for a hard blocker:
> - CAPTCHA/anti-bot requiring human interaction
> - OTP/2FA/email/SMS security code or security challenge you cannot legitimately complete
> - identity/business documents
> - payment/subscription/Stripe/card/bank authorization
> - existing account with uncertain ownership
> - Terms/policy conflict
> - destructive irreversible action
>
> Credential fields: use the approved local secret workflow when the browser environment permits it. If the browser security boundary prevents moving a secret from local runtime into a credential field, ask me to fill only those credential/verification fields directly in the browser, then immediately continue the rest autonomously. Do not expose the secret in chat, logs, repo files, reports, or commit metadata.
>
> After public QA succeeds:
> - update `state/accounts.csv`
> - update `brand/OFFICIAL_LINKS.yaml` only with verified public Substack URL(s)
> - resolve any Substack blocker in `state/manual_actions.md`
> - create/update a Substack platform report
> - scan the diff for secrets
> - run `git diff --check`
> - commit the non-secret changes
> - report the public URLs and commit SHA
> - STOP
>
> Do not start Blogger or any other platform.

## Human checkpoints

Routine UI is not a checkpoint.

Human input is expected only for:
- credential entry if the browser cannot securely transfer local secrets;
- CAPTCHA/anti-bot;
- OTP/2FA/security verification;
- identity/business documents;
- payment/financial authorization;
- ambiguous ownership;
- destructive irreversible actions.

## Expected output

Codex should report:
- whether an existing Substack property was found;
- whether a new profile/publication was created;
- handle and public URLs;
- whether canonical website appears publicly;
- whether brand/avatar/About passed QA;
- whether the welcome issue was published;
- any hard blocker encountered;
- exact state/report files updated;
- commit SHA;
- confirmation that no secret was committed.

## After Substack

Stop for audit.

Blogger is the next candidate only after the Substack result is reviewed.
