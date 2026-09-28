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

_None yet._

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
