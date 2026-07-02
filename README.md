# Customer Portal – Product Mockups

This repository contains product-oriented mockups for a customer portal, focusing on system structure, feature design, and iterative development.

## Portfolio Context

This repository is part of a product management portfolio.  
It documents how customer-facing platform features evolve from an initial product concept into structured, system-oriented solutions.

The focus is not visual design alone, but product thinking:
- understanding user and business needs
- structuring feature flows
- translating requirements into usable interfaces
- preparing features for implementation and future iteration

## Structure

The mockups are organized into two stages:

- **Unbranded**  
  Focus on product logic, structure, and feature flows without visual design constraints.

- **Design System**  
  The same features translated into a consistent design system, including layout, interaction patterns, and visual identity.

## Current Features

| Feature                    | Status         | Description                                                                                                                    | Unbranded                                                                             | Design System  | Product Vision |
| -------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- | -------------- | -------------- |
| Virtual Network Management | Available      | Self-service management of virtual networks and assigned resources within a customer portal.                                   | [Open](features/virtual-network-management/virtual-network-management-unbranded.html) | [Open](features/virtual-network-management/virtual-network-management-design-system.html) | —              |
| API Management             | Available      | API activation, key lifecycle, documentation, request transparency and access restrictions for platform customers.             | [Open](features/api-management/api-management-unbranded.html)                         | —              | —              |
| eCommerce Checkout         | Available      | Commerce-first B2B SaaS ordering flow with configuration, checkout, payment verification, account activation and order status. | [Open](features/commerce-checkout/commerce-checkout-unbranded.html)                   | —              | —              |
| Customer MFA Policies      | In Preparation | Customer-level security policies for mandatory MFA and passkey adoption.                                                       | —                                                                                     | —              | —              |
| User & Role Management     | In Progress    | Next-generation user administration, role management and permission handling.                                                  | —                                                                                     | —              | —              |
| Bulk User Operations       | In Preparation | Administrative bulk actions for customer user management.                                                                      | —                                                                                     | —              | —              |


## Goals, Signals & Metrics

The mock-ups are not only visual prototypes. Each feature is framed around a product goal, observable success signals and potential metrics that could be used to evaluate whether the feature creates value for customers and the platform.

| Feature                    | Goal                                                                                                                                                                                | Signals                                                                                                                                                                                     | Potential Metrics                                                                                                                                                                                   |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Virtual Network Management | Enable customers to manage virtual networks and assigned resources independently through a clear self-service interface.                                                            | Customers can find existing networks, understand their status, create or edit networks, and identify assigned resources without support involvement.                                        | Self-service completion rate, reduction of support requests for network changes, number of successfully created networks, time to complete network configuration, failed validation rate.           |
| API Management             | Enable customers to activate API access, manage API keys securely and understand API usage through transparent documentation and activity views.                                    | Customers activate API access successfully, create keys with the right version and expiry, use documentation, identify recent errors and apply access restrictions where needed.            | API activation completion rate, number of active API keys, key rotation rate, documentation usage, API error visibility usage, reduction of API-related support tickets.                            |
| eCommerce Checkout         | Enable new customers to configure, order and activate a B2B SaaS product through a guided commerce-first flow while keeping validation, payment and account activation transparent. | Customers complete product configuration, understand contract and payment steps, pass validation before payment, receive clear activation guidance and can track order/provisioning status. | Checkout completion rate, drop-off rate per step, validation failure rate, payment verification success rate, account activation completion rate, time from order submission to account activation. |

## Development Approach

Each feature is documented across multiple stages:

1. Unbranded Prototype
   - Focus on product logic, workflows and information architecture.

2. Design System Integration
   - Translation into a consistent design language and component structure.

3. Product Vision (where applicable)
   - Exploration of future enhancements and long-term product evolution.

Further features and iterations will be added over time.

## Notes

All data is anonymized and fictional. The prototypes are portfolio artifacts and do not contain production data, proprietary customer information or real internal system access.
