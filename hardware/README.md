# Hardware

## Bill of materials

[`bill_of_materials.csv`](bill_of_materials.csv) lists every component from the final report with quantities and
prices in **BDT** (lowest retail prices found online in Bangladesh).

| Group | Items | Cost (BDT) |
|---|---|---|
| Ground station | 18 | 3,588 |
| Drone / UAV | 17 | 31,437 |
| **Total (sum of the lines)** | **35** | **35,025** |

> The final report states **36 sets and 35,070 BDT**. The line items add up to 35 sets and 35,025 BDT (a difference of
> 1 set and 45 BDT). The motor is listed once, although a quadcopter uses four motors - confirm your own quantities.

## Ground-station pin map (Arduino UNO)

Taken from `firmware/GroundStation/GroundStation.ino`.

| Function | Pin | Notes |
|---|---|---|
| DHT22 data | D2 | `DHT` library, type `DHT22` |
| Soil moisture - Zone 1 | A0 | analogue |
| Soil moisture - Zone 2 | A3 | analogue |
| Soil moisture - Zone 3 (main line) | A5 | analogue |
| Servo 1 (Zone 1 gate) | D9 | closed = 180, open = 90 |
| Servo 2 (Zone 2 gate) | D10 | closed = 0, open = 90 |
| Pump relay | D4 | **active-LOW**: HIGH = pump OFF, LOW = pump ON |

## Safety

- Keep the 12 V adapter and relay wiring dry and insulated; fit a flyback diode across the pump motor.
- Remove the propellers when bench-testing the drone.
- Charge and store the LiPo battery safely and add a low-voltage alert.
- Follow your local aviation authority's rules before flying.
