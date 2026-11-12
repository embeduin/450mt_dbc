# 450mt_dbc
Reverse-engineered CFMOTO 450MT (IBEX) CAN bus messages.

## Habr article
https://habr.com/ru/articles/1092146/

## Bike Used
CFMOTO 450MT (IBEX) 2026MY

## Tools Used
- SavvyCAN: https://github.com/collin80/SavvyCAN
- python-can: https://github.com/hardbyte/python-can
- python-can-isotp: https://github.com/pylessard/python-can-isotp

## CAN Bus Connection
Classic OBDII connector under the seat:
pin 6 = CAN-High;
pin 14 = CAN-Low.

CAN bus baudrate is 500 kbit/s.

## Message Table

| id    | size | cycle time, ms | sender |
|-------|------|----------------|--------|
| 0x110 |    8 |             10 |    ECU |
| 0x111 |    8 |             10 |    ECU |
| 0x120 |    8 |             20 |    CLU |
| 0x123 |    8 |             20 |    ECU |
| 0x12B |    8 |             10 |    ABS |
| 0x12F |    8 |             20 |    ABS |
| 0x151 |    8 |             50 |    CLU |
| 0x153 |    8 |             50 |    CLU |
| 0x154 |    8 |             50 |    CLU |
| 0x163 |    8 |             50 |    CLU |
| 0x251 |    8 |            100 |    CLU |
| 0x2F3 |    8 |            200 |    CLU |
| 0x30E |    8 |            500 |    CLU |
| 0x321 |    8 |            500 |    CLU |
| 0x402 |    8 |           1000 |    CLU |

## Disclaimer (boring stuff)
**Research Only**: All data in this repository provided strictly for educational and research purposes.
**No Guarantees**: Decoded signals may be incomplete, inaccurate, or specific to a single hardware/firmware revision.
**Hardware & Vehicle Risk:** Interacting with an active vehicle CAN bus can trigger DTCs, disable safety systems or cause permanent ECU damage. 
You assume all responsibility for how you use this information.
