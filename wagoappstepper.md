# WagoAppStepper v1.6.1.4

## Overview
WAGO PLC library providing WagoAppStepper functionality.

**Key Features:**
- Control functions
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbCAM_Table
Reading and writing of the terminals internal CAM table

**Description:**
Reading and writing of the terminals internal cam table RAM 1

### FbGetVariable
A base function block which allows to read any variable available by an index

### FbSetFilterValue
A base function block which allows to set the filter value

### FbMoveAbsolute_2
A base function block which allows an absolute movement of a stepper drive

**Description:**
The positioning job is defined by the inputs ``iSpeed``, ``wAcceleration`` and ``diPosition``. The parameter ``iSpeed`` is allowed in the range of 1..25000 while ``wAcceleration`` is allowed from 0..32767. The job will be started by the variable ``xEnable``. Parameter changes(``iSpeed`` or ``diPosition``) on the fly are supported.

### FbMoveVelocity_2
A base function block which allows velocity control of a stepper drive

**Description:**
This block allows changes of the velocity on the fly, so there is no need to disable the block if a new speed value is assigned. This behaviour is different to FbMoveVelocity.

### FbPositionTable
Reading or writing of the terminals internal position table

**Description:**
This function block allows to read and write the position table. Each position in the table is 4 byte long. Input ``bDataCount`` is the number of positions in the table. The size of the position table may be changed through ``POSITION_TABLE_SIZE`` in the parameter list.

### FbDriveProgramTable
Reading and writing of the terminals internal drive program table

**Description:**
If the input xWriteFlash is True the drive program will be stored to the flash memory after it is downloaded to the module. After power on reset the drive program is therefore still available and can be directly executed by using the function block ``FbDriveProgram``.

### FbStepperControlBasic
A base function block which allows to control a stepper drive

**Description:**
| This function block supports different modes of the stepper module: | 0: Absolute positioning | 1: Relative positioning | 2: Homing | 3: Jogging | 4: Velocity control | 6: Executing a drive program | 7: Torque controlled movement | 8: Torque controlled movement | 9: Set the actual position - Absolute positioning The positioning job is defined by the inputs iSpeed, wAcceleration, wDeceleration and diPosition. The parameter iSpeed is allowed in the range of 1..25000 while acceleration and deceleration are allowed from 0..32767. The job will be started by the variable xTriggerStart. If the job is done, the variable xTriggerStart will be reset by the functionblock. - Relative positioning The positioning job is defined by the inputs iSpeed, wAcceleration, wDeceleration and diPosition. The parameter iSpeed is allowed in the range of 1..25000 while acceleration and deceleration are allowed from 0..32767. The job will be started by the variable xTriggerStart. If the job is done, the variable xTriggerStart will be reset by the functionblock. - Homing The Homing job is defined by the inputs xDirPos or xDirNeg and xTriggerStart. The job will be started by the variable xTriggerStart. If the job is done, the variable xTriggerStart will be reset by the functionblock. Homing speed, acceleration and mode are defined through the values in the configuration table. - Jogging Depending on the module the jogging mode is started differently. 750-670,750-671: The Jogging job is defined by the inputs xDirPos or xDirNeg and xTriggerStart. The job will be started by the variable xDirPos or xDirNeg and xTriggerStart

### FbPWM_Mode_670
A base function block which supports PWM mode using module 750-670

**Description:**
High ``wAcceleration`` values ensure a quick increase of the pulswidth rate. Additional it may be necessary to increase the default value for ACC_Fact(see the configuration table) from 80 to 10000 to archieve an even steeper increase. Once started, changes in the input parameters will only be overtaken by a positive edge of the ``xEnable`` input.

### FbReadActualPosition
A base function block which allows to read the actual position of a stepper drive

**Description:**
This function block shows the actual position as well as the actual speed. The output ``bActualMode`` displays the operating modes according to the enumeration ``eMode``:

### FbReadError
A base function block which allows to read the error information of a stepper drive

**Description:**
If the module status 2.7 (error) is TRUE, the output ``xMouduleFault`` is set. If an error occured, detailed information will be read, using the mailbox command 0x49 ERR_GET. The details will be displayed in ``eFeedback``. Output ``xError`` will only be set, if the mailbox command 0x49 shows an error. The output ``xModuleFault`` will show directly status byte Status2.7.

### FbPower
Enable the power stage of a stepper drive

**Description:**
This function block must be used except for running the stepper drive by the function block FbStepperControlBasic. Bit 0 in the Control Byte 1 ist directly controlled. The output ``xStatus`` displays directly Bit 0 from Status Byte 1.

### FbReset
A base function block which allows to reset a stepper drive

**Description:**
This function block performs a reset. Bit 7 in the Control Byte 3 and Control Byte 2 ist directly controlled

### FbStop
A base function block which allows to stop a stepper drive

**Description:**
This function block must be used except for running the stepper drive by the function block FbStepperControlBasic. This functionblock allows to stop the stepper motor. The deceleration ramp is determined by the configuration value ``AccelerationStopFast``.

### FbRestoreDefault
Restore Default values

### FbSetPosition
A base function block which allows to set the actual position

### FbHome
A base function block which allows a homing movement of a stepper drive

**Description:**
This function block allows to start a homing job. Please make sure either ``xRefPositive`` or ``xRefNegative`` is choosen if the input "xExecute" becomes high. Homing mode, speed and acceleration a configured by the configuration table (Reference_Mode,SetupSpeed and SetupAcceleration).

### FbJog_670
A base function block which allows to jog the stepper modules 750-670 and 750-671

### FbConfigurationTable
Reading and writing the terminals internal configuration

**Description:**
This functionblock allows to read and write the configuration table at once. To start the process set ``xExecute`` to TRUE. If the action is finished the output ``xDone`` becomes True. The output ``oStatus`` shows any error. After writing the configuration table the modul resets itself. Therefore the actual position will be reset to Zero.

### FbConfigurationValue
Reading and writing of a single value within the configuration table

**Description:**
This functionblock allows to read and write a single parameter from the configuration table. Writing differentiates between temporarily changes(write to ram) which are lost after power on of the stepper modul and permanent(write to flash) changes.

### FbDriveProgram
Use the drive program capability of a stepper drive

**Description:**
This functionblock allows to execute a drive program. The input ``wStartPositionDriveProgram`` allows to determine the start address within the drive program. While setting up drive program mode, the output oStatus will show "InProgress". If the initialization is finished status OK will be set. Initialization will not start, if the function block FbPower is not active or the function block FbStop is activated. The variable wActualDriveProgramPosition shows the ProgramPosition of the next Position.

### FbJog_672
A base function block which allows to jog the stepper modules 750-672 and 750-673

**Description:**
The jogging is performed by digital inputs direct on the module.

### FbMoveTorque_673
A base function block which allows a torque movement of a stepper drive using module 750-673

### FbMoveVelocity
A base function block which allows velocity control of a stepper drive

### FbMoveAbsolute
A base function block which allows an absolute movement of a stepper drive

**Description:**
The input ``wAcceleration`` will be taken for the decelarion as well. The job will be started by the variable ``xExecute``. Parameter changes on the fly are not supported.

### FbMoveRelative
A base function block which allows a relative movement of a stepper drive

### FbMoveTorque2_673
A base function block which allows a torque movement of a stepper drive using module 750-673

## Data Types

### typStepperVisu_672
Structure type.

### typStepperVisu_671
Structure type.

### typStepperVisu_673
Structure type.

### typStepperVisu_670
Structure type.

### eStatus
Enumeration type.

### eMode
Enumeration type.

### typConfiguration_670
Structure type.

### typConfiguration_671
Structure type.

### typConfiguration_672
Structure type.

### typConfiguration_673
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbCAM_Table: FbCAM_Table;
END_VAR

// Basic function block usage
fbFbCAM_Table(
    // Configure inputs as needed
);

// Check status
IF fbFbCAM_Table.xValid THEN
    // Operation successful
END_IF

IF fbFbCAM_Table.xError THEN
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

