# **Community Water Management System**

## Purpose

The Community Water Management System is a multi-organization platform for any body that supplies water and bills customers by meter. It helps organizations maintain customer and connection records, read meters, bill customers, collect M-Pesa payments, track operating expenses, and produce management reports.

The system is intended to replace paper-based processes, reduce manual errors, support cashless M-Pesa collections, and give managers and committees clearer financial and operational visibility.

## Who the platform serves

The platform is sold as a monthly subscription to organizations such as:

- **Community water schemes**, for example Kituasi A and Kituasi B, often run by a committee.
- **County governments** managing water across several schemes or areas.
- **Water service providers** of any size.
- **Property managers and landlords** who meter and bill tenants across one or more buildings.

**Kituasi Project is used throughout this documentation as a worked example only.** Every rule that differs between organizations (tariffs, penalties, disconnection rules, payment allocation, reading frequency) is an organization setting, not a fixed behaviour.

## Who this documentation is for

- The platform provider and platform administrators
- Organization administrators, managers, and community committees
- Field officers, meter readers, and accountants
- Developers and technical maintainers

## Main capabilities

- Onboard many organizations, each running one or more schemes, with every organization's and scheme's data kept separate.
- Bill organizations a monthly subscription based on active meters, plus SMS charged per message.
- Register customers, manage connections and rental units, and store signed contracts.
- Verify customers by SMS and provide self-service through a web portal and a USSD menu for basic phones.
- Record meter readings with GPS and a meter photo, flag unusual readings, record why a meter could not be read, and work offline.
- Compare main supply readings with water sold to estimate water loss.
- Bill by price per unit for each connection type, with an optional standing fee for zero-usage readings.
- Collect cashless M-Pesa payments to each scheme's own Paybill, reconcile them, and send SMS receipts.
- Apply configurable penalties, disconnection, and reconnection rules.
- Track customer problem reports through to resolution.
- Record expenses with custom categories and receipts, and record donor or government funding.
- Send bills, receipts, reminders, and bulk notices by SMS.
- Import existing customers, meters, readings, and balances from an Excel template.
- Produce internal reports exportable to PDF and Excel.

## Documentation map

- **Requirements** describes expected system capabilities and business rules.
- **Workflows** describes the main processes from the user's perspective.
- **Architecture** lists technical design decisions that are still open.
- **Development** contains setup and maintenance instructions as the implementation is established.

## Scope note

This documentation started from the supplied *Project Operations & Requirements Guide: Community Water Management System* and has been extended through requirements sessions with the product owner. Where a rule is not yet agreed, it is listed under "Questions to confirm" rather than treated as a requirement.
