# Manual Action Queue

Use this file for blockers that require the authorized human owner.

Do **not** put passwords, recovery codes, TOTP secrets, identity-document numbers, card data, or other secrets here.

## Allowed blocker types

- CAPTCHA
- SMS verification
- identity/business verification
- ownership recovery
- payment approval
- naming decision
- ambiguous existing account
- Terms/automation review
- asset approval
- platform-specific legal/compliance review

## Open actions

### Bluesky — account discovery and signup entry point blocked

- Platform ID: bluesky
- Date: 2026-09-30
- Current status: manual_action_required
- URL: https://bsky.app/search
- Step reached: Public Bluesky Explore page; internal search returned “Search is currently unavailable when logged out.” The preferred handle profile URL did not resolve.
- What the platform requires: Sign-in to use internal search; the public signup entry point did not open in the connected browser session.
- What has already been completed: Checked the official links and account state; searched Bluesky public web results for the four requested brand terms with no matches; checked https://bsky.app/profile/nhamycali.bsky.social, which returned “Unable to resolve handle.” No account details or credentials were submitted.
- Exact human action required: Open Bluesky in a normal browser session, complete the in-platform searches for “NHÀ MỸ CALI”, “Nha My Cali”, “nhamycali”, and “nhamycali.com”, and confirm whether an official profile exists. If none exists, open the official signup flow and confirm whether `nhamycali.bsky.social` is available, then resume the pilot. Do not choose another handle.
- Does the account currently exist publicly?: Unknown; the preferred handle did not resolve, but logged-out search is unavailable.
- Safe to resume after action?: yes
- Notes: No CAPTCHA, OTP, or other security challenge was encountered. No DNS changes were made. Do not proceed to another platform.

## Entry template

```markdown
### [Platform] — [short blocker]

- Platform ID:
- Date:
- Current status:
- URL:
- Step reached:
- What the platform requires:
- What has already been completed:
- Exact human action required:
- Does the account currently exist publicly?:
- Safe to resume after action?: yes/no
- Notes:
```

## Resolution rule

When resolved:

1. update `state/accounts.csv`;
2. move the entry to **Resolved actions** below;
3. note the date and result;
4. never paste secrets used to resolve it.

## Resolved actions

_None yet._
