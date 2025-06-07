# WagoSysModule_75x_640 v1.9.1.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysModule_75x_640
- **Version:** 1.9.1.0
- **Categories:** WAGO LayerView|Sys; Application
- **Author:** WAG0 / u010545
- **Placeholder:** WagoSysModule_75x_640

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Support for RTC module 75x-640 [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Support for RTC module 75x-640 [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Functions - Methods FbModule_75x_640.ClearChannels (METH) - FbModule_75x_640.GetAntenna (METH) - FbModule_75x_640.GetAuto (METH) - FbModule_75x_640.GetChannelFlags (METH) - FbModule_75x_640.GetDiagnostic (METH) - FbModule_75x_640.GetDstBias (METH) - FbModule_75x_640.GetLocalDate (METH) - FbModule_75x_640.GetLocalTime (METH) - FbModule_75x_640.GetOperatingHoursByNumber (METH) - FbModule_75x_640.GetServiceFlags (METH) - ... and 14 more Program Organization Global Variable Lists

### Indices and tables ¶


| [1] | Based on WagoSysModule_75x_640.library, last modified 14.01.2019, 18:49:40. The content of this file was automatically generated with None on 14.01.2019, 18:49:44 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysModule_75x_640 Library Documentation


| Company: | WAGO |
| Title: | WagoSysModule_75x_640 |
| Version: | 1.9.1.0 |
| Categories: | WAGO LayerView\|Sys; Application |
| Author: | WAG0 / u010545 |
| Placeholder: | WagoSysModule_75x_640 |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Support for RTC module 75x-640 [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Support for RTC module 75x-640 [1]

### Contents:


- 20 Program Organization Units FbModule_75x_640 (FB) - FuDate_To_Weekday (FUN) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysModule_75x_640.library, last modified 14.01.2019, 18:49:40. The content of this file was automatically generated with None on 14.01.2019, 18:49:44 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysModule_75x_640.library |
| contentFile | WagoSysModule_75x_640_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 18:49:44 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 18:49:40 |
| Description | string | See: Description |
| DocFormat | reStructuredText |
| Author | WAG0 / u010545 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysModule_75x_640 |
| Company | WAGO |
| Title | WagoSysModule_75x_640 |
| Project | WagoSysModule_75x_640 |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Version | version | 1.9.1.0 |
| Version string | string |  |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: True | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False PublishSymbolsInContainer: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. IoStandard Library Identification : Placeholder: IoStandard Default Resolution: IoStandard, * (System) Namespace: IoStandard Library Properties : Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : VisuElem3DPath Library Identification : Placeholder: System_VisuElem3DPath Default Resolution: VisuElem3DPath, 3.5.7.0 (System) Namespace: VisuElem3DPath Library Properties : Library Parameter : Parameter: GC_POINTS_PER_POLYGON = 100 VisuElemCamDisplayer Library Identification : Placeholder: System_VisuElemCamDisplayer Default Resolution: VisuElemCamDisplayer, 3.5.7.0 (System) Namespace: VisuElemCamDisplayer Library Properties : Library Parameter : Parameter: GC_POINTS_PER_CAM = 100 VisuElemMeter Library Identification : Placeholder: System_VisuElemMeter Default Resolution: VisuElemMeter, 3.5.7.0 (System) Namespace: VisuElemMeter Library Properties : VisuElemTextEditor Library Identification : Placeholder: System_VisuElemTextEditor Default Resolution: VisuElemTextEditor, 3.5.7.0 (System) Namespace: VisuElemTextEditor Library Properties : VisuElemTrace Library Identification : Placeholder: System_VisuElemTrace Default Resolution: VisuElemTrace, 3.5.7.0 (System) Namespace: VisuElemTrace Library Properties : VisuElems Library Identification : Placeholder: System_VisuElems Default Resolution: VisuElems, 3.5.7.0 (System) Namespace: VisuElems Library Properties : VisuElemsAlarm Library Identification : Placeholder: System_VisuElemsAlarm Default Resolution: VisuElemsAlarm, 3.5.7.0 (System) Namespace: VisuElemsAlarm Library Properties : VisuElemsDateTime Library Identification : Placeholder: System_VisuElemsDateTime Default Resolution: VisuElemsDateTime, 3.5.7.0 (System) Namespace: VisuElemsDateTime Library Properties : VisuElemsSpecialControls Library Identification : Placeholder: System_VisuElemsSpecialControls Default Resolution: VisuElemsSpecialControls, 3.5.7.0 (System) Namespace: VisuElemsSpecialControls Library Properties : VisuElemsWinControls Library Identification : Placeholder: System_VisuElemsWinControls Default Resolution: VisuElemsWinControls, 3.5.7.0 (System) Namespace: VisuElemsWinControls Library Properties : VisuInputs Library Identification : Placeholder: system_visuinputs Default Resolution: VisuInputs, 3.5.13.0 (System) Namespace: visuinputs Library Properties : VisuNativeControl Library Identification : Placeholder: System_VisuNativeControl Default Resolution: VisuNativeControl, 3.5.7.0 (System) Namespace: VisuNativeControl Library Properties : WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MODULE_QUANTITY = 250 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MAX_RUNNABLES = MAX_MODULE_QUANTITY Parameter: MBX_PIPE_SIZE = 1024 Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MAX_MBX_INPUT_SIZE = 47 WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesBusServices Library Identification : Placeholder: WagoTypesBusServices Default Resolution: WagoTypesBusServices, * (WAGO) Namespace: WagoTypesBusServices Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : Library Parameter : Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MAX_MODULE_QUANTITY = 250 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MAX_RUNNABLES = MAX_MODULE_QUANTITY Parameter: MBX_PIPE_SIZE = 1024 Parameter: MAX_MBX_SIZE = 18 Parameter: MAX_MBX1_SIZE = 18 Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MBX_INPUT_SIZE = 47 WagoTypesModule_75x_640 Library Identification : Placeholder: WagoTypesModule_75x_640 Default Resolution: WagoTypesModule_75x_640, * (WAGO) Namespace: WagoTypesModule_75x_640 Library Properties :

### Function Blocks


## FbModule_75x_640 (FB)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Output | todLocalTime | TOD |  |
| dLocalDate | DATE |  |
| dtUTC_Time | DT |  |
| bWeekday | BYTE |  |
| dwChannelFlags | DWORD |  |
| dwServiceFlags | DWORD |  |
| dwDiagnostic | DWORD |  |
| dwAuto | DWORD | — configuration ————————– |
| diTimeZone | DINT | +/- [sec] |
| diDstBias | DINT | +/- [sec] |
| dwAntenna | DWORD |  |
| aTimer | ARRAY [0..RTC_QUANTITY_TIMER] OF typRtcConfigTimer |  |
| aOperating_Hours | ARRAY [0..RTC_QUANTITY_OPERATING_HOURS_COUNTER] OF typRtcOperatingHours |  |

This function block represents a RTC-Module 750-640. If you get one of this module from the toolbox and place it to your local k-bus an global instance of this FB will be automaticly generated. You may change the name of the instance and give it your own identification.

After this you can use the given methods to configure your module. To get the actual time you have only to read the output parameter <myFbName>.todLocalTime . This variable will be automaticly updated in the background. Also you can get some further information from the module.

For detailed use please read the manual of the module 750-640 .

Graphical Illustration

Graphical Interface of FbModule_75x_640

Interface variables Function This function block represents a RTC-Module 750-640. If you get one of this module from the toolbox and place it to your local k-bus an global instance of this FB will be automaticly generated. You may change the name of the instance and give it your own identification. After this you can use the given methods to configure your module. To get the actual time you have only to read the output parameter <myFbName>.todLocalTime . This variable will be automaticly updated in the background. Also you can get some further information from the module. For detailed use please read the manual of the module 750-640 . Graphical Illustration ![Image](images/wagosysmodule_75x_640_3711e042.png) Graphical Interface of FbModule_75x_640 - FbModule_75x_640.ClearChannels (METH) - FbModule_75x_640.GetAntenna (METH) - FbModule_75x_640.GetAuto (METH) - FbModule_75x_640.GetChannelFlags (METH) - FbModule_75x_640.GetDiagnostic (METH) - FbModule_75x_640.GetDstBias (METH) - FbModule_75x_640.GetLocalDate (METH) - FbModule_75x_640.GetLocalTime (METH) - FbModule_75x_640.GetOperatingHoursByNumber (METH) - FbModule_75x_640.GetServiceFlags (METH) - FbModule_75x_640.GetTimeZone (METH) - FbModule_75x_640.GetTimerByNumber (METH) - FbModule_75x_640.GetUTC_Time (METH) - FbModule_75x_640.GetWeekday (METH) - FbModule_75x_640.SetAntenna (METH) - FbModule_75x_640.SetAuto (METH) - FbModule_75x_640.SetChannels (METH) - FbModule_75x_640.SetDateAndTime (METH) - FbModule_75x_640.SetDstBias (METH) - FbModule_75x_640.SetOperatingHours (METH) - FbModule_75x_640.SetServiceInterval (METH) - FbModule_75x_640.SetTimeZone (METH) - FbModule_75x_640.SetTimer (METH) - FbModule_75x_640.SetToManufacturerSettings (METH)

### Functions


## FuDate_To_Weekday (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuDate_To_Weekday | BYTE |
| Input | dDate | DATE |

Converts a given date to the weekday.

possible return values

Graphical Illustration

Graphical Interface of FuDate_To_Weekday

Interface variables Function Converts a given date to the weekday. possible return values - 1 monday - 2 tuesday - 3 wednesday - 4 thursday - 5 friday - 6 saturday - 7 sunday Graphical Illustration ![Image](images/wagosysmodule_75x_640_d0458d90.png) Graphical Interface of FuDate_To_Weekday

### Methods


## FbModule_75x_640.ClearChannels (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ClearChannels | BOOL |
| Input | dwChannels | DWORD |
| Inout | xTrigger | BOOL |

This method clears the channels. Each bit represents one channel.

You have to connect the input parameter xTrigger with an own bool variable. To clear the channels specified by dwChannels you have to set the variable at xTrigger once to TRUE. If the job was delivered then the variable is set to FALSE by the method.

For detailed use please read the manual of the module 750-640 .

Graphical Illustration

Graphical Interface of FbModule_75x_640.ClearChannels

Interface variables Function This method clears the channels. Each bit represents one channel. You have to connect the input parameter xTrigger with an own bool variable. To clear the channels specified by dwChannels you have to set the variable at xTrigger once to TRUE. If the job was delivered then the variable is set to FALSE by the method. For detailed use please read the manual of the module 750-640 . Graphical Illustration ![Image](images/wagosysmodule_75x_640_fce712ac.png) Graphical Interface of FbModule_75x_640.ClearChannels

## FbModule_75x_640.GetAntenna (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetAntenna | DWORD |

## FbModule_75x_640.GetAuto (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetAuto | DWORD |

## FbModule_75x_640.GetChannelFlags (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetChannelFlags | DWORD |

## FbModule_75x_640.GetDiagnostic (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetDiagnostic | DWORD |

## FbModule_75x_640.GetDstBias (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetDstBias | DINT |

## FbModule_75x_640.GetLocalDate (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetLocalDate | DATE |

## FbModule_75x_640.GetLocalTime (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetLocalTime | TOD |

## FbModule_75x_640.GetOperatingHoursByNumber (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetOperatingHoursByNumber | typRtcOperatingHours |
| Input | usiNumber | USINT (0..RTC_QUANTITY_OPERATING_HOURS_COUNTER) |

## FbModule_75x_640.GetServiceFlags (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetServiceFlags | DWORD |

## FbModule_75x_640.GetTimeZone (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetTimeZone | DINT |

## FbModule_75x_640.GetTimerByNumber (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetTimerByNumber | typRtcConfigTimer |
| Input | usiNumber | USINT (0..RTC_QUANTITY_TIMER) |

## FbModule_75x_640.GetUTC_Time (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetUTC_Time | DT |

## FbModule_75x_640.GetWeekday (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetWeekday | BYTE |

## FbModule_75x_640.SetAntenna (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetAntenna | BOOL |
| Input | bAntenna | BYTE |
| Inout | xTrigger | BOOL |

| Byte | Bit | Function |
| --- | --- | --- |
| 0 | 0..1 | 0: No time signal reception 1: DCF77 Decoder activated 2: WWVB Decoder activated |
| 0 | 2 | DCF77 Polarity reversed 0 = Low-active 1 = High-active |

```
VAR
    myTrigger   :   BOOL;
    FlkStart    :   BOOL;
END_VAR

//--- set myTrigger once with a rising edge from xStart
IF xStart AND NOT FlkStart then
    myTrigger := TRUE;
END_IF
FlkStart := xStart;
//-----------------------------------------------------

myFb640.SetAntenna(bAntenna := 16#05, xTrigger := myTrigger);
```

This method set the decoder scheme for time signal reception. See the manual for further information.

Possible values for ‘bAntenna’

You have to connect the input parameter xTrigger with an own bool variable. To transmit the value from bAntenna to the module you have to set the variable at xTrigger once to TRUE. If the method has delivered the value then the variable is set to FALSE by the method.

On setting the time zone and summer time using different antennas.

Graphical Illustration

Graphical Interface of FbModule_75x_640.SetAntenna

Interface variables Function This method set the decoder scheme for time signal reception. See the manual for further information. Possible values for ‘bAntenna’ You have to connect the input parameter xTrigger with an own bool variable. To transmit the value from bAntenna to the module you have to set the variable at xTrigger once to TRUE. If the method has delivered the value then the variable is set to FALSE by the method. Note On setting the time zone and summer time using different antennas. - The DCF77 transmitter sends CET (Central European Time) or CEST (Central European Summer Time), the summer time setting (DstBias) remains set to zero. The time zone for Germany is 0. - The WWVB transmitter sends in UTC. If the module is operated at the US east coast (Eastern Time) for example, an offset of 5 hours (0xFFFFB9B0) must be entered in the TimeZone. The transition from winter time to summer time is done using a status bit within the time telegram. By setting this bit, one more hour will be transmitted by the module. Within the module, the transition is always performed at 00:00. Graphical Illustration ![Image](images/wagosysmodule_75x_640_ac9f0e5a.png) Graphical Interface of FbModule_75x_640.SetAntenna Example

## FbModule_75x_640.SetAuto (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetAuto | BOOL |
| Input | dwAuto | DWORD |
| Inout | xTrigger | BOOL |

This method switch the automatic mode on / off for the channels. Each bit represents one channel.

The automatic mode of the relevant switching channel is switched off for each bit set in Auto. The off switching channel can only be changed using the methods SetChannels() and ClearChannels().

For detailed use please read the manual of the module 750-640 .

Graphical Illustration

Graphical Interface of FbModule_75x_640.SetAuto

Interface variables Function This method switch the automatic mode on / off for the channels. Each bit represents one channel. The automatic mode of the relevant switching channel is switched off for each bit set in Auto. The off switching channel can only be changed using the methods SetChannels() and ClearChannels(). For detailed use please read the manual of the module 750-640 . Graphical Illustration ![Image](images/wagosysmodule_75x_640_814ca6c5.png) Graphical Interface of FbModule_75x_640.SetAuto

## FbModule_75x_640.SetChannels (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetChannels | BOOL |
| Input | dwChannels | DWORD |
| Inout | xTrigger | BOOL |

## FbModule_75x_640.SetDateAndTime (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetDateAndTime | BOOL |
| Input | dtNewValue | DT |
| Inout | xTrigger | BOOL |

This method set date and time for the module.

You have to connect the input parameter xTrigger with an own bool variable. To set the date and time for the module you have to set the variable at xTrigger once to TRUE. If the job was delivered then the variable is set to FALSE by the method.

For detailed use please read the manual of the module 750-640 .

Graphical Illustration

Graphical Interface of FbModule_75x_640.SetDateAndTime

Interface variables FUNCTION This method set date and time for the module. You have to connect the input parameter xTrigger with an own bool variable. To set the date and time for the module you have to set the variable at xTrigger once to TRUE. If the job was delivered then the variable is set to FALSE by the method. For detailed use please read the manual of the module 750-640 . Graphical Illustration ![Image](images/wagosysmodule_75x_640_ea05a36d.png) Graphical Interface of FbModule_75x_640.SetDateAndTime

## FbModule_75x_640.SetDstBias (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetDstBias | BOOL |  |
| Input | diDstBias | DINT | +/- [sec] |
| Inout | xTrigger | BOOL |  |

This method set the daylight saving time for the module.

For the transition from winter time to summer time, the content of DstBias (Daylight Saving Time) is added to the TimeZone when the time is being evaluated. This way, the transition can be performed without having to change the time or time zone.

For detailed use please read the manual of the module 750-640 .

Graphical Illustration

Graphical Interface of FbModule_75x_640.SetDstBias

Interface variables FUNCTION This method set the daylight saving time for the module. For the transition from winter time to summer time, the content of DstBias (Daylight Saving Time) is added to the TimeZone when the time is being evaluated. This way, the transition can be performed without having to change the time or time zone. For detailed use please read the manual of the module 750-640 . Graphical Illustration ![Image](images/wagosysmodule_75x_640_1e3a9b6e.png) Graphical Interface of FbModule_75x_640.SetDstBias

## FbModule_75x_640.SetOperatingHours (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetOperatingHours | BOOL |  |
| Input | usiCounterNumber | USINT (0..31) | Operating Hours Counter 0 .. 31 |
| udiOperatingHours | UDINT | [ sec] data type TIME is useable for max. 49,7 days |
| Inout | xTrigger | BOOL |  |

## FbModule_75x_640.SetServiceInterval (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetServiceInterval | BOOL |  |
| Input | usiCounterNumber | USINT (0..31) | Operating Hours Counter 0 .. 31 |
| udiServiceInterval | UDINT | [ sec] data type TIME is useable for max. 49,7 days |
| Inout | xTrigger | BOOL |  |

## FbModule_75x_640.SetTimeZone (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetTimeZone | BOOL |  |
| Input | diTimeZone | DINT | +/- [sec] |
| Inout | xTrigger | BOOL |  |

This method set the time zone for the module.

You have to connect the input parameter xTrigger with an own bool variable. To set the time zone specified by diTimeZone (+/- [sec]) you have to set the variable at xTrigger once to TRUE. If the job was delivered then the variable is set to FALSE by the method.

For detailed use please read the manual of the module 750-640 .

Graphical Illustration

Graphical Interface of FbModule_75x_640.SetTimeZone

Interface variables FUNCTION This method set the time zone for the module. You have to connect the input parameter xTrigger with an own bool variable. To set the time zone specified by diTimeZone (+/- [sec]) you have to set the variable at xTrigger once to TRUE. If the job was delivered then the variable is set to FALSE by the method. For detailed use please read the manual of the module 750-640 . Graphical Illustration ![Image](images/wagosysmodule_75x_640_e4a1df8a.png) Graphical Interface of FbModule_75x_640.SetTimeZone

## FbModule_75x_640.SetTimer (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetTimer | BOOL |  |
| Input | usiNumber | USINT (0..31) | Timer 0 .. 31 |
| dtFirstEvent | DT |  |
| dtLastEvent | DT |  |
| tDelay | TIME |  |
| dwOnChannels | DWORD |  |
| dwOffChannels | DWORD |  |
| bWeekDays | BYTE |  |
| Inout | xTrigger | BOOL |  |

## FbModule_75x_640.SetToManufacturerSettings (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetToManufacturerSettings | BOOL |
| Inout | xTrigger | BOOL |

This method set the module to manufacturer settings.

You have to connect the input parameter xTrigger with an own bool variable. To reset the module you have to set the variable at xTrigger once to TRUE. If the job was delivered then the variable is set to FALSE by the method.

All configuration data is overwritten with zero.

For detailed use please read the manual of the module 750-640 .

Graphical Illustration

Graphical Interface of FbModule_75x_640.SetToManufacturerSettings

Interface variables FUNCTION This method set the module to manufacturer settings. You have to connect the input parameter xTrigger with an own bool variable. To reset the module you have to set the variable at xTrigger once to TRUE. If the job was delivered then the variable is set to FALSE by the method. Note All configuration data is overwritten with zero. For detailed use please read the manual of the module 750-640 . Graphical Illustration ![Image](images/wagosysmodule_75x_640_c96ba7c5.png) Graphical Interface of FbModule_75x_640.SetToManufacturerSettings

### Program Organization


## 20 Program Organization Units


- FbModule_75x_640 (FB) FbModule_75x_640.ClearChannels (METH) - FbModule_75x_640.GetAntenna (METH) - FbModule_75x_640.GetAuto (METH) - FbModule_75x_640.GetChannelFlags (METH) - FbModule_75x_640.GetDiagnostic (METH) - FbModule_75x_640.GetDstBias (METH) - FbModule_75x_640.GetLocalDate (METH) - FbModule_75x_640.GetLocalTime (METH) - FbModule_75x_640.GetOperatingHoursByNumber (METH) - FbModule_75x_640.GetServiceFlags (METH) - FbModule_75x_640.GetTimeZone (METH) - FbModule_75x_640.GetTimerByNumber (METH) - FbModule_75x_640.GetUTC_Time (METH) - FbModule_75x_640.GetWeekday (METH) - FbModule_75x_640.SetAntenna (METH) - FbModule_75x_640.SetAuto (METH) - FbModule_75x_640.SetChannels (METH) - FbModule_75x_640.SetDateAndTime (METH) - FbModule_75x_640.SetDstBias (METH) - FbModule_75x_640.SetOperatingHours (METH) - FbModule_75x_640.SetServiceInterval (METH) - FbModule_75x_640.SetTimeZone (METH) - FbModule_75x_640.SetTimer (METH) - FbModule_75x_640.SetToManufacturerSettings (METH) FuDate_To_Weekday (FUN)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

WagoSysModule_75x-640

WagoSysModule_75x-640