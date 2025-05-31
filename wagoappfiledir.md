# WagoAppFileDir v1.6.2.1

## Overview
WAGO PLC library providing WagoAppFileDir functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbBehaviourModel_FileDir_ChannelledTrigger
Channelled Trigger-model with ``oStatus``.

**Description:**
This base model is completely identical to 'WagoChannelledTrigger' with the only difference that the trigger variable and the status output are named slightly differently here. It is composed of two separated sub-modules: Channel: This part controls the opening and closing of an associated communication channel. The description of

### FbGeneralFile_ReadString_mod
Modular FB for reading a single line of text

**Description:**
This FB implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModel_WagoAppExecute>`, as explained in more detail in :ref:`FbGeneralFile_Open_mod`. On the rising edge of the input *xExecute* the FB reads a string of bytes from the file until an end-of-line is encountered. End-of-line is denoted by the byte <LF>, or <CR>, or the combination of both. The end-of-line characters are not part of the output string.

### FbGeneralFile_WriteString_mod
Modular FB for writing data from a string

**Description:**
This FB implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModel_WagoAppExecute>`, as explained in more detail in :ref:`FbGeneralFile_Open_mod`. On the rising edge of the input *xExecute* the FB writes a string of bytes to the file. The number of bytes which are to be written is given by the length of the string. This could be any number between 0 and 255. Note No EOL-indicator will be written unless explicitely contained in the string. The terminating zero is not written to the file either.

### FbGeneralFile_WriteByte_mod
Modular FB for writing a single byte.

**Description:**
This FB implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModel_WagoAppExecute>`, as explained in more detail in :ref:`FbGeneralFile_Open_mod`. On the rising edge of the input *xExecute* the FB writes one data byte to the file.

### FbGeneralFile_ReadByte_mod
Reads a single byte.

**Description:**
This FB implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModel_WagoAppExecute>`, as explained in more detail in :ref:`FbGeneralFile_Open_mod`. On the rising edge of the input *xExecute* the FB reads one data byte from the file.

### FbGeneralFile_GetPos_mod
Modular FB for retrieving the positition within a file.

**Description:**
This FB implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModel_WagoAppExecute>`, as explained in more detail in :ref:`FbGeneralFile_Open_mod`. On a rising edge of the input *xExecute* the FB retrieves the position of the file pointer. If the position of the file index is invalid or cannot be retrieved, -1 is returned.

### FbGeneralFile_Seek_mod
Modular FB for setting the read and write position.

**Description:**
This FB implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModel_WagoAppExecute>`, as explained in more detail in :ref:`FbGeneralFile_Open_mod`. On the rising edge of the input *xExecute* the FB sets the file pointer to a new position. The file pointer is an internal structure which determines the location inside a file from where data is read or where data is written to. The desired new position is given by the input liPos. This number is either relative to the start of the file, or relative to the current end of the file or relative to the current file pointer position. The input *whence* (type :ref:`eSeekMode`, defined in WagoTypesCommon) determines which reference is used here.

### FbGeneralFile_Write_mod
Modular FB for writing to a file

**Description:**
This FB implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModel_WagoAppExecute>`, as explained in more detail in :ref:`FbGeneralFile_Open_mod`. On the rising edge of the input ``Execute`` the FB writes a number of bytes to the file. The input ``pTxBuffer`` represents the location of the data while ``udiTxNBytes`` is the number of bytes to be written.

### FbGeneralFile_Read_mod
Modular FB for reading from a file

**Description:**
This FB implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModel_WagoAppExecute>`, as explained in more detail in :ref:`FbGeneralFile_Open_mod`. On the rising edge of the input *xExecute* the FB transfers a number of bytes from the file into the data buffer. The inputs *pRxBuffer* and *udiRxBufferSize* denote the location of the buffer and its size, respectively. The output *udiRxNBytes* indicates the number of bytes actually transferred, which could be less than the requested number if the end of file is reached.

### FbGeneralFile_Close_mod
Modular FB for closing a file.

**Description:**
This FB implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModel_WagoAppExecute>`, as explained in more detail in :ref:`FbGeneralFile_Open_mod`. On a rising edge of the input *xExecute* the FB closes the file.

### FbGeneralFile_Open_mod
Modular FB for opening a file.

**Description:**
This FB implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModel_WagoAppExecute>`. With the rising edge of xExecute, the file is opened in a mode defined by the input parameters. Please, refer to the section 'Type Definition' or to the library WagoTypesCommon for details about file modes. (The input xExclusive prepares this FB for a future feature. It must always be FALSE.) Modular FBs in this section are designed to each represent each a single operation step with each instance. The 'xDone' output of the first instance triggers the execution of the following instance. Thus we finally get a chain of steps which is processed virtually sequentially, as shown in the following example. Please note that for production code appropriate error handling should be provided which is not shown here. .. figure:: ../../Images/__fbModWriteChain.png :width: 30 % :align: center :alt: fbModWriteChain Chain of modular FBs The in-out variable 'Instance' must be connected to an instance of an :ref:`FbGeneralFile`. The body of that 'Instance' must be operated cyclically, but no further stimulus to this Instance need be applied,because the modular FBs will take care of this internally. All FBs in such a 'chain' as indicated in the figure above must be connected to the same 'Instance'-FB.

### FbChangeWorkingDirectory
Changes the current Working Directory to a given path.

**Description:**
This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbGetWorkingDirectory
Retrieves the name of the current Working Directory.

**Description:**
This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected. There are no error codes expected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbMoveDirectory
Moves a complete directory structure from one location to another.

**Description:**
If the new path does not exist, it will be created. If a directory already exists with the same name, the old directory structure will be overwritten. This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbMoveFile
Moves a file from one location to another but keeps its name.

**Description:**
If the new path does not exist, it will be created. This FB may also move files between different media ('cross-device'). This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbRename
Renames a file or directory within a given directory structure.

**Description:**
The addressed resource (file or directory) is renamed (but not moved within the directory structure). If a file with the new name already exists, that old file will first be deleted (overwritten), if the xOverwriteEnable-Flag is set. Otherwise this function will fail. Non-empty directories will not be overwritten, because it is very likely that the potentially existing content in the existing dirctory may need special treatment anyway. An existing directory will not be overwritten by a regular file and vice versa. This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbRemoveDirectory
Removes a directory with all its contents.

**Description:**
The directory which is to be removed need not be empty. All its contents will also be removed. This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbMakeDirectory
Creates a new directory.

**Description:**
If the creation of the new directory requires the creation of new parent directories, these will also be created. This FB is started with the method ``Start()`` which carries all input parameters. Output parameters are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbCopyFile
Copies one file to a second location.

**Description:**
The 'sDestinationName' may denote a file name or a directory name, in which case the name of the file remains the same and only the path changes. If the new file name needs the creation of parent directories, these will be created. If the destination file already exists, this function fails with EEXIST unless the xOverwrite flag is set. In that case, this function tries to delete the existing file. If deletion fails, the function will again fail with EEXIST. This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbGetFreeSpaceInDirectory
Retrieves the number of freely usable bytes in the given directory.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbGetFileProperties
Retrieves the status if a named file or directory.

**Description:**
This FB retrieves detailed information about a file or directory. The output is provided as :ref:`typFileProperties` which is defined in WagoTypesCommon.library. This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected. The FB returns one of the codes shown below.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbSetFileProperties
Sets or clears the properties or attributes of a file.

**Description:**
The properties which are to be changes are passed in a :ref:`typFileProperties` structure. *Typical usage:* This FB is typically fed with the results of :ref:`FbGgetFileProperty` before setting the file properties. Please note that not all attribute can be changed. e.g.: xDirectory may NOT be changed. Changeable items are typically: - dtLastModification - xArchive - xHidden - xReadonly - xExclusive Not Changeable are: - sFileName - uliSize - xDirectory This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbCheckDirectoryExists
Checks if a named directory exists or not.

**Description:**
The results are provided by the output variables. If the named resource is not a directory but a file, this counts as 'does not exist'. No errors are expected. This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbCheckFileExists
Checks if a named regular file exists or not.

**Description:**
The results are provided by the output variables. If the named resource is not a file but a directory, this counts as 'does not exist'. No errors are expected. This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbDirectoryReader
Scans a directory and retrieves informations about its contents.

**Description:**
*Usage*: 1. Open the directory with the Open() method. 2. Read data with Read() until ENODATA is indicated. 3. Apply Close(). When the last entry has been read or the directory is empty, the following Read() returns ENODATA. Special system entries, such as '.' and '..' are generally skipped. Please note that this FB scans only one hierarchical level of the directory, i.e. the contents of subdirectories are *not* scanned. The returned data is returned as :ref:`typFileProperties`. If some of these properties are not supported by the addressed file system, they carry a reasonable default value. E.g. for non-windows file systems, the xArchive flag will always be FALSE if the file system does not contain such an attribute. *Asynchronous Behaviour:* The methods Open(), Read(), and Close() will return immediately, but they leave their jobs in the asynchronous domain, which is indicated by the output ``xBusy``. While ``xBusy`` is TRUE no further methods must be called. The termination of the asynchronous execution is indicated by ``xTerminated`` . The read data structure, ``eResult``, and other outputs are valid only after ``xTerminated`` is TRUE.

**Methods:**

#### Close
Closes the directory again.

This method returns 0 on Success and EBUSY if the FB is busy with the job of a previously executed method. Results of the opening process are delivered asynchronously.

#### Read
Reads one directory entry.

This method returns 0 on Success and EBUSY if the FB is busy with the job of a previously executed method. Results of the opening process are delivered asynchronously as 'eResult' output in the FB. The information about the read directory content is provided in the FB output 'FileProperties' as explained in the general FB description.

#### Open
Opens a directory for reading.

The input string ``sDirName`` denotes the name of the directory. (It does not matter, if the directory carries a trailing slash or not.) This method returns 0 on Success and EBUSY if the FB is busy with the job of a a previously executed method. Results of the opening process are delivered asynchronously.

### FbRemoveFile
Removes a file.

**Description:**
It is legal to remove a file which is beeing kept open by another process. When the other process closes its file handle, the subsequently passed data is lost without notice. Any restrictions about write protection are not honored. This FB is started with the method ``Start()`` which carries all input parameters. Output values are valid after the output ``xTerminated`` is set by this FB. While ``xBusy`` is set, further calls of ``Start()`` will be rejected.

**Methods:**

#### Start
Initiates the action of the FB.

The results are valid as FB outputs after the FB has set ``xTerminated`` to TRUE.

### FbGeneralFile
Base FB for file handling with comprehensive functionality.

**Description:**
As all functions are triggered using methods, this FB has no dedicated input variables. *Usage:* 1. File operations are initiated by trigger methods Open(), Close(), Write(), etc which also deliver parameters to the FbGeneralFile. 2. When these Functions are called, the underlying functionality is carried out in the background and the trigger methods return immediately. The application has to cyclically observe ``xTerminated`` in order to determine whether the triggered functionality has been completed or not. While ``xBusy`` is ``TRUE``, all further triggering calls are rejected with EBUSY. 3. Results of the operations are delivered at the outputs of the FB, after xTerminated is set. *Example:* Writing some data into a file :: TYPE eProgress // for the state machine ( idle :

**Methods:**

#### GetPos
Retrieves the actual position of the file pointer.

After termination, the following outputs of the FB are relevant:

#### Seek
Sets the filepointer to the desired position.

The position of the next read- or write-access to the file will be set to a new value. The desired position is given relative to either the beginning of the file (absolute positioning), to the end of the file (for writing data at the end of the file), or relative to the actual read/write position. That behaviour is controlled by the parameter :ref:`whence : eSeekMode <eSeekMode>`. If the file pointer is set beyond the end of the file, the file will be filled up with zeroes on the next write() access. It will not be filled up without a write operation. If the desired effective file position points to an address before the start of the file, the result of this operation is EACCES and the file pointer remains unchanged.

#### ReadString
Reads a line of text from an open text file.

This method reads bytes from a file until an end-of-line symbol is encountered and stores the result into the output ``sLine`` of the FB. End-of-line could be <LF>, or a <CR>, or a combination of both - that will be detected automatically. The end-of-line-character(s) will not be included in the result string. The parameter uiSize denotes the size of the string buffer. When the size of the logical line exceeds the size of the string buffer, the FB delivers ENOSPC. Valid values for uiSize are 1..255. Others will produce EINVAL. This method is similar to Read(), but the amount of data actually read is represented as the length of the output string and it depends on the actual file contents.

#### ReadByte
Reads a single byte from an open file.

If the file is not open or EOF is reached, 0 is returned as data byte.

#### Read
Reads data from an open file.

#### WriteString
Writes a string to an open file.

This is a convenience function for 'write', which accepts the data as a string of characters. This method is equivalent to Write() but the size of the data is implicitly given by the string length.

#### WriteByte
Writes a single byte to an open file.

This method is equivalent to a regular Write() call with a fixed amount of one byte of data.

#### Write
Writes to an open file.

The data to be written is specified by a pointer to the location of the transmit buffer and by the size of the data (in bytes). The file must have been opened previously for write access using the open() method.

#### Close
Closes the File.

When data is written to a file, the actual transfer of the data to the real media may be postponed until the FB receives this close() call. If an FbSysFile is not open, an additional close() does no harm, but it ensures that the FB is closed in every case. Once a file is opened, it should be closed again after all operations are done. *Output after termination:* After termination, the following outputs contain relevant data:

#### Open
Opens a file for reading and / or writing.

The method Open() specifies which file is to be accessed and the modalities of the intended access. Open() must be called first before any other method of this FB can be successfully executed. If any access is attempted to an FbGeneralFile which has not been successfully opened, that method will reply EBADFD ('Bad file number or file not open'). After the file operations have been finished, a corresponding Close() method should be called in order to terminate the FB regularly and to release the internal resources. When Open() is applied to an already open file, the previously opened file will be closed and a regular Open() is performed in the now unassigned FB. (Note that the latter Open() call may fail, so the application might end up with a closed FB after trying to open an already open file FB.) Note: The result code of the Open() method represents the success of scheduling the open() call itself, but not the success of the open procedure, because the latter is not known at the time of the call. The result code of successfully or unsuccessfully opening a file is represented by the xError-output of the FB after ``xTerminated`` has signalled termination. The File can be opened in different access modes (:ref:`eAccMode : eFileAccessMode <eFileAccessMode>`). In all writable modes (not FAM_Read), the file will be created if it does not exist. The third parameter controls the timing of write processes to the physical media (:ref:`eSyncMode : eFileSyncMode <eFileSyncMode>`). On success, the FbGeneralFile transits to the state 'Open' and further operations (such as write, read, close) may be performed upon this instance.

## Compact Function Blocks

### FbWriteWholeFile_cpt
Writes a whole file at once.

**Description:**
This FB writes a complete block of data into a file and closes it afterwards. The FB implements the behaviour model :ref:`'WagoTrigger' <FbBehaviourModel_WagoAppTrigger>`, i.e. setting ``xTrigger`` to TRUE initiates the whole process. The FB signals the finishing of the write process by setting ``xTrigger`` to FALSE again. The other inputs carry information about the file name and the data.

### FbReadWholeFile_cpt
Reads a complete file into a buffer.

**Description:**
This FB reads a whole file into a buffer. It implements the behaviour model :ref:`'WagoTrigger' <FbBehaviourModel_WagoAppTrigger>`, i.e. a transition to TRUE on *xTrigger* triggers the read process. The FB resets *xTrigger* to FALSE again, after it has finished its read process. If the file fits into the given buffer, the output *udiRxNBytes* indicates the size of the file and xEofReached is set to TRUE. If the given buffer is too small, only the beginning of the file is read and the output *xEofReached* remains FALSE. It is not possible to read file contents successively with this FB. The status output delivers one of the codes shown below.

### FbSimpleReadFile_cpt
Compact FB for reading a binary file.

**Description:**
This FB reads a file in consecutive blocks. It implements the behaviour model :ref:`'WagoChannelledTrigger' <FbBehaviourModel_FileDir_ChannelledTrigger>`: While the Input ``xOpen`` is ``TRUE``, the file is kept open. This state is reflected by the output ``xIsOpen``. The output ``xIsIdle`` indicates that the FB is ready for opening the file. While ``xIsIdle`` is ``FALSE`` and ``xIsOpen`` is also ``FALSE``, the FB is in some transient state, e.g. in the process of opening or closing a file. xOpen *should only* be changed from ``FALSE`` to ``TRUE`` if ``xIsIdle`` is TRUE. With the falling edge of ``xOpen`` the file is closed again. A FALSE to TRUE transition on the input ``xTrigger`` initiates a read process from the open file. The inputs ``pRxBuffer`` and ``udiRxBufferSize`` specify a buffer space for the read data. The output ``udiRxNBytes`` indicates how many bytes are actually read. This is normally the same as udiRxBufferSize, but if the end of the file was reached, it could be less. The output ``xEofReached`` denotes that the end of the file has been reached by the last read process. It is raised to ``TRUE`` just after the last byte of the file is read.

### FbSimpleWriteFile_cpt
Compact FB for sequentially writing a file.

**Description:**
This FB opens a file in write mode and writes content to the file in consecutive blocks. It implements the behaviour model :ref:`'WagoChannelledTrigger' <FbBehaviourModel_FileDir_ChannelledTrigger>`: While the Input ``xOpen`` is ``TRUE``, the file is kept open in 'FAM_Write'-mode. If the file existed previously, it will be erased. The open state is reflected by the output 'xIsOpen'. The output ``xIsIdle`` indicates that the FB is ready for opening the file. While ``xIsIdle`` is ``FALSE`` and ``xIsOpen`` is also ``FALSE``, the FB is in some temporary state, e.g. in the process of opening or closing a file. ``xOpen`` *should only* be changed from ``FALSE`` to ``TRUE`` if ``xIsIdle`` is ``TRUE``. With the falling edge of xOpen the file is closed again. A FALSE to TRUE transition on the input 'xTrigger' initiates a write process to the open file. The inputs 'pTxBuffer' and 'udiTxNBytes' specify the location and the amount of the write data.

### FbDirectoryReader_cpt
Reads the contents of a directory sequentially.

**Description:**
This FB reads a directory sequentially and delivers the status of each directory entry into a typed buffer space :ref:`'typFileProperties' <typFileProperties>`. It implements the behaviour model :ref:`'WagoChannelledTrigger' <FbBehaviourModel_FileDir_ChannelledTrigger>`, i.e. a transition from FALSE to TRUE at the input ``xOpen`` starts the reading process. With the falling edge of xOpen the FB is closed again. Once the FB is open, each FALSE to TRUE transition will fill the result buffer 'typPropertyBuffer' with the properties of the next entry in the directory. System entries as '.' and '..' will be skipped. A TRUE at the output ``xEofReached`` indicates that all entries of a directory have been read. After this point, further ``xTrigger`` edges will deliver empty result buffers and the code ENODATA at the status output.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbBehaviourModel_FileDir_ChannelledTrigger: FbBehaviourModel_FileDir_ChannelledTrigger;
END_VAR

// Basic function block usage
fbFbBehaviourModel_FileDir_ChannelledTrigger(
    // Configure inputs as needed
);

// Check status
IF fbFbBehaviourModel_FileDir_ChannelledTrigger.xValid THEN
    // Operation successful
END_IF

IF fbFbBehaviourModel_FileDir_ChannelledTrigger.xError THEN
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

