# WagoAppSQL_MySQL v1.6.2.6

## Overview
WAGO PLC library providing WagoAppSQL_MySQL functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbMySql_Login
This function block is used to set up and monitor the connection to a MySQL-Server. ATTENTION: This function block has to be called within every PLC cycle!!!

### FbMySql_Logout
This function block is used to close the connection to a MySQL-Server

### FbMySql_Query
This function block is used to send SQL "SELECT" statements to a server which responds with result sets.

**Description:**
Remarks for ``aSqlStatement``: You can modify the "length" and number of elements in "aSqlStatement" by the global constants from the ParameterList: | - MYSQL_SQL_UPPER_BOUND: | Defines the UpperBound of ``aSqlStatement``, to provide a SQL statement | as "ARRAY [0..MYSQL_SQL_UPPER_BOUND] OF STRING(MYSQL_SQL_LENGTH)" | - MYSQL_SQL_LENGTH: | Defines the Size in byte of an array element of ``aSqlStatement``, | to provide a SQL statement as "ARRAY [0..MYSQL_SQL_UPPER_BOUND] OF STRING(MYSQL_SQL_LENGTH)". All non numeric SQL param values must be "quoted" with an apostroph('). Apostroph(') is also CoDesys-String-Start-End-Identifier. To use an apostroph(') inside a CoDeSys-String type $27 or $'.

### FbMySql_Execute
This function block is used to send SQL statements, such as: | INSERT, UPDATE, DELETE, ALTER, DROP, ... to a server which does not respond with a result set.

**Description:**
Remarks for ``aSqlStatement``: You can modify the "length" and number of elements in "aSqlStatement" by the global constants from the ParameterList: |- MYSQL_SQL_UPPER_BOUND: | Defines the UpperBound of ``aSqlStatement``, to provide a SQL statement | as "ARRAY [0..MYSQL_SQL_UPPER_BOUND] OF STRING(MYSQL_SQL_LENGTH)" | - MYSQL_SQL_LENGTH: | Defines the Size in byte of an array element of ``aSqlStatement``, | to provide a SQL statement as "ARRAY [0..MYSQL_SQL_UPPER_BOUND] OF STRING(MYSQL_SQL_LENGTH)". All non numeric SQL param values must be "quoted" with an apostroph('). Apostroph(') is also CoDesys-String-Start-End-Identifier. To use an apostroph(') inside a CoDeSys-String type $27 or $'.

## Data Types

### eStatus
Enumeration type.

### typMySql_ResultSet
Structure type.

### typMySql_FieldInfo
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbMySql_Login: FbMySql_Login;
END_VAR

// Basic function block usage
fbFbMySql_Login(
    // Configure inputs as needed
);

// Check status
IF fbFbMySql_Login.xValid THEN
    // Operation successful
END_IF

IF fbFbMySql_Login.xError THEN
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

