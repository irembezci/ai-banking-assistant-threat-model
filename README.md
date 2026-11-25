# AI Banking Assistant — Security Assessment

## 1. System Definition

**Scenario:** Meridian Bank plans to deploy an AI-powered assistant accessible through its web application to provide customers with information about banking products, account procedures, card services and frequently asked questions.

**System Architecture:** The assistant uses a Retrieval-Augmented Generation (RAG) architecture, retrieving relevant information from a bank-approved knowledge base to generate responses through a third-party hosted LLM.

**Assessment Scope:** This assessment focuses on the security of the AI assistant's architecture, data flows, knowledge retrieval mechanisms, interfaces and supporting components.

**Initial Scope Limitations:**
- Information-only functionality
- No financial transactions or banking actions
- No direct access to core banking systems
- No customer document uploads
- Third-party LLM integration
- Bank-approved knowledge base

**Assessment Objectives:**
- Identify assets and attack surfaces
- Analyze trust boundaries and data flows
- Identify AI-specific and conventional security threats
- Assess and prioritize security risks
- Recommend security controls and mitigations

*This is a simulated security assessment based on assumed system architecture and design decisions. It does not represent an assessment of a real banking system.*

