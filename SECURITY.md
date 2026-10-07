# Security policy

## Leaked credential (token, password, key)
1. **Revoke it immediately** at its source (GitHub → Settings → Developer settings / Applications, or the service that issued it).
   Deleting the commit is not enough: the secret must be considered public.
2. Notify an organization owner privately (GitHub direct message or e-mail, **not** a public issue).
3. Owners check the audit log (`Organization → Settings → Audit log`) and rotate anything derived from the secret.

## Vulnerability in our code or tooling
Report it privately to an organization owner with the repository, file and a short reproduction. Don't open a public issue.

## Prevention
- Every member enables two-factor authentication.
- Use `gh auth login` (stored by the GitHub CLI) instead of token files in a working tree.
- The `wow-dev` git hooks block token-shaped strings, secret files and client binaries at commit time. Don't bypass them with `--no-verify`.
