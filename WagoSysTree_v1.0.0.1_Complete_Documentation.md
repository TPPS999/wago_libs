# WagoSysTree v1.0.0.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysTree
- **Version:** 1.0.0.1
- **Categories:** WAGO LayerView|Sys; Application
- **Namespace:** WagoSysTree
- **Author:** WAGO / u01045
- **Placeholder:** WagoSysTree

### Description ¶


This document is automatically generated.

Offers classes for create and manage flexible tree structures

This document is automatically generated. Offers classes for create and manage flexible tree structures

### Contents: ¶


Contents: - Documentation Index 10 Documentation - WagoSysTree Library Documentation Project Information Library Information Function Blocks - clsBaseElement (FB) - clsBaseNode (FB) - clsObjectPool (FB) - clsTreeViewBaseElement (FB) - clsTreeViewBaseNode (FB) - doc01_Foreword (FB) Methods - clsBaseElement.Init (METH) - clsBaseNode.Init (METH) - clsBaseNode.appendChild (METH) - clsBaseNode.getChildByIndex (METH) - clsBaseNode.insertChildByIndex (METH) - clsBaseNode.removeChild (METH) - clsBaseNode.removeChildByIndex (METH) - clsObjectPool.addPoolObject (METH) - clsObjectPool.getBaseElement (METH) - clsObjectPool.getBaseNode (METH) - ... and 5 more Program Organization Base Components - 20 BaseTree (class) - I_BaseElement - I_BaseNode - I_TreeViewBaseElement - I_TreeViewBaseElement - I_TreeViewBaseNode - clsBaseElement.IBaseElement (PROP) - clsBaseElement.IParent (PROP) - clsBaseElement.ITag (PROP) - clsBaseElement._Monitoring (PROP) - ... and 25 more Internal Components Global Variable Lists - ErrorTree (GVL) - VersionHistory (GVL) Other Components - 30 Tree View (class) - 60 Object Pool (class) - 80 Status - I_ObjectPool - clsObjectPool.udiTreeViewElements (PROP) - clsObjectPool.udiTreeViewNodes (PROP) - eErrorTree (ENUM)

### Indices and tables ¶


Based on WagoSysTree.library, last modified 20.09.2024, 21:07:41. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysTree.library, last modified 20.09.2024, 21:07:41. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## 10 Documentation ¶


- doc01_Foreword (FB)

## WagoSysTree Library Documentation


| Company: | WAGO |
| Title: | WagoSysTree |
| Version: | 1.0.0.1 |
| Categories: | WAGO LayerView\|Sys; Application |
| Namespace: | WagoSysTree |
| Author: | WAGO / u01045 |
| Placeholder: | WagoSysTree |

### Description


This document is automatically generated.

Offers classes for create and manage flexible tree structures

This document is automatically generated. Offers classes for create and manage flexible tree structures

### Contents:


- 10 Documentation doc01_Foreword (FB) 20 Program Organization Units (classes) - 20 BaseTree (class) - 30 Tree View (class) - 60 Object Pool (class) 80 Status - ErrorTree (GVL) - eErrorTree (ENUM) VersionHistory (GVL)

### Indices and tables


Based on WagoSysTree.library, last modified 20.09.2024, 21:07:41. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysTree.library, last modified 20.09.2024, 21:07:41. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysTree.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 20.09.2024, 21:07:42 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 20.09.2024, 21:07:41 |
| Description | string | See: Description |
| Copyright | © WAGO GmbH & Co. KG, Germany 2023 – All rights reserved |
| Author | WAGO / u01045 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysTree |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysTree |
| DefaultNamespace | WagoSysTree |
| Version | version | 1.0.0.1 |
| Title | string | WagoSysTree |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : SysSocket Library Identification : Placeholder: SysSocket Default Resolution: SysSocket, * (System) Namespace: SysSocket Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties : WagoTypesTree Library Identification : Placeholder: WagoTypesTree Default Resolution: WagoTypesTree, * (WAGO) Namespace: WagoTypesTree Library Properties : Library Parameter : Parameter: MAX_ELEMENT_NAME_LENGTH = 40 Parameter: MAX_BITMAP_ID_LENGTH = 30 Parameter: MAX_ELEMENT_PATH_LENGTH = 128

### Function Blocks


## clsBaseElement (FB)


This class represents a base element (leaf) of a tree. An object of this class is able to be a child of a node.

Typically a child has a parent and can have siblings. All siblings must have the same parent.

Only elements with a parent can have siblings.

So if you want to get more information about the siblings please ask the parent.

Additional it is possible to bind a customized object with an own Interface at the property ‘ITag’ .

Function This class represents a base element (leaf) of a tree. An object of this class is able to be a child of a node. Typically a child has a parent and can have siblings. All siblings must have the same parent. Note Only elements with a parent can have siblings. So if you want to get more information about the siblings please ask the parent. Additional it is possible to bind a customized object with an own Interface at the property ‘ITag’ . - I_BaseElement clsBaseElement.IBaseElement (PROP) - clsBaseElement.IParent (PROP) - clsBaseElement.ITag (PROP) - clsBaseElement.Init (METH) - clsBaseElement.udiChildPosition (PROP) - clsBaseElement.uiGeneration (PROP) - clsBaseElement.uiTag (PROP) - clsBaseElement.xInvisible (PROP) - clsBaseElement.xPreSelected (PROP) - clsBaseElement.xSelected (PROP) Internal - clsBaseElement._Monitoring (PROP)

## clsBaseNode (FB)


This class represents a base node of a tree. An object of this class inherit from clsBaseElement and can be additional a parent of a child. Also it is able to be a child of an other node.

This class has all features of an element clsBaseElement and additional the capability to have childs.

Function This class represents a base node of a tree. An object of this class inherit from clsBaseElement and can be additional a parent of a child. Also it is able to be a child of an other node. This class has all features of an element clsBaseElement and additional the capability to have childs. - I_BaseNode clsBaseNode.appendChild (METH) - clsBaseNode.getChildByIndex (METH) - clsBaseNode.hasChildElements (PROP) - clsBaseNode.hasChildNodes (PROP) - clsBaseNode.hasChilds (PROP) - clsBaseNode.insertChildByIndex (METH) - clsBaseNode.removeChild (METH) - clsBaseNode.removeChildByIndex (METH) - clsBaseNode.udiChildCount (PROP) - clsBaseNode.udiChildElements (PROP) - clsBaseNode.udiChildNodes (PROP) - clsBaseNode.xExpand (PROP) - clsBaseNode.xExpandLock (PROP) clsBaseNode.Init (METH)

## clsObjectPool (FB)


An object of this class is able to manage interface references of base elements, base nodes, treeview elements and treeview nodes.

It works like a automated warehouse. It is able to store references to objects in a storage case.

It has different storage cases for

Also it has Methodes

Function An object of this class is able to manage interface references of base elements, base nodes, treeview elements and treeview nodes. It works like a automated warehouse. It is able to store references to objects in a storage case. It has different storage cases for - Base elements - Base nodes - Treeview elements - Treeview nodes Also it has Methodes - to store objects -> addPoolObject - to recycle used objects -> recycleObjects - to get a base element -> getBaseElement - to get a base node -> getBaseNode - to get a treeview element -> getTreeViewElement - to get a treeview node -> getTreeViewNode - I_ObjectPool clsObjectPool.addPoolObject (METH) - clsObjectPool.getBaseElement (METH) - clsObjectPool.getBaseNode (METH) - clsObjectPool.getTreeViewElement (METH) - clsObjectPool.getTreeViewNode (METH) - clsObjectPool.recycleObjects (METH) - clsObjectPool.udiBaseElements (PROP) - clsObjectPool.udiBaseNodes (PROP) - clsObjectPool.udiTreeViewElements (PROP) - clsObjectPool.udiTreeViewNodes (PROP)

## clsTreeViewBaseElement (FB)


This class represents a base element (leaf) of a tree. An object of this class inherit from clsBaseElement and is also able to be a child of a node.

Additional it has some properties that holds informations for a visualisation.

Typically a child has a parent and can have siblings. All siblings must have the same parent.

Only elements with a parent can have siblings.

So if you want to get more information about the siblings please ask the parent.

Additional it is possible to bind a customized object with an own Interface at the property ‘ITag’ .

Function This class represents a base element (leaf) of a tree. An object of this class inherit from clsBaseElement and is also able to be a child of a node. Additional it has some properties that holds informations for a visualisation. Typically a child has a parent and can have siblings. All siblings must have the same parent. Note Only elements with a parent can have siblings. So if you want to get more information about the siblings please ask the parent. Additional it is possible to bind a customized object with an own Interface at the property ‘ITag’ . - I_TreeViewBaseElement clsTreeViewBaseElement.dwTextColor (PROP) - clsTreeViewBaseElement.sBitmapId (PROP) - clsTreeViewBaseElement.sName (PROP) - clsTreeViewBaseElement.sPath (PROP) clsTreeViewBaseElement.Init (METH)

## clsTreeViewBaseNode (FB)


This class represents a base node of a tree. An object of this class inherit from clsTreeViewBaseElement and can be additional a parent of a child. Also it is able to be a child of an other node.

In addition it has some properties for visualistion.

This class has all features of an tree view element clsTreeViewBaseElement and additional the capability to have childs.

Function This class represents a base node of a tree. An object of this class inherit from clsTreeViewBaseElement and can be additional a parent of a child. Also it is able to be a child of an other node. In addition it has some properties for visualistion. This class has all features of an tree view element clsTreeViewBaseElement and additional the capability to have childs. - I_TreeViewBaseElement clsTreeViewBaseNode.dwTextColor (PROP) - clsTreeViewBaseNode.sBitmapId (PROP) - clsTreeViewBaseNode.sName (PROP) - clsTreeViewBaseNode.sPath (PROP) I_TreeViewBaseNode - clsTreeViewBaseNode.sExpandBitmapId (PROP) clsTreeViewBaseNode.Init (METH)

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


## clsBaseElement.Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Init | BOOL |

Initalizes this element. All internal variables are set to the default

After this the element is unlinked from all relations. This means the element has no parent, no siblings and no binding to any customized object.

Interface variables Function Initalizes this element. All internal variables are set to the default Note After this the element is unlinked from all relations. This means the element has no parent, no siblings and no binding to any customized object.

## clsBaseNode.Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Init | BOOL |

Initalizes this node. All internal variables are set to the default

After this the node is unlinked from all relations This means the element has no parent, no siblings and no binding to any customized object and loose all childs.

Interface variables Function Initalizes this node. All internal variables are set to the default Note After this the node is unlinked from all relations This means the element has no parent, no siblings and no binding to any customized object and loose all childs.

## clsBaseNode.appendChild (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | appendChild | UDINT |
| Input | IChild | WagoTypesTree.I_BaseElement |

Append the given child at the end of the childlist.

Only childs without a parent (IParent = 0) will be appended.

Interface variables Function Append the given child at the end of the childlist. Note Only childs without a parent (IParent = 0) will be appended. @return The list index of the given child. In case that the child was not appendes it returns 0.

## clsBaseNode.getChildByIndex (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | getChildByIndex | WagoTypesTree.I_BaseElement |  |
| Input | udiIndex | UDINT | 1..n |

Interface variables Function @return If the given index exist the method returns an interface to the child at this index at the childlist. Otherwise it returns 0.

## clsBaseNode.insertChildByIndex (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | insertChildByIndex | UDINT |
| Input | IChild | WagoTypesTree.I_BaseElement |
| udiIndex | UDINT |

Insert the given child before the given index. After that the new child has the given index. In case that the given index is greater than the child count the given child will be appended at the end of the list. In case that the given index <= 1 than the given child will be inserted at first position and the return value is 1.

Only childs without a parent (IParent = 0) will be inserted.

Interface variables Function Insert the given child before the given index. After that the new child has the given index. In case that the given index is greater than the child count the given child will be appended at the end of the list. In case that the given index <= 1 than the given child will be inserted at first position and the return value is 1. Note Only childs without a parent (IParent = 0) will be inserted. @return The index of the new child 1..n 0 –> means the child was not inserted

## clsBaseNode.removeChild (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | removeChild | WagoTypesTree.I_BaseElement |
| Input | IBaseElement | WagoTypesTree.I_BaseElement |

This method removes the given child from childlist.

Interface variables Function This method removes the given child from childlist. @return In case that the index was found the method return an interface to the removed child. Otherwise it returns 0.

## clsBaseNode.removeChildByIndex (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | removeChildByIndex | WagoTypesTree.I_BaseElement |  |
| Input | udiIndex | UDINT | 1..n |

This method removes the by index specified child from childlist.

Interface variables Function This method removes the by index specified child from childlist. @return In case that the index was found the method return an interface to the removed child. Otherwise it returns 0.

## clsObjectPool.addPoolObject (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | addPoolObject | BOOL |
| Input | IElement | WagoTypesTree.I_BaseElement |

Store the given interface reference.

Interface variables Store the given interface reference.

## clsObjectPool.getBaseElement (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getBaseElement | WagoTypesTree.I_BaseElement |

Get a base element.

In case that the store case is empty (no more base elements stored) it will return 0.

Interface variables Get a base element. In case that the store case is empty (no more base elements stored) it will return 0.

## clsObjectPool.getBaseNode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getBaseNode | WagoTypesTree.I_BaseNode |

Get a base node.

In case that the store case is empty (no more base node stored) it will return 0.

Interface variables Get a base node. In case that the store case is empty (no more base node stored) it will return 0.

## clsObjectPool.getTreeViewElement (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getTreeViewElement | WagoTypesTree.I_TreeViewBaseElement |

Get a treeview element.

In case that the store case is empty (no more treeview element stored) it will return 0.

Interface variables Get a treeview element. In case that the store case is empty (no more treeview element stored) it will return 0.

## clsObjectPool.getTreeViewNode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getTreeViewNode | WagoTypesTree.I_TreeViewBaseNode |

Get a treeview node.

In case that the store case is empty (no more treeview node stored) it will return 0.

Interface variables Get a treeview node. In case that the store case is empty (no more treeview node stored) it will return 0.

## clsObjectPool.recycleObjects (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | recycleObjects | BOOL |
| Input | IElement | WagoTypesTree.I_BaseElement |

Recycle and store the given interface reference. In case that it is the reference to a node recycle all childs too.

Interface variables Recycle and store the given interface reference. In case that it is the reference to a node recycle all childs too.

## clsTreeViewBaseElement.Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Init | BOOL |

Initalizes this node. All internal variables are set to the default

After this the node is unlinked from all relations This means the element has no parent, no siblings and no binding to any customized objec.

Interface variables Function Initalizes this node. All internal variables are set to the default Note After this the node is unlinked from all relations This means the element has no parent, no siblings and no binding to any customized objec.

## clsTreeViewBaseNode.Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Init | BOOL |

Initalizes this node. All internal variables are set to the default

After this the node is unlinked from all relations This means the element has no parent, no siblings and no binding to any customized object and loose all childs.

Interface variables Function Initalizes this node. All internal variables are set to the default Note After this the node is unlinked from all relations This means the element has no parent, no siblings and no binding to any customized object and loose all childs.

### Program Organization


## 20 Program Organization Units (classes)


- 20 BaseTree (class) clsBaseElement (FB) I_BaseElement clsBaseElement.IBaseElement (PROP) - clsBaseElement.IParent (PROP) - clsBaseElement.ITag (PROP) - clsBaseElement.Init (METH) - clsBaseElement.udiChildPosition (PROP) - clsBaseElement.uiGeneration (PROP) - clsBaseElement.uiTag (PROP) - clsBaseElement.xInvisible (PROP) - clsBaseElement.xPreSelected (PROP) - clsBaseElement.xSelected (PROP) Internal - clsBaseElement._Monitoring (PROP) clsBaseNode (FB) - I_BaseNode clsBaseNode.appendChild (METH) - clsBaseNode.getChildByIndex (METH) - clsBaseNode.hasChildElements (PROP) - clsBaseNode.hasChildNodes (PROP) - clsBaseNode.hasChilds (PROP) - clsBaseNode.insertChildByIndex (METH) - clsBaseNode.removeChild (METH) - clsBaseNode.removeChildByIndex (METH) - clsBaseNode.udiChildCount (PROP) - clsBaseNode.udiChildElements (PROP) - clsBaseNode.udiChildNodes (PROP) - clsBaseNode.xExpand (PROP) - clsBaseNode.xExpandLock (PROP) clsBaseNode.Init (METH) 30 Tree View (class) - clsTreeViewBaseElement (FB) I_TreeViewBaseElement clsTreeViewBaseElement.dwTextColor (PROP) - clsTreeViewBaseElement.sBitmapId (PROP) - clsTreeViewBaseElement.sName (PROP) - clsTreeViewBaseElement.sPath (PROP) clsTreeViewBaseElement.Init (METH) clsTreeViewBaseNode (FB) - I_TreeViewBaseElement clsTreeViewBaseNode.dwTextColor (PROP) - clsTreeViewBaseNode.sBitmapId (PROP) - clsTreeViewBaseNode.sName (PROP) - clsTreeViewBaseNode.sPath (PROP) I_TreeViewBaseNode - clsTreeViewBaseNode.sExpandBitmapId (PROP) clsTreeViewBaseNode.Init (METH) 60 Object Pool (class) - clsObjectPool (FB) I_ObjectPool clsObjectPool.addPoolObject (METH) - clsObjectPool.getBaseElement (METH) - clsObjectPool.getBaseNode (METH) - clsObjectPool.getTreeViewElement (METH) - clsObjectPool.getTreeViewNode (METH) - clsObjectPool.recycleObjects (METH) - clsObjectPool.udiBaseElements (PROP) - clsObjectPool.udiBaseNodes (PROP) - clsObjectPool.udiTreeViewElements (PROP) - clsObjectPool.udiTreeViewNodes (PROP)

### Base Components


## 20 BaseTree (class)


- clsBaseElement (FB) I_BaseElement clsBaseElement.IBaseElement (PROP) - clsBaseElement.IParent (PROP) - clsBaseElement.ITag (PROP) - clsBaseElement.Init (METH) - clsBaseElement.udiChildPosition (PROP) - clsBaseElement.uiGeneration (PROP) - clsBaseElement.uiTag (PROP) - clsBaseElement.xInvisible (PROP) - clsBaseElement.xPreSelected (PROP) - clsBaseElement.xSelected (PROP) Internal - clsBaseElement._Monitoring (PROP) clsBaseNode (FB) - I_BaseNode clsBaseNode.appendChild (METH) - clsBaseNode.getChildByIndex (METH) - clsBaseNode.hasChildElements (PROP) - clsBaseNode.hasChildNodes (PROP) - clsBaseNode.hasChilds (PROP) - clsBaseNode.insertChildByIndex (METH) - clsBaseNode.removeChild (METH) - clsBaseNode.removeChildByIndex (METH) - clsBaseNode.udiChildCount (PROP) - clsBaseNode.udiChildElements (PROP) - clsBaseNode.udiChildNodes (PROP) - clsBaseNode.xExpand (PROP) - clsBaseNode.xExpandLock (PROP) clsBaseNode.Init (METH)

## I_BaseElement


- clsBaseElement.IBaseElement (PROP) - clsBaseElement.IParent (PROP) - clsBaseElement.ITag (PROP) - clsBaseElement.Init (METH) - clsBaseElement.udiChildPosition (PROP) - clsBaseElement.uiGeneration (PROP) - clsBaseElement.uiTag (PROP) - clsBaseElement.xInvisible (PROP) - clsBaseElement.xPreSelected (PROP) - clsBaseElement.xSelected (PROP)

## I_BaseNode


- clsBaseNode.appendChild (METH) - clsBaseNode.getChildByIndex (METH) - clsBaseNode.hasChildElements (PROP) - clsBaseNode.hasChildNodes (PROP) - clsBaseNode.hasChilds (PROP) - clsBaseNode.insertChildByIndex (METH) - clsBaseNode.removeChild (METH) - clsBaseNode.removeChildByIndex (METH) - clsBaseNode.udiChildCount (PROP) - clsBaseNode.udiChildElements (PROP) - clsBaseNode.udiChildNodes (PROP) - clsBaseNode.xExpand (PROP) - clsBaseNode.xExpandLock (PROP)

## I_TreeViewBaseElement


- clsTreeViewBaseNode.dwTextColor (PROP) - clsTreeViewBaseNode.sBitmapId (PROP) - clsTreeViewBaseNode.sName (PROP) - clsTreeViewBaseNode.sPath (PROP)

## I_TreeViewBaseElement


- clsTreeViewBaseElement.dwTextColor (PROP) - clsTreeViewBaseElement.sBitmapId (PROP) - clsTreeViewBaseElement.sName (PROP) - clsTreeViewBaseElement.sPath (PROP)

## I_TreeViewBaseNode


- clsTreeViewBaseNode.sExpandBitmapId (PROP)

## clsBaseElement.IBaseElement (PROP)


Gives the base interface of me

Gives the base interface of me

## clsBaseElement.IParent (PROP)


Interface to the parent of this element. If this element has no parent this Interface is set to 0.

Elements without a parent can not have any sibling.

Function Interface to the parent of this element. If this element has no parent this Interface is set to 0. Note Elements without a parent can not have any sibling.

## clsBaseElement.ITag (PROP)


Here you can bind a customized object to this element. The condition to bind an object is that the object must implement the Interface ‘__System.IQueryinterface’.

This Interface requires no additional methods or properties.

Furthermore the object should implement a customized Interface for the object specific access.

Function Here you can bind a customized object to this element. The condition to bind an object is that the object must implement the Interface ‘__System.IQueryinterface’. This Interface requires no additional methods or properties. Furthermore the object should implement a customized Interface for the object specific access.

## clsBaseElement._Monitoring (PROP) ¶


## clsBaseElement.udiChildPosition (PROP)


Gives the position at the own siblings -> 1..n

Gives the position at the own siblings -> 1..n

## clsBaseElement.uiGeneration (PROP)


This value represents the generation of this object. If this object has no parent this object is generation 0.

Function This value represents the generation of this object. If this object has no parent this object is generation 0. Example The parent of this object exists and the parent of the parent (grandpa) exits too then this object is the 2nd generation.

## clsBaseElement.uiTag (PROP)


Function Here you can place a customized UINT value at this element for give him an reference to a customized data set.

## clsBaseElement.xInvisible (PROP)


Set this element to invisible at the visu

Set this element to invisible at the visu

## clsBaseElement.xPreSelected (PROP)


Mark this element as pre-selected at the visu

Mark this element as pre-selected at the visu

## clsBaseElement.xSelected (PROP)


Mark this element as selected at the visu

Mark this element as selected at the visu

## clsBaseNode.hasChildElements (PROP)


BOOL -> TRUE -> this node has child elements (leafs)

BOOL -> TRUE -> this node has child elements (leafs)

## clsBaseNode.hasChildNodes (PROP)


BOOL -> TRUE -> this node has child nodes

BOOL -> TRUE -> this node has child nodes

## clsBaseNode.hasChilds (PROP)


BOOL -> TRUE -> this node has childs (elements & nodes)

BOOL -> TRUE -> this node has childs (elements & nodes)

## clsBaseNode.udiChildCount (PROP)


total amount of childs (elements & nodes)

total amount of childs (elements & nodes)

## clsBaseNode.udiChildElements (PROP)


total amount of child elements (leafs)

total amount of child elements (leafs)

## clsBaseNode.udiChildNodes (PROP)


total amount of child nodes

total amount of child nodes

## clsBaseNode.xExpand (PROP)


Set this node to expanded at the visu

Set this node to expanded at the visu

## clsBaseNode.xExpandLock (PROP)


Set this node to lock expanded at the visu

Set this node to lock expanded at the visu

## clsObjectPool.udiBaseElements (PROP) ¶


## clsObjectPool.udiBaseNodes (PROP) ¶


## clsTreeViewBaseElement.dwTextColor (PROP)


| Byte | Description |
| --- | --- |
| H-Word/H-Byte | Alpha -> transparency |
| H-Word/L-Byte | Blue |
| L-Word/H-Byte | Green |
| L-Word/L-Byte | Red |

## clsTreeViewBaseElement.sBitmapId (PROP)


Bitmap-Id as string. Specifies the shown bitmap.

Bitmap-Id as string. Specifies the shown bitmap.

## clsTreeViewBaseElement.sName (PROP)


Name of this element. This name is part of the path.

Name of this element. This name is part of the path.

## clsTreeViewBaseElement.sPath (PROP)


The path of this element up to the root node. Each part of the path is separated by a slash.

This path must not be unique. It is possible that this element has a sibling with a equal name. In this case the path of both elements are equal.

The path of this element up to the root node. Each part of the path is separated by a slash. Note This path must not be unique. It is possible that this element has a sibling with a equal name. In this case the path of both elements are equal.

## clsTreeViewBaseNode.dwTextColor (PROP)


| Byte | Description |
| --- | --- |
| H-Word/H-Byte | Alpha -> transparency |
| H-Word/L-Byte | Blue |
| L-Word/H-Byte | Green |
| L-Word/L-Byte | Red |

## clsTreeViewBaseNode.sBitmapId (PROP)


Bitmap-Id as string. Specifies the shown bitmap.

Bitmap-Id as string. Specifies the shown bitmap.

## clsTreeViewBaseNode.sExpandBitmapId (PROP)


Bitmap-Id for an expanded node as string. Specifies the shown bitmap.

Bitmap-Id for an expanded node as string. Specifies the shown bitmap.

## clsTreeViewBaseNode.sName (PROP)


Name of this node. This name is part of the path.

Name of this node. This name is part of the path.

## clsTreeViewBaseNode.sPath (PROP)


The path of this node up to the root node. Each part of the path is separated by a slash.

This path must not be unique. It is possible that this element has a sibling with a equal name. In this case the path of both elements are equal.

The path of this node up to the root node. Each part of the path is separated by a slash. Note This path must not be unique. It is possible that this element has a sibling with a equal name. In this case the path of both elements are equal.

### Internal Components


## Internal ¶


- clsBaseElement._Monitoring (PROP)

### Global Variable Lists


## ErrorTree (GVL)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | ERROR_Tree | ARRAY [0..0] OF WagoTypesErrorBase.typResultItem | [STRUCT(ID := eErrorTree.OK, Severity := eSeverity.none, text := ‘OK’)] |

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 11.07.2024 | 1.0.0.1 | u0103719 | update library compatibility (context: build server,compile file) |
| 20.06.2023 | 1.0.0.0 | u010545 | Init |

WagoSysTree

Release Note

This library provides tree nodes

WagoSysTree Release Note This library provides tree nodes

### Other Components


## 30 Tree View (class)


- clsTreeViewBaseElement (FB) I_TreeViewBaseElement clsTreeViewBaseElement.dwTextColor (PROP) - clsTreeViewBaseElement.sBitmapId (PROP) - clsTreeViewBaseElement.sName (PROP) - clsTreeViewBaseElement.sPath (PROP) clsTreeViewBaseElement.Init (METH) clsTreeViewBaseNode (FB) - I_TreeViewBaseElement clsTreeViewBaseNode.dwTextColor (PROP) - clsTreeViewBaseNode.sBitmapId (PROP) - clsTreeViewBaseNode.sName (PROP) - clsTreeViewBaseNode.sPath (PROP) I_TreeViewBaseNode - clsTreeViewBaseNode.sExpandBitmapId (PROP) clsTreeViewBaseNode.Init (METH)

## 60 Object Pool (class)


- clsObjectPool (FB) I_ObjectPool clsObjectPool.addPoolObject (METH) - clsObjectPool.getBaseElement (METH) - clsObjectPool.getBaseNode (METH) - clsObjectPool.getTreeViewElement (METH) - clsObjectPool.getTreeViewNode (METH) - clsObjectPool.recycleObjects (METH) - clsObjectPool.udiBaseElements (PROP) - clsObjectPool.udiBaseNodes (PROP) - clsObjectPool.udiTreeViewElements (PROP) - clsObjectPool.udiTreeViewNodes (PROP)

## 80 Status ¶


- ErrorTree (GVL) - eErrorTree (ENUM)

## I_ObjectPool


- clsObjectPool.addPoolObject (METH) - clsObjectPool.getBaseElement (METH) - clsObjectPool.getBaseNode (METH) - clsObjectPool.getTreeViewElement (METH) - clsObjectPool.getTreeViewNode (METH) - clsObjectPool.recycleObjects (METH) - clsObjectPool.udiBaseElements (PROP) - clsObjectPool.udiBaseNodes (PROP) - clsObjectPool.udiTreeViewElements (PROP) - clsObjectPool.udiTreeViewNodes (PROP)

## clsObjectPool.udiTreeViewElements (PROP) ¶


## clsObjectPool.udiTreeViewNodes (PROP) ¶


## eErrorTree (ENUM)


| Name | Initial |
| --- | --- |
| OK | 0 |