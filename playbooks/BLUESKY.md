# Bluesky Pilot Playbook

Research snapshot: 2026-09-28  
Platform: https://bsky.app/  
Mode: **human-supervised browser**

## 1. Why this platform is in the pilot

Bluesky supports organization accounts. Its official guidance strongly recommends that official organizations use an owned domain as their handle for identity verification.

Long-term target identity:

**@nhamycali.com**

The domain-handle step requires DNS and is separate from initial account creation.

## 2. Preflight — mandatory

Owner status for this pilot:

> **The authorized NHÀ MỸ CALI project owner confirmed on 2026-09-30 that NHÀ MỸ CALI does not currently have a Bluesky account.**

Therefore, **do not repeat account-discovery/search for this Bluesky pilot**. Logged-out/internal search availability is not a blocker.

Before clicking Sign up:

1. Read `research/WAVE_1_DECISIONS.yaml` and confirm the Bluesky `owner_attestation` is present.
2. Proceed directly to the official Bluesky signup flow.
3. Confirm local runtime secret `REGISTRATION_EMAIL` is available.
4. Confirm the runtime password secret required by the current local pilot configuration is available.
5. Confirm approved asset:
   - `assets/avatar/nhamycali-avatar-square.png`
6. Create **at most one** NHÀ MỸ CALI Bluesky account.

If the signup flow itself reveals that the email/handle is already attached to an existing account or otherwise indicates an ownership conflict:
- stop;
- do not create a duplicate;
- record the conflict for human resolution.

## 3. Identity model

This is a **brand account**, not Helen's personal account.

Use:

- Display name: **NHÀ MỸ CALI**
- Brand avatar: `assets/avatar/nhamycali-avatar-square.png`
- Canonical website: **https://nhamycali.com/**
- Brand mission: **Giúp Người Việt An Tâm Mua Nhà Mỹ**

Do not use Helen's portrait as the default avatar.

## 4. Initial handle

Preferred temporary handle if available:

**nhamycali.bsky.social**

Do not invent random-number variants.

If unavailable:
- stop;
- document availability conflict;
- do not choose a fallback without checking platform syntax and human approval.

Reason: the intended stable handle is eventually **@nhamycali.com**, so there is little value in creating a messy temporary identity.

## 5. Signup fields

Use the current live UI rather than assuming historical field order.

Rules:

- Registration email: load from runtime secret, never from repo.
- Password: load from the approved local runtime secret for the current pilot; never print, log, or commit it. The owner may rotate it after account creation.
- Date/age or other eligibility field: do not fabricate. Human must provide any personal/legal eligibility detail if requested.
- Phone verification: follow `docs/REGISTRATION_POLICY.md`.
- OTP: human action.
- CAPTCHA: human action.

If the UI asks for identity/business documents, stop.

## 6. Profile copy

Preferred concise bio:

> **Bất động sản California dành cho người Việt | San Jose & Bay Area. Giúp bạn hiểu rõ hơn hành trình mua và bán nhà Mỹ. nhamycali.com**

If the live character limit is smaller, shorten in this order:

1. preserve Vietnamese audience;
2. preserve California/San Jose-Bay Area;
3. preserve education/clarity;
4. preserve brand website if clickable/profile-link support is available.

Do not add:
- unsupported awards;
- follower counts;
- “#1” or “best” claims;
- guaranteed investment language.

## 7. Website/link handling

If the live profile UI offers a dedicated website/link field:
- use `https://nhamycali.com/`.

If no dedicated field exists:
- use the canonical website naturally in the bio if it remains readable.

Do not use a shortened URL for the canonical identity link.

## 8. Domain handle — separate Phase B

Do **not** change DNS during initial signup unless the owner explicitly authorizes it in that execution session.

After the base account is publicly verified:

1. Bluesky: Settings → Account → Handle.
2. Choose the option for an owned domain.
3. Bluesky will provide an account-specific DID.
4. Add the TXT record at:
   - host/name: `_atproto`
   - value: the exact DID value provided by Bluesky.
5. Wait for DNS propagation.
6. Use Bluesky's Verify DNS Record action.
7. Confirm public handle becomes:
   - **@nhamycali.com**

Never invent the DID value.

Do not modify unrelated DNS records.

## 9. First content

Do not launch with only a naked backlink.

Use `content/seed/BLUESKY_SEED.md`.

Minimum viable launch:
- completed profile;
- one brand-introduction post;
- one educational post;
- optional third post pointing to a genuinely relevant nhamycali.com resource.

Do not bulk-post.

## 10. Public QA

Open the public profile and verify:

- display name exactly NHÀ MỸ CALI;
- avatar not clipped;
- bio reads naturally;
- canonical website/link is correct;
- no private registration email is visible;
- no private Vietnam verification phone is visible;
- no accidental personal identity field is exposed;
- temporary handle is recorded accurately.

If domain handle was configured:
- verify `@nhamycali.com` resolves publicly.

## 11. State update

Update `state/accounts.csv`.

Allowed resulting statuses:

- `existing_account_found`
- `pending_email_verification`
- `manual_action_required`
- `in_progress`
- `completed`
- `failed_retryable`

Only use `completed` after public QA.

Record:
- final username/handle;
- public profile URL;
- website added;
- public verified;
- email verified;
- manual blocker if any.

Never record password, OTP, registration email, or private verification phone.

## 12. Stop conditions

Stop immediately for:

- signup reveals an unexpected existing-account or ownership conflict;
- CAPTCHA that needs human action;
- OTP;
- age/identity fact not available;
- document verification;
- payment;
- account suspension;
- handle conflict requiring a naming decision;
- DNS change without explicit approval.

## 13. Success definition

Success is **one authentic public NHÀ MỸ CALI account**, not merely a completed signup form.

Preferred final identity:

**NHÀ MỸ CALI — @nhamycali.com**
