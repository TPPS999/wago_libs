# WagoSysModem_Internal_PFC v1.1.4.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysModem_Internal_PFC
- **Version:** 1.1.4.0
- **Categories:** WAGO Internal|Common; WAGO Internal|Feature|Common; WAGO Internal|Feature|Network; WAGO Internal|Target|PFC
- **Namespace:** WagoSysModemInternal
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysModemInternal

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

This is an external library to make the functions of the modem available

The function blocks of this library are NOT thread safe and must be called from one CODESYS task only! Concurrent calls from different tasks may cause loss or corruption of data. [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. This is an external library to make the functions of the modem available The function blocks of this library are NOT thread safe and must be called from one CODESYS task only! Concurrent calls from different tasks may cause loss or corruption of data. [1]

### Contents: ¶


Contents: - Project Information - Library Information - Functions FuGet_modem_device_info (FUN) - FuGet_network_access_info (FUN) - FuGet_network_registration_settings (FUN) - FuGet_sim_info (FUN) - FuGet_wds_enable (FUN) - FuGet_wds_info (FUN) - FuGet_wds_settings (FUN) - FuNetscan_list_get_element (FUN) - FuNetscan_list_get_size (FUN) - FuNetscan_list_refresh (FUN) - ... and 14 more Program Organization Internal Components Global Variable Lists

### Indices and tables ¶


| [1] | Based on WagoSysModem_Internal_PFC.library, last modified 25.05.2021, 16:33:11. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysModem_Internal_PFC.library |
| contentFile | WagoSysModem_Internal_PFC_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 25.05.2021, 16:33:14 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 25.05.2021, 16:33:11 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2020 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | False |
| LanguageModelAttribute | string | qualified-access-only |
| Company | WAGO |
| DocFormat | reStructuredText |
| SourceLibrary | bool | False |
| Project | string | WagoSysModem_Internal_PFC |
| DefaultNamespace | WagoSysModemInternal |
| Version | version | 1.1.4.0 |
| ThreadSafe | string | False |
| Title | WagoSysModem_Internal_PFC |
| Released | bool | False |
| Placeholder | string | WagoSysModemInternal |
| LibraryCategories | library-category-list | WAGO Internal\|Common; WAGO Internal\|Feature\|Common; WAGO Internal\|Feature\|Network; WAGO Internal\|Target\|PFC |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |
| IsEndUserLibrary | bool | False |

### Library Information


## Library Reference


This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces.

### WagoSysVersion


#### Library Identification


Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: WagoSysVersion, 1.0.0.0 (WAGO) SystemLibrary: False | Optional: False |

### WagoTypesModem


#### Library Identification


Placeholder: WagoTypesModem Default Resolution: WagoTypesModem, * (WAGO) Namespace: WagoTypesModem

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: WagoTypesModem SystemLibrary: False | Optional: False |

### Functions


## FuGet_modem_device_info (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGet_modem_device_info | WagoTypesModem.typModemDeviceInfo |
| Input | pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuGet_network_access_info (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGet_network_access_info | WagoTypesModem.typNetworkAccessInfo |
| Input | pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuGet_network_registration_settings (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGet_network_registration_settings | WagoTypesModem.typNetworkRegistrationSettings |
| Input | pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuGet_sim_info (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGet_sim_info | WagoTypesModem.typSimInfo |
| Input | pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuGet_wds_enable (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGet_wds_enable | BOOL |
| Input | pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuGet_wds_info (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGet_wds_info | WagoTypesModem.typWdsInfo |
| Input | pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuGet_wds_settings (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGet_wds_settings | WagoTypesModem.typWdsSettings |
| Input | pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuNetscan_list_get_element (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuNetscan_list_get_element | WagoTypesModem.eResult |  |
| Input | uiIndex | UINT | Index of the network info element in the netscan list |
| Output | NetInfo | WagoTypesModem.typNetworkScanInfo |  |
| sResultText | STRING |  |

## FuNetscan_list_get_size (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuNetscan_list_get_size | WagoTypesModem.eResult |
| Output | uiSize | UINT |
| sResultText | STRING |

## FuNetscan_list_refresh (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuNetscan_list_refresh | WagoTypesModem.eResult |
| Output | sResultText | STRING |

Run a netscan and refresh the list of found networks

Interface variables Run a netscan and refresh the list of found networks

## FuReset_modem (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Input | pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuSet_network_registration_settings (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Input | typNetworkRegistrationSettings | WagoTypesModem.typNetworkRegistrationSettings |
| pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuSet_sim_pin (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Input | sPin | STRING(8) |
| pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuSet_sim_puk (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Input | sPuk | STRING(8) |
| sNewPin | STRING(8) |
| pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuSet_wds_enable (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Input | xEnable | BOOL |
| pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuSet_wds_settings (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Input | typWdsSettings | WagoTypesModem.typWdsSettings |
| pResult | POINTER TO WagoTypesModem.eResult |
| pResultText | POINTER TO STRING |
| uiResultTextSize | UINT |

## FuSms_delete (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSms_delete | WagoTypesModem.eResult |  |
| Input | uiIndex | UINT | Index of the sms in the storage location |
| Output | sResultText | STRING |  |

## FuSms_list_get_element (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSms_list_get_element | WagoTypesModem.eResult |  |
| Input | uiIndex | UINT | Index of the element in the sms_list with meta information |
| Output | SMSMetaData | WagoTypesModem.typSmsMetaData |  |
| sResultText | STRING |  |

## FuSms_list_get_size (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuSms_list_get_size | WagoTypesModem.eResult |
| Output | uiSize | UINT |
| sResultText | STRING |

## FuSms_list_refresh (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuSms_list_refresh | WagoTypesModem.eResult |
| Output | sResultText | STRING |

Referesh the sms_list and get a new list from the modem

Interface variables Referesh the sms_list and get a new list from the modem

## FuSms_read_pdu (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSms_read_pdu | WagoTypesModem.eResult |  |
| Input | uiIndex | UINT | Index of the sms in the storage location |
| Output | PDU | typSmsMsgPDU |  |
| sResultText | STRING |  |

## FuSms_read_text (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSms_read_text | WagoTypesModem.eResult |  |
| Input | uiIndex | UINT | Index of the sms in the storage location |
| Output | sText | STRING(324) |  |
| sResultText | STRING |  |

## FuSms_send_pdu (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuSms_send_pdu | WagoTypesModem.eResult |
| Input | aData | ARRAY [0..256] OF BYTE |
| uiDataLength | UINT |
| Output | sResultText | STRING |

## FuSms_send_text (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuSms_send_text | WagoTypesModem.eResult |
| Input | sReceiverNumber | STRING(24) |
| sSMSCNumber | STRING(24) |
| sText | STRING(160) |
| Output | sResultText | STRING |

### Program Organization


## 20 Program Organization Units


- FuGet_modem_device_info (FUN) - FuGet_network_access_info (FUN) - FuGet_network_registration_settings (FUN) - FuGet_sim_info (FUN) - FuGet_wds_enable (FUN) - FuGet_wds_info (FUN) - FuGet_wds_settings (FUN) - FuNetscan_list_get_element (FUN) - FuNetscan_list_get_size (FUN) - FuNetscan_list_refresh (FUN) - FuReset_modem (FUN) - FuSet_network_registration_settings (FUN) - FuSet_sim_pin (FUN) - FuSet_sim_puk (FUN) - FuSet_wds_enable (FUN) - FuSet_wds_settings (FUN) - FuSms_delete (FUN) - FuSms_list_get_element (FUN) - FuSms_list_get_size (FUN) - FuSms_list_refresh (FUN) - FuSms_read_pdu (FUN) - FuSms_read_text (FUN) - FuSms_send_pdu (FUN) - FuSms_send_text (FUN)

### Internal Components


## WagoSysModem_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysModem_Internal_PFC |
| Version: | 1.1.4.0 |
| Categories: | WAGO Internal\|Common; WAGO Internal\|Feature\|Common; WAGO Internal\|Feature\|Network; WAGO Internal\|Target\|PFC |
| Namespace: | WagoSysModemInternal |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysModemInternal |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

This is an external library to make the functions of the modem available

The function blocks of this library are NOT thread safe and must be called from one CODESYS task only! Concurrent calls from different tasks may cause loss or corruption of data. [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. This is an external library to make the functions of the modem available The function blocks of this library are NOT thread safe and must be called from one CODESYS task only! Concurrent calls from different tasks may cause loss or corruption of data. [1]

### Contents:


- 20 Program Organization Units FuGet_modem_device_info (FUN) - FuGet_network_access_info (FUN) - FuGet_network_registration_settings (FUN) - FuGet_sim_info (FUN) - FuGet_wds_enable (FUN) - FuGet_wds_info (FUN) - FuGet_wds_settings (FUN) - FuNetscan_list_get_element (FUN) - FuNetscan_list_get_size (FUN) - FuNetscan_list_refresh (FUN) - FuReset_modem (FUN) - FuSet_network_registration_settings (FUN) - FuSet_sim_pin (FUN) - FuSet_sim_puk (FUN) - FuSet_wds_enable (FUN) - FuSet_wds_settings (FUN) - FuSms_delete (FUN) - FuSms_list_get_element (FUN) - FuSms_list_get_size (FUN) - FuSms_list_refresh (FUN) - FuSms_read_pdu (FUN) - FuSms_read_text (FUN) - FuSms_send_pdu (FUN) - FuSms_send_text (FUN) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysModem_Internal_PFC.library, last modified 25.05.2021, 16:33:11. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## VersionHistory (GVL)


| Date | Version | Author | Change |
| 07.01.2021 | 1.1.4.0 | WAGO / u0100179 | Add new functions for network scan handling |
| 02.12.2020 | 1.1.3.0 | WAGO / u013972 | Add new functions for network registration settings |
| 30.10.2020 | 1.1.2.0 | WAGO / u013972 | Add new functions for sms handling |
| 18.08.2020 | 1.1.0.0 | WAGO / u013972 | Move eResult to WagoTypesModem |
| 12.08.2020 | 1.0.1.0 | WAGO / u013972 | Add reset function |
| 24.07.2020 | 1.0.0.0 | WAGO / u013972 | Release Version |

WagoSysModem_Internal_PFC

WagoSysModem_Internal_PFC