# SaaS CTO Security Checklist

**Source:** https://web.archive.org/web/20230324072622/https://www.goldfiglabs.com/guide/saas-cto-security-checklist/
**Section:** Technologies

---

## Key Insights

**Employee Security**
- Require 2FA universally - passwords alone insufficient protection
- Hardware-based 2FA (Yubikeys) more secure than phone-based
- Computer locking prevents physical access exploitation in <5 minutes
- Never share user accounts - prevents access tracking and compromises offboarding
- Encrypt all laptops/phones with remote wipe capability
- Use centralized account management with SSO to automate provisioning/deprovisioning
- Hire first security engineer only when engineering team bought-in but overwhelmed

**Code Security**  
- Never commit secrets to code - use separate secret management (AWS Secrets Manager, etc.)
- Never build custom cryptography - use established libraries like NaCl
- Integrate SAST tools in CI/CD but expect high false positive rates
- Run team security testing sessions targeting account isolation, token uniqueness, unauthenticated paths
- Automate security scanning in SDLC to avoid velocity impact

**Application Security**
- WAFs outdated - use Runtime Application Self-Protection (RASP) closer to application
- Track all dependencies for known vulnerabilities (major OWASP risk)
- Run applications unprivileged to limit attack impact
- FaaS requires centralized code repos, minimal privileges, CI deployment

**Infrastructure Security**
- Test backup restoration frequently - backup without restore verification is useless
- Enable automatic container image security scanning with dashboard alerts
- Monitor network for unexpected exposed services using scanners
- Isolate internal services behind bastion hosts/VPNs with IP restrictions
- Watch metrics for unusual patterns indicating compromise (bandwidth, CPU, memory)

**Company Security**
- Create asset inventory - can't secure what you don't know exists
- Separate guest WiFi, rotate password every 2 months
- Domain protection: transfer locks, different domain for admin email, security-focused registrar
- Bug bounty programs require internal security expertise to evaluate reports

## Bottom Line
Security scales through automation and cultural integration rather than adding more manual processes that slow development velocity.