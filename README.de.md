[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · **Deutsch** · [日本語](README.ja.md) · [中文](README.zh.md) · [हिन्दी](README.hi.md)

# U-MA Hanon

Alle 60 Übungen aus *Der Klaviervirtuose* von Charles-Louis Hanon im Browser: Du siehst sie im Notensystem, siehst **beide Hände auf der Tastatur** mit nummerierten Fingern, hörst sie im gewählten Tempo, und mit einem MIDI-Keyboard hört die App dir zu und analysiert dein Spiel.

**▶ App öffnen:** https://buenosairesfront.github.io/hanon/

Nichts zu installieren. Die Oberfläche ist auf Spanisch.

## So funktioniert's

1. **Übung wählen.** Die 60 Übungen sind nach den drei Teilen des Buchs gruppiert: **I · 1–20** vorbereitend (Magenta), **II · 21–43** fortgeschritten (Cyan) und **III · 44–60** Virtuosität (Gelb). Tippe auf eine Nummer unter der Tastatur oder auf die große Nummer oben, um das komplette Raster 1–60 zu öffnen.
2. **Variante wählen**, wenn es eine gibt: Tonleitern (39) und Arpeggien (41) in allen 24 Tonarten in der Reihenfolge des Buchs (jedes Dur gefolgt von seiner Moll-Parallele; Moll harmonisch und melodisch), chromatische Tonleitern (40) in 8 Intervallen und Richtungen, Tonwiederholungen (45) mit 6 Fingersätzen, gestoßene Terzen oder Sexten (48)…
3. **Noten lesen.** Zwei Systeme zeigen die Übung: **↑ aufwärts** (Cyan) und **↓ abwärts** (Magenta). Auf dem Handy wechselt man per Tabs.
4. **Hände beobachten.** Die Tastatur ist das Herz der App. Beide Hände sind mit Handflächen über den Tasten gezeichnet, jeder Finger trägt seine Nummer (1 = Daumen … 5 = kleiner Finger, jeder in eigener Farbe), und ein gestrichelter Umriss zeigt **die nächste Handposition**. Unter der Tastatur zeigt eine Zeile pro Hand die Fingerfolge der aktuellen Gruppe und leuchtet beim klingenden Ton auf.
5. **Abspielen.**
   - **▶ 2 Durchgänge**: kurze Demo mit den ersten und letzten zwei Gruppen, um die Form schnell zu hören.
   - **↑ aufwärts** / **↓ abwärts**: nur eine Richtung.
   - **↑↓×2**: die ganze Übung, zweimal.
   - **loop** wiederholt bis **stop**.
6. **Tempo einstellen** von 40 bis 160 BPM mit Regler oder – / +. Das gelbe Band markiert Hanons Bereich (60 → 108): langsam anfangen und steigern. Das Metronom **MET** blinkt und klickt im Takt der Übung (2/4, 3/4, 4/4 oder 6/8), Betonung in Magenta.

## Üben mit MIDI-Keyboard

**MIDI** drücken und Zugriff erlauben. Danach:

- gespielte Tasten leuchten auf der Bildschirmtastatur in Cyan;
- **REC** spielt die Übung als Leitstimme und nimmt auf, was du dazu spielst;
- am Ende kommt die **Analyse deiner Aufnahme**: Genauigkeit (%), mittlere Abweichung (ms), Gleichmäßigkeit (%) und Fehler; ein Timing-Diagramm (zu früh ↓ / zu spät ↑ pro Ton), Verzögerung und Kraft pro Finger und die Dynamik jeder Hand (rechts oben, links unten).

Ohne MIDI zeigt **neue Beispielaufnahme**, wie die Analyse aussieht.

## Hell und dunkel

Der Knopf **hell / dunkel** wechselt das Design; die Wahl bleibt in diesem Browser gespeichert.

## Unter der Haube

Eine einzige `index.html` ohne Abhängigkeiten: Die Übungen sind nicht Note für Note gespeichert, sondern werden **erzeugt**. Jede ist eine Melodiezelle (in Tonleiterstufen) plus Fingersatz für jede Hand; die Engine verschiebt sie pro Takt eine Stufe nach oben und wieder zurück und notiert jede Note mit dem richtigen Vorzeichen (Kreuze aufwärts, Bs abwärts bei den chromatischen). Tonleitern, Arpeggien und Oktavübungen werden für alle 24 Tonarten mit den traditionellen Fingersätzen gebaut. Die Noten werden in SVG gezeichnet, Tastatur und Analyse auf `<canvas>`, Klang und Metronom mit Web Audio, die Keyboard-Eingabe mit Web MIDI.

## Lokal starten

`index.html` herunterladen und öffnen oder den Ordner ausliefern:

```
python3 -m http.server 8000
```

<!-- u-ma:more -->
**Mehr von U-MA:** alle Instrumente und Werkzeuge an einem Ort → [U-MA-Übersicht](https://github.com/buenosairesfront/U-ma/blob/main/README.de.md)
<!-- /u-ma:more -->

## Credits

Übungen aus *Le Pianiste virtuose en 60 exercices* von Charles-Louis Hanon (1873, gemeinfrei). App von U-MA サウンド · [Buenos Aires Front](https://www.instagram.com/buenos.aires.front/).
