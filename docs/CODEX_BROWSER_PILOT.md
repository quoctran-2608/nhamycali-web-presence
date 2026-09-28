# Codex Browser Pilot — Start Here

This is the entry point to give Codex when the browser environment is ready.

## First live task

**Run only the Bluesky pilot. Do not proceed to Substack or Blogger in the same run.**

Required reading:

1. `AGENTS.md`
2. `brand/BRAND_ENTITY.yaml`
3. `brand/OFFICIAL_LINKS.yaml`
4. `assets/ASSET_MANIFEST.yaml`
5. `assets/PLATFORM_ASSET_POLICY.yaml`
6. `docs/REGISTRATION_POLICY.md`
7. `research/WAVE_1_DECISIONS.yaml`
8. `playbooks/PILOT_SEQUENCE.yaml`
9. `playbooks/BLUESKY.md`
10. `content/seed/BLUESKY_SEED.md`
11. `state/accounts.csv`
12. `state/manual_actions.md`

## Instruction to Codex

Use this task wording:

> Execute the NHÀ MỸ CALI Bluesky pilot exactly according to the repository rules and `playbooks/BLUESKY.md`. Before creating anything, search inside Bluesky for an existing official NHÀ MỸ CALI account. Create at most one account, only if no official account exists. Use approved brand assets and runtime secrets; never print or commit secrets. Stop for CAPTCHA, OTP, security challenge, payment, identity verification, ambiguous existing ownership, or any live-policy conflict. Do not change DNS unless I explicitly approve that step during the run. After the public profile is verified, update only the non-secret repository state and produce a platform report. Do not start another platform.

## Human preparation before running

The browser/runtime should have:

- legitimate access to the approved registration mailbox;
- the approved phone available if an OTP is required;
- a secure place to save a unique password outside Git;
- access to this repository;
- browser access to Bluesky.

No password, OTP or private verification number should be pasted into repository files.

## Expected human checkpoints

Codex should pause when:
- email verification needs user action;
- SMS/OTP arrives;
- CAPTCHA appears;
- a handle conflict requires a decision;
- DNS verification is proposed.

For the first pilot, **do not authorize DNS automatically**. First establish and audit the basic account.

## Expected output after the run

Codex should report:

- whether an existing account was found;
- whether a new account was created;
- public URL;
- final handle;
- whether canonical website appears publicly;
- whether avatar/bio passed QA;
- any security/manual blockers;
- exact state files updated;
- no secrets.

## After Bluesky

Review the result manually.

Only after the Bluesky audit is satisfactory should the project move to:

1. Substack
2. audit
3. Blogger

One platform at a time.
