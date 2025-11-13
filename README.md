# tuxcare-poc

## Dependabot Security Monitoring

This repository is configured with Dependabot to monitor Java dependencies in `pom.xml` for security vulnerabilities.

### Configuration

The Dependabot configuration (`.github/dependabot.yml`) is set up to:
- ✅ Scan Maven dependencies daily
- ✅ Alert about security vulnerabilities
- ✅ **NOT** create automatic version update PRs (`open-pull-requests-limit: 0`)
- ✅ Only generate security alerts visible in GitHub Security tab

### How to View Security Alerts

1. Navigate to the **Security** tab in this GitHub repository
2. Click on **Dependabot alerts** in the left sidebar
3. View all detected CVEs and vulnerabilities in your dependencies

### How It Works

- Dependabot runs daily checks against the `pom.xml` file
- When vulnerabilities are found, they appear in the Security tab
- You receive notifications (if enabled) about new vulnerabilities
- **No automatic PRs are created** - you control when and how to update dependencies
- You can review CVE details, severity, and affected versions

### Example Dependencies

The sample `pom.xml` includes common dependencies:
- Spring Boot 2.6.1
- Jackson Databind 2.13.0
- Log4j2 2.14.1 (intentionally older version with known CVEs for testing)
- JUnit 4.13.2

### Managing Vulnerabilities

When Dependabot detects a vulnerability:

1. Review the alert details in the Security tab
2. Check the CVE information and severity
3. Decide if/when to upgrade based on your security policy
4. Manually update the version in `pom.xml` when ready
5. Dependabot will automatically close the alert once fixed

### Benefits

- 🔒 Stay informed about security issues
- 🎯 No noise from non-security version updates
- 📊 Centralized security dashboard
- ⚡ Daily automated scanning
- 📧 Optional email notifications