# Cybersecurity

## Overview

Cybersecurity helps protect a public-service AI assistant, its users, backend systems, and government service information from unauthorized access and malicious activity. Security must be considered throughout the design, development, deployment, and maintenance of the assistant.

## 1. Prompt Injection

Prompt injection occurs when malicious instructions are included in user input or untrusted external content to manipulate an AI system's behavior.

For example, an attacker might submit a request instructing the assistant to ignore its original instructions or attempt to reveal confidential information. Malicious instructions could also appear in retrieved documents used by a Retrieval-Augmented Generation (RAG) system.

Prompt injection can influence model behavior, but its impact depends on the system's architecture, available tools, permissions, and security controls.

## 2. Unauthorized Access

Unauthorized access occurs when a person or system accesses information or functions without appropriate permission. In a government-service assistant, this could expose sensitive information or allow unauthorized actions against backend services.

Access should be granted according to the user's identity, role, and the specific resources required.

## 3. Data Protection and Privacy

Chat logs and user requests may contain personal or sensitive information. The system should collect only the information necessary for its purpose and protect stored and transmitted data.

Recommended practices include:
- Encrypting sensitive data in transit and at rest.
- Restricting access to chat logs.
- Establishing appropriate retention and deletion policies.
- Avoiding unnecessary collection of personal information.
- Redacting sensitive information from application logs where appropriate.

## 4. Security Controls

The following controls can help reduce cybersecurity risks:

- **Input validation:** Validate input formats and enforce appropriate size and content limits.
- **Access control:** Apply least privilege and verify permissions on the server.
- **Instruction and data separation:** Treat user prompts and retrieved documents as untrusted content rather than trusted system instructions.
- **Tool restrictions:** Limit the assistant's tools and permissions to those required for its intended functions.
- **Output validation:** Check generated responses and validate any proposed actions before execution.
- **Human approval:** Require appropriate authorization for sensitive or high-impact actions.
- **Monitoring:** Record relevant security events and investigate suspicious activity.
- **Security testing:** Test for prompt injection, data leakage, broken access controls, and other application vulnerabilities.

No single control can eliminate all prompt-injection risks. Multiple layers of protection are needed.

## 5. Incident Response

If suspicious activity is detected, the organization should follow an established incident-response process:

1. Identify and assess the potential incident.
2. Contain the affected system or restrict the relevant access.
3. Investigate the cause and determine the potential impact.
4. Remove the underlying weakness and restore normal operation safely.
5. Document the incident and improve preventive controls.

## Conclusion

Cybersecurity is essential to building a trustworthy public-service AI assistant. Prompt injection, unauthorized access, and privacy risks should be addressed through layered security controls, least-privilege access, careful handling of untrusted content, and continuous testing and monitoring.

## References

1. OWASP Foundation. *LLM01:2025 Prompt Injection.* https://genai.owasp.org/llmrisk/llm01-prompt-injection/
2. National Institute of Standards and Technology (NIST). *Artificial Intelligence Risk Management Framework (AI RMF 1.0).* https://doi.org/10.6028/NIST.AI.100-1
3. National Institute of Standards and Technology (NIST). *Cybersecurity Framework (CSF) 2.0.* https://doi.org/10.6028/NIST.CSWP.29
