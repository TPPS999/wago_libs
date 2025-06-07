# WagoTypesModule_75x_65x v1.0.0.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesModule_75x_65x
- **Version:** 1.0.0.2
- **Categories:** WAGO Internal|Common|Types and Interfaces
- **Author:** WAGO
- **Placeholder:** WagoTypesModule_75x_65x

### Description ¶


This document is automatically generated.

Datatypes and Interfaces for Handling serial 750er modules

This document is automatically generated. Datatypes and Interfaces for Handling serial 750er modules

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Interfaces I_Module_75x_1652 (ITF) - I_Module_75x_652 (ITF) Program Organization Global Variable Lists - Channels_1652 (GVL) - VersionHistory (GVL) Other Components - 10 Enumeration - I_Module_75x_1652.diRtsPostDelay (PROP) - I_Module_75x_1652.diRtsPreDelay (PROP) - I_Module_75x_1652.eBiasRx (PROP) - I_Module_75x_1652.eBiasTx (PROP) - I_Module_75x_1652.eRs485SwitchTime (PROP) - I_Module_75x_1652.eTerminationResistor (PROP) - I_Module_75x_1652.xInit (PROP) - I_Module_75x_652.diRtsPostDelay (PROP) - I_Module_75x_652.diRtsPreDelay (PROP) - ... and 4 more

### Indices and tables ¶


Based on WagoTypesModule_75x_65x.library, last modified 29.05.2024, 20:18:12. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesModule_75x_65x.library, last modified 29.05.2024, 20:18:12. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesModule_75x_65x Library Documentation


| Company: | WAGO |
| Title: | WagoTypesModule_75x_65x |
| Version: | 1.0.0.2 |
| Categories: | WAGO Internal\|Common\|Types and Interfaces |
| Author: | WAGO |
| Placeholder: | WagoTypesModule_75x_65x |

### Description


This document is automatically generated.

Datatypes and Interfaces for Handling serial 750er modules

This document is automatically generated. Datatypes and Interfaces for Handling serial 750er modules

### Contents:


- 20 Program Organization Units 10 Enumeration - Channels_1652 (GVL) - I_Module_75x_1652 (ITF) - I_Module_75x_652 (ITF) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesModule_75x_65x.library, last modified 29.05.2024, 20:18:12. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesModule_75x_65x.library, last modified 29.05.2024, 20:18:12. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesModule_75x_65x.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:18:12 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:18:12 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesModule_75x_65x |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesModule_75x_65x |
| Version | version | 1.0.0.2 |
| Version string | string |  |
| Title | WagoTypesModule_75x_65x |
| LibraryCategories | library-category-list | WAGO Internal\|Common\|Types and Interfaces |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCom Library Identification : Name: WagoTypesCom Version: newest Company: WAGO Namespace: WagoTypesCom Library Properties :

### Interfaces


## I_Module_75x_1652 (ITF)


- I_Module_75x_1652.diRtsPostDelay (PROP) - I_Module_75x_1652.diRtsPreDelay (PROP) - I_Module_75x_1652.eBiasRx (PROP) - I_Module_75x_1652.eBiasTx (PROP) - I_Module_75x_1652.eRs485SwitchTime (PROP) - I_Module_75x_1652.eTerminationResistor (PROP) - I_Module_75x_1652.xInit (PROP)

## I_Module_75x_652 (ITF)


- I_Module_75x_652.diRtsPostDelay (PROP) - I_Module_75x_652.diRtsPreDelay (PROP) - I_Module_75x_652.xInit (PROP)

### Program Organization


## 20 Program Organization Units


- 10 Enumeration eTTYBias (ENUM) - eTTYRs485SwitchTime (ENUM) - eTTYTerminationResistor (ENUM) Channels_1652 (GVL) I_Module_75x_1652 (ITF) - I_Module_75x_1652.diRtsPostDelay (PROP) - I_Module_75x_1652.diRtsPreDelay (PROP) - I_Module_75x_1652.eBiasRx (PROP) - I_Module_75x_1652.eBiasTx (PROP) - I_Module_75x_1652.eRs485SwitchTime (PROP) - I_Module_75x_1652.eTerminationResistor (PROP) - I_Module_75x_1652.xInit (PROP) I_Module_75x_652 (ITF) - I_Module_75x_652.diRtsPostDelay (PROP) - I_Module_75x_652.diRtsPreDelay (PROP) - I_Module_75x_652.xInit (PROP)

### Global Variable Lists


## Channels_1652 (GVL)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | MAX_CHANNEL_1652 | USINT | 1 | max. channels for 75x-1652 |

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 05.02.2024 | 1.0.0.2 | u010636 | Compiled with SP16.3 |
| 05.04.2023 | 1.0.0.1 | u010545 | update doku -> WAT35337 |
| 14.02.2023 | 1.0.0.0 | u010545 | bugfix doku |
| 10.12.2021 | 0.0.0.3 | u010545 | rename to ..75x_65x |
| 09.12.2021 | 0.0.0.2 | u010545 | development |
| 17.08.2021 | 0.0.0.1 | u010545 | init |

WagoTypesModule_75x_65x.library

Release Notes:

WagoTypesModule_75x_65x.library Release Notes:

### Other Components


## 10 Enumeration


- eTTYBias (ENUM) - eTTYRs485SwitchTime (ENUM) - eTTYTerminationResistor (ENUM)

## I_Module_75x_1652.diRtsPostDelay (PROP)


-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

## I_Module_75x_1652.diRtsPreDelay (PROP)


-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

## I_Module_75x_1652.eBiasRx (PROP)


| Member | Value | Description |
| --- | --- | --- |
| Default | -1 | use interface default settings |
| Disabled | 0 | Off |
| Network_1 | 1 | Network 1 |
| Network_2 | 2 | Network 2 |

WagoTypesModule_75x_1652.eTTYBias

WagoTypesModule_75x_1652.eTTYBias

## I_Module_75x_1652.eBiasTx (PROP)


| Member | Value | Description |
| --- | --- | --- |
| Default | -1 | use interface default settings |
| Disabled | 0 | Off |
| Network_1 | 1 | Network 1 |
| Network_2 | 2 | Network 2 |

WagoTypesModule_75x_1652.eTTYBias

WagoTypesModule_75x_1652.eTTYBias

## I_Module_75x_1652.eRs485SwitchTime (PROP)


| Member | Value | Description |
| --- | --- | --- |
| Default | -1 | use interface default settings |
| NoDelay | 0 | Off |
| _100us | 1 | 100 us |
| _2Characters | 2 | 2 character times |
| _4Characters | 3 | 4 character times |

WagoTypesModule_75x_1652.eTTYRs485SwitchTime

WagoTypesModule_75x_1652.eTTYRs485SwitchTime

## I_Module_75x_1652.eTerminationResistor (PROP)


| Member | Value | Description |
| --- | --- | --- |
| Default | -1 | use interface default settings |
| Off | 0 | Off |
| On | 1 | On |

WagoTypesModule_75x_1652.eTTYTerminationResistor

WagoTypesModule_75x_1652.eTTYTerminationResistor

## I_Module_75x_1652.xInit (PROP) ¶


## I_Module_75x_652.diRtsPostDelay (PROP)


-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

## I_Module_75x_652.diRtsPreDelay (PROP)


-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

## I_Module_75x_652.xInit (PROP) ¶


## eTTYBias (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Default | -1 | Use default behaviour of the interface |
| Deactivated | 0 | bias network disabled |
| Network_1 | 1 | bias network 1 |
| Network_2 | 2 | bias network 2 |

Configuration parameter for the bias network

InOut: Configuration parameter for the bias network

## eTTYRs485SwitchTime (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Default | -1 | Use default behaviour of the interface |
| NoDelay | 0 | no delay |
| _100us | 1 | 100 us |
| _2Characters | 2 | 2 characters |
| _4Characters | 3 | 4 characters |

Configuration parameter for the switchover time RS485

InOut: Configuration parameter for the switchover time RS485

## eTTYTerminationResistor (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Default | -1 | Use default behaviour of the interface |
| Off | 0 |  |
| On | 1 |  |

Configuration parameter for the termination resistor

InOut: Configuration parameter for the termination resistor