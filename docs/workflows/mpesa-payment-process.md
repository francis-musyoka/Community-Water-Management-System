# M-Pesa payment workflow

## Expected flow

1. The customer pays from the portal or USSD (PIN prompt), or sends money directly to the scheme's Paybill with their account number.
2. The system receives the M-Pesa transaction.
3. If the transaction code has already been recorded, the duplicate is ignored.
4. If the account number matches a customer in that scheme, the payment is recorded.
5. The payment is allocated in the organization's configured order (default: fines, reconnection fees, overdue bills, current bill).
6. Any remaining amount is kept as account credit.
7. The customer receives an SMS receipt with the amount, M-Pesa code, and updated balance.

## Unmatched payment

1. The account number is wrong or missing, so the payment goes to the unmatched payments list.
2. The accountant identifies the right customer, for example from the payer's name or phone number.
3. The accountant matches the payment. The match is logged.
4. Allocation and SMS receipt follow as above.

## Unresolved payment cases

Handling of reversals and failed transactions still needs to be specified before the payment integration is implemented.
