# WagoSysSSL_Internal_PFC v1.1.6.2

## Overview
WAGO PLC library providing WagoSysSSL_Internal_PFC functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbSSL_Sock_Internal
This function block contains the the main SSL/TLS structure.

**Description:**
This function block contains the the main SSL/TLS structure which is created by a server or client per established connection. This actually is the core structure in the SSL API. At run-time the application usually deals with this structure which has links to mostly all other structures. The methods of this function block allow differnt operations on the connection.

**Methods:**

#### write
This method writes bytes to a TLS/SSL connection.

The write function will only return with success when the complete contents of pBuffer of length udiNBytes has been written. The behaviour of FbSSL_Sock.write() depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.write() will only return, once the write operation has been finished or an error occurred. .. note:: This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value. This method has the following return values:

#### read
This method tries to read bytes from a TLS/SSL connection.

This method tries to read bytes from a TLS/SSL connection into the buffer specified with pBuffer. The behaviour of FbSSL_Sock.read() depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.read() will only return, once the read operation has been finished or an error occurred. FbSSL_Sock.read() works based on the SSL/TLS records. Only when a record has been completely received, it can be processed (decryption and check of integrity). Therefore data that was not retrieved at the last call of FbSSL_Sock.read() can still be buffered inside the SSL layer and will be retrieved on the next call to FbSSL_Sock.read(). If no more bytes are in the buffer, FbSSL_Sock.read() will trigger the processing of the next record. Only when the record has been received and processed completely, FbSSL_Sock.read() will return reporting success. .. note:: This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value. This method has the following return values:

#### load_client_CA_file
This method loads certificate names from file.

Reads certificates from file and returns a typSSL_Stack with the subject names found. Use the return to call FbSSL_CTX.set_client_CA_list() .. note:: If the return value is 0, an error has occurred.

#### handshake_connect
This method initiate the TLS/SSL handshake with an TLS/SSL server.

This method initiates the TLS/SSL handshake with a server. The communication channel must already have been set and assigned to the ssl by setting an underlying BIO. The behaviour of FbSSL_Sock.handshake_connect() depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.handshake_connect() will only return once the handshake has been finished or an error occurred. .. note:: This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value. This method has the following return values:

#### get_error
This method obtain result code for TLS/SSL I/O operation.

This method returns a result code for a preceding call to handshake_connect(), handshake_accept(), read() or write() on ssl. This method has the following return values: - eSSL_Error.SSL_ERROR_NONE Operation successfull finished. This result code is returned if and only if ret > 0. - eSSL_Error.SSL_ERROR_ZERO_RETURN The TLS/SSL connection has been closed. If the protocol version is SSL 3.0 or higher, this result code is returned only if a closure alert has occurred in the protocol, i.e. if the connection has been closed cleanly. Note that in this case SSL_ERROR_ZERO_RETURN does not necessarily indicate that the underlying transport has been closed. - eSSL_Error.SSL_ERROR_WANT_READ / eSSL_Error.SSL_ERROR_WANT_WRITE The operation did not complete; the same TLS/SSL I/O function should be called again later. - eSSL_Error.SSL_ERROR_WANT_CONNECT / eSSL_Error.SSL_ERROR_WANT_ACCEPT The operation did not complete; the same TLS/SSL I/O function should be called again later. The underlying BIO was not connected yet to the peer and the call would block in connect()/accept(). The SSL function should be called again when the connection is established. - eSSL_Error.SSL_ERROR_WANT_X509_LOOKUP The operation did not complete; The TLS/SSL I/O function should be called again later. Details depend on the application. - eSSL_Error.SSL_ERROR_SYSCALL Some non-recoverable I/O error occurred. - eSSL_Error.SSL_ERROR_SSL A failure in the SSL library occurred, usually a protocol error.

#### handshake_accept
This method wait for a TLS/SSL client to initiate a TLS/SSL handshake.

This method waits for a TLS/SSL client to initiate the TLS/SSL handshake. The communication channel must already have been set and assigned to the ssl by setting an underlying BIO. The behaviour of FbSSL_Sock.handshake_accept() depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.handshake_accept() will only return once the handshake has been finished or an error occurred. .. note:: This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value. This method has the following return values:

#### shutdown
This method shuts down a TLS/SSL connection.

Tries to send the "close notify" shutdown alert to the peer. The shutdown procedure consists of 2 steps: the sending of the "close notify" shutdown alert and the reception of the peer's "close notify" shutdown alert. According to the TLS standard, it is acceptable for an application to only send its shutdown alert and then close the underlying connection without waiting for the peer's response (this way resources can be saved, as the process can already terminate or serve another connection). The behaviour of FbSSL_Sock.shutdown() additionally depends on the underlying BIO. If the underlying BIO is blocking, FbSSL_Sock.shutdown() will only return once the handshake step has been finished or an error occurred. .. note:: This function is able to work some seconds. So do not use this functionality in high prior task with small timeout value.

### FbSSL_CTX_Internal
This function block contains the SSL_CTX (SSL Context).

**Description:**
This function block contains the SSL_CTX (SSL Context), that's the global context structure which is created by a server or client once per program life-time and which holds mainly default values for the SSL structures which are later created for the connections. The values of the SSL_CTX can be set with the different methods oh this funftion block.

**Methods:**

#### load_revocation_list
This method specifies the locations for ctx, at which a revocation list for verification purposes are located.

A certificate revocation list provides a list of certificates that have been revoked. To specify more than one revocation list the function must be called repeatedly. This method has the following return values:

#### verify_depth
#### set_verify
#### use_PrivateKey_file
This method loads the list of private keys stored in the specified file.

Adds sFile as private key to FbSSL_CTX. If a certificate has already been set and the private does not belong to the certificate an error is returned. To change a certificate, private key pair the new certificate needs to be set with FbSSL_CTX.use_certificate_file() before setting the private key. This method has the following return values:

#### use_certificate_file
This method defines the file that contains the certificates during the verification process. The certificates are loaded at this time.

Loads the first certificate stored in sFile into FbSSL_CTX. The formatting type of the certificate must be specified with eFileType. This method has the following return values:

#### set_method
This method sets the method of SSL handling.

This method sets the method of SSL handling. Must be called first during using the FbSSL_CTX. This method has the following return values:

#### set_client_CA_list
This methos sets the list of CAs sent to the client when requesting a client certificate for channel.

When a TLS/SSL server requests a client certificate, it sends a list of CAs, for which it will accept certificates, to the client. This method has the following return values:

#### sess_set_cache_size
This method manipulate session cache size.

Sets the size of the internal session cache of context FbSSL_CTX to udiCacheSize. .. note:: A special case is the size 0, which is used for unlimited size. This method returns the previously valid size.

#### load_verfiy_locations
This method specifies the locations for ctx, at which CA certificates for verification purposes are located.

This function loads the list of certificates that are automatically confirmed. This list is located in the file system and will be loaded by FbSSL_CTX at this time. This method has the following return values:

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbSSL_Sock_Internal: FbSSL_Sock_Internal;
END_VAR

// Basic function block usage
fbFbSSL_Sock_Internal(
    // Configure inputs as needed
);

// Check status
IF fbFbSSL_Sock_Internal.xValid THEN
    // Operation successful
END_IF

IF fbFbSSL_Sock_Internal.xError THEN
    // Handle error
END_IF
```

## Best Practices

### Error Handling
```iec
IF fbInstance.xError THEN
    CASE fbInstance.eStatus OF
        // Handle specific error codes
    END_CASE
END_IF
```

### Performance Considerations
- Use appropriate polling intervals
- Handle communication errors gracefully
- Consider device response times
- Test thoroughly in target environment

## Important Notes

- This documentation was automatically generated from XML specification
- Always refer to official WAGO documentation for complete details
- Test thoroughly in your specific application environment
- Check library compatibility with your PLC hardware

