# System architecture

## Status

**To be defined.** The business requirements are documented; the technology stack and system architecture have not yet been chosen.

## Decisions to document

- Web, mobile, or progressive web application approach for staff and customers
- Frontend and backend technologies
- Database technology and the multi-tenant strategy for keeping organizations and schemes separate
- Authentication, SMS verification, role-based access control, and password recovery
- M-Pesa integration provider, per-scheme Paybill configuration, callbacks, duplicate transaction handling, and reconciliation
- SMS provider, sender names per organization, delivery handling, and per-message counting for billing
- USSD provider, shared USSD code, and session handling
- Platform subscription billing: monthly active-meter counts, invoicing, and read-only mode for unpaid organizations
- Offline storage and synchronization of meter readings and photos
- GPS capture, map provider, and location-data access controls
- File storage for contracts, meter photos, and receipts
- Excel import and PDF/Excel report export
- Audit logging and data retention
- Hosting, deployment, backups, monitoring, and disaster recovery

## Architecture principles from the requirements

- **Data isolation.** No organization can access another's data. Within an organization, customer lists, bills, and ledgers are scoped to schemes, and staff access is scoped to assigned schemes. The design must show how this is enforced on every operation.
- **Configuration over code.** Tariffs, standing fees, reading frequency, payment allocation order, and penalty and disconnection rules are organization settings.
- **Payments never blocked.** Customer M-Pesa payments, allocation, and receipts must keep working even when an organization's subscription is unpaid.
- **Offline-first field work.** Meter reading must work without network coverage.
- **Basic phone support.** Core customer actions must be available through SMS and USSD, not only the web portal.
