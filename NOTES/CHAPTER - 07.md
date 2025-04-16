**PKI and Cryptography Applications**

**RSA** - Ronald Rivest, Adi Shamir and Leonard Adleman proposed the RSA Public key algorithm in the year 1977.

**ECC** - The same year that Elgamal published his algorithm, two other mathematicians, NealKoblitz from the University of Washington and Victor Miller from IBM, independently proposed the application of elliptic curve cryptography (ECC).

**HASH FUNCTIONS**- Hash functions have a very simple purpose - they take a potentially long message and generate unique output derived from the content of the message. This value is commonly referred to as the message digest. 

According to RSA Security, there are five basic requirement for a cryptography hash function:
- *The input can be of any length*
- *The output has a fixed length* 
- *The hash  function is relatively easy to compute for any input*
- *The hash function is one way.*
- *The hash function is collision resistant.* 

**SHA** -*Secure Hash Algorithm*
SHA was introduced by the NIST for official purposes. SHA 1 was deprecated in 2017 
SHA 256 produces 256BIT MD using 512 bit block
SHA 512 produces 512BIT MD using 1024 bit block


**MD5** - Message Digest 

The MD2 has algorithm was developed by Ronald Rivest in 1989 it supported the 8 bit processor, In 1990 Rivest enhanced his message digest algorithm to support 32 bit processors and increase the level of security with a version called MD4. In 1991, Rivest released the next version of Message Direct Algorithm, which he called MD5, It also produces 512 bit blocks of the message, but it uses four distinct rounds of computation to produce a digest of the same as the MD2 and MD4(128) bits. MD 5 has the same padding requirements as MD4 - the message length must be 64 bits less than a multiple of 512 bits. MD5 implements addition security features that reduces the speed of the message digest production significantly , Unfortunately in 2005 cryptanalysts were able to demonstrate 2 similar digital certificates from public key that have the same MD5 hash.

**RIPEMD**

The RIPE Message Digest (RIPEMD) series of hash functions is an alternative to the SHA family that is used in some applications, such as bitcoin cryptocurrency implementations. The family contains a series of increasingly sophisticated functions:
- RIPEMD produced a 128-bit digest and contained some structural flaws that rendered it insecure.
- RIPEMD-128 replaced RIPEMD also producing a 128 bit digest, it is also no longer considered secure
- RIPEMD-160 is the replacement for RIPEMD-128 that remains secure today and is the most commonly used of the RIPEMD variants. It produces a 160-bit hash value. 

| NAME | HASH VALUE LENGTH |
| ---- | ---- |
| HAVAL | 128, 160, 192, 224 & 256 |
| HMAC | Variable |
| MD5 | 128 |
| SHA-1 | 160 |
| SHA2-224/SHA3-224 | 224 |
| SHA2-256/SHA3-256 | 256 |
| SHA2-384/SHA3-384 | 384 |
| SHA2-512/SHA3-512 | 512 |
| RIPEMD-128 | 128 |
| RIPEMD-160 | 160 |
| RIPEMD-256 | 256 ~ 128 |
| RIPEMD-320 | 320 ~ 160 |

**DIGITAL SIGNATURES**
Once you have chosen cryptographically sound hash function and cryptographic algorithm, you can use it to implement a digital signature system.
- Digitally signed messages assure the recipient that the message truly came from the claimed sender. They enforce nonrepudiation(that is they preclude the sender from the later claiming that the message is a forgery)
- Digitally signed messages assure the recipient that the message as not altered while in transit between the sender and recipient. This protects against both malicious modifications and unintentional modification. 
Digital Signatures ensure the cryptographic goals of integrity, authentication and nonrepudiation are met.

**HMAC**
The Hashed Message Authentication algorithm implements a partial digital signature -  it guarantees the integrity of a message during transmission, but it does not provide for non repudiation. 

HMAC can be combines with any standard message digest generation algorithm, such as MD5, SHA-2 or SHA-3 by using a shared secret key. Therefore, only communication parties who know the key can generate or verify the digital signature. If the recipient decrypts the message digest but cannot successfully compare it to a message digest generate from the plaintext message, that means the message was altered 

**DIGITAL SIGNATURE STANDARD**
The National Institute of Standards and Technology specifies the digital signature algorithms acceptable for federal government use in federal information processing standard (FIPS) 186-4.
- THE Digital Signature Algorithm (DSA) as specified in FIPS 186-4. 
- The RSA algorithm, as specified in ANSI X9.31
- The Elliptic Curve DSA (ECDSA), as specified in ANSI X9.62

**CERTIFICATES**
Digital Certificates provide communicating parties with the assurance that the people they are communicating with truly are who they claim to be. Digital Certificates are essentially endorsed copies of an individuals public key. When users verify that a certificated was signed by a trusted certificate authority, They know that the public key is legitimate.

*Digital Certificate is governed by a international standard - X.509* 

*Registration Authorities assist CAs with the burden of verifying users' identities prior to issuing digital certificates. They do not directly issue certificates themselves, but they plan an important role in the certification process allowing CA to remotely validate user identities*


**Certificate Lifecycle**
	***Enrollment*** - When you want to obtain a digital certificate, you must first prove your identity to the CA in some manner; this process is call enrollment. 
	Where you have to provide some identification documents and they might check your credit report to verify you  and identity verification by trusted community leaders. 
	Once you've satisfied the certificate authority regarding your identity, you provide them with your public key in the the form of a certificate signing request (CSR). The CA next creates an X.509 digital certificate containing your identifying information and a copy of your public key. The CA then digitally signs the certificate using CA's Private Key and provides you with a copy of your digitally signed certificate. You may then safely distribute this certificate to anyone with whom you want to communicate securely. 
	Certificate authorities issue different types of certificates depending upon the level of identity verification that they perform. The simplest and most common certificates are CHAPTER Validation (DV) certificates , where the CA simply verifies that the certificates subject has control of the CHAPTER name. Extended Valuation (EV) certificates provide a higher level of business assurance and the CA takes steps to verify that the certificate owner is legitimated business before issuing the certificate. 
	***Verification*** - When you receive a certificate digitally from someone with whom you want to communicate, you verify the certificate by checking the CA's digital signature using the CA's Public key. You then must check the validity period of the certificate to ensure that the current date is after the starting date of the certificate and that the certificate has no yet expired. 
	Finally you must check and ensure that the certificate was not revoked using a certificate revocation list  (CRL) or the Online certificate Status Portal (OSCP). 
	- The Digital signature of the CA is authentic 
	- You Trust the CA
	- The Certificate is not listed on a CRL 
	- The Certificate actually contains the data you are trusting 
	***Revocation*** - Occasionally a certificate authority needs to revoke a certificate. This might occur for one of the following reasons:
	- The Certificate was compromised
	- The Certificate was erroneously issued 
	- The details of the certificate changed
	- The Security association changed
	- **CRL** - Certificate Revocation List CRLs are maintained by the various certificate authorities and the serial number of the certificates that have been issued by a CA and that have been revoked, along with the due date and time the revocation went into effect. The major disadvantage here is that the list must be downloaded and cross referenced periodically, introducing a period of latency between the time a certificate is revoked and the end user gets are notified.
	- **OCSP** - Online Certificate Status Protocol eliminates the latency inherent in the use of the certificate revocation lists by providing a means for real time certificate verification. When a client receives a certificate, its sends an OCSP request to the CA's OCSP server. The server then responds with a status of valid, invalid or unknown. The browser uses the information to determine whether the certificate is valid.
	- **Certificate Stapling** - The primary issue with OCSP is that it places a significate burden on the OCSP server operated by Certificate authorities. These server must process requests from single every single visitor to a website or other user of digital signature, verifying that the certificate is valid and not revoked. In certificate stapling, the web server contacts the OCSP server itself and receives a signed and timestamped response from the OCSP server,which it then attaches, or staples, to the digital certificate. Then, when a user requests a secure web connection, the web server sends the certificate with the stapled OCSP response to the user. The user’s browser then verifies that the certificate is authentic and also validates that the stapled OCSP response is genuine and recent. The time savings come when the next user visits the website. The web server can simply reuse the stapled certificate without contacting OCSP server. As long as the time stamp is recent enough, the user will accept the stapled certificate without needing to contact the CA's OCSP server again. Its common to have stapled certificates with a validity period of 24 hours. That reduces the burden on an OCSP server from handling on request per user over the course of a day, which could be millions of requests, to handling one request per certificate per day. That's a tremendous reduction. 


**Certificate Formats**
Digital certificates are stored in files and those files come in a variety of different format both binary and text based. 
- The most common binary format is the Distinguished Encoding Rules (DER) format. DER certifications are normally stored in files with .der, .crt or .cer extension.
- The Privacy Enhanced Module (PEM) certificate format is an ASCII text version of the DER format. PEM certificates are normally stored in with the .pem or .crt extension.
- For .crt file extension you will not be able to differentiate whether the .crt file is binary or non binary unless you look the contents of the file. 

| Standard | Format | File Extension |
| ---- | ---- | ---- |
| Distinguished Encoding Rules (DER) | BINARY | .der, .crt, .cer |
| Privacy Enhanced Mail (PEM) | TEXT | .pem, .crt |
| Personal Information Exchange  | BINARY  | .pfx, .p12 |
| P7B | TEXT | .p7b |

**Email** 
- If you need confidentiality while sending your message, encrypt the message 
- If your message must maintain integrity, you must hash the message
- If your message needs authentication, integrity and or non repudiation, you should digitally sign the message
- If your message requires confidentiality, integrity, origin authentication and non-repudiation, you should encrypt and digitally sign the message. 

**PGP**- Used for Communication, Digitally Sign Message & works on Web of Trust (optionally) 

**S/MIME** - Secure Multipurpose Internet Mail Extensions protocol has emerged as a de facto standard for encrypted email. S/MIME uses the RSA encryption algorithm and has received the backing of major industry players, including RSA Security. S/MIME relies of the use of X.509 certificates for exchanging cryptographic keys. The public keys contained in these certificates are used for digital signatures and for the exchange of symmetric keys used for longer communications sessions. User who receive a message signed with S/MIME will be able to digitally verify their signature

**SSL** - SSL was originally developed by Netscape to Provide client/server encryption for web traffic sent using the Hypertext Transfer Protocol Secure (HTTPS). Over the years, security researches discovered a number of critical flaws in the SSL protocol that render it insecure for use today. However SSL serves as the technical foundation for its successor, Transport Layer Security (TLS), which remains widely used today. 

**TLS** - TLS relies on the exchanged server's digital certificates to negotiate encryption/decryption parameters between the browser and the web server. TLS's goals is to create secure communication channel that remain open for an entire web browsing session. It depends on a combination of symmetric and asymmetric cryptography. The following steps are involved.

- When a user accesses a website. The bowser retrieves the web servers certificate and extracts the public key from it.
- The browser then creates a random symmetric key, uses the servers public key to encrypt it and sends the encrypted symmetric key to the server. 
- The server decrypts the symmetric key using its own private key and the two systems exchange all future messages using the symmetric key encryption.

It is important to understand that TLS is not an encryption algorithm itself. It is a framework within which other encryption algorithm may function. Therefore, it isn't sufficient to verify that a system is using a secure version of TLS.

TLS_DH_RSA_WITH_AES_256_CBC_SHA384

**Circuit Encryption**

Security administrators use two types of encryption techniques to protect data travelling over networks

- *Link encryption*- Protects the entire communication circuits by creating a secure tunnel between two points using either a hardware solution or a software solution that encrypts all traffic entering one end of the tunnel and decrypts all traffic entering the other end of the tunnel. 
- E2E - All the communications from the start till the end will be encrypted and ensured that the data will be safe while in transit, but although E2E encryption works in the top layer of the network level it will not work on the bottom layers. 
