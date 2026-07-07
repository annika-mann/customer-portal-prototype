# Virtual Network Management Case Study

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
- [Strategic Product Evolution](#strategic-product-evolution)
- [What This Case Demonstrates](#what-this-case-demonstrates)
- [Related Portfolio Context](#related-portfolio-context)

## Product Context

Virtual Network Management is a product case within the Customer Portal prototype portfolio.

It explores how customers can view, create and manage virtual networks and connect them to assigned infrastructure resources through a guided self-service experience.

The case started as a focused product capability for managing virtual networks. Over time, it became a broader product exploration around how CloudHub could evolve from a product-centric dashboard into a more structured infrastructure management experience.

This makes Virtual Network Management both a feature case and a strategic platform case.

It demonstrates how a specific infrastructure capability can become the entry point for rethinking navigation, product hierarchy, resource relationships, project context and the future structure of a B2B cloud portal.

## Prototype

The current prototypes cover both the first functional feature concept and a more mature design-system-aligned reconstruction.

| Prototype | Status | Link |
|---|---|---|
| Virtual Network Management – Unbranded Prototype | Available | [Open prototype](./unbranded/virtual-network-management-unbranded.html) |
| Virtual Network Management – Design System / MVP Reconstruction | Available | [Open prototype](./design-system/virtual-network-management-design-system.html) |
| Product Vision / CloudHub Evolution Basis | Exploration | Coming soon |

## Problem

B2B cloud portals often expose infrastructure products as isolated items.

Customers may be able to see booked products, instances or services, but it is often difficult to understand how these resources relate to each other from an infrastructure perspective.

Virtual networks are a good example of this challenge.

Customers need to understand:

- which virtual networks exist
- which resources are connected
- whether changes are active or still pending
- how network changes affect assigned resources
- where product-level configuration ends and resource-level configuration begins
- whether additional documentation or support is required
- how the network relates to the broader product or project context

At the same time, virtual network changes can be operationally sensitive. They may require asynchronous provisioning, validation, status changes, resource-level configuration, or support involvement when limits are reached.

The product challenge is therefore to make infrastructure relationships understandable and manageable without overwhelming the customer or hiding operational complexity that matters.

## Target Users

| User Group | Need |
|---|---|
| Technical customer users | View and manage virtual networks and connected resources independently. |
| Customer admins | Understand which resources are connected and whether changes are pending or active. |
| Infrastructure-oriented users | Use the portal as a starting point for managing network-related resource relationships. |
| Internal support teams | Reduce repetitive support requests by making network status, limits and next steps clearer. |
| Product and development teams | Discuss how infrastructure capabilities should be represented in the customer portal. |
| Platform stakeholders | Explore how CloudHub could evolve from product management toward infrastructure management. |

## Product Goal

The goal of the Virtual Network Management case is to create a self-service experience that helps customers understand and manage virtual network relationships within the customer portal.

The feature should allow customers to:

- view existing virtual networks
- understand their status
- create new virtual networks
- inspect assigned resources
- add or remove resource connections
- understand pending changes
- access documentation when further configuration is required
- move between network-level and resource-level views

On a strategic level, the case also explores how Virtual Networks could become part of a broader infrastructure management model that connects products, resources, projects, networking and operations into a more coherent customer portal experience.

## Prototype Scope

The prototypes cover the core Virtual Network Management journey and selected resource-level interactions.

| Area | Covered in Prototype |
|---|---|
| Virtual Network Overview | List of virtual networks with status, VLAN ID, description, assigned resources and actions. |
| Search & Filtering | Status filters, search input and search-result highlighting in the table. |
| Create Virtual Network | Create flow with automatic VLAN assignment, optional manual VLAN ID and validation. |
| View Network Details | Drawer-based detail view with description and connected resources. |
| Edit Network | Edit flow for description and assigned resources. |
| Pending Changes | Add and remove resource changes are collected before saving and only applied after confirmation. |
| Remove Network | Removal flow with confirmation and impact messaging. |
| Resource Relationships | Connected resources can be shown from both the Virtual Networks area and the instance detail context. |
| Product Detail Integration | Virtual Networks appear as a tab within an instance detail view. |
| Status Handling | Active and Pending states are represented visually and in interaction logic. |
| Support Limit | When the self-service limit is reached, the customer is guided into a support request flow. |
| Documentation Guidance | The prototype includes guidance that additional configuration may be required on resource level. |

The prototypes are intentionally scoped around product logic, interaction patterns, information hierarchy and handover clarity rather than full technical implementation.

## Key Product Decisions

| Decision | Rationale |
|---|---|
| Represent Virtual Networks as both a standalone area and a product detail tab | Customers may enter the topic from network management or from an individual resource context. Both paths need to make sense. |
| Use a table-based overview | Virtual networks are operational objects. A table makes status, identifiers, descriptions and assigned resources easy to compare. |
| Keep actions close to each network row | View, edit and remove actions need to be available in context. |
| Use drawer-based detail and edit interactions | The customer can inspect or modify a network without losing the overview context. |
| Treat add and remove resource changes as pending until save | Network changes can affect infrastructure relationships and should not be applied accidentally. |
| Show Active and Pending states clearly | Customers need to understand when a network is usable and when changes are still being processed. |
| Include documentation and support paths | Some network tasks require additional resource-level configuration or support involvement. |
| Keep the first implementation focused | The MVP focuses on visibility, creation, assignment and status before expanding into topology, routing or project-level infrastructure management. |
| Connect the feature to a larger platform evolution | Virtual Networks reveals a broader need to rethink Product Dashboard, Products/Resources, Projects, Networking and Operations. |

## User Flow

The prototype follows two main entry paths: a network-first flow and a resource-first flow.

| Step | Description |
|---|---|
| 1. Virtual Networks Entry | Customer enters the Virtual Networks area from the portal navigation. |
| 2. Overview | Customer sees existing virtual networks, status, VLAN IDs, descriptions and assigned resources. |
| 3. Search / Filter | Customer filters by status or searches for a network, VLAN ID or resource. |
| 4. View Network | Customer opens a drawer to inspect the selected virtual network and connected resources. |
| 5. Create Network | Customer creates a new virtual network with automatic or manually entered VLAN ID. |
| 6. Edit Network | Customer edits the description or prepares changes to assigned resources. |
| 7. Add / Remove Resources | Customer selects resources to add or marks existing resource connections for removal. |
| 8. Review Pending Changes | Changes are collected in a pending list before being saved. |
| 9. Save Changes | Saving sets the network status to Pending while changes are processed. |
| 10. Return to Active State | After processing, the network returns to Active. |
| 11. Resource Detail Context | Customer can also view assigned virtual networks from an individual instance detail page. |
| 12. Documentation / Support | Customer is guided to documentation or support where self-service limits or additional configuration apply. |

## Edge Cases & System Dependencies

The case includes selected edge cases because virtual network changes can affect infrastructure relationships and operational stability.

| Area | Example |
|---|---|
| VLAN ID Validation | Manual VLAN IDs must be checked for valid range and duplicates. |
| Self-Service Limit | Customers may reach the maximum number of virtual networks and need to start a support process. |
| Pending Provisioning | Creating or editing a network may temporarily set the network status to Pending. |
| Resource-Level Configuration | Assigned resources may require additional configuration outside the network overview. |
| Add / Remove Consistency | Adding and removing resources should be staged before saving, not applied immediately. |
| Network Removal Impact | Removing a network may remove existing resource connections and requires confirmation. |
| Role-Aware Actions | Some users may only view networks, while others can create, edit or remove them. |
| Documentation Dependency | Customers need guidance for technical steps that cannot be fully handled inside the portal. |
| Product Dashboard Dependency | A broader product vision requires understanding the current Product Dashboard and existing product hierarchy before evolving it. |

These dependencies are intentionally reflected in the prototypes to support better discussion between product, design, development, support and infrastructure stakeholders.

## Goals, Signals & Metrics

The prototype is framed around product outcomes rather than screens alone.

The goal is to make virtual network relationships easier to understand and manage while reducing support dependency and preparing the portal for a more infrastructure-oriented product model.

| Goal | Signal | Potential Metrics |
|---|---|---|
| Improve infrastructure transparency | Customers can see which virtual networks exist and which resources are connected. | Virtual Network overview usage, resource detail visits, assigned resource lookup success, search usage. |
| Increase network self-service adoption | Customers can create and manage virtual networks without contacting support for standard tasks. | Create flow completion rate, edit flow completion rate, resource add/remove completion rate, support tickets related to network setup. |
| Reduce errors in network changes | Customers can review pending add/remove changes before saving. | Cancelled changes before save, failed network updates, number of accidental removals, edit rework rate. |
| Improve status understanding | Customers understand whether a network is active, pending or still being processed. | Pending status page visits, repeated refreshes, “what happens next” support requests, time from Pending to Active. |
| Clarify resource relationships | Customers can navigate between virtual networks and assigned resources. | Click-through between network and resource detail views, resource lookup success, reduced questions about connected resources. |
| Support operational handover | Product, development, support and infrastructure teams can discuss the same interaction model and edge cases. | Clarified requirements before development, documented edge cases, reduced implementation rework, stakeholder review feedback. |
| Prepare platform evolution | The feature provides a concrete starting point for rethinking Product Dashboard, Projects, Resources, Networking and Operations. | Adoption of project filters, usage of infrastructure navigation, engagement with network/resource views, qualitative stakeholder feedback. |

These metrics are intentionally defined as potential indicators. The prototype does not measure them directly, but uses them to frame what a successful implementation would need to improve: infrastructure clarity, customer autonomy, operational reliability and platform scalability.

## Prototype Stages

The Virtual Network Management case is intended to evolve across three prototype stages.

| Stage | Focus |
|---|---|
| Unbranded | First functional self-service concept for virtual network overview, creation, edit, removal, assigned resources, status states and product detail integration. |
| Design System / MVP Reconstruction | Customer-portal-aligned reconstruction with refined navigation, improved tables, search highlighting, status handling, pending changes, dark mode, language switching and more realistic interaction patterns. |
| Product Vision | Broader CloudHub infrastructure management evolution connecting Product Dashboard, Projects, Products/Resources, Networking, Operations and adoption/transition patterns. |

The Product Vision stage is not complete yet. It requires a separate reconstruction of the current Product Dashboard and product hierarchy before the evolution can be shown convincingly.

## Strategic Product Evolution

Virtual Network Management is more than a single feature.

It exposes a larger product question:

How should a cloud customer portal represent infrastructure?

The current product experience is still largely product-centric. Customers move from a product dashboard to product lists and individual product details. Virtual Networks can be added to this structure as a feature, but the topic also reveals that customers may need a more infrastructure-oriented model over time.

The strategic evolution can be understood in four steps:

| Stage | Product Direction | Description |
|---|---|---|
| Current / MVP | Product Dashboard remains central | Virtual Networks are added as a manageable feature within the existing portal structure. |
| Short-Term Evolution | Projects and project filters | Existing product and operations areas remain stable, but project context helps customers understand relationships. |
| Mid-Term Evolution | Networking becomes visible | Networking starts to become its own area, while Operations remains available for familiar service tasks. |
| Long-Term Product Vision | Infrastructure management model | Products evolve toward Resources, Projects become a stronger organizing layer, and Networking becomes a dedicated domain. |
| Adoption / Transition Layer | Soft migration | Old and new navigation paths coexist so customers can learn the new model without losing familiar entry points. |

This evolution should not be treated as a simple navigation redesign. It is a shift in the mental model of the portal.

The long-term product challenge is to help customers move from Products as isolated items towards Projects, resources and networks as connected infrastructure systems

A Product Dashboard reconstruction is therefore a required next step for the Product Vision stage. Without showing the current dashboard and product hierarchy first, the future infrastructure model would lack context.

## What This Case Demonstrates

This case highlights the product capabilities behind the Virtual Network Management prototype.

| Capability | Evidence in this case |
|---|---|
| Platform product thinking | Connects a specific infrastructure feature to a broader portal and infrastructure strategy. |
| Infrastructure self-service design | Makes network-related tasks understandable and manageable for customers. |
| Product hierarchy analysis | Explores how products, resources, projects and networks relate to each other. |
| Information architecture | Structures complex infrastructure concepts into usable portal areas. |
| Operational realism | Reflects status states, pending changes, limits, validation and support paths. |
| Product evolution | Moves from MVP feature implementation toward a broader infrastructure management model. |
| Stakeholder alignment | Uses prototypes to support product, development, support and infrastructure discussions. |

## Related Portfolio Context

Virtual Network Management is one product area within the broader Customer Portal prototype portfolio.

It connects to other portal areas such as Commerce Checkout, API Management, User Management, My Account, MFA and future contract-related journeys.

Within the portfolio, this case has a specific role:

Commerce Checkout demonstrates customer journey and conversion thinking.
API Management demonstrates technical self-service and developer-oriented product thinking.
Virtual Network Management demonstrates infrastructure platform thinking and product architecture evolution.

The case is especially relevant for roles focused on platform products, infrastructure services, B2B self-service, cloud portals, customer experience, product discovery, information architecture and long-term product evolution.
