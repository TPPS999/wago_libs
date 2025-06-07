# WagoAppDatalogger v1.0.5.6

## Overview
WAGO PLC library providing WagoAppDatalogger functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbDatalogger
Function block for Datalogging with WAGO I/O System

**Description:**
The FbDatalogger function block logs entries from up to 160 channels at an interval of min. one second in a CSV file. The CSV file can be generated in 3 different formats: #. Standard Wago datalogger format #. Econ format #. Dataplotter format: Specific for the ``Dataplotter`` Web application. .. note:: the Dataplotter can only display up to 80 channels. The Parameter MAX_CHANNELS under ParameterList has to be set to a maximum of 80 Due to the limitation of the maximum number of files in the root directory of the storage medium, the FbDatalogger function block forces a subdirectory called “CSV_Files”, in which the CSV files are stored. If the file path contains a subdirectory already, “sPath” is kept unchanged. The “sPath” file path specified is adjusted automatically. Example: #. “/media/sd/logfile.csv” → “/media/sd/CSV_Files/logfile.csv” #. “/media/sd/Tag1/logfile2.csv” → “/media/sd/Tag1/logfile2.csv” The FbDatalogger function block checks if a folder with the specified “sPath” file path already exists. If not, the FbDatalogger function block creates the folder automatically. Setting the "typConfigParameters.xAppendDate" input appends the current date of the controller to the file name. Therefore a new file is generated every day because the file name changes every day. Setting the "typConfigParameters.atypChannelConfig.xLogAlarm" appends another column to the end of the respective channel in the file in which an alarm is marked with "1" and no alarm with "0". (This is only relevant for the "Standard Wago datalogger format"). The "xEvent" input triggers the logging operation once. It should should be taken into account when using trigger times less than one second that the function block has set the "xReady" output to TRUE to avoid possible complications associated with a wrongly opened file. The output "xReady" represents a feature for coordinating the simultaneous access to a single file from different Instances of FbDatalogger. -Note specifically about Econ format "bDatalogger_type

## Data Types

### typChannelConfig
Structure type.

### typChannelConfigIntern
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbDatalogger: FbDatalogger;
END_VAR

// Basic function block usage
fbFbDatalogger(
    // Configure inputs as needed
);

// Check status
IF fbFbDatalogger.xValid THEN
    // Operation successful
END_IF

IF fbFbDatalogger.xError THEN
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

