# WagoAppFTP v1.3.1.7

## Overview
WAGO PLC library providing WagoAppFTP functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbFTPES
This function block provides FTPES-Client-Services.

**Description:**
The FbFTPES is the base function block for FTPES-Client-Services. The Fb provide functions like read and write files, rename or remove files and create or remove directories. The inputs of the FbFTPES handle the gerneral information for the FTPES connection and the outputs signal the process and the result of the operations. The operations are triggered by call the specific method for the operation. After a call the methods will return immediately and the FbFTPES start the operation. .. note:: This function block must called cyclic.

**Methods:**

#### List
List files and directories

This method starts an operation to performs a directory listing. The linsting includ only those files that match the specification stored in``sFileSpec``. The input parameter ``pRxBuffer`` is pointing to the first element of the buffer and the buffersize is defined by the input parameter ``udiRxBufferSize``. If more details of the files and direcotries should list, the input parameter ``xWithDetails`` must set to true. The status and result of the operation are displayed by the outputs of the FbFTPES. This method has the following return values:

#### FileWriteFromMem
Write a file

This method starts an operation to write the data from the TxBuffer to a file on the remote host specified by ``sRemotePath``. If the remote file exit, it will be overwritten. The status and result of the operation are displayed by the outputs of the FbFTPES. This method has the following return values:

#### FileWrite
Write a file

This method starts an operation to write the data form the local file, that is specified by the input parameter ``sLocalPath``, to the remote file, that is specified by the input parameter ``sRemotePath``. If the remote file exit, it will be overwritten. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbFTPES. This method has the following return values:

#### FileRename
Rename a file

This method starts an operation to rename the file, that is defined by the input parameter ``sOldFileName``, to the name, that is defined by the input parameter ``sNewFileName``. The status and result of the operation are displayed by the outputs of the FbFTPES. This method has the following return values:

#### FileRemove
Remove a file

This method starts an operation to remove the file, that is specified by ``sRemotePath``. An error is returned if the file does not exists, the file cannot be removed, or if the user does not have the appropriate privilege level. The status and result of the operation are displayed by the outputs of the FbFTPES. This method has the following return values:

#### FileReadToMem
Read a file

This method starts an operation to reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the RxBuffer, that is specified by the input parameter ``pRxBuffer`` and ``udiRxBufferSize``. The status and result of the operation are displayed by the outputs of the FbFTPES. This method has the following return values:

#### FileRead
Read a file

This method starts an operation to reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the local file, that is specified by the input parameter ``sLocalPath``. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbFTPES. This method has the following return values:

#### FileAppendFromMem
Append a data from a buffer to a remote file

This method starts an operation to append data from the TxBuffer to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. The status and result of the operation are displayed by the outputs of the FbFTPES. This method has the following return values:

#### FileAppend
Append a local file to a remote file

This method starts an operation to append a local file specified by ``sLocalPath`` to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbFTPES. This method has the following return values:

#### DirRemove
This method starts an operation to remove the directory, that is specified by ``sRemotePath``. An error is returned if the directory does not exists, the dircectory cannot removed (in use, or not empty), or if the user does not have the appropriate privilege level. The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

#### DirCreate
Create a directory

This method starts an operation to create a new directory specified by ``sRemotePath``. The method create only the last directory in the path. If a directory in the path is missing or the driectory, that schould create, already exists an error occur. The status and result of the operation are displayed by the outputs of the FbFTPES. This method has the following return values:

### FbSFTP_List
List files and directories

**Description:**
This functionblock performs a directory listing. The input parameter ``pRxBuffer`` is pointing to the first element of the buffer and the buffersize is defined by the input parameter ``udiRxBufferSize``. If more details of the files and direcotries should list, the input parameter ``xWithDetails`` must set to true. Transition to ``TRUE`` on ``xTrigger`` triggers the process to make a directory listing. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbSFTP_FileWriteFromMem
Write a file

**Description:**
This functionblock write the data from the TxBuffer to a file on the remote host specified by ``sRemotePath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to write the transfer buffer to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbSFTP_FileWrite
Write a file

**Description:**
This functionblock write the data form the local file, that is specified by the input parameter ``sLocalPath``, to the remote file, that is specified by the input parameter ``sRemotePath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to write the local file to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbSFTP_FileRename
Rename a file

**Description:**
This functionblock rename the file, that is defined by the input parameter ``sOldFileName``, to the name, that is defined by the input parameter ``sNewFileName``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to rename a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbSFTP_FileRemove
Remove a file

**Description:**
This functionblock remove the file, that is specified by ``sRemotePath``. An error is returned if the file does not exists, the file cannot be removed, or if the user does not have the appropriate privilege level. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbSFTP_FileReadToMem
Read a file

**Description:**
This functionblock reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the RxBuffer, that is specified by the input parameter ``pRxBuffer`` and ``udiRxBufferSize``. If the remote file not exist or the parameter ``pRxBuffer`` and ``udiRxBufferSize`` are 0 then an error occur. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbSFTP_FileRead
Read a file

**Description:**
This functionblock reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the local file, that is specified by the input parameter ``sLocalPath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to read the remote file to a local file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbSFTP_FileAppendFromMem
Append a data from a buffer to a remote file

**Description:**
Thisfunction block append data from the TxBuffer to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. Transition to ``TRUE`` on ``xTrigger`` triggers the process to append the transfer buffer to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbSFTP_FileAppend
Append a local file to a remote file

**Description:**
This functionblock append a local file specified by ``sLocalPath`` to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. Transition to ``TRUE`` on ``xTrigger`` triggers the process to append the local file to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbSFTP_DirRemove
Remove a directory

**Description:**
This functionblock remove remove the directory, that is specified by ``sRemotePath``. An error is returned if the directory does not exists, the dircectory cannot be removed (in use, or not empty), or if the user does not have the appropriate privilege level. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a directory. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbSFTP_DirCreate
Create a directory

**Description:**
This functionblock create a new directory specified by ``sRemotePath``. The Fb create only the last directory in the path. If a directory in the path is missing or the driectory, that schould create, already exists an error occur. Transition to ``TRUE`` on ``xTrigger`` triggers the process to create a new directory. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbSFTP
This function block provides SFTP-Client-Services.

**Description:**
The FbSFTP is the base function block for SFTP-Client-Services. The Fb provide functions like read and write files, rename or remove files and create or remove directories. The inputs of the FbSFTP handle the gerneral information for the SFTP connection and the outputs signal the process and the result of the operations. The operations are triggered by call the specific method for the operation. After a call the methods will return immediately and the SFTP start the operation. .. note:: This function block must called cyclic.

**Methods:**

#### List
List files and directories

This method starts an operation to performs a directory listing. The input parameter ``pRxBuffer`` is pointing to the first element of the buffer and the buffersize is defined by the input parameter ``udiRxBufferSize``. If more details of the files and direcotries should list, the input parameter ``xWithDetails`` must set to true. The status and result of the operation are displayed by the outputs of the FbSFTP. This method has the following return values:

#### FileWriteFromMem
Write a file

This method starts an operation to write the data from the TxBuffer to a file on the remote host specified by ``sRemotePath``. If the remote file exit, it will be overwritten. The status and result of the operation are displayed by the outputs of the FbSFTP. This method has the following return values:

#### FileWrite
Write a file

This method starts an operation to write the data form the local file, that is specified by the input parameter ``sLocalPath``, to the remote file, that is specified by the input parameter ``sRemotePath``. If the remote file exit, it will be overwritten. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbSFTP. This method has the following return values:

#### FileRename
Rename a file

This method starts an operation to rename the file, that is defined by the input parameter ``sOldFileName``, to the name, that is defined by the input parameter ``sNewFileName``. The status and result of the operation are displayed by the outputs of the FbSFTP. This method has the following return values:

#### FileRemove
Remove a file

This method starts an operation to remove the file, that is specified by ``sRemotePath``. An error is returned if the file does not exists, the file cannot be removed, or if the user does not have the appropriate privilege level. The status and result of the operation are displayed by the outputs of the FbSFTP. This method has the following return values:

#### FileReadToMem
Read a file

This method starts an operation to reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the RxBuffer, that is specified by the input parameter ``pRxBuffer`` and ``udiRxBufferSize``. The status and result of the operation are displayed by the outputs of the FbSFTP. This method has the following return values:

#### FileRead
Read a file

This method starts an operation to reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the local file, that is specified by the input parameter ``sLocalPath``. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbSFTP. This method has the following return values:

#### FileAppendFromMem
Append a data from a buffer to a remote file

This method starts an operation to append data from the TxBuffer to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. The status and result of the operation are displayed by the outputs of the FbSFTP. This method has the following return values:

#### FileAppend
Append a local file to a remote file

This method starts an operation to append a local file specified by ``sLocalPath`` to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbSFTP. This method has the following return values:

#### DirRemove
This method starts an operation to remove the directory, that is specified by ``sRemotePath``. An error is returned if the directory does not exists, the dircectory cannot removed (in use, or not empty), or if the user does not have the appropriate privilege level. The status and result of the operation are displayed by the outputs of the FbSFTP. This method has the following return values:

#### DirCreate
Create a directory

This method starts an operation to create a new directory specified by ``sRemotePath``. The method create only the last directory in the path. If a directory in the path is missing or the driectory, that schould create, already exists an error occur. The status and result of the operation are displayed by the outputs of the FbSFTP. This method has the following return values:

### FbFTPES_List
List files and directories

**Description:**
This functionblock performs a directory listing. The linsting includ only those files that match the specification stored in ``sFileSpec``. The input parameter ``pRxBuffer`` is pointing to the first element of the buffer and the buffersize is defined by the input parameter ``udiRxBufferSize``. If more details of the files and direcotries should list, the input parameter ``xWithDetails`` must set to true. Transition to ``TRUE`` on ``xTrigger`` triggers the process to make a directory listing. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPES_FileWriteFromMem
Write a file

**Description:**
This functionblock write the data from the TxBuffer to a file on the remote host specified by ``sRemotePath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to write the transfer buffer to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPES_FileWrite
Write a file

**Description:**
This functionblock write the data form the local file, that is specified by the input parameter ``sLocalPath``, to the remote file, that is specified by the input parameter ``sRemotePath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to write the local file to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbFTPES_FileRename
Rename a file

**Description:**
This functionblock rename the file, that is defined by the input parameter ``sOldFileName``, to the name, that is defined by the input parameter ``sNewFileName``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to rename a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPES_FileRemove
Remove a file

**Description:**
This functionblock remove the file, that is specified by ``sRemotePath``. An error is returned if the file does not exists, the file cannot be removed, or if the user does not have the appropriate privilege level. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPES_FileReadToMem
Read a file

**Description:**
This functionblock reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the RxBuffer, that is specified by the input parameter ``pRxBuffer`` and ``udiRxBufferSize``. If the remote file not exist or the parameter ``pRxBuffer`` and ``udiRxBufferSize`` are 0 then an error occur. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPES_FileRead
Read a file

**Description:**
This functionblock reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the local file, that is specified by the input parameter ``sLocalPath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to read the remote file to a local file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbFTPES_FileAppendFromMem
Append a data from a buffer to a remote file

**Description:**
Thisfunction block append data from the TxBuffer to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. Transition to ``TRUE`` on ``xTrigger`` triggers the process to append the transfer buffer to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPES_FileAppend
Append a local file to a remote file

**Description:**
This functionblock append a local file specified by ``sLocalPath`` to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. Transition to ``TRUE`` on ``xTrigger`` triggers the process to append the local file to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbFTPES_DirRemove
Remove a directory

**Description:**
This functionblock remove remove the directory, that is specified by ``sRemotePath``. An error is returned if the directory does not exists, the dircectory cannot be removed (in use, or not empty), or if the user does not have the appropriate privilege level. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a directory. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPES_DirCreate
Create a directory

**Description:**
This functionblock create a new directory specified by ``sRemotePath``. The Fb create only the last directory in the path. If a directory in the path is missing or the driectory, that schould create, already exists an error occur. Transition to ``TRUE`` on ``xTrigger`` triggers the process to create a new directory. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPS_DirRemove
Remove a directory

**Description:**
This functionblock remove remove the directory, that is specified by ``sRemotePath``. An error is returned if the directory does not exists, the dircectory cannot be removed (in use, or not empty), or if the user does not have the appropriate privilege level. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a directory. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPS_DirCreate
Create a directory

**Description:**
This functionblock create a new directory specified by ``sRemotePath``. The Fb create only the last directory in the path. If a directory in the path is missing or the driectory, that schould create, already exists an error occur. Transition to ``TRUE`` on ``xTrigger`` triggers the process to create a new directory. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPS_List
List files and directories

**Description:**
This functionblock performs a directory listing. The linsting includ only those files that match the specification stored in ``sFileSpec``. The input parameter ``pRxBuffer`` is pointing to the first element of the buffer and the buffersize is defined by the input parameter ``udiRxBufferSize``. If more details of the files and direcotries should list, the input parameter ``xWithDetails`` must set to true. Transition to ``TRUE`` on ``xTrigger`` triggers the process to make a directory listing. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPS_FileWriteFromMem
Write a file

**Description:**
This functionblock write the data from the TxBuffer to a file on the remote host specified by ``sRemotePath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to write the transfer buffer to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPS_FileWrite
Write a file

**Description:**
This functionblock write the data form the local file, that is specified by the input parameter ``sLocalPath``, to the remote file, that is specified by the input parameter ``sRemotePath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to write the local file to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbFTPS_FileRename
Rename a file

**Description:**
This functionblock rename the file, that is defined by the input parameter ``sOldFileName``, to the name, that is defined by the input parameter ``sNewFileName``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to rename a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPS_FileRemove
Remove a file

**Description:**
This functionblock remove the file, that is specified by ``sRemotePath``. An error is returned if the file does not exists, the file cannot be removed, or if the user does not have the appropriate privilege level. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPS_FileReadToMem
Read a file

**Description:**
This functionblock reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the RxBuffer, that is specified by the input parameter ``pRxBuffer`` and ``udiRxBufferSize``. If the remote file not exist or the parameter ``pRxBuffer`` and ``udiRxBufferSize`` are 0 then an error occur. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPS_FileRead
Read a file

**Description:**
This functionblock reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the local file, that is specified by the input parameter ``sLocalPath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to read the remote file to a local file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbFTPS_FileAppendFromMem
Append a data from a buffer to a remote file

**Description:**
Thisfunction block append data from the TxBuffer to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. Transition to ``TRUE`` on ``xTrigger`` triggers the process to append the transfer buffer to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPS_FileAppend
Append a local file to a remote file

**Description:**
This functionblock append a local file specified by ``sLocalPath`` to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. Transition to ``TRUE`` on ``xTrigger`` triggers the process to append the local file to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbFTP_List
List files and directories

**Description:**
This functionblock performs a directory listing. The linsting includ only those files that match the specification stored in ``sFileSpec``. The input parameter ``pRxBuffer`` is pointing to the first element of the buffer and the buffersize is defined by the input parameter ``udiRxBufferSize``. If more details of the files and direcotries should list, the input parameter ``xWithDetails`` must set to true. Transition to ``TRUE`` on ``xTrigger`` triggers the process to make a directory listing. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTP_FileWriteFromMem
Write a file

**Description:**
This functionblock write the data from the TxBuffer to a file on the remote host specified by ``sRemotePath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to write the transfer buffer to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTP_FileWrite
Write a file

**Description:**
This functionblock write the data form the local file, that is specified by the input parameter ``sLocalPath``, to the remote file, that is specified by the input parameter ``sRemotePath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to write the local file to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbFTP_FileRename
Rename a file

**Description:**
This functionblock rename the file, that is defined by the input parameter ``sOldFileName``, to the name, that is defined by the input parameter ``sNewFileName``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to rename a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTP_FileRemove
Remove a file

**Description:**
This functionblock remove the file, that is specified by ``sRemotePath``. An error is returned if the file does not exists, the file cannot be removed, or if the user does not have the appropriate privilege level. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTP_FileReadToMem
Read a file

**Description:**
This functionblock reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the RxBuffer, that is specified by the input parameter ``pRxBuffer`` and ``udiRxBufferSize``. If the remote file not exist or the parameter ``pRxBuffer`` and ``udiRxBufferSize`` are 0 then an error occur. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTP_FileRead
Read a file

**Description:**
This functionblock reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the local file, that is specified by the input parameter ``sLocalPath``. Transition to ``TRUE`` on ``xTrigger`` triggers the process to read the remote file to a local file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbFTP_FileAppendFromMem
Append a data from a buffer to a remote file

**Description:**
Thisfunction block append data from the TxBuffer to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. Transition to ``TRUE`` on ``xTrigger`` triggers the process to append the transfer buffer to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTP_FileAppend
Append a local file to a remote file

**Description:**
This functionblock append a local file specified by ``sLocalPath`` to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. Transition to ``TRUE`` on ``xTrigger`` triggers the process to append the local file to the remote file. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT://

### FbFTP_DirRemove
Remove a directory

**Description:**
This functionblock remove remove the directory, that is specified by ``sRemotePath``. An error is returned if the directory does not exists, the dircectory cannot be removed (in use, or not empty), or if the user does not have the appropriate privilege level. Transition to ``TRUE`` on ``xTrigger`` triggers the process to remove a directory. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTP_DirCreate
Create a directory

**Description:**
This functionblock create a new directory specified by ``sRemotePath``. The Fb create only the last directory in the path. If a directory in the path is missing or the driectory, that schould create, already exists an error occur. Transition to ``TRUE`` on ``xTrigger`` triggers the process to create a new directory. The function block resets ``xTrigger`` to ``FALSE`` again after it has finished the process. If something went wrong during the process ``xTrigger`` resets to ``FALSE`` and ``xError`` is set to ``TRUE`` . The output ``xBusy`` indicates that the function block is still processing.

### FbFTPS
This function block provides FTPS-Client-Services.

**Description:**
The FbFTPS is the base function block for FTPS-Client-Services. The Fb provide functions like read and write files, rename or remove files and create or remove directories. The inputs of the FbFTPS handle the gerneral information for the FTPS connection and the outputs signal the process and the result of the operations. The operations are triggered by call the specific method for the operation. After a call the methods will return immediately and the FbFTPS start the operation. .. note:: This function block must called cyclic.

**Methods:**

#### List
List files and directories

This method starts an operation to performs a directory listing. The linsting includ only those files that match the specification stored in``sFileSpec``. The input parameter ``pRxBuffer`` is pointing to the first element of the buffer and the buffersize is defined by the input parameter ``udiRxBufferSize``. If more details of the files and direcotries should list, the input parameter ``xWithDetails`` must set to true. The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

#### FileWriteFromMem
Write a file

This method starts an operation to write the data from the TxBuffer to a file on the remote host specified by ``sRemotePath``. If the remote file exit, it will be overwritten. The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

#### FileWrite
Write a file

This method starts an operation to write the data form the local file, that is specified by the input parameter ``sLocalPath``, to the remote file, that is specified by the input parameter ``sRemotePath``. If the remote file exit, it will be overwritten. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

#### FileRename
Rename a file

This method starts an operation to rename the file, that is defined by the input parameter ``sOldFileName``, to the name, that is defined by the input parameter ``sNewFileName``. The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

#### FileRemove
Remove a file

This method starts an operation to remove the file, that is specified by ``sRemotePath``. An error is returned if the file does not exists, the file cannot be removed, or if the user does not have the appropriate privilege level. The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

#### FileReadToMem
Read a file

This method starts an operation to reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the RxBuffer, that is specified by the input parameter ``pRxBuffer`` and ``udiRxBufferSize``. The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

#### FileRead
Read a file

This method starts an operation to reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the local file, that is specified by the input parameter ``sLocalPath``. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

#### FileAppendFromMem
Append a data from a buffer to a remote file

This method starts an operation to append data from the TxBuffer to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

#### FileAppend
Append a local file to a remote file

This method starts an operation to append a local file specified by ``sLocalPath`` to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

#### DirCreate
Create a directory

This method starts an operation to create a new directory specified by ``sRemotePath``. The method create only the last directory in the path. If a directory in the path is missing or the driectory, that schould create, already exists an error occur. The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

#### DirRemove
This method starts an operation to remove the directory, that is specified by ``sRemotePath``. An error is returned if the directory does not exists, the dircectory cannot removed (in use, or not empty), or if the user does not have the appropriate privilege level. The status and result of the operation are displayed by the outputs of the FbFTPS. This method has the following return values:

### FbFTP
This function block provides FTP-Client-Services.

**Description:**
The FbFTP is the base function block for FTP-Client-Services. The Fb provide functions like read and write files, rename or remove files and create or remove directories. The inputs of the FbFTP handle the gerneral information for the FTP connection and the outputs signal the process and the result of the operations. The operations are triggered by call the specific method for the operation. After a call the methods will return immediately and the FbFTP start the operation. .. note:: This function block must called cyclic.

**Methods:**

#### FileReadToMem
Read a file

This method starts an operation to reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the RxBuffer, that is specified by the input parameter ``pRxBuffer`` and ``udiRxBufferSize``. The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

#### FileWrite
Write a file

This method starts an operation to write the data form the local file, that is specified by the input parameter ``sLocalPath``, to the remote file, that is specified by the input parameter ``sRemotePath``. If the remote file exit, it will be overwritten. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

#### FileWriteFromMem
Write a file

This method starts an operation to write the data from the TxBuffer to a file on the remote host specified by ``sRemotePath``. If the remote file exit, it will be overwritten. The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

#### FileRemove
Remove a file

This method starts an operation to remove the file, that is specified by ``sRemotePath``. An error is returned if the file does not exists, the file cannot be removed, or if the user does not have the appropriate privilege level. The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

#### FileAppendFromMem
Append a data from a buffer to a remote file

This method starts an operation to append data from the TxBuffer to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

#### FileRead
Read a file

This method starts an operation to reads the data form the remote file, that is specified by the input parameter ``sRemotePath``, and stored it in the local file, that is specified by the input parameter ``sLocalPath``. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

#### FileRename
Rename a file

This method starts an operation to rename the file, that is defined by the input parameter ``sOldFileName``, to the name, that is defined by the input parameter ``sNewFileName``. The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

#### FileWrite2
Write a file

This method starts an operation to write the data form the local file, that is specified by the input parameter ``sLocalPath``, to the remote file, that is specified by the input parameter ``sRemotePath``. In contrast to FileWrite() this method set the last modification date of the file to be transferred at the server with the command 'MFMT'. If the remote file exit, it will be overwritten. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// .. note:: The ftp server must support the MFMT command, otherwise an error is returned. The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

#### List
List files and directories

This method starts an operation to performs a directory listing. The linsting includ only those files that match the specification stored in``sFileSpec``. The input parameter ``pRxBuffer`` is pointing to the first element of the buffer and the buffersize is defined by the input parameter ``udiRxBufferSize``. If more details of the files and direcotries should list, the input parameter ``xWithDetails`` must set to true. The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

#### FileAppend
Append a local file to a remote file

This method starts an operation to append a local file specified by ``sLocalPath`` to the end of a file on the remote host specified by ``sRemotePath``. If the remote file dosen´t exit, it will be created. For ''sLocalPath'' you can use the following prefixes, known form WagoAppFileDir: - HOME:// - CARD:// - TEMP:// - ROOT:// The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

#### DirRemove
This method starts an operation to remove the directory, that is specified by ``sRemotePath``. An error is returned if the directory does not exists, the dircectory cannot removed (in use, or not empty), or if the user does not have the appropriate privilege level. The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

#### DirCreate
Create a directory

This method starts an operation to create a new directory specified by ``sRemotePath``. The method create only the last directory in the path. If a directory in the path is missing or the driectory, that schould create, already exists an error occur. The status and result of the operation are displayed by the outputs of the FbFTP. This method has the following return values:

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbFTPES: FbFTPES;
END_VAR

// Basic function block usage
fbFbFTPES(
    // Configure inputs as needed
);

// Check status
IF fbFbFTPES.xValid THEN
    // Operation successful
END_IF

IF fbFbFTPES.xError THEN
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

