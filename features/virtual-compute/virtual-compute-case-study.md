# Virtual Compute Case Study

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

Virtual Compute is a product case within the Customer Portal prototype portfolio.

It explores how customers can order a Cloud Project, understand the relationship between contractual products and runtime resources, and deploy and manage Virtual Machines through a guided self-service experience.

The case started with a concrete product requirement: introduce Virtual Machine ordering and management into an existing B2B customer portal. During discovery, it became clear that the feature could not be represented convincingly as a single order form or an isolated table. The experience needed to distinguish between three connected but different layers:

- the **Cloud Project** as the contractual and organizational container
- the **Virtual Machine** as a configurable runtime resource
- the **Virtual Network** as shared infrastructure connected to one or more resources

This makes Virtual Compute both a feature case and a product-model case.

It demonstrates how a technically complex infrastructure concept can be translated into a coherent customer journey spanning commerce, product management, resource configuration, operational status and usage transparency.

## Prototype

The current prototype covers the first functional product concept for ordering and managing Virtual Compute resources.

| Prototype | Status | Link |
| --- | --- | --- |
| Virtual Compute – Unbranded Prototype | Available | [Open prototype](virtual-compute-unbranded.html) |
| Virtual Compute – Design System / MVP Reconstruction | Planned | Coming soon |
| Product Vision / Infrastructure Management Evolution | Exploration | Coming soon |

The unbranded prototype is intentionally focused on product logic, information hierarchy, interaction patterns and stakeholder alignment. It is not a representation of a final visual design.

## Problem

B2B cloud portals often present infrastructure products as separate commercial or technical objects.

Customers may be able to order a product, see an active contract or access a resource list, but the relationship between these layers is not always clear. For Virtual Compute, customers need to understand:

- what they are ordering at contract level
- which Cloud Project contains their resources
- which Virtual Machines belong to that project
- which networks are connected to which machines
- which configuration changes affect price
- whether a resource is active, stopped or still being provisioned
- where product-level configuration ends and resource-level management begins
- how usage and consumption relate to the active configuration
- where support or documentation is required

At the same time, Virtual Machine provisioning is not an instant front-end action. It may involve asynchronous backend processing, quota validation, image and flavor availability, IP allocation, network assignment, billing integration and status transitions.

The product challenge is therefore to make infrastructure ordering and management understandable without hiding the operational complexity that customers need in order to make informed decisions.

## Target Users

| User Group | Need |
| --- | --- |
| Technical customer users | Deploy and manage Virtual Machines without relying on support for standard tasks. |
| Customer admins | Understand which projects and resources exist, how they are configured and what they may cost. |
| Infrastructure-oriented users | Manage compute, network and usage relationships within a clear project context. |
| Finance- or contract-aware users | Understand where a contractual product ends and usage-based resource costs begin. |
| Internal support teams | Reduce repetitive requests by making configuration, status, relationships and next steps clearer. |
| Product and development teams | Align on the product model, system boundaries, interaction logic and open implementation questions. |
| Platform stakeholders | Explore how the customer portal can evolve from product lists toward connected infrastructure management. |

## Product Goal

The goal of the Virtual Compute case is to create a coherent self-service experience for ordering and managing compute infrastructure in the customer portal.

The experience should allow customers to:

- configure and order a Cloud Project
- understand that the Cloud Project becomes the contractual and organizational container
- view all existing Cloud Projects in one overview
- open a project and inspect its configuration
- view, search and filter Virtual Machines
- deploy a new Virtual Machine within an existing project
- understand the price impact before confirming deployment
- inspect machine-level configuration and operational status
- start, stop, restart, edit or remove a Virtual Machine
- understand network assignments
- move between Virtual Machine and Virtual Network contexts
- inspect usage information and understand its current limitations
- access documentation or support where self-service is insufficient

On a strategic level, the case also explores how Virtual Compute, Virtual Networks, Projects, Products, Usage and Operations could become parts of one coherent infrastructure-management model.

## Prototype Scope

The prototype covers the core Cloud Project and Virtual Machine journeys and selected infrastructure relationships.

| Area | Covered in Prototype |
| --- | --- |
| Order Wizard | Guided configuration of a new Cloud Project before entering the separate commerce checkout flow. |
| Cloud Project Configuration | Project name, region and contract assignment. |
| Configuration Summary | Persistent summary of selected configuration and the distinction between base price and usage-based resources. |
| Product Overview | Table of existing Virtual Compute projects with region, VM count and project status. |
| Project Details | Instance-level page with product context, configuration summary and tabs for related domains. |
| Virtual Machine Overview | VM table with status, operating system, flavor, IPs, network and actions. |
| Search & Filtering | Search combined with status-based quick filters for Virtual Machines. |
| Create Virtual Machine | Two interaction variants: a guided stepper and a one-page form for comparison. |
| Configuration Options | Operating system, flavor, storage, network and public-IP configuration. |
| Price Transparency | Confirmation step showing illustrative hourly and monthly price impact before provisioning. |
| Resource Status | Running, stopped and processing states. |
| VM Actions | View, start, stop, restart, edit configuration, manage firewall and delete. |
| VM Details | Drawer with configuration overview, firewall, consumption, console log and activity tabs. |
| Virtual Network Integration | Reuse of the Virtual Network Management pattern and shared resource relationships. |
| Usage | Initial structure for project- and resource-level consumption data. |
| Additional Product Tabs | Access, Monitoring, Logs and Tickets included as structural placeholders for the broader product context. |

The prototype intentionally stops before reproducing the complete checkout journey. Order Review, Checkout and Order Overview are covered by the separate Commerce Checkout case and are referenced rather than duplicated.

## Key Product Decisions

| Decision | Rationale |
| --- | --- |
| Separate Cloud Project ordering from Virtual Machine deployment | The Cloud Project is the contractual container, while Virtual Machines are runtime resources created after the project exists. Combining both into one flow would blur product and resource responsibilities. |
| Reuse the existing Commerce Checkout flow after configuration | Contract review, account details, payment and order status already exist as a separate portfolio case. Reusing that journey avoids inconsistent duplicate concepts. |
| Use Products as the main entry point for existing projects | Customers need a stable overview of their contractual Virtual Compute instances before entering resource management. |
| Make the entire project row clickable | The project is the primary object in the overview. A row-level interaction creates a clear path to its details while the VM count remains a secondary shortcut. |
| Use Product → Instance → Details as the hierarchy | The breadcrumb reflects the existing customer-portal product model while still preparing the experience for a more infrastructure-oriented future. |
| Treat the Cloud Project as the resource boundary | Virtual Machines and Virtual Networks belong to a project context. This gives customers a comprehensible container for related infrastructure. |
| Use tabs for project-level domains | Information, VMs, networks, access, monitoring, usage, logs and tickets belong to one project but serve different tasks. Tabs preserve context without mixing unrelated actions. |
| Provide both stepper and one-page Create VM variants | The prototype is also a decision tool. Both variants allow stakeholders to compare guidance, density and speed before selecting a final interaction model. |
| Keep price confirmation separate from configuration | Usage-based infrastructure can create ongoing costs. A dedicated confirmation step makes the financial impact visible before provisioning begins. |
| Reuse Virtual Network Management components and data | Compute and network resources represent the same underlying infrastructure relationships. Shared patterns reduce conceptual fragmentation and support future component reuse. |
| Show operational states directly in tables and details | Customers need to know whether a resource is running, stopped or still being processed before taking further action. |
| Keep usage values illustrative in the first prototype | The intended information structure can be explored before data availability, billing precision and aggregation rules are fully confirmed. |
| Keep the first implementation focused | The prototype prioritizes ordering, project context, VM deployment, status, actions, network relationships and price transparency before expanding into advanced orchestration. |

## User Flow

The prototype follows two connected journeys: Cloud Project ordering and Virtual Machine management.

| Step | Description |
| --- | --- |
| 1. Order Wizard Entry | Customer starts a new Virtual Compute order from the portal navigation or project overview. |
| 2. Configure Cloud Project | Customer enters a project name and reviews the role of the project as a resource container. |
| 3. Select Region | Customer chooses the region in which the project and resources will be created. |
| 4. Assign Contract | Customer chooses a new Contract ID or an eligible existing contract. |
| 5. Review Configuration Summary | Customer sees the selected values and the distinction between the Cloud Project base price and usage-based resources. |
| 6. Continue to Commerce Flow | Customer continues to Order Review, Checkout and Order Overview in the separate Commerce Checkout journey. |
| 7. Open Product Overview | After provisioning, the customer sees the Virtual Compute project in the Products overview. |
| 8. Open Project Details | Customer opens the project and sees its product context, project data and related tabs. |
| 9. View Virtual Machines | Customer opens the VM tab, searches, filters and reviews current resources. |
| 10. Create Virtual Machine | Customer starts either the stepper or one-page configuration variant. |
| 11. Configure Resource | Customer selects operating system, flavor, storage, network and public-IP options. |
| 12. Review Price Impact | Customer reviews illustrative hourly and monthly costs before confirming. |
| 13. Start Provisioning | The new Virtual Machine enters a processing state while backend provisioning runs. |
| 14. Manage Resource | Once available, the customer can inspect, start, stop, restart, edit or delete the Virtual Machine. |
| 15. Inspect Related Network | Customer can view network assignments from the VM context or open the Virtual Networks tab. |
| 16. Review Usage | Customer can inspect the intended consumption structure and understand where data limitations still exist. |
| 17. Use Documentation or Support | Customer is guided to further help when configuration, quota or operational issues exceed self-service scope. |

## Edge Cases & System Dependencies

The case includes selected edge cases and dependencies because compute infrastructure is affected by commercial, technical and operational systems.

| Area | Example |
| --- | --- |
| Project Provisioning | A newly ordered Cloud Project may not be immediately available after checkout. |
| Region Availability | Images, flavors, networks or capacity may differ by region. |
| Contract Assignment | Only eligible contracts should be available for assignment. |
| Project Name Validation | Project names may require uniqueness, character and length rules. |
| Resource Quotas | VM count, vCPU, RAM, storage or public-IP limits may block provisioning. |
| Image Availability | Operating-system images may be deprecated, restricted or temporarily unavailable. |
| Flavor Availability | A selected flavor may not have sufficient regional capacity. |
| Network Dependency | VM creation depends on an available and valid network assignment. |
| Public IP Allocation | A public IP may be optional, limited, unavailable or billed separately. |
| Asynchronous Provisioning | A confirmed VM may remain in Processing before becoming Running or returning an error. |
| Action Eligibility | Start, stop, restart, edit or delete actions depend on the current VM status. |
| Configuration Changes | Some changes may require restart, reprovisioning or a new price confirmation. |
| Price Calculation | Estimated costs depend on active configuration, runtime, billing units and applicable product conditions. |
| Usage Data | Availability, freshness, aggregation and VM-level mapping require confirmed backend data. |
| Role-Aware Actions | Some users may only view resources, while others can create, edit or delete them. |
| Auditability | Operational actions should create activity or log entries that support traceability. |
| Support Dependency | Failed provisioning, quota increases or infrastructure incidents may require a ticket. |
| Commerce Dependency | The project order depends on the separate Order Review, Checkout and Order Overview flow. |
| Virtual Network Dependency | VM and network views should use the same relationship data to avoid contradictory resource assignments. |

These dependencies are intentionally visible in the prototype because they support more realistic alignment between product, development, infrastructure, billing, support and design stakeholders.

## Goals, Signals & Metrics

The case is framed around product outcomes rather than screens alone.

The goal is to make compute infrastructure easier to order, understand and manage while reducing avoidable support dependency and improving transparency around resource relationships, status and cost.

| Goal | Signal | Potential Metrics |
| --- | --- | --- |
| Clarify the product model | Customers understand the difference between Cloud Project, Virtual Machine, Virtual Network and contract. | Successful navigation between project and resource views, reduced terminology-related support questions, task-comprehension testing. |
| Increase self-service adoption | Customers deploy and manage standard Virtual Machines without contacting support. | Create VM completion rate, successful start/stop/restart actions, self-service action rate, related support-ticket volume. |
| Improve configuration success | Customers complete valid VM configurations with fewer corrections. | Form-error rate, abandoned configurations, validation failures, provisioning success rate, configuration rework. |
| Improve price transparency | Customers understand the expected price impact before creating or changing resources. | Price-confirmation completion, cancellations before confirmation, billing-related support requests, qualitative confidence feedback. |
| Improve status understanding | Customers understand whether resources are running, stopped or still processing. | Repeated refreshes, status-related support questions, time spent in details, failed action attempts. |
| Clarify infrastructure relationships | Customers can understand which VMs and networks belong to a project and how they relate. | Click-through between VM and network views, network lookup success, reduced questions about resource assignment. |
| Improve operational control | Customers can perform appropriate VM actions in context. | Action completion rate, failed or reversed actions, accidental deletions, use of activity and log views. |
| Improve usage transparency | Customers can connect resource configuration with actual consumption. | Usage-tab visits, VM-level usage drill-down, billing-data lookup success, usage-related support requests. |
| Support product and technical alignment | Stakeholders discuss the same product model, user flow and system boundaries before implementation. | Resolved open questions, documented dependencies, reduced implementation rework, stakeholder review feedback. |
| Prepare platform evolution | The case establishes Projects and Resources as connected infrastructure concepts. | Adoption of project context, usage of cross-resource navigation, qualitative validation of the future information architecture. |

These metrics are potential indicators. The prototype does not measure them directly, but uses them to define what a successful implementation would need to improve: customer autonomy, conceptual clarity, configuration quality, cost awareness and operational reliability.

## Prototype Stages

The Virtual Compute case is intended to evolve across three prototype stages.

| Stage | Focus |
| --- | --- |
| Unbranded | First functional concept for Cloud Project ordering, project overview, VM deployment, VM management, network relationships, usage structure and price transparency. |
| Design System / MVP Reconstruction | Customer-portal-aligned reconstruction with refined components, validated terminology, production-oriented states, responsive behavior, accessibility and final interaction decisions. |
| Product Vision | Broader infrastructure-management evolution connecting Projects, Resources, Networking, Usage, Operations and commerce into a coherent platform model. |

The current unbranded stage deliberately includes unresolved and comparative elements, such as the two Create VM variants. This allows the prototype to function as a discovery and decision-making tool rather than presenting an unvalidated solution as final.

## Strategic Product Evolution

Virtual Compute is more than a new product page.

It exposes a broader product question:

**How can a technically complex cloud infrastructure concept become a coherent and usable self-service product?**

The current portal model is still largely product-centric. Customers order contractual products and then navigate into their details. Virtual Compute can be introduced within that model, but the resource relationships revealed by the case suggest a gradual evolution toward a more infrastructure-oriented experience.

| Stage | Product Direction | Description |
| --- | --- | --- |
| Current / MVP | Product and instance hierarchy remains central | Virtual Compute is introduced through the existing Products structure. Cloud Projects act as contractual instances and contain runtime resources. |
| Short-Term Evolution | Stronger project context | Project names and identifiers become visible across compute, networking, usage, tickets and operations so customers can understand related resources. |
| Mid-Term Evolution | Resources become a clearer product layer | Virtual Machines, networks, IPs and storage are represented as connected resources rather than isolated product details. |
| Long-Term Product Vision | Infrastructure management model | Projects become the organizing layer, Resources become a shared domain, Networking becomes a dedicated domain and Usage connects technical activity with commercial transparency. |
| Adoption / Transition Layer | Familiar and new paths coexist | Existing Product Dashboard and Products entry points remain available while customers learn project- and resource-oriented navigation. |

This evolution should not be treated as a navigation redesign alone. It changes the mental model of the portal.

The long-term challenge is to help customers move from seeing **products as isolated contractual items** toward understanding **projects, machines, networks, usage and operations as one connected infrastructure system**.

Virtual Compute provides a particularly useful foundation for that evolution because it connects the commercial entry point, the infrastructure container, the runtime resource and the operational lifecycle in one case.

## What This Case Demonstrates

This case highlights the product capabilities behind the Virtual Compute prototype.

| Capability | Evidence in this case |
| --- | --- |
| Platform product thinking | Connects commerce, product management, compute resources, networking, usage and operations. |
| Technical concept translation | Converts Cloud Projects, VMs, networks, flavors, images and provisioning states into a comprehensible customer experience. |
| Product-model design | Separates contractual containers from runtime resources while preserving their relationship. |
| End-to-end journey design | Covers configuration, commerce handover, product overview, deployment, management and usage. |
| Information architecture | Structures complex infrastructure domains into a clear project hierarchy and tab model. |
| Self-service design | Enables customers to deploy and manage standard resources without hiding relevant operational constraints. |
| Price-transparency thinking | Makes usage-based cost implications visible before resource creation. |
| Operational realism | Reflects asynchronous provisioning, status-dependent actions, quotas, dependencies and support paths. |
| Component and pattern reuse | Reuses Commerce Checkout and Virtual Network Management concepts instead of creating disconnected feature solutions. |
| Comparative prototyping | Uses stepper and one-page variants to support an explicit product decision. |
| Stakeholder alignment | Turns open technical and product questions into a concrete interaction model for discussion. |
| Product evolution | Uses one feature to explore a broader project- and resource-oriented portal model. |

## Related Portfolio Context

Virtual Compute is one product area within the broader Customer Portal prototype portfolio.

It connects directly to:

- **Commerce Checkout**, which provides the Order Review, Checkout, Payment and Order Overview journey after Cloud Project configuration
- **Virtual Network Management**, which provides the shared network-management pattern and resource-relationship model
- **API Management**, which demonstrates technical self-service and developer-oriented platform capabilities
- **User and Role Management**, which will influence who can view, create, edit or delete infrastructure resources
- **MFA and Account Security**, which support secure access to operationally sensitive actions
- future **contract, billing and cancellation journeys**, which will connect infrastructure usage with commercial lifecycle management

Within the portfolio, each case has a different focus:

- Commerce Checkout demonstrates conversion, compliance and end-to-end customer journey thinking.
- API Management demonstrates developer-oriented self-service and activation flows.
- Virtual Network Management demonstrates infrastructure relationships and product architecture evolution.
- Virtual Compute demonstrates how commerce, contractual products and runtime infrastructure can be combined into one coherent platform experience.

The case is especially relevant for roles focused on platform products, cloud infrastructure, B2B self-service, customer portals, product discovery, technical product management, information architecture and the translation of complex systems into usable customer experiences.
