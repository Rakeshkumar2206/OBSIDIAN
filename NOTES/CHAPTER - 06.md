**CRYPTOGRAPHY AND SYMMETRIC KEY ALGORITHIMS**

**Confidentiality** - Confidentiality ensures that data remains private in three different situations: When it is at Rest, When it is in Transit and when it is in Use.

There are two types of Cryptosystems 
- *Symmetric Cryptosystems* - Which uses a shared key available to all users of the system 
- *Asymmetric Cryptosystems* - Which uses Individual combination of  Private and Public key for each user of the system 

DATA IN TRANSIT <-> DATA ON THE WIRE

**Integrity**- It ensure that data is not altered without authorization
**Authentication** - Verifies the claimed identity of system users and is a major function of cryptosystems

CRYTPOGRAPHIC KEYS <-> CRYPTOVARIABLES

**AND** - <^> Check whether the both values are true 

| X | Y | X^Y |
| ---- | ---- | ---- |
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |
**OR** - (v) Checks at least one of the input value is true 

| X | Y | XvY |
| ---- | ---- | ---- |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

**NOT**- <~> Simply reverses the Value and it operates only on 1 Value at a time

| X | ~X |
| ---- | ---- |
| 0 | 1 |
| 1 | 0 |

**XOR** - <⊕> The XOR function returns a true value when only one of the input values is true.

| X | Y | X⊕Y |
| ---- | ---- | ---- |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |
**One Way Functions**
A one way function is a mathematical operation that easily produces output values for each possible combination of inputs but makes it impossible to retrieve the input values.

**NONCE**
A Nonce is a random number that acts as placeholder variable in mathematical functions. 

**Split Knowledge**
When the information or privilege required to perform an operation is divided among multiple users, no single person has sufficient privileges to compromise the security of an environment. This separation of duties and two person control contained in a single solution is called split knowledge. 

**Codes** 
Codes are cryptographic systems that represent words or phrases, are sometimes secret, but they are not necessarily meant to provide confidentiality. 

**Ciphers**
Ciphers on the other hand are always meant to hide the true meaning of message. They use a variety of techniques to alter or rearrange the character or bits of a message to achieve confidentiality  

**Block Ciphers**
They operate on chunks or blocks of a message and apply the encryption algorithm to an entire message block at the same time. 

**Stream Cipher**
Stream Cipher operate on one character or bit of a message at a time. 

**Symmetric Key Algorithms**
Symmetric Key Algorithms rely on a shared secret encryption key that is distributed to all members who participate in the communications. Symmetric Key cryptography can also be called secret key cryptography and private jey cryptography

**Asymmetric Key Algorithms**
Asymmetric key algorithms provide a solution to the weakness of symmetric key encryption. Public key algorithms are the most common example of asymmetric algorithms.

**Electronic Code Book (ECB) Mode:**
This is like breaking your message into blocks and turning each block into a secret code separately.

**Cipher Block Chaining (CBC) Mode:**
Here, you take the secret code of one block and mix it up with the next block before turning it into a new secret code.

**Cipher Feedback (CFB) Mode:**
Instead of turning whole blocks into secret codes, you take a bit of your message at a time and mix it up to make a secret code bit by bit.

**Output Feedback (OFB) Mode:**
Similar to CFB, but here you take a bit of the plain text and XOR it with the  secret code and mix it with your message bit by bit.

**Counter (CTR) Mode:**
You use a counter (like counting numbers) to create a different secret code for each part of your message.

**Galois Counter Mode (GCM):**
This is like using CTR mode but with an extra layer of protection to make sure your message hasn't been changed by someone.

**Counter with Cipher Block Chaining Message Authentication Code (CCM) Mode:**
It's a mix of counter mode and cipher block chaining to keep your message safe and also make sure it's really from you.

**Data Encryption Standard**
DES was introduced by US government in the year 1977 and it was superseded by AES in the year 2001. DES us a 64 bit block cipher that has five modes of operation. 
- ECB 
- CBC
- CFB
- OFB
- CTR
The key used by DES is 56 bits long. DES uses a long series of exclusive or(XOR) operations to generate cipher text. Each repetition is commonly referred to as a round of encryption, explaining the statement that DES performs 16 rounds of encryption.

**Triple DES** 

Triple DES user the same algorithm as DES to produces encryption what is stronger but that is no longer considered as adequate security. There are several versions of 3DES that each use different numbers of independent keys. The first two DES-EDE3 and DES  EEE-3 use three independent keys k1, k2 and k3. 

*DES-EDE3 - E(K1,D(K2,E(K3,P)))* 

*DES-EEE3 - E(K1,E(K2,E(K3,P)))*

It is also important to note that NIST recently deprecated the use of all 3DES variants and will disallow their use in federal government applications at the end of 2023.

**International Data Encryption Algorithm**
IDEA block cipher was developed in response to complaints about the insufficient key length of the DES algorithm. Like DES, IDEA operates on 64-bit blocks of plaintext/ciphertext. However, it begins it's operation with a 128 bit key. The key is broken up in a series of operations into 52 16-bit subkeys

**Blowfish**
Blowfish operates on 64 bit blocks of text. However it extends IDEA's key strength even further by allowing the use of variable-length keys ranging from a relatively insecure 32 bits to an extremely strong 448 bits 

**Skipjack**
Skipjack uses 64 bit block of text and it uses an 80 bit key and supports the same four mode of operations as DES. Skipjack is an Escrowed Encryption Standards

**Rivest Ciphers**
Rob Rivest of Rivest-Shamir-Adleman (RSA) data security created a series of symmetric ciphers over the years known as the Rivest Ciphers family of algorithims. Several of these RC4, RC5 and RC6 have particular importance today.

**RC4**
RC4 was developed in the year 1987. It had a single round of encryption and allows the use of variable-length keys ranging from 40 bits to 2048 bits. RC4's adoption was widespread because it was integrated into Wired Equivalent Privacy (WEP), WPA, SSL and TLS protocols

**RC5**
Uses a key value from 0 to 2040 bits. It is important to note that RC5 is not simply the next version of RC4

**RC6**
RC6 is a block cipher that was developed as the next version of RC5. It uses a 128 bit block size and allows the use of 128,192 or 256 bit symmetric key. 

**Advances Encryption Standard**

In October 2000, NIST announced that Rijndael block cipher had been chosen as the replacement for DES. In November 2001, NIST released FIPS 197, which mandated the sue of AES/Rijndael for the encryption for all sensitive but unclassified data by the US government.

AES Cipher allows the use of three key strengths: 128bits, 192bits and 256 bits. AES only allows the processing of 128-bit blocks, but Rijndael exceed the specification 
- 128 bit of Keys require 10 rounds of encryption 
- 192 bit of Keys require 12 rounds of encryption 
- 256 bit of Keys require 14 rounds of encryption 


| NAME     | BOCK SIZE | KEY SIZE            |
| -------- | --------- | ------------------- |
| AES      | 128       | 128,192,256         |
| RIJNDAEL | VARIABLE  | 128,192,256         |
| BLOWFISH | 64        | 32-448              |
| DES      | 64        | 56                  |
| IDEA     | 64        | 128                 |
| RC4      | NA        | 40-2048             |
| RC5      | 32,64,128 | 0-2040              |
| RC6      | 128       | 128,192,256         |
| Skipjack | 64        | 80                  |
| 3DES     | 64        | 112 or 168          |
| CAST-128 | 64        | 40-128              |
| CAST-256 | 128       | 128,160,192,224,256 |
