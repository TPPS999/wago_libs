# WagoSysBehaviourModels v1.6.3.1

## Overview
WAGO PLC library providing WagoSysBehaviourModels functionality.

**Key Features:**
- Communication protocols
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbBehaviourModel_AppTrigger_bare
This is a bare model for Wago Trigger with oStatus.

**Description:**
As this is a bare model, it has no graphical inputs nor outputs. The follwing variables are used for communication:

**Methods:**

#### protSetErrorFromMemberMethod
This method sets the general status outputs of the model according to the given status object.

If an error has occurred, ``xError`` will be set and ``xBusy`` and ``xDone`` will be reset.

#### initialize
#### protRun
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | The action has successfully terminated, reset xTxTrigger again. EAGAIN The action has to be repeated. other The action has terminated with an error, reset xTxTrigger again. ============= ============================================================== |

### FbBehaviourModel_AppChannelledTrigger_bare
Channelled Trigger with oStatus.

**Description:**
A Channelled trigger is a WagoCommunicator without a receiving channel. As this is a bare model, it has no graphical inputs nor outputs. The follwing variables are used for communication:

**Methods:**

#### protRun
Main runner. (For details see :ref:`general description of the model <FbBehaviourModel_AppChannelledTrigger_bare>`)

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | The action has successfully terminated, reset xTxTrigger again. EAGAIN The action has to be repeated. other The action has terminated with on error, reset xTxTrigger again. ============= ============================================================== |

#### protOpen
Opening the channel. (For details see :ref:`general description of the model <FbBehaviourModel_AppChannelledTrigger_bare>`)

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Opening of the channel was successfully completed. EAGAIN Opening still in progress. other Opening failed. Channel returns to idle state without calling close(). ============= ====================================================================== |

#### protClose
Closing the channel. (For details see :ref:`general description of the model <FbBehaviourModel_AppChannelledTrigger_bare>`)

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Closing of the channel was successfully completed. EAGAIN Closing still in progress. other Closing failed for some reason. ============= ================================================= |

#### initialize
### FbEmbeddedStatusHandler
Base object for all models wch use a result factory.

**Methods:**

#### IsNotInitialized
This method returns ``TRUE`` if the result factory is not properly initialized.

#### clearStatusObject
This method sets the result object to OK and erases all traces from previous errors.

#### setupResultFactory
This Method sets upt the details of the result catory.

#### setStatusObject
Reflects a result code to the output.

With this method a new result code is fed into the status handler. Depending on the constellation of the new result code and previous result codes a result object is generated or not. The return value ``TRUE`` undicates that a new object has been created, while the value ``FALSE`` indicates that the result object is left untouched. The output ``xError`` indicates, if an error (not in *info* nor a *warning* ) has occurred so far. A new object is created if - the severity of the new result is higher than the severity of any previous results or if - the previous result was in *information* - informations will be superseded by more actual informations and also by 'OK'. A result code ``OK`` will supersede only previous *information* objects but nothing else. This method is neither PROTECTED nor FINAL, because it my be overloaded in child classes for filtering results or it may be used to inject result codes.

### FbBehaviourModel_WagoAppExecute
This model is a base class for behaviour model WagoExecute with oStatus output.

**Description:**
*States* This model has three internal states: Idle: The FB waits for ``xExecute`` to transit from ``FALSE`` TO ``TRUE``, then transits to 'Run'. This state is indicated to the user by having ``xDone`` and ``xBusy`` both reset to ``FALSE``. Please note that ``xError`` is also reset in this state. Run: The FB calls ``protRun()`` repeatedly until ``protRun()`` returns ``OK`` or any code other than ``EAGAIN``. This state is indicated by having ``xBusy`` set to ``TRUE`` and ``xDone`` reset to ``FALSE``. Terminated: The FB waits for ``xExecute`` to return to ``FALSE`` for at least one cycle, then transits to 'Idle'. This state is indicated by having ``xDone`` set to ``TRUE`` and ``xBusy`` reset to ``FALSE``. .. note:: The forth case, i.e. ``xDone`` and ``xBusy`` both set to ``TRUE`` is illegal and is prevented by the framework of this model (would be a programming error if it did occur). *Behaviour:* - Base class interface variables are cleared when ``xExecute`` transits to ``FALSE``. Interface Variables of derived FBs are not affected by this and retain their values until the next Run-cycle. - The output ``oStatus`` remain unchanged as long as ``xDone`` or ``xError`` are not set yet, unless the derived FB overwrites them. The behaviour of the child FB is mainly controlled by the result code of the runner method:

**Methods:**

#### protSetErrorFromMemberMethod
This method sets the general status outputs of the model according to the given status object.

If an error has occurred, ``xError`` will be set and ``xBusy`` and ``xDone`` will be reset.

#### initialize
Initializes the FB WagoAppExecute at FB_Init().

Use this for inherited objects: :: SUPER^.Initialize();

#### protRun
The protected method ``protRun()`` is called after the rising edge of ``xExecute``.

With its result code this method indicates, if repetition is necessary.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Execution has successfully terminated, set xDone = TRUE. EAGAIN Execution is still in progress, repeat protRun() in next cycle. other Execution has terminated with an error. Display that code and set xError. ============= ========================================================================= |

#### protClearOutputs
This method is called each time the FB transits to its idle state, i.e. when its status outputs were reset.

*Application hints* At the time of the call, the primary outputs (xDone, xError, eError) have not yet been cleared, so this method has the full information about the circumstances of its call: - execution has terminated with or without an error; - initialization of FB (all outputs FALSE). This method does not return anything.

### FbBehaviourModel_WagoAppEnable
Base class for behaviour model PLCopenEnable with oStatus.

**Methods:**

#### protSetErrorFromMemberMethod
This method sets the general status outputs of the model according to the given status object.

If an error has occurred, ``xError`` will be set and ``xBusy`` and ``xDone`` will be reset.

#### protTerminate
As described in the general FB description.

**Result Codes:**
| Code | Description |
|------|-------------|
| OK=0 | Successful termination, return to state 'Idle'. ENOSYS Method is not implemented, return to 'state Idle'. EAGAIN Shutdown is in progress and must be resumed. EBREAKPT Shutdown in progress, but direct transit to 'Run' if xEnable=TRUE is enabled other Display error code. ============= ====================================================================================== |

#### initialize
Initializes FB at FB_Init().

Use this for inherited objects: :: SUPER^.Initialize();

#### protRun
As described in the general FB description.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Successful operation, set xValid EAGAIN Output variables not yet valid, reset xValid, eStatus := EINPROGRESS, xError := FALSE other Reset xValid, set eStatus to this code, set xError := TRUE ============= ====================================================================================== |

### FbBehaviourModel_WagoAppTrigger
This is a base class for behaviour model WagoTxTrigger with oStatus.

**Description:**
This base model is completely identical to ``WagoTrigger`` with the only difference that the trigger variable and the status output are named slightly differently here. *States* This model has three internal states: NotInitialized: The very first cycle in the life of an application. As ``xTrigger`` cannot be reset during initialization, due to technical reasons, it is initialized in this first cycle. This state is indicated by ``eStatus`` set to ``EDEFAULT``. The value of ``xTxTrigger`` is not defined at this moment. The FB transits into 'Idle' from this state within one cycle. Idle: The FB waits for ``xTxTrigger`` to be set to ``TRUE`` by external stimulus. Then the FB transits into 'Run'. The 'Idle' state is indicated by the FB having ``xTxTrigger`` reset to ``False`` and ``eStatus`` being set to anything other than ``EDEFAULT``. Run: The FB calls ``protRun()`` repeatedly until the runner returns either OK or any code other than ``EAGAIN``. Then the FB transits into 'Idle' and it resets ``xTxTrigger`` from within the FB framework again. The 'Run' state is indicated by having ``eStatus`` set intermediately to 'EINPROGRESS' and ``xTxTrigger`` not yet being reset. Upon termination of the action, ``eStatus`` will be set either to ``OK`` or to the error code. which was returned from the runner. .. note:: When this model is used, it is *strongly recommended* that the application never reset ``xAction`` to ``FALSE``. It should only be set to ``TRUE``. .. note:: When the action returns either ``EINPROGRESS`` or ``EDEFAULT``, that result code will be re-mapped to ``EUNSPECIFIC`` in order to avoid ambiguities with ``eStatus``. The overall behaviour is controlled by the result code of the runner:

### FbBehaviourModel_WagoAppCommunicator
This is a base class for behaviour model WagoAppCommunicator with oStatus outputs.

**Description:**
This base class is used for general communication needs. *Usage* This FB is composed of three separated sub-modules: Channel: This part controls the opening and closing of an associated communication channel. The description of ``WagoChannel`` applies to this part. Please note that any parameters for opening the channel (such as filenames, ip-addresses, COM-ports, etc) only apply to FBs which are derived from this model, and not to this base model itself. Transmitter: This part controls the transmission of data. The description of ``WagoTransmitter`` directly applies to it. The Transmitter part is only active while the ``Channel``-Part is open. Otherwise the transmitter is not called. If there is a transmission request while the channel is not open, the FB responds with the error code ``EBADF`` ('Bad File num,ber / File not open'); Receiver: The third part is a straightforward embedding of the ``WagoReceiver``-Model. Like the transmitter, it is called only as long as the Channel is open. *Channel:* On the rising edge of the input ``xOpen`` the channel is opened. Unless an error occurrs, the channel stays open while xOpen is kept ``TRUE``. This status is indicated by the output ``xIsOpen``, which is ``TRUE`` while the channel is operative. Any errors concerning the channel status are signalled via the output ``oStatus``. When ``xOpen`` returns to ``FALSE`` the channel is closed again after pending communication is finished. *Transmitter:* The transmitt er section implements the behaviour 'WagoTransmitter'. For transmitting data, the input 'pTxBuffer' is to be set to the address of the data block and the input ``udiTxNBytes`` has to hold the size of the data block. Setting ``xTxTrigger`` to TRUE initiates the transmission of the data. The transmitter indicates the completion of the transmitting process by setting ``xTxTrigger`` to ``FALSE`` again. .. note:: The application MUST NOT reset ``xTxTrigger`` to ``FALSE``, because in that case the FB has no means to signal to itself the completion of the process. .. note:: The term 'completion' in this context does not mean that the data has actually been sent physically. Rater it indicates that the data is delivered out of the FB und new data may be processed now. Any errors while transmitting data are displayed on the output eTxStatus. *Receiver:* The inputs pRxBuffer and udiRxBufferSize have to be fed with the location and the size of the raw buffer space for received data. (E.g.: :: pRxBuffer :

**Methods:**

#### protSetErrorFromMemberMethod
This method sets the general status outputs of the model according to the given status object.

If an error has occurred, ``xError`` will be set and ``xBusy`` and ``xDone`` will be reset.

#### initialize
Initializes FbBehaviourModel_WagoCommunicator at FB_Init().

#### protWriteOut
This is called from the model fro transmitting data out of the communicator. (For details see :ref:`general description of this model <FbBehaviourModel_WagoAppCommunicator>`.)

**Result Codes:**
| Code | Description |
|------|-------------|
| OK | Data transfer without any error (but may contain no data). other Data transfer failed with error. ============= ====================================================================================== |

#### protAcquire
This is called from the model for receiving incoming data. (For details see :ref:`general description of this model <FbBehaviourModel_WagoAppCommunicator>`.)

**Result Codes:**
| Code | Description |
|------|-------------|
| OK | Data acquisition without any error (but may contain no data). other Data acquisition failed with error. ============= ====================================================================================== |

#### protOpen
This is called from the model when opening the channel. (For details see :ref:`general description of this model <FbBehaviourModel_WagoAppCommunicator>`.)

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Opening of the channel was successfully completed. EAGAIN Opening still in progress. other Opening failed. Channel returns to idle state without calling close() ============= ===================================================================== |

#### protClose
This is called from the model when closing the channel. (For details see :ref:`general description of this model <FbBehaviourModel_WagoAppCommunicator>`.)

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Closing of the channel was successfully completed. EAGAIN Closing still in progress. other Closing failed for some reason. ============= ================================================== |

### FbBehaviourModel_oStatus_Base
This is a base object for all models which use a result factory. It embeds a result factory and handles the production of status objects. It provides for individual and automatic naming of status producers. All behaviour models whioch use status objects are supposed to be derived from this base.

**Description:**
A typical usage is the following :: FUNCTION_BLOCK FbBehaviourModel_NewEnable EXTENDS FbBehaviourModel_oStatus_Base; VAR_INPUT xEnable : BOOL; // Enables the operation. END_VAR VAR_OUTPUT xError : BOOL; xValid : BOOL; // Indicates that Data is valid. xBusy : BOOL; // Indicates that the FB is working. END_VAR VAR _model : _FbAppEnable_Model; // a child of FbBeghaviorModelWagoEnable END_VAR // (see tutorial documentation of this lib) ////////////////////////////////// // body code ////////////////////////////////// SUPER^(); _model(pBody:

**Methods:**

#### getFactoryName
This method retrieves the name of the result factory ('Producer').

#### protSetErrorFromMemberMethod
This method sets the general status outputs of the model according to the given status object.

This method should be re-implemented according to the specific needs of the child FB. A minimalistic re-implementation would be: :: METHOD PROTECTED protSetErrorFromMemberMethod VAR_INPUT eResult : eResultCode; // Status code to be processed END_VAR setStatusObject(eResult); xError :

#### protInitializeResultFactory
This protected method will be called automatically for initializazion of the result factory.

In derived FBs this method should contain code for individual settings of the status codes of the derived FB, e.g. like the following: :: {attribute 'inheritanceonly'} {attribute 'hide'} METHOD PROTECTED protInitializeResultFactory protSetupResultFactory(ADR('Name of the FB or the Instance'), ADR(ERROR_ARRAY), SIZEOF(ERROR_ARRAY)); ///////////////////////////////////////////// // place individual initialization code here ///////////////////////////////////////////// In this example ``protSetupResultFactory()`` is a member function for initialization of the error factory and ``ERROR_ARRAY`` is am individual or global array of predefined ``FbStatus``-objects.

#### clearStatusCode
This method sets the result object to OK and erases all traces from previous errors.

This method is neither PROTECTED nor FINAL, because it my be overloaded in child classes for filtering results or it may be used to inject result codes. *Caveat:* This method does not reset any extra status variables in child objects.

#### protSetupResultFactory
This method initializes the embedded result factory acording to the individial settings. Normally, it is called automatically from within the ``protInitializeResultFactory()`` method.

A typical usage would be the following: :: METHOD PROTECTED protInitializeResultFactory protSetupResultFactory(ADR('Name of the FB or the Instance'), ADR(ERROR_ARRAY), SIZEOF(ERROR_ARRAY)); ///////////////////////////////////////////// // place individual initialization code here /////////////////////////////////////////////

#### setStatusObject
This method reflects a result code to the output.

A new object is created if - the severity of the new result is higher than the severity of any previous results or if - the previous result was in *information* - informations will be superseded by more actual informations and also by 'OK'. A result code ``OK`` will supersede only previous *information* objects but nothing else. This method is neither FINAL nor PROTECTED, because it my be overloaded in child classes for filtering results or it may be used to inject result codes.

### FbBehaviourModel_WagoAppChannel
This is a base class for behaviour model WagoChannel with oStatus.

**Description:**
This base model is completely identical to :ref:`FbBehaviourModel_WagoChannel` with the only difference that the status output is named slightly differently here. This model is suitable for situations where an action has to be performed for allocating a resource ('opening') and another action for releasing the resource again ('closing'). Successful termination of these actions denotes this resource as 'now usable' or 'not usable'. Prominent examples for such resources are files and sockets as well as general communication channels. Beside actions for opening and closing, there is no 'main runner' included, as this base class represents just the state of the resource. Nevertheless, there are other classes derived from this base class, which combine this channel behaviour with an action, e.g. :ref:`ChannelledTrigger <FbBehaviourModel_WagoAppChannelledTrigger>`. *States* Idle: Waiting for xOpen to go TRUE, then call protOpen() and transit into 'Opening'. This state is indicated by having ``xIsIdle`` set to ``TRUE``. Opening: Waiting for the protOpen() to return either OK or any code other than ``EAGAIN``. On OK, transit to 'Run' and set ``xIsOpen`` to ``TRUE``; On Error, ``xIsOpen`` is left ``FALSE`` and the FB transits to 'Recovery'. This state is indicated by having both ``xIsIdle`` and ``xIsOpen`` reset to ``FALSE`` and ``eStatus`` set to ``EINPROGRESS``. Run: Waiting for ``xOpen`` to return to ``FALSE``, then call protClose() and transit into ``Closing``. This state is indicated by having ``xIsOpen`` set to ``TRUE``. Closing: Repeatedly call ``protClose()`` until it returns OK or any code other than ``EAGAIN``. In that case the FB transits to ``Idle``. This state is indicated by having both ``xIsIdle`` and ``xIsOpen`` reset to ``FALSE`` and ``eStatus`` set to ``ETERMINATED``. Recovery: This state is used when ``protOpen()`` failed with an error. In this state, the FB waits for ``xOpen`` to return to ``FALSE`` and transits then directly to ``Idle`` without calling ``protClose()``. This state is indicated by having both ``xIsIdle`` and ``xIsOpen`` reset to ``FALSE`` and ``eStatus`` set to an error code other than ``OK``, ``EINPROGRESS`` or ``ETERMINATED``. .. note:: The state ``xIsIdle`` and ``xIsOpen`` both set to ``TRUE`` is illegal and will be prevented by this base class. As usual, the detailed behaviour of this model is controlled by the result codes of the virtual methods, i.e. ``protOpen()`` and ``protClose()``:

**Methods:**

#### protSetErrorFromMemberMethod
This method sets the general status outputs of the model according to the given status object.

If an error has occurred, ``xError`` will be set.

#### Initialize
Initializes the framework of the FB at FB_init().

#### protClose
This method is called when the FB is closed. (details: see :ref:`general model description <FbBehaviourModel_WagoAppChannel>`)

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Closing of the channel was successfully completed. EAGAIN Closing still in progress. other Closing failed for some reason. ============= ================================================= |

#### protOpen
This method is called when the FB is opened. (details: see :ref:`general model description <FbBehaviourModel_WagoAppChannel>`)

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Opening of the channel was successfully completed. EAGAIN Opening still in progress. other Opening failed. Channel returns to idle state without calling close(). ============= ====================================================================== |

### FbBehaviourModel_WagoMethodStart
This is a base class for method driven FBs with status output.

**Description:**
*Overview* This is a base class for a method oriented execution model, similar to WagoExecute, but triggered by methods instead of by variables and with ``xTerminated`` instead of ``xDone``. It has no stimulus by variables but only stimuli by methods. (Please note that ``xTerminate`` indicates the termination of the implemented process, including the error case. *Intended usage* When only one functionality is implemented, the execution is, by convention, initiated by a single PUBLIC method called ``Start()``, which owns an interface with inputs which depend on the desired functionality. Because of that variablility, no prototype for ``Start()`` could be given here. Instead, we have a PROTECTED ``_TriggerExecute()``, which is called by the PUBLIC ``Start(...)`` of the child. The name ``Start()`` is, however, just a non-obligatory convention. If more than one functionality is included in a single FB (e.g. in file FBs or Socket FBs), each functionality will have its own starter method with more expessive names. The most important usage is to implement sevaeral ``Start(...)`` methods in parallel, sich as: - ``StartOneAction(sResourcename);`` - ``StartOtherAction(xImportantFlag);`` - ``StartThirdAction(sName, xImportantFlag);`` *Fundamental interface of behaviour model WagoMethodStart* This model has three internal states: Idle: The FB waits for _TriggerExecute() to be called, then transits to 'Run'. This state is indicated to the user by having ``xTerminated`` and ``xBusy`` both reset to FALSE. Note: ``xError`` is also reset in this state. Run: The FB calls ``protRun()`` repeatedly until ``protRun()`` returns OK or any code other than ``EAGAIN.`` This state is indicated by having ``xBusy`` set to ``TRUE`` and ``xTerminated`` reset to ``FALSE``. Terminated: The FB waits for a new ``_TriggerExecute()`` or ``_AcknowledgeTermination()`` to be called. In the latter case, the outputs are turned to a passive state and protClearOutputs() is called. In the first case, the same is done, but additionally a new run() is issued, as if the FB were in the idle state. Again, the detailed behaviour is controlled by the return codes of the runner:

**Methods:**

#### _IsReadyForExecution
#### _AcknowledgeTermination
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Successful acknowledge EBADSTATE Not in state 'Terminated' ============= ========================= |

#### _TriggerExecute
**Result Codes:**
| Code | Description |
|------|-------------|
| OK | OK or runer EINPROGRESS Runner requires more subsequent calls. EBUSY FB was not ready. EUNSPECIFIC Runner delivered EBUSY. other Specific codes of the runner ============= ====================================================================================== |

#### Initialize
#### protClearOutputs
#### protRun
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Execution has successfully terminated, set xDone = TRUE. EAGAIN Execution is still in progress, repeat protRun() in next cycle. other Execution has terminated with an error. ============= ====================================================================================== |

### Fb_CycleCountingState
**Methods:**

#### protSetState
#### protResetCycleCounter
#### protAdvanceCycleCounter
### FbBehaviourModelWagoEnable
**Methods:**

#### protRun
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Successful operation, set xValid EAGAIN Output variables not yet valid, reset xValid, eStatus := EINPROGRESS, xError := FALSE other Reset xValid, set eStatus to this code, set xError := TRUE ============= ====================================================================================== |

#### protTerminate
**Result Codes:**
| Code | Description |
|------|-------------|
| OK=0 | Successful termination, return to state 'Idle'. ENOSYS Method is not implemented, return to 'state Idle'. EAGAIN Shutdown is in progress and must be resumed. EBREAKPT Shutdown in progress, but direct transit to 'Run' if xEnable=TRUE is enabled other Display error code. ============= ====================================================================================== |

#### Initialize
### FbBehaviourModel_WagoCommunicator
Ths is a base class for behaviour model WagoCommunicator which is used for general communication needs.

**Description:**
*Submodules* This FB is composed of three separated sub-modules: Channel: This part controls the opening and closing of an associated communication channel. The description of :ref:`WagoChannel <FbBehaviourModel_WagoChannel>` applies to this part. Please note that any parameters for opening the channel (such as filenames, ip-addresses, COM-ports, etc) only apply to FBs which are derived from this model, and not to this base model itself. Transmitter: This part controls the transmission of data. The Transmitter part is only active while the Channel-Part is open. Otherwise the transmitter is not called. Receiver: While the channel is open, the FB tries to acquire data from the channel and to provide it to the application. *Channel* On the rising edge of the input ``xOpen`` the channel is opened. Unless an error occurrs, the channel stays open while xOpen is kept ``TRUE``. This status is indicated by the output ``xIsOpen``, which is ``TRUE`` while the channel is operative. Any errors concerning the channel status are signalled via the output ``eChanStatus``. When ``xOpen`` returns to ``FALSE`` the channel is closed again after pending communication is finished. *Transmitter Interface* The transmitter section is an indirect derivative from the :ref:`WagoTrigger <FbBehaviourModelWagoTrigger>`-Model. For transmitting data, the input ``pTxBuffer`` is to be set to the address of the data block and the input ``udiTxNBytes`` has to hold the size of the data block. Setting ``xTxTrigger`` to ``TRUE`` initiates the transmission of the data. The transmitter indicates the completion of the transmitting process by setting ``xTxTrigger`` to FALSE again. .. note:: The application MUST NOT reset ``xTxTrigger`` to ``FALSE``, because in that case the FB has no means to signal to itself the completion of the process. .. note:: The term 'completion' in this context does not mean that the data has actually been sent physically. Rather it indicates that the data is delivered out of the FB und new data may be processed now. Any errors while transmitting data are displayed on the output *eTxStatus*. *Transmitter Processing* Processing of the data takes place via the method ``protWriteOut()``, which gets a pointer to the data. This method has to be re-implemented by the user according to his specific functionality. ``protWriteOut()`` is allowed to process the data as whole, partially, or even nothing at all. It *must* return the number of bytes, which it a successfully processed. On the next cycle it will be called with a pointer to the remaining portion of the data and the number of bytes remaining, until all data is processed or an error occurrs. When an error occurrs or no more data is to be processed, the action is terminated and ``protWriteOut()`` is not called any further until the next ``xTxTrigger`` is applied. .. note:: The original ``protRun()`` from :ref:`WagoTrigger <FbBehaviourModelWagoTrigger>` is hidden here, because it contains final code now and is NOT to be overloaded by child classes from this FB. *Receiver Interface* The inputs ``pRxBuffer`` and ``udiRxBufferSize`` have to be fed with the location and the size of the raw buffer space for received data. (E.g.: ``pRxBuffer :

**Methods:**

#### protAcquire
This PROTECTED method is called from the FB when data is to be acquired.

(As described in the general FB description :ref:`FbBehaviourModel_WagoCommunicator`.)

**Result Codes:**
| Code | Description |
|------|-------------|
| OK | Data acquisition without any error (but may contain no data). other Data acquisition failed with error. ============= ====================================================================================== |

#### protWriteOut
This PROTECTED method is called when data is to be sent out.

(As described in the general FB description :ref:`FbBehaviourModel_WagoCommunicator`.)

**Result Codes:**
| Code | Description |
|------|-------------|
| OK | Data transfer without any error (but may contain no data). other Data transfer failed with error. ============= ====================================================================================== |

#### protOpen
This PROTECTED method is called from the FB when the channel is to be opened.

(As described in the general FB description :ref:`FbBehaviourModel_WagoCommunicator`.)

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Opening of the channel was successfully completed. EAGAIN Opening still in progress. other Opening failed. Channel returns to idle state without calling close() ============= ===================================================================== |

#### protClose
This PROTECTED method is called from the FB when the channel is to be closed.

(As described in the general FB description :ref:`FbBehaviourModel_WagoCommunicator`.)

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Closing of the channel was successfully completed. EAGAIN Closing still in progress. other Closing failed for some reason. ============= ================================================== |

#### Initialize
### FbBehaviourModel_WagoChannel
This FB provides a fundamental interface for the behaviour model WagoChannel. This model is suitable for situations where an action has to be performed for allocating a resource ('opening') and another action for releasing the resource again ('closing').

**Description:**
*Overview* For using this base model, the user is supposed to derive a child FB and re-implement some of the protected methods according to his needs. Normally these methods are associated ith the allocation and the release of a resource. Successful termination of the opening- and closing- actions denotes the associated resource as 'now usable' or 'not usable'. Prominent examples for such resources are files and sockets as well as general communication channels. .. note:: Beside actions for opening and closing, there is no 'main runner' included, as this base class represents just the state of the resource. Nevertheless, there are other classes derived from this base class, which combine this channel behaviour with an action, which is again represented by a runner (e.g. ``WagoChannelledTrigger``). *States of Operation* This base FB differentiates between the following internal states: Idle: Waiting for xOpen to go TRUE, then call ``protOpen()`` and transit into 'Opening'. This state is indicated by having ``xIsIdle`` set to ``TRUE``. Opening: Waiting for the protOpen() to return either OK or any code other than ``EAGAIN``. On ``OK``, transit to ``Run`` and set ``xIsOpen`` to ``TRUE``; On Error, ``xIsOpen`` is left ``FALSE`` and the FB transits to ``Recovery``. This state is indicated by having both ``xIsIdle`` and ``xIsOpen`` reset to ``FALSE`` and ``eStatus`` set to ``EINPROGRESS``. Run: Waiting for ``xOpen`` to return to ``FALSE``, then call ``protClose()`` and transit into ``Closing``. This state is indicated by having ``xIsOpen`` set to ``TRUE``. Closing: Repeatedly call ``protClose()`` until it returns ``OK`` or any code other than ``EAGAIN``. In that case the FB transits to ``Idle``. This state is indicated by having both ``xIsIdle`` and ``xIsOpen`` reset to ``FALSE`` and ``eStatus`` set to ``ETERMINATED``. Recovery: This state is used when ``protOpen()`` failed with an error. In this state, the FB waits for ``xOpen`` to return to ``FALSE`` and transits then directly to ``Idle`` without calling ``protClose()``. This state is indicated by having both ``xIsIdle`` and ``xIsOpen`` reset to ``FALSE`` and ``eStatus`` set to an error code other than ``OK``, ``EINPROGRESS`` or ``ETERMINATED``. .. note:: The state of ``xIsIdle`` and ``xIsOpen`` both set to ``TRUE`` is illegal and will be prevented by this base class. As usual, the detailed behaviour of this model is controlled by the result codes of the virtual methods, i.e. ``protOpen()`` and ``protClose()``:

**Methods:**

#### protClose
This code is called when the FB is closed. The user may place own closing code into a re-implementation of this method.

When this function is re-implemented, it is supposed to return the below shown result codes to the :ref:`WagoChannel behaviour model <FbBehaviourModel_WagoChannel>`.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Closing of the channel was successfully completed. EAGAIN Closing still in progress. other Closing failed for some reason. ============= ================================================= |

#### Initialize
If a derivied FB requires individial initialization code, this code is supposed to be placed in a re-implementation of this method. This method is called by FB_Init().

#### protOpen
This code is called when the FB is opened. The user may place own opening code into a re-implementation of this method.

When this function is re-implemented, it is supposed to return one of the below listed result codes to the behaviour model :ref:`WagoChannel <FbBehaviourModel_WagoChannel>`.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Opening of the channel was successfully completed. EAGAIN Opening still in progress. other Opening failed. Channel returns to idle state without calling close(). ============= ====================================================================== |

### FbBehaviourModelWagoTrigger
**Methods:**

#### ResetStatus
This method resets the ``xError`` and ``eStatus`` to ``OK`` (independently of the processing state).

#### Initialize
#### protRun
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | The action has successfully terminated, reset xTrigger again. EAGAIN The action has to be repeated. other The action has terminated with an error, reset xTrigger again. ============= ============================================================== |

### FbBehaviourModelWagoExecute
**Methods:**

#### protClearOutputs
#### Initialize
#### protRun
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Execution has successfully terminated, set xDone = TRUE. EAGAIN Execution is still in progress, repeat protRun() in next cycle. other Execution has terminated with an error. Display that code and set xError. ============= ========================================================================= |

## Data Types

### eExecutionState
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbBehaviourModel_AppTrigger_bare: FbBehaviourModel_AppTrigger_bare;
END_VAR

// Basic function block usage
fbFbBehaviourModel_AppTrigger_bare(
    // Configure inputs as needed
);

// Check status
IF fbFbBehaviourModel_AppTrigger_bare.xValid THEN
    // Operation successful
END_IF

IF fbFbBehaviourModel_AppTrigger_bare.xError THEN
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

