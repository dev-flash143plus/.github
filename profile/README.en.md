 <img width="948" height="106" alt="start_pic_00" src="https://github.com/user-attachments/assets/efb74d04-d14c-404e-b922-2e67a7affb60" />

[🇩🇪 Deutsch](README.md) | [🇬🇧 English](README.en.md)

# flash143plus

**flash143plus** ... a genuine firmware upgrade for the D143 decoder. Finally, 100% performance, Ghost Car mode, switchable lights and individually configurable speed profiles.

These features are exclusively available with <img width="149" height="53" alt="logo_flash143plus_v10" src="https://github.com/user-attachments/assets/7dfec277-713a-4942-a372-8af79089fae7" />

The Windows application is used to transfer the firmware to the microcontroller and to create and edit speed profiles. The firmware is compatible with Carrera® digital slot car racing systems.[^1]

## Development

During the development of flash143plus, the websites of Stephan Heß [slotbaer.de](http://slotbaer.de/) and Peter Niehues [wasserstoffe.de](http://www.wasserstoffe.de) provided essential information about the digital data protocol.

Dusan Borovnik [Die Eifelpiste](https://eifelpiste.jimdofree.com) also played a major role in the development of flash143plus. Many ideas for firmware features and the Windows application came from him. Many thanks!

More information can be found in the forum discussions on [carrera-go.info](https://www.carrera-go.info).

**See also:**

- [carrera-go.info - Alternative firmware for the D143 decoder](https://www.carrera-go.info/forum/index.php?thread/21189-alternative-firmware-f%C3%BCr-den-d143-decoder/&postID=269617#post269617)

## Features

The basic idea behind the flash143plus firmware is to equip the D143 decoder with the features of the D132 decoder. The most important improvement is the ability to adjust the maximum speed.

The original firmware also limits the D143 decoder to only about 80% of its maximum possible speed. Another important feature is Ghost Car mode.

| Decoder firmware feature | Original D143 | flash143plus |
|---|---|---|
| Maximum speed | approx. 80% | 100% |
| Number of speed profiles | 1 | 5 |
| Adjustable speed profiles | No | Yes, graphically editable |
| Ghost Car mode | No | Yes |
| Switchable lights | No | Yes, multiple options |

## Requirements

In addition to a current Windows PC to run the flash143plus application, a programming adapter is required to transfer the flash143plus firmware to the D143 decoder.

One particularly inexpensive option is the USBasp, developed by Thomas Fischl ([fischl.de/usbasp](http://www.fischl.de/usbasp)). Originally intended as a DIY project, the USBasp V2.0 is now available from Far Eastern manufacturers for just a few euros.

The required driver software ([Zadig](https://zadig.akeo.ie/)) for this device is also included in the flash143plus software package.

You will also need a suitable connector for the decoder. The ribbon cable supplied with the USBasp can be modified for this purpose.

## Programming adapter and connector

An ISP connector (**I**n-**S**ystem **P**rogramming) allows a microcontroller to be programmed directly on the fully assembled circuit board.

Modifying the ribbon cable is a simple way to create a suitable connector. Instructions can be found [HERE](https://www.carrera-go.info/forum/index.php?thread/21189-alternative-firmware-f%C3%BCr-den-d143-decoder/&postID=270157#post270157).

- USBasp V2.0
- SOIC8 programming clip
- ISP connector for the D143 decoder
- ISP connector for the D143 lane changer

## Firmware variants

### Decoder firmware

- P.ad.S - Programming on the track
- Lights - Lights and brake lights with flash143plus
- Race - Everything you need, without unnecessary extras
- Pitstop - Mode for CockpitXP

### Lane changer firmware

- PLE - Pit lane entry
- SLC - Track lane changer

## Guides

- [What are throttle curves and what can I do with them?](../docs/speed-curves.en.md)

[^1]: Carrera® is a registered brand name of Stadlbauer Marketing + Vertrieb Ges.m.b.H. <https://carrera-toys.com/about>
