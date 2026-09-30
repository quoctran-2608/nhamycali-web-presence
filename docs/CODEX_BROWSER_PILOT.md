# Codex Browser Pilot — Current Task

This is the current browser-execution entry point.

## Current live task

**Run only the Blogger pilot. Bluesky and Substack are completed.**

Completed canonical properties:
- Bluesky: https://bsky.app/profile/nhamycali.bsky.social
- Substack publication: https://nhamycali.substack.com/
- Substack author profile: https://substack.com/@helenhanguyen

Do not recreate or re-run signup for completed platforms.

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
11. `playbooks/BLOGGER.md`
12. `content/seed/BLOGGER_FIRST_POST.md`
13. `state/accounts.csv`
14. `state/manual_actions.md`

## Instruction to Codex

Use this task wording:

> Execute the NHÀ MỸ CALI **Blogger pilot only** according to the repository rules and `playbooks/BLOGGER.md`.
>
> Operate autonomously for routine reversible browser work. Do not ask me before ordinary Blogger actions such as New blog, Next, Save, Publish, Pages, Layout, Theme, navigation, reasonable non-sensitive field selection, copy fitting, approved asset upload, or public QA when the intended outcome is defined by the repo.
>
> If an ordinary UI action does not respond, retry it up to 3 times using normal browser controls, reload, or direct navigation to the official Blogger page. If browser tooling still cannot activate the control, ask me for one manual click only and then continue from the resulting page without restarting.
>
> Use the authorized Google Account already available in the browser/session. Inspect the Blogger dashboard for an existing NHÀ MỸ CALI blog. If a strong likely official blog already exists, stop for ownership confirmation. If the dashboard shows no matching blog and creation proceeds normally, do not loop on public-search absence; proceed with the pilot.
>
> Preferred Blogger identity:
> - Blog title: NHÀ MỸ CALI — Cẩm Nang Mua Nhà Mỹ
> - Preferred Blogspot address: nhamycali.blogspot.com
> - Canonical website: https://nhamycali.com/
> - Approved brand assets from the repo
>
> If the preferred Blogspot address is unavailable, choose the cleanest brand-consistent descriptive fallback allowed by `playbooks/BLOGGER.md`. Do not add random numbers.
>
> Create the useful static/public structure defined in the playbook:
> - Giới thiệu/About
> - Website chính / canonical link to https://nhamycali.com/
> - clean readable navigation
>
> Publish exactly one approved first article from `content/seed/BLOGGER_FIRST_POST.md`. You may adapt formatting, headings, spacing, excerpt and other non-canonical presentation details for Blogger readability, but preserve factual/canonical meaning. Do not bulk-copy the NHÀ MỸ CALI website.
>
> Do not expose the private registration Gmail or unrelated Google-profile details on public pages.
>
> Stop only for a hard blocker:
> - Google security challenge, CAPTCHA, OTP/2FA
> - identity/business documents
> - strong existing-account ownership conflict
> - payment/custom-domain purchase
> - Terms/policy conflict
> - unsupported material factual claim
> - destructive irreversible action
>
> Credential fields: if the browser security boundary requires the owner to perform Google login/security verification, ask only for that specific manual action, then continue the Blogger workflow autonomously.
>
> After public QA succeeds:
> - update `state/accounts.csv`
> - update `brand/OFFICIAL_LINKS.yaml` only with the verified public Blogger URL
> - resolve any Blogger blocker in `state/manual_actions.md`
> - create/update a Blogger platform report
> - scan the diff for secrets
> - run `git diff --check`
> - commit the non-secret changes
> - report the public blog URL and commit SHA
> - STOP
>
> Do not start another platform.

## Human checkpoints

Routine UI is not a checkpoint.

Human input is expected only for:
- Google login/security verification if the browser requires it;
- CAPTCHA/anti-bot;
- OTP/2FA/security verification;
- identity/business documents;
- payment/financial authorization;
- ambiguous ownership;
- destructive irreversible actions.

## Expected output

Codex should report:
- whether an existing Blogger property was found;
- whether a new blog was created;
- final Blogspot URL;
- whether canonical website appears publicly;
- whether approved brand identity passed QA;
- whether the first article was published;
- any hard blocker encountered;
- exact state/report files updated;
- commit SHA;
- confirmation that no secret was committed.

## After Blogger

Stop for audit.

Do not expand to the next platform until the Blogger result is reviewed.
