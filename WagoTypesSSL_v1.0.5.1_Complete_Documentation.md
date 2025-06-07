# WagoTypesSSL v1.0.5.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesSSL
- **Version:** 1.0.5.1
- **Categories:** Application; WAGO LayerView|Types and Interfaces
- **Author:** WAGO / u013972
- **Placeholder:** WagoTypesSSL

### Description ¶


This document is automatically generated.

This library contains the type definitions for WagoSysSSL

This document is automatically generated. This library contains the type definitions for WagoSysSSL

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Functions - Other Components 29 Types - eSSL_Error (ENUM) - eSSL_FileType (ENUM) - eSSL_Method (ENUM) - eSSL_Verify (ENUM) - eSSL_X509_Check (ENUM) - eSSL_X509_V (ENUM) - eSSL_X509_Verification (ENUM) - typSSL_Stack (ALIAS) - typeSSL_X509 (ALIAS) - ... and 1 more

### Indices and tables ¶


Based on WagoTypesSSL.library, last modified 29.05.2024, 19:52:38. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesSSL.library, last modified 29.05.2024, 19:52:38. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesSSL Library Documentation


| Company: | WAGO |
| Title: | WagoTypesSSL |
| Version: | 1.0.5.1 |
| Categories: | Application; WAGO LayerView\|Types and Interfaces |
| Author: | WAGO / u013972 |
| Placeholder: | WagoTypesSSL |

### Description


This document is automatically generated.

This library contains the type definitions for WagoSysSSL

This document is automatically generated. This library contains the type definitions for WagoSysSSL

### Contents:


- 29 Types eSSL_Error (ENUM) - eSSL_FileType (ENUM) - eSSL_Method (ENUM) - eSSL_Verify (ENUM) - eSSL_X509_Check (ENUM) - eSSL_X509_V (ENUM) - eSSL_X509_Verification (ENUM) - typSSL_Stack (ALIAS) - typeSSL_X509 (ALIAS) - typeSSL_param (ALIAS) FuGetVersionHistory (FUN)

### Indices and tables


Based on WagoTypesSSL.library, last modified 29.05.2024, 19:52:38. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesSSL.library, last modified 29.05.2024, 19:52:38. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesSSL.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:52:38 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:52:38 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesSSL |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesSSL |
| DefaultNamespace |  |
| Version | version | 1.0.5.1 |
| Title | string | WagoTypesSSL |
| LibraryCategories | library-category-list | Application; WAGO LayerView\|Types and Interfaces |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties :

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 28.02.2024 | 1.0.5.1 | WAGO / u010663 | Compiled SP16.3 |
| 23.11.2020 | 1.0.5.0 | WAGO / u013972 | Add new ssl methods |
| 08.01.2019 | 1.0.4.0 | u015842 | Properties: free placeholder added |
| 21.08.2018 | 1.0.3.0 | WAGO / u013972 | Release Version |

WagoTypesTemplate.library

Interface variables WagoTypesTemplate.library

### Other Components


## 29 Types


- eSSL_Error (ENUM) - eSSL_FileType (ENUM) - eSSL_Method (ENUM) - eSSL_Verify (ENUM) - eSSL_X509_Check (ENUM) - eSSL_X509_V (ENUM) - eSSL_X509_Verification (ENUM) - typSSL_Stack (ALIAS) - typeSSL_X509 (ALIAS) - typeSSL_param (ALIAS)

## eSSL_Error (ENUM)


| Name | Initial |
| --- | --- |
| SSL_ERROR_NONE | 0 |
| SSL_ERROR_SSL | 1 |
| SSL_ERROR_WANT_READ | 2 |
| SSL_ERROR_WANT_WRITE | 3 |
| SSL_ERROR_WANT_X509_LOOKUP | 4 |
| SSL_ERROR_SYSCALL | 5 |
| SSL_ERROR_ZERO_RETURN | 6 |
| SSL_ERROR_WANT_CONNECT | 7 |
| SSL_ERROR_WANT_ACCEPT | 8 |
| SSL_ERROR_UNKNOWN | 255 |

Attributes: qualified_only InOut: - eSSL_Error.SSL_ERROR_NONE Operation successfull finished. This result code is returned if and only if ret > 0. - eSSL_Error.SSL_ERROR_ZERO_RETURN The TLS/SSL connection has been closed. If the protocol version is SSL 3.0 or higher, this result code is returned only if a closure alert has occurred in the protocol, i.e. if the connection has been closed cleanly. Note that in this case SSL_ERROR_ZERO_RETURN does not necessarily indicate that the underlying transport has been closed. - eSSL_Error.SSL_ERROR_WANT_READ / eSSL_Error.SSL_ERROR_WANT_WRITE The operation did not complete; the same TLS/SSL I/O function should be called again later. - eSSL_Error.SSL_ERROR_WANT_CONNECT / eSSL_Error.SSL_ERROR_WANT_ACCEPT The operation did not complete; the same TLS/SSL I/O function should be called again later. The underlying BIO was not connected yet to the peer and the call would block in connect()/accept(). The SSL function should be called again when the connection is established. - eSSL_Error.SSL_ERROR_WANT_X509_LOOKUP The operation did not complete; The TLS/SSL I/O function should be called again later. Details depend on the application. - eSSL_Error.SSL_ERROR_SYSCALL Some non-recoverable I/O error occurred. - eSSL_Error.SSL_ERROR_SSL A failure in the SSL library occurred, usually a protocol error.

## eSSL_FileType (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| PEM | 1 | Base64 coded certificate or key |
| DER | 2 | Binary coded certificate or key |

Attributes: qualified_only InOut:

## eSSL_Method (ENUM)


| Name | Initial |
| --- | --- |
| SSLv23 | 3 |
| SSLv23_server | 4 |
| SSLv23_client | 5 |
| SSLv3 | 6 |
| SSLv3_server | 7 |
| SSLv3_client | 8 |
| TLSv1 | 9 |
| TLSv1_server | 10 |
| TLSv1_client | 11 |
| TLSv1_1 | 12 |
| TLSv1_1_server | 13 |
| TLSv1_1_client | 14 |
| TLSv1_2 | 15 |
| TLSv1_2_server | 16 |
| TLSv1_2_client | 17 |
| DTLSv1 | 18 |
| DTLSv1_server | 19 |
| DTLSv1_client | 20 |
| DTLSv1_2 | 21 |
| DTLSv1_2_server | 22 |
| DTLSv1_2_client | 23 |
| DTLS | 24 |
| DTLS_server | 25 |
| DTLS_client | 26 |
| TLS | 27 |
| TLS_server | 28 |
| TLS_client | 29 |

Attributes: qualified_only InOut:

## eSSL_Verify (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| SSL_VERIFY_NONE | 0 | Server mode: the server will not send a client certificate request to the client, so the client will not send a certificate. Client mode: if not using an anonymous cipher (by default disabled), the server will send a certificate which will be checked. |
| SSL_VERIFY_PEER | 1 | Server mode: the server sends a client certificate request to the client. The certificate returned (if any) is checked. If the verification process fails, the TLS/SSL handshake is immediately terminated with an alert message containing the reason for the verification failure. |
| SSL_VERIFY_FAIL_IF_NO_PEER_CERT | 2 | Server mode: if the client did not return a certificate, the TLS/SSL handshake is immediately terminated with a “handshake failure” alert. This flag must be used together with SSL_VERIFY_PEER. Client mode: ignored |
| SSL_VERIFY_CLIENT_ONCE | 4 | Server mode: only request a client certificate on the initial TLS/SSL handshake. Do not ask for a client certificate again in case of a renegotiation. This flag must be used together with SSL_VERIFY_PEER. Client mode: ignored |

Attributes: qualified_only InOut:

## eSSL_X509_Check (ENUM)


| Name | Initial |
| --- | --- |
| X509_CHECK_FLAG_NO_PARTIAL_WILDCARDS | 0 |
| X509_CHECK_FLAG_NO_WILDCARDS | 1 |

Attributes: qualified_only InOut:

## eSSL_X509_V (ENUM)


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
| ERR_UNKNOWN | 255 |  |

Attributes: qualified_only InOut:

## eSSL_X509_Verification (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| FLAG_CRL_CHECK | 16#4 | enables CRL checking for the certificate chain leaf certificate. An error occurs if a suitable CRL cannot be found. |
| FLAG_CRL_CHECK_ALL | 16#8 | enables CRL checking for the entire certificate chain. |

Attributes: qualified_only InOut:

## typSSL_Stack (ALIAS) ¶


## typeSSL_X509 (ALIAS) ¶


## typeSSL_param (ALIAS) ¶
