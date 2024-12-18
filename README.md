# Budget RF Lab

Build a RF lab on a budget. For homebrewers.

This page is intended to be a `Systemization of Knowledge (SoK)` article.

## Equipment list

- Proper earthing is a must!

  Use a regular 220v (standard line voltage in India) LED bulb between Live and
  Earth to check.

  Time: 2 minutes

  Cost: ~0 INR

- RF probe

  Build one by following [this article](https://n5ese.com/rfprobe1.htm).

  Time: 1 hour

  Cost: < 200 INR

  Vendors: LCSC, Robu, Project Point, Synergy Telecom - Delhi

- Frequency generator (VFO)

  Hack: Build a VFO (for shortwave) using Raspberry Pico 2

  Cost: 500 to 700 INR

  Details: https://github.com/kholia/pico-hf-oscillator

  Alternate: Use https://github.com/kholia/EasyVFO to build a VFO using the Si5351 module.

- Frequency counter

  In many use cases, an oscilloscope can be used for checking the frequency of AF and RF signals.

  DIY using Raspberry Pi Pico 2 and following projects:

  - https://github.com/kholia/pico_ft8_xcvr/tree/main/PicoFrequencyCounter-v2

  - https://github.com/kholia/pico_ft8_xcvr/tree/main/PicoFrequencyCounter

  - https://github.com/richardjkendall/rp2040-freq-counter

  Cost: 500 to 800 INR

  Time: 2 minutes

  Note: Pico 2 has many 5v tolerant pins which is a very useful feature!

  Alternate: 9V Frequency Meter 500 MHz High Precision Reader RF

  Cost: 1100 INR

  Vendor: https://rees52.com/

  Related: Build a RF frequency counter buffer for HF

  https://www.nutsvolts.com/magazine/article/build-an-rf-frequency-counter-buffer-for-hf

- Frequency reference

  DIY using https://github.com/kholia/uBlox7_TimePulse project

  Time: 15 minutes

- Soldering iron options

  BABA i12 Soldering iron

  Cost: 4200 INR

  The soldering iron should have temperature control.

  In a pinch `HIKO Micro Soldering Iron Station – 12V` (350 INR) also works fine but is slow to heat up or `Soldron 25W` (350 INR)!

  Pro-Tip: Invest in good soldering bits (tips) and ceramic tips if you can find them!

- Multimeter - UNI-T ones are recommended.

  UNI-T UT33D+ is quite good for 800 INR.

  Vendor: https://www.toolworld.in

  In a pinch, `Mastech MAS830L Digital Multimeter` (700 INR) works fine.

- Linear power supply options

  - SUGON 3005D Adjustable DC Power Supply (30V~5A) - 5300 INR

  - SUGON 3010PM Adjustable Power Supply (30V~10A) - 9000 INR

  CC CV functionality is a must for running experiments safely!

- Capacitance meter - MS8910 Mastech SMD Measuring Tweezers

  Cost: 2000 INR

  VU2ESE uses Mastech MS8910 too.

- Oscilloscope options

  Any >= 100 MHz Siglent scope which is in your budget.

  Note: `Buy once, cry once` applies here.

  Get a DSO at a minimum.

- NanoVNA

  Recommended vendor: https://www.banggood.in/

- TinySA (Ultra)

  Recommended vendor: https://www.banggood.in/

  Get attenuators from Synergy Telecom - Delhi. Get a bunch of them to mix-and-match.

- RF power + SWR meter

  - Diamond SX20C Power Meter - expensive but worth it

  A cross-needle power and swr meter is super useful for RF work.

  Vendor: https://www.sanchartelesystems.com/ (Delhi)

- RF Dummy load - DIY using a 50 ohms RF flange resistor + a suitable aluminium heat sink

  - Cost: 500 to 700 INR

  - Time: 30 minutes

- Hot air station options

  https://g2mark.com/ and https://babaocamachine.com/ have various options.

  Buy a one which has multiple nozzle sizes and suits your budget.

- SDR options

  - RTL-SDR v3 / v4 - https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/

  - Airspy HF+ Discovery - Possibly the best HF receiver out there?

- Jumper cables - Buy high quality ones from `Project Point` - They are the best!

- Desoldering braid (wick) - Buy Chemtronics branded ones from Otovon vendor

- Magnification

  https://g2mark.com/ and https://babaocamachine.com/ have various options.

  Choose one to suit your budget.

  In a pinch, chose a basic magnifying setup that comes with LED lighting that begin from 300 INR and based on your needs you can upgrade.

- Local WSPR / FT8 / CW 10mW RF source

  Cost: 500 INR

  Time: 2 minutes

  https://github.com/kholia/Easy-Digital-Beacons-v1

  https://github.com/kholia/Pico-FT8-TX

- Local SSB signal source

  Time: 15 minutes (one wire to solder / plug-in)

  https://github.com/kholia/rpitx

- Soldering wire

  - 22 SWG "60/40" mix with rosin core is what we need

  - 0.3mm soldering wire (from 2UUL or Mechanic brand) for soldering finer SMD
    components

- Hardware tools: ESD safe tweezers, nose pliers, screwdriver set (Miniso branded one is decent enough), side cutters, clamp, mini-vice

  Taparia and Stanley tend to make decent stuff.

  You can get good quality tools from most of the local hardware markets as well.

- Line Tester

  - Measuring range of upto 400V

  Any local hardware store for upto 100 INR

- Bench Vice/PCB Vice

  Basic vice from Taparia, etc. from a local hardware shop

  Entry level vice will range from 300 INR to 800 INR

## Tips

- Do NOT make PCBs (very initially)

  Learn to use the standard 1.6mm FR4 copper clad board to build and test
  circuits.

  See https://www.youtube.com/watch?v=xPUmuRSxqys for more details.

## RF security extended list

- HackRF One

- CC1101 SPI module (two)

  - https://www.ktron.in/product/cc1101-433mhz-module/

- Logic analyzer options

  - DIY using Raspberry Pi Pico.

    https://github.com/gusmanb/logicanalyzer

  - https://robu.in/product/usb-logic-analyze-24m-8ch-mcu-arm-fpga-dsp-debug-tool/

- Fault injection

  - https://github.com/MKesenheimer/fault-injection-library

## Software (Free / FOSS)

- LTspice - Sanity-check your ideas using LTspice

- Elsie (https://tonnesoftware.com/elsie.html) for filters - best software ever?

- http://www.ke5fx.com/aadeflt.htm - AADE Filter Design V4.5

- https://www.dl0hst.de/mini-ringkern-rechner.htm#en

- https://coil32.net/ - coil inductance calculating app

- KiCad EDA (EAGLE is dead, waiting for other proprietary software to die too...)

## Fun Activities

- I want to get started with HF in 30 minutes? Tell me how!

  Build a 10mW WSPR beacon for 10m band using a Raspberry Pi Pico 2 MCU board.

  Use https://github.com/kholia/Easy-Beacons-STEM.

  Alternate: Already own a Raspberry Pi SBC? Then try https://github.com/JamesP6000/WsprryPi.

- I want to start receive HF traffic today - tell me how!

  - RTL-SDR v3 + random wire / active antenna

  - CD2003 receiver (< 500 INR) + random wire / active antenna

    See https://github.com/kholia/ConsensusBasedTimeSync for more details

## Credits

- Folks from the [HAMBREWERS group on Telegram](https://t.me/+TwzGyKGe8_QI_B3y)

- https://voidstarsec.com/hw-hacking-lab/vss-lab-guide

- VU2ESE - Ashhar Farhan spoke about starting out home-brewing at LARC 2024.

- R2BDY - Roman

- VU2TNA - Sanal Kumar G

## References

- https://github.com/kholia/HF-Balcony-Antenna-System

- https://github.com/kholia/talks/

- https://www.kk5jy.net/three-wire-gp/

- https://www.pa0fri.com/ (active receiving antenna)
