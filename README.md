# sandblasting_machine_SIEMENS
SPS project in Siemens TiaPortal
TIA Portal Version: v16

Requirement: Suitable for libraries

Task definition (auf Deutsch)

Grundlegende Aufgabenstellung:
Mit dem Hauptschalter S6 wird die Steuerspannung eingeschaltet. Der Hydraulikdruckwächter
S7 und der Not-Aus-Taster S8(Öffner) müssen geschlossen sein.
Mit den Tastschaltern S0, S1 und S2 kann eine Programmauswahl vorgenommen werden.
Die einzelnen Programme werden teilweise von Hand oder automatisch gesteuert.
Ein Programmwechsel kann nur unter bestimmten Bedingungen oder nach Betätigung des
Not-Aus-Tasters vorgenommen werden. Die ablaufenden Funktionen werden durch
verschiedene Meldeeinrichtungen angezeigt.
Die Anlage wird in allen Programmen bei Betätigung des Not-Aus-Tasters bzw. bei Ausfall der
Steuerspannung oder des Hydraulikdruckwächters abgeschaltet.

Funktionsbeschreibung 1:
Programmvorwahl: TÜR AUF
Bei der Inbetriebnahme der Anlage ist die Tür normalerweise geschlossen.
Die Anlage kann in diesem Fall nur mit dem Programm Tür Auf gestartet werden.
Ist die Tür geschlossen, kann mit dem Tastschalter S1 die Tür manuell im Tippbetrieb geöffnet
werden. Gleichzeitig schaltet sich der Abtransport ein.
Ist die Tür geöffnet (Leuchtband vollständig), schalten sich der Türantrieb und der Abtransport
aus, das Raupenband lässt sich mit S3 und S4 vor und zurück fahren.
Der Rückwärtslauf ist im Tippbetrieb und der Vorlauf läuft in Selbsthaltung. Das Band wird
über den Tastschalter S5 Halt angehalten.
Steht das Raupenband und die Tür ist vollständig geöffnet, so kann mit dem Tastschalter S0 die
Tür manuell geschlossen oder mit dem Tastschalter S2 der Automatikbetrieb gestartet werden.
(Funktionsbeschreibung 2-3)
Wird die Anlage über Not-Aus/Abfall der Steuerspannung/Hydraulikdruckwächters abgeschaltet,
müssen alle Programme in Grundstellung starten/Tür darf nur nach kompletter Öffnung wieder
geschlossen werden.

Funktionsbeschreibung 2:
Programmvorwahl: Grundposition und Tür Zu
Um das Programm “Tür Zu'' zu starten, muss der Beschicker in der Grundposition stehen.
Hierzu sind die folgenden Funktionen zu erfüllen:
Hauptschalter Steuerspannung (I0.6) ist geschlossen
Hydraulikdruckwächter (I0.7) meldet: Druck ist vorhanden
Rückmeldung Not-Aus (Q1.1) in Funktion
Die Tür ist offen (I1.1)
Das Raupenband steht (Q0.3/Q0.4)
Das Schleuderrad steht (Q0.2)
Die Zuteilung ist geschlossen und die Schwingförderrinne steht (Q1.2/Q0.1)
Der Strahlmitteltransport steht (Q0.5)
Steht die Strahlanlage in Grundposition, schließt sich bei Betätigung des Tastschalters S0 die
Tür. Während sich die Tür schließt, ist das Läutewerk eingeschaltet. Der Endschalter “Tür unten"
schaltet den Türantrieb ab.
Wird beim Zufahren der Tür die Anlage abgeschaltet, muss bei erneuter Inbetriebnahme
zunächst die Tür vollständig geöffnet werden, um die Grundposition zu erreichen.

Funktionsbeschreibung 3:
Programmvorwahl: AUTO-START/Schleuderrad
Um den Automatikbetrieb zu starten, muss der Beschicker in der Grundposition stehen.
Nachdem der Beschicker in der Grundposition steht, kann mit S2 der Automatikbetrieb gestartet
werden.
Die Tür schließt sich und wird über den Endschalter “Tür Unten" quittiert. Während die Tür
schließt, ertönt das Läutewerk (symbolisch).
Wenn die Tür unten ist, schalten sich der Strahlmitteltransport und das Raupenband (vor) ein.
Verzögert läuft das Schleuderrad an. Den Betrieb des Schleuderrades signalisiert das
Rundumlicht (Blinkfrequenz 2 Hz).
Nach 10 Sekunden (simulierte Stern-Dreieck-Umschaltung) wird die Strahlmittelzuteilung
geöffnet und die Schwingförderrinne in Betrieb gesetzt.
Die Strahlzeit wird auf 20 Sekunden festgesetzt.
Nach Ablauf der Strahlzeit wird der Bremsvorgang eingeleitet, das Schleuderrad angehalten
und eine weitere Standzeit für das Absetzen des Staubes läuft an.
Nach Ablauf der Bearbeitungszeit schaltet sich der Automatikbetrieb ab und über die Vorwahl
Tür Auf lässt sich die Strahlkammer mit S1 öffnen und entleeren.
Die Anlage wird bei Betätigung des Not-Aus-Tasters bzw. bei Ausfall der Steuerspannung oder
des Hydraulikdruckwächters abgeschaltet.
Bei erneuter Inbetriebnahme muß zunächst die Grundposition wieder erreicht werden.

Funktionsbeschreibung 4:
Programmvorwahl: Automatik - Raupenband Störung
Falls sich während des Strahlens das zu strahlende Gut im Raupenband verkeilt, kann der
Bediener das Raupenband über S5 anhalten und mit S3 im Tippbetrieb rückwärts laufen lassen,
bzw. mit S4 wieder einschalten. Diese Steuerung ist wiederholbar, bis die Strahlzeit abgelaufen
ist. Die Strahlzeit wird hiervon nicht beeinflusst, alle anderen Programmfunktionen bleiben
erhalten.

