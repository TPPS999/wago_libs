# WagoTypesCurl v1.1.2.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesCurl
- **Version:** 1.1.2.1
- **Categories:** WAGO FunctionalView|Base; WAGO LayerView|Types and Interfaces; WAGO Internal|Target|PFC; Application
- **Author:** WAGO / u013972
- **Placeholder:** WagoTypesCurl

### Description ¶


This document is automatically generated.

Type Definitions for SysCurl

This document is automatically generated. Type Definitions for SysCurl

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Functions - Methods - Global Variable Lists GVL (GVL) - Status (GVL) Other Components - 22 Ftp - 23 SSL - 24 SSH - 29 Other - eCurlCode (ENUM) - eCurlFtpCreateMissingDirs (ENUM) - eCurlFtpMethod (ENUM) - eCurlFtpSslAuth (ENUM) - eCurlFtpSslCCC (ENUM) - eCurlOptions_BOOL (ENUM) - ... and 8 more

### Indices and tables ¶


Based on WagoTypesCurl.library, last modified 29.05.2024, 20:39:35. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesCurl.library, last modified 29.05.2024, 20:39:35. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesCurl Library Documentation


| Company: | WAGO |
| Title: | WagoTypesCurl |
| Version: | 1.1.2.1 |
| Categories: | WAGO FunctionalView\|Base; WAGO LayerView\|Types and Interfaces; WAGO Internal\|Target\|PFC; Application |
| Author: | WAGO / u013972 |
| Placeholder: | WagoTypesCurl |

### Description


This document is automatically generated.

Type Definitions for SysCurl

This document is automatically generated. Type Definitions for SysCurl

### Contents:


- 21 curl_easy_setopt eCurlOptions_BOOL (ENUM) - eCurlOptions_DINT (ENUM) - eCurlOptions_STRING (ENUM) - eCurlOptions_slist (ENUM) 22 Ftp - eCurlFtpCreateMissingDirs (ENUM) - eCurlFtpMethod (ENUM) - eCurlFtpSslAuth (ENUM) - eCurlFtpSslCCC (ENUM) 23 SSL - eCurlUseSsl (ENUM) - typSSL_Options (STRUCT) 24 SSH - typSSH_Options (STRUCT) 29 Other - eCurlCode (ENUM) - eCurlProxyType (ENUM) - eCurlTimeCondition (ENUM) FuGetVersionHistory (FUN) GVL (GVL) Status (GVL)

### Indices and tables


Based on WagoTypesCurl.library, last modified 29.05.2024, 20:39:35. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesCurl.library, last modified 29.05.2024, 20:39:35. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesCurl.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:39:36 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:39:35 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesCurl |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesCurl |
| DefaultNamespace |  |
| Version | version | 1.1.2.1 |
| Title | string | WagoTypesCurl |
| LibraryCategories | library-category-list | WAGO FunctionalView\|Base; WAGO LayerView\|Types and Interfaces; WAGO Internal\|Target\|PFC; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 28.02.2024 | 1.1.2.1 | u010663 | Compiled SP16.3 |
| 08.01.2019 | 1.1.2.0 | u015842 | Properties: free placeholder added |
| 06.03.2016 | 1.1.1.1 | WAGO / u013972 | Add category Applicantion |
| 29.11.2016 | 1.1.1.0 | WAGO / u013972 | Add typSSH_Options |
| 25.10.2016 | 1.1.0.0 | WAGO / u013972 | Rename eCurlFtpSslAuth and add eCurlUseSsl |
| 16.11.2016 | 1.0.0.6 | WAGO / u013972 | Change the value of CURLOPT_PORT in eCurlOptions_DINT |
| 15.11.2016 | 1.0.0.5 | WAGO / u013773 | typSSL_Options: Documentation updated |
| 06.10.2016 | 1.0.0.4 | WAGO / u013773 | typSSL_Options: Set xVerifyPeer and xVerifyHost to TRUE |
| 28.09.2016 | 1.0.0.3 | WAGO / u013773 | typSSL_Options added |
| 26.02.2016 | 1.0.0.2 | WAGO / u010663 | WagoSysVersion eliminated |
| 16.02.2016 | 1.0.0.1 | WAGO / u010663 | GVL Status added |
| 07.07.2015 | 1.0.0.0 | WAGO / u013972 | Release Version |

WagoTypesCurl

Interface variables WagoTypesCurl

### Methods


## 21 curl_easy_setopt


- eCurlOptions_BOOL (ENUM) - eCurlOptions_DINT (ENUM) - eCurlOptions_STRING (ENUM) - eCurlOptions_slist (ENUM)

### Global Variable Lists


## GVL (GVL)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | CURL_NULL | STRING(6) | ‘ NULL$N’ |

## Status (GVL)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | STATUS_CURL | ARRAY [0..100] OF WagoTypesErrorBase.typResultItem | [STRUCT(ID := CURLE_OK, Severity := WagoTypesErrorBase.eSeverity.none, Text := ‘OK’), STRUCT(ID := CURLE_UNSUPPORTED_PROTOCOL, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Protocol not supported ‘), STRUCT(ID := CURLE_FAILED_INIT, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Initialisation failed, internal curl error’), STRUCT(ID := CURLE_URL_MALFORMAT, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘URL not correct fomatted’), STRUCT(ID := CURLE_NOT_BUILT_IN, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Feature not build in this curl implementation’), STRUCT(ID := CURLE_COULDNT_RESOLVE_PROXY, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Couldn not resolve proxy. The given proxy host could NOT be resolved’), STRUCT(ID := CURLE_COULDNT_RESOLVE_HOST, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Couldn not resolve host. The given remote host was not resolved’), STRUCT(ID := CURLE_COULDNT_CONNECT, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Failed to connect() to host or proxy.’), STRUCT(ID := CURLE_FTP_WEIRD_SERVER_REPLY, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘FTP server response unexpected’), STRUCT(ID := CURLE_REMOTE_ACCESS_DENIED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Access denied to the resource given in the URL’), STRUCT(ID := CURLE_FTP_ACCEPT_FAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘FTP accept command failed’), STRUCT(ID := CURLE_FTP_WEIRD_PASS_REPLY, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘After having sent the FTP password to the server unexpected response received’), STRUCT(ID := CURLE_FTP_ACCEPT_TIMEOUT, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘FTP timeout while accept state’), STRUCT(ID := CURLE_FTP_WEIRD_PASV_REPLY, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘FTP server response unexpected ‘), STRUCT(ID := CURLE_FTP_WEIRD_227_FORMAT, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘FTP response error 227-line parsing’), STRUCT(ID := CURLE_FTP_CANT_GET_HOST, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘FTP failure looking up the host’), STRUCT(ID := CURLE_HTTP2, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘A problem was detected in the HTTP2 framing layer’), STRUCT(ID := CURLE_FTP_COULDNT_SET_TYPE, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Received an error when trying to set the transfer mode to binary or ASCII’), STRUCT(ID := CURLE_PARTIAL_FILE, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘A file transfer was shorter or larger than expected’), STRUCT(ID := CURLE_FTP_COULDNT_RETR_FILE, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘This was either a weird reply to a RETR command or a zero byte transfer complete’), STRUCT(ID := CURLE_QUOTE_ERROR, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Server returned an error code that was 400 or higher’), STRUCT(ID := CURLE_HTTP_RETURNED_ERROR, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘CURLOPT_FAILONERROR is TRUE and HTTP server returns an error code that is >= 400’), STRUCT(ID := CURLE_WRITE_ERROR, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘An error occurred when writing received data to a local file’), STRUCT(ID := CURLE_UPLOAD_FAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Failed starting the upload’), STRUCT(ID := CURLE_READ_ERROR, Severity := WagoTypesErrorBase.eSeverity.none, Text := ‘There was a problem reading a local file’), STRUCT(ID := CURLE_OUT_OF_MEMORY, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘A memory allocation request failed ‘), STRUCT(ID := CURLE_OPERATION_TIMEDOUT, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Operation timeout’), STRUCT(ID := CURLE_FTP_PORT_FAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘The FTP PORT command returned error’), STRUCT(ID := CURLE_FTP_COULDNT_USE_REST, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘The FTP REST command returned error’), STRUCT(ID := CURLE_RANGE_ERROR, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘The server does not support or accept range requests’), STRUCT(ID := CURLE_HTTP_POST_ERROR, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘This is an odd error that mainly occurs due to internal confusion’), STRUCT(ID := CURLE_SSL_CONNECT_ERROR, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘A problem occurred somewhere in the SSL/TLS handshake’), STRUCT(ID := CURLE_BAD_DOWNLOAD_RESUME, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Download could not be resumed because the offset was out of the file boundary’), STRUCT(ID := CURLE_FILE_COULDNT_READ_FILE, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘A file given with FILE:// could not be opened’), STRUCT(ID := CURLE_LDAP_CANNOT_BIND, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘LDAP cannot bind. LDAP bind operation failed’), STRUCT(ID := CURLE_LDAP_SEARCH_FAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘LDAP search failed’), STRUCT(ID := CURLE_FUNCTION_NOT_FOUND, Severity := WagoTypesErrorBase.eSeverity.none, Text := ‘Function not found. A required lib function was not found’), STRUCT(ID := CURLE_ABORTED_BY_CALLBACK, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Aborted by callback. A callback returned “abort” to libcurl ‘), STRUCT(ID := CURLE_BAD_FUNCTION_ARGUMENT, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Internal error. A function was called with a bad parameter’), STRUCT(ID := CURLE_INTERFACE_FAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Interface error’), STRUCT(ID := CURLE_TOO_MANY_REDIRECTS, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Too many redirects’), STRUCT(ID := CURLE_UNKNOWN_OPTION, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘An option passed to libcurl is not recognized/known’), STRUCT(ID := CURLE_TELNET_OPTION_SYNTAX, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘A telnet option string was Illegally formatted’), STRUCT(ID := CURLE_PEER_FAILED_VERIFICATION, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘The remote servers SSL certificate OR SSH md5 fingerprint was deemed NOT OK’), STRUCT(ID := CURLE_GOT_NOTHING, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Nothing was returned from the server’), STRUCT(ID := CURLE_SSL_ENGINE_NOTFOUND, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘The specified crypto engine was not found’), STRUCT(ID := CURLE_SSL_ENGINE_SETFAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Failed setting the selected SSL crypto engine as default’), STRUCT(ID := CURLE_SEND_ERROR, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Failed sending network data’), STRUCT(ID := CURLE_RECV_ERROR, Severity := WagoTypesErrorBase.eSeverity.none, Text := ‘Failure with receiving network data’), STRUCT(ID := CURLE_SSL_CERTPROBLEM, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Problem with the local client certificate ‘), STRUCT(ID := CURLE_SSL_CIPHER, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Could not use specified cipher’), STRUCT(ID := CURLE_SSL_CACERT, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Peer certificate cannot be authenticated with known CA certificates’), STRUCT(ID := CURLE_BAD_CONTENT_ENCODING, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Unrecognized transfer encoding’), STRUCT(ID := CURLE_LDAP_INVALID_URL, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Invalid LDAP URL’), STRUCT(ID := CURLE_FILESIZE_EXCEEDED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Maximum file size exceeded’), STRUCT(ID := CURLE_USE_SSL_FAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Requested FTP SSL level failed’), STRUCT(ID := CURLE_SEND_FAIL_REWIND, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘rewind the data to retransmit, but the rewinding operation failed’), STRUCT(ID := CURLE_SSL_ENGINE_INITFAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Initiating the SSL Engine failed’), STRUCT(ID := CURLE_LOGIN_DENIED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘The remote server denied curl to login’), STRUCT(ID := CURLE_TFTP_NOTFOUND, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘File not found on TFTP server’), STRUCT(ID := CURLE_TFTP_PERM, Severity := WagoTypesErrorBase.eSeverity.none, Text := ‘Permission problem on TFTP server’), STRUCT(ID := CURLE_REMOTE_DISK_FULL, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Out of disk space on the server’), STRUCT(ID := CURLE_TFTP_ILLEGAL, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Illegal TFTP operation’), STRUCT(ID := CURLE_TFTP_UNKNOWNID, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Unknown TFTP transfer ID’), STRUCT(ID := CURLE_REMOTE_FILE_EXISTS, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘File already exists and will not be overwritten’), STRUCT(ID := CURLE_TFTP_NOSUCHUSER, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘This error should never be returned by a properly functioning TFTP server’), STRUCT(ID := CURLE_CONV_FAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Character conversion failed’), STRUCT(ID := CURLE_CONV_REQD, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Caller must register conversion callbacks’), STRUCT(ID := CURLE_SSL_CACERT_BADFILE, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Problem with reading the SSL CA cert’), STRUCT(ID := CURLE_REMOTE_FILE_NOT_FOUND, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘The resource referenced in the URL does not exist’), STRUCT(ID := CURLE_SSH, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘An unspecified error occurred during the SSH session’), STRUCT(ID := CURLE_SSL_SHUTDOWN_FAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Failed to shut down the SSL connection’), STRUCT(ID := CURLE_AGAIN, Severity := WagoTypesErrorBase.eSeverity.none, Text := ‘Socket is not ready for send/recv wait till it is ready and try again’), STRUCT(ID := CURLE_SSL_CRL_BADFILE, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Failed to load CRL file ‘), STRUCT(ID := CURLE_SSL_ISSUER_ERROR, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Issuer check failed’), STRUCT(ID := CURLE_FTP_PRET_FAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘The FTP server does not understand the PRET command’), STRUCT(ID := CURLE_RTSP_CSEQ_ERROR, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Mismatch of RTSP CSeq numbers’), STRUCT(ID := CURLE_RTSP_SESSION_ERROR, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Mismatch of RTSP Session Identifiers’), STRUCT(ID := CURLE_FTP_BAD_FILE_LIST, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Unable to parse FTP file list’), STRUCT(ID := CURLE_CHUNK_FAILED, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘Chunk callback reported error’), STRUCT(ID := CURLE_NO_CONNECTION_AVAILABLE, Severity := WagoTypesErrorBase.eSeverity.error, Text := ‘No connection available, the session will be queued’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

### Other Components


## 22 Ftp


- eCurlFtpCreateMissingDirs (ENUM) - eCurlFtpMethod (ENUM) - eCurlFtpSslAuth (ENUM) - eCurlFtpSslCCC (ENUM)

## 23 SSL


- eCurlUseSsl (ENUM) - typSSL_Options (STRUCT)

## 24 SSH ¶


- typSSH_Options (STRUCT)

## 29 Other


- eCurlCode (ENUM) - eCurlProxyType (ENUM) - eCurlTimeCondition (ENUM)

## eCurlCode (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CURLE_OK | 0 | All fine. Proceed as usual. |
| CURLE_UNSUPPORTED_PROTOCOL | 1 | The URL you passed to libcurl used a protocol that this libcurl does not support. The support might be a compile- time option that you didn’t use, it can be a misspelled protocol string or just a protocol libcurl has no code for. |
| CURLE_FAILED_INIT | 2 | Very early initialization code failed. This is likely to be an internal error or problem, or a resource problem where something fundamental couldn’t get done at init time. |
| CURLE_URL_MALFORMAT | 3 | The URL was not properly formatted. |
| CURLE_NOT_BUILT_IN | 4 | A requested feature, protocol or option was not found built- in in this libcurl due to a build-time decision. This means that a feature or option was not enabled or explicitly disabled when libcurl was built and in order to get it to function you have to get a rebuilt libcurl. |
| CURLE_COULDNT_RESOLVE_PROXY | 5 | Couldn’t resolve proxy. The given proxy host could not be resolved. |
| CURLE_COULDNT_RESOLVE_HOST | 6 | Couldn’t resolve host. The given remote host was not resolved. |
| CURLE_COULDNT_CONNECT | 7 | Failed to connect() to host or proxy. |
| CURLE_FTP_WEIRD_SERVER_REPLY | 8 | After connecting to a FTP server, libcurl expects to get a certain reply back. This error code implies that it got a strange or bad reply. The given remote server is probably not an OK FTP server. |
| CURLE_REMOTE_ACCESS_DENIED | 9 | We were denied access to the resource given in the URL. For FTP, this occurs while trying to change to the remote directory. |
| CURLE_FTP_ACCEPT_FAILED | 10 | While waiting for the server to connect back when an active FTP session is used, an error code was sent over the control connection or similar. |
| CURLE_FTP_WEIRD_PASS_REPLY | 11 | After having sent the FTP password to the server, libcurl expects a proper reply. This error code indicates that an unexpected code was returned. |
| CURLE_FTP_ACCEPT_TIMEOUT | 12 | During an active FTP session while waiting for the server to connect, the CURLOPT_ACCEPTTIMEOUT_MS (or the internal default) timeout expired. |
| CURLE_FTP_WEIRD_PASV_REPLY | 13 | libcurl failed to get a sensible result back from the server as a response to either a PASV or a EPSV command. The server is flawed. |
| CURLE_FTP_WEIRD_227_FORMAT | 14 | FTP servers return a 227-line as a response to a PASV command. If libcurl fails to parse that line, this return code is passed back. |
| CURLE_FTP_CANT_GET_HOST | 15 | An internal failure to lookup the host used for the new connection. |
| CURLE_HTTP2 | 16 | A problem was detected in the HTTP2 framing layer. This is somewhat generic and can be one out of several problems, see the error buffer for details. |
| CURLE_FTP_COULDNT_SET_TYPE | 17 | Received an error when trying to set the transfer mode to binary or ASCII. |
| CURLE_PARTIAL_FILE | 18 | A file transfer was shorter or larger than expected. This happens when the server first reports an expected transfer size, and then delivers data that doesn’t match the previously given size. |
| CURLE_FTP_COULDNT_RETR_FILE | 19 | This was either a weird reply to a ‘RETR’ command or a zero byte transfer complete. |
| CURLE_QUOTE_ERROR | 21 | When sending custom “QUOTE” commands to the remote server, one of the commands returned an error code that was 400 or higher (for FTP) or otherwise indicated unsuccessful completion of the command. |
| CURLE_HTTP_RETURNED_ERROR | 22 | This is returned if CURLOPT_FAILONERROR is set TRUE and the HTTP server returns an error code that is >= 400. |
| CURLE_WRITE_ERROR | 23 | An error occurred when writing received data to a local file, or an error was returned to libcurl from a write callback. |
| CURLE_UPLOAD_FAILED | 25 | Failed starting the upload. For FTP, the server typically denied the STOR command. The error buffer usually contains the server’s explanation for this. |
| CURLE_READ_ERROR | 26 | There was a problem reading a local file or an error returned by the read callback. |
| CURLE_OUT_OF_MEMORY | 27 | A memory allocation request failed. This is serious badness and things are severely screwed up if this ever occurs. |
| CURLE_OPERATION_TIMEDOUT | 28 | Operation timeout. The specified time-out period was reached according to the conditions. |
| CURLE_FTP_PORT_FAILED | 30 | The FTP PORT command returned error. This mostly happens when you haven’t specified a good enough address for libcurl to use. See CURLOPT_FTPPORT. |
| CURLE_FTP_COULDNT_USE_REST | 31 | The FTP REST command returned error. This should never happen if the server is sane. |
| CURLE_RANGE_ERROR | 33 | The server does not support or accept range requests. |
| CURLE_HTTP_POST_ERROR | 34 | This is an odd error that mainly occurs due to internal confusion. |
| CURLE_SSL_CONNECT_ERROR | 35 | A problem occurred somewhere in the SSL/TLS handshake. You really want the error buffer and read the message there as it pinpoints the problem slightly more. Could be certificates (file formats, paths, permissions), passwords, and others. |
| CURLE_BAD_DOWNLOAD_RESUME | 36 | The download could not be resumed because the specified offset was out of the file boundary. |
| CURLE_FILE_COULDNT_READ_FILE | 37 | A file given with FILE:// couldn’t be opened. Most likely because the file path doesn’t identify an existing file. Did you check file permissions? |
| CURLE_LDAP_CANNOT_BIND | 38 | LDAP cannot bind. LDAP bind operation failed. |
| CURLE_LDAP_SEARCH_FAILED | 39 | LDAP search failed. |
| CURLE_FUNCTION_NOT_FOUND | 41 | Function not found. A required zlib function was not found. |
| CURLE_ABORTED_BY_CALLBACK | 42 | Aborted by callback. A callback returned “abort” to libcurl. |
| CURLE_BAD_FUNCTION_ARGUMENT | 43 | Internal error. A function was called with a bad parameter. |
| CURLE_INTERFACE_FAILED | 45 | Interface error. A specified outgoing interface could not be used. Set which interface to use for outgoing connections’ source IP address with CURLOPT_INTERFACE. |
| CURLE_TOO_MANY_REDIRECTS | 47 | Too many redirects. When following redirects, libcurl hit the maximum amount. Set your limit with CURLOPT_MAXREDIRS. |
| CURLE_UNKNOWN_OPTION | 48 | An option passed to libcurl is not recognized/known. Refer to the appropriate documentation. This is most likely a problem in the program that uses libcurl. The error buffer might contain more specific information about which exact option it concerns. |
| CURLE_TELNET_OPTION_SYNTAX | 49 | A telnet option string was Illegally formatted. |
| CURLE_PEER_FAILED_VERIFICATION | 51 | The remote server’s SSL certificate or SSH md5 fingerprint was deemed not OK. |
| CURLE_GOT_NOTHING | 52 | Nothing was returned from the server, and under the circumstances, getting nothing is considered an error. |
| CURLE_SSL_ENGINE_NOTFOUND | 53 | The specified crypto engine wasn’t found. |
| CURLE_SSL_ENGINE_SETFAILED | 54 | Failed setting the selected SSL crypto engine as default! |
| CURLE_SEND_ERROR | 55 | Failed sending network data. |
| CURLE_RECV_ERROR | 56 | Failure with receiving network data. |
| CURLE_SSL_CERTPROBLEM | 58 | problem with the local client certificate. |
| CURLE_SSL_CIPHER | 59 | Couldn’t use specified cipher. |
| CURLE_SSL_CACERT | 60 | Peer certificate cannot be authenticated with known CA certificates. |
| CURLE_BAD_CONTENT_ENCODING | 61 | Unrecognized transfer encoding. |
| CURLE_LDAP_INVALID_URL | 62 | Invalid LDAP URL. |
| CURLE_FILESIZE_EXCEEDED | 63 | Maximum file size exceeded. |
| CURLE_USE_SSL_FAILED | 64 | Requested FTP SSL level failed. |
| CURLE_SEND_FAIL_REWIND | 65 | When doing a send operation curl had to rewind the data to retransmit, but the rewinding operation failed. |
| CURLE_SSL_ENGINE_INITFAILED | 66 | Initiating the SSL Engine failed. |
| CURLE_LOGIN_DENIED | 67 | The remote server denied curl to login (Added in 7.13.1) |
| CURLE_TFTP_NOTFOUND | 68 | File not found on TFTP server. |
| CURLE_TFTP_PERM | 69 | Permission problem on TFTP server. |
| CURLE_REMOTE_DISK_FULL | 70 | Out of disk space on the server. |
| CURLE_TFTP_ILLEGAL | 71 | Illegal TFTP operation. |
| CURLE_TFTP_UNKNOWNID | 72 | Unknown TFTP transfer ID. |
| CURLE_REMOTE_FILE_EXISTS | 73 | File already exists and will not be overwritten. |
| CURLE_TFTP_NOSUCHUSER | 74 | This error should never be returned by a properly functioning TFTP server. |
| CURLE_CONV_FAILED | 75 | Character conversion failed. |
| CURLE_CONV_REQD | 76 | Caller must register conversion callbacks. |
| CURLE_SSL_CACERT_BADFILE | 77 | Problem with reading the SSL CA cert (path? access rights?) |
| CURLE_REMOTE_FILE_NOT_FOUND | 78 | The resource referenced in the URL does not exist. |
| CURLE_SSH | 79 | An unspecified error occurred during the SSH session. |
| CURLE_SSL_SHUTDOWN_FAILED | 80 | Failed to shut down the SSL connection. |
| CURLE_AGAIN | 81 | Socket is not ready for send/recv wait till it’s ready and try again. This return code is only returned from curl_easy_recv and curl_easy_send (Added in 7.18.2) |
| CURLE_SSL_CRL_BADFILE | 82 | Failed to load CRL file (Added in 7.19.0) |
| CURLE_SSL_ISSUER_ERROR | 83 | Issuer check failed (Added in 7.19.0) |
| CURLE_FTP_PRET_FAILED | 84 | The FTP server does not understand the PRET command at all or does not support the given argument. Be careful when using CURLOPT_CUSTOMREQUEST, a custom LIST command will be sent with PRET CMD before PASV as well. (Added in 7.20.0) |
| CURLE_RTSP_CSEQ_ERROR | 85 | Mismatch of RTSP CSeq numbers. |
| CURLE_RTSP_SESSION_ERROR | 86 | Mismatch of RTSP Session Identifiers. |
| CURLE_FTP_BAD_FILE_LIST | 87 | Unable to parse FTP file list (during FTP wildcard downloading). |
| CURLE_CHUNK_FAILED | 88 | Chunk callback reported error. |
| CURLE_NO_CONNECTION_AVAILABLE | 89 | (For internal use only, will never be returned by libcurl) No connection available, the session will be queued. (added in 7.30.0) |

## eCurlFtpCreateMissingDirs (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CURLFTP_CREATE_DIR_NONE | 0 | Kein Directory anlegen |
| CURLFTP_CREATE_DIR | 1 | Directories werden angelegt |
| CURLFTP_CREATE_DIR_RETRY | 2 | Falls das Anlegen eines Directories fehlschlägt, wird nochmals ein CWD versucht, ein anderer Client könnte das Verzeichnis schon angelegt haben. |

## eCurlFtpMethod (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CURLFTPMETHOD_MULTICWD | 1 | Die Standard-Methode: FüR jede Hierarchieebene wird ein CWD- Kommando abgesetzt. |
| CURLFTPMETHOD_NOCWD | 2 | libcurl setzt überhaupt kein CWD-Kommando ab |
| CURLFTPMETHOD_SINGLECWD | 3 | libcurl setzt ein CWD-Kommando füR den ganzen Pfad ab |

## eCurlFtpSslAuth (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CURLFTPAUTH_DEFAULT | 0 | libcurl bestimmt die Methode |
| CURLFTPAUTH_SSL | 1 | SSL-Authentifizierung benutzen, nur wenn das fehlschläGT, TLS benutzen. |
| CURLFTPAUTH_TLS | 2 | TLS-Authentifizierung benutzen, nur wenn das fehlschläGT, SSL benutzen. |

## eCurlFtpSslCCC (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CURLFTPSSL_CCC_NONE | 0 | Default: kein SSL/TLS-Shutdown |
| CURLFTPSSL_CCC_PASSIVE | 1 | Warte auf den Server füR den SSL/TLS-Shutdown |
| CURLFTPSSL_CCC_ACTIVE | 2 | Client initiiert den SSL/TLS-Shutdown |

## eCurlOptions_BOOL (ENUM)


| Name | Initial |
| --- | --- |
| CURLOPT_CRLF | 27 |
| CURLOPT_VERBOSE | 41 |
| CURLOPT_HEADER | 42 |
| CURLOPT_NOPROGRESS | 43 |
| CURLOPT_NOBODY | 44 |
| CURLOPT_FAILONERROR | 45 |
| CURLOPT_UPLOAD | 46 |
| CURLOPT_POST | 47 |
| CURLOPT_DIRLISTONLY | 48 |
| CURLOPT_APPEND | 50 |
| CURLOPT_FOLLOWLOCATION | 52 |
| CURLOPT_TRANSFERTEXT | 53 |
| CURLOPT_PUT | 54 |
| CURLOPT_AUTOREFERER | 58 |
| CURLOPT_HTTPPROXYTUNNEL | 61 |
| CURLOPT_SSL_VERIFYPEER | 64 |
| CURLOPT_FILETIME | 69 |
| CURLOPT_FRESH_CONNECT | 74 |
| CURLOPT_FORBID_REUSE | 75 |
| CURLOPT_HTTPGET | 80 |
| CURLOPT_FTP_USE_EPSV | 85 |
| CURLOPT_DNS_USE_GLOBAL_CACHE | 91 |
| CURLOPT_COOKIESESSION | 96 |
| CURLOPT_NOSIGNAL | 99 |
| CURLOPT_UNRESTRICTED_AUTH | 105 |
| CURLOPT_FTP_USE_EPRT | 106 |
| CURLOPT_TCP_NODELAY | 121 |
| CURLOPT_IGNORE_CONTENT_LENGTH | 136 |
| CURLOPT_FTP_SKIP_PASV_IP | 137 |
| CURLOPT_CONNECT_ONLY | 141 |
| CURLOPT_SSL_SESSIONID_CACHE | 150 |
| CURLOPT_HTTP_TRANSFER_DECODING | 157 |
| CURLOPT_HTTP_CONTENT_DECODING | 158 |
| CURLOPT_PROXY_TRANSFER_MODE | 166 |
| CURLOPT_CERTINFO | 172 |
| CURLOPT_SOCKS5_GSSAPI_NEC | 180 |
| CURLOPT_FTP_USE_PRET | 188 |
| CURLOPT_WILDCARDMATCH | 197 |
| CURLOPT_TRANSFER_ENCODING | 207 |
| CURLOPT_TCP_KEEPALIVE | 213 |
| CURLOPT_SASL_IR | 218 |
| CURLOPT_SSL_VERIFYSTATUS | 232 |

## eCurlOptions_DINT (ENUM)


| Name | Initial |
| --- | --- |
| CURLOPT_PORT | 3 |
| CURLOPT_TIMEOUT | 13 |
| CURLOPT_INFILESIZE | 14 |
| CURLOPT_LOW_SPEED_LIMIT | 19 |
| CURLOPT_LOW_SPEED_TIME | 20 |
| CURLOPT_RESUME_FROM | 21 |
| CURLOPT_SSLVERSION | 32 |
| CURLOPT_TIMECONDITION | 33 |
| CURLOPT_TIMEVALUE | 34 |
| CURLOPT_NETRC | 51 |
| CURLOPT_PROXYPORT | 59 |
| CURLOPT_POSTFIELDSIZE | 60 |
| CURLOPT_MAXREDIRS | 68 |
| CURLOPT_MAXCONNECTS | 71 |
| CURLOPT_CONNECTTIMEOUT | 78 |
| CURLOPT_SSL_VERIFYHOST | 81 |
| CURLOPT_HTTP_VERSION | 84 |
| CURLOPT_SSLENGINE_DEFAULT | 90 |
| CURLOPT_DNS_CACHE_TIMEOUT | 92 |
| CURLOPT_BUFFERSIZE | 98 |
| CURLOPT_PROXYTYPE | 101 |
| CURLOPT_HTTPAUTH | 107 |
| CURLOPT_FTP_CREATE_MISSING_DIRS | 110 |
| CURLOPT_PROXYAUTH | 111 |
| CURLOPT_FTP_RESPONSE_TIMEOUT | 112 |
| CURLOPT_IPRESOLVE | 113 |
| CURLOPT_MAXFILESIZE | 114 |
| CURLOPT_USE_SSL | 119 |
| CURLOPT_FTPSSLAUTH | 129 |
| CURLOPT_FTP_FILEMETHOD | 138 |
| CURLOPT_LOCALPORT | 139 |
| CURLOPT_LOCALPORTRANGE | 140 |
| CURLOPT_SSH_AUTH_TYPES | 151 |
| CURLOPT_FTP_SSL_CCC | 154 |
| CURLOPT_TIMEOUT_MS | 155 |
| CURLOPT_CONNECTTIMEOUT_MS | 156 |
| CURLOPT_NEW_FILE_PERMS | 159 |
| CURLOPT_NEW_DIRECTORY_PERMS | 160 |
| CURLOPT_POSTREDIR | 161 |
| CURLOPT_ADDRESS_SCOPE | 171 |
| CURLOPT_TFTP_BLKSIZE | 178 |
| CURLOPT_PROTOCOLS | 181 |
| CURLOPT_REDIR_PROTOCOLS | 182 |
| CURLOPT_RTSP_REQUEST | 189 |
| CURLOPT_RTSP_CLIENT_CSEQ | 193 |
| CURLOPT_RTSP_SERVER_CSEQ | 194 |
| CURLOPT_GSSAPI_DELEGATION | 210 |
| CURLOPT_ACCEPTTIMEOUT_MS | 212 |
| CURLOPT_TCP_KEEPIDLE | 214 |
| CURLOPT_TCP_KEEPINTVL | 215 |
| CURLOPT_SSL_OPTIONS | 216 |
| CURLOPT_SSL_ENABLE_NPN | 225 |
| CURLOPT_SSL_ENABLE_ALPN | 226 |
| CURLOPT_EXPECT_100_TIMEOUT_MS | 227 |
| CURLOPT_HEADEROPT | 229 |
| CURLOPT_TLSAUTH_TYPE | 10206 |
| CURLOPT_INFILESIZE_LARGE | 30115 |
| CURLOPT_RESUME_FROM_LARGE | 30116 |
| CURLOPT_MAXFILESIZE_LARGE | 30117 |
| CURLOPT_POSTFIELDSIZE_LARGE | 30120 |
| CURLOPT_MAX_SEND_SPEED_LARGE | 30145 |
| CURLOPT_MAX_RECV_SPEED_LARGE | 30146 |

## eCurlOptions_STRING (ENUM)


| Name | Initial |
| --- | --- |
| CURLOPT_URL | 10002 |
| CURLOPT_USERPWD | 10005 |
| CURLOPT_PROXYUSERPWD | 10006 |
| CURLOPT_PROXY | 10004 |
| CURLOPT_REFERER | 10016 |
| CURLOPT_RANGE | 10007 |
| CURLOPT_POSTFIELDS | 10015 |
| CURLOPT_FTPPORT | 10017 |
| CURLOPT_USERAGENT | 10018 |
| CURLOPT_COOKIE | 10022 |
| CURLOPT_SSLCERT | 10025 |
| CURLOPT_KEYPASSWD | 10026 |
| CURLOPT_KRBLEVEL | 10063 |
| CURLOPT_CAINFO | 10065 |
| CURLOPT_RANDOM_FILE | 10076 |
| CURLOPT_EGDSOCKET | 10077 |
| CURLOPT_SSL_CIPHER_LIST | 10083 |
| CURLOPT_SSLCERTTYPE | 10086 |
| CURLOPT_SSLKEY | 10087 |
| CURLOPT_SSLKEYTYPE | 10088 |
| CURLOPT_SSLENGINE | 10089 |
| CURLOPT_COOKIEFILE | 10031 |
| CURLOPT_CUSTOMREQUEST | 10036 |
| CURLOPT_INTERFACE | 10062 |
| CURLOPT_COOKIEJAR | 10082 |
| CURLOPT_CAPATH | 10097 |
| CURLOPT_ACCEPT_ENCODING | 10102 |
| CURLOPT_NETRC_FILE | 10118 |
| CURLOPT_FTP_ACCOUNT | 10134 |
| CURLOPT_COOKIELIST | 10135 |
| CURLOPT_FTP_ALTERNATIVE_TO_USER | 10147 |
| CURLOPT_SSH_PUBLIC_KEYFILE | 10152 |
| CURLOPT_SSH_PRIVATE_KEYFILE | 10153 |
| CURLOPT_SSH_HOST_PUBLIC_KEY_MD5 | 10162 |
| CURLOPT_COPYPOSTFIELDS | 10165 |
| CURLOPT_CRLFILE | 10169 |
| CURLOPT_ISSUERCERT | 10170 |
| CURLOPT_USERNAME | 10173 |
| CURLOPT_PASSWORD | 10174 |
| CURLOPT_PROXYUSERNAME | 10175 |
| CURLOPT_PROXYPASSWORD | 10176 |
| CURLOPT_NOPROXY | 10177 |
| CURLOPT_SOCKS5_GSSAPI_SERVICE | 10179 |
| CURLOPT_SSH_KNOWNHOSTS | 10183 |
| CURLOPT_MAIL_FROM | 10186 |
| CURLOPT_RTSP_SESSION_ID | 10190 |
| CURLOPT_RTSP_STREAM_URI | 10191 |
| CURLOPT_RTSP_TRANSPORT | 10192 |
| CURLOPT_TLSAUTH_USERNAME | 10204 |
| CURLOPT_TLSAUTH_PASSWORD | 10205 |
| CURLOPT_DNS_SERVERS | 10211 |
| CURLOPT_MAIL_AUTH | 10217 |
| CURLOPT_XOAUTH2_BEARER | 10220 |
| CURLOPT_DNS_INTERFACE | 10221 |
| CURLOPT_DNS_LOCAL_IP4 | 10222 |
| CURLOPT_DNS_LOCAL_IP6 | 10223 |
| CURLOPT_UNIX_SOCKET_PATH | 10231 |
| CURLOPT_LOGIN_OPTIONS | 10224 |
| CURLOPT_PINNEDPUBLICKEY | 10230 |

## eCurlOptions_slist (ENUM)


| Name | Initial |
| --- | --- |
| CURLOPT_HTTPHEADER | 10023 |
| CURLOPT_QUOTE | 10028 |
| CURLOPT_POSTQUOTE | 10039 |
| CURLOPT_PREQUOTE | 10093 |
| CURLOPT_TELNETOPTIONS | 10070 |
| CURLOPT_HTTP200ALIASES | 10104 |
| CURLOPT_MAIL_RCPT | 10187 |
| CURLOPT_RESOLVE | 10203 |
| CURLOPT_PROXYHEADER | 10228 |

## eCurlProxyType (ENUM)


| Name | Initial |
| --- | --- |
| CURLPROXY_HTTP | 0 |
| CURLPROXY_HTTP_1_0 | 1 |
| CURLPROXY_SOCKS4 | 4 |
| CURLPROXY_SOCKS5 | 5 |
| CURLPROXY_SOCKS4A | 6 |
| CURLPROXY_SOCKS5_HOSTNAME | 7 |

## eCurlTimeCondition (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CURL_TIMECOND_NONE | 0 |  |
| CURL_TIMECOND_IFMODSINCE | 1 | File nur übertragen, wenn es nach TIMEVALUE modifiziert wurde |
| CURL_TIMECOND_IFUNMODSINCE | 2 | File nur übertragen, wenn es nach TIMEVALUE nicht modifiziert wurde |

## eCurlUseSsl (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CURLUSESSL_NONE | 0 | Don’t attempt to use SSL. |
| CURLUSESSL_TRY | 1 | Try using SSL, proceed as normal otherwise. |
| CURLUSESSL_CONTROL | 2 | Require SSL for the control connection or fail with CURLE_USE_SSL_FAILED. |
| CURLUSESSL_ALL | 3 | Require SSL for all communication or fail with CURLE_USE_SSL_FAILED. |

## typSSH_Options (STRUCT)


| Name | Type | Initial | Comment |
| --- | --- | --- | --- |
| xAuthPassword | BOOL | TRUE | Authentication with Password |
| xAuthKey | BOOL |  | Authentication with Public Key File |
| sPrivateKey | STRING(255) |  | Path to the Private Key File of the client. Example: /root/.ssh/id_dsa |
| sPassphrase | STRING(255) |  | Passphrase for the Private Key |
| xAuthHost | BOOL |  | Accept only connections with a Host form the known host file |
| sKnownHosts | STRING(255) |  | Path to the the known host file to use. The known hosts file should use the OpenSSH file format as supported by libssh2. |

## typSSL_Options (STRUCT)


| Name | Type | Initial | Comment |
| --- | --- | --- | --- |
| sCA_Cert | STRING |  | This options tells to use the specified certificate file to verify the server. The file may contain multiple CA certificates. The certificate(s) must be in PEM format. Example: /etc/certificates/mycerts.pem If this parameter is not set, the Mozilla CA certificate store is used which is a part of the controller firmware! |
| sCA_Path | STRING |  | This option tells to use the specified certificate directory to verify the server. Multiple paths can be provided by separating them with ”:” (e.g. “path1:path2:path3”). The certificates must be in PEM format and the directory must have been processed using the c_rehash utility supplied with OpenSSL. |
| xVerifyPeer | BOOL | TRUE | Determines whether the authenticity of the certificate send from the server is verified. During the SSL handshake the certificate send from the server will be checked against the certificates provided with sCA_Certificate or sCA_Path . TRUE : Authenticity of the certificate is verified FALSE: Authenticity of the certificate is NOT verified |
| xVerifyHost | BOOL | TRUE | Determines whether the common name in the server certificate must match the server name you are connecting to. TRUE : The certificate must indicate that the server is the server to which you meant to connect or the connection fails FALSE: The connection succeeds regardless of the names in the certificate. Use that ability with caution! |
| sClientCert | STRING |  | Set SSL client certificate which is send to the server if it asks for it. The file must be provided in PEM format. Example: /etc/certificates/mycerts.pem |
| sClientCert_Key | STRING |  | Specifies private keyfile for SSL client cerificate. The file must be provided in PEM format. Example: /etc/certificates/mycerts.pem |
| sClientCert_KeyPasswd | STRING |  | Set password for private keyfile that is associated with SSL client cerificate sClientCert_Key |

```
//---------------------------------------------------------------------------------------
//---Set SSL Options---------------------------------------------------------------------
//---------------------------------------------------------------------------------------

//CURLOPT_CAPATH - specify directory holding CA certificates
IF LEN(typSSL_Options.sCA_Path) > 0 THEN
    _oCurl.curl_easy_setopt_STRING(eCurlOption:= WagoTypesCurl.eCurlOptions_STRING.CURLOPT_CAPATH, sParameter:= typSSL_Options.sCA_Path);
END_IF

//CURLOPT_CAINFO - path to Certificate Authority (CA) bundle
IF LEN(typSSL_Options.sCA_Cert) > 0 THEN
    _oCurl.curl_easy_setopt_STRING(eCurlOption:= WagoTypesCurl.eCurlOptions_STRING.CURLOPT_CAINFO, sParameter:= typSSL_Options.sCA_Cert);
END_IF

//CURLOPT_SSL_VERIFYHOST - verify the certificate's name against host
// 2 =  The ertificate must indicate that the server is the server to which you meant to connect or the connection fails
// 0 =  The connection succeeds regardless of the names in the certificate. Use that ability with caution
IF typSSL_Options.xVerifyHost THEN
    _oCurl.curl_easy_setopt_DINT(eCurlOption:= WagoTypesCurl.eCurlOptions_DINT.CURLOPT_SSL_VERIFYHOST, diParameter:= 2);
ELSE
    _oCurl.curl_easy_setopt_DINT(eCurlOption:= WagoTypesCurl.eCurlOptions_DINT.CURLOPT_SSL_VERIFYHOST, diParameter:= 0);
END_IF

//CURLOPT_SSL_VERIFYPEER - verify the peer's SSL certificate
_oCurl.curl_easy_setopt_BOOL(eCurlOption:= WagoTypesCurl.eCurlOptions_BOOL.CURLOPT_SSL_VERIFYPEER, xParameter:= typSSL_Options.xVerifyPeer);

//CURLOPT_SSLCERT - set SSL client certificate
IF LEN(typSSL_Options.sClientCert) > 0 THEN
    _oCurl.curl_easy_setopt_STRING(eCurlOption:= WagoTypesCurl.eCurlOptions_STRING.CURLOPT_SSLCERT, sParameter:= typSSL_Options.sClientCert);
END_IF

//CURLOPT_SSLKEY - specify private keyfile for TLS and SSL client cert
IF LEN(typSSL_Options.sClientCert_Key) > 0 THEN
    _oCurl.curl_easy_setopt_STRING(eCurlOption:= WagoTypesCurl.eCurlOptions_STRING.CURLOPT_SSLKEY, sParameter:= typSSL_Options.sClientCert_Key);
END_IF

//CURLOPT_KEYPASSWD - set passphrase to private key
IF LEN(typSSL_Options.sClientCert_KeyPasswd) > 0  THEN
    _oCurl.curl_easy_setopt_STRING(eCurlOption:= WagoTypesCurl.eCurlOptions_STRING.CURLOPT_KEYPASSWD, sParameter:= typSSL_Options.sClientCert_KeyPasswd);
END_IF
```

Example for the usage of typSSL_Options:

InOut: Example for the usage of typSSL_Options: