# sleeping-cell-indicator-data

This repository contains three groups of sleeping cell indicator data. Sleeping cell is a special kind of cell degradation. A cell is called degraded in case if it is not 100% functional - its services are suffering in terms of quality what affects user experience. There exist a vague classification of degraded cells depending on how much they affect the network operation:
- Degraded cell - which still carries some traffic, but the performance characteristics are slightly lower, than in case of fully operational cell.
- Crippled cell - is characterized by a severely decreased capacity due to a failure of a base station component.
- Catatonic cell - does not carry any traffic in one or both directions and is inoperable. This might be a result of severe equipment or software failure.

Network simulation is performed to simulate the three types of sleeping cell acenarios, wich uses a system-level simulation platform, [NS3](https://www.nsnam.org/). Each data file contians 8 attributes, i.e., time, user coordinate X, user coordinate Y, user ID, base station ID, RSRP, RSRQ, RLF indicator. Transmit power of base station 4 is set as 36dBm, 26dBm and 6dBm (the transmit power of healthy cell is 46dBm) to generate degraded cell, crippled cell and catatonic cell, respectively, and transmit power is changed at fifth minute.

# simulation parameters

| Parameter | Value | 
| ------ | ------ | 
| Num. cells | 21 |
| Num. users | 200 |
| Macro cell layout | radius:500m|
|Path loss model| Friis spectrum propagation |
| UE distribution | Uniform random distribution |
| UEs’ mobile model | 30 km/h |
| Shadow fading | Log-normal,std=8dB |
|Tx power for healthy cell| 46 dBm |
|x power for degraded cell | 36 dBm |
|Tx power for crippled cell | 26 dBm |
|Tx power for catatonic cell | 6 dBm |
| A2 RSRP/RSRQ threshold | -110/-10 |
| A2 RSRP/RSRQ hysteresis | 3/2 |

