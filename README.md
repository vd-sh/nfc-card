# nfc-card
This PCB card features an integrated NFC antenna. I built this to replace traditional paper cards with a sleek piece of hardware that instantly shares a digital portfolio or contact info when tapped to a compatible device.

## What is this?
This is a PCB NFC Card designed around a custom 13.56MHz copper antenna loop. The card operates as a passive **Near Field Communication (NFC) transponder**. When brought near an active NFC reader (such as a smartphone or dedicated scanner), the integrated copper coil harvests electromagnetic energy over the air to power the onboard IC. Once energized, the chip modulates the field to transmit its stored data payload wirelessly, enabling data transfers, automated logic triggering, or wireless access authentication without requiring a battery.

1) Schematic:

   <img src="Assets/Screenshot-2026-09-22-222913.png" width="300">

2) Raw PCB:

   <img src="Assets/Screenshot-2026-09-23-174717.png" width="300">

3) 3D PCB (Black, Front):

   <img src="Assets/Screenshot-2026-09-23-180846.png" width="300">

4) 3D PCB (Black, Back):

   <img src="Assets/Screenshot-2026-09-23-181054.png" width="300">

## Repository Structure

```text
nfc-card/
|
|---- Assets/-----------# Images and visual references for the project
|            -----------# (Schematic diagrams, Raw PCB renders, 3D PCB views, Fonts, etc)
|
|---- Hardware/---------# Source design files for the PCB
|              ---------# (EasyEDA schematics, PCB layout, Gerber files, all PCBA Manufacturing Files)
|
|---- BOM.csv-----------# Bill of Materials
|
|---- LICENSE-----------# MIT License
|
|---- README.md---------# Project documentation and instructions
```

## How to edit the source files and get your NFC PCB Card?
1. First, download all the source files from the [Hardware](Hardware/) directory
2. Open the web interface or desktop client for EasyEDA Standard
3. Go to File > Open > EasyEDA Standard Project
4. Select and import the files from this repository to load the schematics and PCB layout
5. Hurray, edit your name and printables like a QR Code, etc you want on your silk layer (top and bottom), and export YOUR gerber.zip to JLCPCB (Or any fabricator) to get a print!
6. Once you get your card shipped to you. You can write on it with a writing tool to make it fully functional. In my case, I am using a PN532 Module with a CP2102 USB 2.0 to TTL Converter for laptop compatibility.
7. You may also password-protect it to avoid overwriting. (Optional)

## Fabrication specs
If you want to order a batch of these for yourself, here is the exact recipe to use on a manufacturing unit like JLCPCB to get the same;

- Layer: 2 Layers (Do not change this to 1, or the antenna jump loop will break)
- Base Material: FR4 (1mm thickness)
- Solder Mask: (You can choose your preferred color)
- Silkscreen: White (Default) (Choose whatever contrasts well with your PCB color)
- Finish: HASL
- Via Covering: Via Tented

## [BOM](BOM.csv) as a table

|Item                                                                  |Quantity|Price (USD)|Link                      |
|----------------------------------------------------------------------|--------|-----------|--------------------------|
|2 Layer PCB (Includes Shipping)                                       |10       |19.24      |https://jlcpcb.com                |
|PN532 NFC Reader/ Writer Module (Includes Shipping)                   |1       |5.0        |https://amzn.in/d/0ftbYPtk|
|CP2102 USB 2.0 to TTL UART Serial Converter Module (Includes Shipping)|1       |3.0        |https://amzn.in/d/03JLL8i2|
|Total Amount                                                          |        |27.24      |                          |


## Cart Images
1) JLCPCB

    ![jlcpcb cart](Assets/Screenshot-2026-09-25-025149.png)

2) Amazon

    <img src="Assets/Screenshot-2026-09-28-005618.png" width="200">
## License
[MIT](LICENSE) - Use, modify, share, etc. as you like!

## Notes
- Will update on how to use once I get my card shipped!
- The card in the repo has less info due to privacy, but you may add whatever you like while editing the source PCB.
- If y'all like this, you may love to see [Stardance- Luminator](https://github.com/vd-sh/luminator) and [Stardance- MP3 Player](https://github.com/vd-sh/mp3-player)
- To see my latest projects, you may visit my [profile](https://github.com/vd-sh) :)
