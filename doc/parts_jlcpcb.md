# Parts list

## 2026/11 server (tag: 20261126-jlcpcb-order-server)

Here is a parts list of the 2026/11 order of the server board for JLCPCB.

| Parts | Package | Manufacturer | Product | JLCPCB ID |
|--|--|--|--|--|
| Pin header       | --         | --        | (Hand soldering) | --       |
| XH 6-pin         | Horizontal | JST       | (Hand soldering) | --       |
| Resistor (5.1k)  | 0603       | UNI-ROYAL | 0603WAF5101T5E   | C23186   |
| Resistor (10k)   | 0603       | UNI-ROYAL | 0603WAF1002T5E   | C25804   |
| Diode (TVS)      | SOD-323    | Diodes    | DESD5V0S1BA-7    | C177022  |
| Diode (Schottky) | SOD-123    | R+O       | B5819W           | C7420330 |
| USB-C            | Horizontal | SHOU HAN  | TYPE-C 6P        | C456012  |


## 2026/11 remote (tag: 20261126-jlcpcb-order-remote)

Here is a parts list of the 2026/11 order of the remote board for JLCPCB.

| Parts | Package | Manufacturer | Product | JLCPCB ID |
|--|--|--|--|--|
| Pin header       | --         | --        | (Hand soldering) | --       |
| XH 4-pin         | Horizontal | JST       | (Hand soldering) | --       |
| Resistor (5.1k)  | 0603       | UNI-ROYAL | 0603WAF5101T5E   | C23186   |
| Resistor (10k)   | 0603       | UNI-ROYAL | 0603WAF1002T5E   | C25804   |
| Diode (TVS)      | SOD-323    | Diodes    | DESD5V0S1BA-7    | C177022  |
| Diode (Schottky) | SOD-123    | R+O       | B5819W           | C7420330 |
| USB-C            | Horizontal | SHOU HAN  | TYPE-C 6P        | C456012  |

Notes:

* The B5819W (C7420330) needs `FT Rotation Offset` = 180 for the Fabrication Toolkit, or it is placed in reverse.


## Requirements for replacement parts

Parts may be discontinued.
Choose replacement parts that meet these requirements.
Check the rotation and position in the JLCPCB preview again after replacing parts.

| Parts | Requirements | Used for |
|--|--|--|
| Pin header       | 2.54mm pitch, 1x10 and 1x12 | Holding the M5Stamp C3 |
| XH connector     | JST XH, 2.5mm pitch, right angle (S6B-XH-A for server, S4B-XH-A for remote) | Server: to motor boards, Remote: to external buttons |
| Diode (TVS)      | Bidirectional, VRWM >= 5V, VBR(min) >= 5.5V, IPP >= 6A (8/20us), SOD-323 | ESD and surge protection of USB-C VBUS |
| Diode (Schottky) | VR >= 20V, IF >= 1A, SOD-123, low VF | Reverse current protection between USB-C VBUS and the 5V pin of M5Stamp C3 |
| USB-C            | Power only 6-pin (VBUS, GND, CC1, CC2), pads compatible with GCT USB4125-xx-x 6P | Power input |

* TVS: VBUS can be 5.25V or higher (5.36V measured with no load), so a part with higher VBR(min) leaks less.
  DESD5V0S1BA-7 (VBR min 5.5V, IPP 12A) was chosen over D5V0L1B2WS-7 (VBR min 6V, IPP 6A) for the higher surge current.
* TVS: Unidirectional parts also work on VBUS, but check the orientation (cathode to VBUS).
* USB-C: Check the position in the JLCPCB preview. The part may not match the footprint origin.
