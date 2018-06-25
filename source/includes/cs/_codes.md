#Číselníky

##Stav identifikace
Stav identifikace klientského profilu

Hodnota parametru|Popis
-----------------|-----
PENDING| Probíhající identifikace
IDENTIFIED| Identifikace provedena
PARTIALLY_IDENTIFIED| Identifikace částečně provedena
NOT_IDENTIFIED| Identifikace nebyla provedena

##reasons
Seznam důvodů, proč nebyla identifikace Klienta provedena, či proč stále probíhá

Hodnota parametru|Popis
-----------------|-----
EXPIRED_IDENTIFICATION|
EXPIRED_IDENT_DOCUMENT|
WAITING_IDENT_DOCUMENT|
WAITING_ADDITIONAL_DOCUMENT|
WAITING_ADDRESS|
WAITING_BANK_ACCOUNT|
DENIED_FRAUD|
DENIED_FACEMATCH|
DENIED_BAD_QUALITY_DOCUMENT|

##subjectType
Právní povaha identifikovaného subjektu

Hodnota parametru|Popis
-----------------|-----
PERSON|Fyzická osoba
COMPANY|Právnická osoba

##sex
Pohlaví

Hodnota parametru|Popis
-----------------|-----
MALE|Muž
FEMALE|Žena

##source
Zdroj poskytnutí obrazu

Hodnota parametru|Popis
-----------------|-----
UPLOAD| Nahrání souboru
WEBCAM| Webová kamera
MOBILE| Mobilní telefon

##Stav dokladu
Stav nahraného dokladu

Hodnota parametru|Popis
-----------------|-----
VERIFIED|Platný
EXPIRED|Neplatný

##documentType
Typ nahraného dokladu

Hodnota parametru|Popis
-----------------|-----
ID_CARD| Průkaz totožnosti
DRIVING_LICENSE| Řidičský průkaz
PASSPORT| Cestovní pas
VISA| Vízum
UNSUPPORTED| Nepodporovaný doklad
UTILITY_BILL| Účet za služby
BANK_STATEMENT| Výpis z bankovního účtu

##Stav ověření bankovního účtu
Stav ověření bankovního účtu

Hodnota parametru|Popis
-----------------|-----
VERIFIED|Oveřen
