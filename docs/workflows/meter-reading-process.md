# Meter-reading workflow

## Online reading

1. The reader opens the app and selects an assigned route.
2. The reader selects the meter.
3. The app displays the previous reading.
4. The reader enters the current reading and takes a photo of the meter.
5. The app requests location permission and captures GPS coordinates when available.
6. The system checks whether the reading is lower than the previous reading or an unusually large increase.
7. The reader reviews any warning and submits.
8. The system produces a bill and sends it by SMS.

## Meter cannot be read

1. The reader selects **Not read** and chooses a reason (locked gate, broken meter, obstructed, other).
2. No bill and no standing fee are produced for the period.
3. The meter appears on the unread meters report.
4. The next real reading covers all usage since the last real reading.

## Offline reading

1. The reader records readings, photos, and not-read reasons without a network connection.
2. They are saved on the phone.
3. When connectivity returns, the app synchronizes them and bills are produced.

Offline conflict handling and synchronization status indicators still need to be designed.

## Main supply reading

Readers also capture readings from the main source meter, such as a pumping station or tank. The system compares supplied water with water sold to estimate water loss.
