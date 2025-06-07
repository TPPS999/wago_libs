# WagoAppControl v1.6.2.0

## Overview
WAGO PLC library providing WagoAppControl functionality.

**Key Features:**
- Control functions
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbWagoApplicationControl
This Fb provides control about starting, stoppping, and resetting of other applications.

**Description:**
For operation, the FB is attached to the desired application with the method ``AttachToApplication()``. Once the Fb is successfully attached to the controlled application, this application may be started, stopped or reset by the corresponding methods. The output 'xBusy' indicates that certain asynchronous operations (e.g. stop()) are still pending and that the desired state has not yet been reached. When the state of the application has reached its target state, xBusy will return to FALSE again. Typical usage: :: VAR Ctrl : FbWagoApplicationControl; END_VAR Ctrl(); // cyclic operation for updating outputs IF not xInitialized THEN IF Ctrl.AttachToApplication('OtherApplication') <>0 THEN React_Adequately_Upon_Missing_OtherApplication(); END_IF xInitialized :

**Methods:**

#### getAppName
Retrieves the name of the attached application.

Returns an empty string, if no application is attached.

#### ResetApplicationOrigin
Resets the attached application (origin).

This process might take some time. While the transition is not completed the output 'xBusy' is TRUE.

#### ResetApplicationWarm
Resets the attached application (warm).

This process might take some time. While the transition is not completed the output 'xBusy' is TRUE.

#### ResetApplicationCold
Resets the attached application (cold)

This process might take some time. While the transition is not completed the output 'xBusy' is TRUE.

#### StopApplication
Stops the attached application.

This process might take some time. While the transition is not completed the output 'xBusy' is TRUE.

#### StartApplication
Starts the attached application.

This process might take some time. While the transition is not completed the output 'xBusy' is TRUE.

#### Detach
Releases the control

Note (1): Technically, the use of Detach() is neither mandatory nor strictly needed. However, it is good practice to use Detach(), because in this case subsequent calls of StopApplication() etc. would not stop any application which has been attached previously but whos attachment is obsolete now. Note (2): This method never fails (always returns OK), because there is no interaction with any previously attached applications.

#### AttachToApplication
Attaches the FB to a named application.

An empty string denotes *this* application, i.e. the application which issues the call.

### FbWagoPlcOperationControl
Temporarily disabling critical PLC operations.

**Description:**
This FB provides means for temporarily preventing the PLC from being stopped, written to or being otherwise manipulated by external means. Additionaly to the fundamental functiatity, a pair of

**Methods:**

#### LeaveSection
Restores the allowances for PLC operations.

The PLC operation flags are restored to that state, which was stored by the preceding EnterSection() call.

#### EnterSection
Disables a set of certain PLC operations.

Before disabling the referred operations this method stores the previous state internally. Later, the stored state will be effective again after the corresponding LeaveSection() method has been called. The set of PLC operations which were allowed before this call becomes effective is provided as the return value of this method. There is *no* nesting implemented for this method pair. When EnterSection() is called successively without calling LeaveSection() inbetween, further PLC operations may be disabled by these calls. The next LeaveSection() will restore the state from before the first EnterSection() call was issued. Only one LeaveSection() is needed for a series on EnterSections(). Note (1): As a consequence of this, if *EnterSection()* is called when the program flow has already entered a section (and not left it again), the returned value is *not* necessarily the state which will be restored with *LeaveSection()*. Note(2): The addressed properties are only *disabled* by this call. If they are not addressed here, the will *not* be automatically enabled, but they are left in their current state. Typical usage: :: VAR CriticalSection: FbWagoPlcOperationControl; END_VAR CriticalSection.EnterSection(ePlcOp.Stop + ePlcOp.Download + ePlcOp.OnlineChange); : // : // stopping, downloading, and online-change are disabled here : // CriticalSection.LeaveSection();

## Data Types

### eAppState
Enumeration type.

This represents the execution status of an application.

### ePLCop
Enumeration type.

This represents the arguments for FbWagoPlcOperationControl.Enter()

The values are intended to be superimposed in a way like like: :: EnterSection(ePLCop.Stop OR ePLCop.Reset); When a bit is set in a variable of this type, the corresponding feature is

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbWagoApplicationControl: FbWagoApplicationControl;
END_VAR

// Basic function block usage
fbFbWagoApplicationControl(
    // Configure inputs as needed
);

// Check status
IF fbFbWagoApplicationControl.xValid THEN
    // Operation successful
END_IF

IF fbFbWagoApplicationControl.xError THEN
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

