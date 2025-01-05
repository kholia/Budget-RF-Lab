# Home-brew projects
Please feel free to add to this list of projects or modify this accordingly.

## List of starter projects
This contains a list of home-brew projects that you can try.

| Si. No | Name                                 | Assembly Time (in min) | Cost (in INR) | Where to Buy                                       | Comments                                                                                                                                                               | Links                                                                                                                                                                                                                                                           |
|--------|--------------------------------------|------------------------|---------------|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1      | Earthing                             | 2                      | ~0            | NA                                                 | Use a regular 220v (standard line voltage in India) LED bulb between Live and Earth to check.                                                                          |                                                                                                                                                                                                                                                                 |
| 2      | RF Probe                             | 60 minutes             | <200          | LCSC, Robu, Project Point, Synergy Telecom - Delhi |                                                                                                                                                                        | Build one by following [this article](https://n5ese.com/rfprobe1.htm).                                                                                                                                                                                          |
| 3      | Frequency generator (VFO)            |                        | 500-700       | NA                                                 |                                                                                                                                                                        | Details: https://github.com/kholia/pico-hf-oscillator, Alternate: Use https://github.com/kholia/EasyVFO to build a VFO using the Si5351 module and as a hack build a VFO (for shortwave) using Raspberry Pico 2                                                 |
| 4      | Frequency counter                    | 2                      | 500-800       |                                                    | In many use cases, an oscilloscope can be used for checking the frequency of AF and RF signals. Note: Pico 2 has many 5v tolerant pins which is a very useful feature! | DIY using Raspberry Pi Pico 2 and following projects: https://github.com/kholia/pico_ft8_xcvr/tree/main/PicoFrequencyCounter-v2, https://github.com/kholia/pico_ft8_xcvr/tree/main/PicoFrequencyCounter, https://github.com/richardjkendall/rp2040-freq-counter |
| 5      | Commercial Frequency Counter         |                        | 1100          | https://rees52.com/                                | 9V Frequency Meter 500 MHz High Precision Reader RF                                                                                                                    | Related: Build a RF frequency counter buffer for HF https://www.nutsvolts.com/magazine/article/build-an-rf-frequency-counter-buffer-for-hf                                                                                                                      |
| 6      | Frequency reference                  | 15                     |               |                                                    |                                                                                                                                                                        | DIY using https://github.com/kholia/uBlox7_TimePulse project                                                                                                                                                                                                    |
| 7      | Local WSPR / FT8 / CW 10mW RF source | 2                      | ~500          |                                                    |                                                                                                                                                                        | https://github.com/kholia/Easy-Digital-Beacons-v1, https://github.com/kholia/Pico-FT8-TX                                                                                                                                                                        |
| 8      | Local SSB signal source              | 15                     |               |                                                    | All it takes is one wire to solder / plug-in                                                                                                                           | https://github.com/kholia/rpitx                                                                                                                                                                                                                                 |
| 9      | RF Dummy load                        | 30                     | 500-700       |                                                    | DIY using a 50 ohms RF flange resistor + a suitable aluminium heat sink                                                                                                |                                                                                                                                                                                                                                                                 |

## List of more projects

| Si. No | Name                                 | Assembly Time (in min)        | Cost (in INR) | Where to Buy                                       | Comments                                                                                                                                                               | Links                                                                                                                                                                                                                                                           |
|--------|--------------------------------------|-------------------------------|---------------|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1      | Vector Network Analyzer              | 10 hours (with SMT assembly)  |               | JLCPCB, LCSC with factory SMT assembly             | 30 kHz - 1 GHz, 2 port                                                                                                                                                 | https://github.com/profdc9/VNA/                                                                                                                                                                                                                                 | 
| 2      | Antenna Impedance Matcher (Tuner)    | 40 hours                      |               | JLCPCB, LCSC                                       | 1.8 to 30 MHz                                                                                                                                                          | https://github.com/profdc9/ModularTuner/                                                                                                                                                                                                                        | 
| 3      | Carlson Superprobe                   | 1 hour                        |               | JLCPCB, LCSC with factory SMT assembly             | Noise measurement                                                                                                                                                      | https://github.com/profdc9/SuperProbe/                                                                                                                                                                                                                          | 
| 4      | TMatchPCB                            | 1 hour                        |               | JLCPCB, LCSC                                       | HF T-Match for portable use, very cheap, capacitors and inductors are on PCB!                                                                                          | https://github.com/profdc9/TMatchPCB/                                                                                                                                                                                                                           | 
| 5      | Schottky Diode Noise Source          | 1 hour                        |               | JLCPCB, LCSC with factory SMT assembly             | Based on BAT17 diode, up to 2 GHz, 10 to 30 dB attenuation                                                                                                             | https://github.com/profdc9/SchottkyNoiseSource/                                                                                                                                                                                                                 | 
| 6      | RFUtilityKnife                       | 4 hours                       |               | JLCPCB, LCSC with factory SMT assembly             | Five useful circuits: probe, UHF amplifier, Zener Noise Source, Single Balanced Mixer, Differential Probe                                                              | https://github.com/profdc9/RFUtilityKnife/                                                                                                                                                                                                                      | 
| 7      | RFBitBanger                          | 20 hours                      |               | JLCPCB, LCSC with factory SMT assembly             | CW, SSB HF QRP Transceiver built from simple parts for off-grid maintainability                                                                                        | https://github.com/profdc9/RFBitBanger/                                                                                                                                                                                                                         | 
| 8      | SI5351A PLLBoard                     | 1 hour                        |               | JLCPCB, LCSC with factory SMT assembly             | SI5351A PLL breakout board where TCXO can be installed                                                                                                                 | https://github.com/profdc9/PLLBoard/                                                                                                                                                                                                                            | 
| 9      | WA2EBY HF Amplifier                  | 20 hours                      |               | JLCPCB, LCSC                                       | WA2EBY HF amplifier with some minor enhancements                                                                                                                       | https://github.com/profdc9/QRPAmplifier/                                                                                                                                                                                                                        | 

## RF security extended list

- HackRF One

- CC1101 SPI module (two)

  - https://www.ktron.in/product/cc1101-433mhz-module/

- Logic analyzer options

  - DIY using Raspberry Pi Pico

    https://github.com/pico-coder/sigrok-pico

  - [Alternate 1] DIY using Raspberry Pi Pico

    https://github.com/gusmanb/logicanalyzer

  - [Alternate 2] https://robu.in/product/usb-logic-analyze-24m-8ch-mcu-arm-fpga-dsp-debug-tool/

- Fault injection

  - https://github.com/MKesenheimer/fault-injection-library

## Fun Activities

- I want to get started with HF in 30 minutes? Tell me how!

  Build a 10mW WSPR beacon for 10m band using a Raspberry Pi Pico 2 MCU board.

  Use https://github.com/kholia/Easy-Beacons-STEM.

  Alternate: Already own a Raspberry Pi SBC? Then try https://github.com/JamesP6000/WsprryPi.

- I want to start receive HF traffic today - tell me how!

  - RTL-SDR v3 + random wire / active antenna

  - CD2003 receiver (< 500 INR) + random wire / active antenna

    See https://github.com/kholia/ConsensusBasedTimeSync for more details
