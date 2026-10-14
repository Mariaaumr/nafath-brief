
Version: NAFATH-V3

Track: Cybersecurity

## Overview
A trustworthy public-service AI assistant depends on six connected IT fields. Software versioning helps teams manage API changes and maintain compatibility with the mobile application. Retrieval-Augmented Generation (RAG) can provide answers based on current government service documents, reducing reliance on outdated information. Mobile security protects communication between the app and its backend through secure connections. IPv6 supports a much larger address space as the number of connected devices grows. Cybersecurity controls help protect the assistant against prompt injection and unauthorized access to sensitive systems. Data protection practices help ensure that chat logs are stored and handled responsibly. These fields must work together because accurate answers alone do not guarantee a safe service. The assistant also needs secure communication, controlled access, and appropriate privacy safeguards. The key cybersecurity concern in this project is prompt injection and how it can manipulate an AI assistant through user input or untrusted external content. This project also reflects my interest in Cybersecurity, particularly in building secure, reliable, and privacy-aware digital services for government applications.
## Software
Semantic Versioning uses MAJOR.MINOR.PATCH numbers for public APIs. Increase MAJOR when making incompatible API changes, MINOR when adding functionality in a backward-compatible way, and PATCH when making backward-compatible bug fixes. For the government assistant, this helps the mobile team plan integrations and upgrades. Teams should document API changes and avoid treating every internal code change as a reason to increase the MAJOR version.

Resource: Semantic Versioning 2.0.0 - https://semver.org/spec/v2.0.0.html
## AI
Retrieval-Augmented Generation (RAG) retrieves relevant information from an external knowledge source and provides it to a language model when generating an answer. The assistant could retrieve current government service rules rather than relying only on information learned during training. This can improve factual accuracy and make answers easier to verify, especially when documents are updated. However, RAG does not guarantee correctness: retrieval quality, source quality, and the model's use of evidence still need evaluation.

Resource: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks - https://arxiv.org/abs/2005.11401
## Mobile
Apple's App Transport Security (ATS) requires network connections made through its standard URL-loading system to meet security requirements, including appropriate TLS protection. In general, a plain HTTP endpoint does not meet ATS requirements and the connection is blocked. The assistant's backend should therefore use HTTPS with a valid, properly configured TLS setup. Developers should avoid broad ATS exceptions; any necessary exception should be limited and justified.

Resource: Preventing Insecure Network Connections - https://developer.apple.com/documentation/security/preventing-insecure-network-connections
## Networking
IPv4 uses 32-bit addresses, while IPv6 uses 128-bit addresses, providing a vastly larger address space. As more phones, sensors, servers, and other devices connect to public services, IPv6 helps address the limits of available IPv4 addresses. It also supports modern network deployment, although migration and interoperability require planning. The government service should ensure that its infrastructure, hosting provider, and security controls support the IP versions it needs.

Resource: RFC 8200: Internet Protocol, Version 6 (IPv6) Specification - https://www.rfc-editor.org/rfc/rfc8200
## Cybersecurity
Prompt injection is an attack that attempts to manipulate an AI model through instructions embedded in input. Direct injection comes from a user's prompt; indirect injection comes from untrusted content, such as a webpage or document the assistant processes. Two mitigations are least-privilege access, which limits the assistant's permissions, and human approval before sensitive actions. Input separation and testing can also help, but no single prompt design reliably prevents every attack.

Resource: LLM01: Prompt Injection - https://genai.owasp.org/llmrisk2023-24/llm01-24-prompt-injection/
## Data
Anonymization removes identifying information so that a person can no longer reasonably be identified from the data, considering available means. Pseudonymization replaces direct identifiers with codes or other values, but additional information may allow the data to be linked back to a person. Under the GDPR, properly anonymized information falls outside its personal-data scope, whereas pseudonymized information remains personal data. Chat logs should also be minimized, access-controlled, and retained only as long as justified.

Resource: General Data Protection Regulation (GDPR), Recital 26 and Article 4(5) - https://eur-lex.europa.eu/eli/reg/2016/679/oj
## Misconception in My Track
A common misconception is that a strong system prompt or a keyword filter can completely prevent prompt injection. In reality, attackers may place malicious instructions in direct messages or external content that the assistant retrieves or reads. OWASP explains that prevention within the language model alone is not foolproof. The application must also restrict permissions, separate untrusted content, and require human approval for sensitive actions. The OWASP section titled “LLM01: Prompt Injection” describes these risks and mitigations.
## Open Question
How effectively can the assistant detect indirect prompt injection hidden in official-looking service documents, while still answering citizens' legitimate questions accurately?
