# WagoTypesErrorBase v1.6.2.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesErrorBase
- **Version:** 1.6.2.1
- **Categories:** WAGO FunctionalView|Base; WAGO LayerView|Types and Interfaces; Application
- **Namespace:** WagoTypesErrorBase
- **Author:** WAGO / u010545
- **Placeholder:** WagoTypesErrorBase

### Description ¶


This document is automatically generated.

data types for error handling

This document is automatically generated. data types for error handling

### Contents: ¶


Contents: - Project Information - Library Information - Methods I_Result.GetAuxInfo (METH) - I_Result.GetDescription (METH) - I_Result.GetID (METH) - I_Result.GetInstancePath (METH) - I_Result.GetLogLevel (METH) - I_Result.GetProducerName (METH) - I_Result.GetResultObject (METH) - I_Result.GetSeverity (METH) - I_Result.GetSeverityAsString (METH) - I_Result.IsError (METH) - ... and 2 more Interfaces - I_Result (ITF) - I_ResultProperties (ITF) Base Components Global Variable Lists - Logger (GVL) - VersionHistory (GVL) Other Components - 30 Interfaces - 40 DataTypes - 99 Logger - I_ResultProperties.eSeverity (PROP) - I_ResultProperties.sDescription (PROP) - I_ResultProperties.sProducerName (PROP) - I_ResultProperties.sSeverity (PROP) - I_ResultProperties.uiID (PROP) - I_ResultProperties.xError (PROP) - typResultItem (STRUCT)

### Indices and tables ¶


Based on WagoTypesErrorBase.library, last modified 29.05.2024, 19:49:04. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesErrorBase.library, last modified 29.05.2024, 19:49:04. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesErrorBase.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:49:04 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:49:04 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u010545 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesErrorBase |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesErrorBase |
| DefaultNamespace | WagoTypesErrorBase |
| Version | version | 1.6.2.1 |
| Title | string | WagoTypesErrorBase |
| LibraryCategories | library-category-list | WAGO FunctionalView\|Base; WAGO LayerView\|Types and Interfaces; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties :

### Methods


## I_Result.GetAuxInfo (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetAuxInfo | DWORD |

gets auxiliary information which is stored together with the result object

Interface variables gets auxiliary information which is stored together with the result object

## I_Result.GetDescription (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetDescription | STRING |

gets the description string of the result

Interface variables gets the description string of the result

## I_Result.GetID (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetID | UINT |

gets the numerical ID of the result

Interface variables gets the numerical ID of the result

## I_Result.GetInstancePath (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetInstancePath | STRING(255) |

gets the tree representation (path) of the instance which has thrown the result

Interface variables gets the tree representation (path) of the instance which has thrown the result

## I_Result.GetLogLevel (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetLogLevel | WORD |

gets the log level of the represented result

Interface variables gets the log level of the represented result

## I_Result.GetProducerName (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetProducerName | STRING |

gets the string representation of the instance which has thrown the result

Interface variables gets the string representation of the instance which has thrown the result

## I_Result.GetResultObject (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetResultObject | I_Result |

## I_Result.GetSeverity (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetSeverity | WagoTypes.eSeverity |

gets the severity of the represented result

Interface variables gets the severity of the represented result

## I_Result.GetSeverityAsString (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetSeverityAsString | STRING |

## I_Result.IsError (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IsError | BOOL |

## I_Result.SetUp (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | SetUp | BOOL |  |  |
| Input | IFactory | I_ResultFactory | 0 | reference to the factory that generates this result |
| pResultItem | POINTER TO typResultItem |  | pointer to result list with possible results [array[0..n] of typResultItem] |
| dwAdditionalInformation | DWORD |  | additional information; |

Construct a Result Object from the ResultItem and the Producer information

Interface variables Construct a Result Object from the ResultItem and the Producer information

## I_Result.ShowResult (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Output | xIsError | BOOL |
| uiId | UINT |
| sDescription | STRING |
| sProducer | STRING |
| sInstance | STRING(255) |
| eSeverity | WagoTypes.eSeverity |

Description: This method provide to show the result content directly in CFC with one call

This function block is to split a result object to output variables for comfortable showing the content inside the IDE in CFC.

The output xError is TRUE by severity equal error or exception.

Interface variables Description: This method provide to show the result content directly in CFC with one call This function block is to split a result object to output variables for comfortable showing the content inside the IDE in CFC. The output xError is TRUE by severity equal error or exception.

### Interfaces


## I_Result (ITF)


this interface may <optional> implement in application FB’s for iteration over several FB’s to find error objects - I_Result.GetAuxInfo (METH) - I_Result.GetDescription (METH) - I_Result.GetID (METH) - I_Result.GetInstancePath (METH) - I_Result.GetLogLevel (METH) - I_Result.GetProducerName (METH) - I_Result.GetResultObject (METH) - I_Result.GetSeverity (METH) - I_Result.GetSeverityAsString (METH) - I_Result.IsError (METH) - I_Result.SetUp (METH) - I_Result.ShowResult (METH)

## I_ResultProperties (ITF)


this interface may <optional> implement in application FB’s for iteration over several FB’s to find error objects - I_ResultProperties.eSeverity (PROP) - I_ResultProperties.sDescription (PROP) - I_ResultProperties.sProducerName (PROP) - I_ResultProperties.sSeverity (PROP) - I_ResultProperties.uiID (PROP) - I_ResultProperties.xError (PROP)

### Base Components


## WagoTypesErrorBase Library Documentation


| Company: | WAGO |
| Title: | WagoTypesErrorBase |
| Version: | 1.6.2.1 |
| Categories: | WAGO FunctionalView\|Base; WAGO LayerView\|Types and Interfaces; Application |
| Namespace: | WagoTypesErrorBase |
| Author: | WAGO / u010545 |
| Placeholder: | WagoTypesErrorBase |

### Description


This document is automatically generated.

data types for error handling

This document is automatically generated. data types for error handling

### Contents:


- 30 Interfaces I_Result (ITF) - I_ResultProperties (ITF) 40 DataTypes - typResultItem (STRUCT) 99 Logger - Logger (GVL) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesErrorBase.library, last modified 29.05.2024, 19:49:04. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesErrorBase.library, last modified 29.05.2024, 19:49:04. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## Logger (GVL)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | LOG_LEVEL_NONE | WORD | 16#0 | no logging |
| LOG_LEVEL_1 | WORD | 16#1 |  |
| LOG_LEVEL_2 | WORD | 16#2 |  |
| LOG_LEVEL_3 | WORD | 16#4 |  |
| LOG_LEVEL_4 | WORD | 16#8 |  |
| LOG_LEVEL_5 | WORD | 16#10 |  |
| LOG_LEVEL_6 | WORD | 16#20 |  |
| LOG_LEVEL_7 | WORD | 16#40 |  |
| LOG_LEVEL_8 | WORD | 16#80 |  |
| LOG_LEVEL_9 | WORD | 16#100 |  |
| LOG_LEVEL_10 | WORD | 16#200 |  |
| LOG_LEVEL_11 | WORD | 16#400 |  |
| LOG_LEVEL_12 | WORD | 16#800 |  |
| LOG_LEVEL_13 | WORD | 16#1000 |  |
| LOG_LEVEL_14 | WORD | 16#2000 |  |
| LOG_LEVEL_15 | WORD | 16#4000 |  |
| LOG_LEVEL_16 | WORD | 16#8000 |  |
| LOG_LEVEL_ALL | WORD | 16#FFFF |  |

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 26.02.2024 | 1.6.2.1 | u010663 | Compiled SP16.3 |
| 15.01.2021 | 1.6.2.0 | u015842 | I_ResultProperties added |
| 08.01.2019 | 1.6.1.0 | u015842 | Properties: free placeholder added |
| 16.12.2016 | 1.6.0.0 | u010545 | I_ResultLogListener removed |
| 30.03.2016 | 1.5.0.1 | u010545 | Bugfix ‘global_init_slot’ |
| 24.02.2016 | 1.5.0.0 | u010545 | First version |

WagoTypesErrorBase

Release Notes:

WagoTypesErrorBase Release Notes:

### Other Components


## 30 Interfaces


- I_Result (ITF) I_Result.GetAuxInfo (METH) - I_Result.GetDescription (METH) - I_Result.GetID (METH) - I_Result.GetInstancePath (METH) - I_Result.GetLogLevel (METH) - I_Result.GetProducerName (METH) - I_Result.GetResultObject (METH) - I_Result.GetSeverity (METH) - I_Result.GetSeverityAsString (METH) - I_Result.IsError (METH) - I_Result.SetUp (METH) - I_Result.ShowResult (METH) I_ResultProperties (ITF) - I_ResultProperties.eSeverity (PROP) - I_ResultProperties.sDescription (PROP) - I_ResultProperties.sProducerName (PROP) - I_ResultProperties.sSeverity (PROP) - I_ResultProperties.uiID (PROP) - I_ResultProperties.xError (PROP)

## 40 DataTypes ¶


- typResultItem (STRUCT)

## 99 Logger ¶


## I_ResultProperties.eSeverity (PROP) ¶


## I_ResultProperties.sDescription (PROP) ¶


## I_ResultProperties.sProducerName (PROP) ¶


## I_ResultProperties.sSeverity (PROP) ¶


## I_ResultProperties.uiID (PROP) ¶


## I_ResultProperties.xError (PROP) ¶


## typResultItem (STRUCT)


| Name | Type | Initial | Comment |
| --- | --- | --- | --- |
| ID | UINT | 0 | error number |
| LogLevel | WORD | LOG_LEVEL_NONE |  |
| Severity | WagoTypes.eSeverity | WagoTypes.eSeverity.error | INFO, ERROR, etc (from WagoTypesCommon) |
| text | STRING | ‘->Unknown<-‘ | error description |

combination of numerical identification of a result and string representation of that result.

Please note: for different languages there might be different ResultItem objects containing the same ID but different localized texts.

InOut: combination of numerical identification of a result and string representation of that result. Please note: for different languages there might be different ResultItem objects containing the same ID but different localized texts.