# Datenschutzerklärung für Flit

Inkrafttreten: 6. November 2026
Zuletzt aktualisiert: 6. November 2026

Flit (im Folgenden „die App“) ist eine Notiz-App, die ausschließlich lokal auf Ihrem Gerät arbeitet. Sie notieren einen Gedanken, sobald er Ihnen einfällt, und ergänzen ihn später um weitere Notizen, sodass aus jedem Eintrag nach und nach eine zeitlich geordnete Aufzeichnung entsteht. Diese Erklärung beschreibt, welche Informationen die App tatsächlich verarbeitet und wie sie gespeichert werden. Bitte lesen Sie sie, bevor Sie die App verwenden.

## 1. Welche Informationen die App speichert

Alles, was Sie in die App eingeben oder über die Sprachaufnahme diktieren, wird auf Ihrem Gerät gespeichert, insbesondere:

- Titel und Text jedes Eintrags (der Text wird auch zur Erstellung der Listenzusammenfassung verwendet);
- die von Ihnen hinzugefügten Ergänzungen samt Zeitstempel;
- das Status-Kennzeichen eines Eintrags und die Anheftung („Pin“);
- Erstellungs- und Änderungszeitpunkte von Einträgen und Ergänzungen.

Die App hält außerdem eine lokale Sicherungskopie des vorherigen Datenstands bereit, um bei einer Beschädigung der Hauptdatei wiederherstellen zu können (siehe Abschnitt 2).

Die App erhebt keine Gerätemodell-, Betriebssystemversions-, Gerätekennungs- (IDFV oder IDFA), Standort-, Kontakt-, Foto-, Kamera-, Gesundheits- oder Zahlungsdaten. Die Sprachaufnahme erzeugt keine Audiodatei und behält keine Aufnahme; gespeichert wird nur der erkannte Text als Inhalt des Eintrags. Sie protokolliert auch nicht Ihr Nutzungsverhalten oder Ihre Navigationswege.

## 2. Wo Ihre Informationen gespeichert werden

Die Einträge liegen als JSON-Datei in der Sandbox der App (Application Support/Flit), daneben eine `.bak`-Sicherungskopie. Beim Speichern schreibt die App zunächst eine temporäre Datei und ersetzt dann die Hauptdatei atomar, um das Risiko einer Beschädigung bei unterbrochenem Schreiben zu verringern; kann die Hauptdatei nicht gelesen werden, versucht die App die Wiederherstellung aus der Sicherung.

Die App verfügt über keinen Server. Sie lädt diese Inhalte nicht hoch, überträgt sie nicht und synchronisiert sie nicht mit Cloud-Diensten oder Dritten. Wir können Ihre Einträge weder einsehen noch auslesen oder wiederherstellen.

## 3. Netzwerkzugriff, Export und Teilen

Die Kernfunktionen der App arbeiten vollständig offline, und Ihre gespeicherten Einträge werden nie über das Netzwerk übertragen. Um festzustellen, ob das Netzwerk verfügbar ist (etwa um offline einen Hinweis anzuzeigen und die Liste nach Wiederherstellung der Verbindung zu aktualisieren), führt die App Folgendes aus:

- Über Apples Network-Framework liest sie den aktuellen Verbindungstyp (WLAN oder Mobilfunk) sowie aus, ob die Verbindung volumenabhängig abgerechnet wird oder sich im Low-Data-Modus befindet. Diese Informationen werden nur auf Ihrem Gerät verwendet und nicht hochgeladen.
- Sie sendet eine HTTPS-GET-Anfrage an die von Apple betriebene Adresse `https://captive.apple.com/hotspot-detect.html` und wertet Erfolg oder Fehlschlag als Erreichbarkeitssignal. Die Anfrage verwendet eine temporäre (ephemerale) Sitzung, enthält keine Cookies, schreibt keinen Cache und enthält weder Ihre Einträge noch Texte, die Sie in der App eingegeben haben. Wie bei jeder HTTPS-Anfrage kann Apple als Betreiber dieser Adresse die Quell-IP-Adresse und die für den Verbindungsaufbau erforderlichen üblichen Netzwerkinformationen sehen; wir erhalten und speichern diese Informationen nicht.

Außer dieser Verbindungsprüfung sendet die App von sich aus keine Daten nach außen.

Die aktuelle Version bietet keine Funktion zum Exportieren oder Teilen von Einträgen und übergibt Inhalte auch nicht über das iOS-Systemfreigabemenü an andere Apps. Sollte eine künftige Version eine solche Funktion einführen, erläutern wir sie vor der Nutzung und aktualisieren diese Erklärung.

Ob eine iOS-Gerätesicherung (iCloud- oder Computersicherung) die Eintragsdateien in der Sandbox der App enthält, hängt von Ihren System-Sicherungseinstellungen ab. Diese Sicherung wird von einer Systemfunktion von Apple ausgeführt und steht in keinem Zusammenhang mit der App.

## 4. Systemberechtigungen und Gerätezugriff

Die Sprachaufnahme ist die einzige Funktion, die eine Berechtigung benötigt. Wenn Sie die Schaltfläche für die Sprachaufnahme zum ersten Mal antippen, fragt iOS, ob die App das Mikrofon verwenden darf; je nach verwendeter System-API kann iOS dabei auch eine Abfrage zur Spracherkennung anzeigen. Die App fordert keine Berechtigungen für Mitteilungen, Fotomediathek, Kamera, Standort, Kontakte oder Gesundheitsdaten an und greift auch nicht darauf zu.

### Mikrofon und Sprachaufnahme

- Zweck: Die App wandelt das Gesprochene in den Text eines Eintrags um, den Sie vor dem Speichern bearbeiten können. Der erkannte Text wird ausschließlich in die lokale Datendatei der App (cards.json) geschrieben; darüber hinaus entsteht nichts.
- Zeitpunkt der Abfrage: nur beim ersten Verwenden der Sprachaufnahme. Die App schaltet das Mikrofon weder beim Start noch im Hintergrund ein, und die Aufnahme endet, sobald Sie das Diktieren beenden, den Editor verlassen oder die App schließen.
- Keine Speicherung und keine Übertragung der Aufnahme: Die App erzeugt keine Audiodatei und behält keine Aufnahme. Die Sprachaufnahme nutzt die Spracherkennung direkt auf dem Gerät. Die Aufnahme wird daher ausschließlich auf Ihrem Gerät verarbeitet und weder an Server von Apple noch an uns übermittelt; auch der erkannte Text bleibt in der lokalen Datendatei auf Ihrem Gerät. Wenn Ihr Gerät oder Ihre Sprache die Erkennung auf dem Gerät nicht unterstützt, weist die App darauf hin, dass die Sprachaufnahme nicht verfügbar ist, oder weicht auf die Tastatureingabe aus. Auf einen Cloud-Dienst wird nie umgeschaltet.
- Wenn Sie die Berechtigung ablehnen: Alle anderen Funktionen bleiben verfügbar, und Sie können Einträge wie gewohnt über die Tastatur hinzufügen und bearbeiten. Sie können die Berechtigung später in den iOS-Einstellungen erteilen oder jederzeit widerrufen; die Sprachaufnahme ist danach nicht mehr verfügbar.

In den iOS-Einstellungen kann für die App ein Schalter für „Mobile Daten“ erscheinen; dies ist eine systemweite Steuerung für Apps mit Netzwerkzugriff und keine von der App ausgelöste Berechtigungsanfrage. Wenn Sie ihn deaktivieren, funktioniert die App weiterhin, die Prüfung des Netzwerkstatus funktioniert jedoch möglicherweise nicht mehr.

Sollte eine künftige Version eine Funktion einführen, die eine weitere Berechtigung erfordert, zeigen wir vor der ersten Nutzung die standardmäßige iOS-Abfrage an, erläutern deren Zweck und aktualisieren diese Erklärung auf dieser Seite. Erteilte Berechtigungen können Sie jederzeit in den iOS-Einstellungen widerrufen; die betroffene Funktion steht danach gegebenenfalls nicht mehr zur Verfügung.

## 5. Aufbewahrung und Löschung

- Einträge verbleiben auf Ihrem Gerät, bis Sie sie selbst löschen.
- Sie können in der App einen gesamten Eintrag löschen oder einzelne Ergänzungen innerhalb eines Eintrags entfernen.
- Wird die App unter iOS gelöscht, werden auch die Hauptdatei und die Sicherungsdatei in der App-Sandbox gelöscht.
- Löschungen lassen sich nicht rückgängig machen. Da die Daten ausschließlich auf Ihrem Gerät liegen und die App keine Exportfunktion bietet, können wir sie nicht für Sie wiederherstellen; löschen Sie daher bitte mit Bedacht.

## 6. SDKs, Analyse und Werbung durch Dritte

Die App enthält keinerlei SDKs von Dritten – weder für Analyse noch für Werbung, Attribution oder Absturzberichte. Sie zeigt keine Werbung, verfolgt Sie nicht über Apps oder Websites hinweg, verwendet keine IDFA und fordert keine Berechtigung nach App Tracking Transparency an. Ob systemweite Diagnose- und Absturzdaten an Apple übermittelt werden, hängt von Ihrer Einstellung unter iOS > Einstellungen > Datenschutz & Sicherheit > Analyse & Verbesserungen ab und hat mit der App nichts zu tun.

## 7. Datenschutz für Kinder

Die App ist nicht für Kinder konzipiert und erhebt von niemandem personenbezogene Daten. Da alle Einträge ausschließlich lokal gespeichert werden, erhalten, speichern oder teilen wir keine Inhalte, die ein Kind eingibt. Wenn Sie als Erziehungsberechtigte Person Bedenken haben, kontaktieren Sie uns bitte über die untenstehenden Angaben.

## 8. Änderungen dieser Erklärung

Bei Änderungen aktualisieren wir das Datum „Zuletzt aktualisiert“ am Anfang dieser Seite. Betrifft eine Änderung die Art und Weise, wie Ihre Informationen behandelt werden, weisen wir in der App oder in den Versionsinformationen im App Store darauf hin. Wenn Sie die App nach dem Inkrafttreten einer Änderung weiter nutzen, gilt die aktualisierte Erklärung als angenommen.

## 9. Kontakt

Bei Fragen zu dieser Erklärung oder zur Ausübung von Rechten bezüglich Ihrer Daten erreichen Sie uns unter:

- Entwickler: <开发者主体名称 / Developer Name>
- Kontakt-E-Mail: yufei.cjn@outlook.com
- Postanschrift: <通信地址 / Mailing Address> (diese Zeile streichen, falls in Ihrer Jurisdiktion nicht erforderlich)
