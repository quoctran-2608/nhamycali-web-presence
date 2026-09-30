# Platform Pilot Report — Bluesky

## Batch

- Date: 2026-09-30
- Operator/agent: Account created manually by the owner in the browser; Codex completed profile configuration and public QA.
- Wave: Wave 1 pilot
- Goal: Configure and audit one official NHÀ MỸ CALI Bluesky profile, then publish only the first approved introduction post.

## Summary

- Platforms handled: Bluesky only
- Account created: 1, created manually by the owner in the browser
- Profile publicly verified: Yes
- Account status: `manual_action_required`; Bluesky requires email verification before posting
- Website link: `https://nhamycali.com/` appears as an auto-detected link in the bio; the profile editor exposed no separate website field
- Posts published: 0; the first seed post is pending owner email verification
- Manual action required: Complete Bluesky email verification; see `state/manual_actions.md`
- DNS or `_atproto` changes: None

## Profile QA

| Check | Result |
|---|---|
| Public profile URL | https://bsky.app/profile/nhamycali.bsky.social |
| Handle | `@nhamycali.bsky.social` |
| Display name | `NHÀ MỸ CALI` |
| Avatar | Matches approved `assets/avatar/nhamycali-avatar-square.png`; kept unchanged |
| Bio | `Bất động sản California dành cho người Việt | San Jose & Bay Area. Giúp bạn hiểu rõ hơn hành trình mua và bán nhà Mỹ. nhamycali.com` |
| Website/link | `nhamycali.com` is auto-detected as a profile link; no separate website field was available in Edit Profile |
| Registration details visible publicly | No registration email, phone number, or credential appeared on the public profile |
| Following count | 145 observed; no follows were changed |

Bluesky's official [Starter Packs announcement](https://bsky.social/about/blog/06-26-2024-starter-packs) says a pack can recommend up to 150 people. The observed 145 following is compatible with onboarding through a Starter Pack, but the count alone does not establish how these follows were added. No follows were removed or otherwise changed.

## Posting gate

Opening the composer showed that Bluesky requires email verification before an account can post or reply. The verification prompt was left untouched: no verification email was requested and no code or link was entered. The approved seed post 1 has therefore not been published. Resume only after the owner completes email verification, then publish seed post 1 once and verify it publicly.

## State changes

- `state/accounts.csv`: Bluesky records the owner-created handle and verified public profile; status remains `manual_action_required` because posting is gated on email verification.
- `brand/OFFICIAL_LINKS.yaml`: Added the publicly verified, owner-confirmed Bluesky profile URL.
- `state/manual_actions.md`: Resolved the previous discovery/signup blocker and opened a new email-verification action.
- No changes to DNS, `_atproto`, or the Bluesky handle domain.

## Audit statement

- No password, registration email, phone number, OTP, or credential was written to repository files or commit metadata.
- No security control was bypassed; the email-verification gate was not acted on.
- No post was published and no following changes were made.
- No platform other than Bluesky was handled.
