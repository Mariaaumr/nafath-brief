
Version: NAFATH-V3

Track: Cybersecurity

## Overview
A trustworthy public-service AI assistant depends on six connected IT fields. Software versioning helps teams manage API changes and maintain compatibility with the mobile application. Retrieval-Augmented Generation (RAG) can provide answers based on current government service documents, reducing reliance on outdated information. Mobile security protects communication between the app and its backend through secure connections. IPv6 supports a much larger address space as the number of connected devices grows. Cybersecurity controls help protect the assistant against prompt injection and unauthorized access to sensitive systems. Data protection practices help ensure that chat logs are stored and handled responsibly. These fields must work together because accurate answers alone do not guarantee a safe service. The assistant also needs secure communication, controlled access, and appropriate privacy safeguards. The key cybersecurity concern in this project is prompt injection and how it can manipulate an AI assistant through user input or untrusted external content.
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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
