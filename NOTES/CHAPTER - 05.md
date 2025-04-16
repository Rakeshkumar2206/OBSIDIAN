**Protecting Security of Assets** 

**Sensitive Data** - Sensitive data is any information that isn't public or unclassified. It includes confidential, proprietary, protected or any other type of data that an organization needs to protect due to its value to the organization or to comply with existing laws and regulations  

**Personally Identifiable Information** - Personally Identifiable Information (PII) is any information that can identify an individual. NIST SP 800-122 provides a more formal definition 
	Any Information about an individual maintained by an agency, including
	-  Any Information that can be used to distinguish or trace an individual's identity such as name, social, security number, date and place of birth, mother's maiden name or biometric records and
	-  Any other information that is linked or linkable to an individual, such as medical, educational, financial and employment information. 

**Protected Health Information** - Protected Health Information is any health related information that can be related to a specific person. In the United States, the Health Insurance Portability and Accountability Act (HIPAA) mandates PHI protection. HIPAA provides a more formal definition of PHI:
	Health Information means any information, whether oral or recorded in any form or medium, that - 
	- Is created or received by a health care provides, public health authority, employer, life insurer school or university or health care clearing house 
	- Related to the past, present, or future physical or mental health or condition of any individual the provision of health care to an individual or the past, present or future payment for the provision of healt care to an induvial 

**DATA CLASSIFICATION**

| Damage Type | CLASS | Government | Non-Government |
| ---- | ---- | ---- | ---- |
| Exceptionally Grave Damage | Class 3 | Top Secret | Confidential |
| Serious Damage | Class 2 | Secret | Private |
| Damage | Class 1 | Confidential | Sensitive |
| No Damage | Class 0 | Unclassified | Public |

**DATA STATES**

- *Data at Rest* - Is any data stored on media such as system hard drives, SSD, External drive, storage area networks and backup tapes. Strong symmetric encryption protects data at rest. 

- *Data in Transit* - Is any data transmitted over a network. This includes data transmitted over an internal network using wired or wireless methods methods. This also includes data transmitted over public networks such as internet. A combination of symmetric and asymmetric encryption protects data in transit. 

- Data in Use - Is any data in memory or temporary storage buffers while an application is using it. Applications often decrypt encrypted data before placing it in memory. This allows the application to work on it, but its important to flush these buffers when the data is no loner needed. In some cases, it's possible for an application to work on encrypted data using homomorphic encryption. This limits the risk because memory doesn't hold unencrypted data. 

**DATA MAINTENANCE**
- Data Maintenance refers to ongoing efforts to organize and care for data throughout its lifecycle. In general, if an organization stores all sensitive data on once server, it is relatively easy to apply all the security controls in that server. In contrast, if sensitive data is stores throughout an organization on multiple servers and end-user computers and mixed with non sensitive data, it becomes much harder to protect it. 
- One network processes unclassified data only, Another network processes classified data. Techniques such as air gaps ensure the two networks never physically touch each other. An air gap is a physical security control and means that systems and cables from the classified network will never touch the unclassified network. Additionally the classified network cant access internet and the internet attackers cant access it. 

**DATA LOSS PREVENTION**
Data loss prevention systems attempt to detect and block data exfiltration attempts. These systems have the capability of scanning unencrypted data looking for keywords and data patterns.
	**Network Based DLP** - A network based DLP scans all outgoing data looking for specific data. Administrator place it on the edge of the network to scan all data leaving the organization. 
	**Endpoint Based DLP** - An endpoint based DLP can scan files stored on a system as well as files sent to  external devices, such as printers. 

**DATA REMANENCE** 
It is the data that remains on media after the data was supposedly erased

**Erasing** - Erasing media is simply performing a delete operation against file, a selection of files or the entire media. In most cases, the deletion or removal process removes only the directory or catalog link to the file. The actual data remains on the drive.

**Clearing** - Clearing or overwriting is a process of preparing media for reuse and ensuring that the cleared data cannot be recovered using traditional recovery tools 

**Purging** - Purging is a more intense form of clearing that prepares media for reuse in less secure environments. It provides a level of assurance that the original data is not recoverable using any known methods. A purging process will repeat the clearing process multiple times and may combine it with another method, such as degaussing to completely remove the data. Even though purging is intended to remove all data remnants.  

**Cryptographic Erasure** - If data is encrypted on a device, its possible to use cryptographic erasure or crypto shredding to destroy the data. They don't erase or shred the data. Instead they destroy the encryption key or both encryption and decryption key if two are use. 

**DIGITAL RIGHTS MANAGEMENT (DRM)**
	DRM License - A license grants access to a product and defines the terms of use. A DRM license is a small file that includes the terms of use along with a decryption key which provides access to the product
	**Persistent Online Authentication** - Persistent online authentication (also known as  always-on DRM) requires a system to be connected with the internet to use a product. The system periodically connects with an authentication server, and if the connection or authentication fails, DRM blocks the use of the product.
	**Continuous Audit Trail**- A continuous audit trail tracks all use of copyrighted product. When combined with persistence, it can detect abuse, such as concurrent use of a product simultaneously but in two geographically different locations 

**CASB**- Cloud Access Security Broker 

A cloud access security broker is a software placed logically between users and cloud based resources. It can be on premises or within the cloud. Anyone who access the cloud goes through the CASB software. It monitors all activity and enforces administrator-defined security policies.

CASB solutions can also be effective at detecting shadow IT. Shadow IT is the use of IT resources without the approval of, or even knowledge of the IT department. 

**Pseudonymization** 
Pseudonymization refers to the process of using pseudonym to represent other data. GDPR refers pseudonyms as artificial identifiers.

**Tokenization**
Tokenization is the use of a token, typically a random string of characters, to replace other data. 

**Anonymization**
Anonymization is the process of removing all relevant data so that it is theoretically impossible to identify the original subject or person. 

**DATA OWNERS**
Data Owner is the person who has ultimate responsibility for the data. The owner is typically the CEO, President or Department Head. Data owner identify the classification and ensure it is properly labelled. They also ensure that it has adequate security controls based on the classification and the Organizations Security Policy.

**ASSET OWNER**
The Asset owner is the person who owns the asset or system that processes sensitive data. NIST outlines the following responsibilities for the system owner-
- Develops a system security plan in coordination with information owners, the system and administrator and functional users 
- Maintains the system security plan and ensure that he system is deployed and operated according to the agreed-upon security requirements.
- Updates the system security plan whenever a significant change occurs

**BUSINESS OWNERS**
Business owners might own processes that use systems managed by other entities. 

*IT owner < Business Owner --> Biz Owner has to make the decision based on the inputs provided by the IT Team* 

**DATA PROCESSOR**
Data Processor is any system that used to process data. GDPR defines that data processor as a natural or legal person, public authority, agency or other body which processes personal data solely on behalf of the data controller.

**DATA CONTROLLER**
Data Controller is the person or entity that controls the processing of the data. The data controller decides what data to process, why this data should be processed and how it is processed. 

**DATA CUSTODIANS**
Data Owners often delegate day to day tasks to a data custodian. A custodian helps protect the integrity and security of data by ensuring that it is properly stored and protected. 

**Administrators**
Administrators are persons who are granted with full privileges.

**User** - A user is a person who access computing system to accomplish a work tasks 

**Subject** - A subject is an entity that access an object such as file or folders. Subjects can be user, programs, process, services, computers or anything else that access s a resource

