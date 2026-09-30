# Codex Browser Pilot — Current Task

This is the current browser-execution entry point.

## Current live task

**Run only the Blogger pilot. Bluesky and Substack are completed. Do not start another platform in the same task.**

Completed canonical properties:
- Bluesky: https://bsky.app/profile/nhamycali.bsky.social
- Substack publication: https://nhamycali.substack.com/
- Substack author: https://substack.com/@helenhanguyen

Do not recreate or re-run signup for those completed platforms.

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
> Operate autonomously for routine reversible browser work. Do not ask me before ordinary actions such as Next, Continue, Save, Edit, Upload, Create, Publish, navigation, reasonable field selection, copy fitting, theme/layout choices, or public QA when the intended result is already defined by the repo.
>
> If an ordinary UI action does not respond, retry it up to 3 times using normal browser actions, reload, or direct navigation to the official Blogger page. If browser tooling still cannot activate the control, ask me for one manual click only, then continue from the resulting page without restarting the workflow.
>
> Blogger uses an authorized Google Account. Inspect the Blogger dashboard once for an existing NHÀ MỸ CALI/Nha My Cali blog owned by that account. If a strong existing official blog is present, stop for ownership/normalization confirmation. If none is present, proceed with creating one.
>
> Preferred blog identity:
> - title: NHÀ MỸ CALI — Cẩm Nang Mua Nhà Mỹ
> - preferred Blogspot address: nhamycali.blogspot.com
> - description: Kiến thức mua và bán nhà California dành cho người Việt, tập trung San Jose & Bay Area. Nội dung từ NHÀ MỸ CALI.
> - canonical website: https://nhamycali.com/
> - logo/header asset: assets/logo/nhamycali-logo-transparent.png
> - brand avatar: assets/avatar/nhamycali-avatar-square.png
>
> Keep the blog clearly distinct from the canonical website. Do not mirror the full nhamycali.com site or mass-import articles.
>
> Create a useful Giới thiệu/About page and add a normal navigation link labeled `NHÀ MỸ CALI` pointing to https://nhamycali.com/ where Blogger supports it.
>
> Publish only the approved first article from `content/seed/BLOGGER_FIRST_POST.md`. You may improve formatting, heading hierarchy, spacing, excerpt/description, and other non-canonical presentation details while preserving factual meaning.
>
> Use a simple readable mobile-friendly Blogger theme. Do not spend pilot time recreating the main website.
>
> Stop only for a hard blocker:
> - CAPTCHA/anti-bot requiring human interaction
> - Google/OTP/2FA/security verification you cannot legitimately complete
> - identity/business documents
> - payment/custom-domain authorization
> - strong existing official blog with uncertain ownership
> - preferred Blogspot address unavailable and no already-approved clean fallback is available
> - Terms/policy conflict
> - destructive irreversible action
>
> Credential/login fields: use the existing authorized Google session when available. If Google requires the owner to enter credentials or verification directly, ask only for that intervention, then immediately continue the rest autonomously.
>
> After public QA succeeds:
> - update `state/accounts.csv`
> - update `brand/OFFICIAL_LINKS.yaml` only with the verified public Blogger URL
> - resolve Blogger blockers in `state/manual_actions.md`
> - create/update `reports/blogger-pilot-2026-09-30.md`
> - scan the diff for secrets
> - run `git diff --check`
> - commit the non-secret changes
> - report the public blog URL, first-post URL, and commit SHA
> - STOP
>
> Do not start another platform.

## Human checkpoints

Routine UI is not a checkpoint.

Human input is expected only for:
- Google credential/security entry if required;
- CAPTCHA/anti-bot;
- OTP/2FA/security verification;
- identity/business documents;
- payment/custom-domain authorization;
- ambiguous ownership;
- a naming decision if the preferred Blogspot address is unavailable and no approved clean fallback exists;
- destructive irreversible actions.

## Expected output

Codex should report:
- whether an existing Blogger property was found;
- whether a new blog was created;
- final Blogspot URL;
- whether canonical website navigation appears publicly;
- whether brand/About/theme passed QA;
- whether the approved first article was published;
- any hard blocker encountered;
- exact state/report files updated;
- commit SHA;
- confirmation that no secret was committed.

## After Blogger

Stop for audit.

Only after Blogger passes audit should the project expand to Wave 2.
