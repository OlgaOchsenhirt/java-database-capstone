Diese Spring Boot-Anwendung kombiniert MVC mit REST-Architektur. 
Für Admin- und Doktor-Dashboards werden Thymeleaf-Templates eingesetzt, 
während REST-APIs die übrigen Module bedienen. 
Alle Anfragen laufen über eine Service-Schicht, die die Geschäftslogik kapselt und an die Repositories weitergibt. 
Die Datenhaltung erfolgt in zwei Datenbanken: MySQL für strukturierte Daten (Patienten, Ärzte, Termine, Administration) 
mithilfe von JPA-Entitäten sowie MongoDB für flexible, unstrukturierte Daten wie Rezepte in Form von Dokumentmodellen.


1. Ein Benutzer greift über das AdminDashboard, DoctorDashboard, PatientDashboard oder die-Seite auf die Anwendung zu.

2. Die jeweilige Anfrage wird an den zuständigen Thymeleaf-Controller (für Dashboards) oder REST-Controller (für JSON-basierte APIs) weitergeleitet.

3. Der Controller ruft die Service-Schicht auf, welche die Geschäftslogik kapselt und die Anfrage verarbeitet.

4. Die Service-Schicht verwendet entweder ein MySQL Repository oder ein MongoDB Repository, um auf die passenden Datenquellen zuzugreifen.

5. Über das MySQL Repository wird die MySQL-Datenbank angesprochen, in der strukturierte Daten (z. B. Patienten, Ärzte, Termine, Admins) gespeichert sind.

6. Diese strukturierten Daten werden als JPA-Entitäten in den MySQL Models abgebildet und stehen so der Anwendung zur Verfügung.

7. Für unstrukturierte Daten wie Rezepte wird das MongoDB Repository verwendet, das auf die MongoDB-Datenbank zugreift und Dokumentmodelle verarbeitet. 
