# WagoSysVisuBACnet v2.0.1.8 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysVisuBACnet
- **Version:** 2.0.1.8
- **Categories:** WAGO LayerView|Sys; WAGO FunctionalView|Visu; Application
- **Namespace:** WagoSysVisuBACnet
- **Author:** WAGO / u01045
- **Placeholder:** WagoSysVisuBACnet

### Description ¶


This document is automatically generated.

This library provides visualizations to bacnet objects on iec level.

This document is automatically generated. This library provides visualizations to bacnet objects on iec level.

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Base Components Base - BaseTypes Internal Components - 10 Common Internal - 90 Internal - Dialog Internal Action Command - Dialog Internal Action Text - Internal - Internal Global Variable Lists Other Components - ()Helper - ()Helper - 05 Template - 10 Analog Objects - 10 Common - 10 Event / Alarm List - 12 BinaryObjects - 14 Multistate Objects - 20 Calendar Objects - 22 Scheduler Objects - ... and 107 more

### Indices and tables ¶


Based on WagoSysVisuBACnet.library, last modified 20.09.2024, 21:17:27. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysVisuBACnet.library, last modified 20.09.2024, 21:17:27. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysVisuBACnet Library Documentation


| Company: | WAGO |
| Title: | WagoSysVisuBACnet |
| Version: | 2.0.1.8 |
| Categories: | WAGO LayerView\|Sys; WAGO FunctionalView\|Visu; Application |
| Namespace: | WagoSysVisuBACnet |
| Author: | WAGO / u01045 |
| Placeholder: | WagoSysVisuBACnet |

### Description


This document is automatically generated.

This library provides visualizations to bacnet objects on iec level.

This document is automatically generated. This library provides visualizations to bacnet objects on iec level.

### Contents:


- 30 Visualizations 05 Template - 10 Event / Alarm List - 30 Calendar - 40 Scheduler 75 TextList - Internal - txtDataType (Text List) - txtDayOfMonth (Text List) - txtDayOfWeek (Text List) - txtDialogCalendarEntry (Text List) - txtDialogDailyScheduleEntry (Text List) - txtEntryType (Text List) - txtExceptionSchedule (Text List) - txtMonth (Text List) - txtObjectPropertyReferences (Text List) - txtObjectTypes (Text List) - txtPeriodType (Text List) - txtPropertyId (Text List) - txtWeekOfMonth (Text List) 90 Internal - 10 Common Internal - 30 Visu 1280/0800 - 70 Images GlobalTextList (Text List) ParameterVisuBACnet (PARAMS) VersionHistory (GVL)

### Indices and tables


Based on WagoSysVisuBACnet.library, last modified 20.09.2024, 21:17:27. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysVisuBACnet.library, last modified 20.09.2024, 21:17:27. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysVisuBACnet.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 20.09.2024, 21:18:13 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 20.09.2024, 21:17:27 |
| Description | string | See: Description |
| Copyright | © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved |
| Author | WAGO / u01045 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysVisuBACnet |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysVisuBACnet |
| DefaultNamespace | WagoSysVisuBACnet |
| Version | version | 2.0.1.8 |
| Title | string | WagoSysVisuBACnet |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; WAGO FunctionalView\|Visu; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: True | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False PublishSymbolsInContainer: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpApp Library Identification : Placeholder: CmpApp Default Resolution: CmpApp, * (System) Namespace: CmpApp Library Properties : CmpBitmapPool Library Identification : Placeholder: CmpBitmapPool Default Resolution: CmpBitmapPool, * (System) Namespace: CmpBitmapPool Library Properties : CmpIecTask Library Identification : Placeholder: CmpIecTask Default Resolution: CmpIecTask, * (System) Namespace: CmpIecTask Library Properties : Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : StringUtils Library Identification : Placeholder: StringUtils Default Resolution: StringUtils, * (System) Namespace: Stu Library Properties : SysCpuHandling Library Identification : Placeholder: SysCpuHandling Default Resolution: SysCpuHandling, * (System) Namespace: SysCpuHandling Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : Util Library Identification : Placeholder: Util Default Resolution: Util, * (System) Namespace: Util Library Properties : Library Parameter : Parameter: IBLOCKSIZE = 22800 Visu Utils Library Identification : Placeholder: VisuUtils Default Resolution: Visu Utils, * (System) Namespace: VU Library Properties : VisuDialogs Library Identification : Placeholder: VisuDialogs Default Resolution: VisuDialogs, * (System) Namespace: VisuDialogs Library Properties : VisuElem3DPath Library Identification : Placeholder: System_VisuElem3DPath Default Resolution: VisuElem3DPath, 3.5.16.30 (System) Namespace: VisuElem3DPath Library Properties : Library Parameter : Parameter: GC_POINTS_PER_POLYGON = 100 VisuElemBase Library Identification : Placeholder: System_VisuElemBase Default Resolution: VisuElemBase, * (System) Namespace: VisuElemBase Library Properties : VisuElemCamDisplayer Library Identification : Placeholder: System_VisuElemCamDisplayer Default Resolution: VisuElemCamDisplayer, 3.5.16.30 (System) Namespace: VisuElemCamDisplayer Library Properties : Library Parameter : Parameter: GC_POINTS_PER_CAM = 100 VisuElemMeter Library Identification : Placeholder: System_VisuElemMeter Default Resolution: VisuElemMeter, 3.5.16.30 (System) Namespace: VisuElemMeter Library Properties : VisuElemTextEditor Library Identification : Placeholder: System_VisuElemTextEditor Default Resolution: VisuElemTextEditor, 3.5.16.30 (System) Namespace: VisuElemTextEditor Library Properties : VisuElemTrace Library Identification : Placeholder: System_VisuElemTrace Default Resolution: VisuElemTrace, 3.5.16.30 (System) Namespace: VisuElemTrace Library Properties : VisuElemXYChart Library Identification : Placeholder: System_VisuElemXYChart Default Resolution: VisuElemXYChart, 3.5.16.30 (System) Namespace: VisuElemXYChart Library Properties : VisuElems Library Identification : Placeholder: System_VisuElems Default Resolution: VisuElems, 3.5.16.30 (System) Namespace: VisuElems Library Properties : VisuElemsAlarm Library Identification : Placeholder: System_VisuElemsAlarm Default Resolution: VisuElemsAlarm, 3.5.16.30 (System) Namespace: VisuElemsAlarm Library Properties : VisuElemsDateTime Library Identification : Placeholder: System_VisuElemsDateTime Default Resolution: VisuElemsDateTime, 3.5.16.30 (System) Namespace: VisuElemsDateTime Library Properties : VisuElemsSpecialControls Library Identification : Placeholder: System_VisuElemsSpecialControls Default Resolution: VisuElemsSpecialControls, 3.5.16.30 (System) Namespace: VisuElemsSpecialControls Library Properties : VisuElemsWinControls Library Identification : Placeholder: System_VisuElemsWinControls Default Resolution: VisuElemsWinControls, 3.5.16.30 (System) Namespace: VisuElemsWinControls Library Properties : VisuInputs Library Identification : Placeholder: system_visuinputs Default Resolution: VisuInputs, 3.5.16.30 (System) Namespace: visuinputs Library Properties : VisuNativeControl Library Identification : Placeholder: System_VisuNativeControl Default Resolution: VisuNativeControl, 3.5.16.0 (System) Namespace: VisuNativeControl Library Properties : VisuSymbols Library Identification : Name: VisuSymbols Version: newest Company: System Namespace: VisuSymbols Library Properties : WagoAppString Library Identification : Placeholder: WagoAppString Default Resolution: WagoAppString, * (WAGO) Namespace: WagoAppString Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesBACnet Library Identification : Placeholder: WagoTypesBACnet Default Resolution: WagoTypesBACnet, * (WAGO) Namespace: WagoTypesBACnet Library Properties : WagoVisuIconsMaterialDesign Library Identification : Placeholder: WagoVisuIconsMaterialDesign Default Resolution: WagoVisuIconsMaterialDesign, * (WAGO) Namespace: WagoVisuIconsMaterialDesign Library Properties :

### Base Components


## Base ¶


## BaseTypes ¶


### Internal Components


## 10 Common Internal


- Sub Command Action Action Line - ActionCommandLine - Dialog Internal Action Command - Dialog Internal Action Text UpdateGroup - Sub

## 90 Internal


- 10 Common Internal Sub Command Action Action Line - ActionCommandLine - Dialog Internal Action Command - Dialog Internal Action Text UpdateGroup - Sub 30 Visu 1280/0800 - 10 Common - Internal Base Helper DataTypes - BaseTypes - Visu Prio Array BitString - Bool - Dint - LReal - Real - Udint Objects - 10 Analog Objects Input - Output - Value 12 BinaryObjects - Input - Output - Value 14 Multistate Objects - Input ()Helper Output Value 20 Calendar Objects 22 Scheduler Objects - ()Helper 30 Loop Objects 32 Integer Value Objects 34 Large Anlog Value Objects 36 Bit String Value - Sub 40 Command 42 Device 44 Trend Log 45 Trend Log Multiple 46 Event Enrollment 48 Event Log 50 Notification Class tpl - Filter - Header - ObjetView - Table 70 Images - BACnetIcons (Image Pool) - UpdateGroups (Image Pool)

## Dialog Internal Action Command ¶


## Dialog Internal Action Text ¶


## Internal


- Device txtSystemStatus (Text List) Dialogs - Title Command txtDialogObjectActionCommand (Text List) - txtDialogObjectActionText (Text List) txtDialogObjectTypes (Text List) Scheduler - txtScheduler (Text List) txtAction (Text List) txtBinaryPrio (Text List) txtBtLedStatus (Text List) txtDataTypeClientCovInc (Text List) txtEventLogRecordType (Text List) txtEventState (Text List) txtEventType (Text List) txtLoggingType (Text List) txtLoggingTypeMultiple (Text List) txtLoopMode (Text List) txtNotifyType (Text List) txtPrioLevel (Text List) txtReliabilityType (Text List) txtUnits (Text List) txtUnitsSymbole (Text List)

## Internal


- Base Helper DataTypes - BaseTypes - Visu Prio Array BitString - Bool - Dint - LReal - Real - Udint Objects - 10 Analog Objects Input - Output - Value 12 BinaryObjects - Input - Output - Value 14 Multistate Objects - Input ()Helper Output Value 20 Calendar Objects 22 Scheduler Objects - ()Helper 30 Loop Objects 32 Integer Value Objects 34 Large Anlog Value Objects 36 Bit String Value - Sub 40 Command 42 Device 44 Trend Log 45 Trend Log Multiple 46 Event Enrollment 48 Event Log 50 Notification Class tpl - Filter - Header - ObjetView - Table

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 08.08.2024 | 2.0.1.8 | u0103719 | fix C0297 compile error stack overflow (context: PFC 300) |
| 11.07.2024 | 2.0.1.7 | u0103719 | embedded missing images (context: UpdateGroups) |
| 08.04.2024 | 2.0.1.6 | u0103719 | rename path of namespace (context: VisuElems) |
| 20.02.2024 | 2.0.1.5 | u0103719 | modified environment (context: SP16 Patch 3) |
| 18.01.2024 | 2.0.1.4 | u0103719 | change scaling type |
| 17.01.2024 | 2.0.1.3 | u0103719 | add search filter with placeholder (context: FbFilterObjectList) |
| 16.01.2024 | 2.0.1.2 | u0103719 | add new parameter TASK_PRIO_BACNET_DAEMON_FREEWHEELING ->Ctrlx need adjustment |
| 15.01.2024 | 2.0.1.1 | u0103719 | activated sort deamon, modified unit (context: txtUnitsSymbole) |
| 10.01.2024 | 2.0.1.0 | u0103719 | WAT36093: add search filter for objectname (context:VisuBACnetTableView,VisuBACnetObjectView) |
| 20.04.2023 | 2.0.0.0 | u010545 | modifications for CDS |
| 17.08.2022 | 1.0.10.2 | u010545 | bugfix visible groups |
| 04.08.2022 | 1.0.10.1 | u010545 | cleanup placeholder |
| 19.07.2022 | 1.0.10.0 | u010545 | first version for FW22 -> SP17 |
| 12.07.2022 | 1.0.9.4 | u010545 | bugfix |
| 29.06.2022 | 1.0.9.3 | u013972 | Resolve placeholder for SP17 |
| 11.05.2022 | 1.0.9.2 | u010545 | Device removed for correct resolve placeholder at SP17 |
| 27.04.2022 | 1.0.9.1 | u010545 | udiUpdateInterval modified for Rev22 (setter) |
| 13.04.2022 | 1.0.9.0 | u010545 | Task handling modified / bugfixes |
| 19.01.2022 | 1.0.8.0 | u010545 | first release Rev.22 |
| 11.11.2021 | 1.0.5.6 | u010545 | xLoopEnable moved from small to R22 medium |
| 07.10.2021 | 1.0.5.5 | u010545 | development |
| 05.10.2021 | 1.0.5.4 | u010545 | compatibility Rev14 <-> Rev22 |
| 14.06.2021 | 1.0.5.3 | u010545 | bugfix AV_large dtLastCommandTime |
| 03.05.2021 | 1.0.5.2 | u010545 | type cast enumerations & development rev. 22 |
| 30.04.2021 | 1.0.4.11 | u010545 | bugfix type cast enumerations |
| 22.03.2021 | 1.0.4.10 | u010545 | Namespaces for 3.5.16 |
| 16.10.2020 | 1.0.4.9 | u010545 | Bugfixes / Workarounds Textlist |
| 11.05.2020 | 1.0.4.8 | u010545 | WAT31671 Optional Parameter |
| 14.02.2020 | 1.0.4.7 | u010545 | development |
| 03.02.2020 | 1.0.4.6 | u010545 | I_BACnetEventList -> udiAcknowledged |
| 29.01.2020 | 1.0.4.5 | u010545 | Notification Class -> small / medium |
| 15.01.2020 | 1.0.4.4 | u010545 | development |
| 15.01.2020 | 1.0.4.3 | u010545 | alarm / event list -> TC01 |
| 17.12.2019 | 1.0.4.2 | u010545 | change to 1280x800 |
| 02.12.2019 | 1.0.4.1 | u010545 | development |
| 26.11.2019 | 1.0.4.0 | u010545 | bugfix Prio Arrays |
| 15.11.2019 | 1.0.3.0 | u010545 | additional objects |
| 22.07.2019 | 1.0.1.2 | u010545 | Visu switched form intern to public |
| 09.07.2019 | 1.0.1.1 | u010545 | WAT 30189 |
| 03.07.2019 | 1.0.1.0 | u010545 | first version R2 |
|  |  |  |  |
| 01.07.2019 | 1.0.0.3 | u010545 | WAT 30168 / 30098 |
| 01.07.2019 | 1.0.0.2 | u010545 | Test VisuSymbolLibrary |
| 13.06.2019 | 1.0.0.1 | u010545 | Development |
| 06.06.2019 | 1.0.0.0 | u010545 | Release |

WagoSysVisuBACnetConfig

Release Note

This library provides visualizations for bacnet objects

WagoSysVisuBACnetConfig Release Note This library provides visualizations for bacnet objects

### Other Components


## ()Helper ¶


## ()Helper ¶


## 05 Template ¶


## 10 Analog Objects ¶


- Input - Output - Value

## 10 Common ¶


## 10 Event / Alarm List ¶


## 12 BinaryObjects ¶


- Input - Output - Value

## 14 Multistate Objects


- Input ()Helper Output Value

## 20 Calendar Objects ¶


## 22 Scheduler Objects ¶


## 30 Calendar ¶


- Dialogs - Sub Visu Calendar Entry

## 30 Loop Objects ¶


## 30 Visu 1280/0800


- 10 Common - Internal Base Helper DataTypes - BaseTypes - Visu Prio Array BitString - Bool - Dint - LReal - Real - Udint Objects - 10 Analog Objects Input - Output - Value 12 BinaryObjects - Input - Output - Value 14 Multistate Objects - Input ()Helper Output Value 20 Calendar Objects 22 Scheduler Objects - ()Helper 30 Loop Objects 32 Integer Value Objects 34 Large Anlog Value Objects 36 Bit String Value - Sub 40 Command 42 Device 44 Trend Log 45 Trend Log Multiple 46 Event Enrollment 48 Event Log 50 Notification Class tpl - Filter - Header - ObjetView - Table

## 30 Visualizations


- 05 Template - 10 Event / Alarm List Dialogs 30 Calendar - Dialogs - Sub Visu Calendar Entry 40 Scheduler - IEffectivePeriod Dialogs IExceptionSchedule - Dialogs (hidden) - Sub Visu Calendar Entry IListOfObjectPropertyReferences - Dialogs - Sub Visu IWeeklySchedule - Dialogs - Sub Visu Tab

## 32 Integer Value Objects ¶


## 34 Large Anlog Value Objects ¶


## 36 Bit String Value ¶


## 40 Command ¶


## 40 Scheduler


- IEffectivePeriod Dialogs IExceptionSchedule - Dialogs (hidden) - Sub Visu Calendar Entry IListOfObjectPropertyReferences - Dialogs - Sub Visu IWeeklySchedule - Dialogs - Sub Visu Tab

## 42 Device ¶


## 44 Trend Log ¶


## 45 Trend Log Multiple ¶


## 46 Event Enrollment ¶


## 48 Event Log ¶


## 50 Notification Class ¶


## 70 Images


- BACnetIcons (Image Pool) - UpdateGroups (Image Pool)

## 75 TextList


- Internal Device txtSystemStatus (Text List) Dialogs - Title Command txtDialogObjectActionCommand (Text List) - txtDialogObjectActionText (Text List) txtDialogObjectTypes (Text List) Scheduler - txtScheduler (Text List) txtAction (Text List) txtBinaryPrio (Text List) txtBtLedStatus (Text List) txtDataTypeClientCovInc (Text List) txtEventLogRecordType (Text List) txtEventState (Text List) txtEventType (Text List) txtLoggingType (Text List) txtLoggingTypeMultiple (Text List) txtLoopMode (Text List) txtNotifyType (Text List) txtPrioLevel (Text List) txtReliabilityType (Text List) txtUnits (Text List) txtUnitsSymbole (Text List) txtDataType (Text List) txtDayOfMonth (Text List) txtDayOfWeek (Text List) txtDialogCalendarEntry (Text List) txtDialogDailyScheduleEntry (Text List) txtEntryType (Text List) txtExceptionSchedule (Text List) txtMonth (Text List) txtObjectPropertyReferences (Text List) txtObjectTypes (Text List) txtPeriodType (Text List) txtPropertyId (Text List) txtWeekOfMonth (Text List)

## Action


- Action Line - ActionCommandLine - Dialog Internal Action Command - Dialog Internal Action Text

## Action Line ¶


## ActionCommandLine ¶


## BACnetIcons (Image Pool)


| ID | File name | Image | Link type |
| --- | --- | --- | --- |
| 4 | Status_Error.png |  | Embedded |
| 2 | Status_Warning.png |  | Embedded |
| 1 | Status_Info.png |  | Embedded |
| 5 | Status_Help.png |  | Embedded |
| 3 | Status_Ok.png |  | Embedded |
| 9 | Delete.png |  | Embedded |
| 100 | CheckboxChecked_Def.svg |  | Embedded |
| 101 | CheckboxUnchecked_Def.svg |  | Embedded |
| 900 | dp_datapoint.png |  | Embedded |
| 901 | dp_datapoint_dynamic_create.png |  | Embedded |
| 1502 | Write_at_Once.png |  | Embedded |
| WagoBACnetIcon | WagoBACnetIcon.png |  | Embedded |
| 10001 | error_02.png |  | Embedded |
| 10000 | ok_green_04.png |  | Embedded |
| 10002 | error_03.png |  | Embedded |
| WAGO-Icon-152 | WAGO-Icon-152.png |  | Embedded |
| 65535 | No_Image.png |  | Embedded |
| Loupe | Loupe.png |  | Embedded |

## BitString ¶


## Bool ¶


## Calendar Entry ¶


## Calendar Entry ¶


## Command


- txtDialogObjectActionCommand (Text List) - txtDialogObjectActionText (Text List)

## DataTypes


- BaseTypes - Visu Prio Array BitString - Bool - Dint - LReal - Real - Udint

## Device ¶


- txtSystemStatus (Text List)

## Dialogs


- Title Command txtDialogObjectActionCommand (Text List) - txtDialogObjectActionText (Text List) txtDialogObjectTypes (Text List)

## Dialogs ¶


## Dialogs ¶


## Dialogs ¶


## Dialogs ¶


## Dialogs ¶


## Dialogs (hidden) ¶


## Dint ¶


## Filter ¶


## GlobalTextList (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 2171 | `` %s`` |  |
| 1441 | `` %s`` |  |
| 2783 | %.8f |  |
| 2251 | %0.2d |  |
| 2113 | %0.3d |  |
| 424 | %0.4d |  |
| 1997 | %8.8f |  |
| 870 | %d |  |
| 934 | %f |  |
| 635 | %s |  |
| 5528 | %t[dd.MM.yyyy / HH:mm:ss] |  |
| 2096 | %t[HH:mm:ss.ms] |  |
| 2323 | %t[HH:mm:ss] |  |
| 39 | (0) AckedTransition |  |
| 396 | (032) Effective Period |  |
| 962 | (038) Exception Schedule |  |
| 4111 | (054) List of Property References |  |
| 164 | (103) Reliability |  |
| 857 | (104) RelinquishDefault |  |
| 725 | (106) Resolution |  |
| 2676 | (108) SetPoint |  |
| 2074 | (110) Actual StateText |  |
| 403 | (111) StatusFlags |  |
| 1573 | (112) System Status |  |
| 871 | (113) TimeDelay |  |
| 1838 | (114) TimeOfActiveTimeReset |  |
| 52 | (115) TimeOfStateCountReset |  |
| 93 | (117) Units |  |
| 914 | (118) UpdateInterval |  |
| 1675 | (123) Weekly Schedule |  |
| 4769 | (126) BufferSize |  |
| 598 | (127) ClientCovIncrement |  |
| 3665 | (128) CovResubscr.Interval |  |
| 550 | (130) TimeStamp |  |
| 4067 | (133) Enable |  |
| 1340 | (134) LogInterval |  |
| 209 | (137) NotificationThreshold |  |
| 1634 | (14) Bias |  |
| 5058 | (140) RecordsSinceNotification |  |
| 1651 | (141) Record Count |  |
| 3944 | (142) StartTime |  |
| 159 | (143) StopTime |  |
| 4396 | (144) StopWhenFull |  |
| 2389 | (145) Total Record Count |  |
| 3420 | (15) AckRequired |  |
| 1364 | (15) ChangeOfState_Count |  |
| 128 | (16) ChangeOfState_Time |  |
| 922 | (17) NotificationClass |  |
| 477 | (173) LastNotifyRecord |  |
| 1726 | (174) Schedule Default |  |
| 4874 | (193) AlignIntervals |  |
| 378 | (195) IntervalOffset |  |
| 4196 | (197) LoggingType |  |
| 2890 | (2) Action |  |
| 4484 | (2) Action / (3) Action Text |  |
| 287 | (20) ControlledVariableUnits |  |
| 4436 | (203) Time of Device Restart |  |
| 3759 | (205) Trigger |  |
| 4524 | (208) NodeType |  |
| 1913 | (21) ControlledVariableValue |  |
| 685 | (22) CoV_Increment |  |
| 818 | (25) DeadBand |  |
| 3542 | (26) DerivativeConstant |  |
| 2058 | (27) DerivativeConstantUnits |  |
| 211 | (28) Description |  |
| 4382 | (3) Action Text |  |
| 316 | (31) DeviceType |  |
| 1242 | (32) Effective Period |  |
| 1790 | (33) ElapsedActiveTime |  |
| 2500 | (34) ErrorLimit |  |
| 595 | (342) Bit Mask |  |
| 1799 | (343) Bit Text |  |
| 86 | (35) EventEnable |  |
| 965 | (351) EventMessageTexts |  |
| 175 | (352) EventMessageTextsConfig |  |
| 503 | (353) EventDetectionEnable |  |
| 861 | (354) EventAlgorithmInhibit |  |
| 536 | (356) TimeDelayNormal |  |
| 5130 | (357) ReliabilityEval.Inhibit |  |
| 377 | (36) EventState |  |
| 2284 | (38) Exception Schedule |  |
| 1207 | (39) FaultValues |  |
| 916 | (4) ActiveText |  |
| 1465 | (40) FeedbackValue |  |
| 3636 | (44) Firmware Revision |  |
| 426 | (45) HighLimit |  |
| 47 | (46) InactiveText |  |
| 723 | (47) InProcess |  |
| 289 | (49) IntegralConstant |  |
| 2560 | (50) IntegralConstantUnits |  |
| 3077 | (518) Time Before Operation |  |
| 110 | (52) LimtEnable |  |
| 6133 | (523) LoopEnable |  |
| 2237 | (54) List of Property References |  |
| 1715 | (56) Local Date |  |
| 2724 | (57) Local Time |  |
| 4106 | (58) Location |  |
| 99 | (59) LowLimit |  |
| 71 | (6) AlarmValue |  |
| 393 | (61) MaxOutput |  |
| 318 | (65) MaxPresValue |  |
| 954 | (66) MinimumOffTime |  |
| 849 | (67) MinimumOnTime |  |
| 985 | (68) MinOutput |  |
| 827 | (69) MinPresValue |  |
| 1503 | (7) AlarmValues |  |
| 2187 | (70) Model Name |  |
| 605 | (72) NotifyType |  |
| 537 | (74) NumberOfStates |  |
| 298 | (75) ObjectIdentifier |  |
| 640 | (77) ObjectName |  |
| 430 | (81) OutOfService |  |
| 308 | (82) OutputUnits |  |
| 1428 | (84) Polarity |  |
| 982 | (85) PresentValue |  |
| 944 | (86) Priority |  |
| 212 | (87) Priority Array |  |
| 1132 | (88) Priority for Writing |  |
| 1595 | (88) PriorityForWriting |  |
| 1814 | (9) AllWritesSuccessful |  |
| 2412 | (93) ProportionalConstant |  |
| 105 | (94) ProportionalConstantUnits |  |
| 1066 | (CS) isCreated |  |
| 4726 | --- |  |
| 2714 | 0x%0.16llX |  |
| 180 | 0x%0.4X |  |
| 2842 | >> |  |
| 1234 | Ack all |  |
| 3575 | Ack selected |  |
| 2960 | Acked Transition |  |
| 5431 | Acknowledge Source |  |
| 3963 | Action Text |  |
| 515 | Actual |  |
| 1633 | Add |  |
| 1490 | Add a new calendar entry |  |
| 1074 | Alarm |  |
| 6151 | Amount of acknowledged items from total active events and alarms |  |
| 5408 | Amount of valid Items in table from total active events and alarms |  |
| 35 | Anlog Input (IN) |  |
| 131 | Any Year |  |
| 3762 | Array Index |  |
| 2559 | BACnetObjectManager.ObjectList[INDEX]. |  |
| 2566 | BACnetObjectManager.ObjectList[INDEX].I_BACnetBaseObject |  |
| 2573 | BACnetObjectManager.ObjectList[INDEX].sDescription |  |
| 2580 | BACnetObjectManager.ObjectList[INDEX]._ |  |
| 2587 | BACnetObjectManager.ObjectList[INDEX]._07_sDescription |  |
| 2594 | BACnetObjectManager.ObjectList[INDEX]._08_sPresentValue |  |
| 2602 | BACnetObjectManager.ObjectList[INDEX]._09_sUnit |  |
| 2609 | BACnetObjectManager.ObjectList[INDEX]._FbPropInfos.sDescription |  |
| 2616 | BACnetObjectManager.ObjectList[INDEX]._FbPropInfos.sPresentValue |  |
| 2623 | BACnetObjectManager.ObjectList[INDEX]._FbPropInfos.sUnit |  |
| 2630 | BACnetObjectManager.ObjectList[INDEX]._FbPropInfos._07_sDescription |  |
| 2637 | BACnetObjectManager.ObjectList[INDEX]._FbPropInfos._08_sPresentValue |  |
| 2644 | BACnetObjectManager.ObjectList[INDEX]._FbPropInfos._09_sUnit |  |
| 2651 | BACnetObjectManager.ObjectList[INDEX].__FbPropInfos.sDescription |  |
| 739 | Binary Input (xIN) |  |
| 2083 | Binary Output (xOUT) |  |
| 6754 | Bit |  |
| 1891 | Bit Value |  |
| 2275 | Bitcount |  |
| 2014 | BT Status : (%0.2d) |  |
| 183 | Cancel |  |
| 1165 | Config StateText |  |
| 4416 | Create |  |
| 288 | Created |  |
| 2410 | Data |  |
| 1160 | Data Type |  |
| 160 | DataType |  |
| 1499 | Date |  |
| 1221 | Day |  |
| 43 | Delete |  |
| 1559 | Delete the selected calendar entry |  |
| 5415 | Denotation |  |
| 1167 | Description |  |
| 2097 | Device Identifier |  |
| 1032 | dtDateTime |  |
| 278 | dtToFault |  |
| 609 | dtToNormal |  |
| 248 | dtToOffNormal |  |
| 1040 | Dummy to load the action command dialog |  |
| 1283 | Dummy to load the action text dialog |  |
| 2112 | Dummy to load the calendar dialog |  |
| 3386 | Dummy to load the daily schedule dialog |  |
| 3984 | Dummy to load the date range dialog |  |
| 297 | Dummy to load the exception schedule dialog |  |
| 152 | Dummy to load the ObjectPropertyReference dialog |  |
| 3472 | Dummy to load the special event daily schedule dialog |  |
| 5611 | Dyn. |  |
| 395 | Edit |  |
| 334 | Edit the selected calendar entry |  |
| 1661 | End Date |  |
| 2037 | End Day |  |
| 1351 | End Month |  |
| 2476 | End Weekday |  |
| 2647 | End Year |  |
| 4020 | Event |  |
| 3843 | Event Enable |  |
| 449 | Event List |  |
| 3983 | Event Priorities |  |
| 1268 | Event Priority |  |
| 2026 | Event State |  |
| 155 | Event Time Stamp |  |
| 435 | Fault |  |
| 2658 | Filter Measurement Values |  |
| 45 | For mapping the raw input value from the physical analog input. |  |
| 244 | Friday |  |
| 1813 | Get |  |
| 3129 | Goto previous visualisation |  |
| 1756 | GROUP_CYCLIC |  |
| 36 | ID |  |
| 413 | ID : %d |  |
| 578 | Index |  |
| 2650 | Index of the state text to modify. Range -> 1..NumberOfStates |  |
| 1642 | Indicates a unit conversion by property IUnitConversion is set. |  |
| 3281 | Inst |  |
| 997 | Instance |  |
| 1757 | Instance / Data Type |  |
| 330 | INVALID |  |
| 629 | IOUT |  |
| 2373 | IOutOfServiceValue |  |
| 7176 | Is Valid |  |
| 956 | IUnit Conversion is set |  |
| 1064 | iValue |  |
| 2657 | Large |  |
| 208 | Logical TRUE (1) if the Out_Of_Service property has a value of TRUE, otherwise logical FALSE (0). |  |
| 716 | Medium |  |
| 2665 | `` Mode `` |  |
| 2495 | Monday |  |
| 1154 | Month |  |
| 1544 | Multistate Input (IN) |  |
| 2114 | Normal |  |
| 3080 | Notify Type |  |
| 489 | Nr. |  |
| 3218 | NULL |  |
| 129 | Object Identifier |  |
| 5215 | Object Name |  |
| 411 | Object Type |  |
| 4519 | Objects : %d |  |
| 695 | ObjectType |  |
| 4370 | OffNormal |  |
| 1801 | Ok |  |
| 545 | OoS |  |
| 966 | OutOfService |  |
| 48 | Overridden |  |
| 1409 | Period |  |
| 3325 | Period Type |  |
| 140 | Pos |  |
| 1278 | Position |  |
| 1788 | Post Delay |  |
| 4048 | Post Delay |  |
| 358 | PresentValue |  |
| 2886 | Prio |  |
| 214 | Priority |  |
| 2260 | Priority for Writing Range 1..16 1 being considered the highest priority and 16 the lowest. |  |
| 3188 | Property |  |
| 3373 | Property ID |  |
| 2068 | Quit |  |
| 2807 | Quit all Events / Alarms |  |
| 1861 | Quit Event / Alarm |  |
| 2672 | r |  |
| 1507 | Range |  |
| 2441 | Range 0..4194303 |  |
| 1206 | Range 1..16 |  |
| 3756 | Result : %d |  |
| 2064 | rValue |  |
| 2679 | s |  |
| 2778 | Saturday |  |
| 2093 | Set |  |
| 421 | Set Prio |  |
| 2686 | Settings |  |
| 2694 | Settings for all selected rows and their properties |  |
| 6697 | Small |  |
| 1620 | Sort by create state |  |
| 5574 | Sort by create type (dynamic / static) |  |
| 2428 | Sort by Instance Number |  |
| 1239 | Sort by object name |  |
| 5049 | Sort by Object Type |  |
| 1113 | Sort by position |  |
| 5213 | Sort by property out of service |  |
| 2837 | Sort by statusflag alarm |  |
| 5636 | Sort by statusflag fault |  |
| 968 | Sort by statusflag out of service |  |
| 2918 | Sort by statusflag overridden |  |
| 3 | Sort Objects ... |  |
| 49 | Start Date |  |
| 346 | Start Day |  |
| 1237 | Start Month |  |
| 3022 | Start Weekday |  |
| 2163 | Start Year |  |
| 207 | sToFault |  |
| 955 | sToNormal |  |
| 381 | sToOffNormal |  |
| 906 | Sunday |  |
| 168 | The property Out-Of-Service, of the type BOOLEAN, indicates whether the Present_Value of the Analog Value Object and Binary Value Object can be changed (TRUE) or not (FALSE) using local software of the BACnet device in which the object is found. If Out_Of_Service is TRUE, the Present_Value property can be written. If the properties Priority_Array and Relinquish_Default are present, writing the Present_Value property is controlled through the BACnet Command Prioritization mechanism. |  |
| 2601 | `` The property run or stop the loop. TRUE means the loop have to run FALSE stop the loop `` |  |
| 347 | `` This plc property is a replacement value in case of xOutOfService. `` |  |
| 2066 | `` This plc property is provided for mapping a physical output module. It contains the value as REAL, INTEGER and WORD. `` |  |
| 328 | This property defines the priority at which the referenced properties are commanded. It corresponds to the Priority parameter of the WriteProperty service. The value is an unsigned integer in the range 1-16, with 1 being considered the highest priority and 16 the lowest |  |
| 4451 | This property indicates where the loop is implemented. BACnet or PLC |  |
| 407 | This property of the type BACnetObjectIdentifier is a numeric code for identifying the object. It must be unique within the BACnet device containing it. |  |
| 500 | This property of the type BACnetStatusFlags represents four Boolean flags that represent the general "health" of the objects listed above. Three of the flags are linked with the values of other properties of this object. A state with additional details can be determined by reading the properties linked with these flags. The relationship between individual flags is not defined by the protocol. |  |
| 2674 | This property of the type BOOL indicates success or failure of the actions triggered during writing into the property Present_Value. At the same time, In_Process is set to TRUE and All_Writes_Successful is set to FALSE. If all write processes were successful after the execution of the entire list, All_Writes_Successful is set to TRUE and, at the same time, In_Process is set to FALSE. As a result, All_Writes_Successful does not represent valid information on the current or most recent action as long as In_Process is TRUE. |  |
| 1294 | This property of the type BOOL is set to TRUE when writing a value in the Present_Value property. The value TRUE indicates that the Command Object has begun processing an action list. After attempting to execute all write processes by the Command Object, the In-Process property is reset to FALSE. |  |
| 2435 | This property of the type CharacterString is a character string of printable characters with no content restrictions |  |
| 3058 | `` This property of the type DINT Indicates the current value of Ineger Value in Engineering Units. `` |  |
| 1931 | `` This property of the type LREAL Indicates the current value of Analog Value in Engineering Units. `` |  |
| 952 | This property of the type REAL Indicates the current value of Analog Value in Engineering Units. Present_Value can receive optional commands. If Present_Value can receive commands for a specific object instance, the properties Priority_Array and Relinquish_Default must also be present for this instance. The Present_Value property must be writable when Out_Of_Service is TRUE |  |
| 646 | This property, of the type BACnetObjectType, indicates membership in a particular object class |  |
| 222 | This property, of the type CharacterString, specifies the name for the object that is unique within the BACnet Device that maintains it. The minimum length of the string is one character. The set of characters used in the Object_Name is restricted to printable characters. |  |
| 2913 | Thursday |  |
| 2860 | Time |  |
| 748 | Time of Day |  |
| 1025 | ToFault |  |
| 4431 | ToNormal |  |
| 4437 | ToOffNormal |  |
| 1197 | TRUE means this object is created for the BACnet and available at it. Otherwise this object is not available from BACnet. |  |
| 2243 | Tuesday |  |
| 915 | Type |  |
| 3113 | udiValue |  |
| 2084 | Unit |  |
| 2915 | usiToFault |  |
| 969 | usiToNormal |  |
| 917 | usiToOffNormal |  |
| 247 | Value |  |
| 2760 | Values < 1900 represents any year |  |
| 1501 | Wednesday |  |
| 1840 | Week and Day |  |
| 1055 | Weekday |  |
| 729 | wValue |  |
| 1 | X |  |
| 1848 | xActive |  |
| 904 | xAlarm |  |
| 567 | `` xAlarm is logical FALSE (0) if the property Event_State has the value NORMAL; otherwise it is logical TRUE (1). For the Schedule Objects, the value for this flag is logical FALSE (0). `` |  |
| 420 | xFault |  |
| 1266 | xFault is logical TRUE (1) if the Reliability property is present and does not have a value of NO_FAULT_DETECTED; otherwise, it is logical FALSE (0). |  |
| 781 | xHighLimitReporting |  |
| 260 | xLowLimitReporting |  |
| 823 | xOutOfService |  |
| 673 | xOverridden |  |
| 918 | xOverridden is logical TRUE (1) if the object has been overridden by a mechanism local to the BACnet device. In this case, "xOverridden" is taken to mean that the Present_Value property cannot be changed through BACnet services. Otherwise, the value is logical FALSE (0). |  |
| 230 | xToFault |  |
| 655 | xToNormal |  |
| 923 | xToOffNormal |  |
| 4595 | xUnspecified |  |
| 1303 | xValue |  |
| 878 | Year |  |
| 6358 | [%d] |  |
| 4259 | [01] |  |
| 2121 | [02] |  |
| 3898 | [03] |  |
| 5502 | [04] |  |
| 4678 | [05] |  |
| 576 | [06] |  |
| 1668 | [07] |  |
| 3524 | [08] |  |
| 3480 | [09] |  |
| 6442 | [0] AckedTransition |  |
| 1734 | [103] Reliability |  |
| 5860 | [10] |  |
| 4673 | [11] |  |
| 5314 | [12] |  |
| 3302 | [130] TimeStamp |  |
| 6577 | [13] |  |
| 1672 | [14] |  |
| 1015 | [15] |  |
| 5822 | [16] |  |
| 2146 | [17] NotificationClass |  |
| 771 | [351] EventMessageTexts |  |
| 4495 | [352] EventMessageTextsConfig |  |
| 3660 | [353] EventDetectionEnable |  |
| 700 | [357] ReliabilityEval.Inhibit |  |
| 492 | [35] EventEnable |  |
| 85 | [36] EventState |  |
| 636 | [388] FaultHighLimit |  |
| 1923 | [389] FaultLowLimit |  |
| 3267 | [390] LowDiffLimit |  |
| 4474 | [430] CommandTimeArray |  |
| 2989 | [431] CurrentCommandPriority |  |
| 490 | [432] LastCommandTime |  |
| 1589 | [524] LoopMode |  |
| 4058 | [72] NotifyType |  |

## Header ¶


## Helper ¶


## IEffectivePeriod ¶


## IExceptionSchedule


- Dialogs (hidden) - Sub Visu Calendar Entry

## IListOfObjectPropertyReferences ¶


## IWeeklySchedule ¶


## Input ¶


## Input ¶


## Input ¶


## LReal ¶


## Objects


- 10 Analog Objects Input - Output - Value 12 BinaryObjects - Input - Output - Value 14 Multistate Objects - Input ()Helper Output Value 20 Calendar Objects 22 Scheduler Objects - ()Helper 30 Loop Objects 32 Integer Value Objects 34 Large Anlog Value Objects 36 Bit String Value - Sub 40 Command 42 Device 44 Trend Log 45 Trend Log Multiple 46 Event Enrollment 48 Event Log 50 Notification Class

## ObjetView ¶


## Output ¶


## Output ¶


## Output ¶


## ParameterVisuBACnet (PARAMS)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | tDOUBLE_CLICK | TIME | TIME#500ms |  |
| TASK_PRIO_BACNET_DAEMON_FREEWHEELING | USINT | 31 | Ctrlx ->39 ; PFC->0..15, Ctrlx->20..39 |

Attributes: qualified_only InOut:

## Real ¶


## Scheduler ¶


- txtScheduler (Text List)

## Sub ¶


## Sub ¶


## Sub Command


- Action Action Line - ActionCommandLine - Dialog Internal Action Command - Dialog Internal Action Text

## Sub Visu ¶


## Sub Visu ¶


## Sub Visu ¶


## Sub Visu ¶


## Tab ¶


## Table ¶


## Title


- Command txtDialogObjectActionCommand (Text List) - txtDialogObjectActionText (Text List)

## Udint ¶


## UpdateGroup ¶


## UpdateGroups (Image Pool)


| ID | File name | Image | Link type |
| --- | --- | --- | --- |
| config | parameters_upload_normal.png |  | Embedded |
| cyclic | repeat_normal.png |  | Embedded |
| on_trigger | ribbon_group_execute_normal.png |  | Embedded |
| out_of_sync_normal | out_of_sync_normal.png |  | Embedded |

## Value ¶


## Value ¶


## Value ¶


## Visu Prio Array


- BitString - Bool - Dint - LReal - Real - Udint

## tpl ¶


- Filter - Header - ObjetView - Table

## txtAction (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | DIRECT |  |
| 1 | REVERSE |  |

## txtBinaryPrio (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | INACTIVE (0) |  |
| 1 | ACTIVE (1) |  |

## txtBtLedStatus (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | "stopped" -> BACnet not active |  |
| 1 | "running" -> BACnet is operating |  |
| 2 | "starting" -> BACnet is starting |  |
| 3 | "pers.storage changing" -> BACnet storage access. Do not turn off device |  |
| 4 | "log. storage changing" -> BACnet storage access. Do not turn off device |  |
| 5 | "inconsistent objects" -> BACnet difference between runtime and BACnet object |  |
| 6 | "overload" -> BACnet overload. Packet loss is possible |  |
| 7 | "backup and restore" -> BACnet backup and restore is running |  |
| 8 | "invalid configuration" -> BACnet invalid configuration |  |
| 9 | "internal error" -> BACnet internal error |  |
| 10 | "license expired" -> BACnet license is expired |  |

## txtDataType (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | NULL |  |
| 16 | BOOLEAN |  |
| 32 | UNSIGNED |  |
| 48 | SIGNED |  |
| 64 | REAL |  |
| 80 | DOUBLE |  |
| 112 | CHAR_STRING |  |
| 128 | BIT_STRING |  |
| 144 | ENUMERATED |  |

## txtDataTypeClientCovInc (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | NULL |  |
| 64 | REAL |  |

## txtDayOfMonth (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Any Day | Any Day |
| 1 | 1 | 1 |
| 2 | 2 | 2 |
| 3 | 3 | 3 |
| 4 | 4 | 4 |
| 5 | 5 | 5 |
| 6 | 6 | 6 |
| 7 | 7 | 7 |
| 8 | 8 | 8 |
| 9 | 9 | 9 |
| 10 | 10 | 10 |
| 11 | 11 | 11 |
| 12 | 12 | 12 |
| 13 | 13 | 13 |
| 14 | 14 | 14 |
| 15 | 15 | 15 |
| 16 | 16 | 16 |
| 17 | 17 | 17 |
| 18 | 18 | 18 |
| 19 | 19 | 19 |
| 20 | 20 | 20 |
| 21 | 21 | 21 |
| 22 | 22 | 22 |
| 23 | 23 | 23 |
| 24 | 24 | 24 |
| 25 | 25 | 25 |
| 26 | 26 | 26 |
| 27 | 27 | 27 |
| 28 | 28 | 28 |
| 29 | 29 | 29 |
| 30 | 30 | 30 |
| 31 | 31 | 31 |
| 32 | Last Day | Last Day |

## txtDayOfWeek (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Any Week Day | Any Week Day |
| 1 | Monday | Monday |
| 2 | Tuesday | Tuesday |
| 3 | Wednesday | Wednesday |
| 4 | Thursday | Thursday |
| 5 | Friday | Friday |
| 6 | Saturday | Saturday |
| 7 | Sunday | Sunday |

## txtDialogCalendarEntry (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Add New Calendar Entry |  |
| 1 | Edit Calendar Entry |  |

## txtDialogDailyScheduleEntry (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Add New Daily Schedule |  |
| 1 | Edit Daily Schedule |  |

## txtDialogObjectActionCommand (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Add New Command |  |
| 1 | Edit Command |  |

## txtDialogObjectActionText (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Add New Action Text |  |
| 1 | Edit Action Text |  |

## txtDialogObjectTypes (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Analog Input |  |
| 1 | Analog Output |  |
| 2 | Analog Value |  |
| 3 | Binary Input |  |
| 4 | Binary Output |  |
| 5 | Binary Value |  |
| 6 | Calendar |  |
| 7 | Command |  |
| 8 | Device |  |
| 9 | Event Enrollment |  |
| 10 | File |  |
| 11 | Group |  |
| 12 | Loop |  |
| 13 | Multi State Input |  |
| 14 | Multi State Output |  |
| 15 | Notification Class |  |
| 16 | Program |  |
| 17 | Schedule |  |
| 18 | Averaging |  |
| 19 | Multi State Value |  |
| 20 | Trend Log |  |
| 21 | Life Safety Point |  |
| 22 | Life Safety Zone |  |
| 23 | Accumulator |  |
| 24 | Pulse Converter |  |
| 25 | Event Log |  |
| 26 | Global Group |  |
| 27 | Trend Log Multiple |  |
| 28 | Load Control |  |
| 29 | Structured View |  |
| 30 | Access Door |  |
| 31 | Unassigned Depricated |  |
| 32 | Access Credential |  |
| 33 | Access Point |  |
| 34 | Access Rights |  |
| 35 | Access User |  |
| 36 | Access Zone |  |
| 37 | Credential Data Input |  |
| 38 | Network Security |  |
| 39 | Bit String Value |  |
| 40 | Character String Value |  |
| 41 | Date Pattern Value |  |
| 42 | Date Value |  |
| 43 | Date Time Pattern Value |  |
| 44 | Date Time Value |  |
| 45 | Integer Value |  |
| 46 | Large Analog Value |  |
| 47 | Octet String Value |  |
| 48 | Positive Integer Value |  |
| 49 | Time Pattern Value |  |
| 50 | Time Value |  |
| 51 | Notification Forwarder |  |
| 52 | Alert Enrollment |  |
| 53 | Channel |  |
| 54 | Lighting Output |  |

## txtEntryType (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Date |  |
| 1 | Range |  |
| 2 | Week and Day |  |

## txtEventLogRecordType (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Status |  |
| 1 | Notification |  |
| 2 | Time Change |  |

## txtEventState (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Normal |  |
| 1 | Fault |  |
| 2 | Off Normal |  |
| 3 | High Limit |  |
| 4 | Low Limit |  |
| 5 | Life Safety Alarm |  |

## txtEventType (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Change of Bitstring |  |
| 1 | Change of State |  |
| 2 | Change of Value |  |
| 3 | Command Failure |  |
| 4 | Floating Limit |  |
| 5 | Out of Range |  |
| 6 | Complex |  |
| 7 | Buffer Ready |  |
| 8 | Change of Live Safety |  |
| 9 | Extended |  |
| 10 | Buffer Ready 2 |  |
| 11 | Unsigned Range |  |
| 12 | Reserved 12 |  |
| 13 | Access Event |  |
| 14 | Double Out of Range |  |
| 15 | Signed Out of Range |  |
| 16 | Unsigned Out of Range |  |
| 17 | Change of Characterstring |  |
| 18 | Change of Statusflags |  |
| 19 | Change of Reliability |  |
| 20 | None |  |

## txtExceptionSchedule (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Add Special Event |  |
| 1 | Edit Special Event |  |

## txtLoggingType (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Polled |  |
| 1 | Change of Value |  |
| 2 | Trigger |  |

## txtLoggingTypeMultiple (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Polled |  |
| 2 | Trigger |  |

## txtLoopMode (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | BACnet Loop |  |
| 1 | PLC Loop |  |

## txtMonth (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Any Month |  |
| 1 | January |  |
| 2 | February |  |
| 3 | March |  |
| 4 | April |  |
| 5 | May |  |
| 6 | June |  |
| 7 | July |  |
| 8 | August |  |
| 9 | September |  |
| 10 | October |  |
| 11 | November |  |
| 12 | December |  |
| 13 | AnyOdd |  |
| 14 | Any Even |  |

## txtNotifyType (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Alarm |  |
| 1 | Event |  |

## txtObjectPropertyReferences (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Add Object Property Reference |  |
| 1 | Edit Object Property Reference |  |

## txtObjectTypes (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Analog Input |  |
| 1 | Analog Output |  |
| 2 | Analog Value |  |
| 3 | Binary Input |  |
| 4 | Binary Output |  |
| 5 | Binary Value |  |
| 6 | Calendar |  |
| 7 | Command |  |
| 8 | Device |  |
| 9 | Event Enrollment |  |
| 10 | File |  |
| 11 | Group |  |
| 12 | Loop |  |
| 13 | Multi State Input |  |
| 14 | Multi State Output |  |
| 15 | Notification Class |  |
| 16 | Program |  |
| 17 | Schedule |  |
| 18 | Averaging |  |
| 19 | Multi State Value |  |
| 20 | Trend Log |  |
| 21 | Life Safety Point |  |
| 22 | Life Safety Zone |  |
| 23 | Accumulator |  |
| 24 | Pulse Converter |  |
| 25 | Event Log |  |
| 26 | Global Group |  |
| 27 | Trend Log Multiple |  |
| 28 | Load Control |  |
| 29 | Structured View |  |
| 30 | Access Door |  |
| 31 | Unassigned Depricated |  |
| 32 | Access Credential |  |
| 33 | Access Point |  |
| 34 | Access Rights |  |
| 35 | Access User |  |
| 36 | Access Zone |  |
| 37 | Credential Data Input |  |
| 38 | Network Security |  |
| 39 | Bit String Value |  |
| 40 | Character String Value |  |
| 41 | Date Pattern Value |  |
| 42 | Date Value |  |
| 43 | Date Time Pattern Value |  |
| 44 | Date Time Value |  |
| 45 | Integer Value |  |
| 46 | Large Analog Value |  |
| 47 | Octet String Value |  |
| 48 | Positive Integer Value |  |
| 49 | Time Pattern Value |  |
| 50 | Time Value |  |
| 51 | Notification Forwarder |  |
| 52 | Alert Enrollment |  |
| 53 | Channel |  |
| 54 | Lighting Output |  |
| 4294967295 | Invalid |  |

## txtPeriodType (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Calendar Entry |  |
| 1 | Calendar Reference |  |

## txtPrioLevel (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Invalid |  |
| 1 | Prio 1 |  |
| 2 | Prio 2 |  |
| 3 | Prio 3 |  |
| 4 | Prio 4 |  |
| 5 | Prio 5 |  |
| 6 | Prio 6 |  |
| 7 | Prio 7 |  |
| 8 | Prio 8 |  |
| 9 | Prio 9 |  |
| 10 | Prio 10 |  |
| 11 | Prio 11 |  |
| 12 | Prio 12 |  |
| 13 | Prio 13 |  |
| 14 | Prio 14 |  |
| 15 | Prio 15 |  |
| 16 | Prio 16 |  |

## txtPropertyId (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 45 | HIGH_LIMIT |  |
| 59 | LOW_LIMIT |  |
| 85 | PRESENT_VALUE |  |
| 108 | SETPOINT |  |
| 113 | TIME_DELAY |  |
| 133 | LOG_ENABLE |  |
| 356 | TIME_DELAY_NORMAL |  |

## txtReliabilityType (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | No Fault Detected |  |
| 1 | No Sensor |  |
| 2 | Over Range |  |
| 3 | Under Range |  |
| 4 | Open Loop |  |
| 5 | Shorted Loop |  |
| 6 | No Output |  |
| 7 | Unreliable Other |  |
| 8 | Process Error |  |
| 9 | Multi State Fault |  |
| 10 | Configuration Error |  |
| 11 | Reserved 11 |  |
| 12 | Communication Failure |  |
| 13 | Member Fault |  |
| 14 | Monitored Object Fault |  |
| 15 | Tripped |  |

## txtScheduler (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Edit Effective Period |  |

## txtSystemStatus (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Operational |  |
| 1 | Operational Read Only |  |
| 2 | Download Required |  |
| 3 | Download in Progress |  |
| 4 | Non Operational |  |
| 5 | Backup in Progress |  |

## txtUnits (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 166 | METERS_PER_SECOND_PER_SECOND |  |
| 0 | SQ_METERS |  |
| 1 | SQ_FEET |  |
| 115 | SQ_INCHES |  |
| 116 | SQ_CENTIMETERS |  |
| 105 | CURRENCY1 |  |
| 106 | CURRENCY2 |  |
| 107 | CURRENCY3 |  |
| 108 | CURRENCY4 |  |
| 109 | CURRENCY5 |  |
| 110 | CURRENCY6 |  |
| 111 | CURRENCY7 |  |
| 112 | CURRENCY8 |  |
| 113 | CURRENCY9 |  |
| 114 | CURRENCY10 |  |
| 2 | MILLIAMPERES |  |
| 3 | AMPERES |  |
| 167 | AMPERES_PER_METER |  |
| 168 | AMPERES_PER_SQUARE_METER |  |
| 169 | AMPERE_SQUARE_METERS |  |
| 170 | FARADS |  |
| 171 | HENRYS |  |
| 4 | OHMS |  |
| 172 | OHM_METERS |  |
| 145 | MILLIOHMS |  |
| 122 | KILOHMS |  |
| 123 | MEGOHMS |  |
| 190 | MICRO_SIEMENS |  |
| 173 | SIEMENS |  |
| 174 | SIEMENS_PER_METER |  |
| 175 | TESLAS |  |
| 5 | VOLTS |  |
| 124 | MILLIVOLTS |  |
| 6 | KILOVOLTS |  |
| 7 | MEGAVOLTS |  |
| 8 | VOLT_AMPERES |  |
| 9 | KILOVOLT_AMPERES |  |
| 10 | MEGAVOLT_AMPERES |  |
| 11 | VOLT_AMPERES_REACTIVE |  |
| 12 | KILOVOLT_AMPERES_REACTIVE |  |
| 13 | MEGAVOLT_AMPERES_REACTIVE |  |
| 176 | VOLTS_PER_DEGREE_KELVIN |  |
| 177 | VOLTS_PER_METER |  |
| 14 | DEGREES_PHASE |  |
| 15 | POWER_FACTOR |  |
| 178 | WEBERS |  |
| 199 | DECIBELS |  |
| 200 | DECIBELS_MILLIVOLT |  |
| 201 | DECIBELS_VOLT |  |
| 202 | MILLISIEMENS |  |
| 16 | JOULES |  |
| 17 | KILOJOULES |  |
| 125 | KILOJOULES_PER_KG |  |
| 126 | MEGAJOULES |  |
| 18 | WATT_HOURS |  |
| 19 | KILOWATT_HOURS |  |
| 146 | MEGAWATT_HOURS |  |
| 20 | BTUS |  |
| 147 | KILO_BTUS |  |
| 148 | MEGA_BTUS |  |
| 21 | THERMS |  |
| 22 | TON_HOURS |  |
| 203 | WATT_HOURS_REACTIVE |  |
| 204 | KILOWATT_HOURS_REACTIVE |  |
| 205 | MEGAWATT_HOURS_REACTIVE |  |
| 23 | JOULES_PER_KG_DRY_AIR |  |
| 149 | KILOJOULES_PER_KG_DRY_AIR |  |
| 150 | MEGAJOULES_PER_KG_DRY_AIR |  |
| 24 | BTUS_PER_LB_DRY_AIR |  |
| 117 | BTUS_PER_POUND |  |
| 127 | JOULES_PER_DEGREE_K |  |
| 151 | KILOJOULES_PER_DEGREE_K |  |
| 152 | MEGAJOULES_PER_DEGREE_K |  |
| 128 | JOULES_PER_KG_DEGREE_K |  |
| 153 | NEWTON |  |
| 25 | CYCLES_PER_HOUR |  |
| 26 | CYCLES_PER_MINUTE |  |
| 27 | HERTZ |  |
| 129 | KILOHERTZ |  |
| 130 | MEGAHERTZ |  |
| 131 | PER_HOUR |  |
| 28 | GRAMS_OF_WATER_PER_KG |  |
| 29 | RELATIVE_HUMIDITY |  |
| 30 | MILLIMETERS |  |
| 31 | METERS |  |
| 32 | INCHES |  |
| 33 | FEET |  |
| 118 | CENTIMETERS |  |
| 193 | KILOMETERS |  |
| 194 | MICROMETERS |  |
| 179 | CANDELAS |  |
| 180 | CANDELAS_PER_SQUARE_METER |  |
| 34 | WATTS_PER_SQ_FOOT |  |
| 35 | WATTS_PER_SQ_METER |  |
| 36 | LUMENS |  |
| 37 | LUXES |  |
| 38 | FOOT_CANDLES |  |
| 39 | KILOGRAMS |  |
| 40 | POUNDS_MASS |  |
| 41 | TONS |  |
| 195 | GRAMS |  |
| 196 | MILLIGRAMS |  |
| 154 | GS_PER_SECOND |  |
| 155 | GS_PER_MINUTE |  |
| 42 | KGS_PER_SECOND |  |
| 43 | KGS_PER_MINUTE |  |
| 44 | KGS_PER_HOUR |  |
| 45 | LBS_MASS_PER_MINUTE |  |
| 46 | LBS_MASS_PER_HOUR |  |
| 119 | LBS_MASS_PER_SECOND |  |
| 156 | TONS_PER_HOUR |  |
| 132 | MILLIWATTS |  |
| 47 | WATTS |  |
| 48 | KILOWATTS |  |
| 49 | MEGAWATTS |  |
| 50 | BTUS_PER_HOUR |  |
| 157 | KILO_BTUS_PER_HOUR |  |
| 51 | HORSEPOWER |  |
| 52 | TONS_REFRIGERATION |  |
| 53 | PASCALS |  |
| 133 | HECTOPASCALS |  |
| 54 | KILOPASCALS |  |
| 134 | MILLIBARS |  |
| 55 | BARS |  |
| 56 | LBS_FORCE_PER_SQ_INCH |  |
| 57 | CENTIMETERS_OF_WATER |  |
| 58 | INCHES_OF_WATER |  |
| 59 | MILLIMETERS_OF_MERCURY |  |
| 60 | CENTIMETERS_OF_MERCURY |  |
| 61 | INCHES_OF_MERCURY |  |
| 206 | MILLIMETERS_OF_WATER |  |
| 62 | DEGREES_C |  |
| 63 | DEGREES_K |  |
| 181 | DEGREES_KELVIN_PER_HOUR |  |
| 182 | DEGREES_KELVIN_PER_MINUTE |  |
| 64 | DEGREES_F |  |
| 65 | DEGREE_DAYS_C |  |
| 66 | DEGREE_DAYS_F |  |
| 120 | DELTA_DEGREES_FAHRENHEIT |  |
| 121 | DELTA_DEGREES_KELVIN |  |
| 67 | YEARS |  |
| 68 | MONTHS |  |
| 69 | WEEKS |  |
| 70 | DAYS |  |
| 71 | HOURS |  |
| 72 | MINUTES |  |
| 73 | SECONDS |  |
| 158 | HUNDREDTHS_SECONDS |  |
| 159 | MILLISECONDS |  |
| 160 | NEWTON_METERS |  |
| 74 | METERS_PER_SECOND |  |
| 75 | KILOMETERS_PER_HOUR |  |
| 76 | FEET_PER_SECOND |  |
| 77 | FEET_PER_MINUTE |  |
| 78 | MILES_PER_HOUR |  |
| 79 | CUBIC_FEET |  |
| 80 | CUBIC_METERS |  |
| 81 | IMPERIAL_GALLONS |  |
| 82 | LITERS |  |
| 83 | US_GALLONS |  |
| 142 | CUBIC_FEET_PER_SECOND |  |
| 197 | MILLILITERS |  |
| 84 | CUBIC_FEET_PER_MINUTE |  |
| 191 | CUBIC_FEET_PER_HOUR |  |
| 85 | CUBIC_METERS_PER_SECOND |  |
| 165 | CUBIC_METERS_PER_MINUTE |  |
| 135 | CUBIC_METERS_PER_HOUR |  |
| 86 | IMP_GALLONS_PER_MINUTE |  |
| 87 | LITERS_PER_SECOND |  |
| 88 | LITERS_PER_MINUTE |  |
| 136 | LITERS_PER_HOUR |  |
| 89 | US_GALLONS_PER_MINUTE |  |
| 192 | US_GALLONS_PER_HOUR |  |
| 198 | MILLILITERS_PER_SECOND |  |
| 90 | DEGREES_ANGULAR |  |
| 91 | DEGREES_C_PER_HOUR |  |
| 92 | DEGREES_C_PER_MINUTE |  |
| 93 | DEGREES_F_PER_HOUR |  |
| 94 | DEGREES_F_PER_MINUTE |  |
| 183 | JOULE_SECONDS |  |
| 186 | KILOGRAMS_PER_CUBIC_METER |  |
| 137 | KWATT_HOURS_PER_SQ_METER |  |
| 138 | KWATT_HOURS_PER_SQ_FOOT |  |
| 139 | MEGAJOULES_PER_SQ_METER |  |
| 140 | MEGAJOULES_PER_SQ_FOOT |  |
| 95 | NO_UNITS |  |
| 187 | NEWTON_SECONDS |  |
| 188 | NEWTONS_PER_METER |  |
| 96 | PARTS_PER_MILLION |  |
| 97 | PARTS_PER_BILLION |  |
| 98 | PERCENT |  |
| 143 | PERCENT_OBSCUR_PER_FOOT |  |
| 144 | PERCENT_OBSCUR_PER_METER |  |
| 99 | PERCENT_PER_SECOND |  |
| 100 | PER_MINUTE |  |
| 101 | PER_SECOND |  |
| 102 | PSI_PER_DEGREE_F |  |
| 103 | RADIANS |  |
| 184 | RADIANS_PER_SECOND |  |
| 104 | REVOLUTIONS_PER_MIN |  |
| 185 | SQUARE_METERS_PER_NEWTON |  |
| 189 | WATTS_PER_METER_PER_DEGREE_KELVIN |  |
| 141 | WATTS_PER_SQ_M_DEGREE_K |  |
| 207 | PER_MILLE |  |
| 208 | GRAMS_PER_GRAM |  |
| 209 | KILOGRAMS_PER_KILOGRAM |  |
| 210 | GRAMS_PER_KILOGRAM |  |
| 211 | MILLIGRAMS_PER_GRAM |  |
| 212 | MILLIGRAMS_PER_KILOGRAM |  |
| 213 | GRAMS_PER_MILLILITER |  |
| 214 | GRAMS_PER_LITER |  |
| 215 | MILLIGRAMS_PER_LITER |  |
| 216 | MICROGRAMS_PER_LITER |  |
| 217 | GRAMS_PER_CUBIC_METER |  |
| 218 | MILLIGRAMS_PER_CUBIC_METER |  |
| 219 | MICROGRAMS_PER_CUBIC_METER |  |
| 220 | NANOGRAMS_PER_CUBIC_METER |  |
| 221 | GRAMS_PER_CUBIC_CENTIMETER |  |
| 222 | BECQUERELS |  |
| 223 | KILOBECQUERELS |  |
| 224 | MEGABECQUERELS |  |
| 225 | GRAY |  |
| 226 | MILLIGRAY |  |
| 227 | MICROGRAY |  |
| 228 | SIEVERTS |  |
| 229 | MILLISIEVERTS |  |
| 230 | MICROSIEVERTS |  |
| 231 | MICROSIEVERTS_PER_HOUR |  |
| 232 | DECIBELS_A |  |
| 233 | NEPHELOMETRIC_TURBIDITY_UNIT |  |
| 234 | PH |  |
| 235 | GRAMS_PER_SQUARE_METER |  |
| 236 | MINUTES_PER_DEGREE_KELVIN |  |

## txtUnitsSymbole (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | m² | m² |
| 1 | ft² | ft² |
| 2 | mA | mA |
| 3 | A | A |
| 4 | Ohm | Ohm |
| 5 | V | V |
| 6 | kV | kV |
| 7 | MV | MV |
| 8 | VA | VA |
| 9 | kVA | kVA |
| 10 | MVA | MVA |
| 11 | var | var |
| 12 | kvar | kvar |
| 13 |  |  |
| 14 | ° | ° |
| 15 |  |  |
| 16 | J | J |
| 17 | kJ | kJ |
| 18 | Wh | Wh |
| 19 | kWh | kWh |
| 20 | Btu | Btu |
| 21 | thm (US) | thm (US) |
| 22 | ton (US) /h | ton (US) /h |
| 23 | J/kg | J/kg |
| 24 |  |  |
| 25 | 1/h | 1/h |
| 26 | 1/min | 1/min |
| 27 | Hz | Hz |
| 28 | g/kg | g/kg |
| 29 | `` % r.F.`` | % r.F. |
| 30 | mm | mm |
| 31 | m | m |
| 32 | in | in |
| 33 | ft | ft |
| 34 |  |  |
| 35 | W/m³ | W/m132 |
| 36 | lm | lm |
| 37 | lx | lx |
| 38 | ftc | ftc |
| 39 | kg | kg |
| 40 |  |  |
| 41 | t | t |
| 42 | kg/s | kg/s |
| 43 | kg/min | kg/min |
| 44 | kg/h | kg/h |
| 45 |  |  |
| 46 |  |  |
| 47 | W | W |
| 48 | kW | kW |
| 49 | MW | MW |
| 50 | Btuth/h | Btuth/h |
| 51 | PS | PS |
| 52 |  |  |
| 53 | Pa | Pa |
| 54 | kPa | kPa |
| 55 | bar | bar |
| 56 | lbf/in² | lbf/in131 |
| 57 |  |  |
| 58 | inH2O | inH2O |
| 59 |  |  |
| 60 | cm Hg | cm Hg |
| 61 | inHg | inHg |
| 62 | °C | °C |
| 63 | K | K |
| 64 | °F | °F |
| 65 |  |  |
| 66 |  |  |
| 67 | a | a |
| 68 | mo | di |
| 69 | wk | wk |
| 70 | d | d |
| 71 | h | h |
| 72 | min | min |
| 73 | s | s |
| 74 | m/s | m/s |
| 75 | km/h | km/h |
| 76 | ft/s | ft/s |
| 77 | ft/min | ft/min |
| 78 | mile/h | mile/h |
| 79 | ft³ | ft132 |
| 80 | m³ | m132 |
| 81 |  |  |
| 82 | l | l |
| 83 | gal (US) | gal (US) |
| 84 | ft³/min | ft³/min |
| 85 | m³/s | m³/s |
| 86 | gal (UK) /min | gal (UK) /min |
| 87 | l/s | l/s |
| 88 | l/min | l/min |
| 89 | gal (US) /min | gal (US) /min |
| 90 | ° | ° |
| 91 | °C/h | °C/h |
| 92 | °C/min | °C/min |
| 93 | °F/h | °F/h |
| 94 | °F/min | °F/min |
| 95 |  |  |
| 96 | ppm | ppm |
| 97 | ppb | ppb |
| 98 | % | % |
| 99 | %/s | %/s |
| 100 | 1/min | 1/min |
| 101 | 1/s | 1/s |
| 102 |  |  |
| 103 | rad/s | rad/s |
| 104 | r/min | r/min |
| 105 |  |  |
| 106 |  |  |
| 107 |  |  |
| 108 |  |  |
| 109 |  |  |
| 110 |  |  |
| 111 |  |  |
| 112 |  |  |
| 113 |  |  |
| 114 |  |  |
| 115 | in² | in131 |
| 116 | cm² | cm131 |
| 117 | BtuIT/lb | BtuIT/lb |
| 118 | cm | cm |
| 119 |  |  |
| 120 |  |  |
| 121 |  |  |
| 122 | k? | k? |
| 123 | M? | M? |
| 124 | mV | mV |
| 125 | kJ/kg | kJ/kg |
| 126 | MJ | MJ |
| 127 |  |  |
| 128 |  |  |
| 129 | kHz | kHz |
| 130 | MHz | MHz |
| 131 |  |  |
| 132 | mW | mW |
| 133 | hPa | hPa |
| 134 | mbar | mbar |
| 135 | m³/h | m³/h |
| 136 |  |  |
| 137 | kWh/m³ | kWh/m132 |
| 138 |  |  |
| 139 | MJ/m² | MJ/m131 |
| 140 |  |  |
| 141 | `` W/(m²*K) `` | W/(m²*K) |
| 142 |  |  |
| 143 |  |  |
| 144 |  |  |
| 145 | mOhm | mOhm |
| 146 | MW·h | MW·h |
| 147 |  |  |
| 148 |  |  |
| 149 |  |  |
| 151 | kJ/K | kJ/K |
| 152 |  |  |
| 153 | N | N |
| 154 | g/s | g/s |
| 155 | g/min | g/min |
| 156 | t/h | t/h |
| 157 |  |  |
| 158 |  |  |
| 159 | ms | ms |
| 160 | Nm | Nm |
| 161 | mm/s | mm/s |
| 162 | mm/min | mm/min |
| 163 | m/min | m/min |
| 164 | m/h | m/h |
| 165 | m³/min | m³/min |
| 166 | m/s² | m/s131 |
| 167 | A/m | A/m |
| 168 | A/m² | A/m131 |
| 169 | A·m² | A·m131 |
| 170 | F | F |
| 171 | H | H |
| 172 | ?m | ?m |
| 173 | S | S |
| 174 | S/m | S/m |
| 175 | T | T |
| 176 | V/K | V/K |
| 177 | V/m | V/m |
| 178 | Wb | Wb |
| 179 | cd | cd |
| 180 | cd/m² | cd/m131 |
| 181 | K/h | K/h |
| 182 | K/min | K/min |
| 183 | J·s | J·s |
| 184 | rad/s | rad/s |
| 185 | m²/N | m²/N |
| 186 | kg/m³ | kg/m132 |
| 187 | N·s | N·s |
| 188 | N/m | N/m |
| 189 | W/(m·K) | W/(m·K) |
| 190 | µS | µS |
| 191 | ft³/h | ft³/h |
| 192 |  |  |
| 193 | km | km |
| 194 | µm | µm |
| 195 | g | g |
| 196 | mg | mg |
| 197 | ml | ml |
| 198 | ml/s | ml/s |
| 199 | dB | dB |
| 200 | dBmV | dBmV |
| 201 | `` dBV `` | dBV |
| 202 | mS | mS |
| 203 | `` Whr `` | Whr |
| 204 | `` kWhr `` | kWhr |
| 205 | MWhr | MWhr |
| 206 | mmWS | mmWS |
| 207 |  |  |
| 208 | `` g/g `` | g/g |
| 209 | kg/kg | kg/kg |
| 210 | g/kg | g/kg |
| 211 | mg/g | mg/g |
| 212 | mg/kg | mg/kg |
| 213 | g/ml | g/ml |
| 214 | g/l | g/l |
| 215 | mg/l | mg/l |
| 216 | µg/l | µg/l |
| 217 | g/m³ | g/m132 |
| 218 | mg/m³ | mg/m132 |
| 219 | µg/m³ | µg/m132 |
| 220 | ng/m³ | ng/m132 |
| 221 | g/cm³ | g/cm132 |
| 222 | Bq | Bq |
| 223 | kBq | kBq |
| 224 | MBq | MBq |
| 225 | Gy | Gy |
| 226 | mGy | mGy |
| 227 |  |  |
| 228 | Sv | Sv |
| 229 | mSv | mSv |
| 230 |  |  |
| 231 | µSv/h | µSv/h |
| 232 |  |  |
| 233 |  |  |
| 234 | pH | pH |
| 235 | g/m² | g/m131 |
| 236 |  |  |
| 237 |  |  |
| 238 |  |  |
| 239 |  |  |
| 240 |  |  |
| 241 |  |  |
| 242 |  |  |
| 243 |  |  |
| 244 |  |  |
| 245 |  |  |
| 246 |  |  |
| 247 |  |  |
| 248 |  |  |
| 249 |  |  |
| 250 |  |  |
| 251 |  |  |
| 252 |  |  |
| 253 |  |  |
| 254 |  |  |

## txtWeekOfMonth (Text List)


| ID | Default | englisch |
| --- | --- | --- |
| 0 | Any Week | Any Week |
| 1 | Week 1..7 | Week 1..7 |
| 2 | Week 8..14 | Week 8..14 |
| 3 | Week 15..21 | Week 15..21 |
| 4 | Week 22..28 | Week 22..28 |
| 5 | Week 29..31 | Week 29..31 |
| 6 | Last 7 days | Last 7 days |