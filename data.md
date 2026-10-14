# Data

## Overview

Data is essential to a trustworthy public-service AI assistant. The assistant may use government service documents, user questions, retrieved information, and operational logs to provide relevant responses and maintain service quality. These data sources should be managed carefully to support accuracy, privacy, security, and accountability.

## 1. Data Collection

The system should use authorized and reliable sources of government service information. Documents should be reviewed for accuracy, relevance, publication date, and authority before they are made available to the assistant.

Only collect user information that is necessary for the service's intended purpose. Data collection practices should follow applicable privacy requirements and organizational policies.

## 2. Data Quality

Poor-quality or outdated information can lead to incorrect answers. Data quality can be improved by:

- Checking the accuracy and completeness of source documents.
- Recording publication dates and document versions.
- Removing duplicate or obsolete documents.
- Reviewing conflicting information before publication.
- Updating the document collection when official guidance changes.

## 3. Retrieval-Augmented Generation (RAG)

Retrieval-Augmented Generation combines information retrieval with text generation. A RAG-based assistant retrieves relevant passages from a document collection and uses them as context when generating a response.

A typical workflow includes:

1. Collect authorized government service documents.
2. Extract and prepare the document text.
3. Split the text into suitable passages.
4. Index the passages for retrieval.
5. Retrieve relevant passages for a user's question.
6. Generate a response grounded in the retrieved context.
7. Provide source references when supported by the system.

RAG can help the assistant use current, relevant information, but it does not guarantee that every answer will be correct. Retrieval quality, document quality, and response validation remain important.

## 4. Data Security and Privacy

Chat logs, user questions, and retrieved records may contain sensitive information. Appropriate safeguards include:

- Encrypting sensitive data in transit and at rest.
- Restricting access according to job responsibilities.
- Defining data retention and deletion periods.
- Removing or masking unnecessary personal information in logs.
- Protecting backups and monitoring access to stored data.
- Preventing retrieved documents from granting unauthorized access to tools or systems.

## 5. Data Governance

Data governance establishes how information is collected, maintained, accessed, and used. For a public-service AI assistant, governance should define:

- Data ownership and responsibility.
- Approved sources and permitted uses.
- Access permissions and review procedures.
- Data quality requirements.
- Retention and deletion rules.
- Processes for correcting inaccurate or outdated information.

## 6. Monitoring and Improvement

The system should be evaluated regularly to identify outdated documents, retrieval failures, inaccurate responses, and potential privacy issues. Feedback should be reviewed carefully, and changes to source documents or retrieval settings should be tested before deployment.

Evaluation should consider answer accuracy, relevance, source consistency, privacy, and security rather than relying on a single performance measure.

## Conclusion

Responsible data management helps a public-service AI assistant provide useful and reliable information while protecting users' privacy. Reliable sources, data-quality checks, controlled access, clear retention policies, and continuous evaluation are important parts of a trustworthy RAG-based system.

## References

1. Lewis, P. et al. (2020). *Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks.* https://arxiv.org/abs/2005.11401
2. National Institute of Standards and Technology (NIST). *Artificial Intelligence Risk Management Framework (AI RMF 1.0).* https://doi.org/10.6028/NIST.AI.100-1
3. OWASP Foundation. *LLM02:2025 Sensitive Information Disclosure.* https://genai.owasp.org/llmrisk/llm022025-sensitive-information-disclosure/
