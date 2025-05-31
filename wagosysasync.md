# WagoSysAsync v1.6.2.1

## Overview
WAGO PLC library providing WagoSysAsync functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### Fb_Daemon_Base
``Fb_Daemon_Base`` is a base class for asynchronous DAEMON-FBs.

**Description:**
*Overview* In the context of this library a 'daemon' is a functionality which runs repetitively or continuously in the background and which has only loose interactions with other applications. This FB is a base class for such a daemon according to the base model :ref:`WagoChannel <FbBehaviourModel_WagoChannel>`. Like for :ref:`GenericRunner <Fb_GenericRunner>` or :ref:`OneShot <Fb_AsyncOneShot_Base>`, the functionality is provided by the method ``run()``, while this base FB provides for the framework of starting with a certain scheduling mode or priority and of stopping the daemon again. For usage, the user is supposed to derive a child object from this base and implement the functionality in the *run()* method *Behaviour* When the input ``xOpen`` transits from ``FALSE`` to ``TRUE``, the daemon is scheduled according to the mode given by the input ``eSchedMode`` at that moment. E.g. as follows: :: eSchedMode :

**Methods:**

#### Run
This is the runner method of the daemon.

This runner is executed asynchronously. The user is supposed to implement his specific ``run()`` method according to his desired functionality. .. note:: This method is semantically a PROTECTED one, but for technical reasons it must be declared PUBLIC. Although there are no logical or technical restrictions in the base class, please, treat it as if it were PROTECTED in child classes.

### Fb_AsyncOneShot_Base
The ``Fb_AsyncOneShot_Base`` is a base class for a one-shot runner which is to be scheduled.

**Description:**
This function block provides for simple asynchronous deferring of a non-repetitive job. It behaves according to the :ref:`WagoTrigger <FbBehaviourModelWagoTrigger>`- behaviour model. The additional parameter :ref:`eSchedMode <eSchedulingMode>` controls the scheduling mode and/or priority. The scheduling mode can be given in various alternative ways, e.g.: :: eSchedMode :

### Fb_Run_Generic_Async
Runs a 'generic runner' asynchronously.

**Description:**
In contrast to the behaviour model classes, this FB is not meant in the first place to serve as a base for inheritance, but this one is intended to be used directly. Its main public method 'TriggerExecute()' takes a pointer to a generic runner FB as input. This runner can virtually be treated as a function pointer together with member variables. Its method 'run()' will be executed asynchronously. In contrast to the behaviour models, this runner is executed only once per trigger.

**Methods:**

#### Initialize
Initializes the FB.

This method sets the FB into a predefined state with appropriate variable settings. Use this in derived FBs for initialization: :: METHOD FB_Init : BOOL initialize(); METHOD initialize super^.initialize(); or (not suitable for further inheritance but shorter in simple cases): :: METHOD FB_Init : BOOL super^.initialize(); : : // my own initialization.

#### TriggerExecute
Starts the runner.

### FbBehaviourModelWagoEnableAsync
Base class for Wago Behaviour Model WagoEnable in asynchronous mode.

**Description:**
*Overview* For use the user has to re-implement the PROTECTED methods :ref:`protRun() <FbBehaviourModelWagoEnableAsync.protRun>` and :ref:`protTerminate() <FbBehaviourModelWagoEnableAsync.protTerminate>`. The first is the main runner wich is called periodically while ``xEnable`` is TRUE. The latter is used for controlled shutdown of the FB when ``xEnable`` is turned FALSE again. *States* This model has three internal states: Idle: The FB waits for ``xEnable`` to get ``TRUE`` and then transits to 'Run'. This state is indicated to the user by having ``xBusy`` reset to ``FALSE``. Note: ``xValid`` and ``xError`` are also reset in this state. Run: The FB calls :ref:`protRun() <FbBehaviourModelWagoEnableAsync.protRun>` while in this state. When ``xEnable`` gets ``FALSE``, it transits to 'Terminating' This state is indicated by having ``xBusy`` set ``TRUE`` while the ``xEnable``-Input is also set. Terminating: The FB calls :ref:`protTerminate() <FbBehaviourModelWagoEnableAsync.protTerminate>` while in this state. Depending on the result, it transits either to 'Idle' or to 'Run'. This state is indicated by having ``xBusy`` set ``TRUE`` while the ``xEnable``-Input is already reset to ``FALSE``. *Behaviour* While ``xEnable`` is ``TRUE``, the Method ``protRun()`` is executed asynchronously and repeatedly. As long as :ref:`protRun() <FbBehaviourModelWagoEnableAsync.protRun>` returns ``EAGAIN``, the FB output ``xValid`` is kept ``FALSE``. This output gets ``TRUE`` when ``protRun()`` returns OK. Other result codes will be interpreted as an error condition and they will be displayed accordingly at the outputs.

**Methods:**

#### protTerminate
Code for termination of activity.

(See FB description for details.)

#### Initialize
Initializes the FB.

This method sets the FB into a predefined state with appropriate variable settings. Use this in derived FBs for initialization: :: METHOD FB_Init : BOOL initialize(); METHOD initialize super^.initialize(); or (not suitable for further inheritance but shorter in simple cases): :: METHOD FB_Init : BOOL super^.initialize(); : : // my own initialization.

#### protRun
Code for the main functionality.

(See FB description for details.)

### FbBehaviourModelWagoTriggerAsync
Base class for behaviour model WagoTrigger in an asynchronous context.

**Description:**
*States* This model has three internal states NotInitialized: The very first cycle in the life of an application. As xAction cannot be reset during initialization due to technical reasons, it is initialized in this first cycle. This state is indicated by ``eStatus`` being set to ``EDEFAULT``. The value of ``xTrigger`` is not defined at this moment. The FB transits into ``Idle`` from this state within one cycle. Idle: The FB waits for xAction to become TRUE, then transits to 'Run'. This state is indicated by having ``xTrigger`` reset to ``False`` and ``eStatus`` having set to anything other than ``EDEFAULT``. Run: The FB calls protRun() repeatedly until it returns OK or any code other than EAGAIN, then transits to Idle and resets xAction again. This state is indicated by having ``eStatus`` set temporarily to ``EINPROGRESS`` and ``xTrigger`` not being reset. Upon termination of the action, ``eStatus`` will be set either to ``OK`` or to the returned error code. .. note:: When this model is used, the application is *strongly recommended* to ensure that ``xAction`` is never reset to FALSE from outside of this FB. From outside, ``xAction`` should only be set to TRUE, never to FALSE. .. note:: When the action returns either EINPROGRESS or EDEFAULT, that code will be re-mapped to EUNSPECIFIC in order to avoid ambiguities if eStatus.

**Methods:**

#### Initialize
Initializes the FB.

This method sets the FB into a predefined state with appropriate variable settings. Use this in derived FBs for initialization: :: METHOD FB_Init : BOOL initialize(); METHOD initialize super^.initialize(); or (not suitable for further inheritance but shorter in simple cases): :: METHOD FB_Init : BOOL super^.initialize(); : : // my own initialization.

#### protRun
Code for the main functionality.

See FB-description for details.

### FbBehaviourModelWagoExecuteAsync
Base class for asynchronous behaviour model WagoExecute.

**Description:**
*States* This model has three internal states: Idle: The FB waits for xExecute to transit from FALSE TO TRUE, then transits itself to 'Run'. This state is indicated to the user by having ``xDone`` and ``xBusy`` both reset to FALSE. ``xError`` is also reset in this state. Run: The FB calls protRun() repeatedly until protRun() returns OK or any other code than EAGAIN. This state is indicated by having ``xBusy`` set to TRUE and ``xDone`` reset to FALSE. Terminated: The FB waits for xExecute to return to FALSE level for at least one cycle, then transits to 'Idle'. This state is indicated by having ``xDone`` set to TRUE and ``xBusy`` reset to FALSE. The forth case, i.e. ``xDone`` and ``xBusy`` both set to TRUE is illegal and is prevented by the framework of this model (would be a programming error if it should occur.). *Behaviour* - Basic interface variables were cleared on FALSE level of xExecute. Interface Variables of derived FBs are not affected by this and stay at their values until the next Run-cycle. - While xDone or xError are not set yet, the output eStatus remains unchanged unless the derived FB overwrites it.

**Methods:**

#### protClearOutputs
Code for clearing user defined outputs.

This method is called each time when the FB transits into its idle state, i.e. when its status outputs were reset. At the time of call, the primary outputs (xDone, xError, eError) are not cleared yet, so this method has the full information about the circumstances of its call: - execution has terminated with error or not - initialization of FB (all outputs FALSE). This method has no return value.

#### Initialize
Initializes the FB.

This method sets the FB into a predefined state with appropriate variable settings. Use this in derived FBs for initialization: :: METHOD FB_Init : BOOL initialize(); METHOD initialize super^.initialize(); or (not suitable for further inheritance but shorter in simple cases): :: METHOD FB_Init : BOOL super^.initialize(); : : // my own initialization.

#### protRun
Code for main functionality.

See FB-description for details.

### Fb_VirtualMethodsForAsyncExecution
**Methods:**

#### protAsynchronousCleanup
Code for asynchronous cleanup.

When, in a derived FB, code for cleaning up is needed, which may run so long that it also has to be deferred to an asynchronous task, this code is to be placed in this method. Although it allows the return of a result code for uniformity reasons, the result will be discarded. Explanation: The eResult of the derived FB reflects the status of the main functionality, which is represented by protMainRun() rather than by protAsynchronousCleanup(). This method is not expected to run repeatedly but only once per trigger. The method should return OK. It should not return other codes, especially not EAGAIN.

#### protInitialize
Code for initialization in derived FBs.

This method will be called synchronously, i.e. directly after triggering the derived FB. This method is called from the base FB immediately (always synchronously) with the call of _TriggerExecute(), before the main run starts. It is intended to provide the initialization of the variables (esp. buffering of input variables) of the derived FB immediately after starting, while the (probably long-running) main process might be postponed asynchronously. When protInitialize() returns a result code other than OK (

#### protDone
Code for postprocessing.

This method provides synchronous post-processing after termination of the main task. This method allows for easy passing of output results from inner FB layers (e.g. the FILE object in an asynchronous File-FB or other local variables) to the output variables of the specialized FB. When using this, protMainRun() has to deal only with internal variables and is completely decoupled from the public interface. This method accepts as input the result code of the terminated process in order to allow for appropriate reactions to error conditions, if needed. It does not provide a result code itself, because it is not supposed to contain failable code.

#### protMainRun
Code for repeated asynchronous execution.

This method is executed asynchronously with native breakpoints at the end of each cycle. This method is called asynchronously following the synchronous call of protInitialize(). In contrast to the latter, ProtMainRun() is not guaranteed to start immediately, but in might be scheduled for future execution, depending on the scheduling mode. Typically, this method carries out the main (long-running) functionality of the derived FB. .. note:: Via the property 'CycleCount', protMainRun() is able to detect whether it is called initially or subsequently. Due to the potentially deferred execution, the input variables of the derived FB should not be processed directly within this method, because of the rather poorly defined timing. Instead they should be buffered from protInitialize() or from the derived trigger call. .. note:: The output 'xBusy' will be set synchronously with the _TriggerExecute() but this does *not* indicate that protMainRun() has yet started. The protMainRun() is supposed to return OK (

#### protAbortionCleanup
Code for cleaning up an aborted job.

When the processing of ths FB stops prematurely this method is called (always synchronously) to clean up the interrupted FB state. The cause of the premature stop could be: - TimeOut from the framework; - external AbortRequest signal; or - MainRun() returned with ECANCELED. If the cleanup could be finished normally, this method returns OK (

### Fb_Async_Base
``Fb_Async_base`` is a base FB for asynchronous execution of jobs. It is never instatiated directly but it serves as base class for deriving own FBs.

**Description:**
*Overview* Although this base FB has some uniform status outputs it is completely method driven. As indicated in the section 'General', the user is supposed to derive his own FB from this base FB and implement his own protected methods according to his needs. The asynchronous job is started with the PROTECTED method :ref:`_TriggerExecute() <Fb_Async_Base._TriggerExecute>` of the base interface. Typically, when the user derives his own FB, he will provide his own public ``Trigger()`` method for PUBLIC use, which sets up variables and then internally calls the PROTECTED :ref:`_TriggerExecute() <Fb_Async_Base._TriggerExecute>`. *General Application Rules* #. The body of the derived FB MUST contain ``super^();`` for using the execution logic. #. Unless especially noted, most methods of this FB are intended to be either PRIVATE or PROTECTED. I.e. they should never be called directly from outside of the class, even if not all of them are actually declared PRIVATE or PROTECTED for technical reasons. Either the child FB inherits these methods for direct protected usage or the child FB re-implements some (or all) of them. Thus, no component of the :ref:`PROTECTED Interface <fld-20 Program Organization Units.fld-30 Base Classes.Fb_Async_Base.fld-41 PROTECTED Interface>`) appears in the public interface of the child by default. The child is supposed to use its own wrapper methods or interface variables for making the desired subset of them accessible to the application. *Base FB Outputs* xTerminated: This output indicates that the execution is terminated, successfully or with errors. This output is cleared with successful calls of the methods :ref:`_TriggerExecute() <Fb_Async_Base._TriggerExecute>` or :ref:`_AcknowledgeTermination() <Fb_Async_Base._AcknowledgeTermination>`. xBusy: Indicates that :ref:`_TriggerExecute() <Fb_Async_Base._TriggerExecute>` has been executed successfully and that the job has not yet terminated. It is cleared after termination of the job. While set to TRUE this output indicates that other output variables may vary spontaneously. While set to FALSE, outputs do not vary spontaneously. xError: Indicates the presence of an error. Attn: This output may be TRUE simultaneously with other outputs. eResult: This indicates the actual state of processing or errors. While the job is not terminated, it displays EINPROGRESS which is not an error condition but just tells that the process is still in progress. The outputs are cleared with successful calls of the methods :ref:`_TriggerExecute() <Fb_Async_Base._TriggerExecute>` or :ref:`_AcknowledgeTermination() <Fb_Async_Base._AcknowledgeTermination>`. .. note:: The output interface resembles the behaviour model ``WagoExecute`` but it is not the same due to the many necesseties of method driven operation. For using the standard behaviour directly, other asynchronous FBs are derived from the base and provided by this library. Those are less flexible, but they carry the canonical interfaces of :ref:`WagoEnable (async) <FbBehaviourModelWagoEnableAsync>`, :ref:`WagoExecute (async) <FbBehaviourModelWagoExecuteAsync>`, and :ref:`WagoTrigger (async) <FbBehaviourModelWagoTriggerAsync>`. *Scheduling of protected methods* Depending on the input stimulus of the base interface, the virtual methods :ref:`protInitialize() <Fb_VirtualMethodsForAsyncExecution.protInitialize>`, :ref:`protMainRun() <Fb_VirtualMethodsForAsyncExecution.protMainRun>`, :ref:`protDone() <Fb_VirtualMethodsForAsyncExecution.protDone>`, :ref:`protAbortionCleanup() <Fb_VirtualMethodsForAsyncExecution.protAbortionCleanup>`, and :ref:`protAsynchronousCleanup() <Fb_VirtualMethodsForAsyncExecution.protAsynchronousCleanup>` were called from within the framework of the Fb_Async_Base. These methods (or some of them) should be re-implemented in the derived class according to following specifications given in the interface description :ref:`Fb_VirtualMethodsForAsyncExecution`. The outputs variables of the base FB are set according to the results of the function calls in derived FBs. Depending on the scheduling mode, the execution of these methods may be deferred to other asynchronous tasks in order to keep the calling instance non-blocking while waiting for the result during several cycles. This process is hidden from the application by the interface. Thus, the call to the derived FB may return even before the called functionalities have terminated. By observing ``xTerminated`` the calling application is notified that the execution in the background is terminated. The application may signal its wish for abortion of the FB's process either explicitly by the or :ref:`_Abort() <Fb_Async_Base._Abort>`-Method or implicitly by setting the property ``tTimeOut`` (0

**Methods:**

#### Initialize
Initializes FB_Async_Base.

This method sets the FB into a predefined state with appropriate variable settings. Use this in derived FBs for initialization: :: METHOD FB_Init : BOOL initialize(); METHOD initialize SUPER^.initialize(); or (not suitable for further inheritance but shorter in simple cases): :: METHOD FB_Init : BOOL SUPER^.initialize(); : : // my own initialization if necessary :

#### Finish
Tears down FB_Async_Base.

Normally you need not call it, because it is called automatically at exit. Use this in derived FBs for tearing down the FB after use: :: METHOD FB_Exit : BOOL : : // my own exit code here if necessary : SUPER^.finish();

#### _IsRunning
Indicates that the runner method is running.

This method is intended to differentiate between regular run and possible cleanup in derived FBs. It is not intended for use in external calls (PROTECTED).

#### _SetSchedulingParameters
Sets the scheduling parameters (mode, timeout).

Derived Objects must call this method at least once before letting an asynchronous job run. No check for parameter validity is done, thus this method always returns 'OK'. Please note that the parameter 'tTimeOut' does not cause a hard abortion of the runner, it rely signals a wish to the runner to terminate now cooperatively after a timeout has occurred. For the meaning of the scheduling modes, please refer to the section 'Common Type Definitions' below.

#### _Done
#### _IsReadyForExecution
Indicates that the FB is ready for execution.

This method returns TRUE if the FB is ready for scheduling the runner procedure. It returns FALSE if it is not ready, e.g. because the previous job is still running. This is especially intended to be used when copying of input parameters is required before triggering. :: FUNCTION_BLOCK Fb_MyAsyncExecutor EXTENDS Fb_Async_Base METHOD StartIt(InputParameter [...]) // Starting the intended procedure with specific parameters IF not _IsReadyForExecution() THEN // Check if copying the parameters is OK StartIt :

#### _AcknowledgeTermination
Acknowledges the termination of the runner.

After termination of the main runner this method sets the basic output variables back to their idle values and then transits the FB back into the idle state.

#### _TriggerExecute
Triggers the execution of the process.

#### _Abort
Signals the runner to abort cooperatively.

This method sets the flag for cooperative abortion, which will be evaluated by the runner process. When the runner detects this flag, it may cooperatively abort prematurely if this behaviour is implemented in the runner code. If the runner has returned EAGAIN (and has possibly has ignored the abortion signal), it will NOT be restarted after this method is called and the framework will show the result code ECANCELED. .. note:: This method does not unconditionally abort the runner. It merely sets flags which the runner may regard or disregard.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFb_Daemon_Base: Fb_Daemon_Base;
END_VAR

// Basic function block usage
fbFb_Daemon_Base(
    // Configure inputs as needed
);

// Check status
IF fbFb_Daemon_Base.xValid THEN
    // Operation successful
END_IF

IF fbFb_Daemon_Base.xError THEN
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

