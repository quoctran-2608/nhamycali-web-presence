# Blogger Pilot Report — 2026-09-30

## Status

The Blogger pilot is **in progress** and is not marked completed. The blog is live and core public content passed QA, but the approved brand header logo is not yet applied. Blogger currently shows its default theme background image. The Page Header gadget's Edit control did not open through browser automation, so one owner click is pending.

## Public properties verified

- Blog: https://nhamycali.blogspot.com/
- Blog title: **NHÀ MỸ CALI — Cẩm Nang Mua Nhà Mỹ**
- Description: **Kiến thức mua và bán nhà California dành cho người Việt, tập trung San Jose & Bay Area. Nội dung từ NHÀ MỸ CALI.**
- About page: https://nhamycali.blogspot.com/p/gioi-thieu.html
- First post: https://nhamycali.blogspot.com/2026/09/mua-nha-o-my-nen-bat-au-tu-au.html
- Canonical navigation item: **NHÀ MỸ CALI** → https://nhamycali.com/
- Public Blogger profile name: **NHÀ MỸ CALI**
- The About page accurately describes the brand, its California/San Jose–Bay Area focus, and Helen's canonical professional relationship.
- Exactly one approved first post is published. No bulk import or additional post was made.
- Public pages inspected did not show the registration email, private phone, or credentials.

## Remaining work

- Owner: click Edit beside the Page Header gadget in Blogger Layout so the editor opens.
- Codex: upload `assets/logo/nhamycali-logo-transparent.png`, save the header, and verify the logo on the public blog.
- Re-run full public identity QA. Until then, `state/accounts.csv` remains `manual_action_required` and `brand/OFFICIAL_LINKS.yaml` is unchanged.

## Cookie notice and integrations

Blogger's default EU cookie notice remains enabled. No third-party analytics, AdSense, Maps widget, or other external cookie-generating integration was added. The notice was not verified from an EU-geolocated public session.

## Signup and security

The owner completed Google's re-authentication/security verification directly in the browser. The blog was created under the authorized Google Account. No security control was bypassed. No DNS, `_atproto`, or custom-domain setting was changed; no paid feature was enabled.

## Repository state

- `state/accounts.csv`: Blogger recorded as `manual_action_required`; public URL and verified canonical navigation recorded.
- `state/manual_actions.md`: Google re-authentication moved to Resolved; Page Header editor click recorded as Open.
- `brand/OFFICIAL_LINKS.yaml`: unchanged pending approved-header QA.
- No registration email, password, OTP, phone number, or other runtime secret is included in this report.
