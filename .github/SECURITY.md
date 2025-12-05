# Security Policy

## Supported Versions

We are committed to maintaining a secure project. Security vulnerabilities are taken very seriously. Please report any vulnerabilities you find to us.

We are currently supporting and actively monitoring the latest stable release of the `ContentFlow-Publish-And-Archive-Platform`.

## Reporting a Vulnerability

We appreciate your efforts to responsibly disclose your findings. We are following the best practices for vulnerability disclosure. To report a security vulnerability, please use the GitHub Security Advisory form or send an email to `security@example.com` (replace with a real security contact if available).

Please do not report security vulnerabilities through public GitHub issues.

When reporting a security issue, please include:

*   The vulnerability details (what it is, how to reproduce it).
*   The affected version of the project.
*   Your suggested remediation (if any).

We will review all reports and will respond to acknowledge your report within 48 hours. We will also endeavor to let you know of the progress towards a fix and the release of a patch.

## Security Best Practices

*   **Dependency Management:** All project dependencies are managed using `uv` and are regularly scanned for known vulnerabilities. We aim to keep dependencies up-to-date.
*   **Code Reviews:** All code changes undergo rigorous peer review processes before merging into the main branch, with a focus on security best practices.
*   **Automated Checks:** CI pipelines include automated security checks, including dependency vulnerability scanning and linting with Ruff, to catch potential issues early.
*   **Principle of Least Privilege:** The platform is designed to operate with the minimal necessary permissions.

*For more information on our development and security standards, please refer to the `AGENTS.md` file.*