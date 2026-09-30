# Manual Action Queue

Use this file for blockers that require the authorized human owner.

Do **not** put passwords, recovery codes, TOTP secrets, identity-document numbers, card data, or other secrets here.

## Allowed blocker types

- CAPTCHA
- email verification
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

### Bluesky — registration email verification required before posting

- Platform ID: bluesky
- Date: 2026-09-30
- Current status: manual_action_required
- URL: https://bsky.app/profile/nhamycali.bsky.social
- Step reached: Owner-created account is public and the profile has been configured and verified. Bluesky requires email verification before allowing the first post; the verification dialog was left untouched.
- What the platform requires: Complete Bluesky's email verification from the owner's mailbox and account session.
- What has already been completed: Owner created the account manually in the browser. Codex set and publicly verified the display name, approved avatar, bio, and website link. Following count 145 was observed and left unchanged. No post was published; no DNS changes were made.
- Exact human action required: Verify the account email directly with Bluesky. Do not send the verification code or link to Codex. Resume after the account is verified to publish only seed post 1 and verify it.
- Does the account currently exist publicly?: Yes; public URL and handle are verified.
- Safe to resume after action?: yes
- Notes: Email verification gate encountered; no verification email was requested and no code/link was entered. Do not proceed to another platform.

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

### Bluesky — account discovery and signup entry point blocked

- Platform ID: bluesky
- Date resolved: 2026-09-30
- Resolution: Owner created the account manually in the browser; profile is publicly reachable at https://bsky.app/profile/nhamycali.bsky.social. The later email-verification gate is tracked as a separate open action above.
