# WagoAppSunspec v1.0.1.12

## Overview
SunSpec communication library for solar inverters via Modbus TCP/RTU protocol.

**Key Features:**
- Master/slave communication with SunSpec devices
- Support for multiple PICS implementations
- Automatic device discovery and model detection
- Read/write operations for supported data points
- Inverter, meter, and storage system support

## Core Function Blocks

### FbSunspecPICS_S802
The function block ``FbSunspecPICS_S802`` enables evaluation of the PICS S802 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS S802. The readable values of the PICS S802 are available in the output structure ``typPICS_S802``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER708
The function block ``FbSunspecPICS_DER708`` enables evaluation of the PICS DER708 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER708. The readable values of the PICS DER708 are available in the output structure ``typPICS_DER708``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER712
The function block ``FbSunspecPICS_DER712`` enables evaluation of the PICS DER712 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER712. The readable values of the PICS DER712 are available in the output structure ``typPICS_DER712``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER706
The function block ``FbSunspecPICS_DER706`` enables evaluation of the PICS DER706 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER706. The readable values of the PICS DER706 are available in the output structure ``typPICS_DER706``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER704
The function block ``FbSunspecPICS_DER704`` enables evaluation of the PICS DER704 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER704. The readable values of the PICS DER704 are available in the output structure ``typPICS_DER704``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER710
The function block ``FbSunspecPICS_DER710`` enables evaluation of the PICS DER710 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER710. The readable values of the PICS DER710 are available in the output structure ``typPICS_DER710``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunSpec_Model
### FbSunspecMaster
The block ``FbSunspecMaster`` enables communication to a Sunspec slave via Modbus TCP/RTU.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The block can be used individually to identify a Sunspec device, and (in combination with one of the following PICS blocks) for reading out the PICS supported by the device. For the second case, the input ``bPort`` is used for the assignment to the PICS function blocks. The input structure ``typConfigParameters`` defines the modbus communication type and holds the settings for Modbus TCP and Modbus RTU. Serial settings are initialized to standard parameter from Sunspec specification. Some typical settings are: +---------------+---------------+---------------+ |

### FbSunspecPICS_DER713
The function block ``FbSunspecPICS_DER713`` enables evaluation of the PICS DER713 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER713. The readable values of the PICS DER713 are available in the output structure ``typPICS_DER713``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER709
The function block ``FbSunspecPICS_DER709`` enables evaluation of the PICS DER709 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER709. The readable values of the PICS DER709 are available in the output structure ``typPICS_DER709``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER707
The function block ``FbSunspecPICS_DER707`` enables evaluation of the PICS DER707 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER707. The readable values of the PICS DER707 are available in the output structure ``typPICS_DER707``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER705
The function block ``FbSunspecPICS_DER705`` enables evaluation of the PICS DER705 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER705. The readable values of the PICS DER705 are available in the output structure ``typPICS_DER705``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER715
The function block ``FbSunspecPICS_DER715`` enables evaluation of the PICS DER715 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER715. The readable values of the PICS DER715 are available in the output structure ``typPICS_DER715``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER702
The function block ``FbSunspecPICS_DER702`` enables evaluation of the PICS DER702 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER702. The readable values of the PICS DER702 are available in the output structure ``typPICS_DER702``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER711
The function block ``FbSunspecPICS_DER711`` enables evaluation of the PICS DER711 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER711. The readable values of the PICS DER711 are available in the output structure ``typPICS_DER711``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER714
The function block ``FbSunspecPICS_DER714`` enables evaluation of the PICS DER714 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER714. The readable values of the PICS DER714 are available in the output structure ``typPICS_DER714``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER703
The function block ``FbSunspecPICS_DER703`` enables evaluation of the PICS DER703 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER703. The readable values of the PICS DER703 are available in the output structure ``typPICS_DER703``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_DER701
The function block ``FbSunspecPICS_DER701`` enables evaluation of the PICS DER701 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS DER701. The readable values of the PICS DER701 are available in the output structure ``typPICS_DER701``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_NC010
The function block ``FbSunspecPICS_NC010`` enables evaluation of the PICS NC010 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS NC010. An active communication is signaled by the output ``xBusy``. When the communication has been successfully completed, this is indicated via the ``xValid`` output and the values read out can be used. An error that occurs during the communication is displayed via the ``xError`` output. The readable values of the PICS NC010 are available in the output structure ``typPICS_NC010``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_I101
The function block ``FbSunspecPICS_I101`` enables evaluation of the PICS I101 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS I101. The readable values of the PICS I101 are available in the output structure ``typPICS_I101``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_I102
The function block ``FbSunspecPICS_I102`` enables evaluation of the PICS I102 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS I102. The readable values of the PICS I102 are available in the output structure ``typPICS_I102``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_I103
The function block ``FbSunspecPICS_I103`` enables evaluation of the PICS I103 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS I103. The readable values of the PICS I103 are available in the output structure ``typPICS_I103``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_NC018
The function block ``FbSunspecPICS_NC018`` enables evaluation of the PICS NC018 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS NC018. The readable values of the PICS NC018 are available in the output structure ``typPICS_NC018``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_NC013
The function block ``FbSunspecPICS_NC013`` enables evaluation of the PICS NC013 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS NC013. The readable values of the PICS NC013 are available in the output structure ``typPICS_NC013``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_NC016
The function block ``FbSunspecPICS_NC016`` enables evaluation of the PICS NC016 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS NC016. The readable values of the PICS NC016 are available in the output structure ``typPICS_NC016``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_NC015
The function block ``FbSunspecPICS_NC015`` enables evaluation of the PICS NC015 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS NC015. The readable values of the PICS NC015 are available in the output structure ``typPICS_NC015``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_NC012
The function block ``FbSunspecPICS_NC012`` enables evaluation of the PICS NC012 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS NC012. The readable values of the PICS NC012 are available in the output structure ``typPICS_NC012``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_I113
The function block ``FbSunspecPICS_I113`` enables evaluation of the PICS I113 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS I113. The readable values of the PICS I113 are available in the output structure ``typPICS_I113``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_NC014
The function block ``FbSunspecPICS_NC014`` enables evaluation of the PICS NC014 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS NC014. The readable values of the PICS NC014 are available in the output structure ``typPICS_NC014``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_NC017
The function block ``FbSunspecPICS_NC017`` enables evaluation of the PICS NC017 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS NC017. The readable values of the PICS NC017 are available in the output structure ``typPICS_NC017``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_I160
The function block ``FbSunspecPICS_I160`` enables evaluation of the PICS I160 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS I160. The readable values of the PICS I160 are available in the output structure ``typPICS_I160``. The PICS I160 can contain several repeating data blocks, placed in the output structure ``typPICS_I160``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_I160``, the variable ``ParameterList.MAX_BLOCKS_I160`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_I112
The function block ``FbSunspecPICS_I112`` enables evaluation of the PICS I112 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS I112. The readable values of the PICS I112 are available in the output structure ``typPICS_I112``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_I111
The function block ``FbSunspecPICS_I111`` enables evaluation of the PICS I111 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS I111. The readable values of the PICS I111 are available in the output structure ``typPICS_I111``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_NC019
The function block ``FbSunspecPICS_NC019`` enables evaluation of the PICS NC019 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS NC019. The readable values of the PICS NC019 are available in the output structure ``typPICS_NC019``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC122
The function block ``FbSunspecPICS_IC122`` enables evaluation of the PICS IC122 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC122. The readable values of the PICS IC122 are available in the output structure ``typPICS_IC122``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC123
The function block ``FbSunspecPICS_IC123`` enables evaluation of the PICS IC123 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC123. The input / output data of the PICS IC123 is made available in the input / output structure ``typPICS_IC123``. If any of the write-privileged values are filled with new data, they are automatically detected and written to the Sunspec device the next cycle. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC121
The function block ``FbSunspecPICS_IC121`` enables evaluation of the PICS IC121 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC121. The input / output data of the PICS IC121 is made available in the input / output structure ``typPICS_IC121``. If any of the write-privileged values are filled with new data, they are automatically detected and written to the Sunspec device the next cycle. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC120
The function block ``FbSunspecPICS_IC120`` enables evaluation of the PICS IC120 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC120. The readable values of the PICS IC120 are available in the output structure ``typPICS_IC120``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC124
The function block ``FbSunspecPICS_IC124`` enables evaluation of the PICS IC124 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC124. The input / output data of the PICS IC124 is made available in the input / output structure ``typPICS_IC124``. If any of the write-privileged values are filled with new data, they are automatically detected and written to the Sunspec device the next cycle. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC125
The function block ``FbSunspecPICS_IC125`` enables evaluation of the PICS IC125 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC125. The input / output data of the PICS IC125 is made available in the input / output structure ``typPICS_IC125``. If any of the write-privileged values are filled with new data, they are automatically detected and written to the Sunspec device the next cycle. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC126
The function block ``FbSunspecPICS_IC126`` enables evaluation of the PICS IC126 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC126. The readable values of the PICS IC126 are available in the output structure ``typPICS_IC126``. The PICS IC126 can contain several repeating data blocks, placed in the output structure ``typPICS_IC126``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC126``, the variable ``ParameterList.MAX_BLOCKS_IC126`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC127
The function block ``FbSunspecPICS_IC127`` enables evaluation of the PICS IC127 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC127. The input / output data of the PICS IC127 is made available in the input / output structure ``typPICS_IC127``. If any of the write-privileged values are filled with new data, they are automatically detected and written to the Sunspec device the next cycle. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC128
The function block ``FbSunspecPICS_IC128`` enables evaluation of the PICS IC128 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC128. The input / output data of the PICS IC128 is made available in the input / output structure ``typPICS_IC128``. If any of the write-privileged values are filled with new data, they are automatically detected and written to the Sunspec device the next cycle. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC129
The function block ``FbSunspecPICS_IC129`` enables evaluation of the PICS IC129 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC129. The readable values of the PICS IC129 are available in the output structure ``typPICS_IC129``. The PICS IC129 can contain several repeating data blocks, placed in the output structure ``typPICS_IC129``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC129``, the variable ``ParameterList.MAX_BLOCKS_IC129`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC130
The function block ``FbSunspecPICS_IC130`` enables evaluation of the PICS IC130 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC130. The readable values of the PICS IC130 are available in the output structure ``typPICS_IC130``. The PICS IC130 can contain several repeating data blocks, placed in the output structure ``typPICS_IC130``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC130``, the variable ``ParameterList.MAX_BLOCKS_IC130`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC131
The function block ``FbSunspecPICS_IC131`` enables evaluation of the PICS IC131 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC131. The readable values of the PICS IC131 are available in the output structure ``typPICS_IC131``. The PICS IC131 can contain several repeating data blocks, placed in the output structure ``typPICS_IC131``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC131``, the variable ``ParameterList.MAX_BLOCKS_IC131`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC132
The function block ``FbSunspecPICS_IC132`` enables evaluation of the PICS IC132 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC132. The readable values of the PICS IC132 are available in the output structure ``typPICS_IC132``. The PICS IC132 can contain several repeating data blocks, placed in the output structure ``typPICS_IC132``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC132``, the variable ``ParameterList.MAX_BLOCKS_IC132`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC133
The function block ``FbSunspecPICS_IC133`` enables evaluation of the PICS IC133 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC133. The readable values of the PICS IC133 are available in the output structure ``typPICS_IC133``. The PICS IC133 can contain several repeating data blocks, placed in the output structure ``typPICS_IC133``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC133``, the variable ``ParameterList.MAX_BLOCKS_IC133`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC134
The function block ``FbSunspecPICS_IC134`` enables evaluation of the PICS IC134 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC134. The readable values of the PICS IC134 are available in the output structure ``typPICS_IC134``. The PICS IC134 can contain several repeating data blocks, placed in the output structure ``typPICS_IC134``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC134``, the variable ``ParameterList.MAX_BLOCKS_IC134`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC135
The function block ``FbSunspecPICS_IC135`` enables evaluation of the PICS IC135 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC135. The readable values of the PICS IC135 are available in the output structure ``typPICS_IC135``. The PICS IC135 can contain several repeating data blocks, placed in the output structure ``typPICS_IC135``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC135``, the variable ``ParameterList.MAX_BLOCKS_IC135`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC136
The function block ``FbSunspecPICS_IC136`` enables evaluation of the PICS IC136 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC136. The readable values of the PICS IC136 are available in the output structure ``typPICS_IC136``. The PICS IC136 can contain several repeating data blocks, placed in the output structure ``typPICS_IC136``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC136``, the variable ``ParameterList.MAX_BLOCKS_IC136`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC137
The function block ``FbSunspecPICS_IC137`` enables evaluation of the PICS IC137 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC137. The readable values of the PICS IC137 are available in the output structure ``typPICS_IC137``. The PICS IC137 can contain several repeating data blocks, placed in the output structure ``typPICS_IC137``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC137``, the variable ``ParameterList.MAX_BLOCKS_IC137`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC138
The function block ``FbSunspecPICS_IC138`` enables evaluation of the PICS IC138 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC138. The readable values of the PICS IC138 are available in the output structure ``typPICS_IC138``. The PICS IC138 can contain several repeating data blocks, placed in the output structure ``typPICS_IC138``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC138``, the variable ``ParameterList.MAX_BLOCKS_IC138`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC139
The function block ``FbSunspecPICS_IC139`` enables evaluation of the PICS IC139 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC139. The readable values of the PICS IC139 are available in the output structure ``typPICS_IC139``. The PICS IC139 can contain several repeating data blocks, placed in the output structure ``typPICS_IC139``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC139``, the variable ``ParameterList.MAX_BLOCKS_IC139`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC140
The function block ``FbSunspecPICS_IC140`` enables evaluation of the PICS IC140 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC140. The readable values of the PICS IC140 are available in the output structure ``typPICS_IC140``. The PICS IC140 can contain several repeating data blocks, placed in the output structure ``typPICS_IC140``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC140``, the variable ``ParameterList.MAX_BLOCKS_IC140`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC141
The function block ``FbSunspecPICS_IC141`` enables evaluation of the PICS IC141 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC141. The readable values of the PICS IC141 are available in the output structure ``typPICS_IC141``. The PICS IC141 can contain several repeating data blocks, placed in the output structure ``typPICS_IC141``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC141``, the variable ``ParameterList.MAX_BLOCKS_IC141`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC142
The function block ``FbSunspecPICS_IC142`` enables evaluation of the PICS IC142 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC142. The readable values of the PICS IC142 are available in the output structure ``typPICS_IC142``. The PICS IC142 can contain several repeating data blocks, placed in the output structure ``typPICS_IC142``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC142``, the variable ``ParameterList.MAX_BLOCKS_IC142`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC143
The function block ``FbSunspecPICS_IC143`` enables evaluation of the PICS IC143 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC143. The readable values of the PICS IC143 are available in the output structure ``typPICS_IC143``. The PICS IC143 can contain several repeating data blocks, placed in the output structure ``typPICS_IC143``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC143``, the variable ``ParameterList.MAX_BLOCKS_IC143`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC144
The function block ``FbSunspecPICS_IC144`` enables evaluation of the PICS IC144 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC144. The readable values of the PICS IC144 are available in the output structure ``typPICS_IC144``. The PICS IC144 can contain several repeating data blocks, placed in the output structure ``typPICS_IC144``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_IC144``, the variable ``ParameterList.MAX_BLOCKS_IC144`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_IC145
The function block ``FbSunspecPICS_IC145`` enables evaluation of the PICS IC145 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS IC145. The readable values of the PICS IC145 are available in the output structure ``typPICS_IC145``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_M201
The function block ``FbSunspecPICS_M201`` enables evaluation of the PICS M201 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS M201. The readable values of the PICS M201 are available in the output structure ``typPICS_M201``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_M202
The function block ``FbSunspecPICS_M202`` enables evaluation of the PICS M202 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS M202. The readable values of the PICS M202 are available in the output structure ``typPICS_M202``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_M203
The function block ``FbSunspecPICS_M203`` enables evaluation of the PICS M203 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS M203. The readable values of the PICS M203 are available in the output structure ``typPICS_M203``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_M204
The function block ``FbSunspecPICS_M204`` enables evaluation of the PICS M204 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS M204. The readable values of the PICS M204 are available in the output structure ``typPICS_M204``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_M211
The function block ``FbSunspecPICS_M211`` enables evaluation of the PICS M211 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS M211. The readable values of the PICS M211 are available in the output structure ``typPICS_M211``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_M212
The function block ``FbSunspecPICS_M212`` enables evaluation of the PICS M212 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS M212. The readable values of the PICS M212 are available in the output structure ``typPICS_M212``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_M213
The function block ``FbSunspecPICS_M213`` enables evaluation of the PICS M213 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS M213. The readable values of the PICS M213 are available in the output structure ``typPICS_M213``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_M214
The function block ``FbSunspecPICS_M214`` enables evaluation of the PICS M214 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS M214. The readable values of the PICS M214 are available in the output structure ``typPICS_M214``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_E302
The function block ``FbSunspecPICS_E302`` enables evaluation of the PICS E302 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS E302. The readable values of the PICS E302 are available in the output structure ``typPICS_E302``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_E303
The function block ``FbSunspecPICS_E303`` enables evaluation of the PICS E303 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS E303. The readable values of the PICS E303 are available in the output structure ``typPICS_E303``. The PICS E303 can contain several repeating data blocks, placed in the output structure ``typPICS_E303``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_E303``, the variable ``ParameterList.MAX_BLOCKS_E303`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_E304
The function block ``FbSunspecPICS_E304`` enables evaluation of the PICS E304 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS E304. The readable values of the PICS E304 are available in the output structure ``typPICS_E304``. The PICS E304 can contain several repeating data blocks, placed in the output structure ``typPICS_E304``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_E304``, the variable ``ParameterList.MAX_BLOCKS_E304`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_E305
The function block ``FbSunspecPICS_E305`` enables evaluation of the PICS E305 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS E305. The readable values of the PICS E305 are available in the output structure ``typPICS_E305``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_E306
The function block ``FbSunspecPICS_E306`` enables evaluation of the PICS E306 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS E306. The readable values of the PICS E306 are available in the output structure ``typPICS_E306``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_E307
The function block ``FbSunspecPICS_E307`` enables evaluation of the PICS E307 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS E307. The readable values of the PICS E307 are available in the output structure ``typPICS_E307``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_E308
The function block ``FbSunspecPICS_E308`` enables evaluation of the PICS E308 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS E308. The readable values of the PICS E308 are available in the output structure ``typPICS_E308``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_SC401
The function block ``FbSunspecPICS_SC401`` enables evaluation of the PICS SC401 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS SC401. The readable values of the PICS SC401 are available in the output structure ``typPICS_SC401``. The PICS SC401 can contain several repeating data blocks, placed in the output structure ``typPICS_SC401``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_SC401``, the variable ``ParameterList.MAX_BLOCKS_SC401`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_SC402
The function block ``FbSunspecPICS_SC402`` enables evaluation of the PICS SC402 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS SC402. The readable values of the PICS SC402 are available in the output structure ``typPICS_SC402``. The PICS SC402 can contain several repeating data blocks, placed in the output structure ``typPICS_SC402``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_SC402``, the variable ``ParameterList.MAX_BLOCKS_SC402`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_SC403
The function block ``FbSunspecPICS_SC403`` enables evaluation of the PICS SC403 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS SC403. The readable values of the PICS SC403 are available in the output structure ``typPICS_SC403``. The PICS SC403 can contain several repeating data blocks, placed in the output structure ``typPICS_SC403``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_SC403``, the variable ``ParameterList.MAX_BLOCKS_SC403`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_SC404
The function block ``FbSunspecPICS_SC404`` enables evaluation of the PICS SC404 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS SC404. The readable values of the PICS SC404 are available in the output structure ``typPICS_SC404``. The PICS SC404 can contain several repeating data blocks, placed in the output structure ``typPICS_SC404``. The output ``wQuantityBlocks`` indicates the quantity of repeating blocks. To get all data inside ``typPICS_SC404``, the variable ``ParameterList.MAX_BLOCKS_SC404`` must be edited in the |ParameterList|, with the quantity of repeating blocks. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

### FbSunspecPICS_NC011
The function block ``FbSunspecPICS_NC011`` enables evaluation of the PICS NC011 of a Sunspec slave.

**Description:**
By activating the input ``xEnable``, the block is enabled and the communication starts automatically. The input ``bPort`` is used for the assignment to the master function block. The output ``wPICS_StartAddress`` indicates the start address of the PICS NC011. The readable values of the PICS NC011 are available in the output structure ``typPICS_NC011``. .. note:: For an example see also |doc02_HowTo|. .. note:: For usefull information about the readable values see also |doc03_UsefulInformation|. .. note:: For usefull information about the evaluation of errors see also |doc03_UsefulInformation|.

## Usage Examples

### Basic SunSpec Communication
```iec
VAR
    oMaster: FbSunspecMaster;
    oPICS_I113: FbSunspecPICS_I113;  // 3-phase inverter
    ac_power: REAL;
    ac_voltage: REAL;
END_VAR

// Configure master
oMaster.typConfigParameters.eProtocol := TCP;
oMaster.typConfigParameters.sIPAddress := '192.168.1.100';
oMaster.typConfigParameters.wPort := 502;
oMaster.typConfigParameters.bUnitID := 1;
oMaster.xEnable := TRUE;

// Configure PICS
oPICS_I113.xEnable := TRUE;
oPICS_I113.bPort := oMaster.bPort;

// Read data
IF oPICS_I113.xValid AND NOT oPICS_I113.xError THEN
    ac_power := oPICS_I113.typPICS_I113.wW;
    ac_voltage := oPICS_I113.typPICS_I113.wPPVph;
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

