[🇩🇪 Deutsch](speed-curves.de.md) | [🇬🇧 English](speed-curves.en.md)
# Was sind die Gaskurven und was kann ich damit machen?

Ein Erfahrungsbericht von [go-digital-132](https://www.carrera-go.info/index.php?user/8085-go-digital-132/) aus dem carrera-go Forum. Vielen Dank dafür!
---

## 1. Was machen die Gaskurven?
Mit den Gaskurven lässt sich beeinflussen, wieviel Gas (= Spannung) vom Decoder an das Auto weitergereicht wird.

Technisch funktioniert das so, dass der Regler je nach Stellung des Reglers einen von fünfzehn Gaspedalwerten an die CU schickt, von dort aus geht der Befehl weiter an den Decoder des betreffenden Autos, die Spannung am Motor des Autos höher oder niedriger zu setzen, was das Auto dann schneller oder langsamer macht. Mit den Gaskurven kann man nun festlegen, wieviel Gas (= also wieviel Spannung) beim Auto ankommen soll. Es gibt insgesamt fünfzehn Gaspunkte, die zusammen die Kurve ergeben. Ein Wert von 0 bedeutet „Motor aus“, ein Wert von 255 bedeutet „Vollgas“, Werte dazwischen entsprechend mehr oder weniger Gas.\\

## 2. Warum ist das relevant?
Damit lassen sich viele Dinge nach persönlichen Vorlieben erreichen:

   - **Freischaltung des technisch maximal möglichen Vollgas an einem D143 Auto**, was bei den Decodern im Carrera-Originalzustand nicht der Fall ist - dort ist bei ca. 80% der möglichen Leistung Schluss, obwohl die Autos Vollgas verkraften würden.
   - **Umgekehrt ist auch eine Drosselung des Vollgases möglich**, z.B. wenn Fahrzeuge eingesetzt werden, die aufgrund Ihres Aufbaus bei zu starkem Gas unkontrollierbar werden (Autos mit hohen Schwerpunkt oder magnetlose Autos). Oder auch, wenn man z.B. mit Kindern spielt, die noch nicht das Gefühl haben in den Fingern, ein Auto an den Grenzen der Physik zu fahren.
   - **Eine bessere Dosierung des Reglers wird möglich nach persönlichen Präferenzen**. Manche bevorzugen einen Regler, der anfangs nur wenig das Gas beeinflusst, später dafür schneller zum Vollgas kommt. Andere bevorzugen das Gegenteil – schnell auf eine mittlere Geschwindigkeit kommen, und „ganz oben“ am Ende des Spektrums dann sehr feinfühlig dosieren zu können. Manche setzen die Gaswerte an den unteren Punkten schon relativ hoch an, denn was bringt es, wenn am Auto bei der niedrigsten Reglerstellung zwar Spannung/Leistung anliegt, das Auto aber so sehr schleicht, dass es die nächste Weiche wird nicht packen können?
   - **Beeinflussung der Verlangsamung des Autos, wenn mit der 132er CU gefahren wird und einer der beiden Tankmodi eingeschaltet ist**. Carrera hat das nämlich sehr elegant gelöst – stellt die CU fest, dass ein Auto „leer“ ist, dann wird die Maximalgeschwindigkeit des Wagens in diesem Zustand auf den zehnten von fünfzehn Gaspunkten gesetzt (selbst wenn man den Regler komplett durchgedrückt hat, es kommt niemals mehr Gas am Auto an, als bei der zehnten Reglerstellung). Man kann sich also eine Gaskurve so bauen, dass man die Verlangsamung des Auto kaum merkt (höhere Werte nahe an 255), oder dass die Verlangsamung des Autos sehr spürbar ist (Werte um die 130). Das letztere ist vor allem für die spannend, die nicht dauerhaft Driver Displays, Bildschirme, Tablets oder Handys im Blick haben können oder wollen, um so sofort zu merken, dass der Tank alle ist.\\

## 3. Wie kann ich die Gaskurven in flash143plus verwenden?
Von Haus aus sind 5 Gaskurven mitgeliefert, die bei Installation von flash143plus verfügbar sind:
  * Kind 1
  * Kind 2
  * Kind 3
  * Vollgas 1
  * Vollgas 2
Für jede Kurve sind die entsprechenden Gaswerte hinterlegt:

  * So läuft z.B. die Kurve „Kind 3“ vom Gaswert 38 bis Gaswert 179 – das ist also eine Gaskurve, die absichtlich auf Vollgas verzichtet, die Autos also „abregelt“ bei ca. 70% ihrer technisch möglichen Maximalgeschwindigkeit. „Kind 2“ und „Kind 1“ drosseln die Maximalgeschwindigkeit noch stärker, perfekt für die allerersten Fahrversuche der Kleinsten.
  * Die Kurve „Vollgas 1“ schaltet das Vollgas frei und das in einer Art und Weise, dass bei niedrigeren und mittleren Regelstellungen relativ wenig zusätzliches Gas abgegeben wird, zum Ende hin (wenn man also den Regler durchdrückt) dann nochmals ein fetter „Boost“ dazukommt. So eine Art Turboloch am Anfang, und wenn der Turbo dann genügend Luft zum Atmen hat, dann haut er nochmal so richtig ins Volle rein 😊
  * Die Kurve „Vollgas 2“ schaltet ebenfalls das Vollgas frei, aber in einer Art und Weise, dass das Gas linear angehoben wird mit jedem tieferen Drücken des Reglers. Eher mit einem Elektroauto zu vergleichen, wo stets dasselbe Drehmoment das Auto wie mit einem Gummiband beschleunigt.
  * Wie bereits weiter oben beschrieben ist der zehnte Punkt auf der Gaskurve (P10 genannt) sehr relevant, weil dies die maximale Geschwindigkeit ist, falls man mit einem der beiden Tankmodi der 132er CU fährt und der Tank „leergefahren“ ist. Man kann sich also die Kurve so legen, dass man genau die Maximalgeschwindigkeit bei leerem Tank bekommt, die man als vernünftig erachtet (z.B. um leeren Autos deutlich zu zeigen, dass sie jetzt nun wirklich in die Box müssen, ohne dass der betroffene Wagen sofort zum Unfallschwerpunkt wird, wenn er zu langsam wird).

Die Schaltflächen sind beschriftet, und tun das was draufsteht. Nicht alle sind in der Demo aktiv.

**Kurve Zeichnen**. Um eine Kurve zu Zeichnen wählt man durch Klick auf eines der farbigen Kurvenfelder zuerst die gewünschte Kurve aus. Anschließend positioniert man den Mauszeiger in das Grafikfenster und klickt mit der linken Maustaste um diese Position zu übernehmen. Das wiederholt man für jeden der 15 Geschwindigkeitswerte. Mit dem Mausrad lassen sich die Werte fein einstellen.

**Kurve Speichern**. Damit wird die aktive kurve nach Eingabe eines Namens in die Motorkurven-Datenbank übernommen.

**Kurve Zuordnen**. Die gespeicherten Kurven in der Motorkurven-Datenbank könne dort mit einem rechten Mausklick einer Kurve zugeordnet oder gelöscht werden.

**Kurve Flashen**. Alle Kurven die sich im Grafikfenster befinden werden durch "Kurven flashen" auf den Controller übertragen. \\

## 3. Was könnte die Zukunft bringen?
Eventuell gibt es in kommenden Updates von flash143plus neue Features, die die Gaskurvenfunktion benutzen, z.B.

  * Eine Option, wie ein Auto schon vor „leerem Tank“ langsam immer langsamer wird, um auf das Leerwerden des Tanks aufmerksam zu werden und es noch rechtzeitig in die Box zu schaffen, bevor Runden nicht mehr gezählt werden.
  * Eine Hardcore Variante, wo bei einem leeren Tank das Auto brutal stoppt und der betroffene Fahrer damit sofort wie im richtigen Leben auch aus dem Rennen ausgeschieden ist.
  * Man könnte z.B. damit auch zufallsbedingt Autoschäden simulieren durch unregelmäßig auftretendes Stottern des Autos und damit einhergehend in die Box fahren müssen, um dies richten zu können.

Aber selbst ohne künftige neue Features: Die Gaskurven sind sehr mächtig und ermöglichen es jedem 143er Fahrer Einfluss auf das Fahrverhalten der Autos auszuüben.

**Beispiel gefällig?** Der folgende Screenshot zeigt die 5 mitgelieferten Gaskurven in der Motorkurven-Datenbank, plus einer zusätzlichen Kurve („Vollgas 3“) die für ein Fahren mit einem der Tankmodi der 132er CU optimiert wurde: Wenn ein leerer Tank festgestellt wird, dann drosseln die Fahrzeuge auf etwa die Hälfte ihrer Leistung – schnell genug um nicht sofort einen Unfall beim Drosseln zu verursachen und während dem leeren Zustand eventuelle Weichen gut überfahren zu können, aber auch langsam genug, um dem Fahrer herrliche Frustmomente zu geben, bis er/sie endlich in der Boxengasse angekommen ist. Diese Kurve beginnt auch schon bei einem Gaswert von 56, da langsamere Werte darunter auf der entsprechenden Strecke „Bitzenheimer Berg“ nicht wirklich fahrbar sind.

![Die fünf mitgelieferten Gaskurven und die zusätzliche Kurve „Vollgas 3“](images/godigital132_bild1.png)


<!-- Hinweis: Das Originalbild muss im Repository unter docs/images/godigital132_bild1.png abgelegt werden. -->
