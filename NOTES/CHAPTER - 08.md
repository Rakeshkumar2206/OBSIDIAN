**Principles of Security Models, Design, and Capabilities**

**Subject** - The Subject is the active entity that makes a request to access a resource. A subject is commonly a user, but it can also be a process, program, computer or organization. 

**Object** - The Object is the passive entity that the subject wants to access. An object is commonly a resource, such as file or printer, but it can also be a user, process, program, computer or organization.

Fail open - Protect People --- Protect Availability 
Fail Safe - Protect People --- Protect Confidentiality & Integrity 
Fail Closed - Protect Assets --- Protect Confidentiality & Integrity 
Fail Secure - Protect Assets --- Protect Confidentiality & Integrity 

**KISS** - Keep It Stupid Simple

PbD - Privacy By Design 
There are 7 basic fundamental principles of Privacy By Design 
- Proactive not Reactive, Preventive not Remedial
- Privacy as the Default 
- Privacy embedded into Design
- Full Functionality - Positive sum, not Zero-sum
- End-to-end security - Full Lifecycle Protection 
- Visibility and Transparency 
- Respect for User Privacy 

Techniques for ensuring CIA
**Confinement**
Software Designers use process confinement to restrict the actions of a program. Simple put, process confinement allows a process to read from and write to only a certain memory locations and resources. This is also known as sandboxing. It is the application of the principle of least privilege to processes. the Goal of confinement is to prevent data leakage to unauthorized programs, users or systems.

**Bounds**
The bounds of a process consist of limits set on the memory addresses and resources it can access. The bonds state the area within which a process is confined or contained.

**Isolation**
Isolation is used to protect the operating environment, the kernel of the operating system and other independent applications. Isolation is an essential component of a stable operating system. Isolation is what prevents an application from accessing the memory or resources of another application. Isolation allows for fail-soft environment. So that separate processes can operate normally or fail/crash without interfering or affecting other processes. Isolation is achieved through the enforcement of containment using bounds

**TCB - Trusted Computing Base**
The TCB design principle is the combination of hardware and software and controls that work together to forma  trusted base to enforce you security policy. The TCB is a subset of a complete information system. It should be as small as possible so that a detailed analysis can reasonably ensure that the system meets design specifications and requirements. The TCB is the only portion of that system that can trusted to adhere and enforce the security policy. It is the responsibility of TCB components to ensure that a system behaves properly in all cases and that it  adheres to the security policy under all circumstances.
- Security Perimeter - The security perimeter systems is an imaginary boundary that separates TCB from the rest of the system. This boundary ensures that no insecure communications or interactions occur between the TCB and the remaining elements of the computer system, for the TCB to communication with the rest of the  system, it must create secure channels, also called trusted paths. A trusted path is a channel established with strict standards to allow necessary communication to occur without exposing the TCB to security exploitations. A security perimeter may also allow for the use of a trusted shell, it allows a subject to perform command line operations without risk to the TCB or the subject 
- The part of the TCB that validates access to every resource prior to granting access requests is called the reference monitor. The reference monitor stands between every subject and object, verifying that a requesting subjects credentials meet the object access requirements before any requests are allowed to proceed.

**Information Flow Model**
The Information flow model focus on controlling the flow of information. Information flow models are based on the state machine model. Information flow models doesn't necessary deal with only the direction of information flow, they can also address the type of flow. Information flow can be between subjects and objects at the same or difference classification levels. An information flow model allows all authorised information flows and prevents all unauthorised information flows 

**Non-interference Model**
The non interference models is loosely based on the information flow model. However instead of being concerned about the flow of information, the non interference models is concerned with how the action of a subject at a higher security level affect the system state or the actions of a subject at a lower security 

**Take-Grant Model**
Take Rule - Allows a subject to take rights over an object
Grant Rule - Allows a subject to grant rights to an object 
Create Rule - Allows a subject to create new rights 
Remove Rule - Allows a subject to remove rights it has

**Bell-LaPadula** - Prevents leaking of Confidential Information
- The Simple Security Property states that a subject may not read information at a higher sensitivity level ( No Read Up)
- The * (star) Security property states that a subject may not write down information to an object at a lower sensitivity level ( NO write down) This is knowns as confinement property 
- The Discretionary Security property states that the system uses an access matrix to enforce discretionary access control.


**BIBA Model** - It addresses Integrity
- The Simple Integrity Property states that a subject cannot read a object lower integrity level (no read-down)
- The * (star) Integrity property states that an subject cannot modify an object at a higher integrity level ( no write up)
