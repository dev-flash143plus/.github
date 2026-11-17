<img src="images/start_pic_00.jpg" width="800" alt="flash143plus">

# flash143plus

<img src="images/logo_flash143plus_v10.png" width="200" align="right" alt="flash143plus Logo">

**flash143plus**... ein echtes Firmware-Upgrade für den D143 Decoder. Endlich 100% Leistung und den Ghostcar-Modus, schaltbares Licht und individuelle Geschwindigkeitsprofilen.

Diese gibt es nur bei flash143plus.

Die Windows App dient dabei zur Übertragung der Firmware auf den µController und zum erstellen und editieren der Geschwindigkeitsprofilen. Die Firmware ist kompatibel mit den digitalen Rennbahnen von Carrera®.[^1]

## Entwicklung

Bei der Entwicklung von flash143plus konnte für die grundlegenden Informationen über das digitale Datenprotokoll auf die Webseiten von Stephan Heß [slotbaer.de](http://slotbaer.de/) und Peter Niehues [wasserstoffe.de](http://www.wasserstoffe.de) zurück gegriffen werden. Maßgeblich beteiligt am entstehen von flash143plus ist auch Dusan Borovnik [Die Eifelpiste](https://eifelpiste.jimdofree.com). Viele Ideen für Funktionen der Firmware und der Windows Anwendung stammen von ihm. Vielen Dank dafür!

Mehr Informationen darüber finden sich in den Forenbeiträgen auf [carrera-go.info](https://www.carrera-go.info).

**siehe auch:**

- [carrera-go.info - Alternative Firmware für den D143 Decoder](https://www.carrera-go.info/forum/index.php?thread/21189-alternative-firmware-f%C3%BCr-den-d143-decoder/&postID=269617#post269617)

## Funktionen

Die grundlegende Idee der flash143plus Firmware ist es, den D143-Decoder mit den Funktionen des D132-Decoders auszustatten. Am wichtigsten ist die Möglichkeit die Höchstgeschwindigkeit einstellen zu können. Die originale Firmware begrenzt den D143-Decoder zudem auf nur etwa 80% der max. möglichen Geschwindigkeit. Ein weiterer wichtiger Punkt ist der Ghostcar Modus.

| Funktion der Decoder-Firmware | original D143 | flash143plus |
|---|---|---|
| Höchstgeschwindigkeit | ca. 80% | 100% |
| Anz. Geschwindigkeitsprofile | 1 | 5 |
| Geschwindigkeitsprofil anpassen | nein | ja, grafisch editierbar |
| Ghostcar Modus | nein | ja |
| schaltbare Beleuchtung | nein | ja, mehrere Optionen |

## Voraussetzungen

Neben dem aktuellen Windows-PC zum ausführen der flash143plus Anwendung wird zum übertragen der flash143plus Firmware auf den D143-Decoder ein Programmieradapter benötigt. Ein besonders günstiges Gerät ist der USBasp, entwickel von Thomas Fischl. [fischl.de/usbasp](http://www.fischl.de/usbasp) Zu Anfang als Selbstbauprojekt gedacht, gibt es inzwischen den USBasp V2.0 aus fernöstlicher Produktion für wenige Euros. Die nötige Treibersoftware [Zadig](https://zadig.akeo.ie/) für dieses Gerät findet sich auch im flash143plus Softwarepaket. Des weiteren braucht man einen passenden Anschlussstecker für den Decoder. Dem USBasp liegt ein Flachbandkabel bei, das dafür umgebaut werden kann.

## Programmieradapter und Stecker

Ein ISP-Stecker (**I**n-**S**ystem-**P**rogrammierung) ermöglicht das programmieren eines µControllers direkt in der fertig aufgebauten Platine. Der Umbau des Flachbandkabels ist eine einfache Möglichkeit sich einen passenden Stecker herzustellen und ist [HIER](https://www.carrera-go.info/forum/index.php?thread/21189-alternative-firmware-f%C3%BCr-den-d143-decoder/&postID=270157#post270157) beschrieben.

- USBasp V2.0
- SOIC8 Programmier-Clip
- ISP-Stecker für den D143 Decoder
- ISP-Stecker für die D143 Weiche

## Firmware-Varianten

### Decoder Firmware

- P.ad.S - Programmierung auf der Schiene
- Lights - Licht und Bremslicht mit flash143plus
- Race - Alles, nur kein Schnickschnack
- Pitstop - Modus für CockpitXP

### Weichen-Firmware

- PLE - Einfahrt Boxengasse
- SLC - Streckenweiche

## Anleitungen

- [Installation von flash143plus Version 0.9.3](docs/install_v0931.md)
- [Was sind die Gaskurven und was kann ich damit machen?](docs/gaskurven_01.md)

## Download

[flash143plus Freeware2025](downloads/)

[^1]: Carrera® ist ein Markenname der Stadlbauer Marketing + Vertrieb Ges.m.b.H. <https://carrera-toys.com/about>
