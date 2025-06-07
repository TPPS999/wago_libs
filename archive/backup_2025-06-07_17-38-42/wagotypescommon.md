# WagoTypesCommon v1.6.0.0

## Overview
WAGO PLC library providing WagoTypesCommon functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### Fb_GenericRunner
**Description:**
For usage, derive a new class from this base and add input and output variables as necessary. Put whatever the function is supposed to do into the method ``run()``. Parameters are expected to be passed via member variables of the derived class.

**Methods:**

#### run
This method is called when the runner is executed.

This method is expected to be implemented (overwritten) by derived classes. In this fundamental state of definition, no assumptions are made for return values. Thus, if not used, the return value might have undefined behaviour. It is, however, good paractice to return at least ``0

## Data Types

### eSeverity
Enumeration type.

Indicates a level how severe a message, event, or report, etc. is. This is used mainly for logfiles.

### eChar
Enumeration type.

Standard ASCII definitions for assigments to BYTE like b := Char.Slash;

### typWagoTimeComponents
Structure type.

This struct contains all information to directly print a calendarial representation of the local time. Note (1): iYearOffsetForWoY denotes a year shift concerning the actually calculated calendar week. It is - ``0`` in regular cases, - ``-1`` if the week is last week of previous year, (e.g. at 01.01.2012, which is in week 52/2011). - ``+1`` if the week is first week of following year (e.g. at 31.12.2013, which is in week 01/2014). So when referencing the year, according the calender week, this value must be added to the year number. Note (2): ``bAmbiguityModifier`` is regularly set to ' ' if the structure is returned from some function in order to distinguish it from the default state ``0``. It is 'A' OR 'B' when the hour is considered, when the timezone switches from DST to ST and the hour 02:00-02:59 appears twice. The hour 02:xx in DST is denoted with 'A' and the following one, (associated to ST) is denoted with 'B' Note (3) the first components of this structure are binary identical to ``SysTimeRtc.SYSTIMEDATE``, but they could not be inherited from there directly due to technical reasons.

### typRTS_SYSTIMEDATE
Structure type.

Paraphrasis of SysTimeRtc.SYSTIMEDATE.

This struct is a direct paraphrasis of ``SysTimeRtc.SYSTIMEDATE``, because that struct is defined abiguously between different library versions and thus is not usable as base structure. Here we have taken the original definitions as temporary replacement for the original structure (which is defined in SysTimeRtc) until this issue is solved. Use this type in new code rather than ``SysTimeRtc.SYSTIMEDATE``.

### typTimeZoneDescription
Structure type.

Information about a timezone.

``iOffset:`` For obtaining the local time with respect to this time zone, this offset (in minutes) has to be added to the GMT value. This iOffset corresponds directly to the value which is given e.g. in ``GMT+0100`` for central european time (1 hour + 0 minutes

### eSchedulingMode
Enumeration type.

This enumeration controls the details of asynchronous scheduling of an FB.

This type is used as input parameter for asynchronous scheduling of jobs. The following values are used: eSchedulingMode.Synchronous: This mode represents execution within the synchrounous IEC task context. The execution is not deferred to other tasks, but takes place immediatelly after calling and blocks the calling application during execution. Note: This mode is mostly used when developing own asnchronous FBs. eSchedulingMode.RealTimeHigh (

### eSeekMode
Enumeration type.

Mode for File-Seek

When a positioning (``Seek()``) is performed within a file, you have to specify the reference index for positioning the new write pointer.

### eFileSyncMode
Enumeration type.

Controls when data is actually written to the physical media.

### typFileProperties
Structure type.

Meta-Information about files or direcories .. note:: The function ``FbSysDir.Read()`` and ``GetFileProperties()`` (in file libraries) use this structure for returning information about files and directories.

### eFileAccessMode
Enumeration type.

Different modes of access (read, write, ... ) for opening files.

When opening a file, the application has to specify the mode of access for further operation. Four modes are defined: FAM_Write: Open write-only. The file will be truncated to zero (if exists) or newly created (if it does not exist) FAM_Read: Open read-only. File must exist. FAM_ReadWrite: Open for random access. File will be overwritten and pointer set to zero-pos (if exists) or file will be newly created (if it does not exist) FAM_Append: Open write-only. Filepointer will be set to End-Of-File if the file exists or the file will be newly created if it does not exist. Please note: These access modes may not match directly to linux or windows access modes.

### eResultCode
Enumeration type.

Operation return status, according to POSIX.1 (1996 edition). This list closely reflects the Posix definitions of error symbols which are used commonly in lots of situations and which should more or less cover a majority of standard situations. They are used here for the sake of international standardization. When functions report errors, however, typically only a small subset of these codes are used by a single function or function block. So, although the general meaning of these codes is listed here, the header of each function SHOULD contain a list of the result codes which are actually used there together with a description of the circumstances in which that function will return a specific code. When a function gets result codes from other functions, it is normally very bad style to pass this result code upwards without further analysis of the code, because the results might be not well-specified. Instead, the result code SHOULD be analyzed internally and mapped to that result code set which is specified in the header.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFb_GenericRunner: Fb_GenericRunner;
END_VAR

// Basic function block usage
fbFb_GenericRunner(
    // Configure inputs as needed
);

// Check status
IF fbFb_GenericRunner.xValid THEN
    // Operation successful
END_IF

IF fbFb_GenericRunner.xError THEN
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

