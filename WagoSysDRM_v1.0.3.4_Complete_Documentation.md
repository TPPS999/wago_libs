# WagoSysDRM v1.0.3.4 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysDRM
- **Version:** 1.0.3.4
- **Categories:** WAGO Internal|Common; Application
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysDRM

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Licensing of Libraries [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Licensing of Libraries [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Methods - Program Organization - Global Variable Lists - Other Components ProjectInfo.IsLicenseOk (PROP) - ProjectInfo.Name (PROP) - ProjectInfo.VersionNumber (PROP)

### Indices and tables ¶


| [1] | Based on WagoSysDRM.library, last modified 27.10.2022, 16:07:47. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysDRM Library Documentation


| Company: | WAGO |
| Title: | WagoSysDRM |
| Version: | 1.0.3.4 |
| Categories: | WAGO Internal\|Common; Application |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysDRM |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Licensing of Libraries [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Licensing of Libraries [1]

### Contents:


- 20 Program Organization Units ProjectInfo (FB) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysDRM.library, last modified 27.10.2022, 16:07:47. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysDRM.library |
| contentFile | WagoSysDRM_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 27.10.2022, 16:07:49 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 27.10.2022, 16:07:47 |
| Description | string | See: Description |
| DocFormat | reStructuredText |
| Author | WAGO / u013972 |
| DefaultNamespace |  |
| LanguageModelAttribute | qualified-access-only |
| Company | WAGO |
| Placeholder | WagoSysDRM |
| Project | WagoSysDRM |
| Version | version | 1.0.3.4 |
| Title | string | WagoSysDRM |
| LibraryCategories | library-category-list | WAGO Internal\|Common; Application |

### Library Information


## Library Reference


This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces.

### CmpLog


#### Library Identification


Placeholder: CmpLog Default Resolution: CmpLog, * (System) Namespace: CmpLog

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: CmpLog SystemLibrary: False | Optional: False |

### Standard


#### Library Identification


Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: Standard SystemLibrary: False | Optional: False |

### SysExcept


#### Library Identification


Placeholder: SysExcept Default Resolution: SysExcept, * (System) Namespace: SysExcept

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: SysExcept SystemLibrary: False | Optional: False |

### SysProcess


#### Library Identification


Placeholder: SysProcess Default Resolution: SysProcess, * (System) Namespace: SysProcess

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: SysProcess SystemLibrary: False | Optional: False |

### SysTarget


#### Library Identification


Placeholder: SysTarget Default Resolution: SysTarget, * (System) Namespace: SysTarget

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: SysTarget SystemLibrary: False | Optional: False |

### WagoSysVersion


#### Library Identification


Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: WagoSysVersion, 1.0.0.0 (WAGO) SystemLibrary: False | Optional: False |

### Function Blocks


## ProjectInfo (FB)


```
(*  MyLibraryName

============ =========== =========== =================
**date**     **version** **author**  **change**
------------ ----------- ----------- -----------------
27.05.2014   0.0.0.9     RE          More Doku, RC for 1.0
07.04.2014   0.0.0.8     RE          Release Notes
24.03.2014   0.0.0.7     RE          Logging of License Mismatch
20.03.2014   0.0.0.6     RE          dependencies to other libraries removed
17.03.2014   0.0.0.5     RE          include license conditions
11.03.2014   0.0.0.4     RE          better documentation
05.02.2014   0.0.0.3     RE          Categories updated
06.11.2013   0.0.0.2     RE          Bugfixes
31.10.2013   0.0.0.1     RE          First Version
============ =========== =========== =================

**Release Notes:**
   <Put important public notes (if they exist) here>
*)

VAR_GLOBAL
    Info : ProjectInfo('0.42','MyLibraryName.library','WAGO');
END_VAR

(*
**Internal Notes:**
    <put internal notes (if they exist) here>
*)
```

```
LibVersion := WagoAppXyz.VersionHistory.Info.VersionNumber;
LibName    := WagoAppXyz.VersionHistory.Info.Name;
```

The function block which contains the versioning information.

Access to its members should be done only via the constructor and the property getters.

Deploy a global variable list VersionHistory (GVL) with only one member, but with versioning history in plain text, e.g.

In projects, you might use it this way:

The function block which contains the versioning information. Access to its members should be done only via the constructor and the property getters. Usage: Deploy a global variable list VersionHistory (GVL) with only one member, but with versioning history in plain text, e.g. In projects, you might use it this way: - ProjectInfo.IsLicenseOk (PROP) - ProjectInfo.LicenseTerms (PROP) - ProjectInfo.Name (PROP) - ProjectInfo.VersionNumber (PROP)

### Methods


## ProjectInfo.LicenseTerms (PROP)


The third string of the constructur. Normally ‘WAGO’ or empty

The third string of the constructur. Normally ‘WAGO’ or empty

### Program Organization


## 20 Program Organization Units


- ProjectInfo (FB) ProjectInfo.IsLicenseOk (PROP) - ProjectInfo.LicenseTerms (PROP) - ProjectInfo.Name (PROP) - ProjectInfo.VersionNumber (PROP)

### Global Variable Lists


## VersionHistory (GVL)


| date | version | author | change |
| 20.10.2022 | 1.0.3.4 | WAGO / u014151 | Add Compiler Error in case of Linking of FB_Init from ProjectInfo |
| 18.08.2022 | 1.0.3.3 | WAGO / u014151 | Optimize exception behavior |
| 11.08.2022 | 1.0.3.2 | WAGO / u014151 | Bugfix |
| 12.07.2022 | 1.0.3.1 | WAGO / u013972 | Allow qualified access only |
| 07.02.2019 | 1.0.2.0 | WAGO / u013972 | Bugfix |
| 03.01.2018 | 1.0.1.0 | WAGO / u013972 | Bugfix |
| 04.04.2018 | 1.0.0.1 | WAGO / u013972 | Bugfix |
| 23.10.2017 | 1.0.0.0 | WAGO / u013972 | Release Version |

### Other Components


## ProjectInfo.IsLicenseOk (PROP)


TRUE if licence terms are fulfilled or not required

Note: Under normal conditions, this should always deliver TRUE, as otherwise the project should not be able to be downloaded.

TRUE if licence terms are fulfilled or not required Note: Under normal conditions, this should always deliver TRUE, as otherwise the project should not be able to be downloaded.

## ProjectInfo.Name (PROP)


```
LibName    := WagoAppXyz.VersionHistory.Info.Name;
```

The name of this library or project

In projects, you might use it this way:

The name of this library or project In projects, you might use it this way:

## ProjectInfo.VersionNumber (PROP)


```
LibVersion := WagoAppXyz.VersionHistory.Info.VersionNumber;
```

The version code of this library or project

e.g. version ‘1.3.6.42’ yields VersionNumber=16#0103_062A

In projects, you might use it this way:

The version code of this library or project e.g. version ‘1.3.6.42’ yields VersionNumber=16#0103_062A In projects, you might use it this way: