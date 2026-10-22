# M-Pesa payments

## Payment channels

All payments are **cashless, through M-Pesa only**. Staff never collect cash.

- **Portal or USSD:** the customer chooses to pay and receives an M-Pesa PIN prompt on their phone.
- **Direct Paybill:** the customer sends money to the scheme's Paybill and enters their account number.

**Each scheme has its own Paybill**, so payments go directly to the scheme and never pass through the platform provider.

## Matching payments

1. The system receives the M-Pesa transaction.
2. If the account number matches a customer in that scheme, the payment is recorded automatically.
3. If the account number is wrong or missing, the payment goes to the **unmatched payments list**. The accountant matches it manually to the right customer. Each manual match is logged.
4. A transaction code is recorded only once, even if M-Pesa sends the same notification more than once.
5. The customer receives an SMS receipt with the amount, M-Pesa code, and updated balance.

## Payment allocation

Payments are applied in this default order:

1. Outstanding fines
2. Reconnection fees
3. Past overdue bills (including imported opening balances)
4. Current usage bill
5. Any remaining amount is kept as **account credit** for the next bill

Each organization can change this order.

## Credit and refunds

- Credit is applied automatically to the next bill.
- When a tenant moves out, credit is first applied to the final bill. Any remaining credit is refunded to the tenant by the accountant, outside the system, and the refund is recorded in the system.

## Revenue categories

Collections are reported separately as:

- Water usage bills
- Standing fees
- Connection and registration fees
- Reconnection fees
- Fines and penalties
- Donor and government funding (recorded by the accountant; see [Expenses and funding](expenses.md))

Kiosks and bowsers are billed as ordinary connections, not as a separate revenue category.

## Requirements

- **BP-01 — Portal and USSD payment:** Customers can start an M-Pesa payment from the portal or USSD.
- **BP-02 — Direct payment:** Payments to a scheme's Paybill are received and matched.
- **BP-03 — Paybill per scheme:** Each scheme's payments go to its own Paybill.
- **BP-04 — Automatic matching:** Payments with a valid account number are matched automatically.
- **BP-05 — Unmatched payments:** Payments that cannot be matched are listed for the accountant to match manually, with an audit trail.
- **BP-06 — Duplicate protection:** Each M-Pesa transaction code is recorded once.
- **BP-07 — Allocation:** Payments are applied in the organization's configured order.
- **BP-08 — Account credit:** Excess payment is kept as credit and applied to the next bill.
- **BP-09 — Refund record:** Refunds made outside the system can be recorded against the account.
- **BP-10 — SMS receipt:** Customers receive a receipt with amount, M-Pesa code, and updated balance.
- **BP-11 — Revenue classification:** Collections can be reported by revenue category.
- **BP-12 — Unaffected by subscription status:** Payments continue even if the organization's platform subscription is unpaid.

## Questions to confirm

- Which M-Pesa integration provider and callback method will be used?
- How should M-Pesa reversals be handled once a payment has been allocated?
- How long can a payment stay unmatched before it is escalated?
- Can a customer request a refund of credit while still connected?
