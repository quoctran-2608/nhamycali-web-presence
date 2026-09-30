# Blogger Pilot Playbook

Research snapshot: 2026-09-28  
Platform: https://www.blogger.com/  
Mode: **autonomous routine browser through an authorized Google Account, with hard security/authorization checkpoints**

## 1. Purpose

Blogger may serve as a supporting educational publication for NHÀ MỸ CALI.

It must not become:
- a clone of nhamycali.com;
- a doorway site;
- a collection of thin pages built only to point at the main website.

## 1.1. Autonomous execution rule

Proceed without asking for permission for ordinary reversible Blogger actions:
- opening dashboard/settings/editor;
- clicking New blog/Next/Save/Publish/Pages/Layout/Theme and equivalent controls;
- retrying an unresponsive normal control up to 3 times;
- filling title, description, About, navigation and other public fields from canonical data;
- choosing reasonable non-sensitive Blogger defaults;
- uploading approved logo/avatar assets where the UI supports them;
- formatting and publishing the one approved first post;
- public QA;
- state/report updates and commit.

If the browser cannot activate a normal button after reasonable retries, ask for one manual click only and continue from the resulting page.

Stop only for hard blockers: Google security challenge/OTP/CAPTCHA, ambiguous ownership, identity/business verification, payment, Terms conflict, unsupported factual claim, or destructive irreversible action.

## 2. Preflight

After authorized Google login:

1. Open Blogger dashboard.
2. Inspect the blog selector.
3. Search for any existing NHÀ MỸ CALI/Nha My Cali blog owned by the account.
4. Also check the candidate Blogspot address before creation when practical.
5. If a strong likely existing official blog is found:
   - do not create another;
   - record public URL;
   - audit it first.

Do not loop on absence-proof. If the authorized Blogger dashboard shows no NHÀ MỸ CALI blog and creation proceeds without an ownership conflict, continue with the pilot.

## 3. Blog identity

Recommended blog title:

**NHÀ MỸ CALI — Cẩm Nang Mua Nhà Mỹ**

Why this is preferred over merely “NHÀ MỸ CALI”:
- gives the Blogger property a distinct educational job;
- reduces the chance it looks like a duplicate microsite;
- stays aligned with the main brand.

Description:

> **Kiến thức mua và bán nhà California dành cho người Việt, tập trung San Jose & Bay Area. Nội dung từ NHÀ MỸ CALI.**

## 4. Blogspot address

First candidate:

**nhamycali.blogspot.com**

Availability must be checked live.

If unavailable:
- do not add random numbers;
- try clean brand-consistent descriptive alternatives derived from the approved title, such as `nhamycalicam nang` only if the platform syntax permits a clean ASCII slug;
- prefer the shortest clear alternative;
- stop only if no clean approved-style alternative is available.

Do not create confusing or spammy numeric variants.

## 5. Assets

Header/full logo where appropriate:
- `assets/logo/nhamycali-logo-transparent.png`

Brand avatar/profile imagery:
- `assets/avatar/nhamycali-avatar-square.png`

Do not automatically use Helen's headshot for the blog brand.

## 6. Required static pages/navigation

Create only useful items.

### Giới thiệu

Use adapted copy from:
- `brand/COPY_LIBRARY.md`

Must clearly state:
- NHÀ MỸ CALI serves Vietnamese audiences interested in California real estate;
- focus on San Jose/Bay Area;
- Helen relationship wording must match `BRAND_ENTITY.yaml`;
- canonical website.

### Website chính

Blogger officially allows an external link item in the Page List.

Create a navigation item:

- label: **NHÀ MỸ CALI**
- URL: **https://nhamycali.com/**

This is a normal navigation link, not a keyword-stuffed anchor.

### Contact

Optional during pilot.

If created, use only approved public contact from `BRAND_ENTITY.yaml`.

Do not expose the registration Gmail.

## 7. First post

Use:
`content/seed/BLOGGER_FIRST_POST.md`

The article must provide independent educational value.

Do not publish:
> “Visit nhamycali.com for real estate.”

as a standalone post.

## 8. Duplicate-content rule

For future posts:

Preferred formats:
- original article;
- substantial adaptation;
- condensed checklist;
- different case/example;
- excerpt plus useful summary.

Do not automatically republish entire nhamycali.com articles verbatim.

## 9. Theme/layout

Keep pilot simple.

Priorities:
- readability;
- mobile compatibility;
- clear brand name;
- clear navigation;
- no excessive widgets;
- no artificial ad clutter.

Do not spend pilot time recreating nhamycali.com visually.

## 10. Google-account privacy

Blogger uses the authorized Google Account, but the public blog must not accidentally expose:

- private registration email;
- unrelated Google profile identity;
- unrelated personal photo;
- private phone.

Preview public pages while logged out where possible.

If Blogger forces an unwanted public Google/Blogger profile identity:
- stop and resolve before publishing.

## 11. Public QA

Verify:

- blog is publicly accessible;
- title correct;
- Blogspot URL exact;
- About/Giới thiệu accurate;
- external navigation item points to `https://nhamycali.com/`;
- approved logo/avatar display correctly;
- first post has value independent of backlink;
- no private registration data visible;
- no copied unsupported claims.

## 12. State update

Update `state/accounts.csv`:

- username if applicable;
- public blog URL;
- website_added = true only after checking external canonical link;
- profile_verified = true only after logged-out/public verification;
- notes with final Blogspot address.

If this becomes a stable official property, add it to `brand/OFFICIAL_LINKS.yaml` after verification.

## 13. Stop conditions

Stop only for:
- a strong likely existing official Blogger property with uncertain ownership;
- Google account security challenge/OTP/CAPTCHA;
- identity/business verification;
- accidental public exposure of private account information that cannot be resolved safely;
- payment or paid custom-domain authorization;
- Terms/policy conflict;
- unsupported factual claim;
- destructive irreversible action.

Ordinary Blogger UI changes, layout differences, clean slug fallback selection, theme choice, profile/page creation, navigation setup and publishing the approved first post are not stop conditions.

## 14. Success definition

The Blogger pilot succeeds only if it becomes a **useful educational satellite publication** with a stable branded identity and a natural link to the owned NHÀ MỸ CALI website.
