# WagoTypesProcessorLoad v1.0.1.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesProcessorLoad
- **Version:** 1.0.1.1
- **Categories:** WAGO LayerView|Types and Interfaces
- **Namespace:** WagoTypesProcessorLoad
- **Author:** WAGO / JSo
- **Placeholder:** WagoTypesProcessorLoad

### Description ¶


This document is automatically generated.

Provides types used by WagoSysProcessorLoad.

This document is automatically generated. Provides types used by WagoSysProcessorLoad.

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Global Variable Lists - Other Components 01 Types - eLogLevel (ENUM) - eOverloadAction (ENUM)

### Indices and tables ¶


Based on WagoTypesProcessorLoad.library, last modified 29.05.2024, 20:39:27. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesProcessorLoad.library, last modified 29.05.2024, 20:39:27. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesProcessorLoad Library Documentation


| Company: | WAGO |
| Title: | WagoTypesProcessorLoad |
| Version: | 1.0.1.1 |
| Categories: | WAGO LayerView\|Types and Interfaces |
| Namespace: | WagoTypesProcessorLoad |
| Author: | WAGO / JSo |
| Placeholder: | WagoTypesProcessorLoad |

### Description


This document is automatically generated.

Provides types used by WagoSysProcessorLoad.

This document is automatically generated. Provides types used by WagoSysProcessorLoad.

### Contents:


- 01 Types eLogLevel (ENUM) - eOverloadAction (ENUM) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesProcessorLoad.library, last modified 29.05.2024, 20:39:27. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesProcessorLoad.library, last modified 29.05.2024, 20:39:27. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesProcessorLoad.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:39:27 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:39:27 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / JSo |
| AutoResolveUnbound | bool | True |
| LanguageModelAttribute | string | qualified-access-only |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesProcessorLoad |
| DefaultNamespace | WagoTypesProcessorLoad |
| Version | version | 1.0.1.1 |
| Title | string | WagoTypesProcessorLoad |
| Released | bool | False |
| Placeholder | string | WagoTypesProcessorLoad |
| LibraryCategories | library-category-list | WAGO LayerView\|Types and Interfaces |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |
| IsEndUserLibrary | bool | False |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties :

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| Date | Version | Author | Change |
| 28.02.2024 | 1.0.1.1 | u010663 | Compiled SP16.3 |
| 08.01.2019 | 1.0.1.0 | u015842 | Properties: free placeholder added |
| 04/21/2011 | 1.0.0.1 | JSo | Remove unused library references |
| 06/10/2015 |  | JMü | ADD Placeholder AND resolve libraries with placeholders |
| 07/09/2015 | 1.0.0.0 | JSo | Created |

WagoTypesProcessorLoad

WagoTypesProcessorLoad

### Other Components


## 01 Types ¶


- eLogLevel (ENUM) - eOverloadAction (ENUM)

## eLogLevel (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Overload | 0 | Only log when overload is detected. |
| None | 1 | Don’t create any log entries. |
| All | 2 | Create log entries for all events. |

Specifies how processor load changes are logged.

InOut: Specifies how processor load changes are logged.

## eOverloadAction (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| None | 0 | No reaction, just keep on working |
| ThrowProcessorLoadException | 1 | Throw ProcessorLoadWatchdog_Exception -> immediately stops all tasks. |

Reaction to overload detection

InOut: Reaction to overload detection