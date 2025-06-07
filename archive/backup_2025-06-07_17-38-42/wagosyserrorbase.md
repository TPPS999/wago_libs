# WagoSysErrorBase v1.6.2.6

## Overview
WAGO PLC library providing WagoSysErrorBase functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbShowResult
Show comfortable the content of a result object This function block is to split a result object to output variables for comfortable showing the content inside the IDE. The output xError is TRUE while severity equal error or equal exception.

### FbResult
The fundamental object which represents an result. A result may be an error or a status. It contains a reference to an ResultItem object, which represents the result itself, and a reference to the producing object, which gives more details about the circumstances of the erroneous behaviour. Its construction method SetUp() is not too comfortable, but it is intended to use a Factory object (FbResultProducer) for this task anyway. There are two cases to set this result object. case 1 : There is an error or an status occured in your FB In this case you have to use your result factory (FbResultFactory) to set this result object.

**Methods:**

#### GetSeverityAsString
Gets the severity as string of the represented result

#### IsError
Returns TRUE if the represented result is an error or an exception.

#### ShowResult
This method provide to show the result content directly in CFC with one call This function block is to split a result object to output variables for comfortable showing the content inside the IDE in CFC. The output xError is TRUE by severity equal error or exception.

#### GetSeverity
Gets the enumeration value severity of the represented result

#### GetAuxInfo
Gets auxiliary information which is stored together with the result object

#### GetResultObject
Gets an interface of this object

#### GetLogLevel
Gets the log level of the represented result

#### GetInstancePath
Gets the tree representation (path) of the instance which has thrown the result. For performance this is the factory path that set last modification at this result.

#### SetUp
Construct a Result Object from the ResultItem and the Producer information

#### GetID
Gets the numerical ID of the result

#### GetProducerName
Gets the class name of the function block which has thrown the result

#### GetDescription
Gets the description string of the result

### FbResultFactory
**Methods:**

#### SetResultWithAuxInfo
Produces an FbResult-Object from a given ID and adds auxiliary information

#### SetProducerName
Assign a name to this factory. This name will be connected to the produced FbResult objects.

#### SetResult
Produces a result-object from the given ID and from the list which is attached to the factory

#### SetResultList
Attaches a list of results to the factory (only one list can be attached simultaneously)

#### GetProducerName
Retrieves the class name of the producing FB

#### GetInstancePath
Gets the tree representation (path) of this instance.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbShowResult: FbShowResult;
END_VAR

// Basic function block usage
fbFbShowResult(
    // Configure inputs as needed
);

// Check status
IF fbFbShowResult.xValid THEN
    // Operation successful
END_IF

IF fbFbShowResult.xError THEN
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

