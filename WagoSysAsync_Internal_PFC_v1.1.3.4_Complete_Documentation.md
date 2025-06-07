# WagoSysAsync_Internal_PFC v1.1.3.4 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysAsync_Internal_PFC
- **Version:** 1.1.3.4
- **Categories:** WAGO Internal|Target|PFC
- **Namespace:** WagoSysAsync_Internal
- **Author:** WAGO / u013972

### Description ¶


This document is automatically generated.

Handling of Asynchronicity specifically for PFC with TSC

This document is automatically generated. Handling of Asynchronicity specifically for PFC with TSC

### Contents: ¶


Contents: - Project Information - Library Information - Function Blocks - Functions IsEventScheduling (FUN) - IsFreeRunScheduling (FUN) - SchedulingModeEvent (FUN) - TscAsyncAdd (FUN) - TscAsyncAddJob (FUN) - TscAsyncGetJobReturnValue (FUN) - TscAsyncRemove (FUN) - TscAsyncRemovesAll (FUN) - getPlainPriorityValue (FUN) Methods - FbAsyncDeferrer.GetRunnerResult (METH) - FbAsyncDeferrer.GetState (METH) - FbAsyncDeferrer.Initialize (METH) - FbAsyncDeferrer.Remove (METH) - FbAsyncDeferrer.RunAsDaemon (METH) - FbAsyncDeferrer.RunAsOneShot (METH) - FbAsyncDeferrer.destroy (METH) Program Organization Main Interfaces Internal Components - 90 Internal - WagoSysAsync_Internal_PFC Library Documentation Global Variable Lists - LibraryResult (GVL) - ResultItems (GVL) - VersionHistory (GVL) - ZGVL (GVL) Other Components - 20 Additional - 30 Administration - 89 TSC - ASYNCJOB_PARAM (STRUCT)

### Indices and tables ¶


Based on WagoSysAsync_internal_PFC.library, last modified 29.05.2024, 19:51:16. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysAsync_internal_PFC.library, last modified 29.05.2024, 19:51:16. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysAsync_internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:51:16 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:51:16 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoSysAsync_Internal |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysAsync_internal_PFC |
| NoPlaceholder |  |
| Version | version | 1.1.3.4 |
| Title | string | WagoSysAsync_Internal_PFC |
| LibraryCategories | library-category-list | WAGO Internal\|Target\|PFC |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysPlainMem Library Identification : Placeholder: WagoSysPlainMem Default Resolution: WagoSysPlainMem, * (WAGO) Namespace: WagoSysPlainMem Library Properties : WagoSysTypedefs_Debugging Library Identification : Placeholder: WagoSysTypedefs_Debugging Default Resolution: WagoSysTypedefs_Debugging, * (WAGO) Namespace: WagoSysTypedefs_Debugging Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesAsync_Internal_PFC Library Identification : Placeholder: WagoTypesAsyncInternal Default Resolution: WagoTypesAsync_Internal_PFC, * (WAGO) Namespace: WagoTypesAsyncInternal Library Properties :

### Function Blocks


## FbAsyncDeferrer (FB)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Output | xStarted | BOOL | Will be set immediately before starting the runner. |
| xFinished | BOOL | Will be set immediately after having finished the runner. |
| oSchedMode | eSchedulingMode | The actual scheduling mode for the runner. |

FB for the book-keeping of asynchronous execution.

With one of the methods RunAsOneShot() or RunAsDaemon() the method Run() of a Fb_GenericRunner will be scheduled for synchronous or asynchronous execution. The method remove() tries to remove the asynchronous job again.

The FbAsyncDeferrer is entirely method driven and does not require any cyclic execution.

Interface variables FB for the book-keeping of asynchronous execution. With one of the methods RunAsOneShot() or RunAsDaemon() the method Run() of a Fb_GenericRunner will be scheduled for synchronous or asynchronous execution. The method remove() tries to remove the asynchronous job again. The FbAsyncDeferrer is entirely method driven and does not require any cyclic execution. - 10 Main Interface FbAsyncDeferrer.Remove (METH) - FbAsyncDeferrer.RunAsDaemon (METH) - FbAsyncDeferrer.RunAsOneShot (METH) 20 Additional - FbAsyncDeferrer.GetRunnerResult (METH) - FbAsyncDeferrer.GetState (METH) 30 Administration - FbAsyncDeferrer.Initialize (METH) - FbAsyncDeferrer.destroy (METH)

### Functions


## IsEventScheduling (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IsEventScheduling | BOOL |
| Input | eSchedMode | eSchedulingMode |

Determines if a given mode is a regular mode.

Attention: the implementation may be strongly hardware depending.

Interface variables Determines if a given mode is a regular mode. Attention: the implementation may be strongly hardware depending.

## IsFreeRunScheduling (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IsFreeRunScheduling | BOOL |
| Input | eSchedMode | eSchedulingMode |

Determines if a given mode is a regular mode.

Attention: the implementation may be strongly hardware depending.

Interface variables Determines if a given mode is a regular mode. Attention: the implementation may be strongly hardware depending.

## SchedulingModeEvent (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SchedulingModeEvent | eSchedulingModeEvent |  |
| Input | eSchedMode | eSchedulingMode | generic scheduling mode |

```
VAR
   eSchedMode := eSchedulingModeEvent;
END_VAR

eSchedMode := eSchedulingModeEvent.Modbus_Watchdog_Expired;           // Device specific mode
eSchedMode := SchedulingModeEvent(eSchedulingMode.Background);        // Regular mode
```

Casts a generic scheduling mode into a device specific event-scheduling mode.

CaveaHallot:

Do not confuse mix this with the similarly named SchedulingMode_EventPriority(), which combines events with priorities and which takes a different number of arguments.

Interface variables Casts a generic scheduling mode into a device specific event-scheduling mode. Usage: CaveaHallot: Do not confuse mix this with the similarly named SchedulingMode_EventPriority(), which combines events with priorities and which takes a different number of arguments.

## TscAsyncAdd (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | TscAsyncAdd | RTS_IEC_HANDLE |  |
| Input | pfAsyncJobFunc | POINTER TO BYTE | points to the standardized - method which is to be deferred |
| pParam | POINTER TO BYTE | the parameter for execution of pfAsyncJobFunc |
| pInstance | POINTER TO BYTE | points to the instance of the deferred FB |
| pudState | POINTER TO UDINT | specifies where to write the execution state |
| udIecFunc | UDINT | 1 for deferring IEC-FBs, 0 otherwise |
| udTimeout | UDINT | Milliseconds after call, 0 for no timeout |
| udJobPriority | UDINT | internal scheduling parameter (=IEC-Priority, 1..15) |
| pResult | POINTER TO UDINT | Location where the result of pfAsyncJobFunc() is written |

| Result Codes |
| 0 | Successful operation |
| 2 | Invalid parameter |

Returns a handle to an JobInfo structure of an anynchronized thread.

On successful operation, ^pResult is always set to 0, ^pudState is set to ASYNCSTATE_PENDING (=0) and the returned handle is valid.

On error, ^pResult is always set to the appropriate error code (>0). On error, the contents of ^pudState and of the returned handle is not specified.

The parameter udTimeout allows to automatically discard the execution of a pending asynchronous job, when it has been in the queue for a too long time. Please note, that once the job is actively executed, it will not be affected anymore by any timeout.

Interface variables Returns a handle to an JobInfo structure of an anynchronized thread. On successful operation, ^pResult is always set to 0, ^pudState is set to ASYNCSTATE_PENDING (=0) and the returned handle is valid. On error, ^pResult is always set to the appropriate error code (>0). On error, the contents of ^pudState and of the returned handle is not specified. The parameter udTimeout allows to automatically discard the execution of a pending asynchronous job, when it has been in the queue for a too long time. Please note, that once the job is actively executed, it will not be affected anymore by any timeout.

## TscAsyncAddJob (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | TscAsyncAddJob | RTS_IEC_HANDLE |  |
| Input | pfAsyncJobFunc | POINTER TO BYTE | points to the standardized - method which is to be deferred |
| pParam | POINTER TO BYTE | the parameter for execution of pfAsyncJobFunc |
| pInstance | POINTER TO BYTE | points to the instance of the deferred FB |
| pudState | POINTER TO UDINT | specifies where to write the execution state |
| udIecFunc | UDINT | 1 for deferring IEC-FBs, 0 otherwise |
| udTimeout | UDINT | Milliseconds after call, 0 for no timeout |
| pJobParam | POINTER TO ASYNCJOB_PARAM | internal job parameter |
| pResult | POINTER TO UDINT | Location where the result of pfAsyncJobFunc() is written to |

| Result Codes |
| 0 | Successful operation |
| 2 | Invalid parameter |

No further description available

Interface variables No further description available

## TscAsyncGetJobReturnValue (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | TscAsyncGetJobReturnValue | UDINT |  |
| Input | hJob | RTS_IEC_HANDLE | handle to the job |
| pudReturnVal | POINTER TO UDINT | location where the async result is written to |

| Result Codes |
| 0 | Successful operation |
| 2 | Invalid Parameter |

Retrieves the return value of the asynchronized function

The return value of the asynchronzied job is written to the location where pudReturnVal points to.

Interface variables Retrieves the return value of the asynchronized function The return value of the asynchronzied job is written to the location where pudReturnVal points to.

## TscAsyncRemove (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | TscAsyncRemove | UDINT |
| Input | hJob | RTS_IEC_HANDLE |

| Result Codes: |
| 0 | Successful operation |
| 2 | Invalid Parameter |
| 10 | Still in progress, cannot be removed |

Removes a job from the joblist.

Note: the Job can only be removed before or after execution, but not while it is actively executed. In the latter case, error ‘10’ is returned.

The job is NOT marked for automatic deletion aufter it has terminated.

Interface variables Removes a job from the joblist. Note: the Job can only be removed before or after execution, but not while it is actively executed. In the latter case, error ‘10’ is returned. The job is NOT marked for automatic deletion aufter it has terminated.

## TscAsyncRemovesAll (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | TscAsyncRemovesAll | UDINT |

| Result Codes : |
| 0 | Successful operation |
| 10 | Still in progress, cannot be removed |

Removes all jobs from the joblist.

When one or more jobs are actively executed, they cannot be removed and this function returns ‘10’ as error code.

The active jobs were NOT deleted automatically.

Interface variables Removes all jobs from the joblist. When one or more jobs are actively executed, they cannot be removed and this function returns ‘10’ as error code. The active jobs were NOT deleted automatically.

## getPlainPriorityValue (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getPlainPriorityValue | DWORD |
| Input | eSchedMode | eSchedulingMode |

Converts a scheduling mode into a device dependent priority value

If the scheduling mode is combined with an event description, the event description will be stripped from the priority part.

Attention: If the values eSchedulingMode.Synchronous or eSchedulingMode.NoScheduling are passed, there exist no sensible corresponding firmware priorities for these values. In those cases, zero is returned.

Interface variables Converts a scheduling mode into a device dependent priority value If the scheduling mode is combined with an event description, the event description will be stripped from the priority part. Attention: If the values eSchedulingMode.Synchronous or eSchedulingMode.NoScheduling are passed, there exist no sensible corresponding firmware priorities for these values. In those cases, zero is returned.

### Methods


## FbAsyncDeferrer.GetRunnerResult (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRunnerResult | eResultCode |

Delivers the result code from the runner.

Interface variables Delivers the result code from the runner.

## FbAsyncDeferrer.GetState (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetState | eResultCode |

| result codes |
| ENOENT | No job to be scheduled, nothing to do. |
| EPENDING | The job is waiting for execution. |
| EINPROGRESS | The job is running right now. |
| ETERMINATED | The job has terminated successfully. |
| EUNSPECIFIC | The job terminated with an unspecific error code. |
| ETIMEDOUT | The job is timed out (but still running). |
| ECANCELED | The job is scheduled for removement. |
| EBADF | The FB does not contain a valid handle. |

In which processing state is the deferred job?

Interface variables In which processing state is the deferred job?

## FbAsyncDeferrer.Initialize (METH)


Sets the FB to a well-defined state.

This is performed before each Add() oder AddJob().

Sets the FB to a well-defined state. This is performed before each Add() oder AddJob().

## FbAsyncDeferrer.Remove (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Remove | eResultCode |

| result codes |
| 0=OK | Success. |
| EBADF | The Job handle is invalid. |
| EPIPE | The handle does not longer refer to a valid job (broken connection). |
| EBUSY | The One-Shot-Job is active and thus will not be attempted to be removed. |
| EPENDING | The daemon job is currently running and will be removed after it has finished. |
| ECODESYS+X | CoDeSys-specific fault (not specified). |

Removes scheduled job and terminates daemons.

This method exhibits different behaviour for one-shot-jobs and daemons:

One-Shot-Jobs:

The method removes the job from the list after the job has terminated. It should not be called before that time, because an active job cannt be killed or removed. When called while the job is still active, remove() returns EPENDING.

This method stops the re-scheduling of daemons and removes them afterwards. If the daemon is currently executed, remove() delivers EPENDING instead of OK, which is not an error. During the remaining run-time of the runner, the job state is ECANCELED. After termination of the runner, no additional remove() is necessary.

If the Fb state indicates that the deferred job is in an invalid state or that the handle has a non-proper value, this method returns immediately EPIPE or EBADF respectively without trying to romove anything.

Interface variables Removes scheduled job and terminates daemons. This method exhibits different behaviour for one-shot-jobs and daemons: One-Shot-Jobs: The method removes the job from the list after the job has terminated. It should not be called before that time, because an active job cannt be killed or removed. When called while the job is still active, remove() returns EPENDING. Daemons: This method stops the re-scheduling of daemons and removes them afterwards. If the daemon is currently executed, remove() delivers EPENDING instead of OK, which is not an error. During the remaining run-time of the runner, the job state is ECANCELED. After termination of the runner, no additional remove() is necessary. If the Fb state indicates that the deferred job is in an invalid state or that the handle has a non-proper value, this method returns immediately EPIPE or EBADF respectively without trying to romove anything.

## FbAsyncDeferrer.RunAsDaemon (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | RunAsDaemon | eResultCode |  |
| Input | pFrame | POINTER TO WagoTypes.Fb_GenericRunner | Points to a structure containing VMT and parameters. |
| eSchedMode | eSchedulingMode | The scheduling mode and priority for scheduling. |

| result codes |
| 0=OK | Successful scheduling. |
| ESRCH | No such process matching the event specification. |
| EINVAL | Invalid combination of input parameters |
| EBUSY | The FB is busy with another job which is still active. |
| ECODESYS+X | Wago-specific fault (not specified) |

```
eSchedMode := eSchedulingMode.Background;                                  // regular assignment
```

```
eSchedMode := SchedulingMode(eSchedulingModeEvent.Modbus_Watchdog_Expired); // device specific assignment
```

```
eSchedMode := SchedulingMode_EventPriority(eSchedulingModeEvent.Modbus_Watchdog_Running,
                                           eSchedulingMode.AsyncLow);
```

Schedules the runner as a daemon.

A daemon is a job in the background which is periodically re-scheduled for execution after it has terminated.

As a consequence, the runner of a daemon SHOULD consume considerably less execution time than its periodicity intervall, because it would otherwise block other daemons. This restriction escpecially includes blocking system calls (such as socket-connect(), e.g.). This is in contrast to regular one-shot jobs, which are deferred as a background job just because they are long-running or blocking.

Note: This restriction is planned to be lifted when the thread-pool is implemented, which would prevent different jobs from blocking each other.

Thus, the points in placing daemons are

and not primarily deferring long-running sequences away from the main task.

Scheduling:

A daemon may either be deferred to another cyclic task according to one of the scheduling modes eSchedulingMode.Background .. eSchedulingMode.RealTimeHigh .

Or alternatively it may be synchronized to an external event, which is indicated by a slightly different but compatible enumeration. In that case, the type-casing wrapper SchedulingMode() has to be employed, e.g. :

If the target hardware supports it, also a combination of both modes defined if the target hardware supports that. In this case a different wrapper is required:

Runner Result:

Like in all other scheduling modes the method getRunnerResult() delivers the result code of the most recent execution of the runner. In contrast to one-shot-jobs, this result is updated periodically in each daemon-cycle and it thus might change asynchronously. Consequently, it is not provided as generic output, but it may be used by derived FBs.

Interface variables Schedules the runner as a daemon. Context: A daemon is a job in the background which is periodically re-scheduled for execution after it has terminated. As a consequence, the runner of a daemon SHOULD consume considerably less execution time than its periodicity intervall, because it would otherwise block other daemons. This restriction escpecially includes blocking system calls (such as socket-connect(), e.g.). This is in contrast to regular one-shot jobs, which are deferred as a background job just because they are long-running or blocking. Note: This restriction is planned to be lifted when the thread-pool is implemented, which would prevent different jobs from blocking each other. Thus, the points in placing daemons are 1. synchronizing the execution to external events, or/and 2. not having to care about cyclic execution in the main task and not primarily deferring long-running sequences away from the main task. Scheduling: A daemon may either be deferred to another cyclic task according to one of the scheduling modes eSchedulingMode.Background .. eSchedulingMode.RealTimeHigh . Or alternatively it may be synchronized to an external event, which is indicated by a slightly different but compatible enumeration. In that case, the type-casing wrapper SchedulingMode() has to be employed, e.g. : If the target hardware supports it, also a combination of both modes defined if the target hardware supports that. In this case a different wrapper is required: Runner Result: Like in all other scheduling modes the method getRunnerResult() delivers the result code of the most recent execution of the runner. In contrast to one-shot-jobs, this result is updated periodically in each daemon-cycle and it thus might change asynchronously. Consequently, it is not provided as generic output, but it may be used by derived FBs.

## FbAsyncDeferrer.RunAsOneShot (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | RunAsOneShot | eResultCode |  |
| Input | pFrame | POINTER TO WagoTypes.Fb_GenericRunner | points to a structure containing VMT and parameters |
| eSchedMode | eSchedulingMode |  |

| Result Codes |
| 0=OK | Synchronous execution of the Job has been executed. |
| EINPROGRESS | Asynchronous execution is scheduled successfully. |
| ESRCH | No such process matching the event specification. |
| EINVAL | Invalid parameters for scheduling. |
| EBUSY | Another job which is connected to this FB is still active. |
| ECODESYS+X | CoDeSys-specific fault (not specified) |

Schedule the runner for non-periodic execution.

The runner will be executed exactly one time after the specified event has occured or the scheling priority allows for it.

Interface variables Schedule the runner for non-periodic execution. The runner will be executed exactly one time after the specified event has occured or the scheling priority allows for it.

## FbAsyncDeferrer.destroy (METH)


Cleaning up before FbAsyncDeferrer is Fb_Exit’ed().

Cleaning up before FbAsyncDeferrer is Fb_Exit’ed().

### Program Organization


## 20 Program Organization Units


- FbAsyncDeferrer (FB) 10 Main Interface FbAsyncDeferrer.Remove (METH) - FbAsyncDeferrer.RunAsDaemon (METH) - FbAsyncDeferrer.RunAsOneShot (METH) 20 Additional - FbAsyncDeferrer.GetRunnerResult (METH) - FbAsyncDeferrer.GetState (METH) 30 Administration - FbAsyncDeferrer.Initialize (METH) - FbAsyncDeferrer.destroy (METH)

### Main Interfaces


## 10 Main Interface


- FbAsyncDeferrer.Remove (METH) - FbAsyncDeferrer.RunAsDaemon (METH) - FbAsyncDeferrer.RunAsOneShot (METH)

### Internal Components


## 90 Internal


- IsEventScheduling (FUN) - IsFreeRunScheduling (FUN) - SchedulingModeEvent (FUN) - getPlainPriorityValue (FUN)

## WagoSysAsync_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysAsync_Internal_PFC |
| Version: | 1.1.3.4 |
| Categories: | WAGO Internal\|Target\|PFC |
| Namespace: | WagoSysAsync_Internal |
| Author: | WAGO / u013972 |

### Description


This document is automatically generated.

Handling of Asynchronicity specifically for PFC with TSC

This document is automatically generated. Handling of Asynchronicity specifically for PFC with TSC

### Contents:


- 20 Program Organization Units FbAsyncDeferrer (FB) 89 TSC - ASYNCJOB_PARAM (STRUCT) - TscAsyncAdd (FUN) - TscAsyncAddJob (FUN) - TscAsyncGetJobReturnValue (FUN) - TscAsyncRemove (FUN) - TscAsyncRemovesAll (FUN) - ZGVL (GVL) 90 Internal - IsEventScheduling (FUN) - IsFreeRunScheduling (FUN) - SchedulingModeEvent (FUN) - getPlainPriorityValue (FUN) LibraryResult (GVL) ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


Based on WagoSysAsync_internal_PFC.library, last modified 29.05.2024, 19:51:16. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysAsync_internal_PFC.library, last modified 29.05.2024, 19:51:16. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## LibraryResult (GVL)


| Name | Type |
| --- | --- |
| Factory | FbResultFactory |

```
VAR
  eMyResult : eResultCode;  // result code whic is to be investigated
  oError    : FbResult;     // result object for use in highe levels.
END_VAR;

eMyResult := myFunction(...);
Namespace.LibraryResult.Factory.SetResult(eMyResult, oError);
```

Factory for standard result objects

Use this to translate result codes from this library into standard result objects.

where ‘Namespace’ denotes the namespace which is used for including the specific library and ‘myFunction()’ is an example for a general function from this library.

Factory for standard result objects Use this to translate result codes from this library into standard result objects. Usage: where ‘Namespace’ denotes the namespace which is used for including the specific library and ‘myFunction()’ is an example for a general function from this library.

## ResultItems (GVL)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | ERROR | ARRAY [0..12] OF WagoSysErrorBase.WagoTypesErrorBase.typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK’), STRUCT(ID := EINPROGRESS, Severity := eSeverity.info, Text := ‘Asynchronous execution is scheduled successfully.’), STRUCT(ID := EPENDING, Severity := eSeverity.info, Text := ‘The job is currently running or aiting for execution.’), STRUCT(ID := ETERMINATED, Severity := eSeverity.info, Text := ‘The job has terminated successfully.’), STRUCT(ID := ECANCELED, Severity := eSeverity.info, Text := ‘The job is scheduled for removement.’), STRUCT(ID := EUNSPECIFIC, Severity := eSeverity.error, Text := ‘The job terminated with an unspecific error code.’), STRUCT(ID := ETIMEDOUT, Severity := eSeverity.error, Text := ‘The job is timed out (but still running).’), STRUCT(ID := EBADF, Severity := eSeverity.error, Text := ‘The FB does not contain a valid handle.’), STRUCT(ID := EPIPE, Severity := eSeverity.error, Text := ‘The handle does not longer refer to a valid job (broken connection).’), STRUCT(ID := EBUSY, Severity := eSeverity.error, Text := ‘The FB is busy with another job or the running job cannot be removed.’), STRUCT(ID := EINVAL, Severity := eSeverity.error, Text := ‘Invalid combination of input parameters.’), STRUCT(ID := ESRCH, Severity := eSeverity.error, Text := ‘No such process matching the event specfiction.’), STRUCT(ID := ENOENT, Severity := eSeverity.error, Text := ‘No job to be scheduled, nothing to do.’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 24.05.2024 | 1.1.3.4 | WAGO / u013972 | Fix firmware interface and replace UDINT against RTS_IEC_HANDLE |
| 05.03.2021 | 1.1.3.3 | WAGO / u013972 | Resolve types from WagoSysErrorBase with namespace |
| 11.05.2020 | 1.1.3.2 | WAGO / u013972 | Remove the license form project info |
| 08.01.2019 | 1.1.3.1 | u015842 | Properties: copyright added |
| 09.06.2017 | 1.1.3.0 | WAGO / u013972 | Remove WagoTypesAsync_Internal_Template; Add WagoTypesAsync_Internal_PFC |
| 02.03.2016 | 1.1.2.0 | WAGO / u013972 | Replace WagoAppErrorBase with WagoSysErrorBase |
| 29.09.2015 | 1.1.1.0 | WAGO / u013972 | Workaround for C0351-Bug, Resolve libraries with placeholders |

WagoSysAsync_Internal_PFC.library

WagoSysAsync_Internal_PFC.library

## ZGVL (GVL)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | ASYNCJOB_INVALID_HANDLE | RTS_IEC_HANDLE | RTS_INVALID_HANDLE | nominally not valid handle |
| ASYNCSTATE_INVALID | UDINT | 16#FFFFFFFF | can be as default value, will never be written |
| ASYNC_TIMEOUT_INFINITE | UDINT | 0 | no timeout |
| ASYNC_IS_IEC | UDINT | 1 | marker for IEC jobs |
| ASYNC_ISNOT_IEC | UDINT | 0 | marker for generic C-jobs. |
| ASYNCSTATE_PENDING | UDINT | 0 | job is in the list but not yet executed |
| ASYNCSTATE_ACTIVE | UDINT | 1 | the job is currently beeing executed |
| ASYNCSTATE_READY | UDINT | 2 | the job is finished |
| ASYNCSTATE_ERROR | UDINT | 3 | an exception has occurred during execution (terminated automatically) |
| ASYNCSTATE_TIMEOUT | UDINT | 4 | job has not been activated due to previous timeout |
| ASYNCSTATE_READY_TO_REMOVE | UDINT | 5 | indicates that the job will be removed in next task cycle |

### Other Components


## 20 Additional


- FbAsyncDeferrer.GetRunnerResult (METH) - FbAsyncDeferrer.GetState (METH)

## 30 Administration


- FbAsyncDeferrer.Initialize (METH) - FbAsyncDeferrer.destroy (METH)

## 89 TSC


- ASYNCJOB_PARAM (STRUCT) - TscAsyncAdd (FUN) - TscAsyncAddJob (FUN) - TscAsyncGetJobReturnValue (FUN) - TscAsyncRemove (FUN) - TscAsyncRemovesAll (FUN) - ZGVL (GVL)

## ASYNCJOB_PARAM (STRUCT)


| Name | Type |
| --- | --- |
| ulJobPriority | UDINT |
| pszExtEvtName | POINTER TO STRING |
| bDeamon | UDINT |

Job parameters for TscAsyncAddJob()

bDeamon : if true, async-job is handled like a deamon. To stop/remove the deamon call TscAsyncRemove()

InOut: Job parameters for TscAsyncAddJob() ulJobPriority : external triggered jobs have always the IEC-Priority 0 in actual firmware-releases. non external jobs could have IEC-Priorities 1,2,3,4,7,14,15 like Sched-Modes in WagoSysAsync pszExtEvtName : name of the external event, that triggers the async-job. actually only localbus-events supported bDeamon : if true, async-job is handled like a deamon. To stop/remove the deamon call TscAsyncRemove()