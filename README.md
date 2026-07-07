# Customer Portal Prototype Portfolio

A modular B2B customer portal prototype portfolio demonstrating product thinking, customer self-service journeys, information architecture, MVP scoping, and iterative product evolution.

This repository is not intended as a frontend engineering portfolio.  
Its purpose is to show how complex customer-facing platform capabilities can be structured, prototyped, and evolved from early MVP concepts towards more mature product experiences.

## Table of Contents

- [Product Context](#product-context)
- [How to Read This Repository](#how-to-read-this-repository)
- [Prototype Stages](#prototype-stages)
- [Current Product Areas](#current-product-areas)
  - [Commerce Checkout](#1-commerce-checkout)
  - [API Management](#2-api-management)
  - [Virtual Network Management](#3-virtual-network-management)
- [Product Areas & Roadmap](#product-areas--roadmap)
- [Portal Architecture](#portal-architecture)
- [Goal Signals & Metrics](#goal-signals--metrics)
- [Product Design Principles](#product-design-principles)
- [Portfolio Focus](#portfolio-focus)
- [Related Portfolio Work](#related-portfolio-work)
- [About This Portfolio](#about-this-portfolio)

## Product Context

The Customer Portal represents a modular self-service platform for B2B customers.

It brings together different customer-facing capabilities such as ordering, account activation, service management, API access, and infrastructure-related product administration.

The portfolio is structured around individual product modules. Each module explores a specific customer need, product challenge, and interaction flow within a broader portal ecosystem.

## How to Read This Repository

This repository is structured as a **product portfolio**, not as a collection of isolated mock-ups.

Each module demonstrates:

- customer journey and workflow design
- MVP thinking and scope definition
- information architecture
- interaction patterns
- product decisions and trade-offs
- potential evolution from first implementation to future product vision

The prototypes are intentionally staged to show how a product experience can mature over time.

## Prototype Stages

| Stage | Purpose |
|---|---|
| **Unbranded** | Early product and interaction concept focused on structure, flow, and functionality without final visual branding. |
| **Design System / MVP Reconstruction** | More mature implementation concept aligned with a consistent visual system and realistic product constraints. |
| **Product Vision** | Future-oriented exploration of how the module could evolve beyond the initial MVP. |

Not every module contains all stages yet. The repository will continue to evolve as additional product areas and prototype stages are added.

## Current Product Areas

| Product Area | Status | Product Focus | Case Study | Prototype Stages |
|---|---|---|---|---|
| Commerce Checkout | In progress | Commerce-first ordering journey, guest and logged-in entry states, order wizard optimization, checkout, payment, account activation and order status. | [View case study](./features/commerce-checkout/commerce-checkout-case-study.md) | Unbranded |
| API Management | Available | API activation, API key management, documentation access and developer-oriented self-service. | [View case study](./features/api-management/api-management-case-study.md) | Unbranded |
| Virtual Network Management | Available | Service overview, product details, resource relationships and selected management actions. | [View case study](./features/virtual-network-management/virtual-network-management-case-study.md) | Unbranded, Design System / MVP Reconstruction |

### 1. Commerce Checkout

A commerce-first ordering and checkout flow for B2B customers.

This module explores how customers can move from product configuration and order review into checkout, registration, payment, and order confirmation.

**Product focus**

- B2B checkout journey
- guest-to-customer conversion
- account activation
- payment and contract confirmation
- order status and post-purchase transparency
- reducing friction between purchase intent and customer onboarding

**What this demonstrates**

Commerce Checkout shows how a customer-facing product flow can combine ordering, registration, compliance, payment, and customer communication into one coherent journey.

**Case Study**

| Case Study | Link |
|---|---|
| Commerce Checkout Case Study | [Open case study](./features/commerce-checkout/commerce-checkout-case-study.html) |

**Prototype Links**

| Stage | Link |
|---|---|
| Unbranded | [Open prototype](./commerce-checkout/unbranded/commerce-checkout-unbranded.html) |
| Design System / MVP Reconstruction | In Preparation |
| Product Vision | Coming soon |

### 2. API Management

A self-service module for activating and managing API access.

This module explores how customers can understand API availability, activate access, create and manage API keys, and access relevant documentation.

**Product focus**

- API access activation
- API key management
- customer guidance
- security-sensitive interactions
- developer-oriented self-service
- documentation entry points

**What this demonstrates**

API Management shows how a technical product capability can be translated into a guided customer-facing workflow that balances autonomy, clarity, and security.

**Case Study**

| Case Study | Link |
|---|---|
| API Management Case Study | [Open case study](./features/api-management/api-management-case-study.md) |

**Prototype Links**

| Stage | Link |
|---|---|
| Unbranded | [Open prototype](./api-management/unbranded/api-management-unbranded.html) |
| Design System / MVP Reconstruction | Coming soon |
| Product Vision | Coming soon |

### 3. Virtual Network Management

A self-service module for managing virtual network-related resources.

This module explores how customers can view network services, inspect related products and resources, and perform selected management actions within a structured portal experience.

**Product focus**

- service and product overview
- resource relationships
- detail views
- role-aware actions
- edit flows
- operational transparency

**What this demonstrates**

Virtual Network Management shows how a complex infrastructure-related capability can be translated into a usable customer-facing product module with clear information hierarchy and guided interaction patterns.

**Case Study**

| Case Study | Link |
|---|---|
| Virtual Network Management Case Study | [Open case study](./features/virtual-network-management/virtual-network-management-case-study.md) |

**Prototype Links**

| Stage | Link |
|---|---|
| Unbranded | [Open prototype](./virtual-network-management/unbranded/virtual-network-management-unbranded.html) |
| Design System / MVP Reconstruction | [Open prototype](./virtual-network-management/design-system/virtual-network-management-design-system.html) |
| Product Vision | Coming soon |

## Product Areas & Roadmap

The Customer Portal portfolio is structured around product areas that represent different parts of a modular B2B self-service portal.

Some areas already contain interactive prototypes. Others are planned based on identified customer and portal needs.

| Product Area | Status | Scope |
|---|---|---|
| Commerce Checkout | Current / In progress | Commerce-first ordering journey, guest and logged-in entry states, order wizard optimization, checkout, payment, account activation and order status. |
| API Management | Current / Available | API activation, API key management, documentation access and developer-oriented self-service. |
| Virtual Network Management | Current / Available | Service overview, product details, resource relationships and selected management actions. |
| User, Contacts, Roles & Rights | Planned | User management, bulk actions, contact persons, roles, permissions and access management. |
| My Account & MFA | Planned | Personal data, company data, account settings and multi-factor authentication. |
| Contract Cancellation Flow | Backlog / Exploration | Contract cancellation journey and related confirmation, status and communication flows. |

## Portal Architecture

The Customer Portal is designed as a modular B2B self-service ecosystem.

Each product area focuses on a specific customer need, while shared portal patterns such as navigation, customer account context, status information, permissions, and cross-module guidance create a coherent overall experience.

| Layer | Purpose | Examples |
|---|---|---|
| Portal Entry & Commerce | Helps customers enter the portal experience, understand available products, complete orders, activate accounts and follow order status. | Guest start page, logged-in start page, order wizard optimization, commerce checkout, order status. |
| Product & Service Management | Enables customers to understand and manage booked services and related product resources. | Virtual Network Management, product details, resource relationships, service actions. |
| Developer & Technical Self-Service | Provides guided access to technical capabilities and documentation. | API Management, API activation, API keys, documentation access. |
| Account & Access Management | Supports customer administration, user access, permissions and account security. | User management, bulk actions, contact persons, roles & rights, My Account, MFA. |
| Support & Contract Journeys | Supports service lifecycle moments beyond initial ordering and product management. | Contract cancellation flow, support-related journeys, contract and billing-related self-service. |

The portfolio currently focuses on selected modules from this architecture. The goal is not to show a complete portal implementation, but to demonstrate how individual product areas can be structured, prototyped and connected into a consistent customer-facing platform experience.

## Goal Signals & Metrics

The prototypes are not connected to real analytics data. However, each product area is designed with potential goal signals and product metrics in mind.

| Product Area | Goal Signal | Example Metrics |
|---|---|---|
| Commerce Checkout | Customers can complete an order and activate their account with reduced friction. | Checkout completion rate, registration completion rate, payment success rate, order status page visits, support contacts after checkout. |
| API Management | Customers can activate and manage API access independently. | API activation rate, successful key creation, documentation visits, API-related support tickets, time to first successful API use. |
| Virtual Network Management | Customers can understand services, resources and available actions without support dependency. | Detail page usage, edit flow completion, resource lookup success, support tickets related to network information, task completion rate. |
| User, Contacts, Roles & Rights | Customers can manage users, contacts and access rights transparently. | User management task completion, role update success, contact data completeness, reduced access-related support requests. |
| My Account & MFA | Customers can manage account and security settings independently. | MFA activation rate, profile completion rate, account update success, reduced account-related support requests. |

## Product Design Principles

The prototypes follow a set of product and interaction principles:

1. Clarity before complexity

Complex B2B processes should be broken down into understandable steps, clear states, and guided actions.

2. Self-service where possible

Customers should be able to complete common tasks independently without unnecessary support dependency.

3. Progressive disclosure

Detailed or technical information should be available when needed, but should not overwhelm the main workflow.

4. Operational realism

The prototypes reflect realistic product constraints such as permissions, compliance steps, account activation, payment confirmation, technical dependencies, and system states.

5. Iterative product evolution

The repository intentionally shows different levels of maturity to demonstrate how product experiences can evolve from MVP to more complete product visions.

## Portfolio Focus

This repository demonstrates work across the following product areas:

Product Management
Platform Product Thinking
Customer Experience
B2B Self-Service
Product Discovery
Information Architecture
MVP Definition
Interactive Prototyping
Requirements Structuring
Stakeholder Alignment
Product Evolution
Related Portfolio Work

This Customer Portal focuses on the customer-facing side of a broader digital service ecosystem.

A related portfolio area, Operations Hub, focuses on internal employee-facing workflows and operational service management.

Together, both portfolios demonstrate how customer experience and employee experience can be designed as connected parts of one service ecosystem.

## Related Portfolio Work

This Customer Portal portfolio focuses on the customer-facing side of a modular B2B service ecosystem.

A related portfolio area, [Operations Hub](https://github.com/annika-mann/operations-hub-prototype), focuses on internal employee-facing workflows such as customer management, customer operations, contracts, credentials, reporting and operational service support.

Together, both portfolios demonstrate how customer experience and employee experience can be designed as connected parts of one service ecosystem:

| Portfolio Area | Perspective | Focus |
|---|---|---|
| Customer Portal | Customer-facing | Self-service, ordering, account activation, API access, product management and customer administration. |
| Operations Hub | Employee-facing | Internal workflows, service operations, customer data, contract handling, credentials and operational transparency. |

The long-term portfolio goal is to show how external customer journeys and internal operational workflows can support each other across the same product and service lifecycle.

## About This Portfolio

All prototypes use anonymized data and generic product structures.

The work is intended to demonstrate product thinking, system understanding, customer journey design, and the ability to translate complex business and technical requirements into structured, testable product concepts.
