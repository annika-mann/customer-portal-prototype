# Patch Management Case Study

## Table of Contents

- [Product Context](#product-context)
- [Prototype](#prototype)
- [Problem](#problem)
- [Target Users](#target-users)
- [Product Goal](#product-goal)
- [Prototype Scope](#prototype-scope)
- [Key Product Decisions](#key-product-decisions)
- [User Flow](#user-flow)
- [Edge Cases & System Dependencies](#edge-cases--system-dependencies)
- [Goals, Signals & Metrics](#goals-signals--metrics)
- [Prototype Stages](#prototype-stages)
- [What This Case Demonstrates](#what-this-case-demonstrates)
- [Related Portfolio Context](#related-portfolio-context)

## Product Context

Patch Management is a product case within the Customer Portal prototype portfolio.

It explores how B2B customers can review scheduled patch maintenance, inspect individual patch runs, and understand device-level processing results in a structured, read-only service experience.

The case focuses on connecting operational information that otherwise appears as separate schedules, execution records and technical resources. It also explores how a customer portal can expose meaningful operational detail without turning the experience into a configuration or execution interface.

## Prototype

The current prototype covers an unbranded, interactive concept for Patch Management and a related Devices area.

| Prototype | Status | Link |
|---|---|---|
| Patch Management – Unbranded Prototype | Available | [Open prototype](./patch-management-unbranded.html) |
| Design System / MVP Reconstruction | Not scoped | — |
| Product Vision | Not scoped | — |

## Problem

Patch maintenance information spans several related objects: recurring schedules, individual runs, affected devices, processing outcomes and reboot requirements.

Without clear relationships between them, customers may struggle to answer questions such as:

- What maintenance is scheduled, and when will it run?
- Which update policy applies to a schedule or run?
- Did a particular run succeed or fail?
- Which devices were included, and what happened to each one?
- Was a reboot completed, still pending or unnecessary?
- How does an individual run relate to its schedule, if any?
- Where can a customer find relevant device information?

The product challenge is to make patch activity understandable and traceable while preserving the operational distinctions that matter.

## Target Users

| User Group | Need |
|---|---|
| Technical customer users | Review patch schedules, execution history and affected devices. |
| Customer administrators | Understand maintenance status, update policies and operational impact. |
| Infrastructure and operations users | Inspect device-level results, package counts and reboot states. |
| Internal support teams | Refer to the same schedule, run and device information when discussing incidents or maintenance. |
| Product and development teams | Review information architecture, edge cases and status semantics before implementation. |

These user groups are design assumptions for the case, not validated research findings.

## Product Goal

The goal is to provide a coherent, read-only Patch Management experience that helps customers move from an overview to the operational details they need.

| Need | Product Implication |
|---|---|
| Maintenance visibility | Show upcoming schedules, intervals, policies and device counts. |
| Execution traceability | Distinguish scheduled maintenance from individual runs and expose run references and results. |
| Device-level clarity | Show processing status, reboot outcome and package information for affected devices. |
| Understandable navigation | Connect schedules, runs and devices through clear list-to-detail journeys. |
| Operational accuracy | Preserve exceptions and distinguish different status dimensions. |

## Prototype Scope

| Area | Covered in Prototype |
|---|---|
| Patch Schedules Overview | Searchable table with schedule name, next run, interval, policy, reboot permission and device count. |
| Schedule Details | General information, update policy, reboot and batch settings, plus Devices and Patch Runs tabs. |
| Patch Runs Overview | Searchable run history with execution status, reference, start/end times, policy and device count. |
| Run Details | Execution information and a device-level results table including processing, reboot and package states. |
| Devices Overview | Searchable technical resource list with project ID, device name, role, product, operating system and IP addresses. |
| Device Details | General information, contract context, credential presentation and a Patches tab. |
| Status Guidance | Legends for run status, device processing, reboot outcome and update policies. |
| Responsive Behaviour | Compact navigation at smaller widths and horizontal scrolling for wide tables. |

The prototype uses illustrative, anonymised data and simulated navigation. It does not execute patches, update schedules or connect to a live patch management backend.

## Key Product Decisions

| Decision | Rationale |
|---|---|
| Separate Patch Schedules from Patch Runs | A recurring maintenance definition is different from an individual execution and its outcome. |
| Connect schedules to their runs and devices | Customers need to move from planned activity to actual execution and affected resources. |
| Support runs without a linked schedule | Manual runs are valid operational records and should not require an invented schedule relationship. |
| Preserve historical device references | A device may no longer exist even though its processing record remains relevant to a past run. |
| Separate run, device and reboot statuses | A successful run, an individual device result and a reboot state answer different questions. |
| Keep update policies visually distinct | Blue, teal and purple policy badges are separate from the green, yellow, red and grey execution states. |
| Use yellow for In Progress and reboot Pending | This distinguishes ongoing operational states from the policy categories shown in the same context. |
| Match legend fills to badge fills | The explanation of each status should visually correspond to its representation in the tables. |
| Keep the experience read-only | The concept prioritises transparency and interpretation rather than configuration or triggering patch operations. |
| Reuse existing portfolio patterns | Tables, badges, tabs and navigation remain consistent with other unbranded portal prototypes. |

## User Flow

The prototype supports three related entry paths: schedule-first, run-first and device-first.

| Step | Description |
|---|---|
| 1. Patch Management Entry | Customer opens the Patch Management area and sees Patch Schedules by default. |
| 2. Schedule Search | Customer searches schedules and compares upcoming maintenance, policies and device counts. |
| 3. Schedule Detail | Customer inspects the schedule's general settings and associated devices. |
| 4. Schedule Runs | Customer switches to the Patch Runs tab to review execution history linked to that schedule. |
| 5. Run Overview | Customer opens the separate Patch Runs list to compare execution statuses and references. |
| 6. Run Detail | Customer inspects a run's schedule reference, settings and per-device results. |
| 7. Status Interpretation | Customer uses processing and reboot legends to interpret individual device outcomes. |
| 8. Devices Entry | Customer opens the Devices area and searches technical resources. |
| 9. Device Detail | Customer reviews device, contract and credential context, then switches to the Patches tab. |
| 10. Return Navigation | Customer returns to the relevant overview from a detail page. |

## Edge Cases & System Dependencies

| Area | Example or Dependency |
|---|---|
| Manual Patch Runs | A run can exist without a linked schedule; the relationship is left unlinked rather than fabricated. |
| Historical Devices | A run may retain a device result even when the original device no longer exists. |
| Mixed Device Outcomes | Device-level failures and processing states require separate presentation from the run-level status. |
| Reboot State | Completed, Pending and Not required are different from device processing outcomes. |
| Disabled Schedules | A disabled schedule should not be presented as having an upcoming run. |
| Update Policy | All updates, Security updates and Check only represent different maintenance intentions. |
| Batch Settings | Schedule and run details expose batch policy and parallel device processing information. |
| Resource Scope | The Devices area can include technical resources that are not shown in a product dashboard. |
| Contract and Credentials | Device details reuse existing contract and credential presentation patterns; no new credential-management flow is implemented. |
| Backend Data | A production implementation would depend on reliable schedule, run, device and result data from operational systems. |

The final dependency is an implementation consideration, not an integration demonstrated by this static prototype.

## Goals, Signals & Metrics

The case defines potential product outcomes and ways to evaluate them in a future implementation.

| Goal | Signal | Potential Metrics |
|---|---|---|
| Improve maintenance visibility | Customers can locate upcoming maintenance and understand schedule settings. | Schedule overview usage, schedule-detail visits, successful schedule lookup rate. |
| Improve execution traceability | Customers can navigate from schedules to runs and interpret run results. | Schedule-to-run navigation rate, run-detail visits, successful run lookup rate. |
| Clarify device-level impact | Customers can identify which devices were affected and how they were processed. | Device-result lookup success, device-detail visits, task-completion rate in usability tests. |
| Improve status comprehension | Customers distinguish run, processing, reboot and policy states correctly. | Status interpretation accuracy in usability tests, related support questions. |
| Reduce repetitive support enquiries | Customers can answer routine maintenance-status questions themselves. | Patch-status support ticket volume, repeat enquiries, self-service resolution rate. |
| Support operational handover | Product, support and technical teams share a consistent view of maintenance records. | Stakeholder feedback, requirements clarified, implementation rework related to missing states. |

These are proposed indicators, not measured results. No customer adoption, support reduction or operational performance outcome has been validated through the prototype.

## Prototype Stages

| Stage | Focus |
|---|---|
| Unbranded | Available interactive read-only concept for schedules, runs, devices, statuses, contextual navigation and responsive presentation. |
| Design System / MVP Reconstruction | Potential future step: integrate with the customer portal design system and refine realistic data, roles and operational messaging; not yet scoped. |
| Product Vision | Potential future exploration of broader maintenance transparency and operational self-service; no confirmed scope or deliverable. |

The current case documents the unbranded stage. Later stages would require separate product decisions and requirements.

## What This Case Demonstrates

| Capability | Evidence in this case |
|---|---|
| B2B service experience design | Translates operational patch data into customer-readable views. |
| Information architecture | Separates schedules, runs and devices while preserving their relationships. |
| Operational product thinking | Represents run outcomes, device processing, reboot requirements and historical exceptions. |
| UX semantics | Distinguishes update policy from execution, device and reboot status through deliberate visual language. |
| Edge-case handling | Includes manual runs without schedules and historical devices that no longer exist. |
| Cross-domain context | Connects patch results to technical resources, contract context and existing credential patterns. |
| Iterative prototyping | Refines badges, legends, navigation and responsive table behaviour through review and QA. |
| Outcome-oriented product thinking | Defines potential signals and metrics without claiming measured impact. |

## Related Portfolio Context

Patch Management is part of the broader Customer Portal prototype portfolio.

It complements API Management's technical self-service journeys and Virtual Network Management's infrastructure relationships with a service-operations perspective: customers need to understand not only what resources they have, but also what maintenance has been planned and performed.

The case is relevant to platform products, B2B customer portals, managed infrastructure services, operational transparency, information architecture, service management and product-to-operations handovers.
