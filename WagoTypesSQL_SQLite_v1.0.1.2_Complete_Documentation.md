# WagoTypesSQL_SQLite v1.0.1.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesSQL_SQLite
- **Version:** 1.0.1.2
- **Categories:** WAGO FunctionalView|Base; WAGO LayerView|Sys
- **Namespace:** WagoTypesSQL_SQLite
- **Author:** WAGO/u014042
- **Placeholder:** WagoTypesSQL_SQLite

### Description ¶


This document is automatically generated.

Functions providing access to SQLite3 databases

This document is automatically generated. Functions providing access to SQLite3 databases

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Global Variable Lists ErrorCodes (GVL) - VersionHistory (GVL) Other Components - 29 Types - typSQLite3 (STRUCT) - typSQLite3_Stmt (STRUCT)

### Indices and tables ¶


Based on WagoTypesSQL_SQLite.library, last modified 29.05.2024, 20:43:21. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesSQL_SQLite.library, last modified 29.05.2024, 20:43:21. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesSQL_SQLite Library Documentation


| Company: | WAGO |
| Title: | WagoTypesSQL_SQLite |
| Version: | 1.0.1.2 |
| Categories: | WAGO FunctionalView\|Base; WAGO LayerView\|Sys |
| Namespace: | WagoTypesSQL_SQLite |
| Author: | WAGO/u014042 |
| Placeholder: | WagoTypesSQL_SQLite |

### Description


This document is automatically generated.

Functions providing access to SQLite3 databases

This document is automatically generated. Functions providing access to SQLite3 databases

### Contents:


- 29 Types typSQLite3 (STRUCT) - typSQLite3_Stmt (STRUCT) ErrorCodes (GVL) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesSQL_SQLite.library, last modified 29.05.2024, 20:43:21. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesSQL_SQLite.library, last modified 29.05.2024, 20:43:21. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesSQL_SQLite.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:43:21 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:43:21 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO/u014042 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesSQL_SQLite |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesSQL_SQLite |
| DefaultNamespace | WagoTypesSQL_SQLite |
| Version | version | 1.0.1.2 |
| Title | string | WagoTypesSQL_SQLite |
| Released | bool | False |
| LibraryCategories | library-category-list | WAGO FunctionalView\|Base; WAGO LayerView\|Sys |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties :

### Global Variable Lists


## ErrorCodes (GVL)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | gc_SQLITE_OK | DINT | 0 | Successful result |
| gc_SQLITE_ERROR | DINT | 1 | Generic error |
| gc_SQLITE_INTERNAL | DINT | 2 | Internal logic error in SQLite |
| gc_SQLITE_PERM | DINT | 3 | Access permission denied |
| gc_SQLITE_ABORT | DINT | 4 | Callback routine requested an abort |
| gc_SQLITE_BUSY | DINT | 5 | The database file is locked |
| gc_SQLITE_LOCKED | DINT | 6 | A table in the database is locked |
| gc_SQLITE_NOMEM | DINT | 7 | A malloc() failed |
| gc_SQLITE_READONLY | DINT | 8 | Attempt to write a readonly database |
| gc_SQLITE_INTERRUPT | DINT | 9 | Operation terminated by sqlite3_interrupt() |
| gc_SQLITE_IOERR | DINT | 10 | Some kind of disk I/O error occurred |
| gc_SQLITE_CORRUPT | DINT | 11 | The database disk image is malformed |
| gc_SQLITE_NOTFOUND | DINT | 12 | Unknown opcode in sqlite3_file_control() |
| gc_SQLITE_FULL | DINT | 13 | Insertion failed because database is full |
| gc_SQLITE_CANTOPEN | DINT | 14 | Unable to open the database file |
| gc_SQLITE_PROTOCOL | DINT | 15 | Database lock protocol error |
| gc_SQLITE_EMPTY | DINT | 16 | Internal use only |
| gc_SQLITE_SCHEMA | DINT | 17 | The database schema changed |
| gc_SQLITE_TOOBIG | DINT | 18 | String or BLOB exceeds size limit |
| gc_SQLITE_CONSTRAINT | DINT | 19 | Abort due to constraint violation |
| gc_SQLITE_MISMATCH | DINT | 20 | Data type mismatch |
| gc_SQLITE_MISUSE | DINT | 21 | Library used incorrectly |
| gc_SQLITE_NOLFS | DINT | 22 | Uses OS features not supported on host |
| gc_SQLITE_AUTH | DINT | 23 | Authorization denied |
| gc_SQLITE_FORMAT | DINT | 24 | Not used |
| gc_SQLITE_RANGE | DINT | 25 | 2nd parameter to sqlite3_bind out of range |
| gc_SQLITE_NOTADB | DINT | 26 | File opened that is not a database file |
| gc_SQLITE_NOTICE | DINT | 27 | Notifications from sqlite3_log() |
| gc_SQLITE_WARNING | DINT | 28 | Warnings from sqlite3_log() |
| gc_SQLITE_ROW | DINT | 100 | sqlite3_step() has another row ready |
| gc_SQLITE_DONE | DINT | 101 | sqlite3_step() has finished executing |

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 28.02.2024 | 1.0.1.2 | u010663 | Compiled SP16.3 |
| 08.01.2019 | 1.0.1.1 | u015842 | Properties: free placeholder added |
| 22.02.2017 | 1.0.0.0 | u014042 | Initlial released Version |

WagoSysSQL_SQLite.library

Release Notes: This library needs PFC-XXX firmware >= 12.

WagoSysSQL_SQLite.library Release Notes: This library needs PFC-XXX firmware >= 12.

### Other Components


## 29 Types


- typSQLite3 (STRUCT) - typSQLite3_Stmt (STRUCT)

## typSQLite3 (STRUCT)


| Name | Type |
| --- | --- |
| SQLite3 | vPointer |

Wraps The Sqlite3 Database Object

InOut: Wraps The Sqlite3 Database Object

## typSQLite3_Stmt (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| SQLite3Stmt | vPointer | Pointer to struct sqlite3_stmt |

Wraps The SQLite3 Prepared Statement Object

An instance of this object represents a single SQL statement that has been compiled into binary form and is ready to be evaluated.

Think of each SQL statement as a separate computer program. The original SQL text is source code. A prepared statement object is the compiled object code. All SQL must be converted into a prepared statement before it can be run.

The life-cycle of a prepared statement object usually goes like this:

InOut: Wraps The SQLite3 Prepared Statement Object An instance of this object represents a single SQL statement that has been compiled into binary form and is ready to be evaluated. Think of each SQL statement as a separate computer program. The original SQL text is source code. A prepared statement object is the compiled object code. All SQL must be converted into a prepared statement before it can be run. The life-cycle of a prepared statement object usually goes like this: 1. Create the prepared statement object using FuSqlite3_Prepare() . 2. Bind values to parameters using the FuSqlite3_Bind_*() interfaces. 3. Run the SQL by calling FuSqlite3_Step() one or more times. 4. Reset the prepared statement using FuSqlite3_Reset() then go back to step 2. Do this zero or more times. 5. Destroy the object using FuSqlite3_Finalize() .