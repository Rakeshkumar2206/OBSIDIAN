
**Controlling and Monitoring Access**

**Permissions** - In General, Permissions refer to the access granted for an object and determine what you can do with it. 

**Rights** - A right primarily refer to the ability to take an action on an object

**Privileges** - Privileges are a combination of rights and permissions


**Discretionary Access Control** - A key characteristic of DAC is that even object has its owner and these owners can grant or deny access to any other subjects

**Role Based Access Control**- A key characteristic of the Role-Based Access Control (RBAC) model is the use of roles or groups.

**Rule Based Access Control** - A key characteristic of the Rule Based Access Control Model is that it applied global rules to all subjects. 

**SSO**- Single Sign On
**XML** - Extensible markup Language 
**SAML** - Security Assertion Markup Language

SAML 2.0 uses three entities: 
- The principal
- The Service provider (SP)
- The Identity provider (IdP)

SAML Working- 
If Alice enter her username and password into hdfc.com, the site sends the credentials to the IdP, The validate and then responds back with an XML message validating Alice Credentials. 

These XML have - Authentication Assertion, Authorisation Assertion and Attribute Assertion 

OAuth - Provides Authorisation framework
OpenID - Provides Authentication framework 
OpenID Connect - Provides Authorisation [Using OAuth 2.0] and Authentication

Open ID connect is also maintained by OpenID foundation but uses a JavaScript Object Notation (JSON) Web Token (JWT), also called an ID token, OpenID connect uses a web service to retrieve the JWT. In addition to providing authentication, the JWT can also include profile information about the user.

**Kerberos** - Kerberos offers a SSO for users and protects logon credentials, It uses AES symmetric encryption protocol. Kerberos provides confidentiality and integrity for authentication traffic using end to end security. Kerberos is used for internal network.

**Key Distribution Centre (KDC)** - The Key Distribution Centre is the trusted third party that provides authentication services. Kerberos uses symmetric-key cryptography to authenticate clients to servers. All clients and servers are registered with the KDC and it maintains the secret keys for all network members

**Kerberos Authentication Server** - The authentication servers hosts the function of the KDC : a ticket granting system (TGS) and an authentication service (AS) . However it is possible to host the ticket granting system on another service. The authentication service verifies or rejects the authenticity and timeliness of tickets. This server is often called the KDC

**Ticket** - A ticket is an encrypted message that provides proof that a subject is authorized to access an object. it is sometimes called a service ticket (ST). Kerberos tickets have specific lifetimes and usage parameters. Once a ticket expires, a client must request a renewal or a new ticket to continue communications with any server. 

**Ticket Granting Ticket** - A Ticket Granting Ticket (TGT) provides proof that a subject has authenticated through KDC and is authorized to request tickets to access other objects, A TGT is encrypted and includes a symmetric key, an expiration time and the users IP address. Subjects present the TGT when a requesting tickets to access objects. 

**Kerberos Principal** : Kerberos issues tickets to Kerberos principals, A Kerberos principal is typically a user but can be any entity that can request a ticket. 

**Kerberos Realm** : Generically, a realm is an area controlled or rules by something. A Kerberos realm is a logical area (such as a CHAPTER or network)ruled by Kerberos. Principals with the realm can request tickets from Kerberos and Kerberos can issue tickets to principals in the realm 

**RADIUS** - Remote Authentication Dial-in User Service (RADIUS) 

**TACACS+** - Terminal Access Controller Access Control System Plus

**MD5 128** - Less Secure & More Collision
