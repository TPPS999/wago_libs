# WagoSolRomutec v1.2.0.4

## Overview
WAGO PLC library providing WagoSolRomutec functionality.

**Key Features:**
- LED control and management
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### Fb2LevelSwitchConverter
Use this function block to convert the structure 'typRBT_2LevelSwitch' to BOOL-Outputs.

### FbLED_Converter
Use this function block to convert Bool-Inputs to typRBT_LED.

### FbRomutecMaster
The function block is used for Romutec BUStec module communication via the RS-485 interface (750-652) using MODBUS communication.

**Description:**
``I_Port`` must be connected with the serial interface for example: ``IoConfig_Globals.RS232_485_Interface``. ``bPortRomutec`` must be connect to the other function blocks. Default physical layer

### FbBAH4000
The function block is used for analogue output module FbBAH 4000 4xAO.

**Description:**
The function block ``FbBAH4000`` is used to actuate the analog encoder card BDH4000. The analog setpoint is converted to a voltage from 0 ... 10 V. The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. In automatic mode, the setpoint of outputs ``bSet_Output1`` to ``bSet_Output4`` is converted to a voltage from 0 ... 10 V. The set voltage is optically indicated by the LED brightness. A TRUE at the outputs ``xAutomatic_Switch1`` to ``xAutomatic_Switch4`` signals the respective automatic mode switch position on the module. The current output voltage values are displayed at the outputs ``bAnalogue_Output1`` to ``bAnalogue_Output4`` in both automatic and manual modes.

### FbBAH4001
The function block is used for analogue output module FbBAH 4001 4xAO/4xAI.

**Description:**
The function block ``FbBAH4001`` is used to actuate the analog encoder card BDH4001. The analog setpoint is converted to a voltage from 0 ... 10 V. The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. In automatic mode, the setpoint of outputs ``bSet_Output1`` to ``bSet_Output4`` is converted to a voltage from 0 ... 10 V. The set voltage is optically indicated by the LED brightness. A TRUE at the outputs ``xAutomatic_Switch1`` to ``xAutomatic_Switch4`` signals the respective automatic mode switch position on the module. The current output voltage values are displayed at the outputs ``bAnalogue_Output1`` to ``bAnalogue_Output4`` in both automatic and manual modes.

### FbBDH1400
The function block is used for digital output module FbBDH 1400 4x1DO.

**Description:**
The function block ``FbBDH1400`` is used to actuate the motor control card BDH1400, whereby the LEDs are actuated by the function block. The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. In automatic mode, the relays can be actuated via inputs ``xRelay1`` to ``xRelay4``. When automatic mode is active, the LEDs for indicating operation are actuated together with the respective relays. In manual mode, the LEDs for indicating operation are switched off. The inputs ``typLED_Switch1_Error`` to ``typLED_Switch4_Error`` control the respective error messages. The LED color is specified via the structure ``typLED``. Here, it is possible to actuate the variables ``LED_RedBlink`` and ``LED_Green`` at the same time (LED yellow/green). A TRUE at the outputs ``xAutomatic_Switch1`` to ``xAutomatic_Switch4`` signals the respective automatic mode switch position on the module.

### FbBDH1401
The function block is used for digital input module FbBDH 1401 4x1DO/8DI.

**Description:**
The function block ``FbBDH1401`` is used to actuate the motor control card BDH1401. The LEDs are actuated with + 24 VDC, which is switched via the I/O modules on the card. The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. In automatic mode, the relays can be actuated via inputs ``xRelay1`` to ``xRelay4``. A TRUE at the outputs ``xAutomatic_Switch1`` to ``xAutomatic_Switch4`` signals the automatic mode switch position. The outputs ``xError_Switch1`` to ``xError_Switch4`` indicate the status of the respective error message; the outputs ``xActivate_Switch1`` to ``xActivate_Switch4`` indicate the status of the respective operating light.

### FbBDH1402
The function block is used for digital input module FbBDH 1402 4x1DO/8DO.

**Description:**
The function block ``FbBDH1402`` is used to actuate the valve card BDH1402. The LEDs are actuated with + 24 VDC, which is switched via the bus power supply on the card. The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. In automatic mode, the relays can be actuated via inputs ``xRelay1`` to ``xRelay4``. A TRUE at the outputs ``xAutomatic_Switch1`` to ``xAutomatic_Switch4`` signals the automatic mode switch position. The outputs ``xClose_Switch1`` to ``xClose_Switch4`` indicate the status of the respective closed valve; the outputs ``xOpen_Switch1`` to ``xOpen_Switch4`` indicate the status of the respective opened valve.

### FbBDH1403
The function block is used for digital input module FbBDH 1403 4x1DO/4DI+4DI(invert).

**Description:**
The function block ``FbBDH1403`` is used to actuate the motor control card BDH1403. The LEDs are actuated with + 24 VDC, which is switched via the bus power supply on the card. The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. In automatic mode, the relays can be actuated via inputs ``xRelay1`` to ``xRelay4``. A TRUE at the outputs ``xAutomatic_Switch1`` to ``xAutomatic_Switch4`` signals the automatic mode switch position. The outputs ``xError_Switch1`` to ``xError_Switch4`` indicate the status of the respective error message; the outputs ``xActivate_Switch1`` to ``xActivate_Switch4`` indicate the status of the respective operating light.

### FbBDH2200
The function block is used for digital output module FbBDH 2200 2x2DO.

**Description:**
The function block ``FbBDH2200`` is used to actuate the motor control card BDH2200, whereby the LEDs are actuated by the function block. The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. In automatic mode, the relays can be actuated for the respective switching level via inputs ``xSwitch1_Level1`` to ``xSwitch2_Level2``. The inputs ``typLED_Switch1_Error`` and ``typLED_Switch2_Error`` control the respective error messages. The LED color is specified via the structure ``typLED``. A TRUE at the outputs ``xAutomatic_Switch1`` and ``xAutomatic_Switch2`` signals the respective automatic modes.

### FbBDH2201
The function block is used for digital input module FbBDH 2201 2x2DO/6DI.

**Description:**
The function block ``FbBDH2201`` is used to actuate the motor control card BDH2201. The LEDs are actuated with + 24 VDC, which is switched via the bus power supply on the card. The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. In automatic mode, the relays can be actuated for the respective switching level via inputs ``xSwitch1_Level1`` to ``xSwitch2_Level2``. A TRUE at the outputs ``xAutomatic_Switch1`` and ``xAutomatic_Switch2`` signals the automatic mode switch position. The outputs ``typLED_Switch1_Error`` and ``typLED_Switch2_Error`` indicate the status of the respective error messages. The outputs ``xLED_Switch1_Level1`` and ``xLED_Switch1_Level2``, along with ``xLED_Switch2_Level1`` and ``xLED_Switch2_Level2``, indicate the status of the LEDs for the operation.

### FbBDH2203
The function block is used for digital input module FbBDH 2203 2x2DO/4DI+2DI(invert).

**Description:**
The function block ``FbBDH2203`` is used to actuate the motor control card BDH2203. The LEDs are actuated with + 24 VDC, which is switched via the bus power supply on the card. The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. In automatic mode, the relays can be actuated for the respective switching level via inputs ``xSwitch1_Level1`` to ``xSwitch2_Level2``. A TRUE at the outputs ``xAutomatic_Switch1`` and ``xAutomatic_Switch2`` signals the automatic mode switch position. The outputs ``typLED_Switch1_Error`` and ``typLED_Switch2_Error`` indicate the status of the respective error messages. The outputs ``xLED_Switch1_Level1`` and ``xLED_Switch1_Level2``, along with ``xLED_Switch2_Level1`` and ``xLED_Switch2_Level2``, indicate the status of the LEDs for the operation.

### FbBDH4800
The function block is used for digital output module FbBDH 4800 16DO/4DI.

**Description:**
The function block ``FbBDH4800`` is used to actuate the illuminated push-button card BDH4800. The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. The LEDs on the module are actuated via inputs ``xLED1_1`` to ``xLED4_3``. Actuating LED1 and LED2 of a group does not cause a collective fault. However, if LED3 is actuated, there is also a collective fault on the central module. The coupling relays can be actuated via inputs ``xRelay1`` to ``xRelay4``. A TRUE at the outputs ``xPushbutton1`` to ``xPushbutton4`` signals the actuation of the respective push-button on the module. .. note:: The push-button polling is dependent on parameter ``tCycleTime``. Now, if the push-button is pressed only during the time between two polling processes, the push-button press might not be detected.

### FbBDH4800_100
The function block is used for digital output module FbBDH 4800-100 12DO/4DI.

**Description:**
The function block ``FbBDH4800_100`` is used to actuate the illuminated push-button card BDH4800_100. The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. The LEDs on the module are actuated via inputs ``xLED1_1`` to ``xLED4_3``. Actuating LED1 and LED2 of a group does not cause a collective fault. However, if LED3 is actuated, there is also a collective fault on the central module. A TRUE at the outputs ``xPushbutton1`` to ``xPushbutton4`` signals the actuation of the respective push-button on the module. .. note:: The push-button polling is dependent on parameter ``tCycleTime``. Now, if the push-button is pressed only during the time between two polling processes, the push-button press might not be detected.

### FbBLM1000
The function block is used for signaling module BLM 1000 10DO.

**Description:**
Function block ``FbBLM1000`` is used to actuate the 10 LEDs on the module BLM1000. Each LED has four different status displays (LED off, LED green, LED yellow/green, LED red). The inputs ``typMessage1`` to ``typMessage10`` actuate the respective LEDs. The LED color is specified via the structure ``typLED``. Here, it is possible to actuate the variables ``LED_RedBlink`` and ``LED_Green`` at the same time (LED yellow/green).

### FbBLM1001
The function block is used for signaling module BLM 1001 10DI.

**Description:**
Function block ``FbBLM1001`` is used to evaluate the status of 10 LEDs. Each LED has three different status displays (LED off, LED green, LED red). The module addressed though ``bModuleaddress`` is cyclically polled if the input ``xEnable`` is TRUE. The ``tCycleTime`` input parameter determines the cycle time. The outputs ``typMessage1`` to ``typMessage10`` indicate the LED status. Depending on the message, either variable ``LED_RedBlink`` or ``LED_Green`` is set in the structure.

### FbBZK1000
The function block is used for central module BZK 1000 to communicate via modbus.

**Description:**
The connection between the Romutec manual mode level BZK1000 and the WAGO-I/O-SYSTEM is realized with the function block ``FbBZK1000``. If the input ``xEnable`` is TRUE, the module is cyclically polled. The ``tCycleTime`` input parameter determines the cycle time. The input ``xReset`` unlocks the relay for the malfunction. A collective fault is handled by a TRUE at the input ``xCollective_Malfunction``. When a collective fault is triggered, the relays for the collective fault and the horn are activated. The relay for the horn is switched off via the input ``xResetHorn``. The lamp test is performed via the input ``xTest_LED``. The output ``xCollective_Error`` is activated when there is a collective fault. The outputs ``xUnlock_Malfunction``, ``xQuit_Horn`` and ``xLED_Test_Activate`` indicate the actuation of the respective push-button on the module BZK1000. .. note:: The push-button polling is dependent on parameter ``tCycleTime``. Now, if the push-button is pressed only during the time between two polling processes, the push-button press might not be detected.

### FbRomutecMaster_RBT
The function block is used to communicate via Modbus_RTU with robutec modules.

**Description:**
The function block can be used to connect the Robutec door station to the WAGO-I/O-SYSTEM. The MODBUS RS485 RTU communication is implemented via the serial module 750-652, not via 750-650/003-000 or 750-653/003-000. Default baud rate

### FbRBT10
Use this function block to communicate with the module RBT 10

**Description:**
The connection between the Romutec manual mode level RBT10 and the WAGO-I/O-SYSTEM is realized with the function block ``FbRBT10``. Each LED has four different status displays (LED off, LED green, LED orange, LED red). If the input ``xEnable`` is TRUE, the module is cyclically polled. The ``tCycleTime`` input parameter determines the cycle time. The position must be entered at the input ``bModulplace`` and the address (see back of RBT module) must be entered at the input ``bModuladdress``. The LEDs on the module are actuated via inputs ``typRBT_LED1`` to ``typRBT_LED12``. The LED color is specified via the structure ``typRBT_LED``. Here, it is possible to actuate the variables ``LED_Red`` and ``LED_Green`` at the same time (LED orange). Different commands can be sent to the RBT module via ``wRBT_Modul``; see input parameters. The ``tBusTimeout`` for the RBT module is set as a decimal in seconds; if no valid telegram is received from the RBT module within this time, the ``Status`` LED starts blinking red.

### FbRBT20
Use this function block to communicate with the module RBT 20

**Description:**
The connection between the Romutec manual mode level RBT20 and the WAGO-I/O-SYSTEM is realized with the function block ``FbRBT20``. Each LED has four different status displays (LED off, LED green, LED orange, LED red). If the input ``xEnable`` is TRUE, the module is cyclically polled. The ``tCycleTime`` input parameter determines the cycle time. The position must be entered at the input ``bModulplace`` and the address (see back of RBT module) must be entered at the input ``bModuladdress``. The LEDs on the module are actuated via inputs ``typRBT_LED1`` to ``typRBT_LED8``. The LED color is specified via the structure ``typRBT_LED``. Here, it is possible to actuate the variables ``LED_Red`` and ``LED_Green`` at the same time (LED orange). Different commands can be sent to the RBT module via ``wRBT_Modul``; see input parameters. The ``tBusTimeout`` for the RBT module is set as a decimal in seconds; if no valid telegram is received from the RBT module within this time, the ``Status`` LED starts blinking red. A TRUE in the output structure variables ``typRBT_2LevelSwitch1`` to ``typRBT_2LevelSwitch4`` signals the switch position of the respective rotary switch.

### FbRBT30
Use this function block to communicate with the module RBT 30

**Description:**
The connection between the Romutec manual mode level RBT30 and the WAGO-I/O-SYSTEM is realized with the function block ``FbRBT30``. Each LED has four different status displays (LED off, LED green, LED orange, LED red). If the input ``xEnable`` is TRUE, the module is cyclically polled. The ``tCycleTime`` input parameter determines the cycle time. The position must be entered at the input ``bModulplace`` and the address (see back of RBT module) must be entered at the input ``bModuladdress``. The LEDs on the module are actuated via inputs ``typRBT_LED1`` to ``typRBT_LED12``. The LED color is specified via the structure ``typRBT_LED``. Here, it is possible to actuate the variables ``LED_Red`` and ``LED_Green`` at the same time (LED orange). Different commands can be sent to the RBT module via ``wRBT_Modul``; see input parameters. The ``tBusTimeout`` for the RBT module is set as a decimal in seconds; if no valid telegram is received from the RBT module within this time, the ``Status`` LED starts blinking red. A TRUE at the output variables ``xButton1`` to ``xButton4`` signals the actuation of the respective push-button.

### FbRBT40
Use this function block to communicate with the module RBT 40

**Description:**
The connection between the Romutec manual mode level RBT40 and the WAGO-I/O-SYSTEM is realized with the function block ``FbRBT40``. If the input ``xEnable`` is TRUE, the module is cyclically polled. The ``tCycleTime`` input parameter determines the cycle time. The position must be entered at the input ``bModulplace`` and the address (see back of RBT module) must be entered at the input ``bModuladdress``. Which value the output ``bActualValueChannel`` should have when no ``xManualOverrideChannel`` manual override is active is specified via the input ``rAutomaticValueChannel``. During a ``xManualOverrideChannel`` manual override, the output ``rActualValueChannel`` is incrementally changed by the value at the input ``bIncrementalFactor``. The bar display brightness can be set between 0 and 100% with the input ``wBrightnessLED``. Different commands can be sent to the RBT module via ``wRBT_Modul``; see input parameters. The ``tBusTimeout`` for the RBT module is set as a decimal in seconds; if no valid telegram is received from the RBT module within this time, the ``Status`` LED starts blinking red.

### FbRBT50
Use this function block to communicate with the module RBT 50.

**Description:**
The connection between the Romutec manual mode level RBT50 and the WAGO-I/O-SYSTEM is realized with the function block ``FbRBT50``. Each LED has four different status displays (LED off, LED green, LED orange, LED red). If the input ``xEnable`` is TRUE, the module is cyclically polled. The ``tCycleTime`` input parameter determines the cycle time. The position must be entered at the input ``bModulplace`` and the address (see back of RBT module) must be entered at the input ``bModuladdress``. Which value the output ``rActualValueChannel`` should have when no ``xManualOverrideChannel`` manual override is active is specified via the input ``rAutomaticValueChannel``. During a ``xManualOverrideChannel`` manual override, the output ``rActualValueChannel`` is incrementally changed by the value at the input ``bIncrementalFactor``. The LEDs on the module are actuated via inputs ``typRBT_LED1`` to ``typRBT_LED6``. The LED color is specified via the structure ``typRBT_LED``. Here, it is possible to actuate the variables ``LED_Red`` and ``LED_Green`` at the same time (LED orange). The bar display brightness can be set between 0 and 100% with the input ``wBrightnessLED``. Different commands can be sent to the RBT module via ``wRBT_Modul``; see input parameters. The ``tBusTimeout`` for the RBT module is set as a decimal in seconds; if no valid telegram is received from the RBT module within this time, the ``Status`` LED starts blinking red. A TRUE in the output structure variables ``typRBT_2LevelSwitch1`` and ``typRBT_2LevelSwitch2`` signals the switch position of the respective rotary switch.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFb2LevelSwitchConverter: Fb2LevelSwitchConverter;
END_VAR

// Basic function block usage
fbFb2LevelSwitchConverter(
    // Configure inputs as needed
);

// Check status
IF fbFb2LevelSwitchConverter.xValid THEN
    // Operation successful
END_IF

IF fbFb2LevelSwitchConverter.xError THEN
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

