# Platform administration and subscriptions

## Description

The platform provider sells the system to many organizations. A **platform admin** manages those organizations and bills them for using the platform. The platform admin does not run any organization's day-to-day operations.

## Platform admin capabilities

- Create and activate a new organization and its first org admin.
- Set and change an organization's subscription plan.
- Generate and track subscription invoices.
- Suspend and reactivate organizations.
- View platform-wide usage: organizations, schemes, active meters, and SMS volume.
- Enter an organization's data only for support purposes. Every support access is recorded in an audit log.

Outside logged support access, an organization's customer and financial data belongs to that organization and is not visible to the platform admin.

## Subscription

- Each organization pays a **monthly subscription based on its number of active meters**.
- Disconnected and suspended meters are not counted.
- The active meter count is taken each month and used to calculate the invoice.
- **SMS is charged per message on top of the subscription.** This covers bills, receipts, reminders, verification codes, and bulk notices.
- Subscription invoices are sent to the org admin and paid by M-Pesa or bank transfer.

## Non-payment of the subscription

1. Reminders are sent to the org admin before and after the due date.
2. After a grace period, the organization becomes **read-only**:
    - Staff can view records and reports.
    - Staff cannot add or change data (readings, customers, expenses, and so on).
    - **Customers keep paying.** M-Pesa payments continue to be received, matched, and allocated, and SMS receipts continue to be sent.
3. When the overdue amount is paid, full access is restored immediately.

## Requirements

- **PA-01 — Onboard organization:** A platform admin can create an organization and its first org admin.
- **PA-02 — Subscription plan:** Each organization has a subscription priced by active meters.
- **PA-03 — Meter count:** Active meters are counted monthly for billing; disconnected and suspended meters are excluded.
- **PA-04 — SMS charging:** SMS sent by or for an organization are counted and charged per message.
- **PA-05 — Subscription invoices:** The platform generates monthly invoices to each organization.
- **PA-06 — Read-only on non-payment:** After the grace period, an unpaid organization's staff have read-only access.
- **PA-07 — Customer payments continue:** Customer payments, allocation, and receipts are never blocked by an organization's subscription status.
- **PA-08 — Restore access:** Paying the overdue amount restores full access.
- **PA-09 — Support access audit:** Any platform admin access to an organization's data is logged with who, when, and why.
- **PA-10 — Platform usage view:** Platform admins can view usage across all organizations.

## Questions to confirm

- Is the per-meter price a flat rate, or are there price bands (for example 1–100 meters, 101–500 meters)?
- How long is the grace period before read-only access applies?
- Is there a minimum monthly charge, setup fee, or free trial?
- What is the price per SMS, and does it vary by message type?
- How is an organization's data handled if it permanently leaves the platform (export, retention, deletion)?
