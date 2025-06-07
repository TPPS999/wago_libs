# WagoTypesCanExtra v1.0.0.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesCanExtra
- **Version:** 1.0.0.1
- **Namespace:** _3SCSS
- **Author:** WAGO
- **Placeholder:** PlaceholderTemplate

### Description ¶


This document is automatically generated.

Extra Types for new CANopen Configurator

This document is automatically generated. Extra Types for new CANopen Configurator

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Global Variable Lists - Other Components 3SImport - DATA_TYPE (ENUM) - OBJECT_PROPERTIES (ENUM) - OD_OBJECT_DATA (STRUCT) - OD_SUBOBJECT_DATA (STRUCT)

### Indices and tables ¶


Based on WagoTypesCanExtra.library, last modified 29.05.2024, 19:56:04. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesCanExtra.library, last modified 29.05.2024, 19:56:04. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesCanExtra Library Documentation


| Company: | WAGO |
| Title: | WagoTypesCanExtra |
| Version: | 1.0.0.1 |
| Namespace: | _3SCSS |
| Author: | WAGO |
| Placeholder: | PlaceholderTemplate |

### Description


This document is automatically generated.

Extra Types for new CANopen Configurator

This document is automatically generated. Extra Types for new CANopen Configurator

### Contents:


- 3SImport DATA_TYPE (ENUM) - OBJECT_PROPERTIES (ENUM) - OD_OBJECT_DATA (STRUCT) - OD_SUBOBJECT_DATA (STRUCT) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesCanExtra.library, last modified 29.05.2024, 19:56:04. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesCanExtra.library, last modified 29.05.2024, 19:56:04. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesCanExtra.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:56:04 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:56:04 |
| Description | string | See: Description |
| DocFormat | reStructuredText |
| Author | WAGO |
| AutoResolveUnbound | bool | True |
| LanguageModelAttribute | string | qualified-access-only |
| Company | WAGO |
| Placeholder | PlaceholderTemplate |
| SourceLibrary | bool | False |
| Project | string | WagoTypesCanExtra |
| DefaultNamespace | _3SCSS |
| Version | version | 1.0.0.1 |
| Title | string | WagoTypesCanExtra |
| Released | bool | False |
| LibraryCategories | library-category-list |  |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |
| IsEndUserLibrary | bool | False |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CAA FB Factory Library Identification : Placeholder: CAA FB Factory Default Resolution: CAA FB Factory, * (CAA Technical Workgroup) Namespace: FBF Library Properties : CAA Types Extern Library Identification : Placeholder: CAA Types Default Resolution: CAA Types Extern, * (CAA Technical Workgroup) Namespace: CAA Library Properties : Common Behaviour Model Library Identification : Placeholder: CBML Default Resolution: Common Behaviour Model, * (3S - Smart Software Solutions GmbH) Namespace: CBML Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties :

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 28.02.2024 | 1.0.0.1 | u010663 | compiled SP16.3 |
| 27.04.2020 | 1.0.0.0 | u013939 | initial version |

WagoTypesCanExtra

### Other Components


## 3SImport


- DATA_TYPE (ENUM) - OBJECT_PROPERTIES (ENUM) - OD_OBJECT_DATA (STRUCT) - OD_SUBOBJECT_DATA (STRUCT)

## DATA_TYPE (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| BOOLEAN | 16#1 |  |
| INT8 | 16#2 |  |
| INT16 | 16#3 |  |
| INT32 | 16#4 |  |
| UINT8 | 16#5 |  |
| UINT16 | 16#6 |  |
| UINT32 | 16#7 |  |
| REAL32 | 16#8 |  |
| VISIBLE_STRING | 16#9 |  |
| INT24 | 16#10 | OCTET_STRING := 16#0A, UNICODE_STRING := 16#0B, TIMEOFDAY := 16#0C, TIME_DIFFERENCE := 16#0D, DOMAIN := 16#0F, |
| REAL64 | 16#11 |  |
| INT40 | 16#12 |  |
| INT48 | 16#13 |  |
| INT56 | 16#14 |  |
| INT64 | 16#15 |  |
| UINT24 | 16#16 |  |
| UINT40 | 16#18 |  |
| UINT48 | 16#19 |  |
| UINT56 | 16#1A |  |
| UINT64 | 16#1B | PDO_COMMUNICATION_PARAMETER := 16#20, PDO_MAPPING := 16#21, SDO_PARAMETER := 16#22, IDENTITY := 16#23 |

internal enum for configuring CANopen local device with configurator 3.5.4

Attributes: qualified_only InOut: internal enum for configuring CANopen local device with configurator 3.5.4

## OBJECT_PROPERTIES (ENUM)


| Name | Initial |
| --- | --- |
| READ_ACCESS | 16#1 |
| WRITE_ACCESS | 16#2 |
| FORMULA | 16#4 |
| EXTERNAL_MEMORY | 16#8 |
| REFUSE_SDO_ACCESS | 16#10 |

internal enum for configuring CANopen local device with configurator 3.5.4

Attributes: qualified_only InOut: internal enum for configuring CANopen local device with configurator 3.5.4

## OD_OBJECT_DATA (STRUCT)


| Name | Type |
| --- | --- |
| wIndex | WORD |
| bySubCnt | BYTE |

internal struct for configuring CANopen local device with configurator 3.5.4

InOut: internal struct for configuring CANopen local device with configurator 3.5.4

## OD_SUBOBJECT_DATA (STRUCT)


| Name | Type |
| --- | --- |
| udiSize | UDINT |
| xwData | __XWORD |
| xwDefault | __XWORD |
| bySubIdx | BYTE |
| eDataType | DATA_TYPE |
| eObjProperties | OBJECT_PROPERTIES |

internal struct for configuring CANopen local device with configurator 3.5.4

InOut: internal struct for configuring CANopen local device with configurator 3.5.4