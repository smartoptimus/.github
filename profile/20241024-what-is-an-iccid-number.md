# What is an ICCID Number

Every SIM card in a mobile device contains an ICCID (Integrated Circuit Card Identification), which serves as its unique identifier within the mobile network. This number is essential for ensuring that devices remain connected and traceable across global networks.

This article explains what an ICCID number is, how to locate and troubleshoot it, and its significance for managing devices at scale. Additionally, it examines how the ICCID interacts with other important identifiers such as IMSI and IMEI, particularly in addressing cross-border connectivity challenges.



## What Do the Numbers in an ICCID Represent?
Although an ICCID may appear as just a long string of numbers, each section contains significant information about the SIM card. Information must be accurate according to ITU-T E.118 standart. 

Let’s examine the sample ICCID: 89 352 02 100000077159 6.

<b>89</b>: The first two digits are always the same, indicating that this is a telecommunications product typically associated with mobile networks, regardless of whether the SIM card is currently active.

<b>352</b>: This segment <i>usually</i> denotes the country code. In this instance, it indicates that the SIM card is linked to Luxembourg.

<b>02</b>: These digits correspond to the mobile network code (MNC), which identifies the mobile network operator that issued the SIM. This information can be used for connecting the SIM card to its home network.

<b>100000077159</b>: The final set of digits makes each ICCID number unique in the world. This number is vital for managing SIM cards, whether for activating services or troubleshooting issues.

<b>6</b>: Check digit calculated by Luhn algo from the ICCID value.

Lengths of the country code and mobile network code may differ, but the sequence and the meaning persists.

## Can ICCID Numbers Be Recycled or Reused?

ICCID numbers are unique identifiers assigned to each SIM card, ensuring they stand out across mobile networks. Once an ICCID is issued, it remains permanently associated with that SIM card, which is vital for effective network and SIM management.

The topic of ICCID recycling is complex. Although it is technically possible, network operators typically avoid this practice due to the risk of conflicts within system databases and network management platforms. Operators often wait an extended period before considering an ICCID for reuse &mdash; if they choose to do so &mdash; due to several reasons:

- <b>Operational Risks:</b> Reusing an ICCID can create conflicting data in billing systems, device management platforms, and inventory databases. A recycled ICCID might mistakenly link to a different SIM or user, leading to significant connectivity issues and misconfigurations.

- <b>Global Uniqueness Standard:</b> The ITU-T E.118 recommendation requires ICCID numbers to be globally unique. While the standard does not prohibit recycling, operators generally regard ICCIDs as unique indefinitely, thereby reducing the chances of reassignment.

Although ICCID recycling may seem like a minor issue for businesses managing numerous SIM cards, it is essential to monitor deactivated ICCIDs to prevent potential errors in system databases. Keeping management platforms current ensures that recycled numbers do not lead to complications during reactivation or SIM swaps.



## ICCID vs. IMSI vs. IMEI

In addition to the ICCID, it’s essential to understand two other mobile network identifiers: IMSI and IMEI. The ICCID identifies your SIM card, the IMSI identifies the specific subscriber, and the IMEI identifies the specific device.

### IMSI

IMSI, or "International Mobile Subscriber Identity" is a unique identification number assigned to mobile subscribers. It is stored on the SIM card, and while most SIM cards contain a single IMSI linked to a list of authorized networks, some SIMs can support multiple IMSIs. This allows the SIM to switch identities, enabling access to more networks and optimizing coverage.

The IMSI should not be confused with a telephone number. It can have up to 15 digits and is divided into three parts:

 - Mobile Country Code (MCC): The first three digits indicate the home country of the operator that issued the SIM. 
 - Mobile Network Code (MNC): The next two or three digits denote the specific network in use. 
 - Subscriber Identification Number: The remaining digits uniquely identify the user, ensuring that no two users share the same IMSI.

Note that here MCC and MNC are different from those of ICCID.

### IMEI

The International Mobile Station Equipment Identity (IMEI) is a unique 15-digit seial number used to identify each mobile device. It consists of four components:

 - Reporting Body Identifier: The first two digits indicate the reporting body identifier, showing the Type Allocation Code (TAC) approved by the GSMA.
 - Type Allocation Code (TAC): The next six digits represent the TAC.
 - Device Identifier: The following six digits uniquely identify the specific device.
 - Check Digit: The final digit is a check digit that helps prevent errors in equipment databases.
There are also software versions of IMEIs known as IMEISVs. An IMEISV does not include a check digit, and the last two digits indicate the Software Version Number (SVN).
