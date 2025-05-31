# WagoAppSQL_MsSQL v1.6.2.2

## Overview
WAGO PLC library providing WagoAppSQL_MsSQL functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbMsSql_Login
This function block is used to set up the connection to a MsSQL-Server

### FbMsSql_Logout
This function block is used to close the connection to a MsSQL-Server

### FbMsSql_Query
This function block is used to send SQL "SELECT" statements to a server which responds with result sets.

**Description:**
Error code ``InvalidResponse`` indicates a mal formated packet. In this case the function block will close the connection. Remarks for ``aSqlStatement``: You can modify the "length" and number of elements in "aSqlStatement" by the global constants from the ParameterList: | - MSSQL_SQL_UPPER_BOUND: | Defines the UpperBound of ``aSqlStatement``, to provide a SQL statement | as "ARRAY [0..UpperBound] OF STRING(Size)" | - MSSQL_SQL_LENGTH: | Defines the Size in byte of an array element of ``aSqlStatement``, | to provide a SQL statement as "ARRAY [0..UpperBound] OF STRING(Size)". All non numeric SQL param values must be "quoted" with an apostroph('). Apostroph(') is also CoDesys-String-Start-End-Identifier. To use an apostroph(') inside a CoDeSys-String type $27 or $'. .. note:: This block must be used in the same task as FbMsSql_Login

### FbMsSql_Execute
This function block is used to send SQL statements, such as: | INSERT, UPDATE, DELETE, ALTER, DROP, ... to a server which does not respond with a result set.

**Description:**
Remarks for ``aSqlStatement``: You can modify the "length" and number of elements in ``aSqlStatement`` by the global constants from the ParameterList: | - MSSQL_SQL_UPPER_BOUND: | Defines the UpperBound of ``aSqlStatement``, to provide a SQL statement | as "ARRAY [0..MSSQL_SQL_UPPER_BOUND] OF STRING(MSSQL_SQL_LENGTH)" | - MSSQL_SQL_LENGTH: | Defines the Size in byte of an array element of ``aSqlStatement``, | to provide a SQL statement as "ARRAY [0..MSSQL_SQL_UPPER_BOUND] OF STRING(MSSQL_SQL_LENGTH)". All non numeric SQL param values must be "quoted" with an apostroph('). Apostroph(') is also CoDesys-String-Start-End-Identifier. To use an apostroph(') inside a CoDeSys-String type $27 or $'.

## Data Types

### eStatus
Enumeration type.

### typMsSql_ResultSet
Structure type.

### typMsSql_Column
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbMsSql_Login: FbMsSql_Login;
END_VAR

// Basic function block usage
fbFbMsSql_Login(
    // Configure inputs as needed
);

// Check status
IF fbFbMsSql_Login.xValid THEN
    // Operation successful
END_IF

IF fbFbMsSql_Login.xError THEN
    // Handle error
END_IF
```

## Best Practices

### Error Handling
```iec
IF fbInstance.xError THEN
    CASE fbInstance.eStatus OF
        // Handle specific error codes
    END_CASE
END_IF
```

### Performance Considerations
- Use appropriate polling intervals
- Handle communication errors gracefully
- Consider device response times
- Test thoroughly in target environment

## Important Notes

- This documentation was automatically generated from XML specification
- Always refer to official WAGO documentation for complete details
- Test thoroughly in your specific application environment
- Check library compatibility with your PLC hardware

