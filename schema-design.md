## MySQL Database Design


### Tabelle: Patienten
- id: INT, Primary Key, Auto Increment
- Vorname: VARCHAR(30) NOT NULL
- Nachname: VARCHAR(30) NOT NULL
- Geburtsdatum: DATE
- E-Mail: VARCHAR(50)
- Telefonnummer: VARCHAR(50)

### Tabelle: Ärzte
- id: INT, Primary Key, Auto Increment
- Vorname: VARCHAR(30) NOT NULL
- Nachname: VARCHAR(30) NOT NULL
- Fachgebiet: VARCHAR(30)
- E-Mail: VARCHAR(50)
- Telefonnummer: VARCHAR(50)

### Tabelle: Termine
- id: INT, Primary Key, Auto Increment
- Arzt_id: INT, Foreign Key → Ärzte(id)
- Patient_id: INT, Foreign Key → Patienten(id)
- Termindatum: DATETIME, Not Null
- Status: INT (0 = geplant, 1 = abgeschlossen, 2 = abgesagt)

### Tabelle: Zahlungen
- id: INT, PRIMARY KEY, AUTO_INCREMENT 
- Termin_id: INT, Foreign Key  → Termine(id)        
- Patient_id: INT, Foreign Key  → Patienten(id) 
- Betrag: DECIMAL(5,2), NOT NULL
- Waehrung: CHAR(3) 
- Zahlungsmethode: VARCHAR(50)
- Status INT (0 = ausstehend, 1 = bezahlt, 2 = erstattet) 
- Zahlungsdatum: DATETIME

### Tabelle: Admin
- id: INT, Primary Key, Auto Increment
- Username: VARCHAR(30)
- Passwort: VARCHAR(30)
- Vorname: VARCHAR(30) NOT NULL
- Nachname: VARCHAR(30) NOT NULL
- E-Mail: VARCHAR(50)



## MongoDB Collection Design

### Collection: Feedback

json

{
  "_id": { "id": "6512b3a8e4b0f8a1c0d2b3b5" },
  "patient_id": 123,
  "termin_id": 512,
  "submitted_at": "2025-11-16T12:05:00Z",
  "anonymous": false,
  "rating": {
    "overall": 4,
    "friendliness": 5,
    "waiting_time": 3
  },
  "comments": "Schnelle Behandlung, freundliches Personal. Wartezeit war etwas lang.",
  "tags": ["warteschlange", "freundlich"],
  "metadata": {
    "source": "email",
    "language": "de"
  }
}

### Collection: Rezepte

json

{
  "_id": { "id": "6512a9f3e4b0f8a1c0d2b3a4" },
  "patient_id": 123,                   
  "arzt_id": 7,                       
  "termin_id": 512,                    
  "issued_at": "2025-11-16T09:30:00Z",
  "valid_until": "2026-05-16",
  "medications": 

    {
      "name": "Paracetamol",
      "dosage": "500 mg",
      "instructions": "Bei Bedarf, max 4×/Tag",
    }
    
  "prescriber_snapshot": {              
    "vorname": "Anna",
    "nachname": "Meier",
    "fachgebiet": "Allgemeinmedizin"
  },


  


  
