# Data Classification & Governance Readiness

## Purpose

Data classification should help people make better decisions about how information is handled. It should not exist only as a label in policy.

A useful model connects:

**data asset → impact → classification → controls → lineage → review**

The operating lifecycle is:

**Identify → Assess Impact → Classify → Apply Controls → Propagate → Review**

## 1. Identify

Start with the data asset and its purpose. Identify the authoritative source, accountable owner and major consumers.

## 2. Assess Impact

Classification should be risk-based rather than determined only by content type.

Ask what would happen if the data were disclosed without authority, changed incorrectly, unavailable, used outside its intended purpose, shared with an unsuitable third party, or used by analytics/AI without appropriate review.

Consider sensitivity, legal/contractual obligations, business criticality, distribution and intended use.

## 3. Classify

The labels below are deliberately generic and can later be mapped to an organisation's terminology.

### Public
Information approved for public distribution.

### Internal
Information intended for normal internal business use.

### Confidential
Information where unauthorised disclosure, alteration or misuse could create material business, privacy, contractual or reputational impact.

### Restricted
Highly sensitive information where compromise could create significant legal, regulatory, security, safety, financial or individual harm.

## 4. Apply Controls

Classification should define the **minimum control baseline**. Business context, regulation, contractual obligations and system risk may require stronger controls.

Typical decisions include ownership, access, sharing, storage, encryption, retention, disposal, monitoring, third-party conditions and AI use.

## 5. Propagate

Classification should follow the data.

Example:

**CRM → API → Data Platform → Report → AI Retrieval Store**

The default principle is:

> **Downstream data inherits the source classification unless there is a documented and approved basis to change it.**

Possible reasons for a justified change include verified aggregation, masking, tokenisation, de-identification, removal of sensitive fields or formal owner-approved reclassification.

Any reclassification should be documented, repeatable, reviewable and reflected in lineage.

**Classification tells us the control requirement.  
Lineage tells us everywhere that requirement has to follow.**

## 6. Review

Typical review triggers include a new integration, new downstream consumer, third-party sharing, AI/analytics use, system migration, material transformation, regulatory/contractual change, M&A/divestment, or a material incident.

## Recommended decision record

A classification assessment should produce more than a label:

- Suggested / approved classification
- Accountable owner
- Primary classification drivers
- Minimum control baseline
- Lineage status
- Downstream inheritance requirement
- AI / analytics implications
- Third-party implications
- Review trigger
- Decision / approval evidence

## Principle

> **Classification is not the end state. It is the starting point for control decisions that must follow the data.**
