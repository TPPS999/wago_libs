# WagoAppHTTP v1.7.3.5

## Overview
WAGO PLC library providing WagoAppHTTP functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbHTTP_Client_Curl
Compact function block performing an HTTP(s) request.

**Description:**
This function block communicate with an HTTP server via HTTP(s) request.

### FbHTTPs_Post_2
Compact function block performing a HTTP Post request

**Description:**
This function block should be used reading data from a webserver by using the HTTP post command. Input ``eAuthentication``: | Option ``digest`` not yet supported Input ``pHeader``: | This input may be used to specify the Header field as defined in RFC7231 | example 1: | pHeader:

### FbHTTPs_Get_2
This function block should be used reading data from a webserver by using the HTTP get command.

**Description:**
This function block should be used reading data from a webserver. As defined by the standard, it is also possible to transfer a small amount of data to the webserver. In this case the URI must contain the data in an appropriate manner. Input ``eAuthentication``: | Option ``digest`` not yet supported Input ``sHeader``: | This input may be used to specify the Header field as defined in RFC7231 | example 1: | sHeader:

### FbHTTP_Post_2
Compact function block performing a HTTP Post request

**Description:**
This function block should be used reading data from a webserver by using the HTTP post command. Input ``eAuthentication``: | Option ``digest`` not yet supported Input ``pHeader``: | This input may be used to specify the Header field as defined in RFC7231 | example 1: | pHeader:

### FbHTTP_Get_2
Compact function block performing a HTTP Get request

**Description:**
This function block should be used reading data from a webserver. As defined by the standard, it is also possible to transfer a small amount of data to the webserver. In this case the URI must contain the data in an appropriate manner. Input ``eAuthentication``: | Option ``digest`` not yet supported Input ``pHeader``: | This input may be used to specify the Header field as defined in RFC7231 | example 1: | sHeader:

### FbHTTPs_Post
Compact function block performing a HTTP Post request

**Description:**
This function block should be used reading data from a webserver by using the HTTP post command. Input ``eAuthentication``: | Option ``digest`` not yet supported Input ``sHeader``: | This input may be used to specify the Header field as defined in RFC7231 | example 1: | sHeader:

### FbHTTPs_Get
This function block should be used reading data from a webserver by using the HTTP get command.

**Description:**
This function block should be used reading data from a webserver. As defined by the standard, it is also possible to transfer a small amount of data to the webserver. In this case the URI must contain the data in an appropriate manner. The size of the URI is limited to 1023 byte. Input ``eAuthentication``: | Option ``digest`` not yet supported Input ``sHeader``: | This input may be used to specify the Header field as defined in RFC7231 | example 1: | sHeader:

### FbHTTP_Get
Compact function block performing a HTTP Get request

**Description:**
This function block should be used reading data from a webserver. As defined by the standard, it is also possible to transfer a small amount of data to the webserver. In this case the URI must contain the data in an appropriate manner. The size of the URI is limited to 1023 byte. Input ``eAuthentication``: | Option ``digest`` not yet supported Input ``sHeader``: | This input may be used to specify the Header field as defined in RFC7231 | example 1: | sHeader:

### FbHTTP_Post
Compact function block performing a HTTP Post request

**Description:**
This function block should be used reading data from a webserver by using the HTTP post command. Input ``eAuthentication``: | Option ``digest`` not yet supported Input ``sHeader``: | This input may be used to specify the Header field as defined in RFC7231 | example 1: | sHeader:

## Data Types

### eStatusHTTP_Curl
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbHTTP_Client_Curl: FbHTTP_Client_Curl;
END_VAR

// Basic function block usage
fbFbHTTP_Client_Curl(
    // Configure inputs as needed
);

// Check status
IF fbFbHTTP_Client_Curl.xValid THEN
    // Operation successful
END_IF

IF fbFbHTTP_Client_Curl.xError THEN
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

