# API Management Case Study

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

API Management is a product case within the Customer Portal prototype portfolio.

It explores how B2B customers can activate API access, understand API availability, create and manage API keys, and access relevant documentation through a guided self-service experience.

The case focuses on translating a technical platform capability into a customer-facing product flow that is understandable, secure and operationally realistic.

Instead of treating API access as a purely technical configuration task, the prototype frames it as a product journey: customers need to understand what is available, what needs to be activated, what security implications exist, and where to find documentation and next steps.

## Prototype

The current prototype focuses on the unbranded MVP flow for API activation and API key management.

| Prototype | Status | Link |
|---|---|---|
| API Management – Unbranded Prototype | Available | [Open prototype](./api-management-unbranded.html) |
| Design System / MVP Reconstruction | Planned | In Preperation |
| Product Vision | Planned | Coming soon |

## Problem

Technical self-service areas in B2B portals are often difficult for customers to navigate.

API access may be available, but customers may not understand:

- whether API access is already active
- how to activate API usage
- how API keys are created
- how credentials should be handled securely
- where documentation can be found
- what happens after activation
- which permissions or roles are required

At the same time, API access is security-sensitive. The product experience needs to support self-service without making risky actions too easy, unclear or uncontrolled.

The product challenge is therefore to design an API Management experience that gives customers autonomy while still providing guidance, structure, security awareness and operational traceability.

## Target Users

| User Group | Need |
|---|---|
| Technical customer users | Activate API access, create API keys and access documentation without contacting support. |
| Customer admins | Understand API availability, permissions and security-sensitive actions. |
| Developers / integration teams | Find credentials, documentation and next steps quickly. |
| Internal support teams | Reduce repetitive API onboarding questions and guide customers to self-service. |
| Product and development teams | Review the API onboarding flow, security states and activation logic before implementation. |

## Product Goal

The goal of the API Management case is to create a guided self-service experience for API activation and API key management.

The flow should help customers understand API access status, complete activation, create initial API keys, access documentation and manage sensitive technical credentials with clarity and confidence.

The product should balance three needs:

| Need | Product Implication |
|---|---|
| Customer autonomy | Customers should be able to activate and manage API access independently. |
| Security awareness | Sensitive actions such as API key creation should be clearly framed and role-aware. |
| Operational clarity | Internal teams should have fewer support requests and clearer activation states. |

## Prototype Scope

The unbranded prototype covers the core API Management journey and related customer states.

| Area | Covered in Prototype |
|---|---|
| API Overview | Customer can see API availability, access status and relevant next steps. |
| API Activation | Customer can start an activation process for API access. |
| Initial API Key Creation | Customer is guided to create the first API key after activation. |
| API Key Management | Customer can view existing keys, create new keys and understand key-related actions. |
| Documentation Access | Customer can access API documentation from the management area. |
| Security Guidance | Sensitive actions are framed with clear guidance and status information. |
| Empty / Initial States | The prototype includes states where no API key exists yet and the customer needs to take the first action. |

The prototype is intentionally unbranded to focus on product logic, activation flow, information hierarchy and handover clarity rather than final visual brand execution.

## Key Product Decisions

| Decision | Rationale |
|---|---|
| Treat API Management as a guided product flow | Customers should not have to interpret technical backend states without guidance. |
| Separate activation from key creation | API access activation and API key creation are related but distinct customer actions. |
| Include an initial empty state | Customers need clear guidance when API access exists but no key has been created yet. |
| Link documentation directly from the product area | API documentation should be available at the moment customers need it. |
| Make security-sensitive actions explicit | API key creation and management require clear labels, states and user awareness. |
| Use status-based guidance | Customers should understand whether API access is inactive, active, incomplete or ready to use. |
| Keep the MVP focused | The first version should support activation, key creation and documentation access before expanding into advanced analytics or governance. |

## User Flow

The prototype follows a guided API onboarding and management journey.

| Step | Description |
|---|---|
| 1. API Management Entry | Customer enters the API Management area from the portal navigation. |
| 2. API Status Overview | Customer sees whether API access is available, inactive, active or requires setup. |
| 3. Activation Start | Customer starts API activation if access is not yet active. |
| 4. Activation Confirmation | Customer confirms the activation and receives guidance on what happens next. |
| 5. Initial API Key State | Customer sees that no API key exists yet and is prompted to create the first key. |
| 6. API Key Creation | Customer creates an API key through a guided dialog or flow. |
| 7. API Key Overview | Customer can view existing keys and key metadata. |
| 8. Documentation Access | Customer can open API documentation to continue integration work. |
| 9. Ongoing Management | Customer can return to manage keys or create additional keys depending on permissions. |

## Edge Cases & System Dependencies

The case includes selected edge cases because API access is both technical and security-sensitive.

| Area | Example |
|---|---|
| No API Access Active | Customer has access to the page but API usage has not yet been activated. |
| No API Key Exists | API access is active, but no key has been created yet. |
| Permission Restrictions | Some users may be able to view API information but not create or manage keys. |
| Key Visibility | API keys may only be visible once or may require special handling after creation. |
| Documentation Dependency | Customers need the correct documentation entry point for successful integration. |
| Security Communication | Customers need clear information about handling credentials responsibly. |
| Support Dependency | Without clear guidance, customers may contact support for activation or key creation. |

These dependencies are intentionally reflected in the prototype to support better discussion between product, design, development, security and support stakeholders.

## Goals, Signals & Metrics

The prototype is framed around product outcomes rather than screens alone.

The goal is to make API access easier to activate and manage while reducing unnecessary support dependency and keeping sensitive actions understandable and secure.

| Goal | Signal | Potential Metrics |
|---|---|---|
| Increase API self-service adoption | Customers can activate API access without contacting support. | API activation rate, activation completion rate, number of API activations started vs. completed. |
| Improve time to first API use | Customers can create an initial API key and access documentation quickly. | Time to first API key, time to first successful API request, documentation click-through rate. |
| Reduce API onboarding support requests | Customers understand activation, key creation and next steps from the portal flow. | Number of API onboarding tickets, support contacts after activation, repeated questions related to API setup. |
| Improve clarity of API status | Customers can understand whether API access is inactive, active, incomplete or ready to use. | Status page engagement, failed activation attempts, user feedback on API setup clarity. |
| Support secure credential handling | Customers understand the sensitivity of API keys and the implications of key creation. | Key creation success rate, key regeneration requests, security-related support tickets, audit log events. |
| Improve stakeholder handover | Product, development, security and support can review the same activation and key management flow. | Clarified requirements before development, documented edge cases, reduced implementation rework, stakeholder review feedback. |

These metrics are intentionally defined as potential indicators. The prototype does not measure them directly, but uses them to frame what a successful implementation would need to improve: customer autonomy, onboarding clarity, security awareness and operational efficiency.

## Prototype Stages

The API Management case is intended to evolve across three prototype stages.

| Stage | Focus |
|---|---|
| Unbranded | API activation, initial API key creation, empty states, API key overview and documentation access. |
| Design System / MVP Reconstruction | Branded customer portal integration, consistent navigation, refined status states, realistic security messaging and role-aware interactions. |
| Product Vision | Advanced API self-service with usage insights, key lifecycle management, audit visibility, integration guidance, alerts and broader developer experience improvements. |

These iterations move the prototype from a focused activation and key creation flow toward a broader API self-service and developer experience area within the customer portal.

## What This Case Demonstrates

This case highlights the product capabilities behind the API Management prototype.

| Capability | Evidence in this case |
|---|---|
| Technical self-service design | Translates API activation and key management into a guided customer-facing workflow. |
| Platform product thinking | Frames API access as part of a broader customer portal and developer experience. |
| Information architecture | Structures API status, activation, key creation and documentation access into one understandable product area. |
| Security-sensitive interaction design | Makes API key creation, credential handling and permission-related actions more explicit and controlled. |
| MVP scoping | Focuses the first prototype on activation, initial key creation, key overview and documentation access. |
| Support reduction | Designs the flow to reduce repetitive API onboarding questions and guide customers toward self-service. |
| Outcome-oriented product thinking | Defines goals, signals and potential metrics around activation, time to first API use, support reduction and security awareness. |
| Stakeholder alignment | Uses the prototype to support product, development, security and support discussions before implementation. |

## Related Portfolio Context

API Management is one product area within the broader Customer Portal prototype portfolio.

It connects to other portal areas such as Commerce Checkout, Virtual Network Management, User Management, Roles & Rights, My Account and MFA.

The case is especially relevant for roles focused on platform products, B2B self-service, technical customer journeys, developer experience, API products, customer portals and product-led operational efficiency.
