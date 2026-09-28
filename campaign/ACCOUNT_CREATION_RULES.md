# Account Creation Rules

These rules govern browser-assisted account creation for NHÀ MỸ CALI.

## 1. Goal

Create or normalize legitimate public accounts that have a real brand, publishing, distribution, creative-portfolio, or community purpose.

Account creation is **not** a target by itself. A platform should only be used when its role is clear.

## 2. Preflight checklist

Before opening a signup form:

- read `AGENTS.md`;
- read canonical brand files;
- inspect `campaign/PLATFORMS.yaml`;
- check `state/accounts.csv`;
- check `brand/OFFICIAL_LINKS.yaml`;
- search for an existing NHÀ MỸ CALI account;
- confirm the exact domain is legitimate;
- confirm the platform is still active;
- confirm the platform purpose fits the campaign;
- note any current Terms/anti-automation restrictions that affect execution.

Do not proceed from a stale saved URL without confirming the domain.

## 3. Allowed signup data

Use only approved fields from `brand/BRAND_ENTITY.yaml` and approved runtime secrets.

Typical allowed public fields:

- NHÀ MỸ CALI
- Nha My Cali
- nhamycali
- https://nhamycali.com/
- San Jose, California
- approved public phone
- approved public contact email
- approved bios
- approved logo/avatar
- approved Helen credential line where appropriate

## 4. Registration email vs public email

The email used to register an account does **not** automatically become a public contact field.

The automation must distinguish:

- `registration_email`: private login/account-purpose value;
- `public_contact_email`: approved public contact from canonical brand data.

Never expose a private registration/recovery email just because a form offers a public email field.

## 5. Passwords

Requirements:

- unique password per service;
- managed through an approved password manager or secure secret store;
- never written to CSV, Markdown, logs, screenshots, commits, issues, or PR comments.

The repository should record only a non-secret reference such as:

`credential_managed_externally: true`

or a password-manager item name if the human explicitly chooses that workflow.

## 6. Username selection

Preferred:

`nhamycali`

Fallback:

1. `nha_my_cali`
2. `nhamycali_realestate`
3. `nhamycalirealestate`

If all are unavailable, stop and request a human naming decision. Do not add arbitrary numbers.

## 7. Existing-account handling

If a likely official account exists:

- do not register a duplicate;
- record URL;
- compare brand identifiers;
- mark `existing_account_found` or `ownership_check_needed`;
- if the human has login access, normalize the profile instead of creating a new one.

If an account exists but clearly belongs to an unrelated party, document that fact before selecting a fallback username.

## 8. Email verification

Allowed when:

- the automation has legitimate access to the approved mailbox;
- the verification flow is ordinary and authorized.

Do not:
- use temporary mail;
- scrape another person's inbox;
- bypass verification.

If mailbox access is unavailable:
- mark `pending_email_verification`;
- record the exact required action.

## 9. CAPTCHA and bot challenges

Never attempt to bypass, outsource deceptively, or defeat CAPTCHA/anti-bot systems.

Allowed outcome:

`manual_action_required`

Record:
- platform;
- step reached;
- what challenge appeared;
- whether entered fields were preserved.

## 10. Phone/SMS

Do not use:
- temporary SMS services;
- rented verification numbers;
- numbers not controlled by the authorized brand owner.

If SMS is mandatory and no approved number is configured:
- stop;
- record manual action.

## 11. Identity/business verification

Never upload identity documents, licenses, tax forms, incorporation records, or payment documents unless a human has explicitly approved that exact platform and action.

Default:
- stop;
- mark manual action.

## 12. Paid plans

Never purchase a plan automatically unless an explicit human instruction authorizes:
- platform;
- plan;
- price/budget;
- payment method.

A signup flow reaching a payment gate is not authorization to pay.

## 13. Profile completion

A newly created account should not be considered complete with only a username.

Where supported, populate appropriate fields:

- display name;
- username;
- profile image;
- bio;
- About;
- location;
- canonical website;
- category;
- relevant official social links.

Do not fill irrelevant fields simply to reach 100% profile completion.

## 14. First content

Only platforms classified for publishing or distribution should receive initial content.

Do not publish generic “Hello world — visit our website” posts just to create a link.

Initial content must provide independent user value.

## 15. Verification of success

Before marking complete:

- save the profile;
- open public profile;
- verify the public URL;
- verify display name;
- verify website link;
- verify avatar/bio where applicable;
- check for accidental private-data exposure.

Then update state.

## 16. Rate and batch discipline

Do not blindly create dozens of accounts in one uninterrupted burst.

Recommended rollout:

- small pilot batch;
- audit;
- adjust rules;
- next batch.

If multiple platforms begin presenting bot/security challenges, stop the batch and review the workflow.

## 17. Failure handling

Record in `state/failures.csv` when:

- signup errors;
- unsupported email;
- duplicate account;
- account immediately suspended;
- domain no longer active;
- service retired;
- repeated technical failure.

Do not create repeated replacement accounts after a suspension without understanding the cause.

## 18. Completion definition

`completed` means:

- account ownership is known;
- public profile is accessible;
- core brand identity is correct;
- canonical website is added if the platform legitimately supports it;
- no unresolved security step exists;
- final URL is recorded.

Anything less must use a different status.
