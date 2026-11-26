# target-3-board

`target-3` is an open-source machine that raises knockdown targets for shooting.

This repository contains the KiCad data of the boards for `target-3`.
The boards hold the microcontroller boards, supply power, and connect them with the servo motors and the push button.

Please refer to these repositories if you are interested in other modules of `target-3`.

* Remote: https://github.com/katsuster/target-3-remote
* Server: https://github.com/katsuster/target-3-server


## Requires

* Software
  * KiCad 10.0


## How to use

TBD


## Source structures

* remote/
  * Remote controller board, holds the remote microcontroller board (e.g. M5Stamp C3)
  * Supplies power to the microcontroller board
  * Has a connector for an external push button
* server/
  * Server board, holds the server microcontroller board (e.g. M5Stamp C3)
  * Sends PWM signals and power enable signals to the motor driver boards
* motor/
  * Motor driver board, used to drive servo motors
  * Supplies power to the servo motors through its own power switch
  * Passes the PWM signals from the server board through to the servo motors


## Other documents

* [Parts list](doc/parts_jlcpcb.md)
