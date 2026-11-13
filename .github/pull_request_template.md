## What this changes

<!-- Plain-English summary. Requirement IDs (VEH-01, RNT-03, …) if any. -->

## Security checklist

Full checklist: Dev By Proxy `business/security-checklist.md`. Tick each box or write why it doesn't apply.

- [ ] I read the diff and Claude explained it in plain English
- [ ] `/security-review` run; findings fixed or explained below
- [ ] `/code-review` run
- [ ] `npm run build` passes
- [ ] No secrets in the diff (gitleaks pre-commit hook ran)
- [ ] No secret / service_role key in any `VITE_` variable
- [ ] Any new npm package is explained below (why it's needed, widely used, maintained)
- [ ] No real client personal data in code, seed files, screenshots or preview links

### Only if the database changed (`supabase/migrations/`)

- [ ] Every new table has RLS enabled **and** policies for each role, in the same migration
- [ ] Supabase dashboard → Advisors → Security Advisor shows no new warnings
- [ ] Tested as the lowest role: tried to read and edit data it shouldn't reach, and it was refused

## Notes

<!-- Review findings, new packages, anything skipped and why. -->
