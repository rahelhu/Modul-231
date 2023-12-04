# Tagesdokumentation 04.12.2023

# Passwörter
# Notwendigkeit von Passwörter - Was sind sichere Passwörter?
Warum Passwörter? (Grund für den Einsatz von Passwörter: Weshalb werden Passwörter eingesetzt?)
- Um persönliche Daten zu schützen
- Damit niemand Änderungen an deinem Konto vornehmen kann.

Was wird geschützt? (Was wird mit Passwörter geschützt? Welche Arten von Informationen werden mit Passwörter geschützt, welche sind frei verfügbar? )
- (persönliche) Daten

Was ist ein sicheres Passwort?
- Min. 8 Zeichen lang
- Mit Gross- und Kleinbuchstaben
- Mit Sonderzeichen

Passwort-Richtlinien:
- Strategie: 3 zufällige Wörter in einem Passwort
- Regelmässige Passwortänderung ist eher kontraproduktiv, da der Nutzer dazu neigt, eher schwächere Passwörter zu verwenden.
- Multifaktor-Authentifizierung ist wichtig
- Länge der Passwörter ist sehr wichtig

# Authentifizierung und Autorisierung
Authentifizierung: Zur Anmeldung an einem Computer oder Netzwerk müssen Sie Ihren Benutzernamen und Ihr Kennwort eingeben.

Autorisierung: Wird überprüft, welche Zugriffsrechte ein Benutzer im Netzwerk hat bzw. ob dieser die Erlaubnis hat, Software selbstständig zu installieren.


"Peter hat das Recht auf den Ordner Geschäftsprozesse zuzugreifen." 
- Autorisierung

"Martina sperrt ihren Bildschirm vor der Kaffeepause und muss ihr Passwort eingeben, wenn Sie zurückkommt." 
- Authentifizierung

"Standard User haben keinen Zugriff auf die Server-Management-Konsole."
- Autorisierung

"Standardmässig kann in Linux Dateisystemen für jede Datei oder Ordner ein Benutzer, eine Gruppe, sowie die Zugriffsberechtigungen Lesen, Schreiben und Ausführen definiert werden." 
- Autorisierung

RADIUS Server 
- Authentifizierung/ Autorisierung

"Nur Lehrerpersonen können in MS Teams einer Gruppe Lernende hinzufügen oder entfernen." 
- Autorisierung

"Permission denied." 
- Autorisierung

"Für das Online-Banking benötige ich mein Benutzername, mein Passwort und das Foto-TAN App."
- Authentifizierung


# MFA - Multi-Faktor-Authentisierung

MFA verwendet zwei oder mehr Authentifizierungsmethoden, wie Passwörter und mobile Codes.

2-Faktor-Authentifizierung erfordert zwei verschiedene Authentifizierungsmethoden, oft ein Passwort und einen einmaligen Code auf dem Smartphone, um auf ein Konto zuzugreifen. Bei 3-Faktor-Authentifizierung sind drei unterschiedliche Authentifizierungsfaktoren erforderlich.

# Backup
- Kein Backup - kein Mitleid
- Ein Backup ist die räumliche Trennung der Orginaldatenträger und der Backup Medien.

# Grundsätze für das Einrichten eines Backups
- Nicht verschieben, Backup als erstes machen
- Git-Repo nutzen (commiten und pushen)
- Firmwareupdate auf einer Firewall: Vorher ein Backup der Konfiguration machen.
- Immer und ausnahmslos Backups erstellen


Thema: Datensicherungsziele, Datenkompression
- Welche Medien/Datenträger/Geräte werden als Backup-Ziel verwenden?
    - externe Festplatten, Cloud
- Was für Kompressionsverfahren werden verwendet?
    - ZIP
- Weshalb ist Datenkompression insbesondere bei einem Image-Backup wichtig?
    - reduziert den Speicherbedarf
    - beschleunigt den Übertragungsprozess
    - optimiert Ressourcennutzung

Thema: Vollsicherung, Differenzielle Sicherung, Inkrementelle Sicherung
- Erklären Sie den Unterschied zwischen den drei Methoden (mithilfe einer Grafik)
    - Vollsicherung: alle Daten werden vollständig gesichert.
    - Differenzielle Sicherung: Nur die Änderungen seit der letzten Vollsicherung.
    - Inkrementelle Sicherung: Nur die Änderungen seit der letzten Sicherung, egal ob Vollsicherung oder inkrementell.
- Wird für die differenzielle und inkrementelle Sicherung ein Vollbackup benötigt?
    - Ja, für die differenzielle Sicherung benötigt man ein vorheriges Vollbackup, während die inkrementelle Sicherung auf dem letzten Backup basiert.
- Vor- und Nachteile der verschiedenen Arten.
    - Vollsicherung:
    Vorteil:  
    einfache Wiederherstellung
    Nachteil:
    hoher Speicherplatzbedarf
    - Differenzielle Sicherung
    Vorteil:
    schnelle Wiederherstellung
    Nachteil:
    wachsender Speicherplatzbedarf mit der Zeit
    - Inkrementelle Sicherung
    Vorteil:
    geringer Speicherplatzbedarf
    Nachteil:
    längere Wiederherstellungszeiten

Thema: Block-Level vs File-Level Backup
- Dateisystem-Ebene: Kopieren von einzelnen Dateien vs. Kopieren von Datenblöcken
- Erklären Sie die Begriffe und die Unterschiede.
    - Block-Level: Sichert nur die geänderten Datenblöcke auf der Festplatte, unabhängig von der Dateistruktur.
    - File-Level: Sichert ganze Dateien auf der anderen Dateisystemebene
- Welche Methode eignet sich besser, wenn ein Image von einer Festplatte erstellt werden soll und weshalb?
    - Block-Level (nur geänderte Datenblöcke werden berücksichtigt)
- Welche Methode eignet sich besser, wenn nur der Home-Folder gesichert werden muss?
    - File-Level (es arbeitet auf Dateiebene)

Thema: Hot Backup vs Cold Backup
- Erklären Sie die Begriffe mithilfe jeweils einen oder zwei praktischen Einsatzzwecken
    - Hot Backup: Sichert Daten, während das System in Betrieb ist. Beispiel: Webseite, die immer verfügbar sein muss.
    - Cold Backup: Sichert Daten, nachdem das System heruntergefahren wurde. Beispiel: wöchentliche Sicherung eines weniger kritischen Server ausserhalb der Geschäftszeiten

Thema: Datensicherungsstrategie
- Wie häufig soll man ein Backup machen?
    - täglich
- Auf wie vielen unterschiedlichen Datenträger soll man Backups machen?
    - 3-2-1 Regel: 2 verschiedene Medien.
- Begriffe zum Recherchieren: Turm von Hanoi, 3-2-1 Regel
    - Turm von Hanoi: 
    Eine Backup-Rotationsstrategie zur Optimierung der Speichernutzung über verschiedene Zeiträume hinweg.
    - 3-2-1 Regel: 
    3 Kopien der Daten auf 2 verschiedenen Medien, 1 außerhalb des Standorts.


# Szenario: Verlust des persönliches Smartphones.

| Service | Funktion | betroffene Daten | Backup | Wiederherstellung
|----------|----------|----------|----------|----------|
| Whatsapp    | Nachrichten/Fotos versenden   | Chats/Bilder   |  in der App | bei der Installation wird man gefragt, ob man die Daten wiederherstellen will
| SocialMedia (TikTok, Insta, Snapchat, ...)    | Videos/Fotos von anderen ansehen/selber hochladen, chatten   | Chats/hochgeladene Bilder/Personalisierung der Vorschläge   | in der Cloud der App | einloggen
| Dateien / OneDrive / Google Drive    | speichert die Dateien   | Text-Files, ...   | in der Cloud, auf dem Samsung-Account (bei Samsung-Geräten) | einloggen
| Google | recherchieren, Daten speichern, ... | Dateien, Fotos, Suchverlauf, ... | in der Cloud von Google | einloggen

      
