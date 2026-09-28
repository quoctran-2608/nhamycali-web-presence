# AGENTS.md — NHÀ MỸ CALI Web Presence

This file is the **primary operating contract for Codex and other automation agents** working in this repository.

## 1. Mission

Build and maintain a trustworthy, consistent public web presence for **NHÀ MỸ CALI**.

The project is **not** a mass-link-spam project. Its goals are:

- consistent brand/entity representation;
- legitimate public profiles;
- useful content distribution;
- branded citations;
- discoverability;
- referral traffic;
- auditable account operations;
- SEO practices that remain within search-engine and platform guidelines.

Core mission of the brand:

> **Giúp Người Việt An Tâm Mua Nhà Mỹ.**

## 2. Required reading order

Before doing any account, profile, content, SEO, or browser work, read in this order:

1. `AGENTS.md`
2. `brand/BRAND_ENTITY.yaml`
3. `brand/OFFICIAL_LINKS.yaml`
4. `brand/BRAND_DNA.md`
5. `brand/COPY_LIBRARY.md`
6. `assets/ASSET_MANIFEST.yaml`
7. `assets/PLATFORM_ASSET_POLICY.yaml`
8. `campaign/ACCOUNT_CREATION_RULES.md`
9. `campaign/SEO_LINK_POLICY.md`
10. `campaign/PLATFORMS.yaml`
11. `docs/REGISTRATION_POLICY.md`
13. the relevant state files under `state/`

If instructions conflict, this order of authority applies:

1. explicit human instruction in the current task;
2. `AGENTS.md`;
3. canonical structured brand data;
4. approved asset manifest and platform asset policy;
5. campaign rules;
6. prior execution state;
7. generated copy/templates.

## 3. Canonical identity

Use `brand/BRAND_ENTITY.yaml` as the machine-readable source of truth.

Never invent or silently alter:

- brand name;
- website;
- phone;
- email;
- office address;
- Helen Hà Nguyễn's name;
- brokerage;
- CalRE number;
- official social URLs;
- legal/business relationship claims.

If a field is unknown, keep it unknown. Do not infer it.

## 4. Account-discovery-first rule

Before creating an account on any platform:

1. Check `brand/OFFICIAL_LINKS.yaml`.
2. Check `state/accounts.csv`.
3. Search the platform and public web for an existing official NHÀ MỸ CALI profile.
4. Compare branding, website, contact details, and ownership clues.
5. If an official account appears to exist, **do not create a duplicate**.
6. Record the finding and flag ownership/login recovery if needed.

The default action is **verify first, create second**.

## 5. Username policy

Preferred username:

`nhamycali`

Fallback order:

1. `nha_my_cali`
2. `nhamycali_realestate`
3. `nhamycalirealestate`

Do not append random numbers unless a human explicitly approves it.

Do not take a username that could misrepresent another organization or person.

## 6. Browser automation safety

Automation may navigate forms, enter approved public brand data, upload approved assets, and complete ordinary signup/profile workflows.

Automation must **not** bypass or defeat:

- CAPTCHA;
- bot detection;
- rate limits;
- email/phone security checks;
- identity verification;
- two-factor authentication;
- access controls;
- platform restrictions;
- payment gates.

When blocked by one of these, stop that platform cleanly and record it in `state/manual_actions.md`.

Never use fake phone numbers, fake addresses, disposable identity documents, synthetic reviews, or fabricated credentials.

## 7. Credential policy

Never commit or print:

- passwords;
- password-manager exports;
- TOTP seeds;
- recovery codes;
- authentication cookies;
- browser storage state;
- identity documents;
- payment-card data;
- bank information.

Secrets belong outside Git. A local `secrets/.env` may be used if the execution environment supports it, but that file is ignored by Git.

Registration email and SMS verification contacts selected by the owner are runtime secrets. Follow `docs/REGISTRATION_POLICY.md`; do not copy those private values into Markdown, YAML, CSV, issues, pull requests, screenshots, or logs.

Do not store passwords in `state/accounts.csv`.

## 8. SEO / link policy

Do not optimize for raw backlink count.

Do not:

- create low-value profiles solely for PageRank;
- automate forum/comment spam;
- post the same thin article across many sites;
- stuff exact-match anchor text;
- manufacture fake engagement;
- create misleading redirects;
- represent utility tools as editorial endorsements.

A public website field on a legitimate brand profile is allowed when it is a normal platform feature.

For publishing platforms, content must have a real audience purpose independent of the backlink.

See `campaign/SEO_LINK_POLICY.md`.

## 9. Community-platform rule

For community-driven platforms such as Reddit and Disqus:

- profile creation may be automated if allowed;
- link-dropping/comment campaigns must not be automated;
- participation must follow community rules;
- no repetitive promotional replies;
- no undisclosed self-promotion;
- no fabricated user conversations.

Default: profile-only until a human-approved community plan exists.

## 10. Content policy

Content should represent NHÀ MỸ CALI as a Vietnamese-first California real-estate guide.

Prefer:

- clarity;
- education;
- local usefulness;
- factual claims;
- trade-offs;
- real next steps.

Avoid:

- fake urgency;
- guarantees of appreciation;
- guaranteed loan approval;
- guaranteed school enrollment;
- unsupported "best/top" claims;
- implying buying property creates immigration status;
- claiming a property is Helen/NHÀ MỸ CALI's exclusive listing without verification.

Dynamic facts must be refreshed before publication.

## 11. Platform execution lifecycle

For each platform:

1. Research current platform purpose and signup requirements.
2. Classify its campaign role.
3. Check for an existing official account.
4. Confirm that account creation is appropriate.
5. Create account only if absent.
6. Complete email verification if accessible through an approved mechanism.
7. Configure display name and username.
8. Upload approved avatar/logo.
9. Add bio/About copy suited to platform constraints.
10. Add canonical website when the platform provides a normal website field.
11. Add other verified official links only if appropriate.
12. Save.
13. Open the public profile in a logged-out/public view when possible.
14. Verify displayed data.
15. Record final profile URL and status in `state/accounts.csv`.
16. Record blockers in `state/manual_actions.md`.
17. Save evidence/screenshot outside Git if it may contain sensitive data.

## 12. State discipline

Every platform must have a state.

Allowed high-level statuses:

- `not_started`
- `research_needed`
- `existing_account_found`
- `ownership_check_needed`
- `in_progress`
- `pending_email_verification`
- `manual_action_required`
- `completed`
- `not_suitable`
- `retired`
- `failed_retryable`
- `failed_permanent`

Never mark `completed` until the public profile has been verified.

## 13. Updating official links

Only update `brand/OFFICIAL_LINKS.yaml` when:

- the profile is publicly reachable;
- branding matches NHÀ MỸ CALI;
- ownership is known;
- the final canonical URL has been verified.

Do not add guessed URLs.

## 14. Asset policy

Asset approval lives in `assets/ASSET_MANIFEST.yaml`. Platform-specific identity choices live in `assets/PLATFORM_ASSET_POLICY.yaml`.

Only use files whose manifest entry has:

`approved_public_use: true`

Canonical first-wave defaults:

- brand account avatar → `assets/avatar/nhamycali-avatar-square.png`
- full transparent logo → `assets/logo/nhamycali-logo-transparent.png`
- Helen individual/author portrait → `assets/helen/helen-ha-nguyen-headshot.png`
- official supplied banner → `assets/cover/nhamycali-cover-official.png`

Identity rule:

- NHÀ MỸ CALI brand account → brand avatar by default;
- Helen individual Realtor/author identity → Helen headshot;
- ambiguous identity → stop and decide before publishing.

The official cover is 851×315 and contains Coldwell Banker Realty co-branding. Treat it as an intact approved banner/reference, not as a universal high-resolution master.

Do not:

- scrape a logo or portrait from web search;
- invent a new logo;
- replace Helen's headshot with generated imagery;
- extract the Coldwell Banker Realty mark from the supplied banner for standalone reuse;
- silently crop away important branding/text;
- substantially upscale the official cover;
- use unlicensed third-party photography.

## 15. Change-management rule

When changing canonical brand facts or campaign policy:

- make the smallest necessary edit;
- preserve history;
- explain the reason in the commit;
- update dependent files when necessary;
- do not silently rewrite prior execution records.

## 16. Stop conditions

Stop and require human action when:

- identity verification is required;
- SMS verification is required and no approved number is available;
- a CAPTCHA cannot be completed normally;
- an existing account may already belong to NHÀ MỸ CALI but ownership is uncertain;
- platform Terms appear to prohibit the intended automation;
- a payment is required;
- a platform requests legal/business documents;
- the platform would require making a claim not supported by canonical data.

## 17. Completion report

After a batch, report:

- platforms checked;
- accounts already existing;
- accounts created;
- public profile URLs;
- website links added;
- manual actions required;
- failures;
- any proposed canonical-data changes.

The report must distinguish **created**, **verified**, and merely **attempted** accounts.

---

If uncertain, preserve trust and stop rather than fabricate, bypass, spam, or create a duplicate identity.
