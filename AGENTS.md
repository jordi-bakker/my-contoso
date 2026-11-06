# AGENTS.md

## Agent skills

### Issue tracker

Issues live in GitHub Issues for `jordi-bakker/my-contoso` (via the `gh` CLI). See `docs/agents/issue-tracker.md`.

### Triage labels

Default vocabulary: `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context. See `docs/agents/domain.md`.

### Skill index

If a prompt starts with `/<name>` and that skill isn't loaded, read its `SKILL.md` from the table and follow it.

| Skill | SKILL.md | User-only |
|---|---|---|
| ask-matt | `.agents/skills/ask-matt/SKILL.md` | yes |
| grilling | `.agents/skills/grilling/SKILL.md` | no |
| grill-with-docs | `.agents/skills/grill-with-docs/SKILL.md` | yes |
| domain-modeling | `.agents/skills/domain-modeling/SKILL.md` | no |
| prototype | `.agents/skills/prototype/SKILL.md` | no |
| handoff | `.agents/skills/handoff/SKILL.md` | yes |
| to-spec | `.agents/skills/to-spec/SKILL.md` | yes |
| to-tickets | `.agents/skills/to-tickets/SKILL.md` | yes |
| implement | `.agents/skills/implement/SKILL.md` | yes |
| tdd | `.agents/skills/tdd/SKILL.md` | no |
| code-review | `.agents/skills/code-review/SKILL.md` | no |
| codebase-design | `.agents/skills/codebase-design/SKILL.md` | no |
| pr | `.agents/skills/pr/SKILL.md` | no |
| retro | `.agents/skills/retro/SKILL.md` | yes |
| writing-for-agents | `.agents/skills/writing-for-agents/SKILL.md` | no |
| diagnosing-bugs | `.agents/skills/diagnosing-bugs/SKILL.md` | no |
| research | `.agents/skills/research/SKILL.md` | no |
| wayfinder | `.agents/skills/wayfinder/SKILL.md` | yes |
| setup-matt-pocock-skills | `.agents/skills/setup-matt-pocock-skills/SKILL.md` | yes |
| karpathy-guidelines | `.agents/skills/karpathy-guidelines/SKILL.md` | no |
| accessibility | `.agents/skills/accessibility/SKILL.md` | no |
| impeccable | `.github/skills/impeccable/SKILL.md` | no |


## Working rules

- Always follow the `karpathy-guidelines` skill: think before coding, keep it simple, change only what's needed, and define success criteria, then verify them.
- The app runs at http://localhost:5174 (Vite `strictPort`). Parallel sessions check their work on port 5176 with `npm run dev -- --port 5176`.
- Build one vertical slice (one ticket) at a time. After each slice, run tests, type checking and the build, then check the page in the browser at 390px and 1280px wide. Finally, give the human a 3-5 step acceptance script. In interactive mode, wait for their approval before committing.
- Use Tailwind CSS only, with no other UI libraries. Follow PRODUCT.md and DESIGN.md when they exist.
- Don't add dependencies without asking first.
- Use synthetic data only. Never use real personal data.
- A customer may only ever see their own policies. When a change loads customer data or sends it to the browser, run the security-review agent before you give the acceptance script, and fix what it finds.
- Reviews and audits judge the work against its ticket. If a finding is already covered by another open ticket, list it with that ticket's number instead of fixing it.
- If a prompt starts with `/<name>` and that skill isn't loaded, read `.agents/skills/<name>/SKILL.md` or `.github/skills/<name>/SKILL.md` and follow it. Do not retry the app skill loader for repository-local skills.
- Never skip or work around the hooks in `.github/hooks/`, and change them only when the human asks. If the quality gate blocks a commit, fix what fails.