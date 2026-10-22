# Customer management

## Customer data

| Field | Notes |
|---|---|
| Full name | Required |
| Mobile phone number | Required; used for SMS, USSD, M-Pesa, and portal login |
| National ID number | Required for community, county, and provider schemes; optional for tenants |
| Member number | Community schemes only |
| Registration date | Required |
| Account (connection) number | Generated; used as the M-Pesa account number |

Fields that only apply to some organization types are optional for the others.

## Connection profile

- Meter serial number
- Connection type: Household, Business, School/Institution, Kiosk, Bowser, or Flat Rate. Each type can have its own price per unit (see [Billing and tariffs](billing.md)).
- Zone, route, or building and unit
- GPS location of the meter
- Connection status:

| Status | Meaning |
|---|---|
| Applied | Application recorded; not yet connected |
| Active | Connected and billed |
| Suspended | Temporarily stopped **at the customer's request**, for example while away |
| Disconnected | Stopped by the organization, usually for non-payment |

Kiosks and bowsers are treated like any other connection: their meter is read and billed. How they resell water is not tracked.

## New connection (community, county, and provider schemes)

1. **Applied:** the customer applies and their details are recorded.
2. **Fee paid:** the connection fee is paid by M-Pesa.
3. **Contract signed:** the user agreement and, where required, land consent form are signed and uploaded.
4. **Installed:** the field officer installs the meter and records its serial number, starting reading, and GPS location.
5. **Active:** billing starts from the starting reading.

A connection cannot be activated until the connection fee is paid and the contract is uploaded.

See [Customer registration workflow](../workflows/customer-registration.md).

## Rental units (property managers)

- The **meter belongs to the unit**, not the tenant.
- A tenant **moves into a unit**. There is no application, connection fee, or water contract.
- A **move-in reading** is taken so the new tenant is not billed for earlier usage.
- A **move-out reading** produces a final bill. Any unpaid amount stays with the outgoing tenant's account, not the unit.
- Credit left after the final bill is refunded to the tenant (see [M-Pesa payments](payments.md)).
- **While a unit is empty, its water is billed to the landlord.**
- Each meter keeps a **history of account holders** over time.

See [Tenant move-in and move-out workflow](../workflows/tenant-move-in-move-out.md).

## Contract documents

- Scanned photos or PDF copies of signed user agreements and land consent forms can be uploaded.
- Accounts missing required signed contracts are flagged.
- Customers can view their signed contract in the portal.
- Contracts do not apply to tenants of property managers.

## Customer account verification

- Field staff attach a new customer to their scheme.
- The system creates a customer account linked to the mobile phone number.
- The customer receives an SMS verification code, uses it to verify their identity, and sets a password.

## Customer self-service

Customers use the **web portal** (smartphone or computer) or the **USSD menu** (any phone). See [Customer communication](communication.md).

| Feature | Portal | USSD |
|---|---|---|
| View current bill and balance | Yes | Yes |
| View past consumption and readings, including meter photos | Yes | Last bill only |
| Pay through M-Pesa | Yes | Yes |
| View signed contract | Yes | No |
| Report a problem | Yes | Yes |

## Requirements

- **CU-01 — Register customer:** Field officers can record customer and connection details against a scheme.
- **CU-02 — Optional fields by organization type:** Fields that do not apply to an organization type are optional.
- **CU-03 — Connection status:** Connections move through Applied, Active, Suspended, and Disconnected.
- **CU-04 — Activation checks:** A new connection cannot be activated until the connection fee is paid and the contract is uploaded (not applicable to rental units).
- **CU-05 — Contract upload:** Signed documents can be uploaded and missing ones flagged.
- **CU-06 — Tenant occupancy:** A tenant can be moved into and out of a unit, with move-in and move-out readings.
- **CU-07 — Final bill:** A move-out reading produces a final bill on the outgoing tenant's account.
- **CU-08 — Empty unit billing:** Usage on an empty unit is billed to the landlord.
- **CU-09 — Account holder history:** Each meter keeps a history of its account holders.
- **CU-10 — SMS verification:** A customer can verify their account by SMS code and set a password.
- **CU-11 — Own data only:** Customers can only view their own account information.

## Acceptance criteria

- A customer record is associated with the correct scheme.
- A new community connection cannot become Active without a paid fee and uploaded contract.
- A tenant moving in is not billed for usage before their move-in reading.
- An empty unit's usage appears on the landlord's account.
- A customer can complete SMS verification and set a password.

## Questions to confirm

- Must National ID numbers be unique across the platform, within an organization, or within a scheme?
- Can one customer have multiple connections or meters, and do they share one balance?
- What is the required document list for each connection type?
- What happens when a customer changes their phone number or cannot receive an SMS?
- Is the landlord a customer account within the scheme, or a separate type of record?
