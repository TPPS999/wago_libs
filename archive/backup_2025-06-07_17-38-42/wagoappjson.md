# WagoAppJSON v1.1.0.32

## Overview
WAGO PLC library providing WagoAppJSON functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbHandleGetSingleKeyValue
**Methods:**

#### JSON_ValueDetected
#### JSON_KeyDetected
### FbJSON_Handler
This function block must be extended by an own function block. The different methods may be used according to the special needs of each application.

**Methods:**

#### JSON_NullDetected
#### JSON_ValueDetected
Called each time a JSON value has been evaluated

#### JSON_ObjectDetected
Called each time an object open "{" has been evaluated

#### JSON_ObjectClosed
Called each time an object close "}" has been evaluated

#### JSON_KeyDetected
Called each time a JSON key has been evaluated

#### JSON_DataFinished
This method is called after the last byte has been detected

#### JSON_ArrayDetected
Called each time an array open "[" has been evaluated

#### JSON_ArrayClosed
Called each time an array close "]" has been evaluated

### FbJSON_Sax_Parser
This function block parses the JSON data.

**Methods:**

#### RegisterParserListener
This method registers a JSON handler to this parser.

### FbJsonCreate
This function block is only for internal use with LIM.

**Description:**
An IEC variable must be defined by the user. The variable must be of typMain. e.g.: .. code-block:: codesys TYPE typMain: STRUCT EDL_DataBase: typElement; END_STRUCT END_TYPE

### FbJson_Advanced
This function block provides the base methods which are needed by the WagoJSON.py python script. WagoJSON.py will automatically generate a function block FbUserJson to read and write a JSON string into or from an IEC variable.

**Description:**
An IEC variable must be defined by the user. The variable must be of typMain. e.g.: .. code-block:: codesys TYPE typMain: STRUCT EDL_DataBase: typElement; END_STRUCT END_TYPE

### FbGetSingleKeyValue
Get a single value defined by a Key from a given JSON string

**Description:**
This function block gets the value from a Key value pair within a large JSON string. Only useful, if only one value withhin a large JSON string is important. Otherwise the use of the Sax-Parser is recommended.

### Fb_JSON_Writer_02
Generate a JSON string from a base template and an array with appropriate JSON values Other than Fb_JSON_Writer_01 this block allows some more flexibility by skipping key value pairs from the basic template string.

**Description:**
This function block generates a JSON string ``sOutput``. All variable values must be replaced by ``#Parameter`` to allow inserting the actual values from the input ``aParameterValues``. Additional it is possible to skip key value pairs. Therefor the value in the array ``aParameterValues`` must be set to ##. This may be changed in the parameterlist by ``JSON_SKIP_STRING``.

### FbWrite_ToIEC_ByRule
Write a JSON string to a variable defind by the user within the IEC-61131 program

**Description:**
This function block imports JSON data, which is stored as an array, to a codesys variable. JSON data may look like: | { | "Data_Objects":[ | { "t1": 1519, "chan": 5, "rx": 1.9, "payload":"567"}, | { "t1": 16786, "chan": 2, "rx": 5.1, "payload": "110a000f00551001"} | ] | } Therefore a variable may be defined as: .. code-block:: codesys VAR MyJsonData:ARRAY[0..1] OF typCustomData; END_VAR with .. code-block:: codesys {attribute 'pack_mode' :

### Fb_JSON_Writer_01
Generate a JSON string from a base template and an array with appropriate JSON values

**Description:**
This function block generates a JSON string ``sOutput``. All variable values must be replaced by ``#Parameter`` to allow inserting the actual values from the input ``aParameterValues``.

### Fb_JSON_ParseAndModify
Parse a JSON string and allow reading and modifying JSON values

**Description:**
Using this block, needs at least one time running the build up process by using input ``xTrigger``. The method ``GetValueByPath`` allows reading a JSON value. The method ``SetValueByPath`` allows writing a JSON value. .. Note: If a large JSON string must be evaluated, this method will increase the cycle time heavily

**Methods:**

#### GetValueByPath
This method allows reading a JSON value identified by ``sPointer`` according to JSON pointer syntax (RFC6901):

Example JSON string: .. code-block:: codesys json_string2: STRING(400):

#### SetValueByPath
This method allows writing a JSON value identified by ``sPointer`` according to JSON pointer syntax (RFC6901):

## Data Types

### eStatus
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbHandleGetSingleKeyValue: FbHandleGetSingleKeyValue;
END_VAR

// Basic function block usage
fbFbHandleGetSingleKeyValue(
    // Configure inputs as needed
);

// Check status
IF fbFbHandleGetSingleKeyValue.xValid THEN
    // Operation successful
END_IF

IF fbFbHandleGetSingleKeyValue.xError THEN
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

