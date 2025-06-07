# WagoTypesModule_75x_658 v1.6.1.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesModule_75x_658
- **Version:** 1.6.1.0
- **Categories:** WAGO LayerView|Types and Interfaces
- **Author:** WAGO/u010663
- **Placeholder:** WagoTypesModule_75x_658

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling Can module 750-658 and onboard Can interfaces [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling Can module 750-658 and onboard Can interfaces [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Functions - Methods I_WagoModule_75x_658Extended.Configuration (METH) - I_WagoModule_75x_658Extended.ConfigurationCheck (METH) - I_WagoModule_75x_658Extended.DoMbxReset (METH) - I_WagoModule_75x_658Extended.GetDiagnosis (METH) - I_WagoModule_75x_658Extended.GetProcessInByte (METH) - I_WagoModule_75x_658Extended.GetStatusByte (METH) - I_WagoModule_75x_658Extended.SetProcessOutByte (METH) - I_WagoModule_75x_658Extended.configurationEx (METH) - typFilterSettings (STRUCT) - typMappingRxSettings (STRUCT) - ... and 1 more Interfaces Program Organization Other Components - CAN_DataTypes - ParameterList (PARAMS) - eBitrate (ENUM) - eDiagQualMode (ENUM) - eDiagQualType (ENUM) - eErrorCode (ENUM) - eL2_FRAME_ERROR (ENUM) - eMode (ENUM) - eStatus (ENUM) - typBusInfoCan (STRUCT) - ... and 9 more

### Indices and tables ¶


| [1] | Based on WagoTypesModule_75x_658.library, last modified 14.01.2019, 18:39:01. The content of this file was automatically generated with None on 14.01.2019, 18:39:05 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesModule_75x_658 Library Documentation


| Company: | WAGO |
| Title: | WagoTypesModule_75x_658 |
| Version: | 1.6.1.0 |
| Categories: | WAGO LayerView\|Types and Interfaces |
| Author: | WAGO/u010663 |
| Placeholder: | WagoTypesModule_75x_658 |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling Can module 750-658 and onboard Can interfaces [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling Can module 750-658 and onboard Can interfaces [1]

### Contents:


- 20 Program Organization Units CAN_DataTypes - I_WagoModule_75x_658Extended (ITF) FuGetVersionHistory (FUN) ParameterList (PARAMS)

### Indices and tables


| [1] | Based on WagoTypesModule_75x_658.library, last modified 14.01.2019, 18:39:01. The content of this file was automatically generated with None on 14.01.2019, 18:39:05 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesModule_75x_658.library |
| contentFile | WagoTypesModule_75x_658_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 18:39:05 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 18:39:01 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO/u010663 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesModule_75x_658 |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesModule_75x_658 |
| Version | version | 1.6.1.0 |
| ActivateSigning | bool | False |
| Title | string | WagoTypesModule_75x_658 |
| LibraryCategories | library-category-list | WAGO LayerView\|Types and Interfaces |
| Version string | string |  |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : WagoTypesCan Library Identification : Placeholder: WagoTypesCan Default Resolution: WagoTypesCan, * (WAGO) Namespace: WagoTypesCan Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_SIZE = 18

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 08.01.2019 | 1.6.1.0 | u015842 | Properties: free placeholder added |
| 26.02.2016 | 1.6.0.0 | u01663 | Update according to WagoSysErrorBase |
| 26.02.2016 | 1.5.2.0 | u01663 | Interface extended |
| 07.12.2015 | 1.5.1.0 | u01663 | Refurbished enumeration names |
| 26.11.2015 | 1.5.0.1 | u01663 | Improvement Can_eErrorCode |
| 29.09.2015 | 1.5.0.0 | u01663 | Libraries inserted by placeholder |
| 24.08.2015 | 0.0.0.7 | u01663 | Placeholder added |
| 01.06.2015 | 0.0.0.6 | u01663 | for internal tests only, included libs changed |

WagoTypesModule_75x_658.library

Interface variables WagoTypesModule_75x_658.library

### Methods


## I_WagoModule_75x_658Extended.Configuration (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Configuration | BOOL |  |
| Input | xExecute | BOOL | start command |
| xWriteRead | BOOL | 0:Read; 1:Write |
| xSaveValues | BOOL | 1:after write command values will be additional stored in EEPROM |
| Inout | eBitrate | eBitrate | baudrate |
| eMode | eMode | transparent,mapped or sniffer mode |
| x29BitEnabled | BOOL | 1:support 29 Bit Cob -IDs |
| xSdoEnabled | BOOL | 1:allow SDO commands over the acyclic mailbox |
| xDiagOverMbx0Enabled | BOOL |  |
| typConfigData | typFullConfiguration | configuration data |
| Output | xDone | BOOL | command successful executed |
| xBusy | BOOL | command in progress |
| xError | BOOL | command executed with error |
| oStatus | WagoSysErrorBase.FbResult | Status and error information |

## I_WagoModule_75x_658Extended.ConfigurationCheck (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ConfigurationCheck | BOOL |  |
| Input | xExecute | BOOL | start the compare functionality |
| Inout | typConfigData | typFullConfiguration | configuration data |
| Output | xDone | BOOL | comparison finished without error |
| xBusy | BOOL | comparison active |
| xError | BOOL | comparison finished with error |
| xDataMatches | BOOL | result |

## I_WagoModule_75x_658Extended.DoMbxReset (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DoMbxReset | BOOL |

## I_WagoModule_75x_658Extended.GetDiagnosis (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetDiagnosis | WagoTypesModuleBase.eServiceState |  |
| Input | xEnable | BOOL |  |
| dtTime | DT |  |
| Output | xValid | BOOL | data valid |
| xBusy | BOOL | busy, waiting for diagnosis messages activated |
| xError | BOOL | function block can not receive diagnosis messages, due to communication error |
| eDiagnosisErrorCode | eErrorCode | Achtung prüfen ob die enumeration nicht besser in diese Bibliothek gehört |
| bDiagnosisChannelNo | BYTE |  |
| eDiagnosisMode | eDiagQualMode |  |
| eDiagnosisType | eDiagQualType |  |
| Inout | xReset | BOOL |  |

## I_WagoModule_75x_658Extended.GetProcessInByte (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetProcessInByte | BYTE |
| Input | ByteNo | UINT |

## I_WagoModule_75x_658Extended.GetStatusByte (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetStatusByte | BYTE |

## I_WagoModule_75x_658Extended.SetProcessOutByte (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | ByteNo | UINT |
| OutData | BYTE |

## I_WagoModule_75x_658Extended.configurationEx (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ConfigurationEx | BOOL |  |
| Input | xExecute | BOOL | start command |
| xWriteRead | BOOL | 0:Read; 1:Write |
| Inout | bSize | BYTE |  |
| bSizeAcyclicMbx | BYTE |  |
| Output | xDone | BOOL | command successful executed |
| xBusy | BOOL | command in progress |
| xError | BOOL | command executed with error |
| oStatus | WagoSysErrorBase.FbResult | Status and error information |

## typFilterSettings (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| LowHigh_ID | WORD |  |
| LowLow_ID | WORD |  |
| HighHigh_ID | WORD |  |
| HighLow_ID | WORD |  |
| Feature1 | WORD | 1:Enable |
| Feature2 | WORD | 1:override |

## typMappingRxSettings (STRUCT)


| Name | Type |
| --- | --- |
| COB_ID_MSW | WORD |
| COB_ID_LSW | WORD |
| CopyToPDIn | WORD |
| Data_0_1 | WORD |
| Data_2_3 | WORD |
| Data_4_5 | WORD |
| Data_6_7 | WORD |

## typMappingTxSettings (STRUCT)


| Name | Type |
| --- | --- |
| COB_ID_MSW | WORD |
| COB_ID_LSW | WORD |
| SendGroup | WORD |
| FixedValue | WORD |
| Data_0_1 | WORD |
| Data_2_3 | WORD |
| Data_4_5 | WORD |
| Data_6_7 | WORD |
| CycleTime | WORD |

### Interfaces


## I_WagoModule_75x_658Extended (ITF)


- I_WagoModule_75x_658Extended.Configuration (METH) - I_WagoModule_75x_658Extended.ConfigurationCheck (METH) - I_WagoModule_75x_658Extended.DoMbxReset (METH) - I_WagoModule_75x_658Extended.GetDiagnosis (METH) - I_WagoModule_75x_658Extended.GetProcessInByte (METH) - I_WagoModule_75x_658Extended.GetStatusByte (METH) - I_WagoModule_75x_658Extended.SetProcessOutByte (METH) - I_WagoModule_75x_658Extended.configurationEx (METH)

### Program Organization


## 20 Program Organization Units


- CAN_DataTypes eBitrate (ENUM) - eDiagQualMode (ENUM) - eDiagQualType (ENUM) - eErrorCode (ENUM) - eL2_FRAME_ERROR (ENUM) - eMode (ENUM) - eStatus (ENUM) - typBusInfoCan (STRUCT) - typCAN_Frame (STRUCT) - typData (STRUCT) - typDiag (STRUCT) - typDiagQualifier (STRUCT) - typFilterSettings (STRUCT) - typFullConfiguration (STRUCT) - typMappedRx (STRUCT) - typMappedTx (STRUCT) - typMappingRxSettings (STRUCT) - typMappingTxSettings (STRUCT) - typMsgMasterRx (STRUCT) - typMsgMasterTx (STRUCT) I_WagoModule_75x_658Extended (ITF) - I_WagoModule_75x_658Extended.Configuration (METH) - I_WagoModule_75x_658Extended.ConfigurationCheck (METH) - I_WagoModule_75x_658Extended.DoMbxReset (METH) - I_WagoModule_75x_658Extended.GetDiagnosis (METH) - I_WagoModule_75x_658Extended.GetProcessInByte (METH) - I_WagoModule_75x_658Extended.GetStatusByte (METH) - I_WagoModule_75x_658Extended.SetProcessOutByte (METH) - I_WagoModule_75x_658Extended.configurationEx (METH)

### Other Components


## CAN_DataTypes


- eBitrate (ENUM) - eDiagQualMode (ENUM) - eDiagQualType (ENUM) - eErrorCode (ENUM) - eL2_FRAME_ERROR (ENUM) - eMode (ENUM) - eStatus (ENUM) - typBusInfoCan (STRUCT) - typCAN_Frame (STRUCT) - typData (STRUCT) - typDiag (STRUCT) - typDiagQualifier (STRUCT) - typFilterSettings (STRUCT) - typFullConfiguration (STRUCT) - typMappedRx (STRUCT) - typMappedTx (STRUCT) - typMappingRxSettings (STRUCT) - typMappingTxSettings (STRUCT) - typMsgMasterRx (STRUCT) - typMsgMasterTx (STRUCT)

## ParameterList (PARAMS)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | CAN_RX_MAX_MESSAGES | DINT | 100 |
| CAN_TX_MAX_MESSAGES | DINT | 100 |

## eBitrate (ENUM)


| Name | Initial |
| --- | --- |
| CAN_10kBits | 0 |
| CAN_20kBits | 1 |
| CAN_50kBits | 2 |
| CAN_125kBits | 3 |
| CAN_250kBits | 4 |
| CAN_500kBits | 5 |
| CAN_800kBits | 6 |
| CAN_1000kBits | 7 |
| CAN_Auto | 8 |

## eDiagQualMode (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| MBX_NoDiag | 0 | no diagnosis message |
| MBX_DiagSingleShot | 1 | diagnosis message |
| MBX_DiagDisappears | 2 | diagnosis disappears |
| MBX_DiagAppears | 3 | diagnosis appears |

## eDiagQualType (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| MBX_DiagType_OK | 0 | OK |
| MBX_DiagNotification | 1 | Diagnosis is a notification |
| MBX_DiagWarning | 2 | Diagnosis is a warning |
| MBX_DiagError | 3 | Diagnosis is an error |

## eErrorCode (ENUM)


| Name | Initial |
| --- | --- |
| _No_Error | 0 |
| CAN_Stuff_Error | 1000 |
| CAN_Form_Error | 1001 |
| CAN_Acknowledgement_Error | 1002 |
| CAN_Bit_Error_recessive | 1003 |
| CAN_Bit_Error_dominant | 1004 |
| CAN_CRC_Error | 1005 |
| CAN_SW_Error | 1006 |
| CAN_Hardware_In_Bus_Off_State | 1007 |
| CAN_RxCounter_Bigger_Than_127 | 1008 |
| CAN_RxCounter_Bigger_Than_96 | 1009 |
| CAN_TxCounter_Bigger_Than_127 | 1010 |
| CAN_TxCounter_Bigger_Than_96 | 1011 |
| CAN_Transmit_Error | 1012 |
| CAN_Arbitration_Lost | 1013 |
| CAN_RxBuffer0_Overrun | 1014 |
| CAN_RxBuffer1_Overrun | 1015 |
| CAN_TxBuffer_Overrun | 1016 |
| CAN_Bus_Off_State | 1017 |
| CAN_DRV_Internal_Upstrm_Buf_Overrun | 1018 |
| CAN_DRV_Internal_Dnstrm_Buf_Overrun | 1019 |
| CAN_General_Error | 2000 |
| CAN_24V_Unpowered | 2001 |
| CAN_ParameterChannel | 2002 |
| CAN_ExtRegCom_Rsp_Not_OK | 2003 |
| CAN_ExtRegCom_Rsp_Access_Denied | 2004 |
| CAN_ExtRegCom_TableReadOnly | 2005 |
| CAN_ExtRegCom_Rsp_Length | 2006 |
| CAN_ExtRegCom_Rsp_TableUnknown | 2007 |
| CAN_ExtRegCom_Rsp_RegUnknown | 2008 |
| CAN_CmdInterface_Err | 2009 |
| CAN_ParamChannel | 2010 |
| CAN_RegComm | 2011 |
| CAN_Rx_Receive_NOK | 1038 |
| CAN_Tx_Receive_NOK | 1039 |
| CAN_Mbx1_Error_0 | 3000 |
| CAN_Mbx1_Error_1 | 3001 |
| CAN_Mbx1_Error_2 | 3002 |
| CAN_Mbx1_Error_3 | 3003 |
| CAN_Mbx1_Error_4 | 3004 |
| CAN_Mbx1_Error_5 | 3005 |
| CAN_Mbx1_Error_6 | 3006 |
| CAN_Mbx1_Error_7 | 3007 |
| CAN_Mbx1_Error_8 | 3008 |
| CAN_Mbx1_Error_9 | 3009 |
| CAN_Mbx1_Error_10 | 3010 |
| CAN_Mbx1_Error_11 | 3011 |
| CAN_Mbx1_Error_12 | 3012 |
| CAN_Mbx1_Error_13 | 3013 |
| CAN_Mbx1_Error_14 | 3014 |
| CAN_Mbx1_Error_15 | 3015 |
| CAN_Mbx1_Error_16 | 3016 |
| CAN_Mbx1_Error_17 | 3017 |
| CAN_Mbx1_Error_18 | 3018 |
| CAN_Mbx1_Error_19 | 3019 |
| CAN_Mbx1_Error_20 | 3020 |
| CAN_Mbx1_Error_21 | 3021 |
| CAN_Mbx1_Error_22 | 3022 |
| CAN_Mbx1_Error_23 | 3023 |
| CAN_Mbx1_Error_24 | 3024 |
| CAN_Mbx1_Error_25 | 3025 |
| CAN_Mbx1_Error_26 | 3026 |
| CAN_Mbx1_Error_27 | 3027 |
| CAN_Mbx1_Error_28 | 3028 |
| CAN_Mbx1_Error_29 | 3029 |
| CAN_Mbx1_Error_30 | 3030 |
| CAN_Mbx1_Error_31 | 3031 |
| CAN_Mbx2_Error_0 | 4000 |
| CAN_Mbx2_Error_1 | 4001 |
| CAN_Mbx2_Error_2 | 4002 |
| CAN_Mbx2_Error_3 | 4003 |
| CAN_Mbx2_Error_4 | 4004 |
| CAN_Mbx2_Error_5 | 4005 |
| CAN_Mbx2_Error_6 | 4006 |
| CAN_Mbx2_Error_7 | 4007 |
| CAN_Mbx2_Error_8 | 4008 |
| CAN_Mbx2_Error_9 | 4009 |
| CAN_Mbx2_Error_10 | 4010 |
| CAN_Mbx2_Error_11 | 4011 |
| CAN_Mbx2_Error_12 | 4012 |
| CAN_Mbx2_Error_13 | 4013 |
| CAN_Mbx2_Error_14 | 4014 |
| CAN_Mbx2_Error_15 | 4015 |
| CAN_Mbx2_Error_16 | 4016 |
| CAN_Mbx2_Error_17 | 4017 |
| CAN_Mbx2_Error_18 | 4018 |
| CAN_Mbx2_Error_19 | 4019 |
| CAN_Mbx2_Error_20 | 4020 |
| CAN_Mbx2_Error_21 | 4021 |
| CAN_Mbx2_Error_22 | 4022 |
| CAN_Mbx2_Error_23 | 4023 |
| CAN_Mbx2_Error_24 | 4024 |
| CAN_Mbx2_Error_25 | 4025 |
| CAN_Mbx2_Error_26 | 4026 |
| CAN_Mbx2_Error_27 | 4027 |
| CAN_Mbx2_Error_28 | 4028 |
| CAN_Mbx2_Error_29 | 4029 |
| CAN_Mbx2_Error_30 | 4030 |
| CAN_Mbx2_Error_31 | 4031 |

## eL2_FRAME_ERROR (ENUM)


| Name | Initial |
| --- | --- |
| CAN_L2_OK | 0 |
| CAN_L2_BUS_IDLE | 1 |
| CAN_L2_PORT_WRONG | 2 |
| CAN_L2_PORT_BUSY | 3 |
| CAN_L2_SEND_OK | 4 |
| CAN_L2_RECEIVE_OK | 5 |
| CAN_L2_SEND_ERROR | 6 |
| CAN_L2_ID_ERROR | 7 |
| CAN_L2_DATALENGTH_ERROR | 8 |
| CAN_L2_RECEIVE_BUFFER_ERROR | 9 |
| CAN_L2_REGISTER_ERROR | 10 |
| CAN_L2_TIMEOUT | 99 |

## eMode (ENUM)


| Name | Initial |
| --- | --- |
| CAN_Sniffer | 0 |
| CAN_Transparent | 1 |
| CAN_Mapped | 2 |

## eStatus (ENUM)


| Name | Initial |
| --- | --- |
| CAN_Module_size_matches | 0 |
| CAN_Error_module_size | 1 |
| CAN_Error_acyclic_channel_size | 2 |
| CAN_Comm_Disabled | 3 |

## typBusInfoCan (STRUCT)


| Name | Type |
| --- | --- |
| uiTxLayer2Error | UINT |
| uiRxLayer2Error | UINT |

## typCAN_Frame (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| COB_ID | DWORD | CAN ID. |
| RTR_FRAME | BOOL |  |
| IDE | BOOL | Identifier bit. Must be TRUE in Ext. Frame. |
| DATALENGTH | BYTE |  |
| DATA | ARRAY [1..8] OF BYTE |  |

## typData (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| Rec | ARRAY [0..CAN_RX_MAX_MESSAGES] OF typMsgMasterRx | aux1 : WORD; |
| RecCount | BYTE |  |
| Send | ARRAY [0..CAN_TX_MAX_MESSAGES] OF typMsgMasterTx |  |
| SendCount | BYTE | neu,weil mehr als eine Nachricht in einem SPS zyklus verschickt werden kann |
| execute | BOOL |  |
| reset | BOOL |  |
| CAN_TXactive | BOOL | dient zur Koordination der Sendeaufträge. |
| CAN_ready | BOOL | wenn der Master auf der richtigen Datenbreite steht, nur dann dürfen die weiteren Bausteine arbeiten |
| MessageCoding29BitActive | BOOL |  |
| CAN_RX_CycleDetection | WORD |  |

## typDiag (STRUCT)


| Name | Type |
| --- | --- |
| Service_ID | BYTE |
| EventCode | WORD |
| ChannelNo | BYTE |
| DiagQualifier | typDiagQualifier |
| DiagCodeString | STRING |
| DiagQualModeString | STRING |
| DiagQualTypeString | STRING |
| DiagTime | DT |

## typDiagQualifier (STRUCT)


| Name | Type |
| --- | --- |
| DiagMode | eDiagQualMode |
| DiagTYPE | eDiagQualType |

## typFullConfiguration (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| aRegister | ARRAY [0..gcCAN_MaxBufferClassicRegister] OF WORD | module register |
| COB_ID_Filter | ARRAY [0..5] OF typFilterSettings |  |
| myTX_Mapping | ARRAY [0..44] OF typMappingTxSettings |  |
| myRX_Mapping | ARRAY [0..44] OF typMappingRxSettings |  |

## typMappedRx (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| COBID | DWORD |  |
| DataByte | BYTE | 1..8 |
| On | BOOL |  |

## typMappedTx (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| COBID | DWORD |  |
| Data | ARRAY [0..7] OF BYTE |  |
| COV | BOOL | Change on value |
| Cyclic | WORD | Wert als ms |
| Group | BYTE | 0 nicht senden, 1..8 Gruppennummer |
| on | BOOL |  |
| DLC | BYTE | Anzahl der Bytes im PDO |
| RTR | BOOL |  |

## typMsgMasterRx (STRUCT)


| Name | Type |
| --- | --- |
| MsgLength | UINT |
| MsgID | BYTE |
| MsgPrio | INT |
| Msg | ARRAY [0..gcCAN_MsgLength] OF BYTE |

## typMsgMasterTx (STRUCT)


| Name | Type |
| --- | --- |
| MsgLength | UINT |
| MsgID | BYTE |
| MsgPrio | INT |
| Msg | ARRAY [0..gcCAN_MsgLength] OF BYTE |