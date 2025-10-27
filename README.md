# CS 305 - Software Security

Nicholas Harris

This is my work from CS 305 where I added security features to a financial services app.

---

## The Project

**Client:** Artemis Financial - they needed secure communication and file verification for their web app.

**What I did:** Found security vulnerabilities and added SHA-256 checksums plus HTTPS encryption to protect client data.

---

## What I Did Well

I used defense-in-depth (multiple security layers):
- Converted HTTP to HTTPS with SSL/TLS
- Added SHA-256 checksums for file verification  
- Integrated OWASP Dependency Check for vulnerability scanning

**Why security matters:** Breaches cost millions, destroy trust, and create legal problems. Way cheaper to build it in from the start than fix it later.

---

## Challenges

**SSL certificates were harder than expected.** Figuring out keystores, certificate formats, and Spring Boot config took some trial and error. Browser warnings about self-signed certs were confusing at first too.

**OWASP Dependency Check was helpful.** Seeing how security scanning works in Maven was cool - it runs automatically as part of the build instead of being separate.

---

## Security Stuff I Added

**Layers:**
1. HTTPS/TLS - SSL encryption, HTTPS-only
2. SHA-256 Checksums - verifies data integrity
3. Secure API - minimal endpoints, good error handling
4. Automated Scanning - OWASP in build pipeline

**Testing:**
- Functional testing (made sure it compiled and ran)
- Security testing (ran dependency check, no new vulnerabilities)
- Code review (looked for common security issues)

**Future approach:**
Use OWASP Dependency Check, static analysis tools, manual code review for OWASP Top 10, and pen testing. Prioritize based on CVSS scores and impact.

---

## Tools & Practices

**Tools:**
- Java Keytool (SSL certificates)
- Maven OWASP Dependency Check
- Spring Boot Security
- Java Security API (SHA-256)

**What I learned:**
- Use strong crypto (SHA-256, not MD5/SHA-1)
- Handle UTF-8 encoding properly
- Error handling that doesn't expose system details
- Make things secure by default
- Document why you made security decisions

Security should be part of development from the start. This project showed me how automated security testing works in real apps.

---

## What This Shows

- Finding and fixing security vulnerabilities
- Working with cryptography (SHA-256, SSL/TLS)
- Integrating security into builds
- Following OWASP guidelines
- Writing technical documentation

Learning how OWASP Dependency Check works in Maven was really useful - automated security scanning is way better than checking manually.

---

## Tech

Java 17 • Spring Boot 3 • Maven • OWASP Dependency Check • SSL/TLS • SHA-256

---

*CS 305 - SNHU*
