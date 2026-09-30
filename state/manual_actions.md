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

### Substack — publication subdomain naming follow-up

- Platform ID: substack
- Date: 2026-09-30
- Current status: manual_action_required
- URL: https://helenhanguyen.substack.com/publish/settings#danger-zone
- Step reached: NHÀ MỸ CALI publication and welcome issue are public at the current Helen-based subdomain. The Change publication subdomain control was confirmed, but the current URL remained unchanged.
- What the platform requires: An owner review of Substack's publication subdomain setting to apply the preferred brand-consistent name or choose an approved fallback.
- What has already been completed: Owner created the account and completed email verification; Codex configured and publicly verified the brand publication, About, official website navigation link, and one web-only welcome issue. The Helen author profile remains separate.
- Exact human action required: Review the publication's Change publication subdomain control and select an available approved brand-consistent handle. Do not add random numbers. Tell Codex the final public URL if repo state should be updated.
- Does the account currently exist publicly?: Yes; https://helenhanguyen.substack.com/ and https://helenhanguyen.substack.com/p/chao-mung-en-voi-nha-my-cali
- Safe to resume after action?: yes
- Notes: User accepted the Publisher Agreement and Privacy Policy. No security challenge was bypassed; no secret was recorded; Stripe, paid subscriptions, and custom domain were not enabled.

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

### Substack — one-time email verification

- Platform ID: substack
- Date resolved: 2026-09-30
- Resolution: Owner completed the one-time email verification and created the account. Codex then completed the publication setup and public QA. A separate subdomain naming follow-up remains open above.

### Bluesky — account discovery and signup entry point blocked

- Platform ID: bluesky
- Date resolved: 2026-09-30
- Resolution: Owner created the account manually in the browser; profile is publicly reachable at https://bsky.app/profile/nhamycali.bsky.social. Email verification was later completed and is recorded in the resolved action below.

### Bluesky — registration email verification required before posting

- Platform ID: bluesky
- Date resolved: 2026-09-30
- Resolution: Owner confirmed email verification was completed. Codex published only seed post 1 and verified the post on the public profile at https://bsky.app/profile/nhamycali.bsky.social/post/3mwppsbyyn726. No DNS changes were made.
