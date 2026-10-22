# Penalties, disconnection, and reconnection

## Description

Organizations handle non-payment differently. Kituasi, for example, has no late penalties and no disconnection deadline. Every rule on this page is an **organization setting** and is **off by default**.

## Organization settings

| Setting | Options |
|---|---|
| Late penalty | On/off; fixed amount or percentage of the overdue bill; number of days after the due date |
| Disconnection rule | On/off; account becomes eligible when overdue by a set number of days or a set amount |
| Reconnection fee | Amount charged to reconnect |
| Reminder SMS | On/off; days before the due date; on becoming overdue |

## Disconnection

1. Accounts meeting the disconnection rule appear on the **field action list**, grouped by zone.
2. A **manager approves** each disconnection. No customer is disconnected automatically.
3. The customer receives a warning SMS before the visit.
4. The field officer disconnects, records the meter reading and a photo, and the connection becomes **Disconnected**.

## Reconnection

1. The customer pays the overdue amount and the reconnection fee.
2. The account appears on the field officer's reconnection list.
3. The field officer reconnects and records the meter reading.
4. The connection returns to **Active**.

## Fines

A manager can add a one-off fine, for example for an illegal connection or meter tampering. Fines are separate from late penalties, are logged, and are paid first under the payment allocation order.

## Suspension

**Suspended** means a temporary stop at the customer's request, for example while away. A suspended connection is not billed and is not counted for the organization's subscription. It is not used for non-payment.

## Requirements

- **DC-01 — Configurable penalties:** Late penalties can be enabled per organization as a fixed amount or percentage.
- **DC-02 — Configurable disconnection rule:** Disconnection eligibility is configured per organization by days or amount overdue.
- **DC-03 — Field action list:** Eligible accounts are listed by zone.
- **DC-04 — Manager approval:** Disconnections require manager approval.
- **DC-05 — Warning SMS:** Customers are warned by SMS before disconnection.
- **DC-06 — Disconnection record:** Disconnections record the reading, photo, field officer, and date.
- **DC-07 — Reconnection:** Paying the overdue amount and reconnection fee places the account on the reconnection list.
- **DC-08 — Fines:** Managers can add logged one-off fines.
- **DC-09 — Customer suspension:** A connection can be suspended and resumed at the customer's request.
- **DC-10 — Reminder SMS:** Organizations can enable due-date and overdue reminders.

## Questions to confirm

- Can a manager waive a penalty, fine, or reconnection fee, and is that logged?
- Should a customer on a payment plan be excluded from the field action list?
- Is there a maximum period a connection can stay Suspended?
- Does a suspension need a reading at the start and the end?
