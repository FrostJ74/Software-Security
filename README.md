# CS 305: Software Security

Projects and coursework for CS 305 Software Security, focused on developing secure code, implementing software security testing protocols, and applying encryption techniques to communicate securely.

## Course Overview

Through the analysis of advanced security concepts, this course teaches how to develop secure code that complies with security testing protocols. It also covers why and how to apply encryption technologies and techniques to communicate securely.

## Competencies

| Code | Competency |
|------|------------|
| CS-30412 | Analyze how advanced security concepts are applied to develop secure code |
| CS-30413 | Design and implement code that complies with software security testing protocols |
| CS-40414 | Write secure communications through the application of current encryption technologies and techniques |

## Repository Contents

| Folder | Description |
|--------|-------------|
| `Project-1/` | Artemis Financial Vulnerability Assessment Report: a review of the client's software for security weaknesses, with recommended mitigations. |
| `Project-2/` | Artemis Financial Practices for Secure Software Report: refactoring the application to fix vulnerabilities and verifying the result. |

This repository will continue to be updated as the course progresses.

## Topics Covered

- Secure coding practices
- Vulnerability analysis and mitigation
- Software security testing
- Encryption and secure communication

---

## Featured Artifact: Artemis Financial Practices for Secure Software Report

The completed **Artemis Financial Practices for Secure Software Report** is in the `Project-2/` folder. It shows my ability to assess vulnerabilities and code securely. The reflection below answers the journal prompts.

### Reflection

**Summarize your client, Artemis Financial, and its software requirements.**
Artemis Financial is a financial consulting company that helps clients with savings, retirement, investments, and insurance planning. Because it handles sensitive personal and financial data, it wanted its web-based application to be secure against modern threats. The company asked me to review its Java Spring Boot RESTful web application, find vulnerabilities in the code and its third-party dependencies, and recommend and apply fixes so customer data stays protected in transit and at rest.

**What did you do well when you found your client's software security vulnerabilities? Why is it important to code securely? What value does software security add to a company's overall well-being?**
I was systematic. I reviewed the code against secure-coding principles, ran a dependency scan, and ranked each finding by severity so the most dangerous issues were handled first. I also documented each finding in plain language, which made the report useful to both technical and non-technical readers. Coding securely matters because vulnerabilities are far cheaper to fix during development than after a breach. For a financial company, secure software protects customers, supports regulatory compliance, and preserves the trust the business depends on. A single incident can mean financial loss, legal trouble, and reputational damage, so security directly supports the company's long-term health.

**Which part of the vulnerability assessment was challenging or helpful to you?**
The most helpful part was reading the dependency scan results, because it showed how a project can inherit risk from libraries it never wrote. The most challenging part was sorting real, exploitable issues from low-risk findings and false positives, which required reading the CVE details and thinking about how the application actually uses each library.

**How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?**
I applied a defense-in-depth approach: encrypting communication with HTTPS/TLS, adding a checksum (hash) verification step to protect data integrity, and updating vulnerable dependencies to patched versions. In the future I would combine a threat-modeling approach such as STRIDE with static analysis, software composition analysis tools such as OWASP Dependency-Check, and the OWASP Top 10 as a checklist. I would weigh each risk by likelihood and impact to decide which mitigations to prioritize.

**How did you make certain the code and software application were functional and secure? After refactoring, how did you check whether you introduced new vulnerabilities?**
After each change I rebuilt and ran the application and tested the endpoints to confirm they still worked as expected. To confirm I hadn't introduced new problems, I re-ran the dependency scan and compared the results to the original baseline, and I reviewed my changes against secure-coding practices such as input validation and proper handling of certificates. Testing and re-scanning after every refactor kept security fixes from breaking functionality, and kept functionality changes from opening new holes.

**What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?**
Useful items included OWASP Dependency-Check, the OWASP Top 10 and secure-coding guidelines, the National Vulnerability Database (NVD/CVE) for researching findings, Maven for dependency management, and Git/GitHub for version control and documentation. The key practices were scanning early and often, keeping dependencies current, validating input, and documenting decisions as I went.

**What might you show future employers from this assignment?**
I would show the completed report as evidence that I can carry a project from vulnerability assessment through mitigation and verification. It demonstrates that I can analyze risk, apply encryption and integrity controls, work with real-world tooling, and communicate technical findings clearly to a client. It also shows that I treat security as part of the whole development process, not an afterthought.

---

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/FrostJ74/Software-Security.git
   ```

2. Open the folder for the project you want to review.
3. Follow the README or instructions inside that project folder to build and run the code.

## Author

**FrostJ74**

