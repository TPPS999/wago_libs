# WagoSysBACnet_Internal_PFC v1.0.4.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysBACnet_Internal_PFC
- **Version:** 1.0.4.2
- **Categories:** WAGO Internal|Common; WAGO Internal|Feature|Common; WAGO Internal|Feature|Network; WAGO Internal|Target|PFC
- **Namespace:** WagoSysBACnet_Internal
- **Author:** WAGO <u010716>

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

This library provides IEC communication with bacnet objects. For use this library you need the license “BACnet/IP 300”. [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. This library provides IEC communication with bacnet objects. For use this library you need the license “BACnet/IP 300”. [1]

### Contents: ¶


Contents: - Project Information - Library Information - Functions FuBACnetAddListElement (FUN) - FuBACnetObjectCreate (FUN) - FuBACnetObjectDelete (FUN) - FuBACnetObjectRead (FUN) - FuBACnetObjectWrite (FUN) - FuBACnetRemoveListElement (FUN) Program Organization Internal Components Global Variable Lists Other Components - 20 Object - 25 Common

### Indices and tables ¶


| [1] | Based on WagoSysBACnet_Internal_PFC.library, last modified 27.08.2022, 20:15:59. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysBACnet_Internal_PFC.library |
| contentFile | WagoSysBACnet_Internal_PFC_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 27.08.2022, 20:15:59 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 27.08.2022, 20:15:59 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved |
| Author | WAGO <u010716> |
| DefaultNamespace | WagoSysBACnet_Internal |
| Company | WAGO |
| Title | WagoSysBACnet_Internal_PFC |
| Project | WagoSysBACnet_Internal_PFC |
| NoPlaceholder |  |
| Version | version | 1.0.4.2 |
| LibraryCategories | library-category-list | WAGO Internal\|Common; WAGO Internal\|Feature\|Common; WAGO Internal\|Feature\|Network; WAGO Internal\|Target\|PFC |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces.

### WagoSysVersion


#### Library Identification


Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: WagoSysVersion, 1.0.0.0 (WAGO) SystemLibrary: False | Optional: False |

### WagoTypesBACnet


#### Library Identification


Placeholder: WagoTypesBACnet Default Resolution: WagoTypesBACnet, * (WAGO) Namespace: WagoTypesBACnet

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: WagoTypesBACnet SystemLibrary: False | Optional: False |

#### Library Parameter


Parameter: MAX_BACNETACTIONS = 5 Parameter: LEN_BACNETOBJECTNAME = 50 Parameter: MAX_BACNETBITTEXTITEMS = 64 Parameter: LEN_BACNETACTIVETEXT = 50 Parameter: LEN_BACNETDEVICETYPE = 50 Parameter: MAX_BACNETACTIONCOMMANDS = 10 Parameter: MAX_BACNETALARMVALUES = 5 Parameter: LEN_BACNETVALUECHARSTRING = 80 Parameter: LEN_BACNETBITTEXT = 50 Parameter: MAX_BACNETACTIONTEXTITEMS = 5 Parameter: MAX_BACNETACTIONLIST = 5 Parameter: MAX_BACNETDATELISTITEMS = 25 Parameter: MAX_BACNETFAULTVALUES = 5 Parameter: MAX_BACNETDAILYSCHEDULEITEMS = 10 Parameter: BACNET_MAX_TASKS = 50 Parameter: MAX_BACNETTIMEVALUES = 10 Parameter: LEN_BACNETACTIONTEXT = 50 Parameter: LEN_BACNETSTATETEXT = 50 Parameter: LEN_BACNETEVENTMESSAGETEXTS = 50 Parameter: LEN_BACNETDESCRIPTION = 50 Parameter: MAX_BACNETSPECIALEVENTS = 10 Parameter: MAX_BACNETPROPERTYREFERENCES = 10 Parameter: LEN_BACNETINCTIVETEXT = 50

### Functions


## FuBACnetAddListElement (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuBACnetAddListElement | DWORD |  |
| Input | ObjectIdentifier | WagoTypesBACnet.typBACnetObjectIdentifier |  |
| ePropertyID | WagoTypesBACnet.eBACnetPropertyIdentifier | UDINT |
| uiSubIndex | UINT | need depend on ePropertyID |
| ptrEntry | POINTER TO BYTE | Type depend on ePropertyID |

## FuBACnetObjectCreate (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuBACnetObjectCreate | DWORD |
| Input | ObjectIdentifier | WagoTypesBACnet.typBACnetObjectIdentifier |
| ObjectName | STRING(50) |
| ptrPropertyList | POINTER TO BYTE |

## FuBACnetObjectDelete (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuBACnetObjectDelete | DWORD |
| Input | ObjectIdentifier | WagoTypesBACnet.typBACnetObjectIdentifier |

## FuBACnetObjectRead (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuBACnetObjectRead | DWORD |  |
| Input | eStructType | WagoTypesBACnet.eBACnetStructType |  |
| ptrDataStruct | POINTER TO BYTE | get optional properties from BACnet |

## FuBACnetObjectWrite (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuBACnetObjectWrite | DWORD |
| Input | eStructType | WagoTypesBACnet.eBACnetStructType |
| ptrDataStruct | POINTER TO BYTE |

## FuBACnetRemoveListElement (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuBACnetRemoveListElement | DWORD |  |
| Input | ObjectIdentifier | WagoTypesBACnet.typBACnetObjectIdentifier |  |
| ePropertyID | WagoTypesBACnet.eBACnetPropertyIdentifier | UDINT |
| uiIndex | UINT | 0..n Index of the list element to delete -> first index = 0 |
| uiSubIndex | UINT | need depend on ePropertyID |

### Program Organization


## 20 Program Organization Units


- 20 Object FuBACnetObjectCreate (FUN) - FuBACnetObjectDelete (FUN) - FuBACnetObjectRead (FUN) - FuBACnetObjectWrite (FUN) 25 Common - FuBACnetAddListElement (FUN) - FuBACnetRemoveListElement (FUN)

### Internal Components


## WagoSysBACnet_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysBACnet_Internal_PFC |
| Version: | 1.0.4.2 |
| Categories: | WAGO Internal\|Common; WAGO Internal\|Feature\|Common; WAGO Internal\|Feature\|Network; WAGO Internal\|Target\|PFC |
| Namespace: | WagoSysBACnet_Internal |
| Author: | WAGO <u010716> |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

This library provides IEC communication with bacnet objects. For use this library you need the license “BACnet/IP 300”. [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. This library provides IEC communication with bacnet objects. For use this library you need the license “BACnet/IP 300”. [1]

### Contents:


- 20 Program Organization Units 20 Object - 25 Common VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysBACnet_Internal_PFC.library, last modified 27.08.2022, 20:15:59. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## VersionHistory (GVL)


| date | version | author | change |
| 28.07.2022 | 1.0.4.2 | u0103719 | replace library (WagoSysDRM->WagoSysVersion) |
| 07.02.2020 | 1.0.4.1 | u010545 | DRM removed |
| 25.11.2019 | 1.0.4.0 | u010545 | new FW-API -> struct type |
| 08.10.2019 | 1.0.3.0 | u010545 | linked object list |
| 30.09.2019 | 1.0.1.0 | u010716 | Obsolet remote property interface and PrioArray interfaces removed |
| 06.06.2019 | 1.0.0.0 | u010545 | Release |

WagoSysBACnet_Internal_PFC

Release Note

This library provides communication with bacnet objects

WagoSysBACnet_Internal_PFC Release Note This library provides communication with bacnet objects

### Other Components


## 20 Object


- FuBACnetObjectCreate (FUN) - FuBACnetObjectDelete (FUN) - FuBACnetObjectRead (FUN) - FuBACnetObjectWrite (FUN)

## 25 Common


- FuBACnetAddListElement (FUN) - FuBACnetRemoveListElement (FUN)