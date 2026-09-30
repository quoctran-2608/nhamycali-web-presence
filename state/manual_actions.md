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

### Blogger — Page Header editor needs one owner click

- Platform ID: blogger
- Date: 2026-09-30
- Current status: manual_action_required
- URL: https://www.blogger.com/blog/layout/5616237818585011709
- Step reached: Blogger blog is public and the Layout canvas is open. Browser control could not activate the Page Header gadget's Edit control after normal retries.
- What the platform requires: No platform security action is pending. One ordinary browser click is needed to open the Header gadget editor.
- What has already been completed: Owner completed Google's security re-authentication. The blog, About page, one approved post, title, description, and canonical website navigation are public and verified. The default Blogger theme image remains in the header; the approved logo has not been uploaded.
- Exact human action required: In Blogger Layout, click the pencil/Edit icon beside the “NHÀ MỸ CALI — Cẩm Nang Mua …” Page Header gadget, then tell Codex when the editor opens. Codex can then upload the approved logo and finish public QA.
- Does the account currently exist publicly?: Yes; https://nhamycali.blogspot.com/
- Safe to resume after action?: yes
- Notes: The Blogger pilot remains incomplete. Do not mark the account completed or add it to canonical official links until the approved header identity is verified. No private account value was written to repo state.

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

### Blogger — Google account re-authentication

- Platform ID: blogger
- Date resolved: 2026-09-30
- Resolution: Owner completed Google's verification in the browser. Blogger dashboard access resumed; the blog was created and public setup continued. No security control was bypassed.

### Substack — publication subdomain naming follow-up

- Platform ID: substack
- Date resolved: 2026-09-30
- Resolution: Owner successfully changed the publication subdomain to https://nhamycali.substack.com/. The canonical repository state was updated and no further Substack subdomain action is required.


### Substack — one-time email verification

- Platform ID: substack
- Date resolved: 2026-09-30
- Resolution: Owner completed the one-time email verification and created the account. Codex then completed the publication setup and public QA. The later subdomain naming follow-up was also resolved on 2026-09-30.

### Bluesky — account discovery and signup entry point blocked

- Platform ID: bluesky
- Date resolved: 2026-09-30
- Resolution: Owner created the account manually in the browser; profile is publicly reachable at https://bsky.app/profile/nhamycali.bsky.social. Email verification was later completed and is recorded in the resolved action below.

### Bluesky — registration email verification required before posting

- Platform ID: bluesky
- Date resolved: 2026-09-30
- Resolution: Owner confirmed email verification was completed. Codex published only seed post 1 and verified the post on the public profile at https://bsky.app/profile/nhamycali.bsky.social/post/3mwppsbyyn726. No DNS changes were made.
