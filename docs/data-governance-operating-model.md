# Data Governance Operating Model

## Purpose

A data governance operating model defines how data decisions are made, implemented, evidenced and maintained.

The objective is not to create a large governance bureaucracy.

The objective is to make:

- ownership;
- decision rights;
- standards;
- controls;
- evidence;
- exceptions;
- escalation

visible in normal delivery and operations.

## Core cycle

**Identify → Own → Classify → Trace → Control → Assure → Improve**

### Identify
Know which data assets matter.

### Own
Assign accountability and practical stewardship.

### Classify
Understand sensitivity, impact and obligations.

### Trace
Understand source, transformations, movement and dependencies.

### Control
Apply appropriate access, sharing, quality, lifecycle and security controls.

### Assure
Test whether controls are operating and evidence is available.

### Improve
Correct issues as technology, risk and use cases change.

## 1. Governance scope

Start with the data that matters most.

Prioritise by:

- customer impact;
- privacy sensitivity;
- regulatory impact;
- financial reporting;
- operational criticality;
- security sensitivity;
- analytics / AI importance;
- M&A / divestment dependency;
- third-party exposure.

Do not attempt to govern every dataset to the same depth on day one.

## 2. Roles and decision rights

### Data Owner

Accountable for:

- purpose and appropriate use;
- classification;
- access decisions;
- quality expectations;
- retention;
- external sharing;
- risk acceptance;
- exception approval or escalation.

The owner must have real decision rights.

### Data Steward

Supports:

- business definitions;
- metadata;
- quality monitoring;
- lineage upkeep;
- issue coordination;
- standards adoption;
- day-to-day governance.

### Technology / Platform Owner

Accountable for:

- platform operation;
- technical controls;
- identity and access;
- integration;
- backup and recovery;
- monitoring;
- supportability;
- technical lifecycle.

### Data / Analytics / AI Teams

Responsible for:

- transparent transformations;
- reproducibility;
- quality checks;
- lineage contribution;
- model/data documentation;
- appropriate reuse;
- evidence.

### Security / Privacy / Risk

Provides:

- minimum control requirements;
- independent challenge;
- privacy interpretation;
- regulatory interpretation;
- assurance;
- incident support.

## 3. Governance hierarchy

A practical hierarchy may be:

**Policy → Standard → Control → Procedure / Pattern → Evidence**

### Policy
States organisational intent.

### Standard
Defines mandatory minimum requirements.

### Control
Defines what must operate.

### Procedure / Pattern
Explains how teams implement the requirement.

### Evidence
Demonstrates the control operates.

This helps prevent policy from becoming disconnected from delivery.

## 4. Core governance domains

1. Ownership & stewardship
2. Classification
3. Lineage & metadata
4. Data quality
5. Access & sharing
6. Lifecycle, retention & disposal
7. Architecture & integration
8. Privacy & security
9. Third-party data
10. Analytics & AI
11. Assurance & evidence
12. Exceptions & risk acceptance

## 5. Governance forums

Keep forums proportionate.

### Operational

Participants:
- stewards;
- platform teams;
- delivery teams;
- business representatives.

Purpose:
- resolve normal data issues;
- review quality;
- maintain lineage;
- coordinate access;
- manage operational exceptions.

### Domain / Program

Participants:
- data owners;
- product / program leadership;
- architecture;
- security;
- data leads.

Purpose:
- prioritise remediation;
- approve material changes;
- resolve cross-system issues;
- decide access / quality / lifecycle trade-offs.

### Enterprise

Participants:
- senior data / technology / risk leadership.

Purpose:
- material risk;
- policy exceptions;
- cross-domain conflict;
- enterprise standards;
- strategic data priorities;
- regulatory / board-level matters.

## 6. Classification and handling

Classification should establish a minimum control baseline.

It should connect to:

- access;
- sharing;
- storage;
- encryption;
- retention;
- disposal;
- monitoring;
- third-party handling;
- AI use.

Classification should propagate through lineage.

## 7. Lineage

For critical datasets, governance should know:

- authoritative source;
- owner;
- classification;
- integration path;
- transformation points;
- destinations;
- downstream consumers;
- quality controls;
- third parties;
- AI consumers;
- retention;
- evidence.

Lineage is the bridge between policy and the real system estate.

## 8. Data quality

Quality expectations should be explicit.

Common dimensions:

- accuracy;
- completeness;
- consistency;
- timeliness;
- validity;
- uniqueness.

A quality rule should define:

- expected condition;
- owner;
- measurement;
- tolerance;
- remediation path;
- escalation threshold.

## 9. Access and sharing

Governance should support:

- least privilege;
- role-based access;
- periodic review;
- privileged-access control;
- external-sharing approval;
- service-account governance;
- third-party access;
- removal of stale access.

Access should reflect both classification and business need.

## 10. Lifecycle, retention and disposal

For important data, define:

- why it is retained;
- retention period;
- legal hold requirements;
- archive approach;
- destruction method;
- downstream deletion requirements;
- third-party deletion obligations.

Retention is part of governance, not just records management.

## 11. Third-party data governance

When data leaves the organisation, define:

- recipient;
- purpose;
- classification;
- transfer method;
- contract / DPA requirement;
- minimum controls;
- onward transfer;
- retention;
- deletion;
- incident notification;
- termination / exit.

## 12. Analytics and AI governance

Before data is used in analytics or AI, ask:

- Is the use consistent with the original purpose?
- Is the provenance known?
- Is sensitive data included?
- Is classification understood?
- Is access appropriate?
- Is the data current and sufficiently accurate?
- Can deletion / correction propagate?
- Are model or agent consumers recorded?
- Are outputs traceable where required?

AI governance should build on data governance rather than operate separately.

## 13. Exceptions and risk acceptance

Not every requirement can be met immediately.

A useful exception should capture:

- requirement;
- reason;
- risk;
- owner;
- compensating control;
- expiry date;
- remediation plan;
- approval.

Avoid permanent exceptions with no review date.

## 14. Governance triggers

Review governance when:

- new systems are introduced;
- new integrations are created;
- classification changes;
- new third parties receive data;
- data is used for AI;
- major transformations occur;
- incidents identify gaps;
- regulation changes;
- M&A or divestment occurs;
- systems are retired.

## 15. Measures

Useful measures show control and improvement.

Examples:

- % critical datasets with named owner;
- % critical datasets classified;
- % critical datasets with current lineage;
- % critical datasets with defined retention;
- unresolved high-risk access exceptions;
- unresolved material data-quality issues;
- stale lineage records;
- unreviewed third-party transfers;
- AI use cases with incomplete provenance;
- overdue governance exceptions.

Avoid metrics that only count meetings, documents or training events.

## 16. Minimum evidence set

For a critical dataset, the organisation should be able to produce:

- owner;
- steward;
- classification;
- authoritative source;
- lineage;
- quality rules;
- access model;
- retention;
- third-party use;
- analytics / AI use;
- active exceptions;
- current review evidence.

## 17. Maturity without bureaucracy

A mature model does not necessarily mean a large central governance function.

A small central function can define:

- policy;
- minimum standards;
- tooling;
- escalation;
- assurance;
- enterprise metrics.

Domain owners and delivery teams then operate within those guardrails.

## Principle

> **Governance works when decision rights and evidence are embedded in normal delivery and operations.**
