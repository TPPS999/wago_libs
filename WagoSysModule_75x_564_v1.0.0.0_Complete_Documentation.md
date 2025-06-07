# WagoSysModule_75x_564 v1.0.0.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysModule_75x_564
- **Version:** 1.0.0.0
- **Categories:** WAGO LayerView|Sys; Application
- **Author:** WAGO
- **Placeholder:** WagoSysModule_75x_564

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling modules 75x-564 [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling modules 75x-564 [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks FbModule_75x_564 (FB) - FbModule_75x_564_dynConfig (FB) Methods - FbModule_75x_564.ClearReadFlags (METH) - FbModule_75x_564.GetModuleConfiguration (METH) - FbModule_75x_564.GetRawChannelCalibration (METH) - FbModule_75x_564.GetRawChannelConfiguration (METH) - FbModule_75x_564.GetRawChannelScaling (METH) - FbModule_75x_564.GetRawChannelSettings (METH) - FbModule_75x_564.SetModuleConfiguration (METH) - FbModule_75x_564.SetRawChannelCalibration (METH) - FbModule_75x_564.SetRawChannelConfiguration (METH) - FbModule_75x_564.SetRawChannelScaling (METH) - ... and 14 more Program Organization Global Variable Lists - Error_564 (GVL) - VersionHistory (GVL) Other Components - 80 Status - Channel - I_ModuleProcessOutputsExtended - I_Module_75x_564 - eError_564 (ENUM)

### Indices and tables ¶


| [1] | Based on WagoSysModule_75x_564.library, last modified 08.04.2020, 16:31:28. The content of this file was automatically generated with None on 08.04.2020, 16:31:44 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysModule_75x_564 Library Documentation


| Company: | WAGO |
| Title: | WagoSysModule_75x_564 |
| Version: | 1.0.0.0 |
| Categories: | WAGO LayerView\|Sys; Application |
| Author: | WAGO |
| Placeholder: | WagoSysModule_75x_564 |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling modules 75x-564 [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling modules 75x-564 [1]

### Contents:


- 20 Program Organization Units FbModule_75x_564 (FB) - FbModule_75x_564_dynConfig (FB) 80 Status - Error_564 (GVL) - eError_564 (ENUM) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysModule_75x_564.library, last modified 08.04.2020, 16:31:28. The content of this file was automatically generated with None on 08.04.2020, 16:31:44 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysModule_75x_564.library |
| contentFile | WagoSysModule_75x_564_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 08.04.2020, 16:31:44 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 08.04.2020, 16:31:28 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysModule_75x_564 |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysModule_75x_564 |
| Version | version | 1.0.0.0 |
| ActivateSigning | bool | False |
| Title | string | WagoSysModule_75x_564 |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |
| Version string | string |  |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False PublishSymbolsInContainer: True | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MODULE_QUANTITY = 250 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MAX_RUNNABLES = MAX_MODULE_QUANTITY Parameter: PARAMETER_COM_TIMEOUT = TIME#5s0ms Parameter: MBX_PIPE_SIZE = 1024 Parameter: REGISTER_COM_TIMEOUT = TIME#5s0ms Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MAX_MBX_INPUT_SIZE = 47 WagoSysModuleBaseProtected Library Identification : Placeholder: WagoSysModuleBaseProtected Default Resolution: WagoSysModuleBaseProtected, * (WAGO) Namespace: WagoSysModuleBaseProtected Library Properties : Library Parameter : Parameter: REGISTER_COM_TIMEOUT = TIME#5s0ms Parameter: PARAMETER_COM_TIMEOUT = TIME#5s0ms WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesBusServices Library Identification : Placeholder: WagoTypesBusServices Default Resolution: WagoTypesBusServices, * (WAGO) Namespace: WagoTypesBusServices Library Properties : Library Parameter : Parameter: MAX_RUNNABLES = MAX_MODULE_QUANTITY Parameter: MAX_MODULE_QUANTITY = 250 WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : Library Parameter : Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MAX_MODULE_QUANTITY = 250 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MAX_RUNNABLES = MAX_MODULE_QUANTITY Parameter: MBX_PIPE_SIZE = 1024 Parameter: MAX_MBX_SIZE = 18 Parameter: MAX_MBX1_SIZE = 18 Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MBX_INPUT_SIZE = 47 WagoTypesModule_75x_564 Library Identification : Placeholder: WagoTypesModule_75x_564 Default Resolution: WagoTypesModule_75x_564, * (WAGO) Namespace: WagoTypesModule_75x_564 Library Properties :

### Function Blocks


## FbModule_75x_564 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

Access to the module 750-564

Function description

This block is needed for each module. The instance of this function block is either automatically generated by the K-Bus configuration or has to be manually added in case of the dynamic configuration.

Interface variables Function Access to the module 750-564 Function description This block is needed for each module. The instance of this function block is either automatically generated by the K-Bus configuration or has to be manually added in case of the dynamic configuration. - I_Module_75x_564 Channel FbModule_75x_564.GetRawChannelCalibration (METH) - FbModule_75x_564.GetRawChannelScaling (METH) - FbModule_75x_564.GetRawChannelSettings (METH) - FbModule_75x_564.SetRawChannelCalibration (METH) - FbModule_75x_564.SetRawChannelScaling (METH) - FbModule_75x_564.SetRawChannelSettings (METH) FbModule_75x_564.ClearReadFlags (METH) FbModule_75x_564.GetModuleConfiguration (METH) FbModule_75x_564.GetRawChannelConfiguration (METH) FbModule_75x_564.SetModuleConfiguration (METH) FbModule_75x_564.SetRawChannelConfiguration (METH)

## FbModule_75x_564_dynConfig (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

Function description

Interface variables Function Access to the module 750-564 with PA-Access In case of dynamic configuration the FB provides additional the PA-Access. Function description This block is needed for each module. The instance of this function block has to be manually added in case of the dynamic configuration. - FbModule_75x_564_dynConfig.GetRawProcessValue (METH) - I_ModuleProcessOutputsExtended FbModule_75x_564_dynConfig.GetModuleOutputSize (METH) - FbModule_75x_564_dynConfig.GetProcessOutBit (METH) - FbModule_75x_564_dynConfig.GetProcessOutByte (METH) - FbModule_75x_564_dynConfig.GetProcessOutData (METH) - FbModule_75x_564_dynConfig.GetProcessOutDword (METH) - FbModule_75x_564_dynConfig.GetProcessOutWord (METH) - FbModule_75x_564_dynConfig.SetProcessOutBit (METH) - FbModule_75x_564_dynConfig.SetProcessOutByte (METH) - FbModule_75x_564_dynConfig.SetProcessOutData (METH) - FbModule_75x_564_dynConfig.SetProcessOutDword (METH) - FbModule_75x_564_dynConfig.SetProcessOutWord (METH) FbModule_75x_564_dynConfig.SetRawProcessValue (METH)

### Methods


## FbModule_75x_564.ClearReadFlags (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ClearReadFlags | WagoTypesBusServices.I_ModuleBaseAccessService |
| Inout | xTrigger | BOOL |

Interface variables Function This function is only needed, if the configuration is done by the plc programm and parallel by an external tool like Wago-IO-Check. The method will reset the internal data storage. This will deactivate an internal optimisation.

## FbModule_75x_564.GetModuleConfiguration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetModuleConfiguration | WagoTypesModuleBase.eServiceState |
| Inout | xTrigger | BOOL |
| utModuleConfiguration | WagoTypesModule_75x_564.typModuleConfiguration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| aChannel | ARRAY of typRawChannelConfiguration | Channel configuration |
| xDiagPowerSupplyEnabled | BOOL | Diagnosis power supply On/Off |
| xSynchronousDAconversion | BOOL | Synchronous DA conversion On/Off |
| xDiagWiringError_AOMinusEnabled | BOOL | Diagnosis wiring error AO- On/Off |
| wWatchdogPostDelay | WORD | K-Bus timeout Post-Delay [ms] |
| xUseStandardProcessImage | BOOL | Standard process image On/Off |

```
VAR
    //--- Module configuration ---------------------------------
    utModuleConfiguration       :   WagoTypesModule_75x_564.typRawChannelConfiguration;
    xModuleConfiguration        :   BOOL;
    oError                      :   WagoSysErrorBase.FbResult;
END_VAR

//--- M O D U L E    C O N F I G U R A T I O N -----------------------
CASE my564.GetModuleConfiguration(
                                        xTrigger                    := xGetModuleConfiguration,
                                        utModuleConfiguration       := utModuleConfiguration,
                                        oError                      => oError
                                    ) OF

    eServiceState.DONE : // OK
            ;// process here your utChannelConfiguration

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

typModuleConfiguration

Graphical Illustration

Graphical Interface of FbModule_75x_564.GetModuleConfiguration

Get the module configuration

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the complete module configuration typModuleConfiguration Graphical Illustration ![Image](images/wagosysmodule_75x_564_c37f194b.png) Graphical Interface of FbModule_75x_564.GetModuleConfiguration Example Get the module configuration Note You have to call the method cyclic until the method returns with DONE or ABORT.

## FbModule_75x_564.GetRawChannelCalibration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelCalibration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..WagoTypesModule_75x_564.MAX_CHANNEL_564) |
| Inout | xTrigger | BOOL |
| utRawChannelCalibration | WagoTypesModule_75x_564.typRawChannelCalibration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserCalibration | FALSE | The user calibration is switched off |
| TRUE | The user calibration is switched on |
| iUserCalibrationOffset | -32768 ... 32767 | User calibration Offset |
| iUserCalibrationGain | -32768 ... 32767 | User calibration Gain * 1/16834 |

```
VAR
    //--- Channel Calibration ---------------------------------
    utChannelCalibration    :   WagoTypesModule_75x_564.typRawChannelCalibration;;
    xGetChannelCalibration  :   BOOL;
    oError                  :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L    C A L I B R A T I O N -----------------------
CASE my564.GetRawChannelCalibration(    usiChannel              := 1,
                                        xTrigger                := xGetChannelCalibration,
                                        utRawChannelCalibration := utChannelCalibration,
                                        oError                  => oError
                                    ) OF

    eServiceState.DONE : // OK
            ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

typRawChannelCalibration

Graphical Illustration

Graphical Interface of FbModule_75x_564.GetRawChannelCalibration

Get the calibration from channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the calibration settings of a channel typRawChannelCalibration Graphical Illustration ![Image](images/wagosysmodule_75x_564_e10a9928.png) Graphical Interface of FbModule_75x_564.GetRawChannelCalibration Example Get the calibration from channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## FbModule_75x_564.GetRawChannelConfiguration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelConfiguration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..WagoTypesModule_75x_564.MAX_CHANNEL_564) |
| Inout | xTrigger | BOOL |
| utRawChannelConfiguration | WagoTypesModule_75x_564.typRawChannelConfiguration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| Settings | typRawChannelSettings | Channel settings |
| Scaling | typRawChannelScaling | Channel scaling |
| Calibration | typRawChannelCalibration | Channel calibration |

```
VAR
    //--- Channel Configuration ---------------------------------
    utRawChannelConfiguration   :   WagoTypesModule_75x_564.typRawChannelConfiguration;
    xGetRawChannelConfiguration :   BOOL;
    oError                      :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L    C O N F I G U R A T I O N -----------------------
CASE my564.GetRawChannelConfiguration(  usiChannel                  := 1,
                                        xTrigger                    := xGetRawChannelConfiguration,
                                        utRawChannelConfiguration   := utRawChannelConfiguration,
                                        oError                      => oError
                                    ) OF

    eServiceState.DONE : // OK
            ;// process here your utChannelConfiguration

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

typRawChannelConfiguration

Graphical Illustration

Graphical Interface of FbModule_75x_564.GetRawChannelConfiguration

Get the configuration from channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the complete raw configuration of a channel typRawChannelConfiguration Graphical Illustration ![Image](images/wagosysmodule_75x_564_f6bd42bf.png) Graphical Interface of FbModule_75x_564.GetRawChannelConfiguration Example Get the configuration from channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## FbModule_75x_564.GetRawChannelScaling (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelScaling | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..WagoTypesModule_75x_564.MAX_CHANNEL_564) |
| Inout | xTrigger | BOOL |
| utRawChannelScaling | WagoTypesModule_75x_564.typRawChannelScaling |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserScalingEnabled | FALSE | User scaling disabled |
| TRUE | User scaling enabled |
| iUserScalingOffset | -32768 ... 32767 | User scaling Offset |
| iUserScalingGain | -32768 ... 32767 | User scaling Gain -> 1/16384 |
| xFactoryScalingEnabled | FALSE | Factory scaling disabled |
| TRUE | Factory scaling enabled |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelScaling    :   WagoTypesModule_75x_564.typRawChannelScaling;;
    xGetChannelScaling  :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S C A L I N G ------------------------
CASE my564.GetRawChannelScaling(    usiChannel           := 1,
                                    xTrigger             := xGetChannelScaling,
                                    utRawChannelScaling  := utChannelScaling,
                                    oError               => oError
                                ) OF

    eServiceState.DONE : // OK
            ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

typRawChannelScaling

Graphical Illustration

Graphical Interface of FbModule_75x_564.GetRawChannelScaling

Get the scaling from channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the scaling settings of a channel typRawChannelScaling Graphical Illustration ![Image](images/wagosysmodule_75x_564_735663b1.png) Graphical Interface of FbModule_75x_564.GetRawChannelScaling Example Get the scaling from channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## FbModule_75x_564.GetRawChannelSettings (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelSettings | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..WagoTypesModule_75x_564.MAX_CHANNEL_564) |
| Inout | xTrigger | BOOL |
| utRawChannelSettings | WagoTypesModule_75x_564.typRawChannelSettings |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| eSignalType | eSignalType | see chapter 10 Enumeration |
| xDiagGlobalEnabled | Channel diagnosis |
| FALSE | Diagnosis disabled |
| TRUE | Diagnosis enabled |
| xDiagWireBreakEnabled | Wire break diagnosis |
| FALSE | Diagnosis disabled |
| TRUE | Diagnosis enabled |
| xDiagShortCircuitEnabled | Short circuit diagnosis |
| FALSE | Diagnosis disabled |
| TRUE | Diagnosis enabled |
| xDiagWiringEnabled | Wiring error diagnosis |
| FALSE | Diagnosis disabled |
| TRUE | Diagnosis enabled |
| xDiagDAC_InternalEnabled | DAC internal diagnosis |
| FALSE | Diagnosis disabled |
| TRUE | Diagnosis enabled |
| xResolution15Bit | Resolution |
| FALSE | 16 bit resolution |
| TRUE | 15 bit resolution |
| eWatchdog | eWatchdog | see chapter 10 Enumeration |
| uiUserSubstituteValue | uSubstituteValue | see chapter 10 Enumeration |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelSettings   :   WagoTypesModule_75x_564.typRawChannelSettings;;
    xGetChannelSettings :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S E T T I N G S ----------------------
CASE my563.GetRawChannelSettings(   usiChannel           := 1,
                                    xTrigger             := xGetChannelSettings,
                                    utRawChannelSettings := utChannelSettings,
                                    oError               => oError
                                ) OF

    eServiceState.DONE : // OK
        ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
        ;// process here your error handling -> see oError for more information

END_CASE
```

typRawChannelSettings

Graphical Illustration

Graphical Interface of FbModule_75x_564.GetRawChannelSettings

Get the settings from channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the general channel settings typRawChannelSettings Graphical Illustration ![Image](images/wagosysmodule_75x_564_14ac685a.png) Graphical Interface of FbModule_75x_564.GetRawChannelSettings Example Get the settings from channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## FbModule_75x_564.SetModuleConfiguration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetModuleConfiguration | WagoTypesModuleBase.eServiceState |
| Inout | xTrigger | BOOL |
| utModuleConfiguration | WagoTypesModule_75x_564.typModuleConfiguration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| aChannel | ARRAY of typRawChannelConfiguration | Channel configuration |
| xDiagPowerSupplyEnabled | BOOL | Diagnosis power supply On/Off |
| xSynchronousDAconversion | BOOL | Synchronous DA conversion On/Off |
| xDiagWiringError_AOMinusEnabled | BOOL | Diagnosis wiring error AO- On/Off |
| wWatchdogPostDelay | WORD | K-Bus timeout Post-Delay [ms] |
| xUseStandardProcessImage | BOOL | Standard process image On/Off |

```
VAR
    //--- Channel Configuration -------------------------------------------------------
    xStartProcess               :   BOOL; // set this variable once to start the process -> this varibale will be automatic reset
    utModuleConfiguration       :   WagoTypesModule_75x_564.typModuleConfiguration;
    oError                      :   WagoSysErrorBase.FbResult;
    xSetModuleConfiguration     :   BOOL;
END_VAR

//--- M O D U L E    C O N F I G U R A T I O N -----------------------
//--- READ BEFORE WRITE --------------------------------------------------------------
CASE my564.GetModuleConfiguration( 1, xStartProcess, utModuleConfiguration, oError => oError) OF

    eServiceState.DONE : // OK -> actual configuration is successful read
        // change here your configuration
        // utModuleConfiguration... :=
        xSetModuleConfiguration := TRUE; // trigger write

    eServiceState.ABORT : // Error -> not able to read -> see oError
            ;// process here your error handling for read -> see oError for more information

END_CASE

//--- WRITE MODYFIED CONFIGURATION ---------------------------------------------------
CASE my564.SetModuleConfiguration( 1, xSetModuleConfiguration, utModuleConfiguration, oError => oError) OF

    eServiceState.DONE : // OK -> new configuration is written

    eServiceState.ABORT : // Error -> not able to write -> see oError
            ;// process here your error handling for write -> see oError for more information

END_CASE
```

typModuleConfiguration

Graphical Illustration

Graphical Interface of FbModule_75x_564.SetModuleConfiguration

Set the module configuration. After reading, an additional writing of the configuration is done if necessary

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the complete module configuration typModuleConfiguration Graphical Illustration ![Image](images/wagosysmodule_75x_564_ef995891.png) Graphical Interface of FbModule_75x_564.SetModuleConfiguration Example Set the module configuration. After reading, an additional writing of the configuration is done if necessary Note You have to call the method cyclic until the method returns with DONE or ABORT.

## FbModule_75x_564.SetRawChannelCalibration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelCalibration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..WagoTypesModule_75x_564.MAX_CHANNEL_564) |
| Inout | xTrigger | BOOL |
| utRawChannelCalibration | WagoTypesModule_75x_564.typRawChannelCalibration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserCalibration | FALSE | The user scaling is switched off |
| TRUE | The user scaling is switched on |
| iUserCalibrationOffset | -32768 ... 32767 | User calibration Offset |
| iUserCalibrationGain | -32768 ... 32767 | User calibration Gain * 1/16384 |

```
VAR
    //--- Channel Calibration ---------------------------------
    utChannelCalibration    :   WagoTypesModule_75x_564.typRawChannelCalibration;;
    xSetChannelCalibration  :   BOOL;
    oError                  :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L    C A L I B R A T I O N -----------------------
CASE my563.SetRawChannelCalibration(    usiChannel              := 1,
                                        xTrigger                := xSetChannelCalibration,
                                        utRawChannelCalibration := utChannelCalibration,
                                        oError                  => oError
                                   ) OF

    eServiceState.DONE : // OK
            ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

WagoTypesModule_75x_564.typRawChannelCalibration

Graphical Illustration

Graphical Interface of FbModule_75x_564.SetRawChannelCalibration

Set the calibration of channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the calibration of a channel WagoTypesModule_75x_564.typRawChannelCalibration Graphical Illustration ![Image](images/wagosysmodule_75x_564_a038a895.png) Graphical Interface of FbModule_75x_564.SetRawChannelCalibration Example Set the calibration of channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## FbModule_75x_564.SetRawChannelConfiguration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelConfiguration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..WagoTypesModule_75x_564.MAX_CHANNEL_564) |
| Inout | xTrigger | BOOL |
| utRawChannelConfiguration | WagoTypesModule_75x_564.typRawChannelConfiguration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| Settings | typRawChannelSettings | Channel settings |
| Scaling | typRawChannelScaling | Channel scaling |
| Calibration | typRawChannelCalibration | Channel calibration |

```
VAR
    //--- Channel Configuration -------------------------------------------------------
    xStartProcess               :   BOOL; // set this variable once to start the process -> this varibale will be automatic reset
    utRawChannelConfiguration   :   WagoTypesModule_75x_564.typRawChannelConfiguration;
    oError                      :   WagoSysErrorBase.FbResult;
    xSetRawChannelConfiguration :   BOOL;
END_VAR

//--- C H A N N E L    C O N F I G U R A T I O N -----------------------
//--- READ BEFORE WRITE --------------------------------------------------------------
CASE my564.GetRawChannelConfiguration( 1, xStartProcess, utRawChannelConfiguration, oError => oError) OF

    eServiceState.DONE : // OK -> actual configuration is successful read
        // change here your configuration
        // utRawChannelConfiguration... :=
        xSetRawChannelConfiguration := TRUE; // trigger write

    eServiceState.ABORT : // Error -> not able to read -> see oError
            ;// process here your error handling for read -> see oError for more information

END_CASE

//--- WRITE MODYFIED CONFIGURATION ---------------------------------------------------
CASE my564.SetRawChannelConfiguration( 1, xSetRawChannelConfiguration, utRawChannelConfiguration, oError => oError) OF

    eServiceState.DONE : // OK -> new configuration is written

    eServiceState.ABORT : // Error -> not able to write -> see oError
            ;// process here your error handling for write -> see oError for more information

END_CASE
```

typRawChannelConfiguration

Graphical Illustration

Graphical Interface of FbModule_75x_564.SetRawChannelConfiguration

Get the configuration from channel one. After reading, an additional writing of the configuration is done

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the complete raw configuration of a channel. typRawChannelConfiguration Graphical Illustration ![Image](images/wagosysmodule_75x_564_b5f2bc95.png) Graphical Interface of FbModule_75x_564.SetRawChannelConfiguration Example Get the configuration from channel one. After reading, an additional writing of the configuration is done Note You have to call the method cyclic until the method returns with DONE or ABORT.

## FbModule_75x_564.SetRawChannelScaling (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelScaling | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..WagoTypesModule_75x_564.MAX_CHANNEL_564) |
| Inout | xTrigger | BOOL |
| utRawChannelScaling | WagoTypesModule_75x_564.typRawChannelScaling |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserScalingEnabled | FALSE | User scaling disabled |
| TRUE | User scaling enabled |
| iUserScalingOffset | -32768 ... 32767 | User scaling Offset |
| iUserScalingGain | -32768 ... 32767 | User scaling Gain -> 1/16384 |
| xFactoryScalingEnabled | FALSE | Factory scaling disabled |
| TRUE | Factory scaling enabled |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelScaling    :   WagoTypesModule_75x_564.typRawChannelScaling;;
    xSetChannelScaling  :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S C A L I N G ------------------------
CASE my563.SetRawChannelScaling(    usiChannel          := 1,
                                    xTrigger            := xSetChannelScaling,
                                    utRawChannelScaling := utChannelScaling,
                                    oError              => oError
                                ) OF

    eServiceState.DONE : // OK
            ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

typRawChannelScaling

Graphical Illustration

Graphical Interface of FbModule_75x_564.SetRawChannelScaling

Set the scaling of channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the scaling of a channel typRawChannelScaling Graphical Illustration ![Image](images/wagosysmodule_75x_564_443ad56e.png) Graphical Interface of FbModule_75x_564.SetRawChannelScaling Example Set the scaling of channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## FbModule_75x_564.SetRawChannelSettings (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelSettings | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..WagoTypesModule_75x_564.MAX_CHANNEL_564) |
| Inout | xTrigger | BOOL |
| utRawChannelSettings | WagoTypesModule_75x_564.typRawChannelSettings |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| eSignalType | eSignalType | see chapter 10 Enumeration |
| xDiagGlobalEnabled | Channel diagnosis |
| FALSE | Diagnosis disabled |
| TRUE | Diagnosis enabled |
| xDiagWireBreakEnabled | Wire break diagnosis |
| FALSE | Diagnosis disabled |
| TRUE | Diagnosis enabled |
| xDiagShortCircuitEnabled | Short circuit diagnosis |
| FALSE | Diagnosis disabled |
| TRUE | Diagnosis enabled |
| xDiagWiringEnabled | Wiring error diagnosis |
| FALSE | Diagnosis disabled |
| TRUE | Diagnosis enabled |
| xDiagDAC_InternalEnabled | DAC internal diagnosis |
| FALSE | Diagnosis disabled |
| TRUE | Diagnosis enabled |
| xResolution15Bit | Resolution |
| FALSE | 16 bit resolution |
| TRUE | 15 bit resolution |
| eWatchdog | eWatchdog | see chapter 10 Enumeration |
| uiUserSubstituteValue | uSubstituteValue | see chapter 10 Enumeration |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelSettings   :   WagoTypesModule_75x_564.typRawChannelSettings;;
    xSetChannelSettings :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S E T T I N G S ----------------------
CASE my563.SetRawChannelSettings(   usiChannel           := 1,
                                    xTrigger             := xSetChannelSettings,
                                    utRawChannelSettings := utChannelSettings,
                                    oError               => oError
                                ) OF

    eServiceState.DONE : // OK
        ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
        ;// process here your error handling -> see oError for more information

END_CASE
```

typRawChannelSettings

Graphical Illustration

Graphical Interface of FbModule_75x_564.SetRawChannelSettings

Set the settings of channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the general channel settings typRawChannelSettings Graphical Illustration ![Image](images/wagosysmodule_75x_564_355dd6e0.png) Graphical Interface of FbModule_75x_564.SetRawChannelSettings Example Set the settings of channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## FbModule_75x_564_dynConfig.GetModuleOutputSize (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetModuleOutputSize | UINT |

Returns the byte size of output data

Interface variables Returns the byte size of output data

## FbModule_75x_564_dynConfig.GetProcessOutBit (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetProcessOutBit | BOOL |  |
| Input | ByteNo | UINT | range 0..(_uiOutputSize - 1) |
| BitNo | USINT | range 0..7 |

## FbModule_75x_564_dynConfig.GetProcessOutByte (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetProcessOutByte | BYTE |  |
| Input | ByteNo | UINT | range 0..(_uiOutputSize - 1) |

## FbModule_75x_564_dynConfig.GetProcessOutData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetProcessOutData | UINT |  |
| Input | pOutData | POINTER TO BYTE | pointer to the area where the process data should store |
| uiNOutData | UINT | SIZEOF(Buffer) |

## FbModule_75x_564_dynConfig.GetProcessOutDword (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetProcessOutDword | DWORD |  |
| Input | ByteNo | UINT | range 0..(_uiOutputSize - 4) |

Graphical Illustration

Graphical Interface of FbModule_75x_564_dynConfig.GetProcessOutDword

Interface variables Function Get the process output dword specified by ByteNo of this module. Graphical Illustration ![Image](images/wagosysmodule_75x_564_46ba5d46.png) Graphical Interface of FbModule_75x_564_dynConfig.GetProcessOutDword

## FbModule_75x_564_dynConfig.GetProcessOutWord (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetProcessOutWord | WORD |  |
| Input | ByteNo | UINT | range 0..(_uiOutputSize - 2) |

Graphical Illustration

Graphical Interface of FbModule_75x_564_dynConfig.GetProcessOutWord

Interface variables Function Get the process output word specified by ByteNo of this module. Graphical Illustration ![Image](images/wagosysmodule_75x_564_643fe4fb.png) Graphical Interface of FbModule_75x_564_dynConfig.GetProcessOutWord

## FbModule_75x_564_dynConfig.GetRawProcessValue (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawProcessValue | UINT |
| Input | usiChannel | USINT (1..WagoTypesModule_75x_564.MAX_CHANNEL_564) |

```
VAR
    uiProcessValue  :   INT;
END_VAR

uiProcessValue := my563.GetProcessValue(1); // here is the process raw value as UINT
```

Get the raw process value of the wanted channel.

In case of error (e.g. an invalid channel number is given) it returns 65535 -> 16#FFFF.

Graphical Illustration

Graphical Interface of FbModule_75x_564_dynConfig.GetRawProcessValue

For get the process value from first channel of the module.

Interface variables Function Get the raw process value of the wanted channel. In case of error (e.g. an invalid channel number is given) it returns 65535 -> 16#FFFF. Graphical Illustration ![Image](images/wagosysmodule_75x_564_1dc65a64.png) Graphical Interface of FbModule_75x_564_dynConfig.GetRawProcessValue Example For get the process value from first channel of the module.

## FbModule_75x_564_dynConfig.SetProcessOutBit (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | ByteNo | UINT | range 0..(_uiOutputSize - 1) |
| BitNo | USINT | range 0..7 |
| OutData | BOOL |  |

## FbModule_75x_564_dynConfig.SetProcessOutByte (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | ByteNo | UINT | range 0..(_uiOutputSize - 1) |
| OutData | BYTE |  |

## FbModule_75x_564_dynConfig.SetProcessOutData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetProcessOutData | UINT |  |
| Input | pOutData | POINTER TO BYTE | pointer to the area with the data to write |
| uiNOutData | UINT | SIZEOF(Buffer) |

## FbModule_75x_564_dynConfig.SetProcessOutDword (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | ByteNo | UINT | range 0..(_uiOutputSize - 4) |
| OutData | DWORD |  |

Graphical Illustration

Graphical Interface of FbModule_75x_564_dynConfig.SetProcessOutDword

Interface variables Function Set the process output dword specified by ByteNo to the value OutData . Graphical Illustration ![Image](images/wagosysmodule_75x_564_0546cd6e.png) Graphical Interface of FbModule_75x_564_dynConfig.SetProcessOutDword

## FbModule_75x_564_dynConfig.SetProcessOutWord (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | ByteNo | UINT | range 0..(_uiOutputSize - 2) |
| OutData | WORD |  |

Graphical Illustration

Graphical Interface of FbModule_75x_564_dynConfig.SetProcessOutWord

Interface variables Function Set the process output word specified by ByteNo to the value OutData . Graphical Illustration ![Image](images/wagosysmodule_75x_564_0832e8a5.png) Graphical Interface of FbModule_75x_564_dynConfig.SetProcessOutWord

## FbModule_75x_564_dynConfig.SetRawProcessValue (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | usiChannel | USINT (1..WagoTypesModule_75x_564.MAX_CHANNEL_564) |
| uiValue | UINT |

```
my564.SetProcessValue(1, 16#1234);
```

Graphical Illustration

Graphical Interface of FbModule_75x_564_dynConfig.SetRawProcessValue

Set the process value 16#1234 to the first channel of the module.

Interface variables Function Set the raw process value Graphical Illustration ![Image](images/wagosysmodule_75x_564_87a26c4e.png) Graphical Interface of FbModule_75x_564_dynConfig.SetRawProcessValue Example Set the process value 16#1234 to the first channel of the module.

### Program Organization


## 20 Program Organization Units


- FbModule_75x_564 (FB) I_Module_75x_564 Channel FbModule_75x_564.GetRawChannelCalibration (METH) - FbModule_75x_564.GetRawChannelScaling (METH) - FbModule_75x_564.GetRawChannelSettings (METH) - FbModule_75x_564.SetRawChannelCalibration (METH) - FbModule_75x_564.SetRawChannelScaling (METH) - FbModule_75x_564.SetRawChannelSettings (METH) FbModule_75x_564.ClearReadFlags (METH) FbModule_75x_564.GetModuleConfiguration (METH) FbModule_75x_564.GetRawChannelConfiguration (METH) FbModule_75x_564.SetModuleConfiguration (METH) FbModule_75x_564.SetRawChannelConfiguration (METH) FbModule_75x_564_dynConfig (FB) - FbModule_75x_564_dynConfig.GetRawProcessValue (METH) - I_ModuleProcessOutputsExtended FbModule_75x_564_dynConfig.GetModuleOutputSize (METH) - FbModule_75x_564_dynConfig.GetProcessOutBit (METH) - FbModule_75x_564_dynConfig.GetProcessOutByte (METH) - FbModule_75x_564_dynConfig.GetProcessOutData (METH) - FbModule_75x_564_dynConfig.GetProcessOutDword (METH) - FbModule_75x_564_dynConfig.GetProcessOutWord (METH) - FbModule_75x_564_dynConfig.SetProcessOutBit (METH) - FbModule_75x_564_dynConfig.SetProcessOutByte (METH) - FbModule_75x_564_dynConfig.SetProcessOutData (METH) - FbModule_75x_564_dynConfig.SetProcessOutDword (METH) - FbModule_75x_564_dynConfig.SetProcessOutWord (METH) FbModule_75x_564_dynConfig.SetRawProcessValue (METH)

### Global Variable Lists


## Error_564 (GVL)


| Scope | Name | Type |
| --- | --- | --- |
| Constant | ERROR_564 | ARRAY [0..5] OF WagoTypesErrorBase.typResultItem |

| Value | Level | Description |
| --- | --- | --- |
| eError_564.OK | WagoTypesErrorBase.eSeverity.none | ‘OK’ |
| eError_564.INVALID_CHANNEL | WagoTypesErrorBase.eSeverity.error | ‘The wanted channel number is not allowed’ |
| eError_564.UNKNOWN_SIGNAL_TYPE | WagoTypesErrorBase.eSeverity.error | ‘Not supported signal type’ |
| eError_564.INVALID_NUMBER_FORMAT | WagoTypesErrorBase.eSeverity.error | ‘Invalid Number Format’ |
| eError_564.INVALID_POWERON_DELAY | WagoTypesErrorBase.eSeverity.error | ‘Invalid Power On Delay’ |
| eError_564.INVALID_WATCHDOG | WagoTypesErrorBase.eSeverity.error | ‘Invalid Action At Kbus Timeout’ |

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 28.11.2019 | 1.0.0.0 | u010663 | First release |

WagoSysModule_75x_564.library

Release Notes:

WagoSysModule_75x_564.library Release Notes:

### Other Components


## 80 Status ¶


- Error_564 (GVL) - eError_564 (ENUM)

## Channel


- FbModule_75x_564.GetRawChannelCalibration (METH) - FbModule_75x_564.GetRawChannelScaling (METH) - FbModule_75x_564.GetRawChannelSettings (METH) - FbModule_75x_564.SetRawChannelCalibration (METH) - FbModule_75x_564.SetRawChannelScaling (METH) - FbModule_75x_564.SetRawChannelSettings (METH)

## I_ModuleProcessOutputsExtended


- FbModule_75x_564_dynConfig.GetModuleOutputSize (METH) - FbModule_75x_564_dynConfig.GetProcessOutBit (METH) - FbModule_75x_564_dynConfig.GetProcessOutByte (METH) - FbModule_75x_564_dynConfig.GetProcessOutData (METH) - FbModule_75x_564_dynConfig.GetProcessOutDword (METH) - FbModule_75x_564_dynConfig.GetProcessOutWord (METH) - FbModule_75x_564_dynConfig.SetProcessOutBit (METH) - FbModule_75x_564_dynConfig.SetProcessOutByte (METH) - FbModule_75x_564_dynConfig.SetProcessOutData (METH) - FbModule_75x_564_dynConfig.SetProcessOutDword (METH) - FbModule_75x_564_dynConfig.SetProcessOutWord (METH)

## I_Module_75x_564


- Channel FbModule_75x_564.GetRawChannelCalibration (METH) - FbModule_75x_564.GetRawChannelScaling (METH) - FbModule_75x_564.GetRawChannelSettings (METH) - FbModule_75x_564.SetRawChannelCalibration (METH) - FbModule_75x_564.SetRawChannelScaling (METH) - FbModule_75x_564.SetRawChannelSettings (METH) FbModule_75x_564.ClearReadFlags (METH) FbModule_75x_564.GetModuleConfiguration (METH) FbModule_75x_564.GetRawChannelConfiguration (METH) FbModule_75x_564.SetModuleConfiguration (METH) FbModule_75x_564.SetRawChannelConfiguration (METH)

## eError_564 (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| OK | 0 | all is well |
| INVALID_CHANNEL | 1 | invalid channel number |
| UNKNOWN_SIGNAL_TYPE | 2 |  |
| INVALID_NUMBER_FORMAT | 3 |  |
| INVALID_POWERON_DELAY | 4 |  |
| INVALID_WATCHDOG | 5 |  |