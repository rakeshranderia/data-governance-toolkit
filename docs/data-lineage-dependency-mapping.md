# Data Lineage & Dependency Mapping

## Purpose

Data lineage explains:

**where data came from → what happened to it → where it moved → what now depends on it**

That makes lineage a governance, architecture and operational capability — not simply a documentation exercise.

A useful lineage model supports:

- data governance;
- security;
- privacy;
- data quality;
- architecture;
- integration;
- incident response;
- change impact;
- migration;
- M&A and divestment;
- analytics;
- AI governance.

## Core flow

**Source → Ingest → Transform → Store → Serve → Consume → Retain / Delete**

At every stage, capture enough context to answer:

- What system or dataset is involved?
- Is this the authoritative source?
- Who owns it?
- What is its classification?
- How did the data move?
- What transformation occurred?
- Has the meaning changed?
- Which systems and processes depend on it?
- What controls apply?
- What evidence exists?
- Is the lineage current?

## 1. Authoritative source and provenance

Every critical data element should have a known origin.

Key questions:

- What is the system of record?
- Is this original data or derived data?
- Was the data imported from a third party?
- Was it entered manually?
- Has it been corrected or enriched?
- Is the source trusted?
- Can provenance be demonstrated?

Data provenance is especially important for:

- regulated data;
- executive reporting;
- financial information;
- customer information;
- machine learning;
- retrieval-augmented generation;
- automated decisions.

## 2. Movement and integration

Lineage should reflect how data actually moves.

Common patterns include:

- synchronous API;
- asynchronous API;
- events and messaging;
- EDI;
- file transfer / SFTP;
- ETL / ELT;
- database replication;
- direct database access;
- SaaS connectors;
- manual exports and spreadsheets.

The movement pattern affects:

- timing;
- failure modes;
- reconciliation;
- duplicate handling;
- retry behaviour;
- monitoring;
- recovery;
- support ownership.

A high-level lineage diagram that ignores the integration method can miss operational risk.

## 3. Transformations

A system-to-system diagram is not enough if the meaning of data changes between systems.

Transformations may include:

- field mapping;
- format conversion;
- enrichment;
- aggregation;
- filtering;
- masking;
- tokenisation;
- de-identification;
- calculations;
- currency conversion;
- timezone conversion;
- identity matching;
- record consolidation;
- data-quality correction;
- business-rule application.

For important transformations, capture:

- what changed;
- why it changed;
- who owns the rule;
- where the logic is implemented;
- how it is tested;
- how exceptions are handled.

## 4. Classification propagation

Classification must follow the data through the lineage.

Default principle:

> **Downstream data inherits the source classification unless there is a documented and approved basis to change it.**

Possible justified changes include:

- verified aggregation;
- masking;
- tokenisation;
- de-identification;
- removal of sensitive fields;
- approved reclassification.

Lineage should show where a classification changes and why.

## 5. Downstream dependencies

For every critical dataset, identify:

- consuming systems;
- reports;
- dashboards;
- operational processes;
- APIs;
- files;
- third parties;
- models;
- agents;
- AI retrieval stores;
- regulatory or executive outputs.

A useful change-impact question is:

> **What breaks, becomes inaccurate or becomes non-compliant if this changes?**

## 6. Reconciliation and quality

Lineage should record where data is validated.

Possible controls include:

- record counts;
- control totals;
- schema validation;
- referential checks;
- duplicate detection;
- exception queues;
- rejected-record handling;
- data-quality rules;
- source-to-target reconciliation.

A lineage map without control points can show movement without showing trust.

## 7. Access and security

Lineage helps identify where sensitive data is duplicated or exposed.

Capture:

- system access model;
- privileged access;
- service identities;
- secrets / credentials;
- encryption boundary;
- external sharing;
- third-party access;
- logging;
- monitoring.

This is particularly important when data moves from a strongly governed source into:

- spreadsheets;
- files;
- collaboration platforms;
- test environments;
- analytics tools;
- AI platforms.

## 8. Third-party lineage

If data leaves the organisation, lineage should identify:

- recipient;
- purpose;
- transfer method;
- classification;
- contractual controls;
- retention requirements;
- deletion obligations;
- subprocessor / onward transfer risk;
- return or destruction requirements.

## 9. AI and model lineage

AI extends traditional lineage.

A simple pattern may be:

**Curated Dataset → Embedding / Indexing → Vector Store → RAG / Agent → Model → User Output**

Questions include:

- What source data is used?
- What classification applies?
- Was the data transformed?
- Is the use permitted?
- Is sensitive data present?
- How is data refreshed?
- How does deletion propagate?
- Which model or agent consumes it?
- Is output traceability required?
- Can a user identify the source of a result?

For model training:

**Source → Preparation → Training Dataset → Model Version → Evaluation → Deployment**

Record:

- training source;
- permissions;
- preparation steps;
- model version;
- evaluation evidence;
- deployment target;
- retirement / retraining history.

## 10. Lineage levels

Not every dataset requires the same depth.

### Level 1 — Business lineage

Example:

**CRM → Integration Platform → Data Platform → Executive Dashboard**

Useful for:
- ownership;
- executive governance;
- business dependency;
- transformation planning;
- M&A / divestment.

### Level 2 — System lineage

Adds:
- interfaces;
- schedules;
- integration methods;
- source/destination systems;
- key transformations;
- support ownership;
- reconciliation.

Useful for:
- architecture;
- change;
- incidents;
- operations;
- migration.

### Level 3 — Technical lineage

Adds:
- databases;
- tables;
- fields;
- schemas;
- pipelines;
- transformation code;
- mappings;
- technical controls.

Useful for:
- engineering;
- regulated datasets;
- debugging;
- data quality;
- model provenance.

Depth should be proportionate to risk, value and dependency.

## 11. M&A, divestment and system retirement

Lineage is critical when changing the technology estate.

It helps identify:

- shared systems;
- shared datasets;
- hidden dependencies;
- interfaces;
- migration order;
- separation requirements;
- TSA dependencies;
- regulatory records;
- archive requirements;
- retirement blockers.

Before decommissioning a system, confirm:

- no critical downstream consumers remain;
- data has been migrated or retained appropriately;
- historical reporting needs are covered;
- interfaces are retired;
- third-party dependencies are closed;
- access is removed;
- data disposal requirements are met.

## 12. Incident response

Lineage improves incident response by helping answer:

- What data was affected?
- Where did it come from?
- Where else did it go?
- Which systems contain copies?
- Which users or third parties received it?
- Which reports or models may now be unreliable?
- What needs to be corrected, revoked or reprocessed?

## 13. Lineage currency

Lineage becomes dangerous if it looks authoritative but is stale.

Update lineage when:

- a new integration is created;
- a source is replaced;
- a transformation changes;
- a new report is introduced;
- a new third-party transfer starts;
- an AI use case is introduced;
- a system is migrated;
- a system is retired;
- M&A or divestment changes the estate;
- material incidents expose undocumented flows.

Every important lineage record should include:

- owner;
- last review date;
- review trigger;
- evidence source.

## Minimum lineage record

| Field | Purpose |
|---|---|
| Data asset | Dataset, table, file, API payload, event, report |
| Authoritative source | System of record / origin |
| Source owner | Accountable owner |
| Classification | Handling level |
| Interface | API, EDI, file, event, ETL/ELT, DB, manual |
| Transformation | Mapping, enrichment, aggregation, masking, calculation |
| Destination | Next system or platform |
| Downstream consumer | Report, system, team, third party, model or process |
| Quality control | Validation or reconciliation |
| Access model | Who can access it |
| Retention | How long it persists |
| Evidence | Schema, mapping, logs, approval, documentation |
| Criticality | Business dependency / impact |
| Review date | Currency |
| Review trigger | Event that requires reassessment |

## Lineage health indicators

A lineage record is weak when:

- authoritative source is uncertain;
- owner is missing;
- classification is missing;
- integration method is unknown;
- transformations are undocumented;
- downstream consumers are incomplete;
- third-party movement is invisible;
- reconciliation is absent;
- manual spreadsheet steps are hidden;
- AI consumers are undocumented;
- retention is unknown;
- review date is stale.

## Practical operating model

Lineage should be captured as part of normal delivery.

It should be updated through:

- architecture reviews;
- integration design;
- data-product delivery;
- change management;
- incident review;
- AI-use assessment;
- system retirement;
- M&A / divestment work.

## Principle

> **You cannot govern data well if you cannot explain where it came from, what happened to it, and where it goes next.**

And:

> **Classification tells us the control requirement. Lineage tells us everywhere that requirement has to follow.**
