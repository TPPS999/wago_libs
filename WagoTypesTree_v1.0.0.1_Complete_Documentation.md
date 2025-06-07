# WagoTypesTree v1.0.0.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesTree
- **Version:** 1.0.0.1
- **Categories:** WAGO LayerView|Sys; Application
- **Namespace:** WagoTypesTree
- **Author:** WAGO / u01045
- **Placeholder:** WagoTypesTree

### Description ¶


This document is automatically generated.

This library provides interfaces for hierarchic tree nodes

This document is automatically generated. This library provides interfaces for hierarchic tree nodes

### Contents: ¶


Contents: - Documentation Index 10 Documentation - WagoTypesTree Library Documentation Project Information Library Information Function Blocks Methods - I_BaseElement.Init (METH) - I_BaseNode.Init (METH) - I_BaseNode.appendChild (METH) - I_BaseNode.getChildByIndex (METH) - I_BaseNode.insertChildByIndex (METH) - I_BaseNode.removeChild (METH) - I_BaseNode.removeChildByIndex (METH) - I_ObjectPool.addPoolObject (METH) - I_ObjectPool.getBaseElement (METH) - I_ObjectPool.getBaseNode (METH) - ... and 3 more Interfaces - I_BaseElement (ITF) - I_BaseNode (ITF) - I_ObjectPool (ITF) - I_TreeViewBaseElement (ITF) - I_TreeViewBaseNode (ITF) Base Components - 20 Base Interfaces - 20 BaseTree - I_BaseElement.IBaseElement (PROP) - I_BaseElement.IParent (PROP) - I_BaseElement.ITag (PROP) - I_BaseElement.udiChildPosition (PROP) - I_BaseElement.uiGeneration (PROP) - I_BaseElement.uiTag (PROP) - I_BaseElement.xInvisible (PROP) - I_BaseElement.xPreSelected (PROP) - ... and 16 more Global Variable Lists Other Components - 30 Tree View (class) - 60 Object Pool (class) - I_ObjectPool.udiTreeViewElements (PROP) - I_ObjectPool.udiTreeViewNodes (PROP) - TreeNodeParameter (PARAMS)

### Indices and tables ¶


Based on WagoTypesTree.library, last modified 29.05.2024, 19:54:22. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesTree.library, last modified 29.05.2024, 19:54:22. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## 10 Documentation ¶


- doc01_Foreword (FB)

## WagoTypesTree Library Documentation


| Company: | WAGO |
| Title: | WagoTypesTree |
| Version: | 1.0.0.1 |
| Categories: | WAGO LayerView\|Sys; Application |
| Namespace: | WagoTypesTree |
| Author: | WAGO / u01045 |
| Placeholder: | WagoTypesTree |

### Description


This document is automatically generated.

This library provides interfaces for hierarchic tree nodes

This document is automatically generated. This library provides interfaces for hierarchic tree nodes

### Contents:


- 10 Documentation doc01_Foreword (FB) 20 Base Interfaces - 20 BaseTree - 30 Tree View (class) - 60 Object Pool (class) TreeNodeParameter (PARAMS) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesTree.library, last modified 29.05.2024, 19:54:22. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesTree.library, last modified 29.05.2024, 19:54:22. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesTree.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:54:23 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:54:22 |
| Description | string | See: Description |
| Copyright | © WAGO GmbH & Co. KG, Germany 2023 – All rights reserved |
| Author | WAGO / u01045 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesTree |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesTree |
| DefaultNamespace | WagoTypesTree |
| Version | version | 1.0.0.1 |
| Title | string | WagoTypesTree |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

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

### Methods


## I_BaseElement.Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Init | BOOL |

Initalizes this element. All internal variables are set to the default

After this the element is unlinked from all relations. This means the element has no parent, no siblings and no binding to any customized object.

Interface variables Function Initalizes this element. All internal variables are set to the default Note After this the element is unlinked from all relations. This means the element has no parent, no siblings and no binding to any customized object.

## I_BaseNode.Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Init | BOOL |

Initalizes this node. All internal variables are set to the default

After this the node is unlinked from all relations This means the element has no parent, no siblings and no binding to any customized object and loose all childs.

Interface variables Function Initalizes this node. All internal variables are set to the default Note After this the node is unlinked from all relations This means the element has no parent, no siblings and no binding to any customized object and loose all childs.

## I_BaseNode.appendChild (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | appendChild | UDINT |
| Input | IChild | I_BaseElement |

Append the given child at the end of the childlist.

Only childs without a parent (IParent = 0) will be appended.

Interface variables Function Append the given child at the end of the childlist. Note Only childs without a parent (IParent = 0) will be appended. @return The list index of the given child (1..n). In case that the child was not appendes it returns 0.

## I_BaseNode.getChildByIndex (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | getChildByIndex | I_BaseElement |  |
| Input | udiIndex | UDINT | 1..n |

Interface variables Function @return If the given index exist the method returns an interface to the child at this index at the childlist. Otherwise it returns 0.

## I_BaseNode.insertChildByIndex (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | insertChildByIndex | UDINT |
| Input | IChild | I_BaseElement |
| udiIndex | UDINT |

Insert the given child before the given index. After that the new child has the given index. In case that the given index is greater than the child count the given child will be appended at the end of the list. In case that the given index <= 1 than the given child will be inserted at first position and the return value is 1.

Only childs without a parent (IParent = 0) will be inserted.

Interface variables Function Insert the given child before the given index. After that the new child has the given index. In case that the given index is greater than the child count the given child will be appended at the end of the list. In case that the given index <= 1 than the given child will be inserted at first position and the return value is 1. Note Only childs without a parent (IParent = 0) will be inserted. @return The index of the new child 1..n 0 –> means the child was not inserted

## I_BaseNode.removeChild (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | removeChild | I_BaseElement |
| Input | IBaseElement | I_BaseElement |

This method removes the given child from childlist.

Interface variables Function This method removes the given child from childlist. @return In case that the index was found the method return an interface to the removed child. Otherwise it returns 0.

## I_BaseNode.removeChildByIndex (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | removeChildByIndex | I_BaseElement |
| Input | udiIndex | UDINT |

This method removes the by index specified child from childlist.

Interface variables Function This method removes the by index specified child from childlist. @return In case that the index was found the method return an interface to the removed child. Otherwise it returns 0.

## I_ObjectPool.addPoolObject (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | addPoolObject | BOOL |
| Input | IElement | I_BaseElement |

## I_ObjectPool.getBaseElement (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getBaseElement | I_BaseElement |

Get a base element.

In case that the store case is empty (no more base elements stored) it will return 0.

Interface variables Get a base element. In case that the store case is empty (no more base elements stored) it will return 0.

## I_ObjectPool.getBaseNode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getBaseNode | I_BaseNode |

Get a base node.

In case that the store case is empty (no more base node stored) it will return 0.

Interface variables Get a base node. In case that the store case is empty (no more base node stored) it will return 0.

## I_ObjectPool.getTreeViewElement (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getTreeViewElement | I_TreeViewBaseElement |

Get a treeview element.

In case that the store case is empty (no more treeview element stored) it will return 0.

Interface variables Get a treeview element. In case that the store case is empty (no more treeview element stored) it will return 0.

## I_ObjectPool.getTreeViewNode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getTreeViewNode | I_TreeViewBaseNode |

Get a treeview node.

In case that the store case is empty (no more treeview node stored) it will return 0.

Interface variables Get a treeview node. In case that the store case is empty (no more treeview node stored) it will return 0.

## I_ObjectPool.recycleObjects (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | recycleObjects | BOOL |
| Input | IElement | I_BaseElement |

Recycle and store the given interface reference. In case that it is the reference to a node recycle all childs too.

Interface variables Recycle and store the given interface reference. In case that it is the reference to a node recycle all childs too.

### Interfaces


## I_BaseElement (ITF)


- I_BaseElement.IBaseElement (PROP) - I_BaseElement.IParent (PROP) - I_BaseElement.ITag (PROP) - I_BaseElement.Init (METH) - I_BaseElement.udiChildPosition (PROP) - I_BaseElement.uiGeneration (PROP) - I_BaseElement.uiTag (PROP) - I_BaseElement.xInvisible (PROP) - I_BaseElement.xPreSelected (PROP) - I_BaseElement.xSelected (PROP)

## I_BaseNode (ITF)


- I_BaseNode.Init (METH) - I_BaseNode.appendChild (METH) - I_BaseNode.getChildByIndex (METH) - I_BaseNode.hasChildElements (PROP) - I_BaseNode.hasChildNodes (PROP) - I_BaseNode.hasChilds (PROP) - I_BaseNode.insertChildByIndex (METH) - I_BaseNode.removeChild (METH) - I_BaseNode.removeChildByIndex (METH) - I_BaseNode.udiChildCount (PROP) - I_BaseNode.udiChildElements (PROP) - I_BaseNode.udiChildNodes (PROP) - I_BaseNode.xExpand (PROP) - I_BaseNode.xExpandLock (PROP)

## I_ObjectPool (ITF)


- I_ObjectPool.addPoolObject (METH) - I_ObjectPool.getBaseElement (METH) - I_ObjectPool.getBaseNode (METH) - I_ObjectPool.getTreeViewElement (METH) - I_ObjectPool.getTreeViewNode (METH) - I_ObjectPool.recycleObjects (METH) - I_ObjectPool.udiBaseElements (PROP) - I_ObjectPool.udiBaseNodes (PROP) - I_ObjectPool.udiTreeViewElements (PROP) - I_ObjectPool.udiTreeViewNodes (PROP)

## I_TreeViewBaseElement (ITF)


- I_TreeViewBaseElement.dwTextColor (PROP) - I_TreeViewBaseElement.sBitmapId (PROP) - I_TreeViewBaseElement.sName (PROP) - I_TreeViewBaseElement.sPath (PROP)

## I_TreeViewBaseNode (ITF)


- I_TreeViewBaseNode.sExpandBitmapId (PROP)

### Base Components


## 20 Base Interfaces


- 20 BaseTree I_BaseElement (ITF) I_BaseElement.IBaseElement (PROP) - I_BaseElement.IParent (PROP) - I_BaseElement.ITag (PROP) - I_BaseElement.Init (METH) - I_BaseElement.udiChildPosition (PROP) - I_BaseElement.uiGeneration (PROP) - I_BaseElement.uiTag (PROP) - I_BaseElement.xInvisible (PROP) - I_BaseElement.xPreSelected (PROP) - I_BaseElement.xSelected (PROP) I_BaseNode (ITF) - I_BaseNode.Init (METH) - I_BaseNode.appendChild (METH) - I_BaseNode.getChildByIndex (METH) - I_BaseNode.hasChildElements (PROP) - I_BaseNode.hasChildNodes (PROP) - I_BaseNode.hasChilds (PROP) - I_BaseNode.insertChildByIndex (METH) - I_BaseNode.removeChild (METH) - I_BaseNode.removeChildByIndex (METH) - I_BaseNode.udiChildCount (PROP) - I_BaseNode.udiChildElements (PROP) - I_BaseNode.udiChildNodes (PROP) - I_BaseNode.xExpand (PROP) - I_BaseNode.xExpandLock (PROP) 30 Tree View (class) - I_TreeViewBaseElement (ITF) I_TreeViewBaseElement.dwTextColor (PROP) - I_TreeViewBaseElement.sBitmapId (PROP) - I_TreeViewBaseElement.sName (PROP) - I_TreeViewBaseElement.sPath (PROP) I_TreeViewBaseNode (ITF) - I_TreeViewBaseNode.sExpandBitmapId (PROP) 60 Object Pool (class) - I_ObjectPool (ITF) I_ObjectPool.addPoolObject (METH) - I_ObjectPool.getBaseElement (METH) - I_ObjectPool.getBaseNode (METH) - I_ObjectPool.getTreeViewElement (METH) - I_ObjectPool.getTreeViewNode (METH) - I_ObjectPool.recycleObjects (METH) - I_ObjectPool.udiBaseElements (PROP) - I_ObjectPool.udiBaseNodes (PROP) - I_ObjectPool.udiTreeViewElements (PROP) - I_ObjectPool.udiTreeViewNodes (PROP)

## 20 BaseTree


- I_BaseElement (ITF) I_BaseElement.IBaseElement (PROP) - I_BaseElement.IParent (PROP) - I_BaseElement.ITag (PROP) - I_BaseElement.Init (METH) - I_BaseElement.udiChildPosition (PROP) - I_BaseElement.uiGeneration (PROP) - I_BaseElement.uiTag (PROP) - I_BaseElement.xInvisible (PROP) - I_BaseElement.xPreSelected (PROP) - I_BaseElement.xSelected (PROP) I_BaseNode (ITF) - I_BaseNode.Init (METH) - I_BaseNode.appendChild (METH) - I_BaseNode.getChildByIndex (METH) - I_BaseNode.hasChildElements (PROP) - I_BaseNode.hasChildNodes (PROP) - I_BaseNode.hasChilds (PROP) - I_BaseNode.insertChildByIndex (METH) - I_BaseNode.removeChild (METH) - I_BaseNode.removeChildByIndex (METH) - I_BaseNode.udiChildCount (PROP) - I_BaseNode.udiChildElements (PROP) - I_BaseNode.udiChildNodes (PROP) - I_BaseNode.xExpand (PROP) - I_BaseNode.xExpandLock (PROP)

## I_BaseElement.IBaseElement (PROP)


Gives the base interface of me

Gives the base interface of me

## I_BaseElement.IParent (PROP)


Interface to the parent of this element. If this element has no parent this Interface is set to 0.

Elements without a parent can not have any sibling.

Function Interface to the parent of this element. If this element has no parent this Interface is set to 0. Note Elements without a parent can not have any sibling.

## I_BaseElement.ITag (PROP)


Here you can bind a customized object to this element. The condition to bind an object is that the object must implement the Interface ‘__System.IQueryinterface’.

This Interface requires no additional methods or properties.

Furthermore the object should implement a customized Interface for the object specific access.

Function Here you can bind a customized object to this element. The condition to bind an object is that the object must implement the Interface ‘__System.IQueryinterface’. This Interface requires no additional methods or properties. Furthermore the object should implement a customized Interface for the object specific access.

## I_BaseElement.udiChildPosition (PROP)


Gives the position at the own siblings -> 1..n

Gives the position at the own siblings -> 1..n

## I_BaseElement.uiGeneration (PROP)


This value represents the generation of this object. If this object has no parent this object is generation 0.

Function This value represents the generation of this object. If this object has no parent this object is generation 0. Example The parent of this object exists and the parent of the parent (grandpa) exits too then this object is the 2nd generation.

## I_BaseElement.uiTag (PROP)


Function Here you can place a customized UINT value at this element for give him an reference to a customized data set.

## I_BaseElement.xInvisible (PROP)


Set this element to invisible at the visu

Set this element to invisible at the visu

## I_BaseElement.xPreSelected (PROP)


Mark this element as pre-selected at the visu

Mark this element as pre-selected at the visu

## I_BaseElement.xSelected (PROP)


Mark this element as selected at the visu

Mark this element as selected at the visu

## I_BaseNode.hasChildElements (PROP)


BOOL -> TRUE -> this node has child elements (leafs)

BOOL -> TRUE -> this node has child elements (leafs)

## I_BaseNode.hasChildNodes (PROP)


BOOL -> TRUE -> this node has child nodes

BOOL -> TRUE -> this node has child nodes

## I_BaseNode.hasChilds (PROP)


BOOL -> TRUE -> this node has childs (elements & nodes)

BOOL -> TRUE -> this node has childs (elements & nodes)

## I_BaseNode.udiChildCount (PROP)


total amount of childs (elements & nodes)

total amount of childs (elements & nodes)

## I_BaseNode.udiChildElements (PROP)


total amount of child elements (leafs)

total amount of child elements (leafs)

## I_BaseNode.udiChildNodes (PROP)


total amount of child nodes

total amount of child nodes

## I_BaseNode.xExpand (PROP)


Set this node to expanded at the visu

Set this node to expanded at the visu

## I_BaseNode.xExpandLock (PROP)


Set this node to lock expanded at the visu

Set this node to lock expanded at the visu

## I_ObjectPool.udiBaseElements (PROP) ¶


## I_ObjectPool.udiBaseNodes (PROP) ¶


## I_TreeViewBaseElement.dwTextColor (PROP)


| Byte | Description |
| --- | --- |
| H-Word/H-Byte | Alpha -> transparency |
| H-Word/L-Byte | Blue |
| L-Word/H-Byte | Green |
| L-Word/L-Byte | Red |

## I_TreeViewBaseElement.sBitmapId (PROP)


Bitmap-Id as string. Specifies the shown bitmap.

Bitmap-Id as string. Specifies the shown bitmap.

## I_TreeViewBaseElement.sName (PROP)


Name of this element. This name is part of the path.

Name of this element. This name is part of the path.

## I_TreeViewBaseElement.sPath (PROP)


The path of this elelment up to the root node. Each part of the path is separated by a slash.

This path must not be unique. It is possible that this element has a sibling with a equal name. In this case the path of both elements are equal.

The path of this elelment up to the root node. Each part of the path is separated by a slash. Note This path must not be unique. It is possible that this element has a sibling with a equal name. In this case the path of both elements are equal.

## I_TreeViewBaseNode.sExpandBitmapId (PROP) ¶


### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 26.02.2024 | 1.0.0.1 | u0103719 | modified environment (SP16 Patch 3) |
| 01.01.2023 | 1.0.0.0 | u010545 | Init |

WagoTypesTree

Release Note

WagoTypesTree Release Note This library provides interfaces for hierarchic tree nodes

### Other Components


## 30 Tree View (class)


- I_TreeViewBaseElement (ITF) I_TreeViewBaseElement.dwTextColor (PROP) - I_TreeViewBaseElement.sBitmapId (PROP) - I_TreeViewBaseElement.sName (PROP) - I_TreeViewBaseElement.sPath (PROP) I_TreeViewBaseNode (ITF) - I_TreeViewBaseNode.sExpandBitmapId (PROP)

## 60 Object Pool (class)


- I_ObjectPool (ITF) I_ObjectPool.addPoolObject (METH) - I_ObjectPool.getBaseElement (METH) - I_ObjectPool.getBaseNode (METH) - I_ObjectPool.getTreeViewElement (METH) - I_ObjectPool.getTreeViewNode (METH) - I_ObjectPool.recycleObjects (METH) - I_ObjectPool.udiBaseElements (PROP) - I_ObjectPool.udiBaseNodes (PROP) - I_ObjectPool.udiTreeViewElements (PROP) - I_ObjectPool.udiTreeViewNodes (PROP)

## I_ObjectPool.udiTreeViewElements (PROP) ¶


## I_ObjectPool.udiTreeViewNodes (PROP) ¶


## TreeNodeParameter (PARAMS)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | MAX_ELEMENT_NAME_LENGTH | USINT | 40 | (40) max. length of a node or leaf name (influence the memsize of each element) |
| MAX_BITMAP_ID_LENGTH | USINT | 30 | (30) max. length of a bitmap id (influence the memsize of each element) |
| MAX_ELEMENT_PATH_LENGTH | UINT | 128 | max. length of an element path |

Attributes: qualified_only InOut: