# GOVERN-AI — Audit & Compliance Intelligence Engine

**Evidence-Grounded Audit Analysis | Explainable Risk Assessment | Human-in-the-Loop Verification**

## Overview

GOVERN-AI is a prototype audit and compliance intelligence dashboard designed to help users inspect government audit documents, extract relevant evidence, identify potential risk indicators, and organize findings for human review.

The project explores a provenance-oriented approach to audit intelligence: extracted findings should remain traceable to their source documents, unavailable information should be identified explicitly, and automated recommendations should support rather than replace human auditors.

## Problem Statement

Government audit workflows often involve reviewing lengthy PDF reports, scanned inspection documents, financial observations, and tabular records. Manual examination can be time-consuming, while automated extraction and risk scoring may introduce errors or unsupported conclusions if the underlying evidence is not traceable.

GOVERN-AI explores a document-centered workflow that combines extraction, data-quality checks, risk analysis, evidence traceability, and human verification in a single dashboard.

## Objectives

- Simplify the inspection of digital and scanned audit PDFs.
- Extract document text and identify potential audit findings.
- Preserve source-document provenance for extracted evidence.
- Evaluate risk indicators using available and verifiable inputs.
- Explore document quality assessment and robust statistical outlier detection.
- Provide transparent processing logs and exportable results.
- Support human review of flagged cases and recommendations.

## Key Features

### 1. Document Ingestion and OCR
- PDF upload interface.
- Digital text extraction using PDF.js.
- Browser-based OCR using Tesseract.js for scanned pages.
- Experimental reconstruction of tabular structures.

### 2. Audit Case and Risk Dashboard
- Audit case tables and risk-related indicators.
- Financial exposure, backlog, severity, and priority fields.
- Explicit handling of fields that are unavailable in the source document.

### 3. Three-Level Evaluation Interface
- Level 1: Document extraction and finding classification.
- Level 2: Risk triage and priority assessment.
- Level 3: Anomaly and outlier analysis.

The interface provides fields for accuracy, precision, recall, F1 score, ROC-AUC, and confusion-matrix analysis. Valid performance claims require appropriate labeled evaluation data.

### 4. Evidence Traceability and Explainability
- Source-oriented evidence chain.
- Highlighting of potentially relevant text.
- Prototype contribution analysis for risk indicators.
- Recommended verification actions for human review.

### 5. Data Quality and Robust Statistics
- Six-dimension quality assessment interface.
- Median Absolute Deviation (MAD) analysis.
- Jaro–Winkler entity similarity and deduplication interface.
- Data-dependent validation and anomaly analysis.

### 6. Human-in-the-Loop Review
- Auditor feedback interface.
- Review status and processing logs.
- Export options for cases, extracted evidence, evaluation metrics, and audit logs.

## System Workflow

1. Upload an audit PDF.
2. Extract digital text and optionally process scanned pages with OCR.
3. Identify candidate findings, numerical values, and tables.
4. Check whether required information is available in the source.
5. Calculate only those indicators supported by the implemented logic and available data.
6. Present findings, quality indicators, and verification suggestions.
7. Allow a human reviewer to inspect the evidence and record feedback.
8. Export supported outputs for further examination.

## Implementation Status and Limitations

GOVERN-AI is a research and demonstration prototype. The interface includes different implementation-status indicators, and these must be interpreted according to the actual source code.

Some components are explicitly identified in the dashboard as prototypes or not implemented, including Huber M-estimation and Isolation Forest. Some evidence-attribution methods are heuristic rather than formal SHAP or LIME implementations.

The presence of evaluation fields or charts does not by itself establish measured model performance. Accuracy, precision, recall, F1 score, and ROC-AUC should be reported as empirical results only after testing against appropriate labeled ground truth.

The current frontend should not be described as a deployed government auditing system or as guaranteeing zero hallucinations, fraud detection, or legally valid conclusions.

## Future Scope

- Develop a validated backend for structured document processing.
- Build an annotated benchmark of audit findings and risk labels.
- Evaluate extraction quality against human-verified ground truth.
- Implement and validate formal anomaly-detection models.
- Add stronger source references, page-level evidence, and confidence reporting.
- Introduce secure storage, authentication, access controls, and privacy safeguards where required.
- Conduct expert-led evaluation before any operational deployment.

## Responsible Use

GOVERN-AI is intended for research, educational demonstration, and assisted document review. Its outputs should be independently verified against the original documents. Risk indicators are not proof of wrongdoing, and final audit decisions must remain with authorized human reviewers.

## Project Status

**Status:** Prototype / Research Project

This repository documents the frontend and its evolving capabilities. Implementation, testing, and validation should be completed before making claims about operational readiness or real-world performance.

## License

No license has been specified yet. Reuse and redistribution permissions depend on the license eventually selected by the repository owner.
