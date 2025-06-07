# WagoSysModule_75x_65x v1.9.5.15 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysModule_75x_65x
- **Version:** 1.9.5.15
- **Categories:** WAGO LayerView|Sys; Application
- **Author:** WAGO / u010545
- **Placeholder:** WagoSysModule_75x_65x

### Description ¶


This document is automatically generated.

This library contains base function blocks to support serial 75x-65x modules for automatic instanziation

This document is automatically generated. This library contains base function blocks to support serial 75x-65x modules for automatic instanziation

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks FbModule_75x_1652 (FB) - FbModule_75x_650 (FB) - FbModule_75x_651 (FB) - FbModule_75x_652 (FB) - FbModule_75x_653 (FB) Methods - FbModule_75x_1652.ReadParameter (METH) - FbModule_75x_1652.WriteParameter (METH) - FbModule_75x_1652.protCheckPaSIze (METH) - FbModule_75x_1652.readStartUpValues (METH) - FbModule_75x_652.ReadParameter (METH) - FbModule_75x_652.WriteParameter (METH) - FbModule_75x_652.diDmxStartAddress (PROP) - FbModule_75x_652.protCheckPaSIze (METH) - FbModule_75x_652.readStartUpValues (METH) Internal Components - 90 Internal - 90 Internal Global Variable Lists - ErrorModule (GVL) - VersionHistory (GVL) Other Components - 10 Error Module - 10 I_ModuleParameter - 10 I_ModuleParameter - 20 Program Organitzation Unit - 80 Status - FbModule_75x_1652.diRtsPostDelay (PROP) - FbModule_75x_1652.diRtsPreDelay (PROP) - FbModule_75x_1652.eBiasRx (PROP) - FbModule_75x_1652.eBiasTx (PROP) - FbModule_75x_1652.eRs485SwitchTime (PROP) - ... and 12 more

### Indices and tables ¶


Based on WagoSysModule_75x_65x.library, last modified 29.05.2024, 20:18:25. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysModule_75x_65x.library, last modified 29.05.2024, 20:18:25. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysModule_75x_65x Library Documentation


| Company: | WAGO |
| Title: | WagoSysModule_75x_65x |
| Version: | 1.9.5.15 |
| Categories: | WAGO LayerView\|Sys; Application |
| Author: | WAGO / u010545 |
| Placeholder: | WagoSysModule_75x_65x |

### Description


This document is automatically generated.

This library contains base function blocks to support serial 75x-65x modules for automatic instanziation

This document is automatically generated. This library contains base function blocks to support serial 75x-65x modules for automatic instanziation

### Contents:


- 20 Program Organitzation Unit FbModule_75x_1652 (FB) - FbModule_75x_650 (FB) - FbModule_75x_651 (FB) - FbModule_75x_652 (FB) - FbModule_75x_653 (FB) 80 Status - 10 Error Module Parameter (PARAMS) VersionHistory (GVL)

### Indices and tables


Based on WagoSysModule_75x_65x.library, last modified 29.05.2024, 20:18:25. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysModule_75x_65x.library, last modified 29.05.2024, 20:18:25. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysModule_75x_65x.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:18:26 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:18:25 |
| Description | string | See: Description |
| Copyright | © WAGO GmbH & Co. KG, Germany 2021 – All rights reserved. |
| Author | WAGO / u010545 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysModule_75x_65x |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysModule_75x_65x |
| DefaultNamespace |  |
| Version | version | 1.9.5.15 |
| Title | string | WagoSysModule_75x_65x |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpEventMgr Library Identification : Placeholder: CmpEventMgr Default Resolution: CmpEventMgr, * (System) Namespace: CmpEventMgr Library Properties : IoStandard Library Identification : Placeholder: IoStandard Default Resolution: IoStandard, * (System) Namespace: IoStandard Library Properties : Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : SysCpuHandling Library Identification : Placeholder: SysCpuHandling Default Resolution: SysCpuHandling, * (System) Namespace: SysCpuHandling Library Properties : SysMem Library Identification : Placeholder: SysMem Default Resolution: SysMem, * (System) Namespace: SysMem Library Properties : SysSocket Library Identification : Placeholder: SysSocket Default Resolution: SysSocket, * (System) Namespace: SysSocket Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : Library Parameter : Parameter: SYSLOG_MBX2_MAX_STRING_LEN = 0 Parameter: STARTUP_MODE = eStartUpMode.NONE Parameter: TASK_PRIO_DAEMON_KBUS = 13 Parameter: SYSLOG_MBX2_LOGLEVEL = 2#10001 Parameter: SYSLOG_SERVER_IP = ‘127.0.0.1’ Parameter: TASK_PRIO_DAEMON_CYCLIC = 14 Parameter: SYSLOG_SERVER_PORT = 514 WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesBusServices Library Identification : Placeholder: WagoTypesBusServices Default Resolution: WagoTypesBusServices, * (WAGO) Namespace: WagoTypesBusServices Library Properties : WagoTypesCom Library Identification : Placeholder: WagoTypesCom Default Resolution: WagoTypesCom, * (WAGO) Namespace: WagoTypesCom Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties : WagoTypesEvent Library Identification : Placeholder: WagoTypesEvent Default Resolution: WagoTypesEvent, * (WAGO) Namespace: WagoTypesEvent Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : WagoTypesModule_75x_65x Library Identification : Placeholder: WagoTypesModule_75x_65x Default Resolution: WagoTypesModule_75x_65x, * (WAGO) Namespace: WagoTypesModule_75x_65x Library Properties :

### Function Blocks


## FbModule_75x_1652 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

Vorabrumpf für Gerätebeschreibung

Interface variables Vorabrumpf für Gerätebeschreibung - 10 I_ModuleParameter FbModule_75x_1652.ReadParameter (METH) - FbModule_75x_1652.WriteParameter (METH) 90 Internal - KbusContext helper FbModule_75x_1652.readStartUpValues (METH) I_Module_75x_1652 - FbModule_75x_1652.diRtsPostDelay (PROP) - FbModule_75x_1652.diRtsPreDelay (PROP) - FbModule_75x_1652.eBiasRx (PROP) - FbModule_75x_1652.eBiasTx (PROP) - FbModule_75x_1652.eRs485SwitchTime (PROP) - FbModule_75x_1652.eTerminationResistor (PROP) FbModule_75x_1652.protCheckPaSIze (METH)

## FbModule_75x_650 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_651 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_652 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

Interface variables - 10 I_ModuleParameter FbModule_75x_652.ReadParameter (METH) - FbModule_75x_652.WriteParameter (METH) 90 Internal - KbusContext helper FbModule_75x_652.readStartUpValues (METH) I_Module_75x_652 - FbModule_75x_652.diRtsPostDelay (PROP) - FbModule_75x_652.diRtsPreDelay (PROP) I_WagoSysDmx - FbModule_75x_652.diDmxStartAddress (PROP) FbModule_75x_652.protCheckPaSIze (METH)

## FbModule_75x_653 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

### Methods


## FbModule_75x_1652.ReadParameter (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ReadParameter | WagoTypesModuleBase.eServiceState |  |
| Input | cliCallerID | WagoTypes.WagoClientIdentification | Unique identifier of the caller |
| usiParameterNo | USINT |  |
| Inout | uiValue | UINT | value of the parameter |
| uiStatus | UINT | status word (register 57) of parameter communication |
| oError | WagoSysErrorBase.FbResult | error object |

| Mailboxstate | Description |
| --- | --- |
| eServiceState.OCCUPIED | occupied by an other caller |
| eServiceState.START | activate the MBX and start a job |
| eServiceState.BUSY | job is in process -> call it again until the return value = eServiceState.DONE |
| eServiceState.ABORT | job is aborted |
| eServiceState.DONE | job is done |

```
VAR
    ID          : WagoTypes.WagoClientIdentification := ADR(ID);  // generate an unique ID
    oError      : WagoSysErrorBase.FbResult;
    uiValue     : UINT; // after successful access value of the parameter
    uiStatus    : UINT; // after successful access status word
                        // (register 57) of parameter communication
END_VAR

CASE myModul.ReadParameter( cliCallerID     := ID,
                            usiParameterNo  := usiParameter,
                            uiValue         := uiValue,
                            uiStatus        := uiStatus,
                            oError          := oError
                        ) OF

    eServiceState.DONE :
        IF oError.GetID() = 0 THEN // OK

            (* place here your code *)

        ELSE
            (* place your error code *)
        END_IF

    eServiceState.ABORT :
        (* place your error code *)

END_CASE
```

Call a Parameter If the parameter channel is free then the wanted service will be triggered and the channel is occupied for other callers.

When the method returns with eServiceState.DONE then the wanted job is done. The user MUST handle the return values DONE and ABORT.

Graphical Illustration

Graphical Interface of FbModuleParameter.ReadParameter

This method can take a some plc cycles. So you have to call this method cyclic until it returns with DONE or ABORT.

Interface variables Function Call a Parameter If the parameter channel is free then the wanted service will be triggered and the channel is occupied for other callers. When the method returns with eServiceState.DONE then the wanted job is done. The user MUST handle the return values DONE and ABORT. RETURN State of the mailbox -> (defined at WagoAppModuleInterface.library) Graphical Illustration Graphical Interface of FbModuleParameter.ReadParameter Example Note This method can take a some plc cycles. So you have to call this method cyclic until it returns with DONE or ABORT.

## FbModule_75x_1652.WriteParameter (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | WriteParameter | WagoTypesModuleBase.eServiceState |  |
| Input | cliCallerID | WagoTypes.WagoClientIdentification | Unique identifier of the caller |
| usiParameterNo | USINT |  |
| uiValue | UINT | value of the parameter |
| Inout | uiStatus | UINT | status word (register 57) of parameter communication |
| oError | WagoSysErrorBase.FbResult | error object |

| Mailboxstate | Description |
| --- | --- |
| eServiceState.OCCUPIED | occupied by an other caller |
| eServiceState.START | activate the MBX and start a job |
| eServiceState.BUSY | job is in process -> call it again until the return value = eServiceState.DONE |
| eServiceState.ABORT | job is aborted |
| eServiceState.DONE | job is done |

```
VAR
    _ID         :   WagoTypes.WagoClientIdentification := ADR(_ID);

    uiValue     :   UINT;
    uiStatus    :   UINT;
    oError      :   WagoSysErrorBase.FbResult;
END_VAR

CASE myFbModuleParameter.WriteParameter( cliCallerID    := _ID,
                                         usiParameterNo := 1,
                                         uiValue        := uiValue,
                                         uiStatus       := uiStatus,
                                         oError         := oError
                                    ) OF
    eServiceState.DONE : // OK -> uiValue was written
            IF oError.GetID() = 0 THEN

                (* OK *)

            ELSE
                (* place your error code *)
            END_IF

    eServiceState.ABORT : // Error
            (* place your error code *)

END_CASE
```

Graphical Illustration

Graphical Interface of FbModuleParameter.WriteParameter

This method can take a some plc cycles. So you have to call this method cyclic until it returns with DONE or ABORT.

Interface variables Function Write the value``uiValue`` at terminals parameter list specified by usiParameterNo . cliCallerID have o be an unique WagoClientIdentification. RETURN State of the mailbox -> (defined at WagoAppModuleInterface.library) Graphical Illustration Graphical Interface of FbModuleParameter.WriteParameter Example Note This method can take a some plc cycles. So you have to call this method cyclic until it returns with DONE or ABORT.

## FbModule_75x_1652.protCheckPaSIze (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | protCheckPaSIze | BOOL |  |  |
| Input | uiPaNominalBitSize | UINT |  | The expected bit size of the module |
| ITerminal | WagoTypesBusServices.I_TerminalBase | 0 | Interface to terminal at that this module is registered |

This method is called at static configuration for Kbus-Modules only. If this method returns with TRUE a reboot of the controller will be initiated.

At the derivated method you have to manipulate the registers of the module to change for the wanted uiPaNominalBitSize .

The wanted uiPaNominalBitSize is calculated by the devcie description.

You have not to return before the needed register change was done by your implementation.

Interface variables This method is called at static configuration for Kbus-Modules only. If this method returns with TRUE a reboot of the controller will be initiated. At the derivated method you have to manipulate the registers of the module to change for the wanted uiPaNominalBitSize . The wanted uiPaNominalBitSize is calculated by the devcie description. Note You have not to return before the needed register change was done by your implementation.

## FbModule_75x_1652.readStartUpValues (METH)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Return | readStartUpValues | BYTE |  |
| Inout | oError | WagoSysErrorBase.FbResult |  |
|  | inst_bInitStep | BYTE | INIT_READ_SOFTWAREVERSION |

## FbModule_75x_652.ReadParameter (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ReadParameter | WagoTypesModuleBase.eServiceState |  |
| Input | cliCallerID | WagoTypes.WagoClientIdentification | Unique identifier of the caller |
| usiParameterNo | USINT |  |
| Inout | uiValue | UINT | value of the parameter |
| uiStatus | UINT | status word (register 57) of parameter communication |
| oError | WagoSysErrorBase.FbResult | error object |

| Mailboxstate | Description |
| --- | --- |
| eServiceState.OCCUPIED | occupied by an other caller |
| eServiceState.START | activate the MBX and start a job |
| eServiceState.BUSY | job is in process -> call it again until the return value = eServiceState.DONE |
| eServiceState.ABORT | job is aborted |
| eServiceState.DONE | job is done |

```
VAR
    ID          : WagoTypes.WagoClientIdentification := ADR(ID);  // generate an unique ID
    oError      : WagoSysErrorBase.FbResult;
    uiValue     : UINT; // after successful access value of the parameter
    uiStatus    : UINT; // after successful access status word
                        // (register 57) of parameter communication
END_VAR

CASE myModul.ReadParameter( cliCallerID     := ID,
                            usiParameterNo  := usiParameter,
                            uiValue         := uiValue,
                            uiStatus        := uiStatus,
                            oError          := oError
                        ) OF

    eServiceState.DONE :
        IF oError.GetID() = 0 THEN // OK

            (* place here your code *)

        ELSE
            (* place your error code *)
        END_IF

    eServiceState.ABORT :
        (* place your error code *)

END_CASE
```

Call a Parameter If the parameter channel is free then the wanted service will be triggered and the channel is occupied for other callers.

When the method returns with eServiceState.DONE then the wanted job is done. The user MUST handle the return values DONE and ABORT.

Graphical Illustration

Graphical Interface of FbModuleParameter.ReadParameter

This method can take a some plc cycles. So you have to call this method cyclic until it returns with DONE or ABORT.

Interface variables Function Call a Parameter If the parameter channel is free then the wanted service will be triggered and the channel is occupied for other callers. When the method returns with eServiceState.DONE then the wanted job is done. The user MUST handle the return values DONE and ABORT. RETURN State of the mailbox -> (defined at WagoAppModuleInterface.library) Graphical Illustration Graphical Interface of FbModuleParameter.ReadParameter Example Note This method can take a some plc cycles. So you have to call this method cyclic until it returns with DONE or ABORT.

## FbModule_75x_652.WriteParameter (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | WriteParameter | WagoTypesModuleBase.eServiceState |  |
| Input | cliCallerID | WagoTypes.WagoClientIdentification | Unique identifier of the caller |
| usiParameterNo | USINT |  |
| uiValue | UINT | value of the parameter |
| Inout | uiStatus | UINT | status word (register 57) of parameter communication |
| oError | WagoSysErrorBase.FbResult | error object |

| Mailboxstate | Description |
| --- | --- |
| eServiceState.OCCUPIED | occupied by an other caller |
| eServiceState.START | activate the MBX and start a job |
| eServiceState.BUSY | job is in process -> call it again until the return value = eServiceState.DONE |
| eServiceState.ABORT | job is aborted |
| eServiceState.DONE | job is done |

```
VAR
    _ID         :   WagoTypes.WagoClientIdentification := ADR(_ID);

    uiValue     :   UINT;
    uiStatus    :   UINT;
    oError      :   WagoSysErrorBase.FbResult;
END_VAR

CASE myFbModuleParameter.WriteParameter( cliCallerID    := _ID,
                                         usiParameterNo := 1,
                                         uiValue        := uiValue,
                                         uiStatus       := uiStatus,
                                         oError         := oError
                                    ) OF
    eServiceState.DONE : // OK -> uiValue was written
            IF oError.GetID() = 0 THEN

                (* OK *)

            ELSE
                (* place your error code *)
            END_IF

    eServiceState.ABORT : // Error
            (* place your error code *)

END_CASE
```

Graphical Illustration

Graphical Interface of FbModuleParameter.WriteParameter

This method can take a some plc cycles. So you have to call this method cyclic until it returns with DONE or ABORT.

Interface variables Function Write the value``uiValue`` at terminals parameter list specified by usiParameterNo . cliCallerID have o be an unique WagoClientIdentification. RETURN State of the mailbox -> (defined at WagoAppModuleInterface.library) Graphical Illustration Graphical Interface of FbModuleParameter.WriteParameter Example Note This method can take a some plc cycles. So you have to call this method cyclic until it returns with DONE or ABORT.

## FbModule_75x_652.diDmxStartAddress (PROP)


-1 –> use terminal settings otherwise allowed range 1..492

-1 –> use terminal settings otherwise allowed range 1..492

## FbModule_75x_652.protCheckPaSIze (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | protCheckPaSIze | BOOL |  |  |
| Input | uiPaNominalBitSize | UINT |  | The expected bit size of the module |
| ITerminal | WagoTypesBusServices.I_TerminalBase | 0 | Interface to terminal at that this module is registered |

This method is called at static configuration for Kbus-Modules only. If this method returns with TRUE a reboot of the controller will be initiated.

At the derivated method you have to manipulate the registers of the module to change for the wanted uiPaNominalBitSize .

The wanted uiPaNominalBitSize is calculated by the devcie description.

You have not to return before the needed register change was done by your implementation.

Interface variables This method is called at static configuration for Kbus-Modules only. If this method returns with TRUE a reboot of the controller will be initiated. At the derivated method you have to manipulate the registers of the module to change for the wanted uiPaNominalBitSize . The wanted uiPaNominalBitSize is calculated by the devcie description. Note You have not to return before the needed register change was done by your implementation.

## FbModule_75x_652.readStartUpValues (METH)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Return | readStartUpValues | BYTE |  |
| Inout | oError | WagoSysErrorBase.FbResult |  |
|  | inst_bInitStep | BYTE | INIT_READ_SOFTWAREVERSION |

### Internal Components


## 90 Internal


- KbusContext helper FbModule_75x_652.readStartUpValues (METH)

## 90 Internal


- KbusContext helper FbModule_75x_1652.readStartUpValues (METH)

### Global Variable Lists


## ErrorModule (GVL)


| Scope | Name | Type |
| --- | --- | --- |
| Constant | MODULE_ERRORS | ARRAY [0..12] OF WagoTypesErrorBase.typResultItem |

| Value | Level | Description |
| --- | --- | --- |
| PARAMETER_OK | WagoTypesErrorBase.WagoTypes.eSeverity.none | ‘OK’ |
| PARAMETER_INVALID_BAUDRATE | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Not supported baudrate’ |
| PARAMETER_INVALID_PARITY | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Not supported parity’ |
| PARAMETER_INVALID_STOPBITS | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Not supported stopbits’ |
| PARAMETER_INVALID_DATABITS | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Not supported databits’ |
| PARAMETER_INVALID_HANDSHAKE | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Not supported handshake’ |
| PARAMETER_INVALID_PHYSICAL_LAYER | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Not supported physical layer’ |
| PARAMETER_INVALID_COMBINATION_PHYSICAL_LAYER_HANDSHAKE | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Not allowed combination physical layer -> handshake’ |
| PARAMETER_UNKNOWN_MODULE | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Unknown module check the orderno. ‘ |
| PARAMETER_INVALID_VERSION | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Invalid software version at the module’ |
| PARAMETER_INVALID_BIASMODE | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Invalid bias mode parameter’ |
| PARAMETER_INVALID_TERMINATION | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Invalid termination parameter’ |
| PARAMETER_INVALID_RS485SWITCHTIME | WagoTypesErrorBase.WagoTypes.eSeverity.error | ‘Invalid RS485 switch time’ |

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 05.02.2024 | 1.9.5.15 | u010663 | Compiled with SP16.3 |
| 25.01.2024 | 1.9.5.14 | u010663 | Test only |
| 20.12.2023 | 1.9.5.13 | u0103719 | WAT36184: add PA update (context: ACTION_IDLE) |
| 24.10.2023 | 1.9.5.12 | u0103719 | replace SysTypes Interfaces via SysTypes2 Interfaces |
| 23.02.2023 | 1.9.5.11 | u010545 | disable continous send 652 |
| 14.02.2023 | 1.9.5.10 | u010545 | bugfixes 1652 |
| 13.12.2022 | 1.9.5.9 | u010545 | fixes at documentation |
| 13.10.2022 | 1.9.5.8 | u010545 | bugfix startup 652 / 1652 |
| 18.05.2022 | 1.9.5.7 | u010545 | bugfix init 652 |
| 24.03.2022 | 1.9.5.6 | u010545 | bugfix init 652 |
| 18.01.2022 | 1.9.5.5 | u010545 | 1652 –> second tag |
| 16.12.2021 | 1.9.5.4 | u010545 | 1652 –> first tag |
| 11.08.2021 | 1.9.5.3 | u010545 | First preparation for 1652 (development) |
| 22.03.2021 | 1.9.5.2 | u010545 | Dummy for 1652 added |
| 07.12.2020 | 1.9.5.1 | u010545 | Sniffer modified |
| 24.11.2020 | 1.9.5.0 | u010545 | Sniffer implemented |
| 15.07.2020 | 1.9.4.1 | u010545 | Bugfix ErrorFactory |
| 04.05.2020 | 1.9.4.0 | u010545 | Parameterservice modified |
| 08.01.2019 | 1.9.3.0 | u015842 | Properties: free placeholder added |
| 22.06.2018 | 1.9.2.3 | u013972 | Change images for the documentation |
| 02.02.2018 | 1.9.2.2 | u010545 | Bugfix change parameter at 750-653/025-000 |
| 20.12.2017 | 1.9.2.1 | u010545 | Bugfix Baudrate 650 / 651 / 653 |
| 04.12.2017 | 1.9.2.0 | u010545 | TscFuse removed |
| 13.11.2017 | 1.9.1.0 | u010545 | update resize module PA |
| 06.11.2017 | 1.9.0.1 | u010545 | update performance |
| 29.09.2017 | 1.9.0.0 | u010545 | changed for compability with old WagoSysModuleBase |
| 22.08.2017 | 1.8.1.1 | u010545 | Resize module PA |
| 03.08.2017 | 1.8.1.0 | u010545 | I_FuseService implemented |
| 20.07.2017 | 1.8.0.2 | u010545 | extends FbModuleBasExtended |
| 23.06.2017 | 1.8.0.1 | u010545 | data types changed |
| 25.04.2017 | 1.8.0.0 | u010545 | First version for new module access concept |
| 05.01.2017 | 1.7.0.6 | u010545 | RS422 for 750-652 implemented |
| 27.09.2016 | 1.7.0.5 | u010545 | I_DmxModule implemented |
| 23.09.2016 | 1.7.0.4 | u010545 | All Bytes Transmitted implemented |
| 21.09.2016 | 1.7.0.3 | u010545 | Modification for 642 (Enocean) |
| 19.09.2016 | 1.7.0.2 | u010545 | Modification for DMX |
| 29.07.2016 | 1.7.0.1 | u010545 | Documentation modified |
| 28.07.2016 | 1.7.0.0 | u010545 | serial modules as tty device at FW mounted -> FW7 needed |
| 02.03.2016 | 1.6.0.0 | u010545 | WagoAppErrorBase changed to WagoSysErrorBase / WagoTypesErrorBase |
| 22.02.2016 | 1.5.1.2 | u010545 | bugfix for receive data |
| 10.02.2016 | 1.5.1.1 | u010545 | oError moved to FbModuleBase |
| 28.01.2016 | 1.5.1.0 | u010545 | Concept changed -> now it runs in kbus context |
| 10.11.2015 | 1.5.0.6 | u010545 | bugfix init |
| 29.09.2015 | 1.5.0.5 | u010545 | placeholder at librarymanger included |
| 24.08.2015 | 1.5.0.4 | u010545 | attribut placeholder included |
| 07.08.2015 | 1.5.0.3 | u010545 | WagoTypesCommon included for Hudson |
| 26.06.2015 | 1.5.0.2 | u010545 | attribute ‘displaysorting’ removed |
| 22.06.2015 | 1.5.0.1 | u010545 | internal datatype fixed |
| 03.06.2015 | 1.5.0.0 | u010545 | released |
| 29.04.2015 | 1.1.0.3 | UU | Pointer To Any changed to Pointer To Byte |
| 07.04.2015 | 1.1.0.2 | UU | Error List modified |
| 19.03.2015 | 1.1.0.1 | JMü | Rename interface variables of method read and write |
| 03.03.2015 | 1.0.0.1 | UU | Property isOpen changed to IsOpen |
| 10.12.2014 | 1.0.0.0 | UU | WagoTypesErrorBase V 1.0.0.0 supported |
| 10.11.2014 | 0.0.0.8 | UU | 600 Baud fo 652 implemented |
| 21.10.2014 | 0.0.0.7 | UU | documentation |
| 09.10.2014 | 0.0.0.6 | UU | rename of structs at WagoSysKbusAsyncCom implemented |
| 23.09.2014 | 0.0.0.5 | UU | version of sub libraries modified |
| 18.09.2014 | 0.0.0.4 | VB | new library name |
| 21.08.2014 | 0.0.0.3 | UU | local RxBuffer implemented |
| 08.08.2014 | 0.0.0.2 | UU | new version of I_WagoSysComBase supported |
| 06.08.2014 | 0.0.0.1 | UU | settings modified |
| 04.08.2014 | 0.0.0.0 | UU | created |

WagoSysModule_75x_65x

WagoSysModule_75x_65x

### Other Components


## 10 Error Module


- ErrorModule (GVL) - eErrorModule (ENUM)

## 10 I_ModuleParameter


- FbModule_75x_652.ReadParameter (METH) - FbModule_75x_652.WriteParameter (METH)

## 10 I_ModuleParameter


- FbModule_75x_1652.ReadParameter (METH) - FbModule_75x_1652.WriteParameter (METH)

## 20 Program Organitzation Unit


- FbModule_75x_1652 (FB) 10 I_ModuleParameter FbModule_75x_1652.ReadParameter (METH) - FbModule_75x_1652.WriteParameter (METH) 90 Internal - KbusContext helper FbModule_75x_1652.readStartUpValues (METH) I_Module_75x_1652 - FbModule_75x_1652.diRtsPostDelay (PROP) - FbModule_75x_1652.diRtsPreDelay (PROP) - FbModule_75x_1652.eBiasRx (PROP) - FbModule_75x_1652.eBiasTx (PROP) - FbModule_75x_1652.eRs485SwitchTime (PROP) - FbModule_75x_1652.eTerminationResistor (PROP) FbModule_75x_1652.protCheckPaSIze (METH) FbModule_75x_650 (FB) FbModule_75x_651 (FB) FbModule_75x_652 (FB) - 10 I_ModuleParameter FbModule_75x_652.ReadParameter (METH) - FbModule_75x_652.WriteParameter (METH) 90 Internal - KbusContext helper FbModule_75x_652.readStartUpValues (METH) I_Module_75x_652 - FbModule_75x_652.diRtsPostDelay (PROP) - FbModule_75x_652.diRtsPreDelay (PROP) I_WagoSysDmx - FbModule_75x_652.diDmxStartAddress (PROP) FbModule_75x_652.protCheckPaSIze (METH) FbModule_75x_653 (FB)

## 80 Status


- 10 Error Module ErrorModule (GVL) - eErrorModule (ENUM)

## FbModule_75x_1652.diRtsPostDelay (PROP)


-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

## FbModule_75x_1652.diRtsPreDelay (PROP)


-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

## FbModule_75x_1652.eBiasRx (PROP)


| Member | Value | Description |
| --- | --- | --- |
| Default | -1 | use interface default settings |
| Disabled | 0 | Off |
| Network_1 | 1 | Network 1 |
| Network_2 | 2 | Network 2 |

WagoTypesModule_75x_65x.eTTYBias

WagoTypesModule_75x_65x.eTTYBias

## FbModule_75x_1652.eBiasTx (PROP)


| Member | Value | Description |
| --- | --- | --- |
| Default | -1 | use interface default settings |
| Disabled | 0 | Off |
| Network_1 | 1 | Network 1 |
| Network_2 | 2 | Network 2 |

WagoTypesModule_75x_65x.eTTYBias

WagoTypesModule_75x_65x.eTTYBias

## FbModule_75x_1652.eRs485SwitchTime (PROP)


| Member | Value | Description |
| --- | --- | --- |
| Default | -1 | use interface default settings |
| NoDelay | 0 | Off |
| _100us | 1 | 100 us |
| _2Characters | 2 | 2 character times |
| _4Characters | 3 | 4 character times |

WagoTypesModule_75x_65x.eTTYRs485SwitchTime

WagoTypesModule_75x_65x.eTTYRs485SwitchTime

## FbModule_75x_1652.eTerminationResistor (PROP)


| Member | Value | Description |
| --- | --- | --- |
| Default | -1 | use interface default settings |
| Off | 0 | Off |
| On | 1 | On |

WagoTypesModule_75x_65x.eTTYTerminationResistor

WagoTypesModule_75x_65x.eTTYTerminationResistor

## FbModule_75x_652.diRtsPostDelay (PROP)


-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

## FbModule_75x_652.diRtsPreDelay (PROP)


-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

-1 –> use terminal settings otherwise allowed range 0..1000 [ms]

## I_Module_75x_1652


- FbModule_75x_1652.diRtsPostDelay (PROP) - FbModule_75x_1652.diRtsPreDelay (PROP) - FbModule_75x_1652.eBiasRx (PROP) - FbModule_75x_1652.eBiasTx (PROP) - FbModule_75x_1652.eRs485SwitchTime (PROP) - FbModule_75x_1652.eTerminationResistor (PROP)

## I_Module_75x_652


- FbModule_75x_652.diRtsPostDelay (PROP) - FbModule_75x_652.diRtsPreDelay (PROP)

## I_WagoSysDmx


- FbModule_75x_652.diDmxStartAddress (PROP)

## KbusContext


- helper FbModule_75x_652.readStartUpValues (METH)

## KbusContext


- helper FbModule_75x_1652.readStartUpValues (METH)

## Parameter (PARAMS)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | MAX_PIPE_SIZE | UDINT | 1024 |

## eErrorModule (ENUM)


| Name | Initial |
| --- | --- |
| PARAMETER_OK | 16#0 |
| PARAMETER_INVALID_BAUDRATE | 16#1 |
| PARAMETER_INVALID_PARITY | 16#2 |
| PARAMETER_INVALID_STOPBITS | 16#3 |
| PARAMETER_INVALID_DATABITS | 16#4 |
| PARAMETER_INVALID_HANDSHAKE | 16#5 |
| PARAMETER_INVALID_PHYSICAL_LAYER | 16#6 |
| PARAMETER_INVALID_COMBINATION_PHYSICAL_LAYER_HANDSHAKE | 16#7 |
| PARAMETER_UNKNOWN_MODULE | 16#8 |
| PARAMETER_INVALID_VERSION | 16#9 |
| PARAMETER_INVALID_BIASMODE | 16#A |
| PARAMETER_INVALID_TERMINATION | 16#B |
| PARAMETER_INVALID_RS485SWITCHTIME | 16#C |

## helper


- FbModule_75x_1652.readStartUpValues (METH)

## helper ¶


- FbModule_75x_652.readStartUpValues (METH)