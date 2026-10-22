# Meter reading and water tracking

## Reading frequency

Each organization sets how often it reads meters. Some read every month; others skip months. A reading period without a reading is **blank**:

- No bill is produced for a blank period.
- No standing fee is charged for a blank period.
- Usage is never estimated.
- The next real reading covers all units used since the last real reading.

**Example:** January is read. February and March are blank. April is read. The April bill charges all units used from the January reading to the April reading.

## Taking a reading

1. The meter reader opens the app and selects an assigned route.
2. The app shows each meter's previous reading.
3. The reader enters the current reading and **takes a photo of the meter**.
4. The app captures GPS coordinates when location permission is granted.
5. The system flags a reading that is lower than the previous reading or an unusually large increase. The reader reviews the warning before submitting.
6. Without network coverage, readings and photos are saved on the phone and synchronized when connectivity returns.

## Meters that cannot be read

When a meter cannot be read, the reader records a **"not read" reason** instead of a number, such as:

- Locked gate or no access
- Meter broken or damaged
- Meter buried or obstructed
- Customer absent (where access requires them)
- Other, with a note

Unread meters and their reasons are shown in the unread meters report. Meters left blank several periods in a row are highlighted for follow-up.

## Meter problems

- **Meter replaced:** the old meter's final reading and the new meter's starting reading are both recorded, so usage is not overstated.
- **Meter rollover:** a reading that wrapped past the meter's maximum (for example 9999 to 0000) is flagged for a manager to confirm. It is never billed as negative usage.
- **Wrong reading:** a manager can correct it. The original value, new value, who changed it, and why are logged. If the reading was already billed, the bill is adjusted.

## Main supply meter

Readers also record readings at the main source meter, such as a pumping station or tank. The system compares water supplied with water sold to estimate water lost through leaks or illegal connections.

## Requirements

- **MR-01 — Route assignment:** Readers see only their assigned routes.
- **MR-02 — Reading history:** The previous reading is visible during data entry.
- **MR-03 — Validation:** Lower-than-previous and unusually high readings are flagged.
- **MR-04 — GPS capture:** Coordinates are attached to a reading when available and permitted.
- **MR-05 — Offline capture:** Readings and photos can be stored offline and synchronized later.
- **MR-06 — Supply readings:** Main supply meter readings are recorded separately from customer meters.
- **MR-07 — Water-loss comparison:** The system compares supplied water with water sold to estimate loss.
- **MR-08 — Map view:** Authorized managers can view meter locations on a map.
- **MR-09 — Meter photo:** Each reading includes a photo of the meter, visible to managers and the customer.
- **MR-10 — Reading frequency setting:** Each organization configures how often meters are read.
- **MR-11 — Not-read reason:** A reader can record why a meter was not read instead of entering a reading.
- **MR-12 — No estimates:** Missing readings are never estimated; the next real reading covers the whole gap.
- **MR-13 — Meter replacement:** Replacing a meter records the old final reading and the new starting reading.
- **MR-14 — Rollover handling:** Rollovers are flagged for manager confirmation.
- **MR-15 — Reading correction:** Managers can correct readings, with an audit trail.

## Questions to confirm

- What counts as an "unusually high" increase, and should the threshold vary by connection type?
- How should conflicting offline edits be resolved?
- Is the unit always cubic metres, or can an organization use litres?
- Is a meter photo mandatory for every reading, or only when the reading is flagged?
- What exact formula and reporting period should be used for water loss?
