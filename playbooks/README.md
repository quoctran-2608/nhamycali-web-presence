# NHÀ MỸ CALI — Execution Playbooks

These playbooks translate research and brand policy into concrete browser-execution instructions.

## Pilot order

Read:

1. `playbooks/PILOT_SEQUENCE.yaml`
2. the exact platform playbook
3. the relevant seed-content file, if publishing is part of that platform

## Current pilot

### Browser-assisted, one at a time

1. `BLUESKY.md`
2. `SUBSTACK.md`
3. `BLOGGER.md`

Do not start platform 2 until platform 1 has been:
- publicly verified;
- recorded in state;
- audited for unexpected security/policy issues.

### Existing-account audits

- `GRAVATAR_AUDIT.md`
- `LINKTREE_AUDIT.md`

### Manual-only platform

- `MEDIUM_MANUAL.md`

## Golden rule

A playbook is not permission to bypass a live platform control.

If the live UI/policy differs from the research snapshot:
- stop;
- verify the current rule;
- update the repo;
- then continue.

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
