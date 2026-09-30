# NHÀ MỸ CALI — Execution Playbooks

These playbooks translate research and brand policy into concrete browser-execution instructions.

## Pilot order

Read:

1. `playbooks/PILOT_SEQUENCE.yaml`
2. the exact platform playbook
3. the relevant seed-content file, if publishing is part of that platform

## Current pilot

### Completed

- `BLUESKY.md` — completed and audited 2026-09-30.
- `SUBSTACK.md` — completed and audited 2026-09-30; publication at https://nhamycali.substack.com/.

### Browser-assisted, one at a time

1. `BLOGGER.md` — **current next pilot**

Routine reversible UI actions are autonomous. Codex should not ask before ordinary navigation, Save/Edit/Upload/Create/Publish actions, copy fitting, or other playbook-defined non-sensitive work.

Hard human checkpoints remain security/authorization events such as CAPTCHA/anti-bot, OTP/2FA/security verification, identity documents, payment/financial authorization, ambiguous ownership, Terms conflicts, and destructive irreversible actions.

### Existing-account audits

- `GRAVATAR_AUDIT.md`
- `LINKTREE_AUDIT.md`

### Manual-only platform

- `MEDIUM_MANUAL.md`

## Golden rule

A playbook is not permission to bypass a live platform control.

If the live UI differs in ordinary layout/control details, adapt and continue autonomously. If the live **policy/Terms** materially conflicts with the intended workflow, stop, verify the rule, update the repo, then continue only if appropriate.

## Secrets

Playbooks never contain:
- passwords;
- OTPs;
- private registration email;
- private Vietnam SMS number;
- recovery codes.

Those belong to the authorized runtime environment outside Git.

## Completion

After any platform:
1. verify its public page;
2. update `state/accounts.csv`;
3. update `brand/OFFICIAL_LINKS.yaml` only for verified official properties;
4. record blockers in `state/manual_actions.md`;
5. produce a batch report from `templates/platform_report.md`.
