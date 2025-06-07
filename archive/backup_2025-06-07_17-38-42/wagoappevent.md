# WagoAppEvent v1.6.3.1

## Overview
WAGO PLC library providing WagoAppEvent functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbWagoEventCatcher
This is a Function block base for catching events.

**Description:**
*Usage:* Derive child FBs from this base and overload the protected method *protRun()* as demonstrated in the 'General' overview. When the event is posted, the protected method *protRun(typWagoEventInfo)* is executed. This runner method is provided with the full set of event parameters via its input Info: typWagoEventInfo Feedback from the runner is provided in two ways: a) If the parameter format indicates a "deny"-Option, the result code of the runner determines, if the event responses with "deny" (code<>0) or "accept" (code

**Methods:**

#### protRun
Runner method template for derived FBs.

This method is called, when the event is caught. Overload it with your own code. The input structure *Info* (:ref:`typWagoEventInfo <.fld-29 Types.typWagoEventInfo>`) provides information about the event identity, the parameter format and possible feedback locations.

#### GetEventCount
Returns how often an event has been caught by this FB.

The number of events of type eEventID is counted since registration. If the event has not been registered by this FB, -1 is returned. If only one event is registered and "0" is passed for the event-ID, the count of the only registered event is returned.

#### Finish
This method is called when the FB is unloaded.

This method is meant to be re-defined when additional cleanup code is required. Remember to call :: SUPER^.finish() in the child's finish()-method.

#### UnregisterAll
Unregisters all events from this FB.

#### Unregister
Unregister one event from the FB.

#### Register
Registering this FB to the specified event.

Note: More than one event can be registered to this FB simultaneously. The maximum number is given by ParameterList.cuiMaxEventsPerCatcher. If an event does not exist at the time of registering, it will be created automatically. In this case it will be deleted automatically when the event is unregistered again.

#### Initialize
This method is called when the FB is constructed.

You might redefine this method if required and insert some initializing registrations here: :: SUPER^.initialize(); // Original initialization. Always insert this! Register(eWagoEventID.DenyStop); // Additional: registering an event Register(eWagoEventID.PrepareDone); // Additional: registering another event Remember to call ``SUPER^.initialize()`` in the first line of the child's initialize()-method.

## Compact Function Blocks

### FbWagoSimpleEventCatcher_cpt
This is a FUP-oriented function block for catching single events.

**Description:**
This function block implements the behaviour model :ref:`'WagoAppChannel' <FbBehaviourModel_WagoAppChannel>`. For using the catcher FB, you are supposed to derive your own FB from this library FB and overload the method ``protRun`` with your specific functionality. (In the introducing section :ref:`'General' <.fld-10 Documentation.doc10_General>` an example is given. Although the example is formally written for the parent this FB (i.e. ``FbWagoEventCatcher`` instead of FbWagoSimpleEventCatcher_cpt), the code which is to be written for using any of these FBs is identical, because both FB differ only in the interface variables of the behaviour model.) The ``xOpen``-Input controls the registering and unregistering of the event. When the registered event is caught, the protected method ``protRun()`` is executed. This runner method is provided with the full set of event parameters via its input Info: :ref:`typWagoEventInfo <typWagoEventInfo>`. Feedback from the runner is provided in two ways: #. If the parameter format indicates a 'deny'-Option, the result code of the runner determines, whether the event is responded with 'deny' (code<>0) or 'accept' (code

**Methods:**

#### protRun
This is a runner method template for derived FBs of :ref:`FbWagoSimpleEventCatcher_cpt`.

This method is called, when the event is caught. Overload it with your own code. The input structure *Info* (:ref:`typWagoEventInfo <.fld-29 Types.typWagoEventInfo>`) provides information about the event identity, the parameter format and possible feedback locations. If the event catcher is expected to make a deny/allow decision, this method is expected to signalize 'allow' by a return value of 0

### FbWagoPostEvent_cpt
This is a FUP-oriented function block for posting events.

**Description:**
This FB implements the behaviour model :ref:`'WagoAppTrigger' <FbBehaviourModel_WagoAppTrigger>`.

## Data Types

### eWagoEventClass
Enumeration type.

### typWagoEventInfo
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbWagoSimpleEventCatcher_cpt: FbWagoSimpleEventCatcher_cpt;
END_VAR

// Basic function block usage
fbFbWagoSimpleEventCatcher_cpt(
    // Configure inputs as needed
);

// Check status
IF fbFbWagoSimpleEventCatcher_cpt.xValid THEN
    // Operation successful
END_IF

IF fbFbWagoSimpleEventCatcher_cpt.xError THEN
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

