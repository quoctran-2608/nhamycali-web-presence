# Registration & Verification Policy

Version: 1.0  
Confirmed by project owner: 2026-09-28

## 1. Security model

Registration credentials and verification contacts are **runtime secrets**, not repository data.

The owner has selected:

- one primary Gmail mailbox for new platform registrations;
- one Vietnam mobile number as the preferred SMS verification number;
- the existing U.S. business phone as the fallback SMS number only when a platform does not accept the Vietnam number.

The exact private registration mailbox and Vietnam phone number must be injected locally through `secrets/.env` or an approved secret/password manager. They must not be committed to this public repository.

The U.S. fallback number is already a public business contact in `brand/BRAND_ENTITY.yaml`, but automation should still consume it through the runtime verification configuration rather than hard-code it into signup scripts.

## 2. Required local environment

Create:

`secrets/.env`

from:

`secrets/.env.example`

Populate locally:

```bash
REGISTRATION_EMAIL=<approved registration Gmail>
SMS_PHONE_PRIMARY=<approved Vietnam mobile in international format>
SMS_PHONE_FALLBACK=<approved U.S. business phone in international format>
```

Recommended international formatting:

- Vietnam: `+84...` with the domestic leading zero removed.
- United States: `+1...`.

Do not commit `secrets/.env`.

## 3. Email rule

The registration/login mailbox is **private account infrastructure**.

It is not automatically:

- the public contact email;
- the About-page email;
- the profile-visible email.

For public-facing email fields, continue to use the approved public contact from `brand/BRAND_ENTITY.yaml`, unless the owner explicitly changes that policy.

## 4. SMS verification precedence

When a platform legitimately requires phone verification:

1. Prefer `SMS_PHONE_PRIMARY` — the owner-approved Vietnam number.
2. If the platform does not accept Vietnam numbers or explicitly requires a U.S. number, use `SMS_PHONE_FALLBACK`.
3. If either number requires an OTP, stop for the authorized human to provide/enter the code through the live browser session.
4. Never store OTP values in Git, logs, CSV, screenshots, Markdown, issues, or pull requests.

Do not use:
- temporary SMS services;
- rented verification numbers;
- third-party numbers not controlled by the owner.

## 5. Phone visibility rule

A phone used for verification must **not** automatically become a public profile field.

The Vietnam verification number is private runtime data.

The U.S. business number may be public because it is already canonical public contact information, but only populate it in a profile when that field is appropriate for the brand.

## 6. Recovery policy

Recovery email is optional and remains unconfigured until the owner explicitly selects one.

Do not infer a recovery email from public brand contact data.

## 7. Password policy

Passwords must be unique per platform and kept outside Git.

Until a password-manager workflow is confirmed:

- do not write passwords to repository files;
- do not put passwords into `state/accounts.csv`;
- allow the authorized browser/password manager to save credentials locally if the human has configured it;
- if secure credential storage is unavailable, stop before scaling account creation.

## 8. Browser-session rule

Codex may fill approved registration fields in a browser session.

Codex must stop for human action when:

- OTP entry is required;
- CAPTCHA requires human interaction;
- identity/business documents are requested;
- an account-recovery decision is required;
- payment authorization is required.

## 9. Platform-specific exceptions

Some platforms use Google OAuth instead of email/password signup.

When “Continue with Google” is available, do not automatically choose it solely for convenience. Research the platform first and use the login method that best preserves account ownership, recovery, and separation from unrelated personal accounts.

## 10. Audit requirement

After each registration attempt, record only non-secret state:

- platform;
- status;
- username;
- public profile URL;
- whether email verification completed;
- whether phone verification completed;
- whether human action remains;
- whether credentials are managed externally.

Do not record the registration email or verification phone values in public state files.
