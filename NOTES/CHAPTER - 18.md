
Disaster Recovery Planning

**Strikes/ Picketing** - When a huge number of employees leave the organization at the same time what impact that would have on your business. 

**SPOF**( Single Point Of Failure) - Is any component that can cause an entire system to fail. 

**System Resilience** - Refers to the ability of a system to maintain an acceptable level of service during an adverse event. 

**Fault Tolerance** - It is the ability of a system to suffer a fault but continue to operate. Fault Tolerance is achieved by adding redundant components, such as addition disks within a properly configured RAID array or additional servers within a failover clustered configuration. 

**RAID Configuration**
**RAID 0** - This also called striping. IT uses two or more disks and improves the disks performance but it does not provide fault tolerance

**RAID 1** - This is called mirroring, It uses two hard disks which both hold the same data. If one disk fails, the other disk includes the data so that a system can continue to operate after a single disk fails. 

**RAID 5** - This is also called stripping with parity, It uses three or more disks with the equivalent of one disk holding parity information. This parity information allows the reconstruction of data through mathematical calculation if a single disk is lost. 

**RAID 6** - This offers an alternative approach to disk stripping with parity. It functions in the same manner as RAID -5 but stores parity information on two disks, protecting against the failure of two separate disks but requiring a minimum of four disks to implement.

**RAID 10** - This is also known as RAID 1 = 0 or a strip of mirrors and it is configured as two or more mirrors (RAID -1) with each mirror configured in a striped (RAID-0)
configuration. It uses at least four disks but can support more as long as an even number of disks are added. 

**Trusted Recovery** - Trusted Recovery provides assurances that after a failure or crash, the system is just as secure as it was before the failure or crash occurred.
- Manual Recovery - An IT administrator is required to manually perform the actions necessary to implement a secure or trusted recovery after a failure or system crash. 
- Automated Recovery - The system is able to perform trusted recovery activities to restore itself against at least one type of failure. 
- Automated Recovery without Undue Loss - this is similar to automated recovery in that a system can restore itself against at least one type of failure. 
- Function Recovery - System that supports function recovery are able to automatically recovery specific functions. This state ensures that the system is able to successfully complete the recovery for the functions. 

**Quality Of Service** - QoS controls protect the availability of data networks under load. 
- Bandwidth 
- Latency 
- Jitter
- Packet Loss
- Interference

**Alternate Processing Sites**
- Cold Sites - No resources will be available everything has to be setup from start 
- Hot Site - HOT AF, Every resources needed for the application will be maintained and the same will be ensured and frequently updated
- Warm Site - Combination of Cold + Hot. Also this site typically takes at least 12 hours to activate from the time of disaster 
