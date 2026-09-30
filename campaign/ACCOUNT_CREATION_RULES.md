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
- search for an existing NHÀ MỸ CALI account **unless the authorized owner has explicitly confirmed that no account exists on this exact platform and that confirmation is recorded in repo context**;
- confirm the exact domain is legitimate;
- confirm the platform is still active;
- confirm the platform purpose fits the campaign;
- note any current Terms/anti-automation restrictions that affect execution.

Do not proceed from a stale saved URL without confirming the domain.

## 2.1. Routine UI autonomy

For an approved platform/workflow, Codex should continue without asking for permission for routine, reversible actions.

Allowed autonomous actions include:
- clicking normal navigation and submit controls;
- retrying an unresponsive normal button up to 3 times;
- reloading or reopening the official page when needed;
- filling public profile fields from canonical data;
- adapting non-canonical copy to character limits;
- selecting reasonable non-sensitive categories/defaults;
- uploading approved assets;
- saving profile changes;
- publishing only the content explicitly authorized by the playbook/seed file;
- updating and committing non-secret state/report files.

If a normal UI button still cannot be activated after reasonable retries, request one manual click and resume from the resulting page. Do not restart the workflow or create a new blocker unless the issue truly prevents progress.

Hard blockers remain CAPTCHA/anti-bot, OTP/2FA/security verification, identity documents, payment authorization, ambiguous ownership, prohibited-workflow Terms conflicts, or destructive irreversible actions.

## 2.2. Standard terms acceptance

Standing owner authorization is recorded in `docs/OWNER_AUTHORIZATIONS.md`.

For approved free-account/profile/publication workflows, Codex may autonomously:
- tick standard Terms/Privacy/Community/Publisher Agreement checkboxes;
- click I agree / Accept / Agree and continue / equivalent controls;
- continue account/publication creation without asking the owner again solely for standard terms acceptance.

Do not stop for standard terms acceptance.

Stop only if the agreement requires:
- payment or paid-plan commitment;
- a factual/legal attestation not supported by canonical data or explicit owner instruction;
- identity/business documents;
- a workflow the live terms expressly prohibit.

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

Use the owner-approved runtime registration mailbox from `secrets/.env` according to `docs/REGISTRATION_POLICY.md`. Do not copy that private login value into public state files.

The automation must distinguish:

- `registration_email`: private login/account-purpose value;
- `public_contact_email`: approved public contact from canonical brand data.

Never expose a private registration/recovery email just because a form offers a public email field.

## 5. Passwords

Preferred long-term requirements:

- unique password per service;
- managed through an approved password manager or secure secret store;
- never written to CSV, Markdown, logs, screenshots, commits, issues, or PR comments.

### Temporary pilot exception

If `docs/REGISTRATION_POLICY.md` records an owner-approved temporary bootstrap password workflow, Codex may use `DEFAULT_ACCOUNT_PASSWORD` from local `secrets/.env` for the pilot.

The literal password must never be exposed or committed.

The repository should record only a non-secret reference such as:

`credential_managed_externally: true`

The owner may rotate pilot accounts to unique passwords after validation. Before broad scaling, return to unique-per-platform credentials.

## 6. Username selection

Preferred:

`nhamycali`

Fallback:

1. `nha_my_cali`
2. `nhamycali_realestate`
3. `nhamycalirealestate`

If all are unavailable, stop and request a human naming decision. Do not add arbitrary numbers.

## 7. Existing-account handling

### Owner confirmation

If the authorized owner explicitly confirms that NHÀ MỸ CALI does not have an account on a specific platform:

- record that confirmation with the platform and date;
- duplicate-discovery may be skipped for that platform;
- proceed to signup if the platform is otherwise approved;
- if signup reveals an existing-account or ownership conflict, stop immediately.

Do not require logged-in search, public API search, or additional discovery solely to prove absence after a clear owner confirmation.

### Existing account found

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

Follow `docs/REGISTRATION_POLICY.md`.

Current precedence is:
1. owner-approved Vietnam mobile from runtime secrets;
2. owner-approved U.S. business phone as fallback only when the platform does not accept Vietnam numbers.

Do not use:
- temporary SMS services;
- rented verification numbers;
- numbers not controlled by the authorized brand owner.

OTP entry is a human-action step. Never store OTP values.

If SMS is mandatory and no approved runtime number is configured:
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

Codex may rewrite or shorten non-canonical profile copy to fit a live platform's field limits without asking again, provided the meaning and canonical facts remain intact.

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
