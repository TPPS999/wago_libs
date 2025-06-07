# WagoTypesEvent v1.5.2.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesEvent
- **Version:** 1.5.2.1
- **Categories:** WAGO FunctionalView|Base; WAGO LayerView|Types and Interfaces; Application
- **Author:** WAGO / u013972
- **Placeholder:** WagoTypesEvent

### Description ¶


This document is automatically generated.

Type Definitions for Handling Events

This document is automatically generated. Type Definitions for Handling Events

### Contents: ¶


Contents: - Documentation Index 10 Documentation - WagoTypesEvent Library Documentation Project Information Library Information Function Blocks Methods - typWagoParam_01b_CmpAppReset (STRUCT) - typWagoParam_03_CmpAppDenyStart (STRUCT) Base Components - typWagoParam_Base_AppName (STRUCT) - typWagoParam_Base_Application (STRUCT) Global Variable Lists Other Components - 20 Principal Types - 21 Components of unWagoEventParameter - eWagoEventID (ENUM) - eWagoEventParameterID (ENUM) - eWagoEventStopReason (ENUM) - typWagoParam_01_CmpApp (STRUCT) - typWagoParam_01a_CmpAppConfig (STRUCT) - typWagoParam_02_CmpAppStop (STRUCT) - typWagoParam_04_CmpAppDenyStop (STRUCT) - typWagoParam_05_Cmp_AllBootAppsLoaded (STRUCT) - ... and 13 more

### Indices and tables ¶


Based on WagoTypesEvent.library, last modified 29.05.2024, 19:53:57. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesEvent.library, last modified 29.05.2024, 19:53:57. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## 10 Documentation ¶


## WagoTypesEvent Library Documentation


| Company: | WAGO |
| Title: | WagoTypesEvent |
| Version: | 1.5.2.1 |
| Categories: | WAGO FunctionalView\|Base; WAGO LayerView\|Types and Interfaces; Application |
| Author: | WAGO / u013972 |
| Placeholder: | WagoTypesEvent |

### Description


This document is automatically generated.

Type Definitions for Handling Events

This document is automatically generated. Type Definitions for Handling Events

### Contents:


- 10 Documentation doc10_General (FB) 20 Principal Types - eWagoEventID (ENUM) - eWagoEventParameterID (ENUM) - unWagoEventParameter (UNION) 21 Components of unWagoEventParameter - eWagoEventStopReason (ENUM) - typWagoParam_01_CmpApp (STRUCT) - typWagoParam_01a_CmpAppConfig (STRUCT) - typWagoParam_01b_CmpAppReset (STRUCT) - typWagoParam_02_CmpAppStop (STRUCT) - typWagoParam_03_CmpAppDenyStart (STRUCT) - typWagoParam_04_CmpAppDenyStop (STRUCT) - typWagoParam_05_Cmp_AllBootAppsLoaded (STRUCT) - typWagoParam_06_CmpAppNameDenyLoadBootproject (STRUCT) - typWagoParam_07_CmpAppNamePrepareLoadBootproject (STRUCT) - typWagoParam_08_CmpAppException (STRUCT) - typWagoParam_09_CmpAppNameRegisterBootproject (STRUCT) - typWagoParam_10_CmpAppOperatingStateChanged (STRUCT) - typWagoParam_11_CmpAppNameSourceDownload (STRUCT) - typWagoParam_12_CmpAppComm (STRUCT) - typWagoParam_13_CmpAppDeny (STRUCT) - typWagoParam_14_CmpAppDenyDelete (STRUCT) - typWagoParam_15_CmpAppOEMServiceTag (STRUCT) - typWagoParam_23_Cmp_CommCycle (STRUCT) - typWagoParam_Base_AppName (STRUCT) - typWagoParam_Base_Application (STRUCT) - typWagoParam_xx_CmpAppStateChanged (STRUCT) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesEvent.library, last modified 29.05.2024, 19:53:57. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesEvent.library, last modified 29.05.2024, 19:53:57. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesEvent.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:53:57 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:53:57 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesEvent |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesEvent |
| DefaultNamespace |  |
| Version | version | 1.5.2.1 |
| Title | string | WagoTypesEvent |
| LibraryCategories | library-category-list | WAGO FunctionalView\|Base; WAGO LayerView\|Types and Interfaces; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpApp Library Identification : Placeholder: CmpApp Default Resolution: CmpApp, * (System) Namespace: CmpApp Library Properties : CmpEventMgr Library Identification : Placeholder: CmpEventMgr Default Resolution: CmpEventMgr, * (System) Namespace: CmpEventMgr Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes_Interfaces Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties :

### Function Blocks


## doc10_General (FB)


This mere type defining library wraps various type definition from the 3S-system-layer.

The most frequently needed type is eWagoEventID, followed by the tuple consisting of unWagoEventParameter and eWagoEventParameterID.

All other definitions are a paraphrasis of the somewhat poorly documented lower system level definitions. Only the input parts are relevant here.

This mere type defining library wraps various type definition from the 3S-system-layer. The most frequently needed type is eWagoEventID, followed by the tuple consisting of unWagoEventParameter and eWagoEventParameterID. All other definitions are a paraphrasis of the somewhat poorly documented lower system level definitions. Only the input parts are relevant here.

### Methods


## typWagoParam_01b_CmpAppReset (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |
| ewResetOption | RESET_OPTION | undocumented |  |

## typWagoParam_03_CmpAppDenyStart (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |

typWagoParam_03_CmpAppDenyStart

InOut: typWagoParam_03_CmpAppDenyStart Note: When comparing this with a corresponding event from CmpApp you will find an additional pointer to a return parameter udiDeny there which is passed via the input structure. For this structure, however, the return information ss passed as a return value of the event catching function and thus intentionally does not appear in this input structure.

### Base Components


## typWagoParam_Base_AppName (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| psAppName | POINTER TO STRING | Name of the application |

## typWagoParam_Base_Application (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure |

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 28.02.2024 | 1.5.2.1 | u010663 | Compiled SP16.3 |
| 08.01.2019 | 1.5.2.0 | u015842 | Properties: free placeholder added |
| 15.02.2016 | 1.5.1.1 | WAGO / u013972 | Add new EventIDs to eWagoEventID |
| 23.09.2015 | 1.5.1.0 | WAGO / u013972 | WagoSysStandard removed |
| 03.07.2015 | 1.5.0.0 | WAGO / u013972 | Release Version |

WagoTypesEvent

Note: This library is not part of WagoSysTypedefs because WagoTypesEvent requires other libraries (hierarchy issue).

WagoTypesEvent Note: This library is not part of WagoSysTypedefs because WagoTypesEvent requires other libraries (hierarchy issue).

### Other Components


## 20 Principal Types


- eWagoEventID (ENUM) - eWagoEventParameterID (ENUM) - unWagoEventParameter (UNION)

## 21 Components of unWagoEventParameter


- eWagoEventStopReason (ENUM) - typWagoParam_01_CmpApp (STRUCT) - typWagoParam_01a_CmpAppConfig (STRUCT) - typWagoParam_01b_CmpAppReset (STRUCT) - typWagoParam_02_CmpAppStop (STRUCT) - typWagoParam_03_CmpAppDenyStart (STRUCT) - typWagoParam_04_CmpAppDenyStop (STRUCT) - typWagoParam_05_Cmp_AllBootAppsLoaded (STRUCT) - typWagoParam_06_CmpAppNameDenyLoadBootproject (STRUCT) - typWagoParam_07_CmpAppNamePrepareLoadBootproject (STRUCT) - typWagoParam_08_CmpAppException (STRUCT) - typWagoParam_09_CmpAppNameRegisterBootproject (STRUCT) - typWagoParam_10_CmpAppOperatingStateChanged (STRUCT) - typWagoParam_11_CmpAppNameSourceDownload (STRUCT) - typWagoParam_12_CmpAppComm (STRUCT) - typWagoParam_13_CmpAppDeny (STRUCT) - typWagoParam_14_CmpAppDenyDelete (STRUCT) - typWagoParam_15_CmpAppOEMServiceTag (STRUCT) - typWagoParam_23_Cmp_CommCycle (STRUCT) - typWagoParam_Base_AppName (STRUCT) - typWagoParam_Base_Application (STRUCT) - typWagoParam_xx_CmpAppStateChanged (STRUCT)

## eWagoEventID (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| PrepareStart | EVT_PrepareStart |  |
| StartDone | EVT_StartDone |  |
| PrepareStop | EVT_PrepareStop |  |
| StopDone | EVT_StopDone |  |
| PrepareReset | EVT_PrepareReset |  |
| ResetDone | EVT_ResetDone |  |
| PrepareOnlineChange | EVT_PrepareOnlineChange |  |
| OnlineChangeDone | EVT_OnlineChangeDone |  |
| PrepareDownload | EVT_PrepareDownload |  |
| DownloadDone | EVT_DownloadDone |  |
| CodeInitDone | EVT_CodeInitDone |  |
| PrepareDelete | EVT_PrepareDelete |  |
| DeleteDone | EVT_DeleteDone |  |
| PrepareExit | EVT_PrepareExit |  |
| ExitDone | EVT_ExitDone |  |
| CreateBootprojectDone | EVT_CreateBootprojectDone |  |
| LoadBootprojectDone | EVT_LoadBootprojectDone |  |
| DenyLoadBootproject | EVT_DenyLoadBootproject |  |
| PrepareLoadBootproject | EVT_PrepareLoadBootproject |  |
| DenyStartBootproject | EVT_DenyStartBootproject |  |
| PrepareStartBootproject | EVT_PrepareStartBootproject |  |
| StartBootprojectDone | EVT_StartBootprojectDone |  |
| DenyStart | EVT_DenyStart |  |
| DenyStop | EVT_DenyStop |  |
| AllBootprojectsLoaded | EVT_AllBootprojectsLoaded |  |
| GlobalExitOnResetDone | EVT_GlobalExitOnResetDone |  |
| ExitDoneWithConfigAppInfo | EVT_ExitDoneWithConfigAppInfo |  |
| RegisterBootproject | EVT_RegisterBootproject |  |
| CreateBootprojectFileFailed | EVT_CreateBootprojectFileFailed |  |
| CreateBootprojectFailed | EVT_CreateBootprojectFailed |  |
| OperationStateChanged | EVT_OperationStateChanged |  |
| SourceDownload | EVT_SourceDownload |  |
| Login | EVT_Login |  |
| Logout | EVT_Logout |  |
| DenyDelete | EVT_DenyDelete |  |
| DenyDeleteBootproject | EVT_DenyDeleteBootproject |  |
| OEMDownloadServiceTag | EVT_OEMDownloadServiceTag |  |
| CommCycle | EVT_CommCycle |  |
| StateChanged | EVT_StateChanged |  |
| Exception | EVT_CmpApp_Exception |  |
| Fuse_ttyRuntime2 | 16#10010002 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime3 | 16#10010003 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime4 | 16#10010004 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime5 | 16#10010005 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime6 | 16#10010006 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime7 | 16#10010007 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime8 | 16#10010008 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime9 | 16#10010009 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime11 | 16#1001000A | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime12 | 16#1001000B | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime13 | 16#1001000C | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime14 | 16#1001000D | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime15 | 16#1001000E | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime16 | 16#1001000F | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime17 | 16#10010010 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime18 | 16#10010011 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime19 | 16#10010012 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime20 | 16#10010013 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime21 | 16#10010014 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime22 | 16#10010015 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime23 | 16#10010016 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime24 | 16#10010017 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime25 | 16#10010018 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime26 | 16#10010019 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime27 | 16#1001001A | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime28 | 16#1001001B | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime29 | 16#1001001C | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime30 | 16#1001001D | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime31 | 16#1001001E | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime32 | 16#1001001F | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime33 | 16#10010020 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime34 | 16#10010021 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime35 | 16#10010022 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime36 | 16#10010023 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime37 | 16#10010024 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime38 | 16#10010025 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime39 | 16#10010026 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime40 | 16#10010027 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime41 | 16#10010028 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime42 | 16#10010029 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime43 | 16#1001002A | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime44 | 16#1001002B | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime45 | 16#1001002C | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime46 | 16#1001002D | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime47 | 16#1001002E | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime48 | 16#1001002F | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime49 | 16#10010030 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime50 | 16#10010031 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime51 | 16#10010032 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime52 | 16#10010033 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime53 | 16#10010034 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime54 | 16#10010035 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime55 | 16#10010036 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime56 | 16#10010037 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime57 | 16#10010038 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime58 | 16#10010039 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime59 | 16#1001003A | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime60 | 16#1001003B | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime61 | 16#1001003C | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime62 | 16#1001003D | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime63 | 16#1001003F | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime64 | 16#10010040 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |
| Fuse_ttyRuntime65 | 16#10010041 | WagoAppEvent.eWagoEventClass.EVTCLASS_FUSE + EventNumber |

A collection of all known events.

This enumeration is a collection of all known events in a WAGO environment. It consists mainly of established events from ‘CmpApp’ but it is not guarateed to be restricted to them and may also contain WAGO-specific events either additional or as substitute.

This type serves as input either directly for posting events or indirectly for catching events. In the latter case this types is contained in the typWagoEventInfo structure, which is passed to the event catchers.

Caveat: Do not confuse this type with eWagoEventParameterID or unWagoEventParameter . These are other components of typWagoEventInfo but they are not strictly related to eWagoEventID (although there are several conicidences).

Note: For technical reasons the enumeration contains a symbol maximum . This symbol is used internally and represents an event identification which is not valid. When used as input this should result to an unknown event.

InOut: A collection of all known events. This enumeration is a collection of all known events in a WAGO environment. It consists mainly of established events from ‘CmpApp’ but it is not guarateed to be restricted to them and may also contain WAGO-specific events either additional or as substitute. This type serves as input either directly for posting events or indirectly for catching events. In the latter case this types is contained in the typWagoEventInfo structure, which is passed to the event catchers. Caveat: Do not confuse this type with eWagoEventParameterID or unWagoEventParameter . These are other components of typWagoEventInfo but they are not strictly related to eWagoEventID (although there are several conicidences). Note: For technical reasons the enumeration contains a symbol maximum . This symbol is used internally and represents an event identification which is not valid. When used as input this should result to an unknown event.

## eWagoEventParameterID (ENUM)


| Name | Initial |
| --- | --- |
| CmpApp | EVTPARAMID_CmpApp |
| CmpAppConfig | 101 |
| CmpAppReset | 102 |
| CmpAppStop | EVTPARAMID_CmpAppStop |
| CmpAppDenyStart | EVTPARAMID_CmpAppDenyStart |
| CmpAppDenyStop | EVTPARAMID_CmpAppDenyStop |
| CmpAppAllBootAppsLoaded | EVTPARAMID_CmpAppAllBootAppsLoaded |
| CmpAppDenyLoadBootproject | EVTPARAMID_CmpAppDenyLoadBootproject |
| CmpAppPrepareLoadBootproject | EVTPARAMID_CmpAppPrepareLoadBootproject |
| CmpAppException | EVTPARAMID_CmpAppException |
| CmpAppRegisterBootproject | EVTPARAMID_CmpAppRegisterBootproject |
| CmpAppOperatingStateChanged | EVTPARAMID_CmpAppOperatingStateChanged |
| CmpAppSourceDownload | EVTPARAMID_CmpAppSourceDownload |
| CmpAppComm | EVTPARAMID_CmpAppComm |
| CmpAppDeny | EVTPARAMID_CmpAppDeny |
| CmpAppDenyDelete | EVTPARAMID_CmpAppDenyDelete |
| CmpAppOEMServiceTag | EVTPARAMID_CmpAppOEMServiceTag |
| CmpAppCommCycle | 23 |

Identifies, which component of unWagoEventParameter is used.

The names of the components of this enumeration match the name of corresponding components in the unWagoEventParameter union. The typical use of this type is to define a variable in combination with that union, where the variable of type eWagoEventParameterID selects, which component of the union applies.

Note: Wherever posssible, the values of this enumeration do carry the values of corresponding internal parameter IDs of the system. But in some cases this is impossible due to ambiguities. In the latter case the values are assigned to other arbitrarily chosen numbers. Anyway: According to its purpuse, this enumeration shoud never be used by the (arbitrarily assigned) values, but it should always be used by its unambiguous enumeration symbol.

InOut: Identifies, which component of unWagoEventParameter is used. The names of the components of this enumeration match the name of corresponding components in the unWagoEventParameter union. The typical use of this type is to define a variable in combination with that union, where the variable of type eWagoEventParameterID selects, which component of the union applies. Note: Wherever posssible, the values of this enumeration do carry the values of corresponding internal parameter IDs of the system. But in some cases this is impossible due to ambiguities. In the latter case the values are assigned to other arbitrarily chosen numbers. Anyway: According to its purpuse, this enumeration shoud never be used by the (arbitrarily assigned) values, but it should always be used by its unambiguous enumeration symbol.

## eWagoEventStopReason (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Unknown | APP_STOP_REASON_UNKNOWN | Unknown reason for stop |
| Shutdown | APP_STOP_REASON_SHUTDOWN | Stop due to shutdown of the PLC |
| Reset | APP_STOP_REASON_RESET | Stop due to a reset of the PLC |
| Exception | APP_STOP_REASON_EXCEPTION | Stop as a result of an exception |
| User | APP_STOP_REASON_USER | Stopped by interaction of the user |
| IecProram | APP_STOP_REASON_IECPROGRAM | Stopped from an IEC program |
| Delete | APP_STOP_REASON_DELETE | Stopped because application is deleted |

Reasons for stopping.

This enumeration is part of some parameter descriptions which are used in unWagoEventParameter and which are related to stopping applications. For those events, this enumeration gives a hint about why the application is to be stopped, so the stopping could be denied for user defined reasons, if applicable.

InOut: Reasons for stopping. This enumeration is part of some parameter descriptions which are used in unWagoEventParameter and which are related to stopping applications. For those events, this enumeration gives a hint about why the application is to be stopped, so the stopping could be denied for user defined reasons, if applicable.

## typWagoParam_01_CmpApp (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |

## typWagoParam_01a_CmpAppConfig (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |
| psConfigApplication | POINTER TO STRING | name of the application |  |

## typWagoParam_02_CmpAppStop (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |
| eStopReason | eWagoEventStopReason | Reason why the stop is issued. |  |

## typWagoParam_04_CmpAppDenyStop (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |
| eStopReason | eWagoEventStopReason | Reason why the stop is issued. |  |

typWagoParam_04_CmpAppDenyStop

InOut: typWagoParam_04_CmpAppDenyStop Note: When comparing this with a corresponding event from CmpApp you will find an additional pointer to a return parameter udiDeny there which is passed via the input structure. For this structure, however, the return information ss passed as a return value of the event catching function and thus intentionally does not appear in this input structure.

## typWagoParam_05_Cmp_AllBootAppsLoaded (STRUCT)


| Name | Type |
| --- | --- |
| diTotalBootApps | DINT |
| diSuccessfullyLoadedBootApps | DINT |

## typWagoParam_06_CmpAppNameDenyLoadBootproject (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| psAppName | POINTER TO STRING | Name of the application | typWagoParam_Base_AppName |

typWagoParam_06_CmpAppNameDenyLoadBootproject

InOut: typWagoParam_06_CmpAppNameDenyLoadBootproject Note: When comparing this with a corresponding event from CmpApp you will find an additional pointer to a return parameter udiDeny there which is passed via the input structure. For this structure, however, the return information ss passed as a return value of the event catching function and thus intentionally does not appear in this input structure.

## typWagoParam_07_CmpAppNamePrepareLoadBootproject (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| psAppName | POINTER TO STRING | Name of the application | typWagoParam_Base_AppName |

## typWagoParam_08_CmpAppException (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |
| hIecTask | RTS_IEC_HANDLE |  |  |
| udiException | UDINT |  |  |

## typWagoParam_09_CmpAppNameRegisterBootproject (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| psAppName | POINTER TO STRING | Name of the application | typWagoParam_Base_AppName |

## typWagoParam_10_CmpAppOperatingStateChanged (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |
| udiPrevOpState | UDINT |  |  |

## typWagoParam_11_CmpAppNameSourceDownload (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| psAppName | POINTER TO STRING | Name of the application | typWagoParam_Base_AppName |
| usiBegin | USINT |  |  |

## typWagoParam_12_CmpAppComm (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |
| udiSessionId | UDINT |  |  |

## typWagoParam_13_CmpAppDeny (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |

typWagoParam_13_CmpAppDeny

InOut: typWagoParam_13_CmpAppDeny Note: When comparing this with a corresponding event from CmpApp you will find an additional pointer to a return parameter udiDeny there which is passed via the input structure. For this structure, however, the return information ss passed as a return value of the event catching function and thus intentionally does not appear in this input structure.

## typWagoParam_14_CmpAppDenyDelete (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |
| udiShutDown | UDINT |  |  |

## typWagoParam_15_CmpAppOEMServiceTag (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |
| udiChannelId | UDINT |  |  |
| udiTopLevelTag | UDINT |  |  |
| udiHeaderTag | UDINT |  |  |
| udiReader | UDINT |  |  |
| udiWriter | UDINT |  |  |

typWagoParam_15_CmpAppOEMServiceTag

InOut: typWagoParam_15_CmpAppOEMServiceTag Note: When comparing this with a corresponding event from CmpApp you will find an additional pointer to a return parameter udiDeny there which is passed via the input structure. For this structure, however, the return information ss passed as a return value of the event catching function and thus intentionally does not appear in this input structure.

## typWagoParam_23_Cmp_CommCycle (STRUCT)


| Name | Type |
| --- | --- |
| ulParam1 | XWORD |
| ulParam2 | XWORD |

## typWagoParam_xx_CmpAppStateChanged (STRUCT)


| Name | Type | Comment | Inherited from |
| --- | --- | --- | --- |
| pApp | POINTER TO APPLICATION | system structure | typWagoParam_Base_Application |
| udiPrevState | UDINT |  |  |

## unWagoEventParameter (UNION)


| Name | Type |
| --- | --- |
| CmpApp | typWagoParam_01_CmpApp |
| CmpAppConfig | typWagoParam_01a_CmpAppConfig |
| CmpAppReset | typWagoParam_01b_CmpAppReset |
| CmpAppStop | typWagoParam_02_CmpAppStop |
| CmpAppDenyStart | typWagoParam_03_CmpAppDenyStart |
| CmpAppDenyStop | typWagoParam_04_CmpAppDenyStop |
| Cmp_AllBootAppsLoaded | typWagoParam_05_Cmp_AllBootAppsLoaded |
| CmpAppNameDenyLoadBootproject | typWagoParam_06_CmpAppNameDenyLoadBootproject |
| CmpAppNamePrepareLoadBootproject | typWagoParam_07_CmpAppNamePrepareLoadBootproject |
| CmpAppException | typWagoParam_08_CmpAppException |
| CmpAppNameRegisterBootproject | typWagoParam_09_CmpAppNameRegisterBootproject |
| CmpAppOperatingStateChanged | typWagoParam_10_CmpAppOperatingStateChanged |
| CmpAppNameSourceDownload | typWagoParam_11_CmpAppNameSourceDownload |
| CmpAppComm | typWagoParam_12_CmpAppComm |
| CmpAppDeny | typWagoParam_13_CmpAppDeny |
| CmpAppDenyDelete | typWagoParam_14_CmpAppDenyDelete |
| CmpAppOEMServiceTag | typWagoParam_15_CmpAppOEMServiceTag |
| CmpAppStateChanged | typWagoParam_xx_CmpAppStateChanged |
| Cmp_CommCycle | typWagoParam_23_Cmp_CommCycle |

A union combining the various parameter formats.

Which format applies is defined by a ParameterID of the type eWagoEventParameterID , which is passed in a separate variable.

The symbolic name of the enumeration is the same as the symbolic name of the union component. E.g.: eWagoEventParameterID.CmpAppConfig indicates that the component unWagoEventParameter.CmpAppConfig applies.

InOut: A union combining the various parameter formats. Which format applies is defined by a ParameterID of the type eWagoEventParameterID , which is passed in a separate variable. The symbolic name of the enumeration is the same as the symbolic name of the union component. E.g.: eWagoEventParameterID.CmpAppConfig indicates that the component unWagoEventParameter.CmpAppConfig applies.