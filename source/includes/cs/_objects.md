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
    "persons": [
      {
        "firstName": "Pavel",
        "lastName": "Novák",
        "dateOfBirth": "1990-06-12",
        "birthNumber": "900612/0001",
        "sex": "MALE",
        "country": "CZE",
        "faceMatch": {
          "verified": true,
          "source": "UPLOAD",
          "relDocumentNumber": 123456,
          "ip": "77.75.77.39",
          "dateReceived": "2018-02-15 17:10:44.760"
        },
        "identDocuments": [
          {
            "documentNumber": 123456,
            "state": "VERIFIED",
            "source": "UPLOAD",
            "documentType": "ID_CARD",
            "expiryDate": "2018-02-15 17:10:44.760",
            "nationalCountry": "CZE",
            "ip": "77.75.77.39",
            "dateReceived": "2018-02-15 17:10:44.760"
          }
        ],
        "bankAccounts": [
          {
            "state": "VERIFIED",
            "country": "CZE",
            "prefix": {},
            "accountNumber": 2174251001,
            "bankCode": 192,
            "iban": "CZ6003000000002174251001",
            "bic": "CEKOCZPP",
            "ip": "77.75.77.39",
            "dateReceived": "2018-02-15 17:10:44.760"
          }
        ],
        "addresses": [
          {
            "state": "VERIFIED",
            "street": "Vinohradská",
            "streetNumber": 22,
            "postalCode": 11000,
            "city": "Praha",
            "country": "CZE",
            "ip": "77.75.77.39",
            "dateReceived": "2018-02-15 17:10:44.760"
          }
        ],
        "additionalDocuments": [
          {
            "documentType": "BANK_STATEMENT",
            "source": "UPLOAD",
            "ip": "77.75.77.39",
            "dateReceived": "2018-02-15 17:10:44.760"
          }
        ]
      }
    ],
    "bankAccounts": [
      {
        "state": "VERIFIED",
        "country": "CZE",
        "prefix": {},
        "accountNumber": 2174251001,
        "bankCode": 192,
        "iban": "CZ6003000000002174251001",
        "bic": "CEKOCZPP",
        "ip": "77.75.77.39",
        "dateReceived": "2018-02-15 17:10:44.760"
      }
    ],
    "addresses": [
      {
        "state": "VERIFIED",
        "street": "Vinohradská",
        "streetNumber": 22,
        "postalCode": 11000,
        "city": "Praha",
        "country": "CZE",
        "ip": "77.75.77.39",
        "dateReceived": "2018-02-15 17:10:44.760"
      }
    ],
    "additionalDocuments": [
      {
        "documentType": "BANK_STATEMENT",
        "source": "UPLOAD",
        "ip": "77.75.77.39",
        "dateReceived": "2018-02-15 17:10:44.760"
      }
    ]
  }
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
[persons](#persons)|Údaje identifikované osoby|objekt
[bankAccounts](#bankaccounts)|Identifikace bankovním účtem|objekt
[addresses](#addresses)|Ověření trvalé adresy|objekt
[additionalDocuments](#additionaldocuments)|Další doklady|objekt

##persons
Údaje identifikované osoby

```json
 [{
        "firstName": "Pavel",
        "lastName": "Novák",
        "dateOfBirth": "1990-06-12",
        "birthNumber": "900612/0001",
        "sex": "MALE",
        "country": "CZE",
        "faceMatch": {
          "verified": true,
          "source": "UPLOAD",
          "relDocumentNumber": 123456,
          "ip": "77.75.77.39",
          "dateReceived": "2018-02-15 17:10:44.760"
        },
        "identDocuments": [
          {
            "documentNumber": 123456,
            "state": "VERIFIED",
            "source": "UPLOAD",
            "documentType": "ID_CARD",
            "expiryDate": "2018-02-15 17:10:44.760",
            "nationalCountry": "CZE",
            "ip": "77.75.77.39",
            "dateReceived": "2018-02-15 17:10:44.760"
          }
        ],
        "bankAccounts": [
          {
            "state": "VERIFIED",
            "country": "CZE",
            "prefix": {},
            "accountNumber": 2174251001,
            "bankCode": 192,
            "iban": "CZ6003000000002174251001",
            "bic": "CEKOCZPP",
            "ip": "77.75.77.39",
            "dateReceived": "2018-02-15 17:10:44.760"
          }
        ],
        "addresses": [
          {
            "state": "VERIFIED",
            "street": "Vinohradská",
            "streetNumber": 22,
            "postalCode": 11000,
            "city": "Praha",
            "country": "CZE",
            "ip": "77.75.77.39",
            "dateReceived": "2018-02-15 17:10:44.760"
          }
        ],
        "additionalDocuments": [
          {
            "documentType": "BANK_STATEMENT",
            "source": "UPLOAD",
            "ip": "77.75.77.39",
            "dateReceived": "2018-02-15 17:10:44.760"
          }
        ]
  }]
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
[bankAccounts](#bankaccounts)|Identifikace bankovním účtem|objekt
[addresses](#addresses)|Ověření trvalé adresy|objekt
[additionalDocuments](#additionaldocuments)|Další doklady|objekt

##faceMatch
Údaje získané rozpoznáním obličeje

```json
 {
      "verified": true,
      "source": "UPLOAD",
      "relDocumentNumber": 123456,
      "ip": "77.75.77.39",
      "dateReceived": "2018-02-15 17:10:44.760"
  }
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
verified|Udává, zda byla identidikace úspěšná|boolean
[source](#source)|Zdroj poskytnutí obrazu|string
relDocumentNumber|Číslo porovnávaného dokladu|string
ip|IP adresa|string
dateReceived|Datum získání obrazu obličeje|string, yyyy-mm-dd HH:MM:SS:MS

##identDocuments
Údaje hlavního identifikačního dokladu

```json
 [
        {
          "documentNumber": 123456,
          "state": "VERIFIED",
          "source": "UPLOAD",
          "documentType": "ID_CARD",
          "expiryDate": "2018-02-15 17:10:44.760",
          "nationalCountry": "CZE",
          "ip": "77.75.77.39",
          "dateReceived": "2018-02-15 17:10:44.760"
        }
  ]
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
documentNumber|Identifikační číslo dokladu|string
[state](#stav-dokladu)|Stav dokladu|string
[source](#source)|Zdroj poskytnutí obrazu|string
[documentType](#documenttype)|Typ nahraného dokladu|string
expiryDate|Datum platnosti dokladu|string, yyyy-mm-dd HH:MM:SS:MS
nationalCountry|Kód země|string
ip|IP adresa|string
dateReceived|Datum získání dokladu|string, yyyy-mm-dd HH:MM:SS:MS

##bankAccounts
Identifikace bankovním účtem

```json
 [
        {
             "state": "VERIFIED",
             "country": "CZE",
             "prefix": {},
             "accountNumber": 2174251001,
             "bankCode": 192,
             "iban": "CZ6003000000002174251001",
             "bic": "CEKOCZPP",
             "ip": "77.75.77.39",
             "dateReceived": "2018-02-15 17:10:44.760"
        }
  ]
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
dateReceived|Datum ověření bankovního účtu|string, yyyy-mm-dd HH:MM:SS:MS

##addresses
Ověření trvalé adresy

```json
[
      {
        "state": "VERIFIED",
        "street": "Vinohradská",
        "streetNumber": 22,
        "postalCode": 11000,
        "city": "Praha",
        "country": "CZE",
        "ip": "77.75.77.39",
        "dateReceived": "2018-02-15 17:10:44.760"
      }
]
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
[state](#stav-overeni-adresy)|Stav ověření adresy|string
street|Ulice|string
streetNumber|Číslo popisné|string
postalCode|Poštovní směrovací číslo|string
city|Město|string
country|Kód země|string
ip|IP adresa|string
dateReceived|Datum ověření adresy Klienta|string, yyyy-mm-dd HH:MM:SS:MS


##additionalDocuments
Další doklady

```json
[
      {
        "documentType": "BANK_STATEMENT",
        "source": "UPLOAD",
        "ip": "77.75.77.39",
        "dateReceived": "2018-02-15 17:10:44.760"
      }
]
```

Název parametru|Popis parametru|Datový typ
---------------|---------------|----------
[documentType](#documenttype)|Typ nahraného dokladu|string
[source](#source)|Zdroj poskytnutí obrazu|string
ip|IP adresa|string
dateReceived|Datum ověření dokladu|string, yyyy-mm-dd HH:MM:SS:MS