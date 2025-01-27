Erklärung des Programms:
Das Programm ist ein einfaches Bankkonto-Verwaltungssystem, das in C# geschrieben wurde. Es ermöglicht es, verschiedene Konten zu erstellen, Geld auf Konten einzuzahlen, abzuheben, und die Kontotransaktionen zu verfolgen. Hier sind die Hauptbestandteile und Funktionen des Codes:

1. Klassenübersicht:
Konto:
Die Basisklasse, die ein allgemeines Konto darstellt.

Attribute:

Kontostand: Speichert den aktuellen Kontostand (decimal).
Kontonummer: Eine eindeutige 3-stellige Nummer, um das Konto zu identifizieren.
transaktionen: Eine Liste, die alle Transaktionen (Einzahlungen, Abhebungen) speichert.
Methoden:

Einzahlen(decimal betrag): Fügt Geld zum Kontostand hinzu und speichert die Transaktion.
Abheben(decimal betrag): Zieht Geld vom Kontostand ab, wenn ausreichend Guthaben vorhanden ist.
TransaktionshistorieAnzeigen(): Zeigt alle Transaktionen des Kontos an.
Jugendkonto (erbt von Konto):
Ein spezielles Konto mit einem Abhebungslimit pro Transaktion.

Zusätzliche Attribute:
Limit: Maximale Abhebesumme pro Transaktion.
Überschreibt die Methode Abheben(decimal betrag), um sicherzustellen, dass das Limit eingehalten wird.
2. Programmlogik (Program):
Das Hauptprogramm verwaltet alle Konten in einer Liste (kontenListe) und bietet ein Menü, um verschiedene Aktionen durchzuführen.

Hauptmenü:
Das Menü bietet die folgenden Optionen:

Neues Konto anlegen:
Entweder ein normales Konto oder ein Jugendkonto.
Der Benutzer muss eine 3-stellige Kontonummer eingeben.
Es wird geprüft, ob die Kontonummer bereits verwendet wird.
Auf Konto einzahlen:
Der Benutzer gibt die Kontonummer und den Betrag ein.
Wenn die Kontonummer gültig ist, wird der Betrag eingezahlt.
Vom Konto abheben:
Der Benutzer gibt die Kontonummer und den Abhebungsbetrag ein.
Es wird geprüft, ob genügend Guthaben vorhanden ist und (bei Jugendkonten) ob das Limit eingehalten wird.
Alle Konten anzeigen:
Zeigt die Kontonummer und den aktuellen Kontostand aller Konten.
Transaktionshistorie anzeigen:
Zeigt alle Transaktionen eines bestimmten Kontos an.
Alles in Datei speichern:
Speichert alle Konten in einer Datei, sodass die Daten später geladen werden können.
Alles aus Datei laden:
Lädt Kontodaten aus einer Datei und fügt sie der kontenListe hinzu.
Konto löschen:
Löscht ein Konto anhand der Kontonummer.
Monatlichen Bericht anzeigen:
Zeigt die Anzahl der Transaktionen und den Kontostand jedes Kontos.
Beenden:
Schließt das Programm.
Fehlerbehandlung:
Bei ungültigen Eingaben (z. B. falsche Kontonummer, Buchstaben statt Zahlen) wird eine Fehlermeldung angezeigt, und der Benutzer muss die Eingabe wiederholen.
Jede Kontonummer muss eindeutig sein; doppelte Kontonummern werden nicht akzeptiert.
Zusätzliche Funktionen:
Zurück-Taste (Backspace):
Ermöglicht es dem Benutzer, im Menü einen Schritt zurückzugehen.
Eingabeprüfung:
Jede Eingabe wird überprüft, um sicherzustellen, dass sie gültig ist. Ungültige Eingaben führen zu einer Fehlermeldung.
