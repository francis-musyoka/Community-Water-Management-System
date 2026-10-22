# Billing and tariffs

## Tariff settings

Each organization sets:

- A **price per unit for each connection type**. For example, a business or kiosk that resells water may pay a lower price per unit than a household.
- An optional **standing fee**.
- A **flat monthly amount** for Flat Rate connections, which have no meter reading.
- A **due date** rule, for example a set number of days after the bill is issued.

## How a bill is calculated

```text
units used    = current reading − previous real reading
water charge  = units used × price per unit for the connection type
bill          = water charge (or standing fee) + other charges due
```

### Standing fee

The standing fee applies **only when a reading is taken and shows 0 units used**.

| Situation | Charge |
|---|---|
| Reading taken, usage 0 | Standing fee |
| Reading taken, usage above 0 | Units × price only, with no standing fee, even if that is less than the standing fee |
| No reading (blank period) | Nothing |

**Example** (standing fee KES 100, price KES 50 per unit):

| Month | Reading | Usage | Bill |
|---|---|---|---|
| January | 105 | 5 | KES 250 |
| February | 105 | 0 | KES 100 (standing fee) |
| March | — | blank | Nothing |
| April | 108 | 3 (since February) | KES 150 |

### Other charges

Fines, penalties, reconnection fees, and connection fees are added to the customer's account as separate charges. See [Penalties, disconnection, and reconnection](disconnection-and-reconnection.md).

## Bills

- A bill is produced when a reading is recorded for the billing period.
- Every bill shows previous reading, current reading, units used, charges, previous balance, total due, due date, the scheme's Paybill, and the customer's account number.
- Bills are sent by SMS and are visible in the portal and through USSD.
- Disconnected and suspended connections are not billed.

## Opening balances

Balances owed or held in credit before an organization joined the platform are imported as opening balances. See [Data import](data-import.md).

## Requirements

- **BL-01 — Price per connection type:** Each organization sets a price per unit for each connection type.
- **BL-02 — Usage-based bill:** Bills are units used multiplied by the price for the connection type.
- **BL-03 — Standing fee:** If enabled, the standing fee is charged only when a recorded reading shows zero usage.
- **BL-04 — No minimum charge:** When usage is above zero, only usage is charged, even if it is less than the standing fee.
- **BL-05 — Blank periods:** Periods without a reading produce no bill and no standing fee.
- **BL-06 — Flat rate:** Flat Rate connections are billed a fixed amount without readings.
- **BL-07 — Bill content:** Bills include readings, units, charges, balance, due date, Paybill, and account number.
- **BL-08 — Bill delivery:** Bills are sent by SMS and available in the portal and USSD.
- **BL-09 — Bill adjustment:** A corrected reading adjusts the related bill, with an audit trail.

## Questions to confirm

- Are Flat Rate connections billed every month, even when other meters are not read?
- Can tariffs change mid-year, and does a new price apply from a date or from the next reading?
- Should a bill covering several months (after blank periods) be split by month for reporting?
- Is VAT or any other tax added to water bills for any organization type?
