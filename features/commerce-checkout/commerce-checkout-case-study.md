# Commerce Checkout Case Study

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

Commerce Checkout is a product case within the Customer Portal prototype portfolio.

It explores a commerce-first B2B checkout journey for customers who want to configure, review and purchase a cloud-related service before or during account creation.

Unlike a simple consumer checkout, this flow has to balance customer convenience with B2B SaaS requirements such as account activation, company data, payment authorization, duplicate checks, fraud signals, compliance review, contract confirmation and operational status communication.

The case demonstrates how a complex ordering and onboarding journey can be structured into a clear, guided and testable product flow.

## Prototype

The current prototype focuses on the unbranded MVP flow for a commerce-first B2B checkout journey.

| Prototype | Status | Link |
|---|---|---|
| Commerce Checkout – Unbranded Prototype | Available | [[Open prototype](./features/commerce-checkout/commerce-checkout-unbranded.html) |
| Design System / MVP Reconstruction | Planned | In Preparation |
| Product Vision | Planned | Coming soon |

## Problem

Traditional B2B customer portals often assume that a customer account already exists before a user can order or manage services.

This creates friction for new customers because registration, company data, product configuration, contract confirmation and payment may be separated into different steps, systems or communication flows.

At the same time, B2B checkout cannot be reduced to a simple consumer-style payment process. It needs to account for operational and compliance-related requirements such as company validation, duplicate account detection, payment authorization, fraud signals, sanctions checks, contract confirmation and provisioning status.

The product challenge is therefore to reduce visible customer friction while still supporting the checks, dependencies and operational steps required behind the scenes.

## Target Users

| User Group | Need |
|---|---|
| New customers | Complete a first order without going through a long separate registration process before checkout. |
| Existing customers | Order additional services faster by reusing known account, company and billing information. |
| Internal operations teams | Receive structured order, customer and payment information for validation, provisioning and follow-up. |
| Product and development teams | Review the complete customer journey, including edge cases and system dependencies, before implementation. |

## Product Goal

The goal of the Commerce Checkout case is to design a more integrated B2B ordering experience that allows customers to move from product configuration to order completion with fewer disconnected steps.

The flow should make the customer journey feel simple and guided while still allowing operational checks, payment authorization, account activation and compliance-related processes to happen reliably in the background.

## Prototype Scope

The unbranded prototype covers the core checkout journey and related exception states.

| Area | Covered in Prototype |
|---|---|
| Ordering Journey | Product configuration, order review, checkout and payment. |
| Portal Entry States | Guest start page, logged-in start page and first customer dashboard entry points. |
| Customer Onboarding | Account details, company data, billing data and email verification. |
| Payment & Authorization | Payment selection, payment authentication and authorization states. |
| Status & Transparency | Order success, order status, pending states and review states. |
| Risk & Operations | Duplicate match handling, compliance review and operational review states. |

The prototype is intentionally unbranded to focus on product logic, user flow, dependencies and handover clarity rather than final visual brand execution.

## Key Product Decisions

| Decision | Rationale |
|---|---|
| Use a commerce-first flow | Customers should be able to start from product intent and move into checkout without being forced into a separate registration journey first. |
| Combine account, company, billing and payment data into one structured checkout | Reduces fragmentation and gives the customer a clearer sense of progress. |
| Keep operational checks in the background where possible | Duplicate checks, fraud signals and compliance review should not unnecessarily complicate the visible customer journey. |
| Support clear post-checkout status communication | Customers need to understand what happens after payment authorization and account activation. |
| Include edge cases in the prototype | Duplicate matches, pending reviews and payment authentication are part of the real product experience and should be visible during product discussion. |
| Connect checkout to the broader portal experience | Guest and logged-in entry states show how checkout fits into a larger customer portal ecosystem. |

## User Flow

The prototype follows a commerce-first journey from product intent to post-order status.

| Step | Description |
|---|---|
| 1. Start Page / Entry | Customer enters through a guest or logged-in portal entry state. |
| 2. Product Configuration | Customer configures the selected product or service. |
| 3. Order Review | Customer reviews product configuration, price, contract information and next steps. |
| 4. Checkout | Customer provides account, company, billing and payment information. |
| 5. Payment Authorization | Payment is selected and authenticated where required. |
| 6. Account Activation / Verification | Email verification and account activation are handled as part of the onboarding process. |
| 7. Order Success / Status | Customer receives confirmation and can understand order status, pending checks or next steps. |
| 8. Operational Review States | Duplicate match, compliance review or manual verification states are represented as part of the broader flow. |

## Edge Cases & System Dependencies

The case includes selected edge cases because they are critical to a realistic B2B checkout experience.

| Area | Example |
|---|---|
| Duplicate Detection | A company or customer may already exist and require review before account activation. |
| Payment Authentication | Payment may require additional authentication or authorization before the order can proceed. |
| Compliance Review | Some orders may require sanctions, fraud or operational checks before activation. |
| Pending Status | Customers need clear communication when an order cannot be completed immediately. |
| Account Activation | Email verification and account creation need to align with the order journey. |
| Internal Handover | Operations teams need enough structured information to review, approve, reject or follow up on an order. |

These dependencies are intentionally reflected in the prototype to support better discussion between product, design, development, operations and compliance stakeholders.

## Goals, Signals & Metrics

The prototype is framed around product outcomes rather than screens alone.

The goal is to improve the first purchase journey while keeping the flow reliable, compliant and suitable for B2B SaaS requirements.

| Goal | Signal | Potential Metrics |
|---|---|---|
| Reduce friction for new customers | Customers can configure, review and complete an order without going through a long separate registration process first. | Checkout completion rate, drop-off rate per step, time to complete first order, abandoned checkout rate. |
| Create a more modern B2B checkout experience | Account, company, billing and payment data are collected in one structured journey instead of several disconnected forms. | Number of visible customer steps, form completion time, support requests during checkout, customer feedback on checkout clarity. |
| Support both guest and existing customer journeys | New customers can enter through a commerce-first flow, while existing customers can reuse known account and company data for additional orders. | Share of orders from new vs. existing customers, repeat order completion rate, amount of prefilled data reused, logged-in checkout completion rate. |
| Keep operational and compliance requirements in the background | Duplicate checks, fraud signals, compliance review and payment risk handling can run without making the customer journey unnecessarily complex. | Orders requiring manual review, duplicate account detection rate, fraud/compliance review time, blocked or delayed order rate. |
| Improve order transparency after checkout | Customers receive clear success, pending or order status communication after payment authorization and verification. | Order status page usage, “what happens next” support requests, provisioning status visibility, time from checkout to activation. |
| Make the flow easier to review and hand over | Product, design, development and operations can discuss the same end-to-end journey, including edge cases and system dependencies. | Clarified requirements before development, reduced rework during implementation, documented edge cases, stakeholder review feedback. |

These metrics are intentionally defined as potential indicators. The prototype does not measure them directly, but uses them to frame what a successful implementation would need to improve: customer completion, flow clarity, operational reliability and handover quality.

## Prototype Stages

The Commerce Checkout case is intended to evolve across three prototype stages.

| Stage | Focus |
|---|---|
| Unbranded | First-purchase checkout journey, consolidated data entry, payment, verification, order status and operational edge cases. |
| Design System / MVP Reconstruction | Branded customer portal integration, guest and logged-in start pages, clearer portal navigation and realistic visual alignment. |
| Product Vision | Logged-in commerce experience, personalized portal entry, active products, reused customer data, product-specific order wizards and lifecycle actions such as upgrades, changes or cancellations. |

These iterations move the prototype from an integrated first-purchase checkout toward a broader customer portal commerce experience.

## What This Case Demonstrates

This case highlights the product capabilities behind the Commerce Checkout prototype.

| Capability | Evidence in this case |
|---|---|
| Customer journey design | Structures the first-purchase journey from product intent to checkout, account activation and order status. |
| B2B commerce thinking | Balances checkout simplicity with company data, billing, payment, contract and compliance requirements. |
| MVP scoping | Focuses the first prototype on the core ordering and onboarding journey plus relevant exception states. |
| Operational realism | Reflects duplicate checks, payment authorization, compliance review, pending states and internal handover needs. |
| Outcome-oriented product thinking | Defines goals, signals and potential metrics around completion, friction, transparency and support reduction. |
| Stakeholder alignment | Uses an interactive prototype to make product, design, development, operations and compliance discussions concrete. |
| Product evolution | Moves from an unbranded first-purchase checkout toward a broader logged-in commerce and portal experience. |

## Related Portfolio Context

Commerce Checkout is one product area within the broader Customer Portal prototype portfolio.

It connects to other portal areas such as API Management, Virtual Network Management, User Management, My Account, MFA, and future contract-related journeys.

The case is especially relevant for roles focused on customer-facing platforms, B2B self-service, digital commerce, product discovery, customer experience, and platform product management.
