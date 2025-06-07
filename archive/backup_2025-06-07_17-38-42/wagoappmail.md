# WagoAppMail v1.1.1.3

## Overview
WAGO PLC library providing WagoAppMail functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbSmtpSendMail
Send plain text email messages via encrypted or unencrypted SMTP.

**Description:**
This function block allows to send email messages via encrypted or unencrypted SMTP. The message body of the email is configureable through the input variable ``sMessage``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to create and send an email message. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing the email message.

### FbSmtpSendRam
Send plain text email messages with attachment data taken directly from the e!COCKPIT application via encrypted or unencrypted SMTP.

**Description:**
This function block allows to send plain text email messages with attachment data taken directly from the e!COCKPIT application via encrypted or unencrypted SMTP. The message body of the email is configureable through the input variable ``sMessage``. ``sAttachmentName`` determines the name of the attachment in the email message. The inputs ``pData`` and ``udiSize`` are determining the data that is attached to the email message. Transition to ``TRUE`` on ``xTrigger`` triggers the process to create and send an email message. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing the email message.

### FbSmtpSendFile
Send plain text email messages with attachment from filesystem via encrypted or unencrypted SMTP.

**Description:**
This function block allows to send email messages with attachment from filesystem via encrypted or unencrypted SMTP. The message body of the email is configureable through the input variable ``sMessage``. The input variable ``sMessage`` contains the path to the file that should be attached to the email message Transition to ``TRUE`` on ``xTrigger`` triggers the process to create and send an email message. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing the email message.

### FbSmtpSend
Send email messages via encrypted or unencrypted SMTP.

**Description:**
This function block allows to send email messages via encrypted or unencrypted SMTP. The message body of the email is configureable through the input variable :ref:`typMessage`. The structure :ref:`typMessage` allows to configure the data area, size, content-type, character set and encoding of the message body. This may be helpful if it is requiered to send HTML content in the message body (text/html). The number of attachments is not limited by the function block. Limiting factors are the available space in the tmp-filesystem of the controller and restrictions of the email provider. Attachments are configureable through the input array :ref:`typAttachment`. Each element of the array holds an description of an attachment. The attachment may be a file located in the filesystem of the controller or a data array declared inside the e!COCKPIT application. Transition to ``TRUE`` on ``xTrigger`` triggers the process to create and send an email message. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing the email message.

## Data Types

### typAttachment
Structure type.

### typMessage
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbSmtpSendMail: FbSmtpSendMail;
END_VAR

// Basic function block usage
fbFbSmtpSendMail(
    // Configure inputs as needed
);

// Check status
IF fbFbSmtpSendMail.xValid THEN
    // Operation successful
END_IF

IF fbFbSmtpSendMail.xError THEN
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

