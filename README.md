# AI Banking Assistant — Security Assessment

## Project Overview

This project examines the security of an AI-powered banking assistant designed to provide customers with information about banking products, card services, account procedures and frequently asked questions.

The system uses a Retrieval-Augmented Generation (RAG) architecture, combining a bank-approved knowledge base with a third-party hosted Large Language Model (LLM) to generate responses.

The assessment aims to analyze the system's architecture, identify potential attack surfaces and threats, evaluate associated risks and propose security recommendations.

## Target System

| Component | Description |
|---|---|
| **Application** | AI Banking Assistant |
| **Business Context** | Banking and Financial Services |
| **Architecture** | Retrieval-Augmented Generation (RAG) |
| **Knowledge Source** | Bank-approved documentation |
| **LLM Provider** | Third-party hosted LLM |
| **Application Scope** | Information-only assistant |

The assistant is designed to provide general banking information. It does not execute financial transactions, access core banking systems directly or accept customer document uploads.

## Assessment Scope

The assessment focuses on the security of the AI application's architecture, data flows, retrieval mechanisms, interfaces and supporting components.

The analysis covers:

- System architecture and data flows
- Assets and attack surfaces
- AI-specific and conventional security threats
- Threat scenarios and risk prioritization
- Security controls and mitigation recommendations

## Assessment Process

### 1. System Definition & Architecture

Define the system, its architecture, scope and initial assumptions.

[View System Definition & Architecture](docs/system-definition.md)

### 2. Data Flow & Trust Boundaries

Examine how data moves across system components and identify trust boundaries.

[View Data Flow Analysis](docs/data-flow-analysis.md)

### 3. Asset & Attack Surface Analysis

Identify critical assets, entry points and potential attack surfaces.

[View Asset & Attack Surface Analysis](docs/asset-attack-surface-analysis.md)

### 4. Threat Identification

Identify AI-specific and conventional security threats and develop attack scenarios.

[View Threat Identification](docs/threat-identification.md)

### 5. Risk Assessment & Prioritization

Evaluate identified threats based on likelihood, impact and risk severity.

[View Risk Assessment](docs/risk-assessment.md)

### 6. Security Controls & Mitigation

Define security controls and mitigation strategies for prioritized risks.

[View Security Controls & Mitigation](docs/security-controls-mitigation.md)

### 7. Final Security Assessment

Consolidate findings, prioritized risks and security recommendations into a final assessment.

[View Final Security Assessment](docs/final-assessment.md)

---

*This assessment uses a fictional banking scenario and synthetic system data for research and portfolio purposes.*
