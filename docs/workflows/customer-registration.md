# Customer registration workflow

This workflow applies to community schemes, counties, and water service providers. For tenants of property managers, see [Tenant move-in and move-out](tenant-move-in-move-out.md).

## Primary flow

1. The field officer selects the scheme they are assigned to.
2. The field officer records the customer's details and connection type. Status: **Applied**.
3. The system creates a customer account linked to the mobile number, and the customer receives an SMS verification code.
4. The customer verifies the account and sets a password (portal), or uses USSD with their phone number.
5. The customer pays the connection fee to the scheme's Paybill. Status: **Fee paid**.
6. The customer signs the user agreement and, where required, land consent form. The field officer uploads them.
7. The field officer installs the meter and records its serial number, starting reading, meter photo, and GPS location. Status: **Installed**.
8. The connection becomes **Active**. The system will not activate it until the fee is paid and the contract uploaded.
9. Billing starts from the starting reading.

## Expected outcome

The customer belongs to the correct scheme, has an active connection with a starting reading, and can use the portal or USSD.

## Exceptions to define

- The phone number is already associated with an account.
- SMS delivery fails or the verification code expires.
- Required customer information is unavailable.
- A contract is missing or an uploaded file cannot be read.
- The customer pays the connection fee but the meter cannot be installed.
