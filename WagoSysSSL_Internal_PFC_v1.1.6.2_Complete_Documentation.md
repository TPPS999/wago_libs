# WagoSysSSL_Internal_PFC v1.1.6.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysSSL_Internal_PFC
- **Version:** 1.1.6.2
- **Categories:** WAGO Internal|Target|PFC; WAGO Internal|Feature|Network
- **Namespace:** WagoSysSSLInternal
- **Author:** WAGO / u010956
- **Placeholder:** WagoSysSSLInternal

### Description ¶


This document is automatically generated.

This document is automatically generated.

### Contents: ¶


Contents: - Project Information - Library Information - Function Blocks FbSSL_CTX_Internal (FB) - FbSSL_Sock_Internal (FB) Functions - X509_free_Internal (FUN) - X509_verify_param_set1_host_Internal (FUN) - X509_verify_param_set_flags_Internal (FUN) - X509_verify_param_set_hostflags_Internal (FUN) - eSSL_X509_V_RTS_TO_eSSL_X509_V (FUN) Methods - FbSSL_CTX_Internal.load_revocation_list (METH) - FbSSL_CTX_Internal.load_verfiy_locations (METH) - FbSSL_CTX_Internal.sess_set_cache_size (METH) - FbSSL_CTX_Internal.set_client_CA_list (METH) - FbSSL_CTX_Internal.set_method (METH) - FbSSL_CTX_Internal.set_verify (METH) - FbSSL_CTX_Internal.use_PrivateKey_file (METH) - FbSSL_CTX_Internal.use_certificate_file (METH) - FbSSL_CTX_Internal.verify_depth (METH) - FbSSL_Sock_Internal.get0_param (METH) - ... and 9 more Program Organization Internal Components - 90 Internal - WagoSysSSL_Internal_PFC Library Documentation Global Variable Lists Other Components - 29 Types - eSSL_X509_V_RTS (ENUM)

### Indices and tables ¶


Based on WagoSysSSL_Internal_PFC.library, last modified 29.05.2024, 19:52:41. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysSSL_Internal_PFC.library, last modified 29.05.2024, 19:52:41. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysSSL_Internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:52:41 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:52:41 |
| Description | string |  |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u010956 |
| DefaultNamespace | WagoSysSSLInternal |
| LanguageModelAttribute | qualified-access-only |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysSSL_Internal_PFC |
| Released | bool | False |
| Version | version | 1.1.6.2 |
| Title | string | WagoSysSSL_Internal_PFC |
| Placeholder | WagoSysSSLInternal |
| LibraryCategories | library-category-list | WAGO Internal\|Target\|PFC; WAGO Internal\|Feature\|Network |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |
| IsEndUserLibrary | bool | False |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesSSL Library Identification : Placeholder: WagoTypesSSL Default Resolution: WagoTypesSSL, * (WAGO) Namespace: WagoTypesSSL Library Properties :

### Function Blocks


## FbSSL_CTX_Internal (FB)


This function block contains the SSL_CTX (SSL Context).

Graphical Illustration

Graphical Interface of FbSSL_CTX_Internal

Function description

This function block contains the SSL_CTX (SSL Context), that’s the global context structure which is created by a server or client once per program life-time and which holds mainly default values for the SSL structures which are later created for the connections. The values of the SSL_CTX can be set with the different methods oh this funftion block.

Function This function block contains the SSL_CTX (SSL Context). Graphical Illustration ![Image](images/wagosysssl_internal_pfc_22974814.png) Graphical Interface of FbSSL_CTX_Internal Function description This function block contains the SSL_CTX (SSL Context), that’s the global context structure which is created by a server or client once per program life-time and which holds mainly default values for the SSL structures which are later created for the connections. The values of the SSL_CTX can be set with the different methods oh this funftion block. Example - FbSSL_CTX_Internal.load_revocation_list (METH) - FbSSL_CTX_Internal.load_verfiy_locations (METH) - FbSSL_CTX_Internal.sess_set_cache_size (METH) - FbSSL_CTX_Internal.set_client_CA_list (METH) - FbSSL_CTX_Internal.set_method (METH) - FbSSL_CTX_Internal.set_verify (METH) - FbSSL_CTX_Internal.use_PrivateKey_file (METH) - FbSSL_CTX_Internal.use_certificate_file (METH) - FbSSL_CTX_Internal.verify_depth (METH)

## FbSSL_Sock_Internal (FB)


This function block contains the the main SSL/TLS structure.

Graphical Illustration

Graphical Interface of FbSSL_Sock_Internal

Function description

This function block contains the the main SSL/TLS structure which is created by a server or client per established connection. This actually is the core structure in the SSL API. At run-time the application usually deals with this structure which has links to mostly all other structures. The methods of this function block allow differnt operations on the connection.

Function* This function block contains the the main SSL/TLS structure. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_25a18b51.png) Graphical Interface of FbSSL_Sock_Internal Function description This function block contains the the main SSL/TLS structure which is created by a server or client per established connection. This actually is the core structure in the SSL API. At run-time the application usually deals with this structure which has links to mostly all other structures. The methods of this function block allow differnt operations on the connection. Example - FbSSL_Sock_Internal.get0_param (METH) - FbSSL_Sock_Internal.get_error (METH) - FbSSL_Sock_Internal.get_peer_certificate (METH) - FbSSL_Sock_Internal.get_verify_result (METH) - FbSSL_Sock_Internal.handshake_accept (METH) - FbSSL_Sock_Internal.handshake_connect (METH) - FbSSL_Sock_Internal.load_client_CA_file (METH) - FbSSL_Sock_Internal.read (METH) - FbSSL_Sock_Internal.shutdown (METH) - FbSSL_Sock_Internal.write (METH)

### Functions


## X509_free_Internal (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | X509_free_Internal | UDINT |
| Input | hCertificate | WagoTypesSSL.typeSSL_X509 |

This function frees up the X509 structure.

Graphical Illustration

Graphical Interface of X509_free_Internal

Function description

This function frees up the X509 structure.

Interface variables Function* This function frees up the X509 structure. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_1153ba1d.png) Graphical Interface of X509_free_Internal Function description This function frees up the X509 structure.

## X509_verify_param_set1_host_Internal (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | X509_verify_param_set1_host_Internal | UDINT |
| Input | hParam | WagoTypesSSL.typeSSL_param |
| sServername | STRING(80) |

This function sets the expected DNS hostname to name clearing any previously specified host name or names.

Graphical Illustration

Graphical Interface of X509_verify_param_set1_host_Internal

Function description

This function sets the expected DNS hostname to name clearing any previously specified host name or names. If name is NULL, or empty the list of hostnames is cleared, and name checks are not performed on the peer certificate.

This function has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

Interface variables Function* This function sets the expected DNS hostname to name clearing any previously specified host name or names. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_4eccffd8.png) Graphical Interface of X509_verify_param_set1_host_Internal Function description This function sets the expected DNS hostname to name clearing any previously specified host name or names. If name is NULL, or empty the list of hostnames is cleared, and name checks are not performed on the peer certificate. This function has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

## X509_verify_param_set_flags_Internal (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | X509_verify_param_set_flags_Internal | UDINT |
| Input | hParam | WagoTypesSSL.typeSSL_param |
| eFlags | WagoTypesSSL.eSSL_X509_Verification |

This function sets the flags in param by oring it with flags.

Graphical Illustration

Graphical Interface of X509_verify_param_set_flags_Internal

Function description

This function sets the flags in param by oring it with flags.

This function has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

Interface variables Function* This function sets the flags in param by oring it with flags. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_bb8e0bf4.png) Graphical Interface of X509_verify_param_set_flags_Internal Function description This function sets the flags in param by oring it with flags. This function has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

## X509_verify_param_set_hostflags_Internal (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | X509_verify_param_set_hostflags_Internal | UDINT |
| Input | hParam | WagoTypesSSL.typeSSL_param |
| eFlags | WagoTypesSSL.eSSL_X509_Check |

This function sets sets the flags.

Graphical Illustration

Graphical Interface of X509_verify_param_set_hostflags_Internal

Function description

This function sets sets the flags.

This function has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

Interface variables Function* This function sets sets the flags. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_2c54f6eb.png) Graphical Interface of X509_verify_param_set_hostflags_Internal Function description This function sets sets the flags. This function has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

## eSSL_X509_V_RTS_TO_eSSL_X509_V (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | eSSL_X509_V_RTS_TO_eSSL_X509_V | WagoTypesSSL.eSSL_X509_V |
| Input | eX509_V_RTS | eSSL_X509_V_RTS |

### Methods


## FbSSL_CTX_Internal.load_revocation_list (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | load_revocation_list | DINT |  |
| Input | sFile | STRING | path and file name |

This method specifies the locations for ctx, at which a revocation list for verification purposes are located.

Graphical Illustration

Graphical Interface of FbSSL_CTX_Internal.load_revocation_list

Function description

A certificate revocation list provides a list of certificates that have been revoked. To specify more than one revocation list the function must be called repeatedly.

This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

Interface variables Function* This method specifies the locations for ctx, at which a revocation list for verification purposes are located. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_06675df9.png) Graphical Interface of FbSSL_CTX_Internal.load_revocation_list Function description A certificate revocation list provides a list of certificates that have been revoked. To specify more than one revocation list the function must be called repeatedly. This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

## FbSSL_CTX_Internal.load_verfiy_locations (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | load_verfiy_locations | UDINT |  |
| Input | sFile | STRING | path and file name |
| eSSL_FileType | WagoTypesSSL.eSSL_FileType | file type |

This method specifies the locations for ctx, at which CA certificates for verification purposes are located.

Graphical Illustration

Graphical Interface of FbSSL_CTX_Internal.load_verfiy_locations

Function description

This function loads the list of certificates that are automatically confirmed. This list is located in the file system and will be loaded by FbSSL_CTX at this time.

This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

Interface variables Function* This method specifies the locations for ctx, at which CA certificates for verification purposes are located. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_f0461aa1.png) Graphical Interface of FbSSL_CTX_Internal.load_verfiy_locations Function description This function loads the list of certificates that are automatically confirmed. This list is located in the file system and will be loaded by FbSSL_CTX at this time. This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

## FbSSL_CTX_Internal.sess_set_cache_size (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | sess_set_cache_size | UDINT |  |
| Input | udiCacheSize | UDINT | maximum number of internal sessions that will be held in the context cache |

This method manipulate session cache size.

Graphical Illustration

Graphical Interface of FbSSL_CTX_Internal.sess_set_cache_size

Function description

Sets the size of the internal session cache of context FbSSL_CTX to udiCacheSize.

A special case is the size 0, which is used for unlimited size.

This method returns the previously valid size.

Interface variables Function This method manipulate session cache size. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_0b88b82d.png) Graphical Interface of FbSSL_CTX_Internal.sess_set_cache_size Function description Sets the size of the internal session cache of context FbSSL_CTX to udiCacheSize. Note A special case is the size 0, which is used for unlimited size. This method returns the previously valid size.

## FbSSL_CTX_Internal.set_client_CA_list (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | set_client_CA_list | UDINT |  |
| Input | hStack | WagoTypesSSL.typSSL_Stack | handle of list returns by SSL_loadClinet_CA_file |

This methos sets the list of CAs sent to the client when requesting a client certificate for channel.

Graphical Illustration

Graphical Interface of FbSSL_CTX_Internal.set_client_CA_list

Function description

When a TLS/SSL server requests a client certificate, it sends a list of CAs, for which it will accept certificates, to the client.

This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

Interface variables Function This methos sets the list of CAs sent to the client when requesting a client certificate for channel. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_d3a31994.png) Graphical Interface of FbSSL_CTX_Internal.set_client_CA_list Function description When a TLS/SSL server requests a client certificate, it sends a list of CAs, for which it will accept certificates, to the client. This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

## FbSSL_CTX_Internal.set_method (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | set_method | UDINT |  |
| Input | eSSL_Method | WagoTypesSSL.eSSL_Method | method of SSL handling in this context |

This method sets the method of SSL handling.

Graphical Illustration

Graphical Interface of FbSSL_CTX_Internal.set_method

Function description

This method sets the method of SSL handling. Must be called first during using the FbSSL_CTX.

This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

Interface variables Function This method sets the method of SSL handling. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_fd5888c8.png) Graphical Interface of FbSSL_CTX_Internal.set_method Function description This method sets the method of SSL handling. Must be called first during using the FbSSL_CTX. This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 An unspecified error has occurred. ======= =====================================================================================

## FbSSL_CTX_Internal.set_verify (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | set_verify | UDINT |
| Input | eVerify | WagoTypesSSL.eSSL_Verify |

set_verify() sets the verification flags for ctx to be mode.

Interface variables set_verify() sets the verification flags for ctx to be mode.

## FbSSL_CTX_Internal.use_PrivateKey_file (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | use_PrivateKey_file | UDINT |  |
| Input | sFile | STRING | path and file name |
| eSSL_FileType | WagoTypesSSL.eSSL_FileType | key file type |

This method loads the list of private keys stored in the specified file.

Graphical Illustration

Graphical Interface of FbSSL_CTX_Internal.use_PrivateKey_file

Function description

Adds sFile as private key to FbSSL_CTX. If a certificate has already been set and the private does not belong to the certificate an error is returned. To change a certificate, private key pair the new certificate needs to be set with FbSSL_CTX.use_certificate_file() before setting the private key.

This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. other An unspecified error has occurred. ======= =====================================================================================

Interface variables Function This method loads the list of private keys stored in the specified file. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_a8fff52e.png) Graphical Interface of FbSSL_CTX_Internal.use_PrivateKey_file Function description Adds sFile as private key to FbSSL_CTX. If a certificate has already been set and the private does not belong to the certificate an error is returned. To change a certificate, private key pair the new certificate needs to be set with FbSSL_CTX.use_certificate_file() before setting the private key. This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. other An unspecified error has occurred. ======= =====================================================================================

## FbSSL_CTX_Internal.use_certificate_file (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | use_certificate_file | UDINT |  |
| Input | sFile | STRING | path and file name |
| eSSL_FileType | WagoTypesSSL.eSSL_FileType | certificate file type |

This method defines the file that contains the certificates during the verification process. The certificates are loaded at this time.

Graphical Illustration

Graphical Interface of FbSSL_CTX_Internal.use_certificate_file

Function description

Loads the first certificate stored in sFile into FbSSL_CTX. The formatting type of the certificate must be specified with eFileType.

This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. other An unspecified error has occurred. ======= =====================================================================================

Interface variables Function This method defines the file that contains the certificates during the verification process. The certificates are loaded at this time. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_8587f0cf.png) Graphical Interface of FbSSL_CTX_Internal.use_certificate_file Function description Loads the first certificate stored in sFile into FbSSL_CTX. The formatting type of the certificate must be specified with eFileType. This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. other An unspecified error has occurred. ======= =====================================================================================

## FbSSL_CTX_Internal.verify_depth (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | verify_depth | UDINT |
| Input | diDepth | DINT |

set the depth of accepte certification chain.

Interface variables set the depth of accepte certification chain.

## FbSSL_Sock_Internal.get0_param (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | get0_param | WagoTypesSSL.typeSSL_param |

## FbSSL_Sock_Internal.get_error (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | get_error | WagoTypesSSL.eSSL_Error |
| Input | diRetCode | DINT |

This method obtain result code for TLS/SSL I/O operation.

Graphical Illustration

Graphical Interface of FbSSL_Sock_Internal.get_error

Function description

This method returns a result code for a preceding call to handshake_connect(), handshake_accept(), read() or write() on ssl.

This method has the following return values:

Interface variables Function This method obtain result code for TLS/SSL I/O operation. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_795814cf.png) Graphical Interface of FbSSL_Sock_Internal.get_error Function description This method returns a result code for a preceding call to handshake_connect(), handshake_accept(), read() or write() on ssl. This method has the following return values: - eSSL_Error.SSL_ERROR_NONE Operation successfull finished. This result code is returned if and only if ret > 0. - eSSL_Error.SSL_ERROR_ZERO_RETURN The TLS/SSL connection has been closed. If the protocol version is SSL 3.0 or higher, this result code is returned only if a closure alert has occurred in the protocol, i.e. if the connection has been closed cleanly. Note that in this case SSL_ERROR_ZERO_RETURN does not necessarily indicate that the underlying transport has been closed. - eSSL_Error.SSL_ERROR_WANT_READ / eSSL_Error.SSL_ERROR_WANT_WRITE The operation did not complete; the same TLS/SSL I/O function should be called again later. - eSSL_Error.SSL_ERROR_WANT_CONNECT / eSSL_Error.SSL_ERROR_WANT_ACCEPT The operation did not complete; the same TLS/SSL I/O function should be called again later. The underlying BIO was not connected yet to the peer and the call would block in connect()/accept(). The SSL function should be called again when the connection is established. - eSSL_Error.SSL_ERROR_WANT_X509_LOOKUP The operation did not complete; The TLS/SSL I/O function should be called again later. Details depend on the application. - eSSL_Error.SSL_ERROR_SYSCALL Some non-recoverable I/O error occurred. - eSSL_Error.SSL_ERROR_SSL A failure in the SSL library occurred, usually a protocol error.

## FbSSL_Sock_Internal.get_peer_certificate (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | get_peer_certificate | WagoTypesSSL.typeSSL_X509 |

## FbSSL_Sock_Internal.get_verify_result (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | get_verify_result | WagoTypesSSL.eSSL_X509_V |

## FbSSL_Sock_Internal.handshake_accept (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | handshake_accept | DINT |  |
| Input | hSysSock | SysTypes.RTS_IEC_HANDLE | Handle of SysSocket |
| pFbSSL_CTX | POINTER TO FbSSL_CTX_Internal | Handle of SSL channel |

This method wait for a TLS/SSL client to initiate a TLS/SSL handshake.

Graphical Illustration

Graphical Interface of FbSSL_Sock_Internal.handshake_accept

Function description

This method waits for a TLS/SSL client to initiate the TLS/SSL handshake. The communication channel must already have been set and assigned to the ssl by setting an underlying BIO.

The behaviour of FbSSL_Sock.handshake_accept() depends on the underlying BIO.

If the underlying BIO is blocking, FbSSL_Sock.handshake_accept() will only return once the handshake has been finished or an error occurred.

This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value.

This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 The TLS/SSL handshake was not successful but was shut down controlled and by the specifications of the TLS/SSL protocol. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. <0 The TLS/SSL handshake was not successful, because a fatal error occurred either at the protocol level or a connection failure occurred. The shutdown was not clean. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. ======= =====================================================================================

Interface variables Function This method wait for a TLS/SSL client to initiate a TLS/SSL handshake. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_8dbdd7dd.png) Graphical Interface of FbSSL_Sock_Internal.handshake_accept Function description This method waits for a TLS/SSL client to initiate the TLS/SSL handshake. The communication channel must already have been set and assigned to the ssl by setting an underlying BIO. The behaviour of FbSSL_Sock.handshake_accept() depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.handshake_accept() will only return once the handshake has been finished or an error occurred. Note This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value. This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 The TLS/SSL handshake was not successful but was shut down controlled and by the specifications of the TLS/SSL protocol. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. <0 The TLS/SSL handshake was not successful, because a fatal error occurred either at the protocol level or a connection failure occurred. The shutdown was not clean. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. ======= =====================================================================================

## FbSSL_Sock_Internal.handshake_connect (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | handshake_connect | DINT |  |
| Input | hSysSock | SysTypes.RTS_IEC_HANDLE | Handle of SysSocket |
| pFbSSL_CTX | POINTER TO FbSSL_CTX_Internal | Handle of SSL channel |

This method initiate the TLS/SSL handshake with an TLS/SSL server.

Graphical Illustration

Graphical Interface of FbSSL_Sock_Internal.handshake_connect

Function description

This method initiates the TLS/SSL handshake with a server. The communication channel must already have been set and assigned to the ssl by setting an underlying BIO.

The behaviour of FbSSL_Sock.handshake_connect() depends on the underlying BIO.

If the underlying BIO is blocking, FbSSL_Sock.handshake_connect() will only return once the handshake has been finished or an error occurred.

This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value.

This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 The TLS/SSL handshake was not successful but was shut down controlled and by the specifications of the TLS/SSL protocol. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. <0 The TLS/SSL handshake was not successful, because a fatal error occurred either at the protocol level or a connection failure occurred. The shutdown was not clean. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. ======= =====================================================================================

Interface variables Function This method initiate the TLS/SSL handshake with an TLS/SSL server. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_1a5892f9.png) Graphical Interface of FbSSL_Sock_Internal.handshake_connect Function description This method initiates the TLS/SSL handshake with a server. The communication channel must already have been set and assigned to the ssl by setting an underlying BIO. The behaviour of FbSSL_Sock.handshake_connect() depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.handshake_connect() will only return once the handshake has been finished or an error occurred. Note This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value. This method has the following return values: ======= ===================================================================================== 1 Operation successfull finished. 0 The TLS/SSL handshake was not successful but was shut down controlled and by the specifications of the TLS/SSL protocol. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. <0 The TLS/SSL handshake was not successful, because a fatal error occurred either at the protocol level or a connection failure occurred. The shutdown was not clean. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. ======= =====================================================================================

## FbSSL_Sock_Internal.load_client_CA_file (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | load_client_CA_file | WagoTypesSSL.typSSL_Stack |  |
| Input | sFile | STRING | path and file name |
| eSSL_FileType | WagoTypesSSL.eSSL_FileType | certificate file type |

This method loads certificate names from file.

Graphical Illustration

Graphical Interface of FbSSL_Sock_Internal.load_client_CA_file

Function description

Reads certificates from file and returns a typSSL_Stack with the subject names found. Use the return to call FbSSL_CTX.set_client_CA_list()

If the return value is 0, an error has occurred.

Interface variables Function This method loads certificate names from file. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_c6bfbf30.png) Graphical Interface of FbSSL_Sock_Internal.load_client_CA_file Function description Reads certificates from file and returns a typSSL_Stack with the subject names found. Use the return to call FbSSL_CTX.set_client_CA_list() Note If the return value is 0, an error has occurred.

## FbSSL_Sock_Internal.read (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | read | DINT |  |
| Input | pBuffer | POINTER TO BYTE | Address of buffer to receive |
| udiSize | UDINT | maximum size of data in byte to receive |

This method tries to read bytes from a TLS/SSL connection.

Graphical Illustration

Graphical Interface of FbSSL_Sock_Internal.read

Function description

This method tries to read bytes from a TLS/SSL connection into the buffer specified with pBuffer. The behaviour of FbSSL_Sock.read() depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.read() will only return, once the read operation has been finished or an error occurred.

FbSSL_Sock.read() works based on the SSL/TLS records. Only when a record has been completely received, it can be processed (decryption and check of integrity). Therefore data that was not retrieved at the last call of FbSSL_Sock.read() can still be buffered inside the SSL layer and will be retrieved on the next call to FbSSL_Sock.read(). If no more bytes are in the buffer, FbSSL_Sock.read() will trigger the processing of the next record. Only when the record has been received and processed completely, FbSSL_Sock.read() will return reporting success.

This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value.

This method has the following return values: ======= ===================================================================================== >0 The read operation was successful. The return value is the number of bytes actually read from the TLS/SSL connection. <=0 The read operation was not successful, because either the connection was closed, an error occurred or action must be taken by the calling process. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. ======= =====================================================================================

Interface variables Function This method tries to read bytes from a TLS/SSL connection. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_814dbe07.png) Graphical Interface of FbSSL_Sock_Internal.read Function description This method tries to read bytes from a TLS/SSL connection into the buffer specified with pBuffer. The behaviour of FbSSL_Sock.read() depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.read() will only return, once the read operation has been finished or an error occurred. FbSSL_Sock.read() works based on the SSL/TLS records. Only when a record has been completely received, it can be processed (decryption and check of integrity). Therefore data that was not retrieved at the last call of FbSSL_Sock.read() can still be buffered inside the SSL layer and will be retrieved on the next call to FbSSL_Sock.read(). If no more bytes are in the buffer, FbSSL_Sock.read() will trigger the processing of the next record. Only when the record has been received and processed completely, FbSSL_Sock.read() will return reporting success. Note This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value. This method has the following return values: ======= ===================================================================================== >0 The read operation was successful. The return value is the number of bytes actually read from the TLS/SSL connection. <=0 The read operation was not successful, because either the connection was closed, an error occurred or action must be taken by the calling process. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. ======= =====================================================================================

## FbSSL_Sock_Internal.shutdown (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | shutdown | DINT |

| <0 | The shutdown was not successful. Call FbSSL_Sock.get_error() with the return value of this method to find out the reason. |
| 0 | The “close notify” was send but the peer did not send it back yet. Call this method again to do a bidirectional shutdown. |
| 1 | The shutdown was successfully completed. The “close notify” alert was sent and the peer’s “close notify” alert was received. |

This method shuts down a TLS/SSL connection.

Graphical Illustration

Graphical Interface of FbSSL_Sock_Internal.shutdown

Function description

Tries to send the “close notify” shutdown alert to the peer. The shutdown procedure consists of 2 steps: the sending of the “close notify” shutdown alert and the reception of the peer’s “close notify” shutdown alert. According to the TLS standard, it is acceptable for an application to only send its shutdown alert and then close the underlying connection without waiting for the peer’s response (this way resources can be saved, as the process can already terminate or serve another connection). The behaviour of FbSSL_Sock.shutdown() additionally depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.shutdown() will only return once the handshake step has been finished or an error occurred.

This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value.

Interface variables Function This method shuts down a TLS/SSL connection. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_42e63a00.png) Graphical Interface of FbSSL_Sock_Internal.shutdown Function description Tries to send the “close notify” shutdown alert to the peer. The shutdown procedure consists of 2 steps: the sending of the “close notify” shutdown alert and the reception of the peer’s “close notify” shutdown alert. According to the TLS standard, it is acceptable for an application to only send its shutdown alert and then close the underlying connection without waiting for the peer’s response (this way resources can be saved, as the process can already terminate or serve another connection). The behaviour of FbSSL_Sock.shutdown() additionally depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.shutdown() will only return once the handshake step has been finished or an error occurred. Note This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value.

## FbSSL_Sock_Internal.write (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | write | DINT |  |
| Input | pBuffer | POINTER TO BYTE | Address of buffer to send |
| udiNBytes | UDINT | size of data in byte to send |

This method writes bytes to a TLS/SSL connection.

Graphical Illustration

Graphical Interface of FbSSL_Sock_Internal.write

Function description

The write function will only return with success when the complete contents of pBuffer of length udiNBytes has been written. The behaviour of FbSSL_Sock.write() depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.write() will only return, once the write operation has been finished or an error occurred.

This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value.

This method has the following return values: ======= ===================================================================================== >0 The write operation was successful, the return value is the number of bytes actually written to the TLS/SSL connection. <=0 The write operation was not successful, because either the connection was closed, an error occurred or action must be taken by the calling process. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. ======= =====================================================================================

Interface variables Function This method writes bytes to a TLS/SSL connection. Graphical Illustration ![Image](images/wagosysssl_internal_pfc_e1fe55f6.png) Graphical Interface of FbSSL_Sock_Internal.write Function description The write function will only return with success when the complete contents of pBuffer of length udiNBytes has been written. The behaviour of FbSSL_Sock.write() depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.write() will only return, once the write operation has been finished or an error occurred. Note This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value. This method has the following return values: ======= ===================================================================================== >0 The write operation was successful, the return value is the number of bytes actually written to the TLS/SSL connection. <=0 The write operation was not successful, because either the connection was closed, an error occurred or action must be taken by the calling process. Call FbSSL_Sock.get_error() with the return value ret to find out the reason. ======= =====================================================================================

### Program Organization


## 20 Program Organization Units


- 90 Internal 29 Types eSSL_X509_V_RTS (ENUM) eSSL_X509_V_RTS_TO_eSSL_X509_V (FUN) FbSSL_CTX_Internal (FB) - FbSSL_CTX_Internal.load_revocation_list (METH) - FbSSL_CTX_Internal.load_verfiy_locations (METH) - FbSSL_CTX_Internal.sess_set_cache_size (METH) - FbSSL_CTX_Internal.set_client_CA_list (METH) - FbSSL_CTX_Internal.set_method (METH) - FbSSL_CTX_Internal.set_verify (METH) - FbSSL_CTX_Internal.use_PrivateKey_file (METH) - FbSSL_CTX_Internal.use_certificate_file (METH) - FbSSL_CTX_Internal.verify_depth (METH) FbSSL_Sock_Internal (FB) - FbSSL_Sock_Internal.get0_param (METH) - FbSSL_Sock_Internal.get_error (METH) - FbSSL_Sock_Internal.get_peer_certificate (METH) - FbSSL_Sock_Internal.get_verify_result (METH) - FbSSL_Sock_Internal.handshake_accept (METH) - FbSSL_Sock_Internal.handshake_connect (METH) - FbSSL_Sock_Internal.load_client_CA_file (METH) - FbSSL_Sock_Internal.read (METH) - FbSSL_Sock_Internal.shutdown (METH) - FbSSL_Sock_Internal.write (METH) X509_free_Internal (FUN) X509_verify_param_set1_host_Internal (FUN) X509_verify_param_set_flags_Internal (FUN) X509_verify_param_set_hostflags_Internal (FUN)

### Internal Components


## 90 Internal


- 29 Types eSSL_X509_V_RTS (ENUM) eSSL_X509_V_RTS_TO_eSSL_X509_V (FUN)

## WagoSysSSL_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysSSL_Internal_PFC |
| Version: | 1.1.6.2 |
| Categories: | WAGO Internal\|Target\|PFC; WAGO Internal\|Feature\|Network |
| Namespace: | WagoSysSSLInternal |
| Author: | WAGO / u010956 |
| Placeholder: | WagoSysSSLInternal |

### Description


This document is automatically generated.

This document is automatically generated.

### Contents:


- 20 Program Organization Units 90 Internal - FbSSL_CTX_Internal (FB) - FbSSL_Sock_Internal (FB) - X509_free_Internal (FUN) - X509_verify_param_set1_host_Internal (FUN) - X509_verify_param_set_flags_Internal (FUN) - X509_verify_param_set_hostflags_Internal (FUN) VersionHistory (GVL)

### Indices and tables


Based on WagoSysSSL_Internal_PFC.library, last modified 29.05.2024, 19:52:41. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysSSL_Internal_PFC.library, last modified 29.05.2024, 19:52:41. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 21.02.2024 | 1.0.6.2 | WAGO / u010663 | Compiled SP16.3 |
| 22.02.2023 | 1.0.6.1 | WAGO / u013972 | Mark as deprecated |
| 23.11.2020 | 1.0.5.0 | WAGO / u013972 | Add new ssl methods |
| 08.01.2019 | 1.1.5.1 | u015842 | Properties: copyright added |
| 26.09.2018 | 1.1.5.0 | WAGO / u013972 | Release Version |

WagoSysSSL_Internal_PFC.library

WagoSysSSL_Internal_PFC.library

### Other Components


## 29 Types ¶


- eSSL_X509_V_RTS (ENUM)

## eSSL_X509_V_RTS (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| OK | 0 |  |
| ERR_UNSPECIFIED | 1 |  |
| ERR_UNABLE_TO_GET_ISSUER_CERT | 2 |  |
| ERR_UNABLE_TO_GET_CRL | 3 |  |
| ERR_UNABLE_TO_DECRYPT_CERT_SIGNATURE | 4 |  |
| ERR_UNABLE_TO_DECRYPT_CRL_SIGNATURE | 5 |  |
| ERR_UNABLE_TO_DECODE_ISSUER_PUBLIC_KEY | 6 |  |
| ERR_CERT_SIGNATURE_FAILURE | 7 |  |
| ERR_CRL_SIGNATURE_FAILURE | 8 |  |
| ERR_CERT_NOT_YET_VALID | 9 |  |
| ERR_CERT_HAS_EXPIRED | 10 |  |
| ERR_CRL_NOT_YET_VALID | 11 |  |
| ERR_CRL_HAS_EXPIRED | 12 |  |
| ERR_ERROR_IN_CERT_NOT_BEFORE_FIELD | 13 |  |
| ERR_ERROR_IN_CERT_NOT_AFTER_FIELD | 14 |  |
| ERR_ERROR_IN_CRL_LAST_UPDATE_FIELD | 15 |  |
| ERR_ERROR_IN_CRL_NEXT_UPDATE_FIELD | 16 |  |
| ERR_OUT_OF_MEM | 17 |  |
| ERR_DEPTH_ZERO_SELF_SIGNED_CERT | 18 |  |
| ERR_SELF_SIGNED_CERT_IN_CHAIN | 19 |  |
| ERR_UNABLE_TO_GET_ISSUER_CERT_LOCALLY | 20 |  |
| ERR_UNABLE_TO_VERIFY_LEAF_SIGNATURE | 21 |  |
| ERR_CERT_CHAIN_TOO_LONG | 22 |  |
| ERR_CERT_REVOKED | 23 |  |
| ERR_INVALID_CA | 24 |  |
| ERR_PATH_LENGTH_EXCEEDED | 25 |  |
| ERR_INVALID_PURPOSE | 26 |  |
| ERR_CERT_UNTRUSTED | 27 |  |
| ERR_CERT_REJECTED | 28 |  |
| ERR_SUBJECT_ISSUER_MISMATCH | 29 | These are ‘informational’ when looking for issuer cert |
| ERR_AKID_SKID_MISMATCH | 30 |  |
| ERR_AKID_ISSUER_SERIAL_MISMATCH | 31 |  |
| ERR_KEYUSAGE_NO_CERTSIGN | 32 |  |
| ERR_UNABLE_TO_GET_CRL_ISSUER | 33 |  |
| ERR_UNHANDLED_CRITICAL_EXTENSION | 34 |  |
| ERR_KEYUSAGE_NO_CRL_SIGN | 35 |  |
| ERR_UNHANDLED_CRITICAL_CRL_EXTENSION | 36 |  |
| ERR_INVALID_NON_CA | 37 |  |
| ERR_PROXY_PATH_LENGTH_EXCEEDED | 38 |  |
| ERR_KEYUSAGE_NO_DIGITAL_SIGNATURE | 39 |  |
| ERR_PROXY_CERTIFICATES_NOT_ALLOWED | 40 |  |
| ERR_INVALID_EXTENSION | 41 |  |
| ERR_INVALID_POLICY_EXTENSION | 42 |  |
| ERR_NO_EXPLICIT_POLICY | 43 |  |
| ERR_DIFFERENT_CRL_SCOPE | 44 |  |
| ERR_UNSUPPORTED_EXTENSION_FEATURE | 45 |  |
| ERR_UNNESTED_RESOURCE | 46 |  |
| ERR_PERMITTED_VIOLATION | 47 |  |
| ERR_EXCLUDED_VIOLATION | 48 |  |
| ERR_SUBTREE_MINMAX | 49 |  |
| ERR_APPLICATION_VERIFICATION | 50 |  |
| ERR_UNSUPPORTED_CONSTRAINT_TYPE | 51 |  |
| ERR_UNSUPPORTED_CONSTRAINT_SYNTAX | 52 |  |
| ERR_UNSUPPORTED_NAME_SYNTAX | 53 |  |
| ERR_CRL_PATH_VALIDATION_ERROR | 54 |  |
| ERR_SUITE_B_INVALID_VERSION | 56 | Suite B mode algorithm violation |
| ERR_SUITE_B_INVALID_ALGORITHM | 57 |  |
| ERR_SUITE_B_INVALID_CURVE | 58 |  |
| ERR_SUITE_B_INVALID_SIGNATURE_ALGORITHM | 59 |  |
| ERR_SUITE_B_LOS_NOT_ALLOWED | 60 |  |
| ERR_SUITE_B_CANNOT_SIGN_P_384_WITH_P_256 | 61 |  |
| ERR_HOSTNAME_MISMATCH | 62 | Host, email and IP check errors |
| ERR_EMAIL_MISMATCH | 63 |  |
| ERR_IP_ADDRESS_MISMATCH | 64 |  |
| ERR_INVALID_CALL | 65 | Caller error |
| ERR_STORE_LOOKUP | 66 | Issuer lookup error |
| ERR_PROXY_SUBJECT_NAME_VIOLATION | 67 |  |

Attributes: qualified_only InOut: