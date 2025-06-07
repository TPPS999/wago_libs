# WagoSolSplusS v1.0.0.7

## Overview
WAGO PLC library providing WagoSolSplusS functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbTHERMASGARD_RPTMx_Modbus_T3
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD RPTM1-Modbus-T3 - THERMASGARD RPTM2-Modbus-T3 It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/ALR4M.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_MWTM_Modbus_T3
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD MWTM-Modbus-T3 It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/CPOVM.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_ALTMx_Modbus_T3
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD ALTM1-Modbus-T3 - THERMASGARD ALTM2-Modbus-T3 It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/BG4MM.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_HFTM_Modbus_T3
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD HFTM-Modbus-T3 It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/CAI4M.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_TM65_Modbus_T3
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD TM65-Modbus-T3 It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/D4VMM.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_ATM2_Modbus_T3
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD ATM2-Modbus-T3 It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/DK2DM.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_TW_Modbus_T3
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD TW-Modbus-T3 It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/8HTDM.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_VFTF_Modbus_T3
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD VFTF-Modbus-T3 It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/8X04M.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_RPFTF_Modbus_T3
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD RPFTF-Modbus-T3 It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/9C6VM.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_KFTF_Modbus_T3
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD KFTF-Modbus-T3 It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/9RDMM.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_AFTF_Modbus_T3
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD AFTF-Modbus-T3 It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/A6KDM.htm>` .. note:: You should always call this FB cyclic.

### FbPREMASGARD_232x_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - PREMASGARD 2328-M - PREMASGARD 2327-M It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/7NFVM.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_AFTF_SD_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD AFTF-SD-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/KQ94M.htm>` .. note:: You should always call this FB cyclic.

### FbPREMASGARD_121x_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - PREMASGARD 1211-M - PREMASGARD 1215-M It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/6DVMM.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_FSFTM_CO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD FSFTM-CO2-Modbus - AERASGARD FSFTM-CO2-Modbus-P :ref:`Manual <http://spluss.de/r/PR5Q5.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_RCO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD RCO2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/IMBDM.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_RLQ_RCO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD RLQ-RCO2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/I74MM.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_RFTM_CO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD RFTM-CO2-Modbus - AERASGARD RFTM-CO2-Modbus-P It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/HRXVM.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_RFTM_LQ_CO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD RFTM-LQ-CO2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/HCR4M.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_ACO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD ACO2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/GXKDM.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_ALQ_CO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD ALQ-CO2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/GIDMM.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_AFTM_LQ_CO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD AFTM-LQ-CO2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/FO04M.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_AFTM_CO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD AFTM-CO2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/G36VM.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_KCO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD KCO2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/F8TDM.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_KLQ_CO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD KLQ-CO2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/ETMMM.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_KFTM_CO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD KFTM-CO2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/EEFVM.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_KFTF_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD KFTF-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/KB2DM.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_ATM2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD ATM2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/O3R4M.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_RPFTF_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD RPFTF-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/JVVMM.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_VFTF_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD VFTF-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/JGOVM.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_TW_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD TW-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/J1I4M.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_RFTF_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD RFTF-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <http://spluss.de/r/CJA85.htm>` .. note:: You should always call this FB cyclic.

### FbHYGRASGARD_FSFTM_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD FSFTM-Modbus - HYGRASGARD FSFTM-Modbus-P :ref:`Manual <http://spluss.de/r/QLJ85.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_TM65_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD TM65-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/NOKDM.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_MWTM_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD MWTM-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/N9DMM.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_HFTM_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD HFTM-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/MU6VM.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_ALTMx_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD ALTM1-Modbus - THERMASGARD ALTM2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/MF04M.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_RPTMx_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD RPTM1-Modbus - THERMASGARD RPTM2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/L5FVM.htm>` .. note:: You should always call this FB cyclic.

### FbTHERMASGARD_RTM1_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD RTM1-Modbus - THERMASGARD RTM1-Modbus-P It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/FWS85.htm>` .. note:: You should always call this FB cyclic.

### FbPREMASGARD_814x_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - PREMASGARD 814x-M It also provide an interface to customize the display behaivior. :ref:`Manual <http://spluss.de/r/SAA85.htm>` .. note:: You should always call this FB cyclic.

### FbAERASGARD_KFTM_LQ_CO2_Modbus
This function block periodically read out process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD KFTM-LQ-CO2-Modbus It also provide an interface to customize the display behaivior. :ref:`Manual <https://spluss.de/r/DZ94M.htm>` .. note:: You should always call this FB cyclic.

### FbSplusS_Master
This communication function block is used for S+S Regeltechnik GmbH measurement converter. Communication utilize RS485-half-duplex using MODBUS-RTU protocol. Without further action the S+S default settings of "19200/E/1" are used: .. note:: You should always call this FB cyclic. Supported interface: - PFC-Onboard-serial-interface-X3(COM1): In conjunction with 750-960 adapter - 750-652: Configurable Serial Interface Terminal RS232/RS485 - 750-653/xxx-xxx: Serial Interface Terminal RS485

## Data Types

### eDisplayMode32400
Enumeration type.

### typ35500Data
Structure type.

The process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD FSFTM-CO2-Modbus - AERASGARD FSFTM-CO2-Modbus-P

### eLedFlashingMode
Enumeration type.

### eLedBarGraphMode
Enumeration type.

### eSensibilityVOC34x00
Enumeration type.

### typ34700Data
Structure type.

The process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD RCO2-Modbus - AERASGARD RFTM-CO2-Modbus - AERASGARD RFTM-CO2-Modbus-P - AERASGARD RFTM-LQ-CO2-Modbus - AERASGARD RLQ-RCO2-Modbus

### typ35400Data
Structure type.

The process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD FSFTM-Modbus - HYGRASGARD FSFTM-Modbus-P

### eDisplayMode31800
Enumeration type.

### typ35200Data
Structure type.

The process data from S+S Regeltechnik GmbH measurement converter of type: - PREMASGARD 814x-M

### typ34800Data
Structure type.

The process data from S+S Regeltechnik GmbH measurement converter of type: - AERASGARD ACO2-Modbus - AERASGARD AFTM-CO2-Modbus - AERASGARD AFTM-LQ-CO2-Modbus - AERASGARD ALQ-CO2-Modbus - AERASGARD-KCO2-Modbus - AERASGARD-KFTM-CO2-Modbus - AERASGARD-KFTM-LQ-CO2-Modbus - AERASGARD KLQ-CO2-Modbus

### typLedColourRegister
Structure type.

### typ32800Data
Structure type.

The process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD RFTF-Modbus

### typ32400Data
Structure type.

The process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD RTM1-Modbus - THERMASGARD RTM1-Modbus-P

### typ31800Data
Structure type.

The process data from S+S Regeltechnik GmbH measurement converter of type: - HYGRASGARD AFTF-SD-Modbus - HYGRASGARD AFTF-Modbus-T3 - HYGRASGARD KFTF-Modbus - HYGRASGARD KFTF-Modbus-T3 - HYGRASGARD RPFTF-Modbus - HYGRASGARD RPFTF-Modbus-T3 - HYGRASGARD TW-Modbus - HYGRASGARD TW-Modbus-T3 - HYGRASGARD VFTF-Modbus - HYGRASGARD VFTF-Modbus-T3

### eDisplayMode35200
Enumeration type.

### eDisplayMode34800
Enumeration type.

### eDisplayMode32800
Enumeration type.

### typ31200Data
Structure type.

The process data from S+S Regeltechnik GmbH measurement converter of type: - THERMASGARD ALTM1-Modbus - THERMASGARD ALTM1-Modbus-T3 - THERMASGARD ALTM2-Modbus - THERMASGARD ALTM2-Modbus-T3 - THERMASGARD ATM2-Modbus - THERMASGARD ATM2-Modbus-T3 - THERMASGARD HFTM-Modbus - THERMASGARD HFTM-Modbus-T3 - THERMASGARD MWTM-Modbus - THERMASGARD MWTM-Modbus-T3 - THERMASGARD RPTM1-Modbus - THERMASGARD RPTM1-Modbus-T3 - THERMASGARD RPTM2-Modbus - THERMASGARD RPTM2-Modbus-T3 - THERMASGARD TM65-Modbus - THERMASGARD TM65-Modbus-T3

### eDisplayMode
Enumeration type.

### typ31000Data
Structure type.

The process data from S+S Regeltechnik GmbH measurement converter of type: - PREMASGARD 1211-M - PREMASGARD 1215-M - PREMASGARD 232x-M

### eDisplayMode34700
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbTHERMASGARD_RPTMx_Modbus_T3: FbTHERMASGARD_RPTMx_Modbus_T3;
END_VAR

// Basic function block usage
fbFbTHERMASGARD_RPTMx_Modbus_T3(
    // Configure inputs as needed
);

// Check status
IF fbFbTHERMASGARD_RPTMx_Modbus_T3.xValid THEN
    // Operation successful
END_IF

IF fbFbTHERMASGARD_RPTMx_Modbus_T3.xError THEN
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

