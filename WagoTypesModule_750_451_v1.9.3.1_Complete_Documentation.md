# WagoTypesModule_750_451 v1.9.3.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesModule_750_451
- **Version:** 1.9.3.1
- **Categories:** WAGO Internal|Common|Types and Interfaces
- **Author:** WAGO
- **Placeholder:** WagoTypesModule_750_451

### Description ¶


This document is automatically generated.

Handling modules 750-451

This document is automatically generated. Handling modules 750-451

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Methods I_Module_750_451.GetModuleSettings (METH) - I_Module_750_451.GetRawChannelCalibration (METH) - I_Module_750_451.GetRawChannelConfiguration (METH) - I_Module_750_451.GetRawChannelScaling (METH) - I_Module_750_451.GetRawChannelSettings (METH) - I_Module_750_451.GetScaledChannelConfiguration (METH) - I_Module_750_451.SetModuleSettings (METH) - I_Module_750_451.SetRawChannelCalibration (METH) - I_Module_750_451.SetRawChannelConfiguration (METH) - I_Module_750_451.SetRawChannelScaling (METH) - ... and 9 more Interfaces - I_Module_750_451 (ITF) - I_Module_750_451_dynConfig (ITF) Program Organization Global Variable Lists - Channels_451 (GVL) - VersionHistory (GVL) Other Components - 10 Enumeration - 15 Datatypes - Channel - Configuration - Module - ProcessValues - Raw - Scaled - eNotchFilter (ENUM) - eSensorType (ENUM) - ... and 6 more

### Indices and tables ¶


Based on WagoTypesModule_750_451.library, last modified 20.09.2024, 21:23:03. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesModule_750_451.library, last modified 20.09.2024, 21:23:03. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesModule_750_451 Library Documentation


| Company: | WAGO |
| Title: | WagoTypesModule_750_451 |
| Version: | 1.9.3.1 |
| Categories: | WAGO Internal\|Common\|Types and Interfaces |
| Author: | WAGO |
| Placeholder: | WagoTypesModule_750_451 |

### Description


This document is automatically generated.

Handling modules 750-451

This document is automatically generated. Handling modules 750-451

### Contents:


- 20 Program Organization Units 10 Enumeration - 15 Datatypes - Channels_451 (GVL) - I_Module_750_451 (ITF) - I_Module_750_451_dynConfig (ITF) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesModule_750_451.library, last modified 20.09.2024, 21:23:03. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesModule_750_451.library, last modified 20.09.2024, 21:23:03. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesModule_750_451.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 20.09.2024, 21:23:03 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 20.09.2024, 21:23:03 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesModule_750_451 |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesModule_750_451 |
| Version | version | 1.9.3.1 |
| Version string | string |  |
| Title | WagoTypesModule_750_451 |
| LibraryCategories | library-category-list | WAGO Internal\|Common\|Types and Interfaces |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_SIZE = 18

### Methods


## I_Module_750_451.GetModuleSettings (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetModuleSettings | WagoTypesModuleBase.eServiceState |  |
| Inout | xTrigger | BOOL | set this variable once to start the process. It will be reset by the Method automatic. |
| utModuleSettings | typModuleSettings |  |
| Output | xError | BOOL |  |
| oError | WagoSysErrorBase.FbResult |  |

| Struct member | Value | Description |
| --- | --- | --- |
| xAmountSignFormat | FALSE | Numeric values appear in two’s complement |
| TRUE | Numeric values appear in amount / sign format |
| xS5FB250Format | FALSE | Numeric values appear in standard format |
| TRUE | Numeric values appear in S5-FB250 format |
| xDisableWatchdog | FALSE | The Watchdog timer is enabled |
| TRUE | The Watchdog timer is not enabled. The Satus LEDs light up continuously |
| eNotchFilter | DISABLED_100HZ | The Notch filter is not enabled (100 Hz) |
| ENABLED_50HZ | Notch filter ( 50 Hz ) |
| ENABLED_60HZ | Notch filter ( 60 Hz ) |
| ENABLED_50_60HZ | Notch filter ( 50/60 Hz ) |

```
VAR
    //--- Module Mode Settings ------------------------------
    utModuleSettings    :   WagoTypesModule_750_451.typModuleSettings;
    xGetModuleSettings  :   BOOL; // set this variable once to start the process. It will be reset by the Method automatic.
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- M O D U L E    S E T T I N G S -----------------------
CASE my451.GetModuleSettings(xGetModuleSettings, utModuleSettings, oError => oError) OF

    eServiceState.DONE : // OK
            ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

Get the common settings of the module at a struct.

Graphical Illustration

Graphical Interface of I_Module_750_451.GetModuleSettings

For get the settings from the module.

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the common settings of the module at a struct. Graphical Illustration ![Image](images/wagotypesmodule_750_451_5db2ce89.png) Graphical Interface of I_Module_750_451.GetModuleSettings Example For get the settings from the module. Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_451.GetRawChannelCalibration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelCalibration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |
| Inout | xTrigger | BOOL |
| utRawChannelCalibration | typRawChannelCalibration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserCalibration | FALSE | The user scaling is switched off |
| TRUE | The user scaling is switched on |
| iUserCalibrationOffset |  |
| uiUserCalibrationGain |  |

```
VAR
    //--- Channel Calibration ---------------------------------
    utChannelCalibration    :   WagoTypesModule_750_451.typRawChannelCalibration;;
    xGetChannelCalibration  :   BOOL;
    oError                  :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L    C A L I B R A T I O N -----------------------
CASE my451.GetRawChannelCalibration(    usiChannel              := 1,
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

Graphical Interface of I_Module_750_451.GetRawChannelCalibration

For get the calibration from channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the calibration of a channel at a struct. typRawChannelCalibration Graphical Illustration ![Image](images/wagotypesmodule_750_451_a818184f.png) Graphical Interface of I_Module_750_451.GetRawChannelCalibration Example For get the calibration from channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_451.GetRawChannelConfiguration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelConfiguration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |
| Inout | xTrigger | BOOL |
| utRawChannelConfiguration | typRawChannelConfiguration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

Graphical Illustration

Graphical Interface of I_Module_750_451.GetRawChannelConfiguration

Interface variables Function Get the complete raw configuration of a channel. Graphical Illustration ![Image](images/wagotypesmodule_750_451_c2440483.png) Graphical Interface of I_Module_750_451.GetRawChannelConfiguration Example

## I_Module_750_451.GetRawChannelScaling (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelScaling | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |
| Inout | xTrigger | BOOL |
| utRawChannelScaling | typRawChannelScaling |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserScaling | FALSE | User scaling disabled -> use manufacturer scaling |
| TRUE | User scaling enabled |
| iUserScalingOffset | -32768 ... 32767 | User scaling Offset |
| uiUserScalingGain | 0 ... 65535 | User scaling Gain |
| uiUserScalingDivisor | 0 ... 65535 | User scaling Divisor default = 256 -> (read only) |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelScaling    :   WagoTypesModule_750_451.typRawChannelScaling;;
    xGetChannelScaling  :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S C A L I N G ------------------------
CASE my451.GetRawChannelScaling(    usiChannel           := 1,
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

Graphical Interface of I_Module_750_451.GetRawChannelScaling

For get the scaling from channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the scaling of a channel at a struct. typRawChannelScaling Graphical Illustration ![Image](images/wagotypesmodule_750_451_18527b69.png) Graphical Interface of I_Module_750_451.GetRawChannelScaling Example For get the scaling from channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_451.GetRawChannelSettings (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelSettings | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |
| Inout | xTrigger | BOOL |
| utRawChannelSettings | typRawChannelSettings |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| eSensorType | Pt100_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Ni100_DIN43760 | DIN 43760 | -60 °C...250 °C | Resolution 0.1 °C |
| Pt1000_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Pt500_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Pt200_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Ni1000_TK6180 | DIN 43760 | -60 °C...250 °C | Resolution 0.1 °C |
| Ni120_MINCO | Minco | -80 °C...260 °C | Resolution 0.1 °C |
| Ni1000_TK5000 | TK 5000 | -60 °C...250 °C | Resolution 0.1 °C |
| Ni1000_TK6180_01 | DIN 43760 | -50 °C...150 °C | Resolution 0.01 °C |
| Ni1000_TK5000_01 | TK 5000 | -50 °C...150 °C | Resolution 0.01 °C |
| Pt1000_EN60751_01 | IEC 751 | -50 °C...150 °C | Resolution 0.01 °C |
| Resistor_1 |  | 0 Ω...5 kΩ | Resolution 0.2 Ω |
| Resistor_2 |  | 0 Ω...1.2 kΩ | Resolution 0.02 Ω |
| xEnableDiagGlobal | FALSE | Diagnostis global functions disabled |
| TRUE | Diagnostis global functions enabled |
| xEnableDiagWireBreak | FALSE | Diagnostis wire break disabled |
| TRUE | Diagnostis wire break enabled |
| xEnableDiagShortCircuit | FALSE | Diagnostis short circuit disabled |
| TRUE | Diagnostis short circuit enabled |
| xEnableDiagCommonError | FALSE | Diagnostis Group error disabled |
| TRUE | Diagnostis Group error enabled |
| xEnableDiagOverflow | FALSE | Diagnostis overrange disabled |
| TRUE | Diagnostis overrange enabled |
| xEnableDiagUnderflow | FALSE | Diagnostis underrange disabled |
| TRUE | Diagnostis underrange enabled |
| xEnable2Wire | FALSE | Channel disabled |
| TRUE | 2-wire |
| uiLineResistance | 0 ... 65535 | Line resistance [Ohm] |
| iUpperUserLimitValue | -32768 ... 32767 | Upper user limit value |
| xEnableDiagLimitOverflow | FALSE | Diagnostis user limiting value overrange disabled |
| TRUE | Diagnostis user limiting value overrange enabled |
| iLowerUserLimitValue | -32768 ... 32767 | Lower user limit value |
| xEnableDiagLimitUnderflow | FALSE | Diagnostis user limiting value underrange disabled |
| TRUE | Diagnostis user limiting value underrange enabled |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelSettings   :   WagoTypesModule_750_451.typRawChannelSettings;;
    xGetChannelSettings :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S E T T I N G S ----------------------
CASE my451.GetRawChannelSettings(   usiChannel           := 1,
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

Graphical Interface of I_Module_750_451.GetRawChannelSettings

For get the settings from channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the settings of a channel at a struct. typRawChannelSettings Graphical Illustration ![Image](images/wagotypesmodule_750_451_8ab1dc13.png) Graphical Interface of I_Module_750_451.GetRawChannelSettings Example For get the settings from channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_451.GetScaledChannelConfiguration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetScaledChannelConfiguration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |
| Inout | xTrigger | BOOL |
| utScaledChannelConfiguration | typScaledChannelConfiguration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

Graphical Illustration

Graphical Interface of I_Module_750_451.GetScaledChannelConfiguration

Interface variables Function Get the complete configuration of a channel. Graphical Illustration ![Image](images/wagotypesmodule_750_451_7663f733.png) Graphical Interface of I_Module_750_451.GetScaledChannelConfiguration Example

## I_Module_750_451.SetModuleSettings (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetModuleSettings | WagoTypesModuleBase.eServiceState |  |
| Inout | xTrigger | BOOL | set this variable once to start the process. It will be automatic reset by this Method. |
| utModuleSettings | typModuleSettings |  |
| Output | xError | BOOL |  |
| oError | WagoSysErrorBase.FbResult |  |

| Struct member | Value | Description |
| --- | --- | --- |
| xAmountSignFormat | FALSE | Numeric values appear in two’s complement |
| TRUE | Numeric values appear in amount / sign format |
| xS5FB250Format | FALSE | Numeric values appear in standard format |
| TRUE | Numeric values appear in S5-FB250 format |
| xDisableWatchdog | FALSE | The Watchdog timer is enabled |
| TRUE | The Watchdog timer is not enabled. The Satus LEDs light up continuously |
| eNotchFilter | DISABLED_100HZ | The Notch filter is not enabled (100 Hz) |
| ENABLED_50HZ | Notch filter ( 50 Hz ) |
| ENABLED_60HZ | Notch filter ( 60 Hz ) |
| ENABLED_50_60HZ | Notch filter ( 50/60 Hz ) |

```
VAR
    //--- Module Mode Settings ------------------------------
    utModuleSettings    :   WagoTypesModule_750_451.typModuleSettings;
    xSetModuleSettings  :   BOOL; // set this variable once to start the process. It will be reset by the Method automatic.
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- S E T   M O D U L E    S E T T I N G S ---------------
CASE my451.SetSettingsModuleMode(xSetModuleSettings, utModuleSettings, oError => oError) OF

    eServiceState.DONE : // OK

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

Set the common settings of the module from a struct.

Graphical Illustration

Graphical Interface of I_Module_750_451.SetModuleSettings

For set the settings from the module.

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the common settings of the module from a struct. Graphical Illustration ![Image](images/wagotypesmodule_750_451_db2c4648.png) Graphical Interface of I_Module_750_451.SetModuleSettings Example For set the settings from the module. Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_451.SetRawChannelCalibration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelCalibration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |
| Inout | xTrigger | BOOL |
| utRawChannelCalibration | typRawChannelCalibration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserCalibration | FALSE | The user scaling is switched off |
| TRUE | The user scaling is switched on |
| iUserCalibrationOffset |  |
| uiUserCalibrationGain |  |

```
VAR
    //--- Channel Calibration ---------------------------------
    utChannelCalibration    :   WagoTypesModule_750_451.typRawChannelCalibration;;
    xSetChannelCalibration  :   BOOL;
    oError                  :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L    C A L I B R A T I O N -----------------------
CASE my451.SetRawChannelCalibration(    usiChannel              := 1,
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

Set the calibration of a channel by a struct.

Graphical Illustration

Graphical Interface of I_Module_750_451.SetRawChannelCalibration

For set the calibration of channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the calibration of a channel by a struct. Graphical Illustration ![Image](images/wagotypesmodule_750_451_f61ea021.png) Graphical Interface of I_Module_750_451.SetRawChannelCalibration Example For set the calibration of channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_451.SetRawChannelConfiguration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelConfiguration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |
| Inout | xTrigger | BOOL |
| utRawChannelConfiguration | typRawChannelConfiguration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

Graphical Illustration

Graphical Interface of I_Module_750_451.SetRawChannelConfiguration

Interface variables Function Set the complete raw configuration of a channel. Graphical Illustration ![Image](images/wagotypesmodule_750_451_abd4a7ba.png) Graphical Interface of I_Module_750_451.SetRawChannelConfiguration Example

## I_Module_750_451.SetRawChannelScaling (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelScaling | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |
| Inout | xTrigger | BOOL |
| utRawChannelScaling | typRawChannelScaling |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserScaling | FALSE | User scaling disabled -> use manufacturer scaling |
| TRUE | User scaling enabled |
| iUserScalingOffset | -32768 ... 32767 | User scaling Offset |
| uiUserScalingGain | 0 ... 65535 | User scaling Gain |
| uiUserScalingDivisor | 0 ... 65535 | User scaling Divisor default = 256 -> (read only) |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelScaling    :   WagoTypesModule_750_451.typRawChannelScaling;;
    xSetChannelScaling  :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S C A L I N G ------------------------
CASE my451.SetRawChannelScaling(    usiChannel          := 1,
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

Graphical Interface of I_Module_750_451.SetRawChannelScaling

For set the scaling of channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the scaling of a channel by a struct. typRawChannelScaling Graphical Illustration ![Image](images/wagotypesmodule_750_451_dd0316d2.png) Graphical Interface of I_Module_750_451.SetRawChannelScaling Example For set the scaling of channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_451.SetRawChannelSettings (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelSettings | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |
| Inout | xTrigger | BOOL |
| utRawChannelSettings | typRawChannelSettings |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| eSensorType | Pt100_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Ni100_DIN43760 | DIN 43760 | -60 °C...250 °C | Resolution 0.1 °C |
| Pt1000_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Pt500_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Pt200_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Ni1000_TK6180 | DIN 43760 | -60 °C...250 °C | Resolution 0.1 °C |
| Ni120_MINCO | Minco | -80 °C...260 °C | Resolution 0.1 °C |
| Ni1000_TK5000 | TK 5000 | -60 °C...250 °C | Resolution 0.1 °C |
| Ni1000_TK6180_01 | DIN 43760 | -50 °C...150 °C | Resolution 0.01 °C |
| Ni1000_TK5000_01 | TK 5000 | -50 °C...150 °C | Resolution 0.01 °C |
| Pt1000_EN60751_01 | IEC 751 | -50 °C...150 °C | Resolution 0.01 °C |
| Resistor_1 |  | 0 Ω...5 kΩ | Resolution 0.2 Ω |
| Resistor_2 |  | 0 Ω...1.2 kΩ | Resolution 0.02 Ω |
| xEnableDiagGlobal | FALSE | Diagnostis global functions disabled |
| TRUE | Diagnostis global functions enabled |
| xEnableDiagWireBreak | FALSE | Diagnostis wire break disabled |
| TRUE | Diagnostis wire break enabled |
| xEnableDiagShortCircuit | FALSE | Diagnostis short circuit disabled |
| TRUE | Diagnostis short circuit enabled |
| xEnableDiagCommonError | FALSE | Diagnostis Group error disabled |
| TRUE | Diagnostis Group error enabled |
| xEnableDiagOverflow | FALSE | Diagnostis overrange disabled |
| TRUE | Diagnostis overrange enabled |
| xEnableDiagUnderflow | FALSE | Diagnostis underrange disabled |
| TRUE | Diagnostis underrange enabled |
| xEnable2Wire | FALSE | Channel disabled |
| TRUE | 2-wire |
| uiLineResistance | 0 ... 65535 | Line resistance [Ohm] |
| iUpperUserLimitValue | -32768 ... 32767 | Upper user limit value |
| xEnableDiagLimitOverflow | FALSE | Diagnostis user limiting value overrange disabled |
| TRUE | Diagnostis user limiting value overrange enabled |
| iLowerUserLimitValue | -32768 ... 32767 | Lower user limit value |
| xEnableDiagLimitUnderflow | FALSE | Diagnostis user limiting value underrange disabled |
| TRUE | Diagnostis user limiting value underrange enabled |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelSettings   :   WagoTypesModule_750_451.typRawChannelSettings;;
    xSetChannelSettings :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S E T T I N G S ----------------------
CASE my451.SetRawChannelSettings(   usiChannel           := 1,
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

Graphical Interface of I_Module_750_451.SetRawChannelSettings

For set the settings of channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the settings for a channel by a struct. typRawChannelSettings Graphical Illustration ![Image](images/wagotypesmodule_750_451_0b66a595.png) Graphical Interface of I_Module_750_451.SetRawChannelSettings Example For set the settings of channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_451.SetScaledChannelConfiguration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetScaledChannelConfiguration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |
| Inout | xTrigger | BOOL |
| utScaledChannelConfiguration | typScaledChannelConfiguration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

Graphical Illustration

Graphical Interface of I_Module_750_451.SetScaledChannelConfiguration

Interface variables Function Set the complete configuration of a channel. Graphical Illustration ![Image](images/wagotypesmodule_750_451_b0008bd5.png) Graphical Interface of I_Module_750_451.SetScaledChannelConfiguration Example

## I_Module_750_451_dynConfig.GetDiagnosis (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetDiagnosis | BYTE |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |

| Bit | Value | Description |
| --- | --- | --- |
| 0 | TRUE | short circuit or broken wire |
| 1 | TRUE | overflow or underflow |
| 2 |  | not used |
| 3 |  | not used |
| 4 |  | not used |
| 5 |  | not used |
| 6 | TRUE | diagnostic not available -> xS5FB250Format not set |
| 7 | TRUE | invalid channel |

```
VAR
    bDiagnostic :   BYTE;
END_VAR

bDiagnostic := my451.GetDiagnosis(1); // here is the diagnostic byte
```

To work with this method the module mode setting xS5FB250Format must be set to TRUE. In other cases there is no access to module diagnosis at this time.

xS5FB250Format must be set ...

Graphical Illustration

Graphical Interface of I_Module_750_451_dynConfig.GetDiagnosis

Interface variables Function To work with this method the module mode setting xS5FB250Format must be set to TRUE. In other cases there is no access to module diagnosis at this time. Note xS5FB250Format must be set ... Graphical Illustration ![Image](images/wagotypesmodule_750_451_72c93489.png) Graphical Interface of I_Module_750_451_dynConfig.GetDiagnosis Example For get the diagnostic byte from first channel of the module.

## I_Module_750_451_dynConfig.GetRawProcessValue (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawProcessValue | INT |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |

```
VAR
    myiProcessValue :   INT;
END_VAR

myiProcessValue := my451.GetProcessValue(1); // here is the process raw value as INT
```

Get the raw process value of the wanted channel. The return value is unscaled in the range -32768 .. 37767.

In case of error (e.g. an invalid channel number is given) it returns 0.

Graphical Illustration

Graphical Interface of I_Module_750_451_dynConfig.GetRawProcessValue

Interface variables Function Get the raw process value of the wanted channel. The return value is unscaled in the range -32768 .. 37767. In case of error (e.g. an invalid channel number is given) it returns 0. Graphical Illustration ![Image](images/wagotypesmodule_750_451_71966858.png) Graphical Interface of I_Module_750_451_dynConfig.GetRawProcessValue Example For get the process value from first channel of the module.

## I_Module_750_451_dynConfig.GetScaledProcessValue (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetScaledProcessValue | REAL |
| Input | usiChannel | USINT (1..MAX_CHANNEL_451) |

```
VAR
    mydiProcessValue    :   DINT;
END_VAR

mydiProcessValue := my451.GetProcessValue(1); // here is the process value
```

Graphical Illustration

Graphical Interface of I_Module_750_451_dynConfig.GetScaledProcessValue

Interface variables Function Get the scaled process value of the wanted channel. The range of the value depends on the configured sensortype. Graphical Illustration ![Image](images/wagotypesmodule_750_451_90275fc2.png) Graphical Interface of I_Module_750_451_dynConfig.GetScaledProcessValue Example For get the process value from first channel of the module.

## typModuleSettings (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| xAmountSignFormat | BOOL | Number notation -> 2-complement / amount-sign (Bit 0) |
| xS5FB250Format | BOOL | S5-Format -> Standard / S5-FB250 format (Bit 1) |
| xDisableWatchdog | BOOL | Watchdog internal data bus -> enable / disable (Bit 2) |
| eNotchFilter | eNotchFilter | (BIT 3..4) |

| Struct member | Value | Description |
| --- | --- | --- |
| xAmountSignFormat | FALSE | Numeric values appear in two’s complement |
| TRUE | Numeric values appear in amount / sign format |
| xS5FB250Format | FALSE | Numeric values appear in standard format |
| TRUE | Numeric values appear in S5-FB250 format |
| xDisableWatchdog | FALSE | The Watchdog timer is enabled |
| TRUE | The Watchdog timer is not enabled. The Satus LEDs light up continuously |
| eNotchFilter | DISABLED_100HZ | The Notch filter is not enabled (100 Hz) |
| ENABLED_50HZ | Notch filter ( 50 Hz ) |
| ENABLED_60HZ | Notch filter ( 60 Hz ) |
| ENABLED_50_60HZ | Notch filter ( 50/60 Hz ) |

## typRawChannelSettings (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| eSensorType | eSensorType | Bit 0..3 (Reg 35) |
| xEnableDiagGlobal | BOOL | Bit 15 (Reg 35) |
| xEnableDiagWireBreak | BOOL | Bit 13 (Reg 35) |
| xEnableDiagShortCircuit | BOOL | Bit 12 (Reg 35) |
| xEnableDiagCommonError | BOOL | Bit 14 (Reg 35) |
| xEnableDiagOverflow | BOOL | Bit 9 |
| xEnableDiagUnderflow | BOOL | Bit 8 |
| xEnable2Wire | BOOL | Bit 4 (Reg 35) |
| iUpperUserLimitValue | INT | (Reg 43) |
| xEnableDiagLimitOverflow | BOOL | Bit 11 (Reg 35) |
| iLowerUserLimitValue | INT | (Reg 42) |
| xEnableDiagLimitUnderflow | BOOL | Bit 10 (Reg 35) |

## typReg35Settings (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| eSensorType | eSensorType | Bit 0..3 |
| xEnable2Wire | BOOL | Bit 4 |
| xUserCalibration | BOOL | Bit 6 * |
| xUserScaling | BOOL | Bit 7 * |
| xEnableDiagUnderflow | BOOL | Bit 8 |
| xEnableDiagOverflow | BOOL | Bit 9 |
| xEnableDiagLimitUnderflow | BOOL | Bit 10 |
| xEnableDiagLimitOverflow | BOOL | Bit 11 |
| xEnableDiagShortCircuit | BOOL | Bit 12 |
| xEnableDiagWireBreak | BOOL | Bit 13 |
| xEnableDiagCommonError | BOOL | Bit 14 |
| xEnableDiagGlobal | BOOL | Bit 15 |

## typScaledChannelSettings (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| eSensorType | eSensorType | (Reg 35.0..3) |
| xEnableDiagGlobal | BOOL | (Reg 35.15) |
| xEnableDiagWireBreak | BOOL | (Reg 35.13) |
| xEnableDiagShortCircuit | BOOL | (Reg 35.12) |
| xEnableDiagCommonError | BOOL | (Reg 35.14) |
| xEnableDiagOverflow | BOOL | (Reg 35.9) |
| xEnableDiagUnderflow | BOOL | (Reg 35.8) |
| xEnable2Wire | BOOL | (Reg 35.4) |
| rUpperUserLimitValue | REAL | (Reg 43) range depends on the selected sensor type |
| xEnableDiagLimitOverflow | BOOL | (Reg 35.11) |
| rLowerUserLimitValue | REAL | (Reg 42) range depends on the selected sensor type |
| xEnableDiagLimitUnderflow | BOOL | (Reg 35.10) |

### Interfaces


## I_Module_750_451 (ITF)


- Channel I_Module_750_451.GetRawChannelCalibration (METH) - I_Module_750_451.GetRawChannelScaling (METH) - I_Module_750_451.GetRawChannelSettings (METH) - I_Module_750_451.SetRawChannelCalibration (METH) - I_Module_750_451.SetRawChannelScaling (METH) - I_Module_750_451.SetRawChannelSettings (METH) Configuration - I_Module_750_451.GetRawChannelConfiguration (METH) - I_Module_750_451.GetScaledChannelConfiguration (METH) - I_Module_750_451.SetRawChannelConfiguration (METH) - I_Module_750_451.SetScaledChannelConfiguration (METH) Module - I_Module_750_451.GetModuleSettings (METH) - I_Module_750_451.SetModuleSettings (METH)

## I_Module_750_451_dynConfig (ITF)


- ProcessValues I_Module_750_451_dynConfig.GetDiagnosis (METH) - I_Module_750_451_dynConfig.GetRawProcessValue (METH) - I_Module_750_451_dynConfig.GetScaledProcessValue (METH)

### Program Organization


## 20 Program Organization Units


- 10 Enumeration eNotchFilter (ENUM) - eSensorType (ENUM) 15 Datatypes - Raw typRawChannelCalibration (STRUCT) - typRawChannelScaling (STRUCT) - typRawChannelSettings (STRUCT) - typReg35Settings (STRUCT) Scaled - typScaledChannelCalibration (STRUCT) - typScaledChannelScaling (STRUCT) - typScaledChannelSettings (STRUCT) typModuleSettings (STRUCT) typRawChannelConfiguration (STRUCT) typScaledChannelConfiguration (STRUCT) Channels_451 (GVL) I_Module_750_451 (ITF) - Channel I_Module_750_451.GetRawChannelCalibration (METH) - I_Module_750_451.GetRawChannelScaling (METH) - I_Module_750_451.GetRawChannelSettings (METH) - I_Module_750_451.SetRawChannelCalibration (METH) - I_Module_750_451.SetRawChannelScaling (METH) - I_Module_750_451.SetRawChannelSettings (METH) Configuration - I_Module_750_451.GetRawChannelConfiguration (METH) - I_Module_750_451.GetScaledChannelConfiguration (METH) - I_Module_750_451.SetRawChannelConfiguration (METH) - I_Module_750_451.SetScaledChannelConfiguration (METH) Module - I_Module_750_451.GetModuleSettings (METH) - I_Module_750_451.SetModuleSettings (METH) I_Module_750_451_dynConfig (ITF) - ProcessValues I_Module_750_451_dynConfig.GetDiagnosis (METH) - I_Module_750_451_dynConfig.GetRawProcessValue (METH) - I_Module_750_451_dynConfig.GetScaledProcessValue (METH)

### Global Variable Lists


## Channels_451 (GVL)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | MAX_CHANNEL_451 | USINT | 8 | max. channels for 750-451 |

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 28.08.2024 | 1.9.3.1 | u0103719 | WAT36092: add missing sensor PT100_EN60751 (context: sensor type) |
| 16.07.2019 | 1.9.3.0 | u010545 | Interface for dyn config added |
| 08.01.2019 | 1.9.1.0 | u015842 | Properties: free placeholder added |
| 11.10.2017 | 1.9.0.2 | u010545 | unifications |
| 09.10.2017 | 1.9.0.1 | u010545 | channel quantity modified |
| 21.07.2017 | 1.8.0.0 | u010545 | new concept for configuration and mapping |
| 31.05.2017 | 1.7.0.0 | u010545 | First release |
| 30.05.2017 | 0.0.0.2 | u010545 | Interfaces modyfied |
| 04.05.2017 | 0.0.0.1 | u010545 | init |

WagoTypesModule_750_451.library

Release Notes:

WagoTypesModule_750_451.library Release Notes:

### Other Components


## 10 Enumeration


- eNotchFilter (ENUM) - eSensorType (ENUM)

## 15 Datatypes


- Raw typRawChannelCalibration (STRUCT) - typRawChannelScaling (STRUCT) - typRawChannelSettings (STRUCT) - typReg35Settings (STRUCT) Scaled - typScaledChannelCalibration (STRUCT) - typScaledChannelScaling (STRUCT) - typScaledChannelSettings (STRUCT) typModuleSettings (STRUCT) typRawChannelConfiguration (STRUCT) typScaledChannelConfiguration (STRUCT)

## Channel


- I_Module_750_451.GetRawChannelCalibration (METH) - I_Module_750_451.GetRawChannelScaling (METH) - I_Module_750_451.GetRawChannelSettings (METH) - I_Module_750_451.SetRawChannelCalibration (METH) - I_Module_750_451.SetRawChannelScaling (METH) - I_Module_750_451.SetRawChannelSettings (METH)

## Configuration


- I_Module_750_451.GetRawChannelConfiguration (METH) - I_Module_750_451.GetScaledChannelConfiguration (METH) - I_Module_750_451.SetRawChannelConfiguration (METH) - I_Module_750_451.SetScaledChannelConfiguration (METH)

## Module


- I_Module_750_451.GetModuleSettings (METH) - I_Module_750_451.SetModuleSettings (METH)

## ProcessValues


- I_Module_750_451_dynConfig.GetDiagnosis (METH) - I_Module_750_451_dynConfig.GetRawProcessValue (METH) - I_Module_750_451_dynConfig.GetScaledProcessValue (METH)

## Raw


- typRawChannelCalibration (STRUCT) - typRawChannelScaling (STRUCT) - typRawChannelSettings (STRUCT) - typReg35Settings (STRUCT)

## Scaled


- typScaledChannelCalibration (STRUCT) - typScaledChannelScaling (STRUCT) - typScaledChannelSettings (STRUCT)

## eNotchFilter (ENUM)


| Name | Initial |
| --- | --- |
| DISABLED_100HZ | 0 |
| ENABLED_50HZ | 1 |
| ENABLED_60HZ | 2 |
| ENABLED_50_60HZ | 3 |

Attributes: qualified_only InOut:

## eSensorType (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Pt100_EN60751 | 0 | EN 60751 -> -200°C ... 850°C -> resolution 0.1°C |
| Ni100_DIN43760 | 1 | DIN 43760 -> - 60°C ... 250°C -> resolution 0.1°C |
| Pt1000_EN60751 | 2 | EN 60751 -> -200°C ... 850°C -> resolution 0.1°C |
| Pt500_EN60751 | 3 | EN 60751 -> -200°C ... 850°C -> resolution 0.1°C |
| Pt200_EN60751 | 4 | EN 60751 -> -200°C ... 850°C -> resolution 0.1°C |
| Ni1000_TK6180 | 5 | TK 6180 / DIN 43760 -> - 60°C ... 250°C -> resolution 0.1°C |
| Ni120_MINCO | 6 | Minco -> - 80°C ... 260°C -> resolution 0.1°C |
| Ni1000_TK5000 | 7 | TK 5000 (Landis+Staefa) -> - 60°C ... 250°C -> resolution 0.1°C |
| Ni1000_TK6180_01 | 8 | TK 6180 / DIN 43760 -> - 50°C ... 150°C -> resolution 0.01°C |
| Ni1000_TK5000_01 | 9 | TK 5000 (Landis+Staefa) -> - 50°C ... 150°C -> resolution 0.01°C |
| Pt1000_EN60751_01 | 10 | EN 60751 -> - 50°C ... 150°C -> resolution 0.01°C |
| Pt100_EN60751_01 | 11 | EN 60751 -> - 50 °C ... 150 °C -> resolution 0.01 °C |
| Resistor_1 | 14 | Resistor -> 0 Ohm ... 5.0 kOhm -> resolution 0.2 Ohm |
| Resistor_2 | 15 | Resistor -> 0 Ohm ... 1.2 kOhm -> resolution 0.05 Ohm |

| Name | Initial | Sensor type | Standard | Measuring range | Resolution |
| --- | --- | --- | --- | --- | --- |
| Pt100_EN60751 | 0 | Pt100 | EN 60751 | -200°C ... 850°C | 0.1°C |
| Ni100_DIN43760 | 1 | Ni100 | DIN 43760 | -60°C ... 250°C | 0.1°C |
| Pt1000_EN60751 | 2 | Pt1000 | EN 60751 | -200°C ... 850°C | 0.1°C |
| Pt500_EN60751 | 3 | Pt500 | EN 60751 | -200°C ... 850°C | 0.1°C |
| Pt200_EN60751 | 4 | Pt200 | EN 60751 | -200°C ... 850°C | 0.1°C |
| Ni1000_TK6180 | 5 | Ni1000 | TK 6180 / DIN 43760 | -60°C ... 250°C | 0.1°C |
| Ni120_MINCO | 6 | Ni120 | Minco | -80°C ... 260°C | 0.1°C |
| Ni1000_TK5000 | 7 | Ni1000 | TK 5000 (Landis+Staefa) | -60°C ... 250°C | 0.1°C |
| Ni1000_TK6180_01 | 8 | Ni1000 | TK 6180 / DIN 43760 -> | -50°C ... 150°C | 0.01°C |
| Ni1000_TK5000_01 | 9 | Ni1000 | TK 5000 (Landis+Staefa) | -50°C ... 150°C | 0.01°C |
| Pt1000_EN60751_01 | 10 | Pt1000 | EN 60751 | -50°C ... 150°C | 0.01°C |
| Pt100_EN60751_01 | 11 | Pt100 | EN 60751 | -50 °C ... 150 °C | 0.01 °C |
| Resistor_1 | 14 | Resistor |  | 0 Ohm ... 5.0 kOhm | 0.2 Ohm |
| Resistor_2 | 15 | Resistor |  | 0 Ohm ... 1.2 kOhm | 0.05 Ohm |

Attributes: qualified_only InOut:

## typRawChannelCalibration (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| xUserCalibration | BOOL | Bit 6 * (Reg 35) |
| uiUserCalibrationGain | UINT | (Reg 38) Anzeige 0 .. 1,9999 |
| iUserCalibrationOffset | INT | (Reg 37) |

## typRawChannelConfiguration (STRUCT)


| Name | Type |
| --- | --- |
| Settings | typRawChannelSettings |
| Scaling | typRawChannelScaling |
| Calibration | typRawChannelCalibration |

| Struct member | Value | Description |
| --- | --- | --- |
| Settings | eSensorType | Pt100_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Ni100_DIN43760 | DIN 43760 | -60 °C...250 °C | Resolution 0.1 °C |
| Pt1000_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Pt500_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Pt200_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Ni1000_TK6180 | DIN 43760 | -60 °C...250 °C | Resolution 0.1 °C |
| Ni120_MINCO | Minco | -80 °C...260 °C | Resolution 0.1 °C |
| Ni1000_TK5000 | TK 5000 | -60 °C...250 °C | Resolution 0.1 °C |
| Ni1000_TK6180_01 | DIN 43760 | -50 °C...150 °C | Resolution 0.01 °C |
| Ni1000_TK5000_01 | TK 5000 | -50 °C...150 °C | Resolution 0.01 °C |
| Pt1000_EN60751_01 | IEC 751 | -50 °C...150 °C | Resolution 0.01 °C |
| Resistor_1 |  | 0 Ohm...5 kOhm | Resolution 0.2 Ohm |
| Resistor_2 | \| 0 Ohm...1.2 kOhm \| Resolution 0.02 Ohm |
| xEnableDiagGlobal | FALSE | Diagnostis global functions disabled |
| TRUE | Diagnostis global functions enabled |
| xEnableDiagWireBreak | FALSE | Diagnostis wire break disabled |
| TRUE | Diagnostis wire break enabled |
| xEnableDiagShortCircuit | FALSE | Diagnostis short circuit disabled |
| TRUE | Diagnostis short circuit enabled |
| xEnableDiagCommonError | FALSE | Diagnostis Group error disabled |
| TRUE | Diagnostis Group error enabled |
| xEnableDiagOverflow | FALSE | Diagnostis overrange disabled |
| TRUE | Diagnostis overrange enabled |
| xEnableDiagUnderflow | FALSE | Diagnostis underrange disabled |
| TRUE | Diagnostis underrange enabled |
| xEnable2Wire | FALSE | Channel disabled |
| TRUE | 2-wire |
| uiLineResistance | 0 ... 65535 | Line resistance [Ohm] |
| iUpperUserLimitValue | -32768 ... 32767 | Upper user limit value |
| xEnableDiagLimitOverflow | FALSE | Diagnostis user limiting value overrange disabled |
| TRUE | Diagnostis user limiting value overrange enabled |
| iLowerUserLimitValue | -32768 ... 32767 | Lower user limit value |
| xEnableDiagLimitUnderflow | FALSE | Diagnostis user limiting value underrange disabled |
| TRUE | Diagnostis user limiting value underrange enabled |
| Scaling | xUserScaling | FALSE | User scaling disabled -> use manufacturer scaling |
| TRUE | User scaling enabled |
| iUserScalingOffset | -32768 ... 32767 | User scaling Offset |
| uiUserScalingGain | 0 ... 65535 | User scaling Gain |
| uiUserScalingDivisor | 0 ... 65535 | User scaling Divisor default = 256 -> (read only) |
| Calibration | xUserCalibration | FALSE | User calibration disabled |
| TRUE | User calibration enabled |
| iUserCalibrationOffset | -32768 ... 32767 | User calibration Offset |
| uiUserCalibrationGain | 0 ... 65535 | User calibration Gain |

## typRawChannelScaling (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| uiLineResistance | UINT | [mOhm] (Reg 36) |
| xUserScaling | BOOL | Bit 7 * (Reg 35) |
| iUserScalingOffset | INT | (Reg 39) |
| uiUserScalingGain | UINT | (Reg 40) |
| uiUserScalingDivisor | UINT | (Reg 41) READ ONLY |

## typScaledChannelCalibration (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| xUserCalibration | BOOL | (Reg 35.6) |
| rUserCalibrationGain | REAL | valid range 0 .. 1,9999 (Reg 38) |
| diUserCalibrationOffset | DINT | valid range -262144 .. 261236 (Reg 37) |

## typScaledChannelConfiguration (STRUCT)


| Name | Type |
| --- | --- |
| Settings | typScaledChannelSettings |
| Scaling | typScaledChannelScaling |
| Calibration | typScaledChannelCalibration |

| Struct member | Value | Description |
| --- | --- | --- |
| Settings | eSensorType | Pt100_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Ni100_DIN43760 | DIN 43760 | -60 °C...250 °C | Resolution 0.1 °C |
| Pt1000_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Pt500_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Pt200_EN60751 | IEC 751 | -200 °C...850 °C | Resolution 0.1 °C |
| Ni1000_TK6180 | DIN 43760 | -60 °C...250 °C | Resolution 0.1 °C |
| Ni120_MINCO | Minco | -80 °C...260 °C | Resolution 0.1 °C |
| Ni1000_TK5000 | TK 5000 | -60 °C...250 °C | Resolution 0.1 °C |
| Ni1000_TK6180_01 | DIN 43760 | -50 °C...150 °C | Resolution 0.01 °C |
| Ni1000_TK5000_01 | TK 5000 | -50 °C...150 °C | Resolution 0.01 °C |
| Pt1000_EN60751_01 | IEC 751 | -50 °C...150 °C | Resolution 0.01 °C |
| Resistor_1 |  | 0 Ohm...5 kOhm | Resolution 0.2 Ohm |
| Resistor_2 |  | 0 Ohm...1.2 kOhm | Resolution 0.02 Ohm |
| xEnableDiagGlobal | FALSE | Diagnostis global functions disabled |
| TRUE | Diagnostis global functions enabled |
| xEnableDiagWireBreak | FALSE | Diagnostis wire break disabled |
| TRUE | Diagnostis wire break enabled |
| xEnableDiagShortCircuit | FALSE | Diagnostis short circuit disabled |
| TRUE | Diagnostis short circuit enabled |
| xEnableDiagCommonError | FALSE | Diagnostis Group error disabled |
| TRUE | Diagnostis Group error enabled |
| xEnableDiagOverflow | FALSE | Diagnostis overrange disabled |
| TRUE | Diagnostis overrange enabled |
| xEnableDiagUnderflow | FALSE | Diagnostis underrange disabled |
| TRUE | Diagnostis underrange enabled |
| xEnable2Wire | FALSE | Channel disabled |
| TRUE | 2-wire |
| rLineResistance | 0 ... 65.535 | Line resistance [Ohm] |
| rUpperUserLimitValue |  | Upper user limit value range depends on sensortype |
| xEnableDiagLimitOverflow | FALSE | Diagnostis user limiting value overrange disabled |
| TRUE | Diagnostis user limiting value overrange enabled |
| rLowerUserLimitValue |  | Lower user limit value range depends on sensortype |
| xEnableDiagLimitUnderflow | FALSE | Diagnostis user limiting value underrange disabled |
| TRUE | Diagnostis user limiting value underrange enabled |
| Scaling | xUserScaling | FALSE | User scaling disabled -> use manufacturer scaling |
| TRUE | User scaling enabled |
| rUserScalingOffset |  | User scaling Offset range depends on sensortype |
| uiUserScalingGain | 0 ... 65535 | User scaling Gain |
| uiUserScalingDivisor | 0 ... 65535 | User scaling Divisor default = 256 -> (read only) |
| Calibration | xUserCalibration | FALSE | User calibration disabled |
| TRUE | User calibration enabled |
| diUserCalibrationOffset | -262144 .. 261236 | User calibration Offset |
| rUserCalibrationGain | 0 ... 1.9999 | User calibration Gain |

## typScaledChannelScaling (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| rLineResistance | REAL | (Reg 36) [Ohm] |
| xUserScaling | BOOL | (Reg 35.7) |
| rUserScalingOffset | REAL | (Reg 39) range depends on the selected sensor type |
| uiUserScalingGain | UINT | (Reg 40)valid range 0 .. 65535 |
| uiUserScalingDivisor | UINT | (Reg 41) read only -> default 256 |