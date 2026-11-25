# Phase 3: Asset Identification

## 1. Overview

This phase identifies the assets within the RAG-based AI banking assistant that require protection. Assets were evaluated based on their relevance to the system's operation, the potential impact of compromise and their role in maintaining the security and reliability of the assistant.

The assessment considers Confidentiality, Integrity and Availability (CIA) as the primary security properties.

## 2. Asset Register

| ID | Asset | Description | C | I | A |
|---|---|---|---|---|---|
| A-01 | Bank Knowledge Base | Approved banking documents and information used to generate responses. | Medium | High | High |
| A-02 | Vector Database & Retrieved Data | Stored vector representations and associated content used during retrieval. | High | High | High |
| A-03 | Customer Queries | User-provided inputs processed by the assistant. | High | High | High |
| A-04 | System Instructions & Prompt Configuration | Instructions and configuration defining the assistant's behavior and restrictions. | High | High | Medium |
| A-05 | Backend API | Component responsible for orchestrating request processing, retrieval and LLM interactions. | High | High | High |
| A-06 | AI-Generated Responses | Responses delivered to users by the assistant. | High | High | High |
| A-07 | Logging Data | Operational records potentially containing queries, retrieved content and system events. | High | High | Medium |
| A-08 | Third-Party LLM Service | External service responsible for processing prompts and generating responses. | High | High | High |
| A-09 | Embedding Model | Model responsible for converting text into vector representations for retrieval. | High | High | High |
| A-10 | Service Availability | Overall availability and usability of the AI assistant service. | Medium | High | High |

## 3. Asset Criticality Rationale

### A-01: Bank Knowledge Base

| Property | Priority | Rationale |
|---|---|---|
| Confidentiality | Medium | Internal documentation may contain information not intended for public disclosure. |
| Integrity | High | Unauthorized modification may introduce incorrect or malicious banking information into responses. |
| Availability | High | Knowledge base unavailability may prevent the assistant from retrieving relevant information. |

### A-02: Vector Database & Retrieved Data

| Property | Priority | Rationale |
|---|---|---|
| Confidentiality | High | Unauthorized access may expose stored content or information represented within the retrieval system. |
| Integrity | High | Manipulated or poisoned content may influence retrieval and produce misleading responses. |
| Availability | High | Retrieval failures may prevent the assistant from accessing relevant knowledge. |

### A-03: Customer Queries

| Property | Priority | Rationale |
|---|---|---|
| Confidentiality | High | User queries may contain personal, sensitive or confidential information. |
| Integrity | High | Adversarially crafted or manipulated inputs may influence retrieval, processing or model behavior. |
| Availability | High | Excessive or malicious requests may disrupt request processing and service availability. |

### A-04: System Instructions & Prompt Configuration

| Property | Priority | Rationale |
|---|---|---|
| Confidentiality | High | Disclosure may reveal operational details that could facilitate attacks. |
| Integrity | High | Unauthorized modification may alter intended behavior or weaken security restrictions. |
| Availability | Medium | Configuration disruption may affect assistant behavior, depending on recovery mechanisms and system design. |

### A-05: Backend API

| Property | Priority | Rationale |
|---|---|---|
| Confidentiality | High | The backend may process queries, retrieved content and prompt data containing sensitive information. |
| Integrity | High | Manipulation of request processing, retrieval orchestration or response handling may affect system behavior. |
| Availability | High | Backend disruption may prevent the core assistant workflow from functioning. |

### A-06: AI-Generated Responses

| Property | Priority | Rationale |
|---|---|---|
| Confidentiality | High | Responses may inadvertently disclose sensitive information or content beyond the intended scope. |
| Integrity | High | Incorrect, manipulated or misleading responses may affect users' understanding of banking products and procedures. |
| Availability | High | Response generation disruptions may prevent users from accessing banking information through the assistant. |

### A-07: Logging Data

| Property | Priority | Rationale |
|---|---|---|
| Confidentiality | High | Logs may contain customer queries, retrieved content or technical information that could expose sensitive data. |
| Integrity | High | Unauthorized modification may undermine incident investigation, monitoring and the reliability of recorded events. |
| Availability | Medium | Log unavailability may impair monitoring and investigation capabilities without necessarily interrupting core functionality. |

### A-08: Third-Party LLM Service

| Property | Priority | Rationale |
|---|---|---|
| Confidentiality | High | Data transmitted to the external provider may expose sensitive information if mishandled or inadequately protected. |
| Integrity | High | Compromised or unreliable model processing may produce misleading or malicious responses. |
| Availability | High | Provider outages or service disruptions may prevent response generation. |

### A-09: Embedding Model

| Property | Priority | Rationale |
|---|---|---|
| Confidentiality | High | The model may process user queries or knowledge base content during embedding generation. |
| Integrity | High | Manipulated or compromised embedding generation may distort semantic representations and affect retrieval accuracy. |
| Availability | High | Embedding generation failures may disrupt query processing or knowledge ingestion. |

### A-10: Service Availability

| Property | Priority | Rationale |
|---|---|---|
| Confidentiality | Medium | The service-level asset may indirectly involve sensitive operational information, although confidentiality is not its primary security property. |
| Integrity | High | The service must maintain reliable processing and delivery of its intended functionality. |
| Availability | High | The assistant must remain operational and accessible across its core components to deliver its intended service. |

## 4. Assessment Notes

The asset criticality ratings represent a preliminary qualitative assessment based on the defined system architecture and assumptions.

The ratings may be revised as additional information becomes available regarding data sensitivity, access controls, infrastructure dependencies, recovery mechanisms and operational security controls.

## 5. Outcome

Ten assets were identified and evaluated according to their Confidentiality, Integrity and Availability requirements.

These assets will serve as the basis for the subsequent attack surface analysis, threat identification and risk assessment phases.
