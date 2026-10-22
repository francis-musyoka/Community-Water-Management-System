# Organizations and schemes

## Description

An **organization** subscribes to the platform and runs one or more **schemes**. Examples: Kituasi community runs Kituasi A and Kituasi B; a county runs several rural schemes; a property manager runs several apartment estates. Each scheme's customers, bills, and ledger are kept separate from other schemes and from other organizations.

## Organization setup

The org admin configures:

- Organization name, type (community scheme, county, water service provider, property manager), and SMS sender name
- Schemes and their administrative locations: County, Sub-County, Ward, Location, and Village
- Zones, routes, or buildings within each scheme
- **One M-Pesa Paybill per scheme**, so customer payments go directly to that scheme
- Tariffs: price per unit for each connection type, and the optional standing fee (see [Billing and tariffs](billing.md))
- Meter-reading frequency (see [Meter reading](meter-reading.md))
- Payment allocation order (see [M-Pesa payments](payments.md))
- Penalty, disconnection, reconnection, and reminder rules (see [Penalties, disconnection, and reconnection](disconnection-and-reconnection.md))
- Expense categories (see [Expenses and funding](expenses.md))
- Staff and their roles and scheme assignments (see [Roles and permissions](roles-and-permissions.md))

## Requirements

- **OS-01 — Create a scheme:** An org admin can create schemes within their organization.
- **OS-02 — Configure locations:** County, Sub-County, Ward, Location, and Village data are defined for each scheme.
- **OS-03 — Zones and buildings:** A scheme can be divided into zones, routes, or buildings.
- **OS-04 — Paybill per scheme:** Each scheme has its own M-Pesa Paybill.
- **OS-05 — Isolate organization data:** No organization can see another organization's data.
- **OS-06 — Isolate scheme data:** Customer lists, bills, and ledgers of one scheme are not mixed with another scheme's.
- **OS-07 — Assign staff:** Staff are assigned to the schemes they may access.
- **OS-08 — Restrict access:** Staff only view and manage data for their assigned schemes; the org admin sees all schemes in the organization.
- **OS-09 — Organization-wide view:** An organization with several schemes can see them side by side in reports.
- **OS-10 — Per-organization settings:** Tariffs and policies are configured per organization and do not affect other organizations.

## Acceptance criteria

- A scheme can be created with its administrative location hierarchy and Paybill.
- A staff member assigned to one scheme cannot access another scheme's customer records, bills, or ledger.
- No user of one organization can access any data of another organization.
- Reports and lists are scoped to the selected and authorized scheme or organization.

## Questions to confirm

- Can tariffs differ between schemes within the same organization, or are they set once per organization?
- Can location records be edited after a scheme has started operating?
- Can a scheme be moved from one organization to another (for example, when a county takes over a community scheme)?
