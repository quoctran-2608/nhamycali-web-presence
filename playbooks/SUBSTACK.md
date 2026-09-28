# Substack Pilot Playbook

Research snapshot: 2026-09-28  
Mode: **human-supervised browser**

## 1. Purpose

Use Substack as a real Vietnamese-language real-estate newsletter/editorial channel, not as a one-page backlink shell.

Canonical owned website remains:

**https://nhamycali.com/**

Do not purchase or configure a Substack custom domain during the pilot.

## 2. Preflight

Before signup:

1. Search Substack internally for:
   - NHÀ MỸ CALI
   - Nha My Cali
   - nhamycali
   - Helen Ha Nguyen / Helen Hà Nguyễn
2. If a likely existing official publication/profile is found:
   - do not create a duplicate;
   - record URL;
   - stop for ownership confirmation.
3. Confirm runtime registration email.
4. Confirm unique credential storage.
5. Load approved assets:
   - publication/avatar: `assets/avatar/nhamycali-avatar-square.png`
   - Helen author identity, only if a distinct author/person field exists: `assets/helen/helen-ha-nguyen-headshot.png`

## 3. Identity architecture

Preferred public architecture:

- Publication/brand: **NHÀ MỸ CALI**
- Human expert/author where Substack exposes a separate person identity: **Helen Hà Nguyễn**
- Canonical website: **https://nhamycali.com/**

Do not collapse the two identities accidentally.

If Substack's live onboarding forces a single personal identity and the public consequence is unclear:
- stop;
- inspect preview;
- choose only after confirming how the name will appear publicly.

## 4. Handle

Preferred:

**nhamycali**

Substack profile URL would normally be:

`https://substack.com/@nhamycali`

Only record that URL after Substack confirms the handle.

If unavailable:
- do not append random numbers;
- stop for a naming decision.

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

Stop for:
- existing likely official account;
- handle conflict;
- CAPTCHA/OTP;
- identity ambiguity;
- payment/Stripe/custom-domain upsell requiring purchase;
- unexpected request for business/legal documents;
- any UI change that makes public identity unclear.

## 14. Success definition

A successful pilot is a **real, useful NHÀ MỸ CALI newsletter/publication**, with a clear reason to subscribe independent of any backlink value.
