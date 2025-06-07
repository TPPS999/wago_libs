# WagoSysDrmInterface v1.0.0.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysDrmInterface
- **Version:** 1.0.0.0
- **Categories:** WAGO Internal|Common; Application
- **Namespace:** WagoSysDrmInterface
- **Author:** u013939 / Wago
- **Placeholder:** WagoSysDrmInterface

### Description ¶


This document is automatically generated.

DRM library for PFC-G2 and TP

This document is automatically generated. DRM library for PFC-G2 and TP

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Functions FuAllocateCredits (FUN) - FuCheckExplicitLicense (FUN) - FuDrmAllocateCredits (FUN) - FuDrmCheckExplicitLicense (FUN) - FuDrmFindExplicitLicense (FUN) - FuDrmGetFreeCredits (FUN) - FuDrmGetLicenseState (FUN) - FuDrmReleaseCredits (FUN) - FuDrmReleaseExplicitLicense (FUN) - FuFindExplicitLicense (FUN) - ... and 4 more Function Groups Internal Components Global Variable Lists Other Components - 20 Programm Organisation Units - 21 ResultCodes - WagoDrmErrno (ENUM)

### Indices and tables ¶


Based on WagoSysDrmInterface.library, last modified 29.05.2024, 19:49:15. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysDrmInterface.library, last modified 29.05.2024, 19:49:15. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysDrmInterface Library Documentation


| Company: | WAGO |
| Title: | WagoSysDrmInterface |
| Version: | 1.0.0.0 |
| Categories: | WAGO Internal\|Common; Application |
| Namespace: | WagoSysDrmInterface |
| Author: | u013939 / Wago |
| Placeholder: | WagoSysDrmInterface |

### Description


This document is automatically generated.

DRM library for PFC-G2 and TP

This document is automatically generated. DRM library for PFC-G2 and TP

### Contents:


- 20 Programm Organisation Units FuDrmAllocateCredits (FUN) - FuDrmCheckExplicitLicense (FUN) - FuDrmFindExplicitLicense (FUN) - FuDrmGetFreeCredits (FUN) - FuDrmGetLicenseState (FUN) - FuDrmReleaseCredits (FUN) - FuDrmReleaseExplicitLicense (FUN) 21 ResultCodes - WagoDrmErrno (ENUM) 90 Internal - Functions VersionHistory (GVL)

### Indices and tables


Based on WagoSysDrmInterface.library, last modified 29.05.2024, 19:49:15. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysDrmInterface.library, last modified 29.05.2024, 19:49:15. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysDrmInterface.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:49:15 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:49:15 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | `` u013939 / Wago `` |
| AutoResolveUnbound | bool | True |
| LanguageModelAttribute | string | qualified-access-only |
| Company | WAGO |
| DocFormat | reStructuredText |
| SourceLibrary | bool | False |
| Project | string | WagoSysDrmInterface |
| DefaultNamespace | WagoSysDrmInterface |
| Version | version | 1.0.0.0 |
| Title | string | WagoSysDrmInterface |
| Released | bool | False |
| Placeholder | string | WagoSysDrmInterface |
| LibraryCategories | library-category-list | WAGO Internal\|Common; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |
| IsEndUserLibrary | bool | False |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : Library Parameter : Parameter: MAX_STRING_LENGTH = 255 Parameter: MAX_WSTRING_LENGTH = 255

### Functions


## FuAllocateCredits (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuAllocateCredits | WagoDrmErrno |
| Input | bCreditType | BYTE |
| dwCreditAmount | DWORD |
| Inout | lwGeneratedHandleNumber | LWORD |

External function to allocate the given amount of credits of the given credit type.

Interface variables Function External function to allocate the given amount of credits of the given credit type.

## FuCheckExplicitLicense (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuCheckExplicitLicense | WagoDrmErrno |
| Input | bLicenseType | BYTE |
| wLicenseCode | WORD |
| Inout | lwHandleNumber | LWORD |

External function to check if the given explicit license is covered or not

Interface variables Function External function to check if the given explicit license is covered or not

## FuDrmAllocateCredits (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuDrmAllocateCredits | WagoDrmErrno |  |
| Input | bCreditType | BYTE | Type of credits |
| dwCreditAmount | DWORD | Amount Amount of credits |
| Inout | lwGeneratedHandleNumber | LWORD | Generated unique number FROM the DRM system, IF the allocation was successful, |

Allocate the given amount of credits of the given credit type.

Returns DRM error code

Interface variables Function* Allocate the given amount of credits of the given credit type. Returns DRM error code

## FuDrmCheckExplicitLicense (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuDrmCheckExplicitLicense | WagoDrmErrno |  |
| Input | bLicenseType | BYTE | Value which represents the type of the explicit license. |
| wLicenseCode | WORD | Specific code of the explicit license. |
| Inout | lwHandleNumber | LWORD | A uint64_t variable, that will get an unique number from the DRM system, if the license is covered, |

Function to check if a function requiring the given explicit license may run or not

Returns DRM error code 0: Success -> license covered or evaluation mode active; 42: Application may not run; other: Error

To discover, if a license is available or not, the license state must be determined by GetLicenseState after calling CheckExpliciteLicense. Never call CheckExpliciteLicense more than once without calling ReleaseExplicitLicense. If it is necessary to update the current license state in a visu element cyclically, call GetLicenseState.

Interface variables Function* Function to check if a function requiring the given explicit license may run or not Returns DRM error code 0: Success -> license covered or evaluation mode active; 42: Application may not run; other: Error Hints: To discover, if a license is available or not, the license state must be determined by GetLicenseState after calling CheckExpliciteLicense. Never call CheckExpliciteLicense more than once without calling ReleaseExplicitLicense. If it is necessary to update the current license state in a visu element cyclically, call GetLicenseState.

## FuDrmFindExplicitLicense (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuDrmFindExplicitLicense | WagoDrmErrno |  |
| Input | bLicenseType | BYTE | Value which represents the type of the explicit license. |
| wLicenseCode | WORD | Specific code of the explicit license. |

Function to find if the given explicit license is covered or not

Returns DRM error code 0: Success -> license covered; 111: License is not covered; other: Error

Interface variables Function* Function to find if the given explicit license is covered or not Returns DRM error code 0: Success -> license covered; 111: License is not covered; other: Error

## FuDrmGetFreeCredits (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuDrmGetFreeCredits | WagoDrmErrno |  |
| Input | bCreditType | BYTE | Type of credits |
| Inout | dwFreeCredits | DINT | Current amount of credits |

Get the current balance from a specific credit type

Returns DRM error code

Interface variables Function Get the current balance from a specific credit type Returns DRM error code

## FuDrmGetLicenseState (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuDrmGetLicenseState | WagoDrmErrno |  |
| Inout | wLicenseState | WORD | Variable who will get the current licenses state. |
| dwEvalTime | DWORD | Variable which will get the remaining time of the evaluation mode in seconds. |

| License State |  |
| Licensed | 0 |
| Evaluation Mode | 1 |
| Expired | 2 |

Function to get the actual state of the device regarding the license management

Returns DRM error code

Interface variables Function* Function to get the actual state of the device regarding the license management Returns DRM error code

## FuDrmReleaseCredits (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuDrmReleaseCredits | WagoDrmErrno |  |
| Input | lwHandleNumber | LWORD | Generated number from the DRM system to release the specific requested amount of credits |

Release the specific amount of credits with the generated handle number

Returns DRM error code

Interface variables Function* Release the specific amount of credits with the generated handle number Returns DRM error code

## FuDrmReleaseExplicitLicense (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuDrmReleaseExplicitLicense | WagoDrmErrno |  |
| Input | bLicenseType | BYTE | Value which represents the type of the explicit license. |
| wLicenseCode | WORD | Specific code of the explicit license |
| lwHandleNumber | LWORD | Generated number from the DRM system to release the specific request of a explicit license. |

Function to release the requested explicit license

Returns DRM error code

Interface variables Function* Function to release the requested explicit license Returns DRM error code

## FuFindExplicitLicense (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuFindExplicitLicense | WagoDrmErrno |
| Input | bLicenseType | BYTE |
| wLicenseCode | WORD |

External function to find if the given explicit license is covered or not

Interface variables Function External function to find if the given explicit license is covered or not

## FuGetFreeCredits (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetFreeCredits | WagoDrmErrno |
| Input | bCreditType | BYTE |
| Inout | dwFreeCredits | DINT |

External function to get the current balance from a specific credit type returns DRMreturns DRM error code

Interface variables Function External function to get the current balance from a specific credit type returns DRMreturns DRM error code

## FuGetLicenseState (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetLicenseState | WagoDrmErrno |
| Inout | wLicenseState | WORD |
| dwEvalTime | DWORD |

External function to get the actual state of the device regarding the license management

Interface variables Function External function to get the actual state of the device regarding the license management

## FuReleaseCredits (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuReleaseCredits | WagoDrmErrno |
| Input | lwHandleNumber | LWORD |

External function to release the specific amount of credits with the generated handle number

Interface variables Function External function to release the specific amount of credits with the generated handle number

## FuReleaseExplicitLicense (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuReleaseExplicitLicense | WagoDrmErrno |
| Input | bLicenseType | BYTE |
| wLicenseCode | WORD |
| lwHandleNumber | LWORD |

External function to release the requested explicit license

Interface variables Function External function to release the requested explicit license

### Function Groups


## Functions


- FuAllocateCredits (FUN) - FuCheckExplicitLicense (FUN) - FuFindExplicitLicense (FUN) - FuGetFreeCredits (FUN) - FuGetLicenseState (FUN) - FuReleaseCredits (FUN) - FuReleaseExplicitLicense (FUN)

### Internal Components


## 90 Internal


- Functions FuAllocateCredits (FUN) - FuCheckExplicitLicense (FUN) - FuFindExplicitLicense (FUN) - FuGetFreeCredits (FUN) - FuGetLicenseState (FUN) - FuReleaseCredits (FUN) - FuReleaseExplicitLicense (FUN)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 07.02.2024 | 1.0.0.0 | u010663 | compiled SP16.3 |
| 01.12.2022 | 0.0.1.2 | u013972 / WAGO | fix documentation for FuDrmFindExplicitLicense and FuGetLicenseState |
| 08.04.2022 | 0.0.1.1 | u0100662 / WAGO | fix implicit type changes |
| 08.03.2021 | 0.0.1.0 | u0100179 / WAGO | add new function FuDrmFindExplicitLicense |
| 22.10.2019 | 0.0.0.4 | u013939 / WAGO | update dokumentation |
| 20.08.2019 | 0.0.0.2 | u013939 / WAGO | first test |
| 15.08.2019 | 0.0.0.1 | u013939 / WAGO | initial version |

WagoSysDrmInterface

### Other Components


## 20 Programm Organisation Units


- FuDrmAllocateCredits (FUN) - FuDrmCheckExplicitLicense (FUN) - FuDrmFindExplicitLicense (FUN) - FuDrmGetFreeCredits (FUN) - FuDrmGetLicenseState (FUN) - FuDrmReleaseCredits (FUN) - FuDrmReleaseExplicitLicense (FUN)

## 21 ResultCodes ¶


- WagoDrmErrno (ENUM)

## WagoDrmErrno (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Success | 0 |  |
| NullPointerError | 1 | libwagodrm function error 1-99 |
| InternalError | 100 | DRM errors 100-199 |
| LicenseKeyAlreadyExists | 101 |  |
| LicenseKeyNotTransferable | 102 |  |
| StorageTargetNotAvailable | 103 |  |
| LicenseKeyNotValid | 104 |  |
| EvaluationModeNotExtendable | 105 |  |
| MaximumLicenseReached | 106 |  |
| LicenseInUse | 107 |  |
| LicenseLocked | 108 |  |
| LicenseNotFound | 109 |  |
| InvalidState | 110 |  |
| LicenseNotCovered | 111 |  |
| NotEnoughCreditsAvailable | 112 |  |
| FileOpenFailed | 200 | System functions errors 200-299 |
| FileCloseFailed | 201 |  |
| IoctlError | 202 |  |