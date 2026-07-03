# Commerce Checkout Case Study

## Product Context

This case study explores a B2B SaaS commerce checkout flow for a customer-facing portal. The prototype focuses on how new customers can configure and order a cloud service through a more compact checkout journey, while account creation, email verification, payment authorization and operational checks are handled as part of one connected process.

The goal of the prototype is to make the improved journey visible: from product configuration and order review to consolidated customer data entry, payment authorization, verification, order status and portal access.

## Problem

Traditional B2B portal journeys often assume that a customer already has an account before they can start an order. This can create friction for new customers, especially when product discovery, configuration and checkout are separated from registration and onboarding.

At the same time, B2B checkout cannot be treated like a simple consumer checkout. The flow needs to account for company details, payment authorization, duplicate checks, fraud signals, compliance checks and clear order status communication.

The product challenge was to structure this journey in a way that keeps the checkout understandable for customers while making the required business and system dependencies visible.

## Target Users

The prototype focuses on two primary customer groups:

### New customers / guest users

New customers want to discover, configure and order a product without being forced into a long upfront registration process. For them, the improved flow reduces friction by combining customer data entry, payment authorization, email verification and portal access into one connected checkout journey.

### Existing customers / logged-in portal users

Existing customers already have a portal account and company context. For them, the flow should make it easier to order additional services by reusing known customer data and reducing the checkout to the information that is still required for the specific order.

### Operational stakeholders

Internal teams are not the primary users of the customer-facing flow, but they depend on the process being safe, traceable and operationally reliable. The flow therefore also considers background checks, duplicate handling, payment risk, compliance review and order provisioning.

## Product Goal

The product goal is to reduce friction in the first purchase journey while keeping the flow safe, traceable and suitable for B2B requirements.

The prototype aims to replace a long, sequential registration-before-checkout experience with a more modern commerce flow where customer data entry, verification, payment authorization and background checks work together as one connected journey.

## Prototype Scope

The unbranded prototype covers the core checkout journey and related exception states. It includes:

- Product configuration
- Order summary
- Consolidated account, company, billing and payment details
- Email verification
- Checkout and payment
- Payment authentication
- Order success and order status
- Duplicate match handling
- Compliance and operational review states

The prototype is intentionally unbranded to focus on product logic, user flow, dependencies and handover clarity rather than visual brand execution.

## Key Product Decisions

### Integrated checkout and onboarding

The prototype combines checkout, account creation and company data collection into one more compact customer journey. Instead of forcing new customers through a long registration process before they can continue to checkout, the flow allows them to enter the required account, company and payment information in one consolidated experience.

### Reduced visible steps for the customer

A key improvement is that the customer does not need to move through separate registration, verification, checkout and payment screens as disconnected steps. The prototype reduces visible friction by grouping required data entry and moving checks into the background where possible.

### One-page data capture for account and company details

The customer can provide the relevant account, company and billing information in one structured page. This follows common checkout expectations and makes the flow feel more modern, especially compared to long B2B registration forms.

### Background checks instead of customer-facing complexity

Duplicate checks, fraud signals, compliance checks and operational validation are treated as background processes. The customer journey remains focused on completing the order, while the system evaluates risk and eligibility behind the scenes.

### Parallel verification and payment authorization

Email verification and payment authorization are part of the same overall checkout journey. The customer can verify the email address, authorize the payment and then move into the portal without experiencing these steps as a long, disconnected registration sequence.

### Clear transition into the customer portal

After successful checkout, verification and authorization, the customer should understand what happens next and be able to enter the portal or view the order status. The flow is designed to make the transition from first purchase to customer portal access feel natural.

### Unbranded first, branded later

The prototype is intentionally built as an unbranded version first. This allows the product structure, checkout logic, background checks, edge cases and handover requirements to be reviewed independently from visual branding decisions. Later branded versions can focus on customer portal entry points, dashboard integration and product-specific order journeys.

## User Flow

The prototype follows a consolidated commerce and onboarding journey:

1. The customer enters the portal through a product or commerce entry point.
2. The customer configures the selected product.
3. The customer reviews the order summary.
4. The customer enters account, company, billing and payment-related information in a compact checkout experience.
5. The system runs duplicate, fraud and compliance checks in the background where possible.
6. The customer verifies the email address as part of the checkout journey.
7. The customer authorizes the payment when required.
8. The customer receives a success or order status view.
9. The customer can continue into the portal or follow the next activation/status steps.
10. Internal systems continue with order processing, review and provisioning where needed.

For existing customers, known account and company data can be reused so that the journey focuses more strongly on ordering additional products from within the customer portal.

## Edge Cases & System Dependencies

The prototype includes or considers several edge cases and system dependencies that are typical for B2B SaaS checkout flows.

### Email verification

The customer may need to verify the email address during the checkout journey. This should feel like part of the order process, not like a separate registration detour.

### Payment authentication

Payment may require additional authorization. The flow needs to support authentication, pending states, failed authorization and a clear return to the order status.

### Duplicate company match

A new order may match an existing company or customer account. The prototype includes duplicate match handling to show that B2B checkout needs to account for existing records without creating uncontrolled duplicate accounts.

### Compliance and operational review

Some orders may require additional checks before the customer account or ordered service can be fully activated. These checks should run in the background where possible, while the customer receives clear status communication.

### Fraud and payment risk

The checkout needs to support fraud signals and payment risk handling. These checks may not need to interrupt the customer immediately, but they can influence whether an order is approved, delayed or reviewed.

### Order status and provisioning

After checkout, the customer needs a clear order status. The prototype connects payment, review and activation states so that the customer is not left without feedback after completing the order.

### System handoffs

The flow depends on multiple systems or services, such as customer account creation, email verification, payment provider handling, duplicate checks, compliance review and product provisioning. The prototype is designed to make these handoffs visible enough for product review and implementation discussion without exposing all operational complexity to the customer.

## Goals, Signals & Metrics

The prototype is framed around product outcomes rather than screens alone. The goal is to improve the first purchase journey while keeping the flow reliable, compliant and suitable for B2B SaaS requirements.

| Goal | Signals | Potential Metrics |
|---|---|---|
| Reduce friction for new customers | Customers can configure, review and complete an order without going through a long separate registration process first. | Checkout completion rate, drop-off rate per step, time to complete first order, abandoned checkout rate |
| Create a more modern B2B checkout experience | Account, company, billing and payment data are collected in one structured journey instead of several disconnected forms. | Number of visible customer steps, form completion time, support requests during checkout, customer feedback on checkout clarity |
| Support both guest and existing customer journeys | New customers can enter through a commerce-first flow, while existing customers can reuse known account and company data for additional orders. | Share of orders from new vs. existing customers, repeat order completion rate, amount of prefilled data reused, logged-in checkout completion rate |
| Keep operational and compliance requirements in the background | Duplicate checks, fraud signals, compliance review and payment risk handling can run without making the customer journey unnecessarily complex. | Number of orders requiring manual review, duplicate account detection rate, fraud/compliance review time, blocked or delayed order rate |
| Improve order transparency after checkout | Customers receive clear success, pending or order status communication after payment authorization and verification. | Order status page usage, number of “what happens next” support requests, provisioning status visibility, time from checkout to activation |
| Make the flow easier to review and hand over | Product, design, development and operations can discuss the same end-to-end journey, including edge cases and system dependencies. | Number of clarified requirements before development, reduced rework during implementation, number of documented edge cases, stakeholder review feedback |

These metrics are intentionally defined as potential indicators. The prototype does not measure them directly, but uses them to frame what a successful implementation would need to improve: customer completion, flow clarity, operational reliability and handover quality.

## Next Iterations

Future iterations could extend the prototype in two stages:

1. **Branded customer portal integration**  
   A branded version could show how guest users and logged-in customers enter the commerce flow from realistic customer portal start pages. The focus would be on portal entry points, navigation, visual alignment and the first distinction between new and existing customer journeys.

2. **Product vision for logged-in commerce and lifecycle management**  
   A later product vision could explore how commerce evolves inside the customer portal after the first order. This could include a personalized dashboard, active products, order and provisioning status, reused customer data, product-specific order wizards and lifecycle actions such as upgrades, changes or cancellations.

These iterations would move the prototype from an integrated first-purchase checkout toward a broader customer portal commerce experience.
