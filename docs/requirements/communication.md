# Customer communication

## Language

All SMS, USSD menus, and portal screens are in **English only**.

## SMS

Every SMS is charged to the organization per message (see [Platform administration](platform-administration.md)). Messages are sent under the organization's own sender name.

| Message | When |
|---|---|
| Verification code | Customer account created |
| Bill | Bill produced after a reading |
| Payment receipt | Payment matched |
| Reminder | Before the due date and on becoming overdue, if enabled |
| Disconnection warning | Before a disconnection visit |
| Problem report update | Report assigned and resolved |
| Bulk notice | Sent by a manager or org admin |

### Bulk notices

A manager or org admin can send a notice, for example "Water will be off on Thursday for repairs", to:

- A whole scheme
- One zone, route, or building
- One connection type

Before sending, the system shows the number of messages and the cost.

## USSD

Customers with basic phones use a USSD menu. The customer is identified by their phone number, so the same menu works for every organization.

| Menu option | Result |
|---|---|
| Check balance | Current balance and due date |
| Last bill | Readings, units, and amount of the latest bill |
| Pay | Sends an M-Pesa PIN prompt to the phone |
| Report a problem | Choose a problem type; the report is created |

## Web portal

Customers with smartphones or computers use the portal. See [Customer management](customer-management.md) for portal features.

## Requirements

- **CM-01 — Transactional SMS:** The system sends the messages listed above.
- **CM-02 — Sender name:** SMS are sent under the organization's sender name.
- **CM-03 — Bulk notices:** Managers and org admins can send notices to a scheme, zone, building, or connection type.
- **CM-04 — Cost preview:** Bulk notices show message count and cost before sending.
- **CM-05 — SMS charging:** All SMS are counted per organization for billing.
- **CM-06 — USSD menu:** Customers can check balance, see their last bill, pay, and report a problem by USSD.
- **CM-07 — English only:** All customer-facing text is in English.

## Questions to confirm

- Is one USSD code shared by all organizations on the platform?
- How does USSD handle a phone number linked to more than one account?
- Who pays for USSD session costs: the customer, the organization, or the platform?
- Can customers opt out of reminders or bulk notices?
