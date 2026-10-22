# Data import

## Description

When an organization joins, its existing records are on paper or in Excel. Records are brought in using an **Excel template** during onboarding.

## Template contents

| Data | Columns |
|---|---|
| Customers | Name, phone number, National ID (where applicable), member number (where applicable) |
| Connections | Account number, connection type, scheme, zone or building and unit, status |
| Meters | Serial number, **last reading and its date** |
| Balances | **Opening balance**: amount owed or credit held |

## Process

1. The org admin, or the platform admin on their behalf, downloads the template.
2. The organization fills it in and uploads it.
3. The system checks the file and lists every problem, such as a missing phone number, duplicate meter, unknown connection type, or text where a number is expected.
4. **Nothing is saved until the file has no errors.**
5. Once clean, the records are created.

## Effects of the import

- **Last reading** becomes the starting point. The first bill in the system is the next reading minus the imported last reading.
- **Opening balances** become the first entry on each account. Amounts owed are treated as overdue bills under the payment allocation order; credit is applied to the next bill.
- Contracts and documents are not imported. They are uploaded afterwards, and missing ones appear in the customer compliance report.

The import can be run again later, for example when a property manager adds a building or a county takes over another scheme.

## Requirements

- **DI-01 — Template download:** A standard Excel template is available.
- **DI-02 — Validation:** Uploaded files are checked and all errors listed.
- **DI-03 — All or nothing:** No records are saved until the file is free of errors.
- **DI-04 — Starting readings:** Imported last readings are used as the previous reading for the first bill.
- **DI-05 — Opening balances:** Imported balances are recorded as the first account entry.
- **DI-06 — Repeat imports:** Imports can be run after onboarding to add new customers.
- **DI-07 — Who can import:** Org admins and platform admins can run imports.

## Questions to confirm

- Should an import be able to update existing records, or only add new ones?
- Is historical reading and payment history imported, or only the latest reading and balance?
- Should imported accounts start verified, or must every customer complete SMS verification?
