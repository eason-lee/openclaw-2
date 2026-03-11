# Errors

Command failures, exceptions, and unexpected behavior captured for later diagnosis.

**Areas**: frontend | backend | infra | tests | docs | config
**Statuses**: pending | in_progress | resolved | wont_fix | promoted

---

## [ERR-20260311-001] clawhub-install

**Logged**: 2026-03-11T12:28:45Z
**Priority**: medium
**Status**: pending
**Area**: docs

### Summary
`clawhub install` does not accept a full ClawHub URL as the package argument.

### Error
```text
Error: Invalid slug: https://clawhub.ai/pskoett/self-improving-agent
```

### Context
- Command attempted: `clawhub install https://clawhub.ai/pskoett/self-improving-agent`
- Working alternative: `clawhub install self-improving-agent`
- Observed while installing a skill from a shared ClawHub link

### Suggested Fix
When given a ClawHub URL, extract the skill slug first and pass the slug to `clawhub install`.

### Metadata
- Reproducible: yes
- Related Files: `skills/self-improving-agent/SKILL.md`

---
