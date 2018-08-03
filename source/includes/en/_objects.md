#Objects
Description of each object used within the communication with the service. 


##internationalBankAccount 
International form of bank account

```json
 {
   "iban":"CZ6508000000192000145399",
   "bic":"KOMBCZPP"
 }
```

Parameter´s name|Parameter´s description| Data´s type
----------------|-----------------------|-------------
iban| IBAN |string
bic|SWIFT |string

##subjectData
Aggregates known information about the client

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

Parameter´s name|Parameter´s description| Data´s type
----------------|-----------------------|-------------
firstName|First name|string
lastName|Last name|string
dateOfBirth|Date of birth|string, yyyy-mm-dd
birthNumber|Birth number|string
[sex](#sex)|Sex|string
country|Country code|string

##identificationData
Contains all of the collected identification data


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

Parameter´s name|Parameter´s description| Data´s type
----------------|-----------------------|-------------
[persons](#persons)|Represents person who is being identified|object
[bankAccounts](#bankaccounts)|Represents bank account verification|object
[addresses](#addresses)|Represents address verification|object
[additionalDocuments](#additionaldocuments)| Additional documents|object

##persons
Represents person who is being identified


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

Parameter´s name|Parameter´s description| Data´s type
----------------|-----------------------|-------------
firstName|First name|string
lastName|Last name|string
dateOfBirth|Date of birth|string, yyyy-mm-dd
birthNumber|Birth number|string
[sex](#sex)|Sex|string
country|Country code|string
[faceMatch](#facematch)|Represents face verification of the person|object
[identDocuments](#identdocuments)|Represents main identification document|object
[bankAccounts](#bankaccounts)|Represents bank account verification|object
[addresses](#addresses)|Represents address verification|object
[additionalDocuments](#additionaldocuments)| Additional documents|object

##faceMatch
Represents face verification of the person

```json
 {
      "verified": true,
      "source": "UPLOAD",
      "relDocumentNumber": 123456,
      "ip": "77.75.77.39",
      "dateReceived": "2018-02-15 17:10:44.760"
  }
```

Parameter´s name|Parameter´s description| Data´s type
----------------|-----------------------|-------------
verified|Holds whether the face verification was successfull|boolean
[source](#source)|Specifies the way of how the face image was provided|string
relDocumentNumber|Relation to document number which was the face image compared to|string
ip|IP address|string
dateReceived|Date when the face image was acquired|string, yyyy-mm-dd HH:MM:SS:MS

##identDocuments
Represents main identification document

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

Parameter´s name|Parameter´s description| Data´s type
----------------|-----------------------|-------------
documentNumber|Official identifier of identification document|string
[state](#document-state)|State of document verification|string
[source](#source)|Specifies the way of how was the document provided|string
[documentType](#documenttype)|Type of uploaded document|string
expiryDate|Date of document's expiration|string, yyyy-mm-dd HH:MM:SS:MS
nationalCountry|Country code|string
ip|IP address|string
dateReceived|Date when the document was acquired|string, yyyy-mm-dd HH:MM:SS:MS

##bankAccounts
Represents bank account verification

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

Parameter´s name|Parameter´s description| Data´s type
----------------|-----------------------|-------------
[state](#verification-status-of-bank-account)|Verification status of bank account|string
country|Country code|string
prefix|Prefix of bank account number|string
accountNumber|Number of client's bank account|string
bankCode|Client's bank code|string
iban|Client's IBAN|string
bic|Client's SWIFT|string
ip|IP address|string
dateReceived|Date when the bank account was acquired|string, yyyy-mm-dd HH:MM:SS:MS

##addresses
Represents address verification

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

Parameter´s name|Parameter´s description| Data´s type
----------------|-----------------------|-------------
[state](#verification-status-of-address)|State of address verification|string
street|Street|string
streetNumber|Street number|string
postalCode|Postal code|string
city|City|string
country|Country code|string
ip|IP address|string
dateReceived|Date when the address was acquired|string, yyyy-mm-dd HH:MM:SS:MS


##additionalDocuments
Additional documents

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

Parameter´s name|Parameter´s description| Data´s type
----------------|-----------------------|-------------
[documentType](#documenttype)|Type of additional document|string
[source](#source)|Specifies the way of how was the document provided|string
ip|IP address|string
dateReceived|Date when the additional document was acquired|string, yyyy-mm-dd HH:MM:SS:MS