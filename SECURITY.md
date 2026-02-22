# Security Policy

## Scope

This policy covers all repositories under the **venantvr-security** organization. These projects are **security research and educational tools**: static analyzers, penetration testing utilities, log analyzers, network scanners, and defensive security tools.

## Important Note

Many repositories in this organization contain **offensive security tools** built for educational purposes, authorized testing, and CTF challenges. Behaviors that are *by design* in these tools (e.g., a port scanner scanning ports, a backdoor demo establishing reverse shells) are **not** vulnerabilities — they are the intended functionality.

## Reporting a Vulnerability

If you discover a **genuine** security vulnerability, please report it responsibly:

1. **Do not open a public issue.** Security vulnerabilities must be reported privately.
2. Go to the affected repository's **Security** tab and click **"Report a vulnerability"** to create a private security advisory.
3. Include as much detail as possible: affected files, steps to reproduce, and potential impact.

## What We Consider Security Issues

- Hardcoded credentials, API keys, or private keys that should not be public
- Vulnerabilities in the tools themselves (e.g., command injection in a scanner's CLI parser)
- Insecure dependencies with known CVEs that affect the tool's own security
- Unintended data exfiltration or phone-home behavior
- Path traversal or arbitrary file access in tool inputs

## What Is NOT a Vulnerability

- Offensive capabilities that are the tool's documented purpose
- "Dangerous" functions used intentionally in security contexts (eval, exec, system calls)
- Test payloads, sample exploits, or deliberately vulnerable PHP/Python files in test directories

## Response

- Acknowledgment within **72 hours**
- Status update within **7 days**
- If confirmed, a fix will be prioritized and you will be credited (unless you prefer anonymity)

## Out of Scope

- Archived repositories
- Deliberately vulnerable sample files (e.g., `tests/php_samples/`)
