# User Stories – Smart Clinic Management System
Dieses Dokument fasst alle definierten User Stories für Admins, Patienten und Ärzte zusammen.
Jede User Story enthält eine kurze Beschreibung, Akzeptanzkriterien, Priorität und Story Points.

# Admin User Stories

#1 Als Admin möchte ich mich mit meinem Benutzernamen und Passwort sicher im Portal anmelden, um die Plattform zu verwalten. 

Akzeptanzkriterien:

1. Der Admin muss einen gültigen Benutzernamen und ein Passwort eingeben.
2. Bei falschen Anmeldedaten wird eine Fehlermeldung angezeigt.
3. Nach erfolgreicher Anmeldung wird der Admin auf das Admin-Dashboard weitergeleitet.

Priorität: Hoch

Story Points: 3

#2 Als Admin möchte ich mich vom Portal abmelden, damit mein Systemzugang geschützt ist.

Akzeptanzkriterien:

1. Beim Klicken auf den Button „Logout“ wird die aktuelle Session des Admins beendet.
2. Nach der Abmeldung wird der Admin auf die Login-Seite weitergeleitet.
3. Nach der Abmeldung ist der Zugriff auf geschützte Seiten ohne erneutes Login nicht mehr möglich.
   
Priorität: Hoch

Story Points: 3

#3 Als Admin möchte ich Ärzte im Portal hinzufügen, damit neue Ärzte Termine verwalten und Patientendaten einsehen können.

Akzeptanzkriterien:

1. Im Admin-Dashboard gibt es einen Button „Arzt hinzufügen“.
2. Beim Klicken erscheint ein Formular mit Pflichtfeldern.
3. Nach dem Absenden wird der Arzt in der MySQL-Datenbank gespeichert.
4. Die Passwörter werden verschlüsselt gespeichert.
5. Nach erfolgreicher Speicherung erhält der Admin eine Bestätigungsmeldung.
6. Neue Ärzte können sich mit den gespeicherten Zugangsdaten einloggen.
   
Priorität: Hoch

Story Points: 5

#4 Als Admin möchte ich Ärzte aus dem System entfernen können, damit die Datenbank nur aktive Ärzte enthält.

Akzeptanzkriterien:

1. Im Admin-Dashboard gibt es eine Übersichtsliste aller Ärzte mit einem „Löschen“-Button neben jedem Eintrag.
2. Beim Klicken auf „Löschen“ erscheint ein Bestätigungsdialog.
3. Nach Bestätigung wird der Arzt dauerhaft aus der MySQL-Datenbank entfernt.
4. Nach erfolgreicher Löschung erhält der Admin eine Bestätigungsmeldung.
5. Der gelöschte Arzt kann sich nicht mehr ins System einloggen.
6. Falls der Arzt noch aktive Termine oder Patientenverknüpfungen hat, wird eine Fehlermeldung angezeigt.
   
Priorität: Hoch

Story Points: 5

#5 Als Admin möchte ich eine gespeicherte Prozedur in MySQL ausführen können, um die Anzahl der Termine pro Monat zu ermitteln und Nutzungsstatistiken zu verfolgen.

Akzeptanzkriterien:

1. Der Admin kann die gespeicherte Prozedur über die MySQL-Datenbank aufrufen.
2. Die Prozedur liefert eine Liste der Monate mit der Anzahl der Termine in jedem Monat.
3. Die Prozedur verwendet aktuelle Daten aus der Datenbank zum Zeitpunkt der Ausführung.
   
Priorität: Mittel

Story Points: 5


#  Patienten User Stories

#6 Als Patient möchte ich ohne Anmeldung eine Liste von Ärzten sehen, damit ich vor der Registrierung die verfügbaren Optionen erkunden kann.

Akzeptanzkriterien:

1. Auf der Startseite gibt es einen Button „Ärzte anzeigen“, der ohne Anmeldung verfügbar ist.
2. Nach Klick wird eine Ärzteliste angezeigt, die mindestens Name, Fachgebiet, verfügbare Termine und Kontaktdaten enthält.
3. Über einen „Zurück“-Button gelangt der Patient zurück auf die Startseite.

Priorität: Hoch

Story Points: 3


#7 Als Patient möchte ich mich mit meiner E-Mail und meinem Passwort anmelden, um Termine zu buchen.

Akzeptanzkriterien:

1. Der Patient gibt E-Mail und Passwort ein.
2. Bei korrekten Daten wird er auf sein Dashboard weitergeleitet.
3. Bei falschen Daten erscheint eine Meldung „Zugangsdaten inkorrekt“.
   
Priorität: Hoch

Story Points: 3



#8 Als Patient möchte ich mich im Portal einloggen, um meine Buchungen zu verwalten.

Akzeptanzkriterien:

1. Nach dem Login gibt es im Dashboard einen Bereich „Meine Buchungen“.
2. Dort werden alle aktiven Termine angezeigt.
3. Der Patient kann Details (Datum, Uhrzeit, Arzt) einsehen.
4. Der Patient kann Buchungen stornieren oder ändern.

Priorität: Mittel

Story Points: 5

#9 Als Patient möchte ich mich vom Portal abmelden, um mein Konto zu sichern.

Akzeptanzkriterien:

1. Es gibt einen sichtbaren Logout-Button im Dashboard.
2. Beim Klick wird die Session beendet.
3. Der Patient wird auf die Startseite weitergeleitet.
   
Priorität: Hoch

Story Points: 3


#10 Als Patient möchte ich mich einloggen und einen einstündigen Termin mit einem Arzt buchen, um eine Konsultation durchzuführen.

Akzeptanzkriterien:

1. Auf der Terminbuchungsseite kann der Patient einen Arzt auswählen.
2. Es werden nur freie Zeitfenster angezeigt.
3. Nach Auswahl wird der Termin für eine Stunde gebucht und in der Datenbank gespeichert.
4. Der Patient erhält eine Bestätigungsmeldung.
   
Priorität: Hoch

Story Points: 8


#11 Als Patient möchte ich meine bevorstehenden Termine einsehen, damit ich mich entsprechend vorbereiten kann.

Akzeptanzkriterien:

1. Im Patienten-Dashboard gibt es einen Bereich „Meine bevorstehenden Termine“.
2. Es werden alle zukünftigen Termine mit Datum, Uhrzeit und Arzt angezeigt.
3. Vergangene Termine werden nicht mehr angezeigt.
   
Priorität: Mittel

Story Points: 5


# Arzt User Stories

#12 Als Arzt möchte ich mich im Portal einloggen können, um meine Termine verwalten zu können.

Akzeptanzkriterien:

1. Der Arzt muss sich mit einer gültigen E-Mail-Adresse und Passwort anmelden können.
2. Nach erfolgreichem Login wird er auf das Arzt-Dashboard geleitet, wo er seine Termine verwalten kann.
3. Bei falschen Zugangsdaten erscheint eine Fehlermeldung: „E-Mail oder Passwort falsch.“

Priorität: Hoch

Story Points: 3


#13 Als Arzt möchte ich mich aus dem Portal ausloggen können, um meine Daten zu schützen.

Akzeptanzkriterien:

1. Beim Klicken auf den Button „Ausloggen“ wird die aktuelle Sitzung beendet.
2. Nach dem Logout wird der Arzt auf die Login-Seite weitergeleitet.
3. Ein erneuter Zugriff auf das Arzt-Dashboard ist nur nach erneutem Login möglich.
   
Priorität: Hoch

Story Points: 3


#14 Als Arzt möchte ich meinen Terminkalender einsehen können, um organisiert zu bleiben.

Akzeptanzkriterien:

1. Auf der Startseite gibt es einen Button „Terminkalender einsehen“.
2. Nach Klick wird der Arzt auf eine Kalenderseite weitergeleitet, die alle zukünftigen Termine mit Datum, Uhrzeit und Patientennamen anzeigt.
3. Vergangene Termine werden nicht mehr im aktiven Kalender angezeigt.
4. Termine sind übersichtlich und chronologisch geordnet.
   
Priorität: Hoch

Story Points: 5


#15 Als Arzt möchte ich meine Unverfügbarkeit markieren, um Patienten nur die verfügbaren Zeiten anzuzeigen.

Akzeptanzkriterien:

1. Im Terminkalender kann der Arzt Zeitfenster (z. B. bestimmte Tage oder Stunden) als „nicht verfügbar“ markieren.
2. Markierte Zeitfenster werden Patienten bei der Buchung nicht mehr als verfügbare Slots angezeigt.
3. Bereits gebuchte Termine sind automatisch blockiert und können nicht zusätzlich gebucht werden.
4. Änderungen an der Verfügbarkeit (z. B. Urlaub eintragen, Termin freigeben) werden sofort in der Patientenansicht aktualisiert.

Priorität: Hoch

Story Points: 5

#16 Als Arzt möchte ich mein Profil mit Fachrichtung und Kontaktdaten aktualisieren können, damit Patienten immer die aktuellsten Informationen sehen.

Akzeptanzkriterien:

1. Der Arzt kann über das Dashboard auf die Profilseite zugreifen.
2. Der Arzt kann dort seine Fachrichtung, Kontaktdaten und ggf. Praxiszeiten bearbeiten.
3. Änderungen werden nach dem Speichern sofort in der Datenbank persistiert.
4. Patienten sehen automatisch die aktualisierten Informationen in ihrer Ansicht.
5. Nach erfolgreicher Aktualisierung erhält der Arzt eine Bestätigungsmeldung.
   
Priorität: Hoch

Story Points: 5


#17 Als Arzt möchte ich die Patientendetails für bevorstehende Termine einsehen können, damit ich vorbereitet bin.

Akzeptanzkriterien:

1. Der Arzt kann im Terminkalender alle bevorstehenden Termine inklusive Patientennamen, Datum und Uhrzeit einsehen.
2. Durch einen Klick auf den jeweiligen Patientennamen öffnet sich eine Detailansicht mit Patientendaten (z. B. Geburtsdatum, Kontaktdaten, Krankheitsgeschichte, Diagnosen und Befunde).
3. Der Arzt hat außerdem die Möglichkeit, eine Liste aller seiner Patienten (Name, Geburtsdatum, Kontaktdaten) einzusehen.
4. Alle Patientendaten werden sicher aus der Datenbank geladen und sind nur für eingeloggte Ärzte zugänglich.
   
Priorität: Hoch

Story Points: 5



















