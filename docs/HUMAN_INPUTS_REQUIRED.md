# Human Inputs Required

This file records information that must come from the authorized NHÀ MỸ CALI owner rather than being inferred by Codex.

## 1. Visual assets — first-wave requirement COMPLETE

Received from the project owner on **2026-09-28** and committed as approved source assets:

1. **Official NHÀ MỸ CALI transparent logo**  
   `assets/logo/nhamycali-logo-transparent.png`

2. **Official square/circular brand avatar**  
   `assets/avatar/nhamycali-avatar-square.png`

3. **Helen Hà Nguyễn official professional portrait**  
   `assets/helen/helen-ha-nguyen-headshot.png`

4. **Official NHÀ MỸ CALI / Coldwell Banker Realty banner**  
   `assets/cover/nhamycali-cover-official.png`

Technical hashes, dimensions and approval state are recorded in:

- `assets/ASSET_MANIFEST.yaml`
- `assets/PLATFORM_ASSET_POLICY.yaml`

### Optional visual inputs still useful later

These are **not blockers for the pilot**:

- official SVG/vector logo;
- horizontal logo;
- light/dark logo variants;
- higher-resolution cover/banner master;
- platform-specific cover source files;
- Canva/exported source templates;
- original San Jose/Bay Area/property photos owned or licensed by NHÀ MỸ CALI;
- separately authorized Coldwell Banker co-brand source files, if available.

## 2. Brand-design facts

If known, provide:

- official colors / HEX values;
- font names;
- logo usage rules;
- preferred visual style;
- any existing brand guideline PDF/Canva kit.

Do not guess these from screenshots if official files exist.

## 3. Registration account decisions

### Confirmed by owner on 2026-09-28

- Primary registration mailbox: **selected** and intentionally kept outside this public repository.
- SMS primary: **owner-controlled Vietnam mobile**, stored only as a runtime secret.
- SMS fallback: **existing U.S. business phone**, used only when a platform does not accept the Vietnam number.
- Exact runtime values belong in local `secrets/.env`; see `docs/REGISTRATION_POLICY.md`.

### Pilot-ready decisions

- temporary bootstrap password workflow approved by owner; literal value stays only in local `secrets/.env`;
- password-manager / unique-per-platform rotation is deferred to post-pilot hardening.

### Still optional/pending

- recovery email.

**Do not put actual passwords, OTPs, recovery codes, the private registration mailbox, or the private Vietnam verification number in GitHub.**

## 4. Existing-account knowledge

For each platform, tell the agent if you already know an account exists.

Known decisions:

- Pinterest — owner confirms NHÀ MỸ CALI already has an account but does not want Pinterest developed in this campaign. Leave it untouched unless reactivated.
- Bluesky — owner confirmed on 2026-09-30 that NHÀ MỸ CALI does **not** have a Bluesky account. The Bluesky pilot may skip duplicate-discovery and proceed directly to signup.

Still useful to identify:

- TikTok — not part of the current target list, but public canonical status is still unresolved.
- Any old Blogger/WordPress/Medium/Tumblr/Substack accounts.
- Any personal Helen account that should **not** be converted into a brand account.

Do not share passwords in this file.

## 5. Public contact confirmation

Current canonical public data in the repo:

- website: https://nhamycali.com/
- phone: 408-623-6577
- email: realestate@nhamycali.com
- office: 1712 Meridian Ave, San Jose, CA 95125
- Helen: Realtor® at Coldwell Banker Realty
- CalRE #01256922

If any of these has changed, update `brand/BRAND_ENTITY.yaml` before account creation.

## 6. Content assets

Helpful for later publishing waves:

- 5–10 best evergreen nhamycali.com articles;
- 5–10 high-quality recent listing/Open House examples;
- buyer FAQ;
- seller FAQ;
- Helen bio;
- testimonials/reviews that are approved for reuse;
- original market commentary;
- RSS/feed URL if known.

These are not required to create the foundation.

## 7. Legal/compliance preferences

If NHÀ MỸ CALI already uses standard disclaimers for:

- equal housing;
- brokerage disclosure;
- licensing;
- financial-information disclaimer;
- third-party listing data;
- privacy;

please provide the authoritative wording.

Codex should not invent legal boilerplate when an approved version exists.

## 8. Never provide through Git commits

Do not upload:

- passwords;
- TOTP seeds;
- backup/recovery codes;
- bank/card data;
- SSN;
- passport/driver license;
- private client documents;
- MLS credentials;
- private contracts;
- browser cookie exports.

If a platform later requires sensitive verification, handle it directly and manually outside this repository.
