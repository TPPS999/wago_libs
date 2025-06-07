# WagoSysSQL_SQLite_Internal_PFC v1.0.0.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysSQL_SQLite_Internal_PFC
- **Version:** 1.0.0.2
- **Categories:** WAGO FunctionalView|Base; WAGO LayerView|Sys
- **Namespace:** WagoSysSQL_SQLite_Internal_PFC
- **Author:** WAGO/u014042
- **Placeholder:** WagoSysSQL_SQLiteInternal

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Functions providing access to SQLite3 databases [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Functions providing access to SQLite3 databases [1]

### Contents: ¶


Contents: - Project Information - Library Information - Functions FuSqlite3_Bind_Blob (FUN) - FuSqlite3_Bind_Double (FUN) - FuSqlite3_Bind_Int (FUN) - FuSqlite3_Bind_Int64 (FUN) - FuSqlite3_Bind_Text (FUN) - FuSqlite3_Clear_Bindings (FUN) - FuSqlite3_Close (FUN) - FuSqlite3_Column_Blob (FUN) - FuSqlite3_Column_Bytes (FUN) - FuSqlite3_Column_Double (FUN) - ... and 11 more Program Organization Internal Components Global Variable Lists

### Indices and tables ¶


| [1] | Based on WagoSysSQL_SQLite_Internal_PFC.library, last modified 14.01.2019, 19:31:01. The content of this file was automatically generated with None on 14.01.2019, 19:31:04 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysSQL_SQLite_Internal_PFC.library |
| contentFile | WagoSysSQL_SQLite_Internal_PFC_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 19:31:04 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 19:31:01 |
| Description | string | See: Description |
| DocFormat | reStructuredText |
| Author | WAGO/u014042 |
| DefaultNamespace | WagoSysSQL_SQLite_Internal_PFC |
| Placeholder | WagoSysSQL_SQLiteInternal |
| Company | WAGO |
| Title | WagoSysSQL_SQLite_Internal_PFC |
| Project | WagoSysSQL_SQLite_Internal_PFC |
| Released | bool | False |
| Copyright | string | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Version | version | 1.0.0.2 |
| LibraryCategories | library-category-list | WAGO FunctionalView\|Base; WAGO LayerView\|Sys |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesSQL_SQLite Library Identification : Placeholder: WagoTypesSQL_SQLite Default Resolution: WagoTypesSQL_SQLite, * (WAGO) Namespace: WagoTypesSQL_SQLite Library Properties :

### Functions


## FuSqlite3_Bind_Blob (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Bind_Blob | DINT |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a Statement Object |
| diSqlParamIndex | DINT | Index of the SQL parameter to be set. The leftmost SQL parameter has an index of 1. |
| pParamValue | POINTER TO BYTE | The value to bind to the parameter. |
| diNumberOfBytes | DINT | The number of bytes in the parameter, which might be unequal to the number of characters in the parameter. |

Binding Blob Values To Prepared Statements

Interface variables Binding Blob Values To Prepared Statements - Returns gc_SQLITE_OK on success or an error code if anything goes wrong.

## FuSqlite3_Bind_Double (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Bind_Double | DINT |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a Statement Object |
| diSqlParamIndex | DINT | Index of the SQL parameter to be set. The leftmost SQL parameter has an index of 1. |
| lrParamValue | LREAL | The value to bind to the parameter. |

Binding Double Values To Prepared Statements

Interface variables Binding Double Values To Prepared Statements - Returns gc_SQLITE_OK on success or an error code if anything goes wrong.

## FuSqlite3_Bind_Int (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Bind_Int | DINT |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a Statement Object |
| diSqlParamIndex | DINT | Index of the SQL parameter to be set. The leftmost SQL parameter has an index of 1. |
| diParamValue | DINT | The value to bind to the parameter. |

Binding Integer Values To Prepared Statements

Interface variables Binding Integer Values To Prepared Statements - Returns gc_SQLITE_OK on success or an error code if anything goes wrong.

## FuSqlite3_Bind_Int64 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Bind_Int64 | DINT |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a Statement Object |
| diSqlParamIndex | DINT | Index of the SQL parameter to be set. The leftmost SQL parameter has an index of 1. |
| liParamValue | LINT | The value to bind to the parameter. |

Binding Integer Values To Prepared Statements

Interface variables Binding Integer Values To Prepared Statements - Returns gc_SQLITE_OK on success or an error code if anything goes wrong.

## FuSqlite3_Bind_Text (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Bind_Text | DINT |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a Statement Object |
| diSqlParamIndex | DINT | Index of the SQL parameter to be set. The leftmost SQL parameter has an index of 1. |
| pParamValue | POINTER TO BYTE | The value to bind to the parameter. |
| diNumberOfBytes | DINT | The number of bytes in the parameter, which might be unequal to the number of characters in the parameter. |

Binding UTF-8 Encoded Text Values To Prepared Statements

Interface variables Binding UTF-8 Encoded Text Values To Prepared Statements - Returns gc_SQLITE_OK on success or an error code if anything goes wrong.

## FuSqlite3_Clear_Bindings (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Clear_Bindings | DINT |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to the sqlite3 statement |

Reset All Bindings On A Prepared Statement.

Interface variables Reset All Bindings On A Prepared Statement.

## FuSqlite3_Close (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuSqlite3_Close | DINT |
| Input | pSqlite3 | POINTER TO typSQLite3 |

Closing A Database Connection

Interface variables Closing A Database Connection - Returns gc_SQLITE_OK if the sqlite3 object is successfully destroyed and all associated resources are deallocated. - Returns gc_SQLITE_BUSY if the database connection is associated with unfinalized prepared statements.

## FuSqlite3_Column_Blob (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a sqlite statement object |
| diColumn | DINT | Column of interrest, starting with 0 for the first column |
| pBlob | POINTER TO BYTE | Pointer to blob buffer |
| udiSize | UDINT | Size of blob buffer |

Result Values From A Query

Interface variables Result Values From A Query

## FuSqlite3_Column_Bytes (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Column_Bytes | DINT |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a sqlite statement object |
| diColumn | DINT | Column of interrest, starting with 0 for the first column |

Result Values From A Query

Interface variables Result Values From A Query

## FuSqlite3_Column_Double (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Column_Double | LREAL |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a sqlite statement object |
| diColumn | DINT | Column of interrest, starting with 0 for the first column |

Result Values From A Query

Interface variables Result Values From A Query

## FuSqlite3_Column_Int (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Column_Int | DINT |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a sqlite statement object |
| diColumn | DINT | Column of interrest, starting with 0 for the first column |

Result Values From A Query

Interface variables Result Values From A Query

## FuSqlite3_Column_Int64 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Column_Int64 | LINT |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a sqlite statement object |
| diColumn | DINT | Column of interrest, starting with 0 for the first column |

Result Values From A Query

Interface variables Result Values From A Query

## FuSqlite3_Column_Text (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a sqlite statement object |
| diColumn | DINT | Column of interrest, starting with 0 for the first column |
| pText | POINTER TO BYTE | Pointer to text buffer |
| udiSize | UDINT | Size of text buffer in bytes |

Result Values From A Query

Interface variables Result Values From A Query

## FuSqlite3_Errcode (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Errcode | DINT |  |
| Input | pSqlite3 | POINTER TO typSQLite3 | Pointer to a sqlite database object |

If the most recent API call associated with [database connection] D failed, then the sqlite3_errcode(D) interface returns the numeric [result code] or [extended result code] for that API call.

Interface variables If the most recent API call associated with [database connection] D failed, then the sqlite3_errcode(D) interface returns the numeric [result code] or [extended result code] for that API call. - Return numeric result or error code.

## FuSqlite3_Errmsg (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | pSqlite3 | POINTER TO typSQLite3 | Pointer to a sqlite database object |
| pMessage | POINTER TO BYTE | Pointer to message buffer |
| udiSize | UDINT | Size of text buffer in bytes |

Return English-language text that describes the error as UTF-8.

Interface variables Return English-language text that describes the error as UTF-8.

## FuSqlite3_Finalize (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuSqlite3_Finalize | DINT |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt |

Destroy A Prepared Statement Object

The FuSqlite3_Finalize() function is called to delete a prepared statement. If the most recent evaluation of the statement encountered no errors or if the statement is never been evaluated, then FuSqlite3_Finalize() returns gc_SQLITE_OK . If the most recent evaluation of statement S failed, then FuSqlite3_Finalize(S) returns the appropriate error code or extended error code.

The FuSqlite3_Finalize() routine can be called at any point during the life cycle of prepared statement S: before statement S is ever evaluated, after one or more calls to FuSqlite3_Reset() , or after any call to FuSqlite3_Step() regardless of whether or not the statement has completed execution.

The application must finalize every prepared statement in order to avoid resource leaks. It is a grievous error for the application to try to use a prepared statement after it has been finalized. Any use of a prepared statement after it has been finalized can result in undefined and undesirable behavior such as segfaults and heap corruption.

Interface variables Destroy A Prepared Statement Object The FuSqlite3_Finalize() function is called to delete a prepared statement. If the most recent evaluation of the statement encountered no errors or if the statement is never been evaluated, then FuSqlite3_Finalize() returns gc_SQLITE_OK . If the most recent evaluation of statement S failed, then FuSqlite3_Finalize(S) returns the appropriate error code or extended error code. The FuSqlite3_Finalize() routine can be called at any point during the life cycle of prepared statement S: before statement S is ever evaluated, after one or more calls to FuSqlite3_Reset() , or after any call to FuSqlite3_Step() regardless of whether or not the statement has completed execution. The application must finalize every prepared statement in order to avoid resource leaks. It is a grievous error for the application to try to use a prepared statement after it has been finalized. Any use of a prepared statement after it has been finalized can result in undefined and undesirable behavior such as segfaults and heap corruption.

## FuSqlite3_Open (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Open | DINT |  |
| Input | sFilename | STRING(256) | Database filename |
| pSqlite3 | POINTER TO typSQLite3 | SQLite db handle |

Opens A New Database Connection

A database connection handle is returned in pSqlite3, even if an error occurs. The only exception is that if SQLite is unable to allocate memory to hold the sqlite3 object, a NULL will be written into pSqlite3->SQLite3 instead of a pointer to the sqlite3 object. If the database is opened (and/or created) successfully, then gc_SQLITE_OK is returned. Otherwise an error code is returned. The FuSqlite3_Errmsg() routine can be used to obtain an English language description of the error following a failure of any of the FuSqlite3_Open() routine.

Interface variables Opens A New Database Connection A database connection handle is returned in pSqlite3, even if an error occurs. The only exception is that if SQLite is unable to allocate memory to hold the sqlite3 object, a NULL will be written into pSqlite3->SQLite3 instead of a pointer to the sqlite3 object. If the database is opened (and/or created) successfully, then gc_SQLITE_OK is returned. Otherwise an error code is returned. The FuSqlite3_Errmsg() routine can be used to obtain an English language description of the error following a failure of any of the FuSqlite3_Open() routine.

## FuSqlite3_Prepare (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Prepare | DINT |  |
| Input | pSqlite3 | POINTER TO typSQLite3 | Pointer to the SQLite3 Database Object |
| pbzUtf8Sql | POINTER TO BYTE | The SQL-Statement to prepare in UTF8 |
| pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Ponter to the resulting SQLite3 Statement Object |
| Output | pbzUtf8Tail | POINTER TO BYTE | Pointer to the end of the prepared SQL-Statement, not NULL when pbzUtf8Sql contains multiple SQL-Statements. |

Compiling An SQL Statement

To execute an SQL statement, it must first be compiled into a byte-code program using this routine. Or, in other words, this routine is a constructor for the prepared statement object.

The first argument, pSqlite3 , is a database connection obtained from a prior successful call to FuSqlite3_Open() . The database connection must not have been closed.

Interface variables Compiling An SQL Statement To execute an SQL statement, it must first be compiled into a byte-code program using this routine. Or, in other words, this routine is a constructor for the prepared statement object. The first argument, pSqlite3 , is a database connection obtained from a prior successful call to FuSqlite3_Open() . The database connection must not have been closed.

## FuSqlite3_Reset (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Reset | DINT |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to a Statement Object |

Reset A Prepared Statement Object

Interface variables Reset A Prepared Statement Object

## FuSqlite3_Step (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSqlite3_Step | DINT |  |
| Input | pSqlite3Stmt | POINTER TO typSQLite3_Stmt | Pointer to the sqlite3 statement |

Evaluate A SQL Statement Advance a typSqlite3_Stmt to the next result row or to completion.

Interface variables Evaluate A SQL Statement Advance a typSqlite3_Stmt to the next result row or to completion.

## FuSqlite3_Version_Number (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuSqlite3_Version_Number | DINT |

Receive Version Number of SQLite Database.

Interface variables Receive Version Number of SQLite Database. - Returns version number as integer value.

### Program Organization


## 20 Program Organization Units


- FuSqlite3_Bind_Blob (FUN) - FuSqlite3_Bind_Double (FUN) - FuSqlite3_Bind_Int (FUN) - FuSqlite3_Bind_Int64 (FUN) - FuSqlite3_Bind_Text (FUN) - FuSqlite3_Clear_Bindings (FUN) - FuSqlite3_Close (FUN) - FuSqlite3_Column_Blob (FUN) - FuSqlite3_Column_Bytes (FUN) - FuSqlite3_Column_Double (FUN) - FuSqlite3_Column_Int (FUN) - FuSqlite3_Column_Int64 (FUN) - FuSqlite3_Column_Text (FUN) - FuSqlite3_Errcode (FUN) - FuSqlite3_Errmsg (FUN) - FuSqlite3_Finalize (FUN) - FuSqlite3_Open (FUN) - FuSqlite3_Prepare (FUN) - FuSqlite3_Reset (FUN) - FuSqlite3_Step (FUN) - FuSqlite3_Version_Number (FUN)

### Internal Components


## WagoSysSQL_SQLite_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysSQL_SQLite_Internal_PFC |
| Version: | 1.0.0.2 |
| Categories: | WAGO FunctionalView\|Base; WAGO LayerView\|Sys |
| Namespace: | WagoSysSQL_SQLite_Internal_PFC |
| Author: | WAGO/u014042 |
| Placeholder: | WagoSysSQL_SQLiteInternal |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Functions providing access to SQLite3 databases [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Functions providing access to SQLite3 databases [1]

### Contents:


- 20 Program Organization Units FuSqlite3_Bind_Blob (FUN) - FuSqlite3_Bind_Double (FUN) - FuSqlite3_Bind_Int (FUN) - FuSqlite3_Bind_Int64 (FUN) - FuSqlite3_Bind_Text (FUN) - FuSqlite3_Clear_Bindings (FUN) - FuSqlite3_Close (FUN) - FuSqlite3_Column_Blob (FUN) - FuSqlite3_Column_Bytes (FUN) - FuSqlite3_Column_Double (FUN) - FuSqlite3_Column_Int (FUN) - FuSqlite3_Column_Int64 (FUN) - FuSqlite3_Column_Text (FUN) - FuSqlite3_Errcode (FUN) - FuSqlite3_Errmsg (FUN) - FuSqlite3_Finalize (FUN) - FuSqlite3_Open (FUN) - FuSqlite3_Prepare (FUN) - FuSqlite3_Reset (FUN) - FuSqlite3_Step (FUN) - FuSqlite3_Version_Number (FUN) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysSQL_SQLite_Internal_PFC.library, last modified 14.01.2019, 19:31:01. The content of this file was automatically generated with None on 14.01.2019, 19:31:04 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 10.01.2018 | 1.0.0.2 | u013972 | Add placeholder property |
| 08.01.2019 | 1.0.0.1 | u015842 | Properties: copyright added |
| 22.02.2017 | 1.0.0.0 | u014042 | Initlial released Version |

WagoSysSQL_SQLite.library

Release Notes: This library needs PFC-XXX firmware >= 12.

WagoSysSQL_SQLite.library Release Notes: This library needs PFC-XXX firmware >= 12.