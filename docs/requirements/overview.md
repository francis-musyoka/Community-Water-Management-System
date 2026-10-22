# Requirements overview

## Problem statement

Organizations that supply water — community schemes, counties, water service providers, and property managers — need accurate customer and meter records, timely bill collection, and clear expense tracking. Paper-based processes introduce manual errors and make it difficult to reconcile collections or understand a scheme's financial position.

## Objectives

1. Provide one platform that many independent water organizations can subscribe to.
2. Centralize customer, connection, meter, billing, payment, and expense records for each organization.
3. Keep each organization's and each scheme's data separate.
4. Let each organization configure its own tariffs and policies instead of hard-coding one scheme's rules.
5. Improve the reliability and timeliness of M-Pesa payment reconciliation.
6. Help field staff collect meter readings, including where network connectivity is unavailable.
7. Make water production, sales, estimated losses, collections, unpaid balances, and operating costs visible to management and committees.
8. Serve customers with smartphones (web portal) and basic phones (SMS and USSD).

## Platform structure

| Level | Description | Examples |
|---|---|---|
| **Platform** | The product run by the platform provider. | — |
| **Organization** | The body that subscribes to the platform. | Kituasi community, a county government, a water company, a property management firm |
| **Scheme** | A water system run by the organization, with its own customers, Paybill, and ledger. | Kituasi A, Kituasi B, a county's rural scheme, an apartment estate |
| **Zone / route / building** | A subdivision of a scheme used for meter reading and follow-up. | Village zone, reading route, Block C |

A small community may have one organization with one scheme. A county may have many schemes and needs an organization-wide view across them.

## Organization types

| Type | Distinguishing features |
|---|---|
| Community water scheme | Often run by a committee; customers apply, pay a connection fee, and sign a contract. |
| County government | Many schemes; needs consolidated reporting. |
| Water service provider | Similar to a community scheme, possibly larger. |
| Property manager | Customers are tenants who occupy units; meters belong to units; empty units are billed to the landlord. |

## User groups

| Role | Responsibilities |
|---|---|
| Platform admin | Onboards organizations, manages subscriptions, suspends or reactivates organizations, and provides logged support access. |
| Org admin | Configures the organization, its schemes, tariffs, and policies; manages staff. |
| Manager | Runs assigned schemes; approves disconnections and corrections; reviews readings and reports. |
| Field officer | Registers customers, installs meters, handles problem reports, disconnections, and reconnections. |
| Meter reader | Captures readings on assigned routes. |
| Accountant | Records expenses and funding, matches unmatched payments, runs financial reports. |
| Committee member | Read-only access to reports and finances. |
| Customer | Views bills and consumption, pays through M-Pesa, views contracts, and reports problems via the portal or USSD. |

See [Roles and permissions](roles-and-permissions.md) for detail.

## Functional areas

- [Platform administration and subscriptions](platform-administration.md)
- [Organizations and schemes](organizations-and-schemes.md)
- [Roles and permissions](roles-and-permissions.md)
- [Customer management](customer-management.md)
- [Meter reading](meter-reading.md)
- [Billing and tariffs](billing.md)
- [M-Pesa payments](payments.md)
- [Penalties, disconnection, and reconnection](disconnection-and-reconnection.md)
- [Problem reports](problem-reports.md)
- [Customer communication](communication.md)
- [Expenses and funding](expenses.md)
- [Reports](reports.md)
- [Data import](data-import.md)

## Out of scope

- Reports for regulators such as WASREB. Reports are for internal management only.
- Cash collection. All payments are cashless through M-Pesa.
- Tracking how kiosks or bowsers resell water. They are billed as ordinary meters.
- Languages other than English.

This requirements set does not yet define the database schema, API contracts, technology stack, hosting, or security implementation. See [System architecture](../architecture/system-architecture.md).
