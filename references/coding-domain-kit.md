# Coding Domain Skill Reference Index

This file contains the expanded reusable engineering skill set. It is reference material: load only the sections relevant to the current task.

---
# accessibility

---
name: accessibility
description: Use for accessible web/mobile UI and inclusive interaction design.
---

# Accessibility

Treat semantic structure, keyboard/focus behavior, screen-reader naming, contrast, target size, motion preferences,
forms, errors, and assistive technology compatibility as functional requirements.

Test with automated checks plus representative manual interaction where practical.

---
# agent-engineering

---
name: agent-engineering
description: Use for agents, tool use, memory, planning, orchestration, and multi-agent workflows.
---

# Agent Engineering

PLAN -> TOOL ACTION -> OBSERVATION -> VALIDATE -> UPDATE STATE -> NEXT ACTION.

Before tools, confirm authorization and define expected evidence. After tools, verify actual artifacts/state.
Do not infer execution from intent. Do not expose private chain-of-thought; record concise operational provenance.

---
# ai-llm

---
name: ai-llm
description: Use for LLM integrations, RAG, structured generation, evaluation, prompting, and model-dependent systems.
---

# AI and LLM Engineering

Separate model capability, application capability, tool capability, retrieved knowledge, actual execution,
and verification.

Use explicit schemas, input/output validation, bounded retries/timeouts, provenance, prompt-injection defenses,
and task-specific evaluations. Evaluate retrieval quality separately from answer quality.

---
# api-design

---
name: api-design
description: Use for REST, GraphQL, RPC, events, webhooks, schemas, versioning, and public service contracts.
---

# API Design

Define resources/contracts, request/response schemas, validation, authentication and authorization, idempotency,
timeouts, retries, pagination, filtering, errors, rate limits, compatibility, deprecation, observability, and ownership.

Treat external contracts as compatibility-sensitive interfaces. Explicitly document breaking versus non-breaking changes.

---
# architecture

---
name: architecture
description: Use for architecture design, decomposition, migrations, trade-offs, and Architecture Decision Records.
---

# Architecture

REQUIREMENTS -> CONSTRAINTS -> QUALITY ATTRIBUTES -> OPTIONS -> TRADE-OFFS -> DECISION -> ADR -> VALIDATION.

Evaluate reliability, scalability, latency, consistency, security, operability, cost, deployment complexity,
team ownership, migration complexity, and failure modes.

Do not introduce microservices, event buses, Kubernetes, CQRS, or other complexity merely because they are fashionable.

Distinguish documented design from observed runtime behavior.

---
# backend

---
name: backend
description: Use for server-side applications, services, workers, APIs, queues, and business logic.
---

# Backend Engineering

Enforce trust boundaries server-side. Design transaction boundaries, concurrency behavior, timeouts, retry policies,
resource limits, graceful failure, structured errors/logging, health checks, idempotency, and observability.

Keep domain logic cohesive and infrastructure dependencies isolated where practical.

---
# cloud

---
name: cloud
description: Use for AWS, Azure, GCP, infrastructure as code, cloud architecture, and cloud operations.
---

# Cloud Engineering

Evaluate identity and least privilege, network boundaries, encryption, backups/recovery, availability,
quotas, autoscaling, cost, observability, disaster recovery, infrastructure as code, and operational ownership.

Configuration files are not proof that resources exist, are reachable, or are secure. Verify actual state.

---
# code-review

---
name: code-review
description: Use for pull-request and patch review focused on correctness, security, maintainability, and regressions.
---

# Code Review

Review in order:
1. Correctness/regressions
2. Security/data exposure
3. Concurrency/failure handling
4. Compatibility/API/data contracts
5. Performance/resource behavior
6. Maintainability/readability
7. Tests
8. Observability/documentation

Each finding needs location/scope, evidence, severity/impact, and remediation.
Do not manufacture findings. State inspected scope and limitations.

---
# codebase-onboarding

---
name: codebase-onboarding
description: Use when entering an unfamiliar repository or performing a repository readiness audit.
---

# Codebase Onboarding

Establish:
- canonical branch/commit and repository identity
- project structure and entrypoints
- build/test/lint commands
- dependency/runtime requirements
- architecture and data flow
- CI/CD and deployment assumptions
- configuration/secrets boundaries
- known risks and missing evidence

Separate observed repository facts from inference. Do not declare a repository complete without checking execution and
deployment evidence relevant to the acceptance criteria.

---
# configuration-management

---
name: configuration-management
description: Use for environment configuration, feature flags, secrets, and deployment-time settings.
---

# Configuration Management

Separate code from environment-specific configuration. Validate required settings at startup or safe boundaries.
Never log secrets. Define defaults deliberately and make unsafe defaults obvious.

For configuration changes, identify environments affected and provide verification steps.

---
# data-engineering

---
name: data-engineering
description: Use for ETL/ELT, data pipelines, warehouses, streaming, backfills, and data quality.
---

# Data Engineering

Define data contracts, lineage, freshness, schema evolution, partitioning, idempotency, deduplication, data-quality
rules, replay/recovery, and observability.

For backfills and reprocessing, explicitly reason about correctness, duplicates, downstream impact, and cutover.

---
# databases

---
name: databases
description: Use for SQL/NoSQL schema design, migrations, transactions, indexes, query tuning, and integrity.
---

# Database Engineering

Inspect the current schema before changing it. Treat schema and migrations as production interfaces.
Design compatibility and rollback/forward-repair strategy. Measure query behavior and inspect execution plans.
Consider locking, isolation, concurrency, cardinality, indexing, and data lifecycle.

Never perform destructive production mutations without explicit authorization and recovery planning.

---
# debugging

---
name: debugging
description: Use for bugs, failures, regressions, flaky behavior, incidents, and unexpected runtime behavior.
---

# Debugging

REPRODUCE/CHARACTERIZE -> BASELINE -> COLLECT EVIDENCE -> FORM FALSIFIABLE HYPOTHESES
-> TEST HIGHEST-INFORMATION HYPOTHESIS -> REPAIR -> RE-EXECUTE -> VERIFY -> RECORD.

Classify failures as transient, environmental, dependency, configuration, implementation, data, authorization,
tool availability, platform limitation, or specification ambiguity.

Do not declare a runtime fix from static inspection alone when execution is available and required for verification.

---
# dependency-management

---
name: dependency-management
description: Use for dependency upgrades, compatibility analysis, lockfiles, SBOMs, and supply-chain hygiene.
---

# Dependency Management

Inventory direct and transitive dependencies. Check compatibility, security advisories, license constraints,
runtime requirements, lockfile behavior, release notes, and rollback options.

Prefer incremental upgrades with targeted regression coverage. Do not assume a semver-compatible update is behavior-free.

---
# devops-cicd

---
name: devops-cicd
description: Use for builds, CI/CD pipelines, deployment automation, artifact integrity, rollback, and release gates.
---

# DevOps and CI/CD

Typical gates:
format/lint -> static checks -> tests -> dependency/security checks -> build -> artifact verification
-> deploy -> smoke/health checks.

Prefer reproducible and versioned artifacts, least privilege, secret isolation, configuration validation,
migration safety, explicit rollback strategy, and deployment observability.

Never claim deployment success without observable evidence.

---
# distributed-systems

---
name: distributed-systems
description: Use for distributed services, queues, event-driven systems, caching, concurrency, and coordination.
---

# Distributed Systems

Reason explicitly about retries, duplicates, ordering, time, clock skew, idempotency, consistency, partitions,
backpressure, leases/locks, message loss, poison messages, replay, and recovery.

Prefer simple guarantees that are observable and testable. State assumptions instead of hiding them.

---
# documentation

---
name: documentation
description: Use for READMEs, runbooks, ADRs, API docs, architecture docs, and engineering guides.
---

# Engineering Documentation

Document purpose, prerequisites, assumptions, commands, expected outputs, failure modes, recovery, ownership,
and verification status. Prefer tested instructions over aspirational prose. Keep docs aligned with actual code.

---
# frontend

---
name: frontend
description: Use for web UI implementation, refactoring, state management, accessibility, and performance.
---

# Frontend Engineering

Make state ownership explicit. Handle loading, error, empty, and partial states. Validate untrusted content.
Preserve accessibility, responsive behavior, predictable async flows, and maintainable component/style boundaries.

Avoid needless global state, render churn, duplicated network calls, and premature abstractions.

---
# git-release-engineering

---
name: git-release-engineering
description: Use for branches, commits, pull requests, releases, changelogs, versioning, and rollback.
---

# Git and Release Engineering

Keep changes cohesive and traceable. Prefer reviewable commits and reproducible release artifacts.
Define release validation and rollback/forward-fix paths.

Do not rewrite history or replace release artifacts destructively without authorization.

---
# migration

---
name: migration
description: Use for framework, database, cloud, service, API, or platform migrations.
---

# Migration Engineering

Inventory current state -> define target -> map compatibility gaps -> design staged migration -> rehearse/validate
-> migrate -> verify -> retire old path.

Prefer dual-read/dual-write or compatibility layers only when justified. Maintain rollback or forward-repair strategy.

---
# mobile

---
name: mobile
description: Use for Android, iOS, React Native, Flutter, and mobile release engineering.
---

# Mobile Engineering

Treat lifecycle, permissions, connectivity changes, offline behavior, persistence, background execution, platform
differences, crash handling, release signing, compatibility, and upgrade paths as first-class concerns.

Verify framework/platform behavior against the actual version when correctness depends on it.

---
# observability

---
name: observability
description: Use for logging, metrics, tracing, SLOs, alerting, diagnostics, and telemetry design.
---

# Observability

Prefer structured, correlatable telemetry. Define useful signals before building dashboards.
Avoid sensitive-data leakage. Make alerts actionable and tied to customer or system risk.

Tie runtime conclusions to actual logs/metrics/traces rather than assumptions.

---
# performance

---
name: performance
description: Use for latency, throughput, CPU, memory, I/O, database, and scalability optimization.
---

# Performance Engineering

MEASURE -> PROFILE -> IDENTIFY BOTTLENECK -> CHANGE -> BENCHMARK -> VERIFY.

Record workload, environment, baseline, metric, and result. Consider algorithmic, I/O, network, database,
serialization, concurrency, allocation, and caching costs. Avoid intuition-only optimization.

---
# product-engineering

---
name: product-engineering
description: Use when engineering decisions affect users, product behavior, delivery risk, or business outcomes.
---

# Product Engineering

Connect technical changes to explicit user/business outcomes. Define acceptance criteria, edge cases, failure impact,
rollout strategy, telemetry, supportability, and rollback.

Prefer the smallest implementation that validates the actual outcome, not code volume.

---
# refactoring

---
name: refactoring
description: Use for structural code improvement while preserving externally observable behavior.
---

# Refactoring

Establish behavior to preserve, create/confirm regression tests, refactor in small coherent steps, and verify after
material changes.

Refactor when it reduces real complexity, coupling, duplication, or risk. Do not mix unrelated functional changes.

---
# reliability-incident-response

---
name: reliability-incident-response
description: Use for production incidents, outages, degraded service, containment, recovery, and postmortems.
---

# Reliability and Incident Response

DETECT -> CONTAIN -> DIAGNOSE -> MITIGATE -> VERIFY -> RECOVER -> LEARN.

Prioritize safe restoration and customer impact. Record timeline, evidence, contributing factors, detection gaps,
and durable corrective actions. Avoid blame-oriented analysis.

---
# research-evidence

---
name: research-evidence
description: Use for technical research, current-state verification, source triangulation, and adversarial analysis.
---

# Evidence-Disciplined Research

QUESTION -> DECOMPOSE -> SEARCH -> SOURCE FILTER -> EXTRACT -> TRIANGULATE -> ADVERSARIAL ATTACK
-> SYNTHESIZE -> DECIDE -> RECORD -> NEXT ACTION.

Prefer primary/official sources. Label material claims VERIFIED, STRONGLY SUPPORTED, LIKELY, UNVERIFIED,
CONTRADICTED, or UNKNOWN. Search for the strongest counterexample before closing a branch.

---
# security

---
name: security
description: Use for application, infrastructure, dependency, secret, and supply-chain security analysis.
---

# Security Engineering

Audit trust boundaries, authentication/authorization, injection, XSS/CSRF where applicable, SSRF, path traversal,
deserialization, secret exposure, dependency risk, privilege boundaries, sensitive logging, tenant isolation,
cryptographic misuse, abuse/rate limits, and supply-chain integrity.

Assume external input is untrusted. Never embed credentials. A clean scan is not proof that no vulnerability exists.

---
# software-engineering

---
name: software-engineering
description: Use for implementation, refactoring, bug fixes, and general production software engineering.
---

# Software Engineering

UNDERSTAND -> MAP DEPENDENCIES -> DEFINE ACCEPTANCE -> IMPLEMENT MINIMAL COHERENT CHANGE -> TEST -> REVIEW -> VERIFY.

Preserve existing behavior unless a breaking change is authorized. Favor cohesion, explicit contracts, readable code,
validated inputs, intentional error handling, isolated side effects, and reusable abstractions only when they reduce
actual complexity. Avoid hacks and unrelated refactors.

For material changes record what changed, what must not change, tests run, and remaining uncertainty.

---
# technical-decision-making

---
name: technical-decision-making
description: Use for comparing architectures, vendors, frameworks, tools, or implementation strategies.
---

# Technical Decision Making

Define decision criteria and constraints before comparing options. Evaluate evidence, trade-offs, migration cost,
operational burden, security, performance, maintainability, lock-in, reversibility, and lifecycle.

Do not convert popularity, vendor marketing, or anecdotal success into technical fact.

---
# testing-tdd

---
name: testing-tdd
description: Use for TDD, test design, regression testing, integration testing, and verification.
---

# Testing and TDD

RED -> GREEN -> REFACTOR.

Choose the cheapest test that proves the required behavior and add stronger tests as risk demands:
unit, integration, contract, end-to-end, security, performance.

Do not treat line coverage as proof of correctness. Report test state as NOT RUN, RUNNING, PASSED, FAILED, or BLOCKED.
