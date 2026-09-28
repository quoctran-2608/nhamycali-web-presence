# NHÀ MỸ CALI — Approved Brand Assets

This directory contains the **approved visual source set** Codex/browser automation may use for NHÀ MỸ CALI public profiles.

Approval and technical metadata live in:

- `assets/ASSET_MANIFEST.yaml`
- `assets/PLATFORM_ASSET_POLICY.yaml`

Codex must not use an asset unless `approved_public_use: true`.

---

## 1. Canonical first-wave assets

### Brand avatar

`assets/avatar/nhamycali-avatar-square.png`

- Source filename: `avatar.png`
- 550 × 550
- PNG / RGBA / transparent outside the circular mark
- Contains:
  - NHÀ MỸ CALI house/star identity
  - “Bay Area Dream Home”
- **Default image for NHÀ MỸ CALI brand accounts.**

Use for:
- social/profile avatars;
- publication icons;
- public brand profiles.

Do not use it as Helen's personal portrait.

---

### Full transparent logo

`assets/logo/nhamycali-logo-transparent.png`

- Source filename: `logo.png`
- 550 × 550
- PNG / RGBA / transparent
- Contains the NHÀ MỸ CALI house/star symbol and wordmark.

Use for:
- headers;
- full-logo fields;
- transparent placements;
- website/resource layouts where the wordmark stays legible.

Avoid using it as the default tiny circular avatar because the full wordmark can become difficult to read.

---

### Helen Hà Nguyễn professional portrait

`assets/helen/helen-ha-nguyen-headshot.png`

- Source filename: `Helen_Ha_Nguyen.png`
- 941 × 1672
- PNG
- Official user-supplied professional portrait.

Use for:
- Helen author profiles;
- Helen Realtor/professional bio pages;
- platforms explicitly representing Helen as a person.

Do **not** automatically replace a NHÀ MỸ CALI brand avatar with Helen's portrait.

Never generate or substitute a fake Helen face.

---

### Official supplied banner

`assets/cover/nhamycali-cover-official.png`

- Source filename: `banner.png`
- 851 × 315
- Approximate aspect ratio: 2.70:1
- PNG
- Contains:
  - Coldwell Banker Realty co-branding;
  - NHÀ MỸ CALI;
  - “Ngôi Nhà Mỹ Mơ Ước Cho Người Việt”;
  - “Kênh bất động sản đáng tin cậy tại Bay Area, California”;
  - “Giúp người Việt an tâm mua nhà Mỹ”;
  - phone;
  - website;
  - Bay Area/San Francisco waterfront visual.

This is an **official supplied banner**, but it is not a universal high-resolution master.

Use only when:
- the target aspect ratio is compatible;
- the text and logos remain readable;
- no destructive crop is required.

Do not:
- significantly upscale it;
- crop out the Coldwell Banker Realty mark;
- crop out contact information or brand text;
- extract the Coldwell Banker Realty logo as a standalone asset.

---

## 2. Brand-vs-person identity rule

This distinction is mandatory.

### NHÀ MỸ CALI brand account

Default:

`assets/avatar/nhamycali-avatar-square.png`

### Helen Hà Nguyễn individual professional/author account

Default:

`assets/helen/helen-ha-nguyen-headshot.png`

### Ambiguous platform

Stop and decide identity before publishing.

Examples where this matters:
- About.me
- Medium
- Substack
- Gravatar when the underlying email/person identity is unclear.

See `assets/PLATFORM_ASSET_POLICY.yaml`.

---

## 3. Exact source preservation

The four files above were committed from the exact files supplied by the project owner on 2026-09-28.

The manifest records:
- original filename;
- byte size;
- dimensions;
- SHA-256;
- Git blob SHA;
- transparency;
- approval state.

This lets future agents confirm they are using the intended asset rather than a scraped or regenerated copy.

---

## 4. Optional assets still useful later

The first-wave account pilot does **not** require these, but they would improve future platform adaptation:

- official SVG/vector logo;
- horizontal logo;
- official light/dark logo variants;
- higher-resolution banner master;
- platform-specific cover derivatives;
- official color HEX values;
- official font names;
- Canva/source templates;
- original Bay Area/property photography;
- current approved Coldwell Banker co-brand source material if separately licensed/authorized.

Do not infer official font or HEX values from screenshots when a source file may exist.

---

## 5. Creating derivatives later

When a platform requires a different size or crop:

1. preserve the original canonical asset;
2. create a separate derivative file;
3. never overwrite the source;
4. keep important text/logo inside the platform safe area;
5. preview circular/square/cover crops;
6. add the derivative to `ASSET_MANIFEST.yaml`;
7. mark it approved before Codex uses it.

Recommended directory pattern:

```text
assets/
├── avatar/
│   ├── nhamycali-avatar-square.png
│   └── derived/
├── cover/
│   ├── nhamycali-cover-official.png
│   └── derived/
├── helen/
│   ├── helen-ha-nguyen-headshot.png
│   └── derived/
└── logo/
    ├── nhamycali-logo-transparent.png
    └── derived/
```

---

## 6. Sensitive/non-public material

Never commit here:

- driver license;
- passport;
- SSN;
- bank statements;
- client transaction documents;
- private contracts;
- card images;
- recovery codes;
- login QR codes;
- authentication screenshots;
- MLS credentials;
- unlicensed third-party photography.

Identity/business-verification documents, if a platform later requires them, must be handled outside Git.

---

## 7. Image-generation rule

Do not generate a replacement Helen portrait.

Generated decorative real-estate visuals may only be used after explicit approval and must never be represented as photographs of a real listing.

---

## 8. Current status

**First-wave visual asset requirement: complete as of 2026-09-28.**

Remaining pre-pilot work is primarily:
- registration/recovery workflow;
- existing-account audit;
- live platform research.
