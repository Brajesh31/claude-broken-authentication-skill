# Claude Broken Authentication Skill

A security-testing skill for assessing authentication and session-management weaknesses in web applications. It covers password policy review, username enumeration, rate limiting, session security, MFA, and password-reset workflows.

## What It Covers

- **Authentication mapping:** Identify login, registration, logout, recovery, and token-based authentication flows.
- **Password policy review:** Evaluate password length, complexity, and weak-password protections.
- **Account enumeration:** Compare responses and timing for valid and invalid account inputs.
- **Rate limiting and lockout:** Assess protection against excessive authentication attempts.
- **Session management:** Review token entropy, cookie flags, session rotation, fixation, timeout, and logout invalidation.
- **MFA testing:** Examine OTP handling, enrollment, recovery, and bypass conditions.
- **Password recovery:** Review reset-token strength, expiration, reuse, and account binding.
- **Reporting:** Document findings, impact, and remediation recommendations.

## Authorization and Scope

Use this skill only for systems you own or are explicitly authorized to assess. Obtain written permission, define the test scope, use designated test accounts, and agree on rate limits and testing windows before conducting security tests.

Do not run credential stuffing, password spraying, brute-force attempts, MFA guessing, or session attacks against real users or third-party systems without explicit authorization and controlled test data. Prefer safe validation using dedicated accounts and non-destructive checks.

## Installation

Clone the repository into your Claude skills directory:

```bash
git clone https://github.com/Brajesh31/claude-broken-authentication-skill.git ~/.claude/skills/broken-authentication
```

## Using the Skill

Example request:

```text
Use the broken-authentication skill to review the session management
controls in my staging application using the test account I provide.
```

The skill provides an assessment workflow and report structure. Review [SKILL.md](SKILL.md) for testing phases, session cookie flags, common findings, constraints, and troubleshooting.

## Assessment Workflow

1. Confirm written authorization and scope.
2. Map authentication and account recovery flows.
3. Review password policy and account enumeration behavior.
4. Assess rate limiting and lockout using controlled test accounts.
5. Inspect session token handling, rotation, and expiration.
6. Review MFA enrollment, verification, and recovery.
7. Test password-reset tokens within the approved scope.
8. Record evidence, severity, and practical remediation steps.

## Reporting

A useful assessment report should include affected endpoint, test account, preconditions, reproducible evidence, impact, severity rationale, and remediation. Avoid recording live passwords, session tokens, or other secrets in the report.
