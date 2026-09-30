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
- Account status: `completed`; owner confirmed email verification and public profile/post QA passed
- Website link: `https://nhamycali.com/` appears as an auto-detected link in the bio; the profile editor exposed no separate website field
- Posts published: 1; seed post 1 only
- Manual action required: None; both earlier Bluesky blockers are resolved
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
| First post | https://bsky.app/profile/nhamycali.bsky.social/post/3mwppsbyyn726 |

Post text: `NHÀ MỸ CALI chia sẻ kiến thức bất động sản California dành cho người Việt — từ chuẩn bị tài chính, xem nhà đến những bước trong giao dịch. Trọng tâm: San Jose & Bay Area. https://nhamycali.com/`

Bluesky's official [Starter Packs announcement](https://bsky.social/about/blog/06-26-2024-starter-packs) says a pack can recommend up to 150 people. The observed 145 following is compatible with onboarding through a Starter Pack, but the count alone does not establish how these follows were added. No follows were removed or otherwise changed.

## Posting gate

The owner confirmed that account email verification had been completed. Codex opened the composer, published only seed post 1 from `content/seed/BLUESKY_SEED.md`, and reloaded the public profile. The refreshed profile shows 1 post, and the exact seed text and website link are visible at the public post URL above.

## State changes

- `state/accounts.csv`: Bluesky is `completed`; the owner-created handle, verified public profile, and verified seed post 1 are recorded.
- `brand/OFFICIAL_LINKS.yaml`: Added the publicly verified, owner-confirmed Bluesky profile URL.
- `state/manual_actions.md`: Resolved the previous discovery/signup blocker and the email-verification blocker.
- No changes to DNS, `_atproto`, or the Bluesky handle domain.

## Audit statement

- No password, registration email, phone number, OTP, or credential was written to repository files or commit metadata.
- No security control was bypassed; the owner completed email verification.
- Exactly one post was published; no following changes were made.
- No platform other than Bluesky was handled.
