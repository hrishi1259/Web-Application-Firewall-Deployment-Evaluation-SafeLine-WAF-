# Web Application Firewall Deployment & Evaluation (SafeLine WAF)

Deployment of the SafeLine Web Application Firewall in front of a containerized DVWA (Damn Vulnerable Web Application) instance, with before/after testing to validate attack mitigation.

## Objective
Evaluate how effectively a modern WAF detects and blocks common web attacks, and measure its impact on legitimate traffic (rate limiting / false positives).

## Scope
- **Protected application:** DVWA, containerized with Docker
- **Firewall under test:** SafeLine WAF
- **Environment:** Isolated Docker lab network

## Methodology
1. **Baseline testing** — confirm SQL injection succeeds against unprotected DVWA
2. **WAF deployment** — stand up SafeLine WAF as a reverse proxy in front of DVWA
3. **Protected testing** — repeat SQL injection attempts and confirm blocking
4. **Rate limiting validation** — test request throttling under abuse conditions

## Key Findings
- SQL injection payloads blocked after SafeLine WAF deployment
- Rate limiting successfully throttled high-frequency malicious requests

## Tools & Technologies
`SafeLine WAF` · `Docker` · `DVWA` · `SQL Injection Testing`

## Skills Demonstrated
WAF deployment and tuning, reverse-proxy security architecture, attack simulation, before/after control validation.

## Repository Structure
```
.
├── reports/
│   ├── SafeLine_WAF_Project.pdf   # Final report
│   └── SafeLine_WAF_Project.docx  # Editable source
├── LICENSE
└── README.md
```

## Disclaimer
This work was performed in an isolated, authorized lab environment for educational and professional development purposes only. Do not use these techniques against any system without explicit written authorization.

## License
Released under the [MIT License](./LICENSE).
