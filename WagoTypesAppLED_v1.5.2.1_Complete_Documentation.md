# WagoTypesAppLED v1.5.2.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesAppLED
- **Version:** 1.5.2.1
- **Categories:** Application; WAGO FunctionalView|Device|Controller; WAGO LayerView|Types and Interfaces; WAGO Internal|Feature|Common|AppLED
- **Author:** WAGO / u013972
- **Placeholder:** WagoTypesAppLED

### Description ¶


This document is automatically generated.

Types for Handling App LEDs

This document is automatically generated. Types for Handling App LEDs

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Functions - Other Components eLedColor (ENUM) - eLedID (ENUM)

### Indices and tables ¶


Based on WagoTypesAppLED.library, last modified 29.05.2024, 19:53:40. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesAppLED.library, last modified 29.05.2024, 19:53:40. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesAppLED Library Documentation


| Company: | WAGO |
| Title: | WagoTypesAppLED |
| Version: | 1.5.2.1 |
| Categories: | Application; WAGO FunctionalView\|Device\|Controller; WAGO LayerView\|Types and Interfaces; WAGO Internal\|Feature\|Common\|AppLED |
| Author: | WAGO / u013972 |
| Placeholder: | WagoTypesAppLED |

### Description


This document is automatically generated.

Types for Handling App LEDs

This document is automatically generated. Types for Handling App LEDs

### Contents:


- FuGetVersionHistory (FUN) - eLedColor (ENUM) - eLedID (ENUM)

### Indices and tables


Based on WagoTypesAppLED.library, last modified 29.05.2024, 19:53:40. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesAppLED.library, last modified 29.05.2024, 19:53:40. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesAppLED.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:53:40 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:53:40 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesAppLED |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesAppLED |
| DefaultNamespace |  |
| Version | version | 1.5.2.1 |
| Title | string | WagoTypesAppLED |
| LibraryCategories | library-category-list | Application; WAGO FunctionalView\|Device\|Controller; WAGO LayerView\|Types and Interfaces; WAGO Internal\|Feature\|Common\|AppLED |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces.

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 22.02.2024 | 1.5.2.1 | u010663 | Compiled SP16.3 |
| 08.01.2019 | 1.5.2.0 | u015842 | Properties: free placeholder added |
| 06.02.2018 | 1.5.1.2 | WAGO / u013972 | Change in the Documentation |
| 23.09.2015 | 1.5.1.0 | WAGO / u013972 | Add Placeholder Property |
| 03.07.2015 | 1.5.0.0 | WAGO / u013972 | Release Version |

WagoTypesAppLED

Interface variables WagoTypesAppLED

### Other Components


## eLedColor (ENUM)


| Name | Initial |
| --- | --- |
| Off | 0 |
| Green | 1 |
| Red | 2 |
| Yellow | 3 |
| Blue | 4 |
| Cyan | 5 |
| Magenta | 6 |
| White | 7 |

```
eLedColor.Red
```

This enumeration specifies one of the colors which the LED could display.

For the PFCX00-System are only the Colors Green, Red and Yello supported.

Prefix-Notations like LED_COLOR_OFF as known from v2.3 is not necessary here, because in V3 the type-name itself serves as sub-namespace.

InOut: Function This enumeration specifies one of the colors which the LED could display. Note For the PFCX00-System are only the Colors Green, Red and Yello supported. Note Prefix-Notations like LED_COLOR_OFF as known from v2.3 is not necessary here, because in V3 the type-name itself serves as sub-namespace. Example

## eLedID (ENUM)


| Name | Initial |
| --- | --- |
| none | 0 |
| AppLED_1 | 1 |
| AppLED_2 | 2 |
| AppLED_3 | 3 |
| AppLED_4 | 4 |
| AppLED_5 | 5 |
| AppLED_6 | 6 |
| AppLED_7 | 7 |

This enumeration identifies one of the LEDs which can be operated with FbAppLED .

On some PLCs only a subset of this enumeration, e.g. AppLED_1 ... AppLED_4 or AppLED_1 ... AppLED_6 , is physically available.

InOut: Function This enumeration identifies one of the LEDs which can be operated with FbAppLED . Note On some PLCs only a subset of this enumeration, e.g. AppLED_1 ... AppLED_4 or AppLED_1 ... AppLED_6 , is physically available.