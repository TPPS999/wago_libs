# WagoTypesModule_75x_487 v1.9.3.0

## Overview
WAGO PLC library providing WagoTypesModule_75x_487 functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Data Types

### typRawChannelScaling
Structure type.

### typRawChannelSettings
Structure type.

### typRawChannelConfiguration
Structure type.

### eSensorType
Enumeration type.

================== ======= =============================== Name Initial Range ================== ======= =============================== TC_Typ_L 0 -25 °C.. 900 °C TC_Typ_K 1 -100 °C.. 1370 °C TC_Typ_J 2 -100 °C.. 1200 °C TC_Typ_E 3 -100 °C.. 1000 °C TC_Typ_T 4 -100 °C.. 400 °C TC_Typ_N 5 -100 °C.. 1300 °C TC_Typ_U 6 -25 °C.. 600 °C TC_Typ_B 7 600 °C.. 1800 °C TC_Typ_R 8 0 °C.. 1700 °C TC_Typ_S 9 0 °C.. 1700 °C PlusMinus_30mV 13 +/- 30mV PlusMinus_60mV 14 +/- 60mV PlusMinus_120mV 15 +/- 120mV ================== ======= ===============================

## Usage Examples

```iec
// Basic usage example
// Refer to function block documentation for specific usage
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

