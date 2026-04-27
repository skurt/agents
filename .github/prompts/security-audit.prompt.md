---
name: Security Audit
description: Run a security audit on a file, folder, or feature. Checks for OWASP Top 10 vulnerabilities, hardcoded secrets, missing input validation, and insecure patterns.
argument-hint: "File path or describe the feature to audit (e.g. 'src/auth/login.ts' or 'the user registration flow')"
agent: agent
tools: [read, search]
---

Perform a thorough security audit on the specified code or feature.

Check for:
1. **Injection flaws** — SQL, command, LDAP, XPath injection
2. **Broken authentication** — weak passwords, missing MFA, insecure session management
3. **XSS** — reflected, stored, and DOM-based cross-site scripting
4. **Insecure direct object references** — unauthorized access to resources by manipulating IDs
5. **Security misconfiguration** — default credentials, verbose error messages, exposed stack traces
6. **Sensitive data exposure** — hardcoded secrets, API keys, unencrypted PII
7. **Missing access controls** — unprotected routes, missing authorization checks
8. **CSRF** — missing anti-forgery tokens on state-changing requests
9. **Vulnerable dependencies** — flag any obviously outdated or risky packages
10. **Logging & monitoring gaps** — missing audit logs for sensitive operations

Output a prioritized findings report. For each issue provide:
- Severity: Critical / High / Medium / Low
- OWASP category
- File and approximate line
- What the problem is and why it matters
- A concrete recommended fix
