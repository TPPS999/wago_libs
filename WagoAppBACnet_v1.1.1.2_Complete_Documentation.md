# WagoAppBACnet v1.1.1.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoAppBACnet
- **Version:** 1.1.1.2
- **Categories:** WAGO BusinessView|Building Automation; WAGO LayerView|App; Application
- **Namespace:** WagoAppBACnet
- **Author:** WAGO / u0103719
- **Placeholder:** WagoAppBACnet

### Description ¶


This document is automatically generated.

visualization for controlling BACnet objects

This document is automatically generated. visualization for controlling BACnet objects

### Contents: ¶


Contents: - Documentation Index 10 Documentation - WagoAppBACnet Library Documentation Project Information Library Information Function Blocks - doc01_Foreword (FB) - doc02_SupportedBACnetObjects (FB) Functions - GetBooleanProperty (FUN) - GetCompany (FUN) - GetLibVersion (FUN) - GetLibVersionNumber (FUN) - GetNumberProperty (FUN) - GetTextProperty (FUN) - GetTextProperty2 (FUN) - GetTitle (FUN) - GetVersion (FUN) - GetVersionProperty (FUN) - ... and 1 more Internal Components Global Variable Lists - VersionHistory (GVL) - gc_Helper (GVL) Other Components - 00 BACnetScheduler - 01 BACnetObjektManagerLite - 02 BACnetEventList - 30 Visualizations - 30 Visualizations - 70 Images - 80 Status - 99 General - Acknowledge - BACnetIcons (Image Pool) - ... and 15 more

### Indices and tables ¶


Based on WagoAppBACnet.library, last modified 29.05.2024, 20:55:02. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoAppBACnet.library, last modified 29.05.2024, 20:55:02. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## 10 Documentation


- doc01_Foreword (FB) - doc02_SupportedBACnetObjects (FB)

## WagoAppBACnet Library Documentation


| Company: | WAGO |
| Title: | WagoAppBACnet |
| Version: | 1.1.1.2 |
| Categories: | WAGO BusinessView\|Building Automation; WAGO LayerView\|App; Application |
| Namespace: | WagoAppBACnet |
| Author: | WAGO / u0103719 |
| Placeholder: | WagoAppBACnet |

### Description


This document is automatically generated.

visualization for controlling BACnet objects

This document is automatically generated. visualization for controlling BACnet objects

### Contents:


- 10 Documentation doc01_Foreword (FB) - doc02_SupportedBACnetObjects (FB) 30 Visualizations 70 Images - BACnetIcons (Image Pool) - ImagePool (Image Pool) - UpdateGroups (Image Pool) 80 Status - gc_Helper (GVL) 90 Internal - 30 Visualizations Bibliotheksinformation - GetLibVersion (FUN) - GetLibVersionNumber (FUN) - IsLibReleased (FUN) GlobalTextList (Text List) ParameterAppBACnet (PARAMS) Projektinformationen - GetBooleanProperty (FUN) - GetCompany (FUN) - GetNumberProperty (FUN) - GetTextProperty (FUN) - GetTextProperty2 (FUN) - GetTitle (FUN) - GetVersion (FUN) - GetVersionProperty (FUN) VersionHistory (GVL)

### Indices and tables


Based on WagoAppBACnet.library, last modified 29.05.2024, 20:55:02. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoAppBACnet.library, last modified 29.05.2024, 20:55:02. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoAppBACnet.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:55:12 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:55:02 |
| Description | string | See: Description |
| Copyright | © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved |
| Author | WAGO / u0103719 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoAppBACnet |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoAppBACnet |
| DefaultNamespace | WagoAppBACnet |
| Version | version | 1.1.1.2 |
| Title | string | WagoAppBACnet |
| LibraryCategories | library-category-list | WAGO BusinessView\|Building Automation; WAGO LayerView\|App; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

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

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CAA FB Factory Library Identification : Placeholder: CAA FB Factory Default Resolution: CAA FB Factory, * (CAA Technical Workgroup) Namespace: FBF Library Properties : CAA Types Extern Library Identification : Placeholder: CAA Types Default Resolution: CAA Types Extern, * (CAA Technical Workgroup) Namespace: CAA Library Properties : Common Behaviour Model Library Identification : Placeholder: CBML Default Resolution: Common Behaviour Model, * (3S - Smart Software Solutions GmbH) Namespace: CBML Library Properties : Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : Util Library Identification : Placeholder: Util Default Resolution: Util, * (System) Namespace: Util Library Properties : Library Parameter : Parameter: IBLOCKSIZE = 22800 VisuDialogs Library Identification : Placeholder: VisuDialogs Default Resolution: VisuDialogs, * (System) Namespace: VisuDialogs Library Properties : VisuElem3DPath Library Identification : Placeholder: System_VisuElem3DPath Default Resolution: VisuElem3DPath, 3.5.16.30 (System) Namespace: VisuElem3DPath Library Properties : Library Parameter : Parameter: GC_POINTS_PER_POLYGON = 100 VisuElemCamDisplayer Library Identification : Placeholder: System_VisuElemCamDisplayer Default Resolution: VisuElemCamDisplayer, 3.5.16.30 (System) Namespace: VisuElemCamDisplayer Library Properties : Library Parameter : Parameter: GC_POINTS_PER_CAM = 100 VisuElemMeter Library Identification : Placeholder: System_VisuElemMeter Default Resolution: VisuElemMeter, 3.5.0.0 (System) Namespace: VisuElemMeter Library Properties : VisuElemTextEditor Library Identification : Placeholder: System_VisuElemTextEditor Default Resolution: VisuElemTextEditor, 3.5.16.30 (System) Namespace: VisuElemTextEditor Library Properties : VisuElemTrace Library Identification : Placeholder: System_VisuElemTrace Default Resolution: VisuElemTrace, 3.5.16.30 (System) Namespace: VisuElemTrace Library Properties : VisuElemXYChart Library Identification : Placeholder: System_VisuElemXYChart Default Resolution: VisuElemXYChart, 3.5.16.30 (System) Namespace: VisuElemXYChart Library Properties : VisuElems Library Identification : Placeholder: System_VisuElems Default Resolution: VisuElems, * (System) Namespace: VisuElems Library Properties : VisuElemsAlarm Library Identification : Placeholder: System_VisuElemsAlarm Default Resolution: VisuElemsAlarm, 3.5.16.30 (System) Namespace: VisuElemsAlarm Library Properties : VisuElemsDateTime Library Identification : Placeholder: System_VisuElemsDateTime Default Resolution: VisuElemsDateTime, 3.5.16.30 (System) Namespace: VisuElemsDateTime Library Properties : VisuElemsSpecialControls Library Identification : Placeholder: System_VisuElemsSpecialControls Default Resolution: VisuElemsSpecialControls, 3.5.16.30 (System) Namespace: VisuElemsSpecialControls Library Properties : VisuElemsWinControls Library Identification : Placeholder: System_VisuElemsWinControls Default Resolution: VisuElemsWinControls, 3.5.16.30 (System) Namespace: VisuElemsWinControls Library Properties : VisuInputs Library Identification : Placeholder: system_visuinputs Default Resolution: VisuInputs, * (System) Namespace: visuinputs Library Properties : VisuNativeControl Library Identification : Placeholder: System_VisuNativeControl Default Resolution: VisuNativeControl, 3.5.16.0 (System) Namespace: VisuNativeControl Library Properties : VisuSymbols Library Identification : Placeholder: VisuSymbols Default Resolution: VisuSymbols, * (System) Namespace: VisuSymbols Library Properties : WagoAppString Library Identification : Placeholder: WagoAppString Default Resolution: WagoAppString, * (WAGO) Namespace: WagoAppString Library Properties : WagoAppTime Library Identification : Placeholder: WagoAppTime Default Resolution: WagoAppTime, * (WAGO) Namespace: WagoAppTime Library Properties : WagoSysPlainMem Library Identification : Placeholder: WagoSysPlainMem Default Resolution: WagoSysPlainMem, * (WAGO) Namespace: WagoSysPlainMem Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesBACnet Library Identification : Placeholder: WagoTypesBACnet Default Resolution: WagoTypesBACnet, * (WAGO) Namespace: WagoTypesBACnet Library Properties : WagoVisuIcons Library Identification : Placeholder: WagoVisuIcons Default Resolution: WagoVisuIcons, * (WAGO) Namespace: WagoVisuIcons Library Properties :

### Function Blocks


## doc01_Foreword (FB)


This document, including all figures and illustrations contained therein, is subject to copyright. Any use of this document that infringes upon the copyright provisions stipulated herein is prohibited. Reproduction, translation, electronic and phototechnical filing/archiving (e.g., photocopying), as well as any amendments require the written consent of WAGO Kontakttechnik GmbH & Co. KG, Minden, Germany. Non-observance will entail the right of claims for damages.

WAGO GmbH & Co. KG reserves the right to make any alterations or modifications that serve to increase the efficiency of technical progress. WAGO GmbH & Co. KG owns all rights arising from granting patents or from the legal protection of utility patents. Third-party products are always mentioned without any reference to patent rights. Thus, the existence of such rights cannot be excluded.

Personnel Qualification

The use of the product described in this document is exclusively geared to specialists having qualifications in PLC programming, electrical specialists or persons instructed by electrical specialists who are also familiar with the appropriate current standards. WAGO GmbH & Co. KG assumes no liability resulting from improper action and damage to WAGO products and third-party products due to non-observance of the information contained in this document.

Intended Use

For each individual application, the components are supplied from the factory with a dedicated hardware and software configuration. Modifications are only admitted within the framework of the possibilities documented in this document. All other changes to the hardware and/or software and the non-conforming use of the components entail the exclusion of liability on part of WAGO Kontakttechnik GmbH & Co. KG.

Please direct any requirements pertaining to a modified and/or new hardware or software configuration directly to WAGO GmbH & Co. KG.

Scope of Applicability

This application note is based on the _stated hardware and software from the specific manufacturer, as well as the associated documentation. This application note is therefore only valid for the described installation. New hardware and software versions may need to be handled differently.

Please note the detailed description in the specific manuals.

Copyright This document, including all figures and illustrations contained therein, is subject to copyright. Any use of this document that infringes upon the copyright provisions stipulated herein is prohibited. Reproduction, translation, electronic and phototechnical filing/archiving (e.g., photocopying), as well as any amendments require the written consent of WAGO Kontakttechnik GmbH & Co. KG, Minden, Germany. Non-observance will entail the right of claims for damages. WAGO GmbH & Co. KG reserves the right to make any alterations or modifications that serve to increase the efficiency of technical progress. WAGO GmbH & Co. KG owns all rights arising from granting patents or from the legal protection of utility patents. Third-party products are always mentioned without any reference to patent rights. Thus, the existence of such rights cannot be excluded. Personnel Qualification The use of the product described in this document is exclusively geared to specialists having qualifications in PLC programming, electrical specialists or persons instructed by electrical specialists who are also familiar with the appropriate current standards. WAGO GmbH & Co. KG assumes no liability resulting from improper action and damage to WAGO products and third-party products due to non-observance of the information contained in this document. Intended Use For each individual application, the components are supplied from the factory with a dedicated hardware and software configuration. Modifications are only admitted within the framework of the possibilities documented in this document. All other changes to the hardware and/or software and the non-conforming use of the components entail the exclusion of liability on part of WAGO Kontakttechnik GmbH & Co. KG. Please direct any requirements pertaining to a modified and/or new hardware or software configuration directly to WAGO GmbH & Co. KG. Scope of Applicability This application note is based on the _stated hardware and software from the specific manufacturer, as well as the associated documentation. This application note is therefore only valid for the described installation. New hardware and software versions may need to be handled differently. Please note the detailed description in the specific manuals.

## doc02_SupportedBACnetObjects (FB)


| VisuBACnetScheduler/dlgBACnetScheduler | small**|**medium**|**large |
| --- | --- |
| Scheduler | o \| o \| x |

| VisuBACnetObjectManagerLite/dlgBACnetObjectManagerLite | small**|**medium**|**large |
| --- | --- |
| AnalogInput,AnalogOutput,AnalogValue | x \| x \| x |
| BinaryInput,BinaryOutput,BinaryValue | x \| x \| x |
| MultistateInput,MultistateOutput,MultistateValue | x \| x \| x |
| IntegerValue | x \| x \| x |
| LargeAnalogValue | x \| x \| x |

x: supported o: not supported

x: supported o: not supported

### Functions


## GetBooleanProperty (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetBooleanProperty | BOOL |
| Input | stKey | WSTRING |

This function has been automatically generated from the project information.

Interface variables This function has been automatically generated from the project information.

## GetCompany (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetCompany | WSTRING |

This function has been automatically generated from the project information.

Interface variables This function has been automatically generated from the project information.

## GetLibVersion (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetLibVersion | VERSION |

This function has been automatically generated from the project information.

Interface variables This function has been automatically generated from the project information.

## GetLibVersionNumber (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetLibVersionNumber | DWORD |

This function has been automatically generated from the project information.

Interface variables This function has been automatically generated from the project information.

## GetNumberProperty (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetNumberProperty | DINT |
| Input | stKey | WSTRING |

This function has been automatically generated from the project information.

Interface variables This function has been automatically generated from the project information.

## GetTextProperty (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetTextProperty | WSTRING |
| Input | stKey | WSTRING |

This function has been automatically generated from the project information.

Interface variables This function has been automatically generated from the project information.

## GetTextProperty2 (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetTextProperty2 | POINTER TO WSTRING |
| Input | stKey | WSTRING |

This function has been automatically generated from the project information.

Interface variables This function has been automatically generated from the project information.

## GetTitle (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetTitle | WSTRING |

This function has been automatically generated from the project information.

Interface variables This function has been automatically generated from the project information.

## GetVersion (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetVersion | VERSION |

This function has been automatically generated from the project information.

Interface variables This function has been automatically generated from the project information.

## GetVersionProperty (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetVersionProperty | VERSION |
| Input | stKey | WSTRING |

This function has been automatically generated from the project information.

Interface variables This function has been automatically generated from the project information.

## IsLibReleased (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IsLibReleased | BOOL |

This function has been automatically generated from the project information.

Interface variables This function has been automatically generated from the project information.

### Internal Components


## 90 Internal


- 30 Visualizations 00 BACnetScheduler MainSub - Sub - SubSub - Wrapper 01 BACnetObjektManagerLite - Wrapper 02 BACnetEventList - Acknowledge - EventList Main - Sub Wrapper 99 General

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 20.02.2024 | 1.1.1.2 | u0103719 | modified enviroment (context: SP16 Patch 3) |
| 20.12.2023 | 1.1.1.1 | u0103719 | WAT35392: enable BACNET_TYPE_NULL (Scheduler: daily item) |
| 14.11.2023 | 1.1.1.0 | u0103719 | Scheduler: add BOOLEAN(ENUMERATED) |
| 10.08.2023 | 1.1.0.7 | u0103719 | WAT 35950: change column width for notify type (de) |
| 02.08.2023 | 1.1.0.6 | u0103719 | WAT 35751: adaptation to 64 bit |
| 15.06.2023 | 1.1.0.5 | u0103719 | VV-5045 |
| 21.03.2023 | 1.1.0.4 | u0103719 | VV-5041,VV-5043,VV-5046 |
| 26.01.2023 | 1.1.0.3 | u0103719 | General: update environment |
| 17.10.2022 | 1.1.0.2 | u0103719 | WAT 35034: modified size of visualization |
| 08.09.2022 | 1.1.0.1 | u0103719 | Scheduler: modified update property |
| 21.07.2022 | 1.1.0.0 | u0103719 | Lib: convert lib to SP 17 |
| 12.07.2022 | 1.0.2.1 | u0103719 | EventList: change ScrolMaxIndex (TotalCount->EventCount) |
| 01.01.2022 | 1.0.2.0 | u0103719 | EventList: add Visualisation |
| 30.03.2022 | 1.0.1.1 | u0103719 | Scheduler: delete user management (header bar) |
| 08.03.2022 | 1.0.1.0 | u0103719 | Scheduler: add UNSIGNED Datatype |
| 04.01.2021 | 1.0.0.0 | u0103719 | first release |

## gc_Helper (GVL)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | BOOLEAN_AS_ENUMERATED | USINT | 4 |

### Other Components


## 00 BACnetScheduler ¶


- MainSub - Sub - SubSub - Wrapper

## 01 BACnetObjektManagerLite ¶


## 02 BACnetEventList


- Acknowledge - EventList Main - Sub Wrapper

## 30 Visualizations ¶


## 30 Visualizations


- 00 BACnetScheduler MainSub - Sub - SubSub - Wrapper 01 BACnetObjektManagerLite - Wrapper 02 BACnetEventList - Acknowledge - EventList Main - Sub Wrapper 99 General

## 70 Images


- BACnetIcons (Image Pool) - ImagePool (Image Pool) - UpdateGroups (Image Pool)

## 80 Status ¶


## 99 General ¶


## Acknowledge ¶


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

## Bibliotheksinformation


- GetLibVersion (FUN) - GetLibVersionNumber (FUN) - IsLibReleased (FUN)

## EventList ¶


## GlobalTextList (Text List) ¶


## ImagePool (Image Pool)


| ID | File name | Image | Link type |
| --- | --- | --- | --- |
| FALSE | CheckboxUnchecked.svg |  | Embedded |
| TRUE | CheckboxGreen.svg |  | Embedded |
| scheduler_public_holiday_hot | scheduler_public_holiday_hot.png |  | Embedded |
| scheduler_public_holidays_hot | scheduler_public_holidays_hot.png |  | Embedded |
| scheduler_weekly_hot | scheduler_weekly_hot.png |  | Embedded |
| scheduler_yearly_hot | scheduler_yearly_hot.png |  | Embedded |
| DE | DE.png |  | Embedded |
| EN | EN.png |  | Embedded |
| FR | FR.png |  | Embedded |
| CloseSymbole | CloseSymbole.PNG |  | Embedded |
| Light_On | Light_On.png |  | Embedded |
| Light_Off | Light_Off.png |  | Embedded |
| StatusFlag_Alarm | StatusFlag_InAlarm_24x24_orange.png |  | Embedded |
| StatusFlag_Fault | StatusFlag_Fault_24x24_red.png |  | Embedded |
| StatusFlag_OutOfService | StatusFlag_OutOfService_24x24_grey.png |  | Embedded |
| StatusFlag_Overriden | StatusFlag_Overridden_24x24_grey.png |  | Embedded |
| CheckGreen | CheckGreen.PNG |  | Embedded |
| UncheckGreen | UncheckGreen.png |  | Embedded |
| CheckRed | CheckRed.PNG |  | Embedded |
| UncheckRed | UncheckRed.png |  | Embedded |
| EnableOff | Element-Switch-RockerSwitch-Green-Off.svg |  | Embedded |
| EnableOn | Element-Switch-RockerSwitch-Green-On.svg |  | Embedded |

## Main ¶


## MainSub ¶


## ParameterAppBACnet (PARAMS)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | MAX_SIZE_ARRAY_ITEMS | INT | 50 |
| MAX_SIZE_ENTRY_ITEMS | INT | 3000 |

{attribute ‘qualified_only’ := ‘’}

InOut: {attribute ‘qualified_only’ := ‘’}

## Projektinformationen


- GetBooleanProperty (FUN) - GetCompany (FUN) - GetNumberProperty (FUN) - GetTextProperty (FUN) - GetTextProperty2 (FUN) - GetTitle (FUN) - GetVersion (FUN) - GetVersionProperty (FUN)

## Sub ¶


## Sub ¶


## SubSub ¶


## UpdateGroups (Image Pool)


| ID | File name | Image | Link type |
| --- | --- | --- | --- |
| cyclic | repeat_normal.png |  | Link to file |
| on_trigger | ribbon_group_execute_normal.png |  | Link to file |
| config | parameters_upload_normal.png |  | Link to file |
| out_of_sync_normal | out_of_sync_normal.png |  | Link to file |

## Wrapper ¶


## Wrapper ¶


## Wrapper ¶
