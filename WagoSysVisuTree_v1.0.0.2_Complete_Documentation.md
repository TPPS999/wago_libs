# WagoSysVisuTree v1.0.0.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysVisuTree
- **Version:** 1.0.0.2
- **Categories:** WAGO LayerView|Sys; Application
- **Namespace:** WagoSysVisuTree
- **Author:** WAGO / u01045
- **Placeholder:** WagoSysVisuTree

### Description ¶


This document is automatically generated.

Offers classes for create and manage flexible tree structures

This document is automatically generated. Offers classes for create and manage flexible tree structures

### Contents: ¶


Contents: - Documentation Index 10 Documentation - WagoSysVisuTree Library Documentation Project Information Library Information Function Blocks - doc01_Foreword (FB) - doc99_Attachment (FB) Methods - I_MouseListener.onMouseClick (METH) - I_MouseListener.onMouseDoubleClick (METH) - I_MouseListener.onMouseDown (METH) - I_MouseListener.onMouseEnter (METH) - I_MouseListener.onMouseLeave (METH) - I_MouseListener.onMouseUp (METH) - I_MouseListener.onNodeCollapse (METH) - I_MouseListener.onNodeExpand (METH) Interfaces Internal Components Global Variable Lists Other Components - 10 Tree - 10 Visu Tree View - 30 Visu - 30 Visu - 35 Images - 40 Listener Interfaces - 90 Helper - GlobalTextList (Text List) - Image (Image Pool) - InvisibleInput - ... and 3 more

### Indices and tables ¶


Based on WagoSysVisuTree.library, last modified 29.05.2024, 19:54:44. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysVisuTree.library, last modified 29.05.2024, 19:54:44. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## 10 Documentation


- doc01_Foreword (FB) - doc99_Attachment (FB)

## WagoSysVisuTree Library Documentation


| Company: | WAGO |
| Title: | WagoSysVisuTree |
| Version: | 1.0.0.2 |
| Categories: | WAGO LayerView\|Sys; Application |
| Namespace: | WagoSysVisuTree |
| Author: | WAGO / u01045 |
| Placeholder: | WagoSysVisuTree |

### Description


This document is automatically generated.

Offers classes for create and manage flexible tree structures

This document is automatically generated. Offers classes for create and manage flexible tree structures

### Contents:


- 10 Documentation doc01_Foreword (FB) - doc99_Attachment (FB) 30 Visu - 10 Visu Tree View - 40 Listener Interfaces 35 Images - Image (Image Pool) 90 Internal - 30 Visu GlobalTextList (Text List) TreeViewParameter (PARAMS) VersionHistory (GVL)

### Indices and tables


Based on WagoSysVisuTree.library, last modified 29.05.2024, 19:54:44. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysVisuTree.library, last modified 29.05.2024, 19:54:44. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysVisuTree.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:54:51 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:54:44 |
| Description | string | See: Description |
| Copyright | © WAGO GmbH & Co. KG, Germany 2023 – All rights reserved |
| Author | WAGO / u01045 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysVisuTree |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysVisuTree |
| DefaultNamespace | WagoSysVisuTree |
| Version | version | 1.0.0.2 |
| Title | string | WagoSysVisuTree |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: True | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpBitmapPool Library Identification : Placeholder: CmpBitmapPool Default Resolution: CmpBitmapPool, * (System) Namespace: CmpBitmapPool Library Properties : CmpLog Library Identification : Placeholder: CmpLog Default Resolution: CmpLog, * (System) Namespace: CmpLog Library Properties : Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : VisuElem3DPath Library Identification : Placeholder: System_VisuElem3DPath Default Resolution: VisuElem3DPath, 3.5.16.30 (System) Namespace: VisuElem3DPath Library Properties : Library Parameter : Parameter: GC_POINTS_PER_POLYGON = 100 VisuElemBase Library Identification : Placeholder: System_VisuElemBase Default Resolution: VisuElemBase, * (System) Namespace: VisuElemBase Library Properties : VisuElemCamDisplayer Library Identification : Placeholder: System_VisuElemCamDisplayer Default Resolution: VisuElemCamDisplayer, 3.5.16.30 (System) Namespace: VisuElemCamDisplayer Library Properties : Library Parameter : Parameter: GC_POINTS_PER_CAM = 100 VisuElemMeter Library Identification : Placeholder: System_VisuElemMeter Default Resolution: VisuElemMeter, 3.5.16.30 (System) Namespace: VisuElemMeter Library Properties : VisuElemTextEditor Library Identification : Placeholder: System_VisuElemTextEditor Default Resolution: VisuElemTextEditor, 3.5.16.30 (System) Namespace: VisuElemTextEditor Library Properties : VisuElemTrace Library Identification : Placeholder: System_VisuElemTrace Default Resolution: VisuElemTrace, 3.5.16.30 (System) Namespace: VisuElemTrace Library Properties : VisuElemXYChart Library Identification : Placeholder: System_VisuElemXYChart Default Resolution: VisuElemXYChart, 3.5.16.30 (System) Namespace: VisuElemXYChart Library Properties : VisuElems Library Identification : Placeholder: System_VisuElems Default Resolution: VisuElems, * (System) Namespace: VisuElems Library Properties : VisuElemsAlarm Library Identification : Placeholder: System_VisuElemsAlarm Default Resolution: VisuElemsAlarm, 3.5.16.30 (System) Namespace: VisuElemsAlarm Library Properties : VisuElemsDateTime Library Identification : Placeholder: System_VisuElemsDateTime Default Resolution: VisuElemsDateTime, 3.5.16.30 (System) Namespace: VisuElemsDateTime Library Properties : VisuElemsSpecialControls Library Identification : Placeholder: System_VisuElemsSpecialControls Default Resolution: VisuElemsSpecialControls, 3.5.16.30 (System) Namespace: VisuElemsSpecialControls Library Properties : VisuElemsWinControls Library Identification : Placeholder: System_VisuElemsWinControls Default Resolution: VisuElemsWinControls, 3.5.16.30 (System) Namespace: VisuElemsWinControls Library Properties : VisuInputs Library Identification : Placeholder: system_visuinputs Default Resolution: VisuInputs, 3.5.16.30 (System) Namespace: visuinputs Library Properties : VisuNativeControl Library Identification : Placeholder: System_VisuNativeControl Default Resolution: VisuNativeControl, 3.5.16.0 (System) Namespace: VisuNativeControl Library Properties : VisuSymbols Library Identification : Placeholder: VisuSymbols Default Resolution: VisuSymbols, * (System) Namespace: VisuSymbols Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesTree Library Identification : Placeholder: WagoTypesTree Default Resolution: WagoTypesTree, * (WAGO) Namespace: WagoTypesTree Library Properties : Library Parameter : Parameter: MAX_ELEMENT_NAME_LENGTH = 40 Parameter: MAX_BITMAP_ID_LENGTH = 30 Parameter: MAX_ELEMENT_PATH_LENGTH = 128 WagoVisuIcons Library Identification : Placeholder: WagoVisuIcons Default Resolution: WagoVisuIcons, * (WAGO) Namespace: WagoVisuIcons Library Properties :

### Function Blocks


## doc01_Foreword (FB)


This document, including all figures and illustrations contained therein, is subject to copyright. Any use of this document that infringes upon the copyright provisions stipulated herein is prohibited. Reproduction, translation, electronic and phototechnical filing/archiving (e.g., photocopying), as well as any amendments require the written consent of WAGO GmbH & Co. KG, Minden, Germany. Non-observance will entail the right of claims for damages.

WAGO GmbH & Co. KG reserves the right to make any alterations or modifications that serve to increase the efficiency of technical progress. WAGO GmbH & Co. KG owns all rights arising from granting patents or from the legal protection of utility patents. Third-party products are always mentioned without any reference to patent rights. Thus, the existence of such rights cannot be excluded.

Personnel Qualification

The use of the product described in this document is exclusively geared to specialists having qualifications in PLC programming, electrical specialists or persons instructed by electrical specialists who are also familiar with the appropriate current standards. WAGO GmbH & Co. KG assumes no liability resulting from improper action and damage to WAGO products and third-party products due to non-observance of the information contained in this document.

Intended Use

For each individual application, the components are supplied from the factory with a dedicated hardware and software configuration. Modifications are only admitted within the framework of the possibilities documented in this document. All other changes to the hardware and/or software and the non-conforming use of the components entail the exclusion of liability on part of WAGO GmbH & Co. KG.

Please direct any requirements pertaining to a modified and/or new hardware or software configuration directly to WAGO GmbH & Co. KG.

Scope of Applicability

This application note is based on the _stated hardware and software from the specific manufacturer, as well as the associated documentation. This application note is therefore only valid for the described installation. New hardware and software versions may need to be handled differently.

Please note the detailed description in the specific manuals.

Copyright This document, including all figures and illustrations contained therein, is subject to copyright. Any use of this document that infringes upon the copyright provisions stipulated herein is prohibited. Reproduction, translation, electronic and phototechnical filing/archiving (e.g., photocopying), as well as any amendments require the written consent of WAGO GmbH & Co. KG, Minden, Germany. Non-observance will entail the right of claims for damages. WAGO GmbH & Co. KG reserves the right to make any alterations or modifications that serve to increase the efficiency of technical progress. WAGO GmbH & Co. KG owns all rights arising from granting patents or from the legal protection of utility patents. Third-party products are always mentioned without any reference to patent rights. Thus, the existence of such rights cannot be excluded. Personnel Qualification The use of the product described in this document is exclusively geared to specialists having qualifications in PLC programming, electrical specialists or persons instructed by electrical specialists who are also familiar with the appropriate current standards. WAGO GmbH & Co. KG assumes no liability resulting from improper action and damage to WAGO products and third-party products due to non-observance of the information contained in this document. Intended Use For each individual application, the components are supplied from the factory with a dedicated hardware and software configuration. Modifications are only admitted within the framework of the possibilities documented in this document. All other changes to the hardware and/or software and the non-conforming use of the components entail the exclusion of liability on part of WAGO GmbH & Co. KG. Please direct any requirements pertaining to a modified and/or new hardware or software configuration directly to WAGO GmbH & Co. KG. Scope of Applicability This application note is based on the _stated hardware and software from the specific manufacturer, as well as the associated documentation. This application note is therefore only valid for the described installation. New hardware and software versions may need to be handled differently. Please note the detailed description in the specific manuals.

## doc99_Attachment (FB)


Internal compiler switches

Internal compiler switches TREVIEWSELECTABLE -> select single entry at mouse down

### Methods


## I_MouseListener.onMouseClick (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | onMouseClick | BOOL |
| Input | IBaseElement | WagoTypesTree.I_BaseElement |
| iMousePosX | INT |
| iMousePosY | INT |

## I_MouseListener.onMouseDoubleClick (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | onMouseDoubleClick | BOOL |
| Input | IBaseElement | WagoTypesTree.I_BaseElement |
| iMousePosX | INT |
| iMousePosY | INT |

## I_MouseListener.onMouseDown (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | onMouseDown | BOOL |
| Input | IBaseElement | WagoTypesTree.I_BaseElement |
| iMousePosX | INT |
| iMousePosY | INT |

## I_MouseListener.onMouseEnter (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | onMouseEnter | BOOL |
| Input | IBaseElement | WagoTypesTree.I_BaseElement |
| iMousePosX | INT |
| iMousePosY | INT |

## I_MouseListener.onMouseLeave (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | onMouseLeave | BOOL |
| Input | IBaseElement | WagoTypesTree.I_BaseElement |
| iMousePosX | INT |
| iMousePosY | INT |

## I_MouseListener.onMouseUp (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | onMouseUp | BOOL |
| Input | IBaseElement | WagoTypesTree.I_BaseElement |
| iMousePosX | INT |
| iMousePosY | INT |

This method is called before the default method is called. In case that this method returns TRUE the default functions for onMouseUp() are disabled

Interface variables This method is called before the default method is called. In case that this method returns TRUE the default functions for onMouseUp() are disabled

## I_MouseListener.onNodeCollapse (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | onNodeCollapse | BOOL |
| Input | IBaseNode | WagoTypesTree.I_BaseNode |
| iMousePosX | INT |
| iMousePosY | INT |

## I_MouseListener.onNodeExpand (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | onNodeExpand | BOOL |
| Input | IBaseNode | WagoTypesTree.I_BaseNode |
| iMousePosX | INT |
| iMousePosY | INT |

### Interfaces


## I_MouseListener (ITF)


- I_MouseListener.onMouseClick (METH) - I_MouseListener.onMouseDoubleClick (METH) - I_MouseListener.onMouseDown (METH) - I_MouseListener.onMouseEnter (METH) - I_MouseListener.onMouseLeave (METH) - I_MouseListener.onMouseUp (METH) - I_MouseListener.onNodeCollapse (METH) - I_MouseListener.onNodeExpand (METH)

### Internal Components


## 90 Internal


- 30 Visu 10 Tree Slider - TreeLine 90 Helper - InvisibleInput

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 08.04.2024 | 1.0.0.2 | u0103719 | rename path of namespace (context: VisuElems) |
| 21.02.2024 | 1.0.0.1 | u010663 | Compiled SP16.3 |
| 20.06.2023 | 1.0.0.0 | u010545 | Init |

WagoSysVisuTree

Release Note

This library provides tree nodes

WagoSysVisuTree Release Note This library provides tree nodes

### Other Components


## 10 Tree ¶


## 10 Visu Tree View ¶


## 30 Visu


- 10 Tree Slider - TreeLine 90 Helper - InvisibleInput

## 30 Visu


- 10 Visu Tree View - 40 Listener Interfaces I_MouseListener (ITF) I_MouseListener.onMouseClick (METH) - I_MouseListener.onMouseDoubleClick (METH) - I_MouseListener.onMouseDown (METH) - I_MouseListener.onMouseEnter (METH) - I_MouseListener.onMouseLeave (METH) - I_MouseListener.onMouseUp (METH) - I_MouseListener.onNodeCollapse (METH) - I_MouseListener.onNodeExpand (METH)

## 35 Images ¶


## 40 Listener Interfaces


- I_MouseListener (ITF) I_MouseListener.onMouseClick (METH) - I_MouseListener.onMouseDoubleClick (METH) - I_MouseListener.onMouseDown (METH) - I_MouseListener.onMouseEnter (METH) - I_MouseListener.onMouseLeave (METH) - I_MouseListener.onMouseUp (METH) - I_MouseListener.onNodeCollapse (METH) - I_MouseListener.onNodeExpand (METH)

## 90 Helper ¶


## GlobalTextList (Text List) ¶


## Image (Image Pool)


| ID | File name | Image | Link type |
| --- | --- | --- | --- |
| cut | cut.png |  | Embedded |
| delete | delete.png |  | Embedded |
| Folder | Folder.png |  | Embedded |
| FolderOpen | FolderOpen.png |  | Embedded |
| leaf | leaf.png |  | Embedded |
| MenuExtend | MenuExtend.png |  | Embedded |
| NodeCollapse | NodeCollapse.png |  | Embedded |
| NodeExpand | NodeExpand.png |  | Embedded |
| copy | copy.png |  | Embedded |

## InvisibleInput ¶


## Slider ¶


## TreeLine ¶


## TreeViewParameter (PARAMS)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | tDOUBLE_CLICK | TIME | TIME#500ms |  |
| MAX_NODE_DEPTH | USINT | 20 | max. depth of nodes |
| DEFAULT_TEXT_COLOR | DWORD | 16#FF000000 | Black –> (A/B/G/R) |
| DEFAULT_ELEMENT_BITMAP | STRING | ‘Image.leaf’ | Default Element Bitmap |
| DEFAULT_NODE_OPEN_BITMAP | STRING | ‘Image.FolderOpen’ | Default Node Open Bitmap |
| DEFAULT_NODE_CLOSE_BITMAP | STRING | ‘Image.Folder’ | Default Node Close Bitmap |

Attributes: qualified_only InOut: