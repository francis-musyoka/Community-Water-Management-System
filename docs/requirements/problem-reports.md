# Problem reports

## Description

Customers report leaks and other service problems. A field officer goes to fix them, and the customer is kept informed.

## Reporting

- **Customers** report through the web portal or the USSD menu.
- **Staff** can log a report on behalf of a customer who phones or visits.
- A report includes a type (leak, no water, meter problem, billing question, other), a description, and optionally a photo and location (portal only).

## Handling

| Status | Meaning |
|---|---|
| Open | Reported, not yet assigned |
| Assigned | A field officer has been assigned by a manager or by zone |
| Resolved | The field officer has fixed it and recorded notes and an optional photo |

The customer receives an SMS when the report is assigned and when it is resolved.

Repair costs are recorded as expenses (see [Expenses and funding](expenses.md)). Leaks on main pipes are relevant to the water-loss report.

See [Problem report workflow](../workflows/problem-report.md).

## Requirements

- **PR-01 — Customer reporting:** Customers can report problems through the portal and USSD.
- **PR-02 — Staff reporting:** Staff can log a report for a customer.
- **PR-03 — Assignment:** Managers can assign reports to field officers, or reports are routed by zone.
- **PR-04 — Status tracking:** Reports move through Open, Assigned, and Resolved.
- **PR-05 — Resolution record:** Field officers record notes and an optional photo when resolving.
- **PR-06 — Customer updates:** Customers receive SMS updates on assignment and resolution.
- **PR-07 — Reporting:** Open and resolved reports and average time to resolve are reported by zone.

## Questions to confirm

- Should reports have a priority, for example a burst main above a single meter fault?
- Can a customer reopen a report they believe is not fixed?
- Can members of the public who are not customers report a leak?
