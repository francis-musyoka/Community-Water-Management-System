# Roles and permissions

## Description

Each organization uses a fixed set of roles. Organizations cannot create custom roles. An org admin assigns roles to staff and assigns staff to schemes.

## Roles

| Role | Scope | Can do |
|---|---|---|
| **Platform admin** | Whole platform | Onboard organizations, manage subscriptions, suspend and reactivate organizations, logged support access. See [Platform administration](platform-administration.md). |
| **Org admin** | All schemes in the organization | Configure schemes, tariffs, Paybills, policies, SMS sender name, expense categories; manage staff; pay the platform subscription; run data imports. |
| **Manager** | Assigned schemes | Approve disconnections, correct readings, assign problem reports, add fines, send bulk SMS notices, review readings and reports. |
| **Field officer** | Assigned schemes | Register customers, upload contracts, install meters, handle problem reports, carry out disconnections and reconnections, record tenant move-in and move-out. |
| **Meter reader** | Assigned routes | Record readings and "not read" reasons for meters on assigned routes, including offline. |
| **Accountant** | Assigned schemes | Record expenses and funding, match unmatched payments, record refunds, run financial reports. |
| **Committee member** | Assigned schemes | Read-only access to reports and finances. |
| **Customer** | Own account | View bills, consumption, and contracts; pay; report problems. |

## Rules

- Access is per scheme. Staff only see schemes they are assigned to.
- One person can hold more than one role, for example meter reader and field officer in a small scheme.
- Expenses are approved by the committee in its meetings, outside the system. The committee role remains read-only.
- Sensitive actions are recorded in an audit log with who, when, and the reason: editing a reading, matching or reversing a payment, waiving or adding a fine, approving or carrying out a disconnection, editing or cancelling an expense, and platform admin support access.

## Requirements

- **RL-01 — Fixed roles:** The system provides the roles above; custom roles are not supported.
- **RL-02 — Multiple roles:** A user can hold more than one role.
- **RL-03 — Scheme assignment:** Staff roles apply only to assigned schemes; meter readers are further limited to assigned routes.
- **RL-04 — Committee read-only:** Committee members cannot create or change data.
- **RL-05 — Audit log:** Sensitive actions are logged and the log is visible to managers and org admins.

## Questions to confirm

- Can a user belong to more than one organization (for example, a contractor meter reader working for two schemes)?
- Can an accountant reverse a payment, or only a manager?
- Should committee members see individual customer details, or only totals?
