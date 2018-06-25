#Objekty
Popis jednotlivých objektů použitých při komunikaci s platební bránou

##internationalBankAccount 
Mezinárodní forma bankovního účtu

```json
 {
   "iban":"CZ6508000000192000145399",
   "bic":"KOMBCZPP"
 }
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
iban|Kód IBAN bankovního účtu Klienta|string
bic|SWIFT kód banky Klienta|string

##subjectData
Objekt obsahující dostupná data o Klientovi

```json
 {
    "firstName": "Pavel",
    "lastName": "Novák",
    "dateOfBirth": "1990-06-12",
    "birthNumber": "900612/0001",
    "sex": "MALE",
    "country": "CZE"
 }
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
firstName|Křestní jméno|string
lastName|Příjmení|string
dateOfBirth|Datum narození|string, yyyy-mm-dd
birthNumber|Rodné číslo|string
[sex](#sex)|Pohlaví|string
country|Kód země|string

##identificationData
Veškeré informace získané procesem identifikace

```json
 {
    "test": "test"
 }
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
[persons](#persons)|Údaje identifikované osoby|objekt
[bankAccounts](#bankAccounts)|Identifikace bankovním účtem|objekt
[addresses](#addresses)|Ověření trvalé adresy|objekt
[additionalDocuments](additionalDocuments)||objekt

##persons
Údaje identifikované osoby

```json
 {
    "test": "test"
 }
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
firstName|Křestní jméno|string
lastName|Příjmení|string
dateOfBirth|Datum narození|string, yyyy-mm-dd
birthNumber|Rodné číslo|string
[sex](#sex)|Pohlaví|string
country|Kód země|string
faceMatch|Údaje získané rozpoznáním obličeje|objekt
identDocuments|Údaje hlavního identifikačního dokladu|objekt
[bankAccounts](#bankAccounts)|Identifikace bankovním účtem|objekt
[addresses](#addresses)|Ověření trvalé adresy|objekt
[additionalDocuments](additionalDocuments)|| 

##faceMatch
Údaje získané rozpoznáním obličeje

```json
 {
    "test": "test"
 }
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
verified|Udává, zda byla identidikace úspěšná|boolean
[source](#source)|Zdroj poskytnutí obrazu|string
relDocumentNumber|Číslo porovnávaného dokladu|string
ip|IP adresa|string
dateReceived|Datum získání obrazu obličeje|string, yyyy-mm-dd

##identDocuments
Údaje hlavního identifikačního dokladu

```json
 {
    "test": "test"
 }
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
documentNumber|Identifikační číslo dokladu|string
[state](#stav-dokladu)|Stav dokladu|string
[source](#source)|Zdroj poskytnutí obrazu|string
[documentType](#documentType)|Typ nahraného dokladu|string
expiryDate|Datum platnosti dokladu|string, yyyy-mm-dd
nationalCountry|Kód země|string
ip|IP adresa|string
dateReceived|Datum získání dokladu|string, yyyy-mm-dd

##bankAccounts
Identifikace bankovním účtem

```json
 {
    "test": "test"
 }
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
[state](#stav-overeni-bankovniho-uctu)|Stav ověření bankovního účtu|string
country|Kód země|string
prefix|Předčíslí bankovního účtu Klienta|string
accountNumber|Číslo bankovního účtu Klienta|string
bankCode|Kód banky Klienta|string
iban|Kód IBAN bankovního účtu Klienta|string
bic|SWIFT kód banky Klienta|string
ip|IP adresa|string
dateReceived|Datum ověření bankovního účtu|string, yyyy-mm-dd

##addresses
Ověření trvalé adresy

```json
 {
    "test": "test"
 }
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------



##additionalDocuments

```json
 {
    "test": "test"
 }
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------