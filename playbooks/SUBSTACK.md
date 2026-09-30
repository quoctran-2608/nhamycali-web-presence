# Substack Pilot Playbook

Research snapshot: 2026-09-28  
Execution update: 2026-09-30  
Mode: **autonomous routine browser with hard security/authorization checkpoints**

## 1. Purpose

Use Substack as a real Vietnamese-language real-estate newsletter/editorial channel, not as a one-page backlink shell.

Canonical owned website remains:

**https://nhamycali.com/**

Do not purchase or configure a Substack custom domain during the pilot.

## 1.1. Autonomous execution rule

For routine reversible UI work, proceed without asking the owner.

Autonomous actions include:
- clicking ordinary Next/Continue/Save/Edit/Create/Publish/Skip controls;
- retrying an unresponsive normal control up to 3 times;
- reloading or directly navigating to the official Substack page when needed;
- filling profile/publication fields from canonical data;
- adapting non-canonical copy to field limits;
- choosing reasonable non-sensitive categories, layout/navigation order, visibility/default settings;
- uploading approved assets;
- publishing the approved welcome issue;
- running public QA and updating repo state/report.

If browser tooling cannot activate a normal button after reasonable retries, ask for **one manual click only**, then resume from the resulting page. Do not restart the workflow.

Hard checkpoints remain CAPTCHA/anti-bot, OTP/2FA/security verification, identity/business documents, payment/Stripe/card/bank authorization, uncertain ownership, Terms conflict, or destructive irreversible actions.

## 2. Preflight

Before signup:

1. Perform one reasonable existing-account check for:
   - NHÀ MỸ CALI
   - Nha My Cali
   - nhamycali
   - Helen Ha Nguyen / Helen Hà Nguyễn
2. If a strong likely official publication/profile is found:
   - do not create a duplicate;
   - record URL;
   - stop for ownership confirmation.
3. If no strong match is found, or logged-out/internal search is unavailable and signup itself shows no ownership conflict, **proceed with signup** rather than looping on discovery.
4. Confirm the approved registration credential workflow is available.
5. Load approved assets:
   - publication/avatar: `assets/avatar/nhamycali-avatar-square.png`
   - Helen author identity, only if a distinct author/person field exists: `assets/helen/helen-ha-nguyen-headshot.png`

## 3. Identity architecture

Preferred public architecture:

- Publication/brand: **NHÀ MỸ CALI**
- Human expert/author where Substack exposes a separate person identity: **Helen Hà Nguyễn**
- Canonical website: **https://nhamycali.com/**

Do not collapse the two identities accidentally.

If Substack's live onboarding forces a single public identity, use **NHÀ MỸ CALI** as the brand/publication-facing identity when the field is clearly for the publication or public brand. Use **Helen Hà Nguyễn** only when the field is clearly a personal author identity.

Inspect preview when available and choose the brand-first option autonomously. Stop only if Substack requires a legal/personal identity fact that cannot be represented truthfully from canonical data.

## 4. Handle

Preferred:

**nhamycali**

Substack profile URL would normally be:

`https://substack.com/@nhamycali`

Only record that URL after Substack confirms the handle.

If unavailable:
- do not append random numbers;
- try the approved username fallback order from `AGENTS.md` when the platform syntax permits;
- choose the first clean brand-consistent fallback autonomously;
- stop only if all approved fallbacks fail.

## 5. Publication name and description

Publication name:

**NHÀ MỸ CALI**

Short description:

> **Cẩm nang bất động sản California dành cho người Việt — mua nhà, bán nhà, tài chính và thị trường San Jose & Bay Area.**

Longer About copy should come from `brand/COPY_LIBRARY.md`.

## 6. Links

Where Substack permits website/social links:

Primary:
- `https://nhamycali.com/`

Then verified official accounts only from:
- `brand/OFFICIAL_LINKS.yaml`

Do not add:
- guessed URLs;
- Pinterest, because it is excluded from active campaign;
- accounts that are not publicly verified.

## 7. Profile image

Publication/brand image:

`assets/avatar/nhamycali-avatar-square.png`

Helen author/profile image:
`assets/helen/helen-ha-nguyen-headshot.png`

Use Helen only for an explicit personal/author identity.

## 8. Paid features

Do not:
- enable paid subscriptions;
- connect Stripe;
- buy a custom domain;
- make a payment;

unless the owner explicitly authorizes the exact action.

Pilot target is a free public editorial/newsletter presence.

## 9. Initial publication structure

Before publishing the first issue, configure:

- title;
- description;
- avatar;
- About;
- canonical website;
- useful navigation if supported.

Do not create excessive navigation links.

## 10. First issue

Use:
`content/seed/SUBSTACK_WELCOME.md`

The first issue should:
- explain why the newsletter exists;
- identify the Vietnamese/California audience;
- explain what subscribers will receive;
- link naturally to nhamycali.com;
- avoid exaggerated sales language.

Do not import/mirror the full nhamycali.com archive during pilot.

## 11. Public QA

Verify:

- publication/profile is public;
- name is correct;
- handle is correct;
- avatar is brand avatar;
- website links to exact canonical URL;
- Helen attribution is accurate if shown;
- no private login email or verification phone is exposed;
- no paid feature was accidentally enabled;
- first issue renders correctly.

## 12. State update

Update `state/accounts.csv` only with non-secret data.

Record:
- handle;
- public profile/publication URL;
- website added;
- public verified;
- email verified;
- manual action required.

If Substack produces separate profile and publication URLs, document both in Notes and add only a stable verified canonical URL to `brand/OFFICIAL_LINKS.yaml`.

## 13. Stop conditions

Stop only for:
- strong likely existing official account with uncertain ownership;
- all approved handle fallbacks unavailable;
- CAPTCHA/anti-bot requiring human interaction;
- OTP/2FA/email/SMS security verification that cannot be legitimately completed;
- identity/business/legal documents;
- payment/Stripe/card/bank/custom-domain purchase authorization;
- Terms/policy conflict;
- destructive irreversible action.

Ordinary UI friction, field-layout changes, copy fitting, category selection, navigation order, avatar upload, Save/Create/Publish controls, and publication/profile identity choices covered above are not stop conditions.

## 14. Success definition

A successful pilot is a **real, useful NHÀ MỸ CALI newsletter/publication**, with a clear reason to subscribe independent of any backlink value.
