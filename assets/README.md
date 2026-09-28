# NHÀ MỸ CALI — Asset Registry

This directory will hold **approved brand-owned visual assets** used by Codex/browser automation.

At the moment, no production asset should be assumed to exist until a human uploads and approves it.

## 1. Required first-wave assets

Please provide the following source files if available.

### A. Primary logo — transparent

Preferred filename:

`assets/logo/nhamycali-logo-transparent.png`

Preferred source:
- PNG with transparent background;
- ideally at least 1600 px on the longest side;
- SVG is welcome as a master source if available.

Use:
- profile branding;
- page headers;
- social/public profiles where a full logo works.

### B. Square avatar/profile mark

Preferred filename:

`assets/avatar/nhamycali-avatar-square.png`

Preferred:
- 1:1;
- 1200 × 1200 px or larger;
- readable at small sizes;
- no tiny text that disappears at 64 px.

If the current NHÀ MỸ CALI logo is already designed for a circular avatar, send that exact official version.

### C. Helen Hà Nguyễn professional headshot

Preferred filename:

`assets/helen/helen-ha-nguyen-headshot.jpg`

Preferred:
- high-resolution;
- official/current;
- neutral or real-estate-appropriate background;
- permission to use across public profiles.

This is important because some platforms are better represented by a real professional/person than by the brand logo.

### D. Generic brand cover/banner

Preferred filename:

`assets/cover/nhamycali-cover-master.jpg`

Suggested master:
- 2560 × 1440 px or larger;
- logo/tagline within a central safe zone;
- no platform-specific UI baked into the master.

The master can later be resized/cropped per platform.

## 2. Helpful second-wave assets

If available:

- horizontal logo;
- monochrome/light logo;
- monochrome/dark logo;
- logo SVG;
- official Coldwell Banker co-brand asset currently approved for use;
- Helen full/half-body professional photo;
- original Bay Area / San Jose property photography;
- original Open House visual template;
- current YouTube/Facebook banner source files;
- brand color/font specification;
- brand icon set;
- Canva/exported social templates.

## 3. Do not upload here

Do not commit:

- driver license;
- passport;
- SSN;
- bank statement;
- real-estate transaction documents containing private client data;
- private contracts;
- credit-card images;
- recovery codes;
- login QR codes;
- authentication screenshots;
- unlicensed stock imagery.

Identity/business-verification documents, if ever required, must be handled outside Git.

## 4. Approval metadata

When assets are added, create/update a small registry in this file or a future `assets/ASSET_MANIFEST.yaml` with:

- filename;
- asset type;
- source;
- owner;
- approved public use: yes/no;
- date approved;
- notes.

Codex must use only assets marked approved.

## 5. Image-generation rule

Do not generate a fake Helen headshot or substitute a synthetic person.

Generated decorative real-estate visuals may only be used if explicitly approved for a specific purpose and must not be presented as photographs of a real listing.
