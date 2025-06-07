# WagoSysCurl v1.1.5.0

## Overview
WAGO PLC library providing WagoSysCurl functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbCurl
Provides libCurl functions

**Description:**
This Fb provides libCurl functions of the easy interface. The Fb holdes a curl easy handle internal

**Methods:**

#### curl_set_FilePath
Sets the local file path

This method sets the local file path for a file transfer.

#### curl_easy_setopt_STRING
Sets options for a curl easy handle

This method sets the options for a curl easy handle. .. note:: For the option CURLOPT_URL the parameter 'sParameter' must be encoded as described in RFC 3986. Amongst other things special characters must be written in the percent-encoding, e.g. for a space as %20. For more information see: http://curl.haxx.se/libcurl/c/curl_easy_setopt.html

#### curl_easy_setopt_DINT
Sets options for a curl easy handle

This method sets the options for a curl easy handle. For more information see: http://curl.haxx.se/libcurl/c/curl_easy_setopt.html

#### curl_slist_append
Appends a STRING to a slist

This method appends a STRING to a slist. slists with a index form 1..9 are available for this method.

#### curl_easy_perform
Perform the configurated operation

Invoke this method after curl_easy_init and all the curl_easy_setopt calls are made, and will perform the transfer as described in the options. For more information see: http://curl.haxx.se/libcurl/c/curl_easy_perform.html

#### curl_easy_reset
Resets all configurated options to their default settings

This method resets all configurated options of the easy handle to their default settings.

#### curl_easy_setopt_BOOL
Sets options for a curl easy handle

This method sets the options for a curl easy handle. For more information see: http://curl.haxx.se/libcurl/c/curl_easy_setopt.html

#### curl_slist_append2
Appends a STRING to a slist

This method appends a STRING to a slist. slists with a index form 1..9 are available for this method.

#### curl_easy_setopt_STRING2
Sets options for a curl easy handle

This method sets the options for a curl easy handle. .. note:: For the option CURLOPT_URL the STRING must be encoded as described in RFC 3986. Amongst other things special characters must be written in the percent-encoding, e.g. for a space as %20. For more information see: http://curl.haxx.se/libcurl/c/curl_easy_setopt.html

#### curl_easy_getResponseCode
Return the response code of the protocol

Return the response code of the protocol. https://curl.haxx.se/libcurl/c/CURLINFO_RESPONSE_CODE.html

#### curl_slist_free_all
Free a slist

This method free all entrys in the slist, the slist is empty after this method.

#### curl_easy_setopt_slist
Sets options for a curl easy handle

This method sets the options for a curl easy handle. slists with a index form 0..9 are available, the slist with the index 0 is empty. For more information see: http://curl.haxx.se/libcurl/c/curl_easy_setopt.html

#### curl_easy_cleanup
End a libcurl easy handle

This method must be the last function to call for an easy session. For more information see: http://curl.haxx.se/libcurl/c/curl_easy_cleanup.html

#### curl_easy_init
Start a libcurl easy session

This method must be the first function to call, and it initialize the CURL easy handle. For more information see: http://curl.haxx.se/libcurl/c/curl_easy_init.html

#### curl_easy_abort
Abort the current operation

This method aborts the current operation.

#### curl_set_RAM
Sets the buffer

This method sets the buffer for a file transfer.

#### curl_set_LogFile
Sets the local file path for the log file

This method sets the local file path for the log file.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbCurl: FbCurl;
END_VAR

// Basic function block usage
fbFbCurl(
    // Configure inputs as needed
);

// Check status
IF fbFbCurl.xValid THEN
    // Operation successful
END_IF

IF fbFbCurl.xError THEN
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

