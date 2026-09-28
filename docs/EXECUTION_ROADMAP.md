# Execution Roadmap

## Phase 0 — Foundation

Goal: create the source of truth and rules.

Deliverables:
- AGENTS.md
- brand identity
- official-link registry
- copy library
- SEO policy
- account-creation rules
- platform registry
- state files
- asset manifest

Status: **built in foundation-v1**

## Phase 1 — Human inputs and asset normalization

Status: **visual asset normalization complete; account-access inputs still pending**

Completed:
- approved logo committed;
- approved brand avatar committed;
- approved Helen professional portrait committed;
- approved official banner committed;
- asset provenance/hashes recorded;
- brand-vs-person usage policy defined.

Confirmed:
- primary registration mailbox selected by the owner and kept as a runtime secret outside Git;
- preferred SMS verification order selected: Vietnam mobile first, U.S. business phone only as fallback when Vietnam numbers are unsupported;
- Pinterest is known to exist and is intentionally excluded from the active campaign.

Still required before pilot signup:
- choose/confirm password-management workflow outside Git;
- optionally choose a recovery email;
- confirm any additional pre-existing accounts already known by the owner.

Current public contact facts remain in `brand/BRAND_ENTITY.yaml` and should be re-confirmed if the owner reports a change.

Do not begin broad signup until the remaining access inputs and the live platform research pass are complete.

## Phase 2 — Platform research pass

Status: **Wave 1 live research completed on 2026-09-28.**

Authoritative snapshot:
- `research/WAVE_1_LIVE_RESEARCH_2026-09-28.md`
- `research/WAVE_1_DECISIONS.yaml`

Key outcomes:
- Gravatar: existing Helen profile found; audit only.
- Bluesky: active pilot candidate; domain handle `@nhamycali.com` is the preferred long-term identity after separate DNS approval.
- About.me: removed from brand signup under current Terms interpretation.
- Medium: manual-only because Medium Rules prohibit automated account registration/posting.
- Substack: active human-supervised pilot candidate.
- Blogger: active human-supervised pilot candidate.
- Google Sites: technically viable but deferred until a distinct resource-hub concept is approved.
- Feedly: removed from SEO signup; optional monitoring utility.
- Inoreader: removed from SEO signup; Terms explicitly identify automated registrations for SEO boosting as abusive.
- Linktree: existing official account audited; manual changes only.
- Pinterest: already excluded by owner decision.

Before any actual signup, re-check the exact target in-platform because a public-search no-match is not proof of absence.

## Phase 3 — Pilot batch

Do not start with all platforms.

### Active browser-assisted creation candidates

1. **Bluesky**
2. **Substack**
3. **Blogger**

### Existing-account audits

4. **Gravatar** — existing Helen profile; no duplicate creation.
5. **Linktree** — existing official account; manual changes only.

### Manual platform execution

6. **Medium** — Codex may prepare copy/content, but account creation and publishing must be performed manually under current Medium Rules.

### Deferred

7. **Google Sites** — wait for a distinct resource-hub/event concept.

### Removed from active signup

- About.me
- Feedly
- Inoreader
- Pinterest

For each active candidate:
- verify existing account inside the platform immediately before signup;
- create only if absent;
- complete profile;
- add canonical website where appropriate;
- verify public view;
- log state;
- stop at CAPTCHA/SMS/OTP/manual verification.

## Phase 4 — Pilot audit

Review:
- account suspension/security issues;
- profile consistency;
- public indexing;
- actual referral usefulness;
- whether website link displays correctly;
- whether signup automation appears permitted/stable.

Adjust rules before continuing.

## Phase 5 — Publishing/distribution expansion

After the pilot audit, research the next candidates individually:

- WordPress.com
- Tumblr
- Flipboard
- Follow.it
- NewsBlur
- Feedspot
- Feeder
- The Old Reader

Medium remains manual-only.

Feedly and Inoreader are no longer active SEO/signup targets; they may be used manually for internal monitoring if useful.

Only seed content where there is an actual content role.

## Phase 6 — Visual/creative expansion

Only with suitable assets:

- Behance
- 500px
- SoundCloud

Pinterest remains excluded unless explicitly reactivated by the owner.

No scraped or synthetic representation of real properties/persons.

## Phase 7 — Community strategy

Separate manual plan for:

- Reddit
- Disqus

No automated promotional link drops.

## Phase 8 — Utility integrations

Only when operationally useful:

- Bitly
- IFTTT
- Trello
- Dropbox
- Evernote
- OneNote
- Raindrop
- Instapaper

Do not count these as SEO profile targets by default.

## Phase 9 — Earned-link program

After entity/distribution foundation is stable, prioritize real authority:

- Vietnamese Bay Area community resources;
- local publications;
- expert quotes/interviews;
- neighborhood guides;
- original local market data;
- professional directories/associations;
- legitimate event/sponsorship pages;
- useful partner/resource pages.

This phase is more valuable long-term than maximizing raw profile count.
