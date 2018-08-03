#Code lists

##state
Identification status of client's profile

Parameter’s value|Description
-----------------|-------------
PENDING| Identification process in progress
IDENTIFIED| Identification completed
PARTIALLY_IDENTIFIED| Identification partially completed
NOT_IDENTIFIED| Identification was not performed

##reasons
List of reasons why the process has failed or not finished yet

Parameter’s value|Description
-----------------|----------
EXPIRED_IDENTIFICATION| Expired identification
EXPIRED_IDENT_DOCUMENT| Expired identification's document
WAITING_IDENT_DOCUMENT| Waiting for identification's document
WAITING_ADDITIONAL_DOCUMENT| Waiting for additional document
WAITING_ADDRESS| Waiting for address verification
WAITING_BANK_ACCOUNT| Waiting for bank account verification
DENIED_FRAUD| Denied - false document
DENIED_FACEMATCH|Denied - disagreement of facematch process
DENIED_BAD_QUALITY_DOCUMENT|Denied - bad quality of document

##subjectType
Legal type of identification subject

Parameter’s value|Description
-----------------|----------
PERSON| Person
COMPANY| Company

##sex
Sex

Parameter’s value|Description
-----------------|----------
MALE| Male
FEMALE| Female

##source
Specifies the way of how the face image was provided

Parameter’s value|Description
-----------------|----------
UPLOAD| File's upload
WEBCAM| Webcam
MOBILE| Mobile phone

##Document state
State of uploaded document

Parameter’s value|Description
-----------------|----------
VERIFIED| Valid
EXPIRED| Expired

##documentType
Type of uploaded document

Parameter’s value|Description
-----------------|----------
ID_CARD| ID card
DRIVING_LICENSE| Driving license
PASSPORT| Passport
VISA| Visa
UNSUPPORTED| Unsupported document
UTILITY_BILL| Utility bill
BANK_STATEMENT| Bank statement

##Verification status of bank account
Verification status of bank account

Parameter’s value|Description
-----------------|----------
VERIFIED| Verified

##Verification status of address
Verification status of address

Parameter’s value|Description
-----------------|----------
VERIFIED| Verified