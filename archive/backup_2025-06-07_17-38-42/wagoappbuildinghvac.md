# WagoAppBuildingHVAC v1.0.5.12

## Overview
WAGO PLC library providing WagoAppBuildingHVAC functionality.

**Key Features:**
- Time and date operations
- Control functions
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbPIDSingleRoomController
Function block allows individual room reference temperature control while taking local influences into account.

**Description:**
The room temperature ``rActualTemperature`` is yielded from the measured room temperature ``rRoomTemperature`` and the variable measured value compensation. The PID controller regulates the room temperature ``rActualTemperature`` to the defined reference value. Depending on the operating mode, the set value is given either at the ``rY_Heating`` or ``rY_Cooling`` output. The output value ``wY_Heating`` has the same meaning as the ``rY_Heating`` output, except that the output has standardized values between 0 – 32767. The output value ``wY_Cooling`` has the same meaning as the ``rY_Cooling`` output, except that the output has standardized values between 0 – 32767. The controller detects four operating modes to each of which is assigned its own set value. The ``rReferenceComfort`` set value is used as a basic set value. All other set values refer to the basic set value and provoke each a set value increase or set value decrease by a parameterized value. The reference value in the Comfort mode can be infinitely shifted via the ``rSetpointCorrection`` input. The active operating mode (Comfort, Stand-by, Night, Antifreeze protection) is determined via the ``xComfortStandby``, ``xNightMode`` and ``xWindowContact`` inputs. The currently selected operating mode is viasualized via ``xComfort``, ``xStandby``, ``xNight`` and ``xFrost_Heat``. If the function module is used for cooling purposes, another ``xDewpoint`` input is required. If a dew point alarm is signalled on this input, the cooling / heating system switches off immediately. The function block has ten monitor outputs for displaying the specified temperatures: ``rSetpointHeating``, ``rSetpointCooling``, ``rComfortHeating``, ``rComfortCooling``, ``rStandbyHeating``, ``rStandbyCooling``, ``rNightHeating``, ``rNightCooling``, ``rSetpointFrost`` and ``rSetpointHeat``. The current set values of the individual operating modes are put out via these outputs. The outputs ``xHeating`` and ``xCooling`` show which mode (heating or cooling) is active. If the set value for heating and cooling is 0%, then the two outputs ``xHeating`` and ``xCooling`` have the signal ``FALSE``. Switching between heating and cooling takes place automatically (see diagram below). The controller is either in the heating mode or in the cooling mode. The mode that is currently not active is switched to 0%. .. figure:: ../../images/PIDSingleRoomController_Characeristic.png :align: center :alt: PID single room controller - Characeristic .. note:: The D part is set to zero with most of the room heating controllers because a PI controller has sufficient precision and is easier to set. .. figure:: ../../images/PIDSingleRoomController_Setpoints.png :align: center :alt: Temperature setpoints for different operating status +-----------------------+------------------------------------------------------+---------------------------------------------------------------+ |

### FbCoolingCharacteristics
The FbCoolingCharacteristics cooling characteristic function block calculates the reference value for the supply/return temperature as a function of the outside temperature. The cooling characteristic is defined by a four point function.

**Description:**
Calculation of the temperature is enabled via the ``xEnable`` input. The specified supply temperature ``rReferenceSupplyTemperature`` is calculated using the Cooling characteristic as a function of the outside temperature ``rOutsideTemperature``.

### FbCalculatedTemperatureCooling
Function block calculates the reference value for the supply temperature as a function of the outside temperature. An additional ramp function is integrated to prevent overly rapid heating of the piping and the noises associated with this.

**Description:**
Calculation of the supply temperature is enabled via the ``xEnable`` input. When first enabled, the current supply/return temperature ``rSupplyTemperature`` is set as the starting value for the ramp function. The specified supply temperature ``rReferenceSupplyTemperature`` is calculated using the cooling characteristic as a function of the outside temperature ``rOutsideTemperature``. The output for the reference supply temperature keeps pace with this as long as the calculated reference temperature, and the change rate, is less than the maximum change rate that has been defined. If the calculated reference supply temperature changes more rapidly than the defined change rate, the reference output will lag behind the calculated reference supply temperature. During this time, the ramp output is set TRUE. When the ``xCoolingMode`` input is activated the value for the ``rReferenceValueRoom`` input is used as the reference room temperature.

### FbStartStopCoolingCircuit
Function block is used for switching the heating circuit on/off.

**Description:**
Two different values are taken into account for detecting a Cooling period. If the averaged outside temperature and the damped outside temperature rising above the defined limit, the Cooling period is enabled. The Cooling period is terminated if one of these two values fall below the defined limit again. The Cooling circuit is enabled when one of the following conditions is met: - ``xManual`` - ``xAuto``, ``xCoolingPeriod`` and ``xSwitchOn``

### FbHxControlVisu
The FbHxControlVisu function block is the interface between the visualization tplHxControlVisu and the referenced functional block ``FbHcControl``.

**Description:**
The ``FbHxControl`` must be referenced via the instance pointer address as shown in the code block below. All Hx-Field datas are transferred via the In-/Out-Variable ``typConfigHxField``. The visualization template ``tplHxControlVisu`` must be inserted as frame and referenced to this instance. .. code-block:: codesys VAR myHxControl : FbHxControl; // instance of FbHxControl myHxField : typConfigHxField; // Hx-Field parameters myHxControlVisu : FbHxControlVisu(ADR(myHxControl)); // instance of FbHxControlVisu with reference to myHxControl END_VAR //--- Call myHxControl ---------------------- // myHxControl( // ... // typConfigParameters:

**Methods:**

#### Fb_Init
### Fb_Init
### FbTCAController
The FbTCAController (Thermal Component Activation) function block controls a thermal activated component, e.g. a underfloor heating, surface cooling or a concrete core activation.

**Description:**
The functional block must be enabled by using the input ``xEnable``. The FB distinguishes between 3 kind of working modes by unsing the input variable ``bEnergyMode``: - 0

**Methods:**

#### refreshGraph
#### minSupplyTemperature
#### getHx_x
#### getHx_T
### FbVolumeFlowRegulator
The function block FbVolumeFlowRegulator is used to actuate motorized volume flow controllers with optional position feedback and optional end position switch messages.

**Description:**
If the block is activated at input ``xEnable``, the setpoint [0 … 100 %] is specified via the input variable ``rAutomaticValue``. As an alternative, the setpoint can be directly specified as the volume flow [m³/h] within the parameterized limits, via the variable ``rAutomaticVolumeFlow``. This requires setting BIT0 in the variable ``wConfig`` (in the configuration structure). The function block can be set into manual mode independently of input ``xEnable``. This requires setting the input variable ``xManualOperation`` to the value TRUE. The setpoint is then specified via the variable ``rManualValue``, within the value range 0 … 100 %. If the volume flow controller to be controlled has end positions OPEN and CLOSED; these messages are connected with the inputs ``xFeedbackOpen`` or ``xFeedbackClosed``. The physical feedback must also be activated, by setting BIT2 in the variable ``wConfig`` (in the configuration structure). If there are no end positions, the function block emulates them internally as follows: - OPEN

### FbRedundancyUnits
Function block is used to ensure uniform utilization of all units in the case of redundantly designed units and to enable replacement units in case of breakdown.

**Description:**
The FbRedundancyUnits function block is used to ensure uniform utilization of all units in the case of redundantly designed units and to enable replacement units in case of breakdown. To avoid excessive wear, e.g., of an individual pump, the operating hours of all available units are compared to then switch on the specific unit or units with the lowest number of hours of operation. If an enabled unit fails (e.g., due to a fault), the next possible unit is automatically activated. The operating hours are also taken into account. The module can ben enabled or disabled at the ``xEnable`` input. Whether the monitored units may be switched during operation is can be enabled or disabled at the ``xEnableShifitingDuringOperation`` input. If the input is set to TRUE, the unit is shifted automatically once the difference in operating ours is greater than or equal to the time specified at the ``rDiffOperatingHours`` input. If the input is set to FALSE, the unit is shifted once the unit currently running is no longer available, the time of the unit to be switched is changed or the unit is manually switched at the ``xShiftNow`` input. When manually switching the unit, please note that the maximum time difference at the ``rDiffOperatingHours`` input is not taken into consideration. The number of units to be switched on by the module is specified by the ``wRequestedUnits`` parameter and can be dynamically adjusted to the operating status, e.g., for an output increase/decrease. The current switched status is output in the binary ``aUnitsOut`` output array where the units with the same index [0..wMaxRedundancyUnits] at the input and output are identical. The ``aUnits`` input array must be configured externally and contains the following parameters of the individual units: - ``xUnitAvailable`` specifies whether the unit is available and error free. - ``dwUnitOperatingMinutes`` specifies the current number of operating hours in minutes. - ``wUnitId`` is an internal parameter and may not be changed/defined. If not enough units are available to switch on, error code ``1`` is output at the ``wError`` output.

### FbPickerTime
function block managed the Visu time input .. note:: The Function block must to be connected to the TimeSelection-Dialog.

### FbHxControl
Function block governs the required control sequences of the secondary controller in order to ensure control that makes sense in terms of energy without having a negative effect on human comfort.

**Description:**
The comfort zone is illustrated below: .. image:: ../../Images/HxControl_ComfortZone.png :align: center :alt: Comfort Zone The so-called comfort zone specifies a range in the h–x diagram in which humans find the climate comfortable. In this zone, humans do not find the air too dry or too humid for the respective temperatures, for example. If the state of the air moves out of this range, humans can find the air too warm and too dry, for example. For the comfort zone, there is no specific point in the h–x diagram provided as a setpoint for the system to move towards (for example, 25 °C and 50 % relative humidity); rather there is a specified zone. In particular, the controller moves towards the points and boundaries of the specified zone that make the most sense in terms of energy. Depending on the starting point, the physical properties of the air may make it necessary to execute a wide variety of control sequences in order to reach the targeted points and boundaries of the zone. This allows the h–x diagram around the comfort zone to be divided into six sectors with different activation points (see Figure 1: Comfort Zone). This type of control is very effective from the point of view of energy, since only as much energy is used as is necessary to reach the zone and not to remain in it. #. Cooling and humidification #. Cooling #. Dehumidification and subsequent heating if necessary #. Humidification #. Heating and humidification #. Heating The configuration parameters from |typConfigHxField| are illustrated below. - “rA” Lower boundary of the temperature - “iB” Left boundary of the relative humidity - “rC” Upper boundary of the temperature - “rD” Right boundary of the absolute relative humidity - “iE” Right boundary of the relative humidity .. image:: ../../Images/HxControl_typConfigHxField.png :align: center :alt: Comfort Zone Parameter typConfigHxField The ``tTimeHysteresis`` input serves to prevent flitting back and forth between the ranges. If the state of the air moves from one range into the other, the controller will use the latter range for control for the amount of time set in the ``tTimeHysteresis`` input. The ``xAdiabat`` input specifies what kind of humidification system is used. The ``rMinPowerHumidify`` input is directly related to the humidification. This is illustrated in Figure 3: ``rMinPowerHumidify``. The behavior of the air during humidification would be different depending on the humidification system. In isothermal humidification, besides being added, water is also heated so the air is not cooled by the humidification. In this case, the comfort zone would be approached parallel to the comfort zone. In adiabatic humidification in contrast, no energy is expended to heat the water, so the air is cooled simultaneously. To avoid wasting too much energy or drifting out of the comfort zone, a delta can be set with the ``rMinPowerHumidify`` input starting at which the humidification activates. If the state of the air is within this delta, it is not humidified. .. image:: ../../Images/HxControl_rMinPowerHumidify.png :align: center :alt: Comfort Zone - rMinPowerHumidify

### FbLowPassFilterTemp
Function block scales the input value and smoothens noisy input signals. It can also be used to define the upper and lower alarm limits.

**Description:**
The ``iInput`` input signal is divided by ten (°C) and smoothed via a PT1 circuit. The scaled and smoothed value is output at the ``rOutput`` output. If the input signal violates the defined limits for a defined time, an alarm message is output at the ``xAlarm`` output. In this case, the ``rOutput`` output assumes the defined default setting. The alarm can be acknowledged after elimination of the error via a positive edge at the ``xQuit`` input, or by automatic acknowledgement. .. note:: - The parameter ``typConfigParameters.tCycleTime`` needs to be smaller than ``typConfigParameters.tT1``.

### FbLowPassFilterBus
Function block scales the input value and smoothens noisy input signals. It can also be used to define the upper and lower alarm limits.

**Description:**
The ``rInput`` input signal is smoothed via a PT1 circuit and output at the ``rOutput`` output. The default value is given at the ``rOutput`` output as long as the sensor receives no value after a restart. As soon as a new measured value is detected at the ``rInput`` input via a positive edge at the ``xUpdate`` input, the ``xReady`` output is set to TRUE. If the input signal violates the defined limits for a defined time, an alarm message is output at the ``xAlarm`` output. Besides the limits, the time between two measured values is also monitored. If the ``xUpdate`` input does not receive a new measured value within the configured time, an alarm is issued at the ``xAlarm`` output. In this case, the ``rOutput`` output assumes the defined default setting. The alarm can be acknowledged after elimination of the error via a positive edge at the ``xQuit`` input, or by automatic acknowledgement. .. note:: - The parameter ``typConfigParameters.tCycleTime`` needs to be smaller than ``typConfigParameters.tT1``.

### FbLowPassFilterAI
Function block scales the input value and smoothens noisy input signals. It can also be used to define the upper and lower alarm limits.

**Description:**
The ``wInput`` input signal is scaled using a 4-point characteristic curve and smoothed via a PT1 circuit. The scaled and smoothed value is output at the ``rOutput`` output. If the input signal violates the defined limits for a defined time, an alarm message is output at the ``xAlarm`` output. In this case, the ``rOutput`` output assumes the defined default setting. The alarm can be acknowledged after elimination of the error via a positive edge at the ``xQuit`` input, or by automatic acknowledgement. .. note:: - The parameter ``typConfigParameters.tCycleTime`` needs to be smaller than ``typConfigParameters.tT1``.

### FbLowPassFilter
Function block is used to smooth noisy input signals. It can also be used to define the upper and lower alarm limits.

**Description:**
The ``rInput`` input signal is smoothed via a PT1 circuit and output at the ``rOutput`` output. If the input signal violates the defined limits for a defined time, an alarm message is output at the ``xAlarm`` output. In this case, the ``rOutput`` output assumes the defined default setting. The alarm can be acknowledged after elimination of the error via a positive edge at the ``xQuit`` input, or by automatic acknowledgement. .. note:: - The parameter ``typConfigParameters.tCycleTime`` needs to be smaller than ``typConfigParameters.tT1``.

### FbContinuousDamper
Function block is used for controlling continuous dampers. As an option, the damper position can also be monitored by the function block.

**Description:**
Damper control is enabled via the ``xEnableSystem`` input. During night ventilation, the damper can also be opened independently of this enable via the ``xNightVentilation`` input. When the Manual mode is activated via the input ``xManualOperation``, the damper is controlled via the ``rManualValue`` input. The damper adjusting motor is controlled via the ``rY`` output. The output value ``wY_Analog`` has the same meaning as the ``rY`` output, the output just has the standardized values between 0 – 32767. When the position check-back signal is present with a permanent position deviation, the damper is closed and the ``xError`` is activated when the delay period is exceeded. The error message can be acknowledged via a flank at the ``xQuit`` input and the function block is enabled again. The current status for the damper is indicated via the ``wStatus`` output. The input/output variable ``dwOperatingMinutes`` indicates the operating time in minutes for the continuous damper. The operating minutes are counted when ``rY`` is greater than ``.rY_Min``. .. note:: The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload.

### Fb2PointDamper
Function block is used to control 2-point dampers with optional limit switches.

**Description:**
The damper is opened in the Automatic mode when the system has been enabled via ``xEnableSystem`` and the ``xOpenDamper`` input has been activated. During night ventilation, the damper can also be opened independently of this enable via the ``xNightVentilation`` input. When the Manual mode is activated via the ``xManualOperation``, the damper is controlled via the ``xManualOpen`` input. The damper adjusting motor is controlled via the ``xDamper`` output. The runtime of the damper is monitored when limit switches are provided for each direction of movement. When the maximum runtime is exceeded, the damper is closed and the ``xError`` output activated. The error message can be acknowledged via a flank at the ``xQuit`` input and the function block is enabled again. The ``xOpen`` and ``xClose`` outputs indicate the status of the damper (opened/closed). .. note:: If no limit switch is provided, the damper position is determined over time.

### FbSequenceController
The Sequence controller can support up to five (5) sequences [Library-parameter (MAX_SEQUENCES)]. If a malfunction occurs in one of these sequences, the sequence concerned is automatically disabled for the control system.

**Description:**
If the controller is enabled via the ``xEnable`` input, the set value for ``rY`` for the sequences is calculated from the input values ``rActualValue`` and ``rReferenceValue``.

### FbCalculatedSupplyTemperature
Function block calculates the reference value for the supply temperature as a function of the outside temperature. An additional ramp function is integrated to prevent overly rapid heating of the piping and the noises associated with this.

**Description:**
Calculation of the supply temperature is enabled via the ``xEnable`` input. When first enabled, the current supply temperature ``rSupplyTemperature`` is set as the starting value for the ramp function. The specified supply temperature ``rReferenceSupplyTemperature`` is calculated using the heating characteristic as a function of the outside temperature ``rOutsideTemperature``. The output for the reference supply temperature keeps pace with this as long as the calculated reference temperature, and the change rate, is less than the maximum change rate that has been defined. If the calculated reference supply temperature changes more rapidly than the defined change rate, the reference output will lag behind the calculated reference supply temperature. During this time, the ramp output is set TRUE. The reference room temperature is used for parallel shifting of the heating characteristic. When the ``xComfortMode`` input is activated (Comfort mode), the value for the ``rReferenceValueRoom`` input is used as the reference room temperature. When the ``xComfortMode`` input is deactivated (night-time economy mode), the temperature defined for the night-time economy mode is used as the reference room temperature. The caracteristic of the supply temperature to the outside temperture can be displayed as follows: .. figure:: ../../images/CalculatedSupplyTemperature_Characteristic.png :align: center :alt: Calculated supply temperature - characteristic Typical values for the heating curve are: +------------------+--------------+-----------+ | |

### FbCascadeController
Function block is a standard PID controller with freely configurable Start and Stop values. Additionally, the function block offers the possibility to change the operating direction of the controller.

**Description:**
The cascade controller (master controller) FbCascadeController function block determines the reference value for the slave controller. The function block also evaluates the required fan level as an option. If the controller is enabled via the ``xEnable`` input, the reference value for the slave controller ``rReferenceValueSlaveController`` is calculated from the input values ``rActualValue`` and ``rReferenceValue``. The outputs ``rMinReferenceValue`` and ``rMaxReferenceValue`` indicate the minimum and maximum reference value for the slave controller. This range applies both for the Automatic mode and for manual override. Manual override is activated via the ``xManualOperation`` input. During manual override, the reference value from the ``rManualValue`` input is output at the ``rReferenceValueSlaveController`` output. If the function for determining the required fan level is enabled, the required fan level is specified at the ``xSpeedLevel1`` and ``xSpeedLevel2`` outputs. At first, the fans run at level 1 as long until the set value for the slave controller has reached its maximum value when heating or its minimum value when cooling. After a defined delay time, the fan is switched to level 2. To prevent the actual value from rising due to the double volume flow rate, the reference value for the slave controller is reduced (heating) or increased (cooling) at the particular switching point. If the reference value for the slave controller falls below its limit (for heating), or rises above its limit (for cooling) again (Offset/2) plus the hysteresis (0.5 K), the fans are switched back to level 1 with a time delay. When switching back to level 1, the reference value for the slave controller is raised or lowered again as required.

### FbPlateHeatExchanger
The FbPlateHeatExchanger function block controls the plate-type heat exchanger. The two dampers for the exhaust air and the two dampers for the supply air of the heat exchanger are controlled separately, since it is important to prevent frost during the winter. This is accomplished by routing only a part of the supply air to the plate-type heat exchanger, while the other part is routed past the heat exchanger (bypass).

**Description:**
Control of the plate-type heat exchanger is enabled via the ``xEnable`` input. When enabled, the set value for energy recovery ``rY_EnergyRecovery`` is passed on to the ``rY_DamperExhaustAir`` output. During normal operation, the entire outside air is routed to the plate-type heat exchanger. There is a risk of freezing if the exhaust air temperature ``rExitAirTemperature`` falls below the minimum exhaust air temperature ``rMinExitAir``. In this case, an internal controller ensures that the supply air dampers ``rY_DamperSupplyAir`` route a portion of the outside air around the plate-type heat exchanger via the bypass. The bypass dampers are always open when the unit is switched off. Fouling of the plate-type heat exchanger is detected by a differential pressure monitor ``xDifferentialPressureMonitor``. In order that the fouling warning message is indicated even if the system is switched off, it is saved and indicated at the ``xError`` output. The warning message can be acknowledged via a flank at the ``xQuit`` input. The output values ``wY_DamperSupplyAir`` and ``wY_DamperExhaustAir`` have the same meaning as the ``rY_DamperSupplyAir`` and ``rY_DamperExhaustAir`` outputs, except that the outputs have standardized values between 0 – 32767. The bypass dampers are always open when the unit is switched off.

### FbValveAndPump
Function block serves to switch on pumps and valves depending on the demand.

**Description:**
The pump is switched via the ``xPump`` output when it is either enabled via the ``xEnablePump`` input, or when ``rValvePosition`` is greater than the minimum set value. When the switch-on conditions for the pump are no longer fulfilled and the a 3-way value has been selected in the configuration, the pump does not shut down until the defined follow-up time has elapsed. During this follow-up time, the ``xFollowUpTime`` output is activated. When ``rValvePosition`` is greater than the minimum set value, the valve is opened via the ``xValve`` output, or the valve position is specified from the input ``rValvePosition`` to the ``rY_Valve`` output. The output value ``wY_Valve`` has the same meaning as the ``rY_Valve`` output, except that the output has standardized values between 0 – 32767. In the Winter mode, the pump can also be switched on while deactivated when the outside temperature ``rOutsideTemperature`` falls below a defined limit. The pump is also switched on even if the system is switched off for ``xFrostAlarmAir`` or ``xFrostAlarmWater``. The valve position is unchanged and will be changed e.g. by the FbAntifreezeAir function block. On initiation of the ``xMaximalThermostat`` maximum thermostat function

### FbPumpFC
Function block is used for controlling and monitoring a pump, with actuation via a frequency converter.

**Description:**
Control of the pump is enabled via the ``xEnablePump`` input. When enabled, the frequency converter is activated via the ``xFC`` output. In the Automatic mode, the required speed from the ``rSpeedPump`` input is output directly at the ``rY_Pump`` output. The output value ``wY_Pump`` has the same meaning as the ``rY_Pump`` output, except that the output has standardized values between 0 – 32767. When the pump enable is canceled, the pump follow-up for a defined time before it switches off. During this follow-up time, the ``xFollowUpTime`` output is activated. A bypass contactor can be used in the event of a frequency converter malfunction. If the frequency converter reports a malfunction via the ``xErrorFC`` input, the frequency converter contactor is disconnected from the pump. When contactor monitoring reports the open (disconnected) status, the bypass contactor is activated with a time delay via the ``xBypass`` output. When the frequency converter malfunction is rectified, the bypass contactor is first opened and the contactor for the frequency converter re-activated with a time delay. When contactor monitoring is activated, the input ``xContactor`` monitors for proper functioning of the power contactor. The switch output is compared with the check-back signal from the contactor for this. If the switch status of the contactor differs from the respective output for more than one second, there is a contactor malfunction. In the event of a defective contactor, or an error message at the ``xMotorProtection`` and ``xRepairSwitch`` inputs, the pump is switched off and the ``xErrorPump`` output activated. A more detailed description of the malfunction is provided by the ``wStatus`` output. The malfunction can be acknowledged via a positive flank at the ``xQuit`` input. Manual override is activated via the ``xManualOperation`` input. During manual override, the frequency converter is activated via the ``xManualOn`` input and the pump controlled via the ``rManualSpeed`` input. In order to avoid pump blocking during extended downtimes, the pump can be put into operation at least once within a defined time period. The blocking protection function must be activated for this. During blocking protection, the pump is controlled with a defined speed. .. note:: #. The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload. #. Blocking protection can also be activated by a timer program, so that a potential pump error message is issued only during a defined time period.

### FbPump
Function block serves to switch on pumps depending on the demand.

**Description:**
Control of the pump is enabled via the ``xEnablePump`` input. When enabled, the pump is switched on via the ``xPump`` output. When the pump enable is canceled, the pump follow-up for a defined time before it switches off. During this follow-up time, the ``xFollowUpTime`` output is activated. In the Winter mode, the pump can also be switched on while deactivated when the outside temperature ``rOutsideTemperature`` falls below a defined limit. The pump is also switched on even if the system is switched off for ``xFrostAlarmAir`` or ``xFrostAlarmWater``. In order to avoid pump blocking during extended downtimes, the pump can be put into operation at least once within a defined time period. The blocking protection function must be activated for this. If there is a pump error message at the input ``xMotorProtection`` or ``xRepairSwitch``, the pump is switched off and the ``xErrorPump`` output activated. The error can be acknowledged via a positive edge at the ``xQuit`` input, or by automatic acknowledgement. Manual override is activated via the ``xManualOperation`` input. During manual override, the pump is controlled via the ``xManualSwitch`` input. .. note:: #. The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload. #. Blocking protection can also be activated by a timer program, so that a potential pump error message is issued only during a defined time period.

### FbHumidifier
Function block controls a humidifier.

**Description:**
Control of the humidifier is enabled via the ``xEnable`` input. When enabled, the set value for the humidifying sequence ``rY`` is passed on to the ``rY_Humidifying`` output. At the same time, the ``xHumidifying`` output is activated. The output value ``wY_Humidifying`` has the same meaning as the ``rY_Humidifying`` output, except that the output has standardized values between 0 – 32767. In the event of an error message at the ``xHumidistat`` and ``xExtErrorHumidifier`` inputs, the humidifier is switched off and the ``xError`` output activated. A more detailed description of the malfunction is provided by the ``wStatus`` output. The malfunction can be acknowledged via a positive flank at the ``xQuit`` input. Manual override is activated via the ``xManualOperation`` input. During manual override, the humidifier is switched on via the ``xManualOn`` input and the valve controlled via the ``rManualValue`` input. .. note:: The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload.

### FbRunAroundCoil
Function block controls a run-around coil system filled with glycol (air – glycol – air).

**Description:**
Control of the run-around coil system is enabled via the ``xEnable`` input. When enabled, the set value for energy recovery ``rY_EnergyRecovery`` is passed on to the ``rY_Valve`` output. The return temperature ``rReturnTemperature`` is monitored for a minimum value to prevent any damage due to frost. The reference value for the return temperature is shifted as a function of the outside temperature ``rOutsideTemperature`` over a 4-point characteristic curve. The return temperature controller is configured via a proportional band, with the set value for the valve ``rY_Valve`` determined via a MIN logic between the set value for energy recovery and the set value for the return temperature controller. The output value ``wY_Valve`` has the same meaning as the ``rY_Valve`` output, except that the output has standardized values between 0 – 32767. Icing (freezing) of the run-around coil system is detected by a differential pressure monitor ``xDifferentialPressureMonitor``. In order that the icing (freezing) message is indicated even if the system is switched off, the warning message is saved and indicated at the ``xError`` output. The warning message can be acknowledged via a flank at the ``xQuit`` input.

### FbRotaryHeatExchanger
Function block controls a rotary heat exchanger. It also provides for a self-cleaning function and control of the bypass dampers.

**Description:**
Control of the rotary heat exchanger is enabled via the ``xEnable`` input. When enabled, the set value for energy recovery ``rY_EnergyRecovery`` is passed on to the ``rY_RotaryHeatExchanger`` output. At the same time, the rotary heat exchanger is switched on via the ``xRotaryHeatExchanger`` output and the bypass dampers closed. The output value ``wY_RotaryHeatExchanger`` has the same meaning as the ``rY_RotaryHeatExchanger`` output, except that the output has standardized values between 0 – 32767. The rotary heat exchanger can be started up at least one time within a defined time period in order to avoid fouling of the heat exchanger over extended outage periods. Self-cleaning must be activated for this. Fouling of the rotary heat exchanger is detected by a differential pressure monitor ``xDifferentialPressureMonitor``. In order that the fouling warning message is indicated even if the system is switched off, it is saved and indicated at the ``xWarning`` output. Using the ``xExtErrorRotaryHeatExchanger`` input, it is possible to monitor for an external error message from the rotary heat exchanger. If an external error occurs, the ``xError`` output is set. At the same time, the rotary heat exchanger is switched off and the bypass dampers opened. The error and warning messages can be acknowledged via a flank at the ``xQuit`` input. Manual override is activated via the ``xManualOperation`` input. During manual override, the rotary heat exchanger is switched on via the ``xManualOn`` input and controlled via the ``rManualValue`` input. .. note:: #. The bypass dampers should be opened when they are de-energized. #. The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload.

### FbSequenceMixedAir
Function block converts the set value for the sequence controller into a setting value for the mixed air damper.

**Description:**
The sequence is enabled via the ``xEnable`` input. The output set value ``rY_FreshAir`` is then calculated from the set value from the sequence controller ``rY``. When enabled, the minimum fresh air rate ``rY_MinFreshAir`` is always maintained. The output value ``wY_FreshAir`` has the same meaning as the ``rY_FreshAir`` output, except that the output has standardized values between 0 – 32767. When the outside temperature ``rOutsideTemperature`` is higher than the exhaust air temperature ``rExhaustAirTemperature``, the fresh air percentage of the minimum fresh air rate is reduced (summer function). A hysteresis of 1 K is taken into account for the summer function. When the system is enabled, it is possible to force the fresh air percentage down to the minimum fresh air rate via the ``xMinFreshAir`` input. The ``xActive`` output indicates whether the set value for the mixed air damper is greater than zero. When the ``xEnable`` input is not activated, or when a malfunction is signaled at the ``xErrorSequence`` input, the variable ``typSequenceController`` notifies the sequence controller that this sequence must be skipped.

### FbSequenceHumidifying
The FbSequenceHumidifying function block converts the set value from the sequence controller into a setting value for the humidifier.

**Description:**
The sequence is enabled via the ``xEnable`` input. The output set value ``rY_Humidifying`` is then calculated from the set value from the sequence controller ``rY``. The output value ``wY_Humidifying`` has the same meaning as the ``rY_Humidifying`` output, except that the output has standardized values between 0 – 32767. The ``xActive`` output indicates whether the set value for the humidifier is greater than zero. When the ``xEnable`` input is not activated, or when a malfunction is signaled at the ``xErrorSequence`` input, the variable ``typSequenceController`` notifies the sequence controller that this sequence must be skipped.

### FbSequenceHeating
Function block converts the set value from the sequence controller into a setting value for the heating element.

**Description:**
The sequence is enabled via the ``xEnable`` input. The output set value ``rY_Heating`` is then calculated from the set value from the sequence controller ``rY``. The output value ``wY_Heating`` has the same meaning as the ``rY_Heating`` output, except that the output has standardized values between 0 – 32767. When the set value ``rY_Dehumidifying`` for dehumidifying is greater than zero, this sequence is inhibited for the heating register (preheater). The ``xActive`` output indicates whether the set value for the heating register is greater than zero. When the ``xEnable`` input is not activated, or when a malfunction is signaled at the ``xErrorSequence`` input, the variable ``typSequenceController`` notifies the sequence controller that this sequence must be skipped.

### FbSequenceEnergyRecovery
Function block converts the set value of the sequence controller into a setting value for energy recovery (rotary heat exchangers, plate-type heat exchangers or run-around coil system).

**Description:**
The sequence is enabled via the ``xEnable`` input. The output set value ``rY_EnergyRecovery`` is then calculated from the set value from the sequence controller ``rY``. The output value ``wY_EnergyRecovery`` has the same meaning as the ``rY_EnergyRecovery`` output, except that the output has standardized values between 0 – 32767. When the outside temperature ``rOutsideTemperature`` is higher than the exhaust air temperature ``rExhaustAirTemperature``, the set value for energy recovery is switched to maximum output (summer function). A hysteresis of 1 K is taken into account for the summer function. The ``xActive`` output indicates whether the set value for energy recovery is greater than zero. When the ``xEnable`` input is not activated, or when a malfunction is signaled at the ``xErrorSequence`` input, the variable ``typSequenceController`` notifies the sequence controller that this sequence must be skipped.

### FbSequenceDehumidifying
Function block converts the set value for the sequence controller into a setting value for the cooling register. The cooling register is actuated via a MAX logic between the set value from the cooling sequence and the set value from the dehumidifying sequence.

**Description:**
The sequence is enabled via the ``xEnable`` input. The output set value ``rY_Dehumidifying`` is then calculated from the set value from the sequence controller ``rY``. The output value ``wY_Dehumidifying`` has the same meaning as the ``rY_Dehumidifying`` output, except that the output has standardized values between 0 – 32767. The ``xActive`` output indicates whether the set value for dehumidifying is greater than zero. When the ``xEnable`` input is not activated, or when a malfunction is signaled at the ``xErrorSequence`` input, the variable ``typSequenceController`` notifies the sequence controller that this sequence must be skipped.

### FbSequenceCooling
Function block converts the set value for the sequence controller into a setting value for the cooling elements.

**Description:**
The sequence is enabled via the ``xEnable`` input. The output set value ``rY_Cooling`` is then calculated from the set value from the sequence controller ``rY``. The output value ``wY_Cooling`` has the same meaning as the ``rY_Cooling`` output, except that the output has standardized values between 0 – 32767. The ``xActive`` output indicates whether the set value for the cooling register is greater than zero. When the ``xEnable`` input is not activated, or when a malfunction is signaled at the ``xErrorSequence`` input, the variable ``typSequenceController`` notifies the sequence controller that this sequence must be skipped.

### FbPIDController2PIDSets
Function block provides the function for switching back and forth between two sets of PID controller parameters.

**Description:**
If the ``xEnable`` input is activated, the input values ``rActualValue`` and ``rReferenceValue`` are used to calculate the set value ``rY``. Manual override is activated via the ``xManualOperation`` input. During manual override, the reference value from the ``rManualValue`` input is output at the ``rY`` output. The output value ``wY_Analog`` has the same meaning as the ``rY`` output, except that the output has standardized values between 0 – 32767. When the controller reaches its maximum set value (``xMaxLimitReached``

### FbPIDController
Function block is a standard PID controller with freely configurable Start and Stop values. Additionally, the function block offers the possibility to change the operating direction of the controller.

**Description:**
If the ``xEnable`` input is activated, the input values ``rActualValue`` and ``rReferenceValue`` are used to calculate the set value ``rY``. Manual override is activated via the ``xManualOperation`` input. During manual override, the reference value from the ``rManualValue`` input is output at the ``rY`` output. The output value ``wY_Analog`` has the same meaning as the ``rY`` output, except that the output has standardized values between 0 – 32767. The output value ``wY_Analog`` has the same meaning as the output ``rY`` and depends on ``.rOutputMin`` and ``.rOutputMax``. The values of ``wY_Analog`` are scaled from 0-32767 instead of 0-100 as in ``rY``. ``wY_Analog`` is usable as long as ``.rOutputMax`` <

### FbLimitController
Function block serves as a limit controller to prevent a reference lower value (e.g. antifreeze controller) or a reference upper value (e.g. return temperature temperature limit controller) from being violated.

**Description:**
If the ``xEnable`` input is activated, the input values ``rActualValue`` and ``rReferenceValue`` are used to calculate the set value ``rY``. The output value ``wY_Analog`` has the same meaning as the ``rY`` output, except that the output has standardized values between 0 – 32767.

### FbDHWController
2-point controller regulates the domestic hot water (DHW) temperature for the storage tank using an upper and lower storage tank temperature sensor. When a supply temperature sensor is provided, the hot water storage tank is additionally protected against forced cooling.

**Description:**
Domestic hot water preparation (DHW preparation) is enabled via the input ``xEnable``. The hot water storage tank is charged when the upper storage tank temperature ``rUpperStorageTankTemperature`` , minus the hysteresis, is situated below the ``rReferenceDHWTemperature``. For charging, the valve ``rValvePosition`` is opened and the pump ``xChargingPump`` enabled. The output ``xPriorityDHWPreparation`` for domestic hot water priority will be activated, when following requirements are fulfilled: #. The upper storage temperature ``rUpperStorageTankTemperature`` is below the limit for the domestic hot water priority function. #. The supply temperature ``rSupplyTemperature`` falls within the upper storage temperature ``rUpperStorageTankTemperature`` plus the adjusted offset to the DHW reference value. The valve is closed and pump enable canceled when the upper storage tank temperature and the lower storage tank temperature is greater than the reference temperature. Forced charging of the storage tank takes place when the storage tank temperature ``rUpperStorageTankTemperature`` or ``rLowerStorageTankTemperature`` falls below the defined limit. This also happens, when the storage tank hasn’t reached the reference temperature and the supply temperature ``rSupplyTemperature`` falls below the defined limit. Forced charging of the storage tank is indicated via the ``xFrostProtection`` output. The specified supply temperature ``rReferenceSupplyTemperature`` is calculated using an offset to the DHW reference value ``rReferenceDHWTemperature`` and ensures sufficient heat transfer. For cooling protection, domestic hot water preparation is not enabled until the supply temperature ``rSupplyTemperature`` is greater than the upper storage tank temperature ``rUpperStorageTankTemperature``. If the supply temperature ``rSupplyTemperature`` does not achieve the required temperature within the defined time period, an alarm is issued via the output ``xSupplyTemperatureAlarm``. When automatic acknowledgement is activated, the malfunction is canceled automatically when the specified supply temperature is reached. The alarm can also be reset via the ``xQuit`` input. If there is a risk of overheating of heating units, the 2-point controller can be enabled via the ``xOverride`` input, independently of the ``xEnable`` input. In this case, the ``rOverrideTemperature`` is used as the specified storage tank temperature. .. note:: - Supply to the sensor can be blocked off when the valve is closed and the pump is shut down, depending on where the supply temperature sensor is installed. In this case the cool-down protection function must be deactivated. - If a 2-way valve is used in place of a 3-way valve, the charging pump will not be switched on as long as the full-way valve is closed. - When a 3-way valve is installed, a shorter overtravel time should be selected for the charging pump, as the hot water is routed directly into the return line and this could, under some circumstances, result in the return temperature being increased excessively. - If only the upper storage tank temperature sensor is present the measured value must be linked both to the input for the upper and for the lower storage tank temperature sensor.

### FbFan_FC
Function block controls and monitors a fan with actuation using frequency converters.

**Description:**
The fan is switched on the Automatic mode when the system has been enabled via ``xEnableSystem`` and the ``xEnableFan`` input has been activated. The frequency converter (FC) is controlled via the ``xFC`` output. In the Automatic mode, the required speed from the ``rSpeedFan`` input is output directly at the ``rY_Fan`` output. The output value ``wY_Fan`` has the same meaning as the ``rY_Fan`` output, the output just has standardized values between 0 – 32767. When night ventilation is enabled via the ``xNightVentilation`` input, the fan is switched on independently of ``xEnableSystem`` via the ``xEnableFan`` input. In this case, the set value ``.rSpeedFanNightVentilation`` is output at the ``rY_Fan`` output. The safety chain of the fan must operate error-free for proper control of the fan. The safety chain consists of the inputs: - ``xRepairSwitch`` (repair switch (break contact)), - ``xMotorProtection`` (motor protection switch (break contact)) - ``xV_Belt`` (runtime monitoring, V-belt monitoring) The following input is added to the safety chain when the ``.xAuxiliaryContact`` parameter is activated: - ``xContactor`` (contactor monitoring) This input monitors for correct functioning of the power contactor. The switch output is compared with the check-back signal from the contactor for this. If the switch status of the contactor differs from the respective output for more than one second, there is a contactor malfunction. If there is a malfunction in the safety chain, the fan is switched off and the ``xErrorFan`` output is activated. Runtime monitoring is only activated after an adjustable startup time, which is required by the motor to achieve the rated speed. In order to avoid a false alarm in the case of pressure fluctuations in the duct while the system is running, an additional response delay can be defined. A bypass contactor can be used in the event of a frequency converter malfunction. If the frequency converter reports a malfunction via the ``xErrorFC`` input, the frequency converter is disconnected from the fan via a contactor. When contactor monitoring reports the open (disconnected) status, the bypass contactor is activated with a time delay via the ``xBypass`` output. When the frequency converter malfunction is rectified, the bypass contactor is first opened and the contactor for the frequency converter re-activated with a time delay. The error message can be acknowledged via a flank at the ``xQuit`` input and the function block is enabled again. Manual override is activated via the ``xManualOperation`` input. During manual override, the fan is switched on via the ``xManualOn`` input and controlled via the ``rManualSpeed`` input. .. note:: The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload.

### FbFan_3Level
Function block controls and monitors a 3-level fan.

**Description:**
Refer to function description for ``FbFan_2Level``. .. note:: The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload.

### FbFan_2Level
Function block controls and monitors a 2-level fan.

**Description:**
The fan is switched on the Automatic mode when the system has been enabled via ``xEnableSystem`` and the ``xEnableFan`` input has been activated. In the automatic mode you can specify the desired fan level via the ``xSpeedLevel1`` and ``xSpeedLevel2`` inputs. If you select both fan levels, the fan remains in its last valid level. If level 2 is specified immediately during fan startup, the fan starts with level 1 and changes to level 2 after the startup time has expired. At the same time, the runtime monitoring is activated. If level 2 is specified immediately during fan startup, the fan starts with level 1 and changes to level 2 after the startup time has expired. At the same time, the runtime monitoring is activated. When night ventilation is enabled via the ``xNightVentilation`` input, the fan is controlled independently of ``xEnableSystem`` via the ``xEnableFan`` and ``xSpeedLevel1`` or ``xSpeedLevel2`` inputs. Manual override is activated via the ``xManualOperation`` input. During manual override, the fan is switched via the ``xManualLevel1`` and ``xManualLevel2`` inputs. The fan is controlled via the ``xLevel1`` and ``xLevel2`` outputs. The safety chain of the fan must operate error-free for proper control of the fan. The safety chain consists of the inputs: - ``xRepairSwitch`` (repair switch (break contact)), - ``xMotorProtection`` (motor protection switch (break contact)) - ``xV_Belt`` (runtime monitoring, V-belt monitoring) The following inputs are added to the safety chain when the ``.xAuxiliaryContact`` parameter is activated: - ``xContactorLevel1`` (monitoring of power contactor, Level 1) - ``xContactorLevel2`` (monitoring of power contactor, Level 2) These inputs monitor for correct functioning of the power contactor. The switching outputs are compared with the check-back signal from the contator for this. If the switch status of the contactor differs from the respective output for more than one second, there is a contactor malfunction. If there is a malfunction in the safety chain, the fan is switched off and the ``xErrorFan`` output is activated. Runtime monitoring is only activated after an adjustable startup time, which is required by the motor to achieve the rated speed. In order to avoid a false alarm in the case of pressure fluctuations in the duct while the system is running, an additional response delay can be defined. The error message can be acknowledged via a flank at the ``xQuit`` input and the function block is enabled again. .. note:: The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload.

### FbAntifreezeWater
Function block serves as a preventive frost protection by flushing the preheater and sends an error message in case of freeze danger (only with return sensor).

**Description:**
Flushing of the heating register is carried out only when the outside temperature ``rOutsideTemperature`` falls below the set limit for flushing. During flushing of the heating register, the ``rY_Flush`` output is set to 100% until the adjustable limit temperature limit in the return line is exceeded. If the return temperature fails to reach the limit temperature within the set delay period (no hot water), an error message is issued at the ``xStartupError`` output and the valve opened 100%. After flushing, the ``rY_Flush`` output is set to a defined value and reduced to 0% via a definable ramp. Even when it is switched off the antifreeze controller regulates the return temperature to a minimum reference value. The antifreeze controller is active as long as the return temperature remains below the limit for terminating the flushing process. If the return temperature falls below the limit for the frost alarm, there is a risk of freezing and the alarm ``xFrostAlarmWater`` is issued. Additionally, the set value for the heating register ``rY_Flush`` is set to 100%. The output value ``wY_Flush`` has the same meaning as the ``rY_Flush`` output, except that the output has standardized values between 0 – 32767. .. note:: If no return temperature sensor is present, flushing is performed in a time-controlled manner.

### FbAntiLegionella
The FbAntiLegionella function block safeguards hot water conditioning against Legionnaire's Disease bacteria by regularly increasing the temperature of the hot water. The hot water is heated further for a set time period to a defined anti-Legionnaires's disease reference value to achieve this.

**Description:**
During normal operation, hot water conditioning is activated either via the ``xManual`` input (Manual mode), or via the ``xAuto`` and ``xSwitchOnDHWPreparation`` inputs (switching signal from the time program). When domestic hot water preparation (DHW) is activated, domestic hot water preparation is enabled via the ``xDHWPreparation`` output and the reference value defined for DHW preparation output at the ``rReferenceDHWPreparation`` output.

### FbAntifreezeAir
Function block controls the temperature in the air intake by means of a freeze protection device and determines the maximum setting value for the heating register.

**Description:**
If the air-side antifreeze ``xFrostMonitor`` is activated, the valve for the heating register is opened 100%. In a non-faulted state, the maximum value for inputs ``rY_Heating``, ``rY_Flush`` and ``rY_Frost`` arrive at the ``rY`` output. The output value ``wY`` has the same meaning as the ``rY`` output, only the output has standardized values between 0 – 32767. The ``xFrostAlarmAir`` output ensures that the HVAC system is switched off via the FbCollectiveMalfunction function block and that the pump for the heating register is switched on as a frost protection measure. If the antifreeze protection device no longer reports an error, the warning message can be acknowledged via a flank at the ``xQuit`` input.

### FbBlockingProtectionAnalog
The FbBlockingProtectionAnalog function block provides a blocking protection function for analog actuating drives. In order to avoid blocking of the driver after extended outage periods, the driver can be put into operation at least once within a certain period of time.

**Description:**
The blocking protection is only checked in position 0 - „.rY_Min`` and activated after „.tMaxOff``. The function block is enabled via the ``xEnable`` input. The set value from the ``rY_Driver`` is output directly at the ``rY`` output as long as the blocking protection function is not active. The output value ``wY`` has the same meaning as the ``rY`` output, the output just has the standardized values between 0 – 32767. .. note:: Blocking protection can also be activated by a timer program, so that a potential driver error message is issued only during a defined time period.

### FbBlinker
The FbBlinker function block generates a blinking signal.

### FbFan_1Level
Function block controls and monitors a 1-level fan.

**Description:**
The fan is switched on the Automatic mode when the system has been enabled via ``xEnableSystem`` and the ``xEnableFan`` input has been activated. During night ventilation, the fan can also be switched on independently of this enable via the ``xNightVentilation`` iniput. When the Manual mode is activated via the input ``xManualOperation``, the fan is actuated via the ``xManualSwitch`` input. The fan is controlled via the ``xLevel1`` output. The safety chain of the fan must operate error-free for proper control of the fan. The safety chain consists of the inputs: - ``xRepairSwitch`` (repair switch (break contact)), - ``xMotorProtection`` (motor protection switch (break contact)) - ``xV_Belt`` (runtime monitoring, V-belt monitoring) - ``xContactor`` (contactor monitoring) If there is a malfunction in the safety chain, the fan is switched off and the ``xErrorFan`` output is activated. Runtime monitoring is only activated after an adjustable startup time, which is required by the motor to achieve the rated speed. In order to avoid a false alarm in the case of pressure fluctuations in the duct while the system is running, an additional response delay can be defined. The ``xContactor`` input monitors for correct functioning of the power contactor. For this purpose the "xLevel1" output is compared with the feedback signal of the contactor. If the switch status of the contactor differs from the "xLevel1" output for more than one second, there is a contactor malfunction. The error message can be acknowledged via a flank at the ``xQuit`` input and the function block is enabled again. .. note:: The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload. .. note:: The idle time is not required with a single-level fan!

### FbPWM
Function block generates a pulse-width modulated output signal from a percentage set value.

**Description:**
When the ``xEnable`` input is activated, the PWM signal is calculated from the ``rY`` input variable and the signal output at the ``xPWM`` output. The ``xPWM`` output is deactivated as soon as the ``xEnable`` input is deactivated. A new cycle duration begins when the PW signal is enabled again. The FbPWM function block works ``dynamically`` to achieve quicker response times. The activation period for the digital output signal is calculated continuously. Thus, the switching times are also adjusted during the active periods.

### FbContinuousDriver
The FbContinuousDriver function block is used for controlling continuous drivers. A driver position can also be monitored as an option.

**Description:**
The driver control is enabled via the ``xEnable`` input. When the Manual mode is activated via the input ``xManualOperation``, the driver is controlled via the ``rManualValue`` input. The driver is controlled via the ``rY`` output. The output value ``wY`` has the same meaning as the ``rY`` output, the output just has the standardized values between 0 – 32767. When the position check-back signal is present with a permanent position deviation, the driver is closed and the ``xError`` is activated when the delay period is exceeded. The error message can be acknowledged via a flank at the ``xQuit`` input and the function block is enabled again. In order to avoid blocking of the driver after extended outage periods, the driver can be put into operation at least once within a certain period of time. The blocking protection function must be activated for this. The driver is moved to a settable position during the blocking protection function period. The current status for the driver is output via the ``wStatus`` output. The input/output variable ``dwOperatingMinutes`` indicates the operating minutes for the continuous driver. The operating minutes are counted when ``rY`` is greater than ``.rY_Min``. .. note:: #. The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload. #. Blocking protection can also be activated by a timer program, so that a potential error is issued only during a defined time period.

### FbAnalog3Point
The FbAnalog3Point function block converts an analog set value into a 3-point signal. The actuating drive has the status OFF, ON and CLOSED. The setting values are calculated dynamically for this.

**Description:**
The input value ``rInput`` is converted into a running time for the control valve. The engine position is stored within the module and is displayed at the output ``rY``. If the value at the ``rInput`` input differs from the output value ``rY`` by the set hysteresis, the driver is actuated via the ``xOpen`` and ``xClose`` in accordance with the given sign for the difference. The check-back signal from the limit switches can be linked via an OR element to the ``xLimitSwitch`` input. A limit switch error is issued at the ``wStatus`` output under the following conditions when the monitoring function is activated: #. When ``rY`` is situated between 10% and 90% and the ``xLimitSwitch`` input is TRUE #. When the override time elapses at ``rY`` 0% or 100% and the ``xLimitSwitch`` input is FALSE The error message is reset only by a synchronization run. A synchronization run is performed either by starting the program, or by a positive edge at the ``xInit`` input. During the synchronizatin run, the actuator is closed for the set maximum runtime, plus the override period and the setting value re-referenced. The synchronization run is indicated at the ``wStatus`` output. The position of the motor is determined using a timing element. Therefore, a synchronization is performed each time an end position is reached. .. note:: Actuation can be continued even after the driver linked to the system has reached its end position by overriding the driver. It should be clarified beforehand with the valve manufacturer, whether this status has no negative effect on the valve. We recommend control valves with built-in limit switches.

### FbSummerNightVentilation
Summer often offers the possibility of cooling down the room temperature with the cool night air. This function block is used to utilize the possibility of effective night cooling to control the unit components necessary for cooling.

**Description:**
Starting conditions for night ventilation: The following points must all be fulfilled before night cooling (ventilation) is enabled via ``xNightVentilation``: - ``xEnable``

### FbStartStopOptimization
Function block calculates the optimal start and stop times of a heating installation.

**Description:**
The FbStartStopOptimization function block calculates the optimal start and stop times of a heating installation. The start time optimization aims to reach the required temperature at the beginning of the service period by starting up the heating on time. The stop time optimization switches the heating off before the end of service. In this process, the temperature may not be/fall below the defined specified temperature. The optimization function can be deactivated by setting the ``xEnable`` input to FALSE signal. In this case, the ``xSwitchOn`` is linked directly to the ``xHeating`` output. The time remaining until the service period ``iTimeBeforeOperation`` begins, or the remaining time up to the end of the service period, is determined by a FbScheduler function block.

### FbStartStopHeatingCircuit
Function block is used for switching the heating circuit on/off.

**Description:**
The FbStartStopHeatingCircuit function block is used for switching the heating circuit on/off. Start optimization, a heating limit based on the outside temperature and a Support mode have been implemented to determine the optimal on/off times. The input signals ``xAuto`` and ``xManual`` are operated by a rotary switch on the switch cabinet and are locked against each other. The rotary switch has the positions: Auto − Off − Manual. The heating circuit is enabled via the ``xEnableSystem`` output when one of the following conditions is met: - ``xManual`` - ``xAuto``, ``xHeatingPeriod`` and ``xSwitchOnComfortMode`` - ``xAuto``, ``xHeatingPeriod`` and ``.xEconomyMode`` (Night-time economy mode) When the heating circuit has been enabled, the Comfort mode is activated via the ``xComfortMode`` output when one of the following conditions is met: - ``xManual`` - ``xAuto`` and ``xSwitchOnComfortMode`` (e.g., enabled from a timer program) The set Comfort mode temperature is specified via the ``rRoomComfortTemperature`` input. A room temperature sensor is required to determine an optimal starting time. The characteristic curve for start optimization is adjusted automatically at the beginning of use as a function of the difference between the current room temperature ``rRoomTemperature`` and the reference room temperature ``rRoomComfortTemperature``. Automatic adjustment of the characteristic curve cannot take place for start optimization without a room temperature sensor. Premature activation of the heating circuit by start optimization is indicated at the ``xOptimization`` output. The time remaining until the beginning of use is communicated to the block via the ``iTimeBeforeOperation`` input. A more detailed description of Start optimization is given in the documentation for the FbStartStopOptimization function block. The heating circuit is switched on in the Support mode if the room temperature ``rRoomTemperature`` drops below the minimum room temperature ``rMinRoomTemperature``. The Support mode is indicated at the ``xSupportMode`` output. Two different values are taken into account for detecting a heating period. If the averaged outside temperature ``rAveragedOutsideTemperature`` and the damped outside temperature ``rDampedOutsideTemperature`` fall below the defined limit, the heating period is enabled via the ``xHeatingPeriod`` output. The heating period is terminated if one of these two values rise above the defined limit again.

### FbStartStop
Function block serves for switching a HVAC system on and/or off.

**Description:**
The input signals ``xAuto`` and ``xManual`` are operated by a rotary switch on the switch cabinet and are locked against each other. The rotary switch has the positions: Auto − Off − Manual. During manual operation, the HVAC system is switched on directly via the ``xEnableSystem`` output. During automatic operation, the ``xEnableSystem`` output is switched via the ``xSwitchOn`` input (e.g. enabling a clock timer). If a system malfunction is reported via the ``xSystemError`` input, the ``xEnableSystem`` and ``xSystemOk`` outputs are set to FALSE. If the malfunction has been corrected and the ``xSystemError`` input is FALSE, the ``xSystemOk`` output is automatically set to TRUE.

### Fb2PointSingleRoomController
Function block allows individual room reference temperature control while taking local influences into account.

**Description:**
The room temperature ``rActualTemperature`` is yielded from the measured room temperature ``rRoomTemperature`` and the variable measured value compensation. The 2-point controller compares the room temperature ``rActualTemperature`` (actual value) with the desired heating and cooling reference values and sends the corresponding switching telegrams for heating ``xHeating`` and cooling ``xCooling``. The controller detects four operating modes to each of which is assigned its own set value. The ``rReferenceComfort`` set value is used as a basic set value. All other set values refer to the basic set value and provoke each a set value increase or set value decrease by a parameterized value. The reference value for the Comfort mode can be infinitely shifted via the ``rSetpointCorrection`` input. The active operating mode (Comfort, Stand-by, Night, Antifreeze protection) is determined via the ``xComfortStandby``, ``xNightMode`` and ``xWindowContact`` inputs. The currently selected operating mode is viasualized via ``xComfort``, ``xStandby``, ``xNight`` and ``xFrost_Heat``. If the function module is used for cooling purposes, another ``xDewpoint`` input is required.If a dew point alarm is signaled at this input, the cooling/heating valves close accordingly. The function module has eight monitor outputs ``rComfortHeating``, ``rComfortCooling``, ``rStandbyHeating``, ``rStandbyCooling``, ``rNightHeating``, ``rNightCooling``, ``rSetpointFrost`` and ``rSetpointHeat``. The current set values of the individual operating modes are put out via these outputs. .. figure:: ../../images/PIDSingleRoomController_Setpoints.png :align: center :alt: Temperature setpoints for different operating status +-----------------------+------------------------------------------------------+--------------------------------------------------------------+ |

### FbRamp
Function block ensures a defined rising or falling rate for a particular setting.

**Description:**
When the function block is activated via the ``xEnable`` input, the output signal ``rOutput`` follows the input signal ``rInput`` only as long as the rising or falling rate of the input signal is less than the maximum rising or falling rate. If the input signal changes more rapidly, the output follows the input signal at the defined maximum rising or falling rate. When the function block is deactivated, the output signal ``rOutput`` follows the ``rInput`` input signal directly. The ``xActive`` output indicates whether the ramp is active.

### FbGlobalMalfunction
Function block evaluates the error messages from up to eight collective malfunction modules and generates a global collective malfunction message from these.

**Description:**
The FbGlobalMalfunction function block evaluates the error messages from up to eight collective malfunction modules and generates a global collective malfunction message from these. The output signal ``xSignalLamp`` for the FbCollectiveMalfunction function block is linked to the ``xSignalLampX`` input for evaluation of the error message. If one of the collective malfunction modules signals an error, this is indicated at the ``xSignalLamp`` output.

### FbFilterMonitoring
The function block indicates the fouling of an air filter using differential pressure monitors to get maintenance.

**Description:**
The filters are normally monitored using differential pressure monitors. The differential pressure monitors report fouling of the filter system via the inputs ``xFilter``. An On-delay ``tOnDelay`` can be defined for the ``xFilter`` input to prevent fouling from being signaled in the duct when pressure fluctuations occur. Fouling of the filter is indicated via the ``xMaintenance`` output. If the differential pressure no longer report fouling of the filter, the message can be acknowledged via a flank at the ``xQuit`` input. .. note:: You can select for visualization of the filter whether the filter is to be located in the supply (incoming) air or in the exhaust air.

### FbCollectiveMalfunction
Function block only collects serious errors that would cause a system shutdown.

**Description:**
This function block has been designed to only collect serious errors that would cause a system shutdown. If the ``xEnableSystem`` or ``xNightVentilation`` input is activated and one of the inputs ``xMains``, ``xEmergencyOff``, ``xStartupError``, ``xErrorFanSupplyAir``, ``xErrorFanExhaustAir``, ``xFrostAlarmAir``, ``xFrostAlarmWater``, ``xErrorPump``, ``xFireAlarm``, ``xErrorDamperSupplyAir``, ``xErrorDamperSupplyAir``, ``xMalfunction1`` or ``xMalfunction2`` is set to TRUE, an alarm is issued. The error messages can be either visual or audible messages. An audible error message can be triggered via the ``xHorn`` output until the error is acknowledged via the ``xQuit`` input. The visual error message can be triggered via the ``xSignalLamp`` output. With every error message that appears, the error indicator lamp starts to blink with a frequency of 1 Hz and the horn is activated. If the error is acknowledged via the ``xQuit`` input, the error indicator lamp will be lit continuously. Only if there is no longer an error at the inputs is it possible to delete the the error message via the ``xQuit`` input. At the same time, the ``xSystemError`` output issues a collective malfunction alarm (non-blinking) that shuts down the system via the FbStartStop function block. .. note:: If you also want to receive error messages when the system is turned off, ``EnableSystem`` should be permanently set to TRUE.

### FbOperatingHours_01
The FbOperatingHours_01 function block determines the operating hours, expressed in minutes.

**Description:**
When the ``xEnable`` input is activated, the minutes of operation ``dwOperatingMinutes`` are counted upward minute by minute. If the counter is to be initialized with values, the variable ``dwOperatingMinutes`` can be directly overwritten. The operating hours calculated from the minutes of operation are indicated at the ``dwOperatingHours`` output. .. Note:: The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload.

### FbMinMidMax
Function block calculates a minimum value, an average value and a maximum value from up six values.

**Description:**
The value ``bNumber`` indicates how many inputs are analyzed for the calculation of these values. The minimum value ``rMinValue``, the average value ``rAverageValue`` and the maximum value ``rMaxValue`` are calculated from the input values ``rValue_1`` – ``rValue_6``.

### FbImpulseCounter
Function block is used for integrating meters with an impulse interface (e.g. electricity, heat or water meters).

**Description:**
This function block counts the impulses at the ``xPulseInput`` and calculates the consumption values from this (energy). The counter values are deleted by a positive edge at the ``xReset`` input. If the counter is to be initialized with values, the variables ``dwCounterValue`` and ``rCounterPostComma`` can be directly overwritten. Power measurement: The pulses are extrapolated with their valence for the defined time base in order to determine the current output ``rTimedRate``. .. note:: #. The calculation of the performance is not exact and regular. The output value for the performance therefore only gives an approximate overview of the currently needed performance. #. The program cycle time must be less than the time between two pulses. #. The input/output variables ``dwCounterValue`` and ``rCounterPostComma`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload. #. If more than 2 decimal places of the ``typConfigParameters.rUnitPerPulse`` are used, the global variable „g_bDecimalPlaces” must be changed.

### FbHysteresis
Function block permits a switching function with adjustable hysteresis.

**Description:**
Two variations are to be considered during the analysis of the input values: #. rActivate > rDeactivate The output signal ``xOutput`` is set to TRUE, if the condition ``rInput`` >

### FbModulatingBoiler
The FbModulatingBoiler function contains various startup processes based on the pumps and valves used in the specific configuration and also regulates a modulating boiler.

**Description:**
The boiler is activated either via the ``xManual`` input, or via the two inputs ``xAuto`` and ``xSwitchOnBoiler``. When activated, the minimum boiler supply temperature is output for evaluation of the system supply temperature at the ``rMinBoilerTemperature`` output. The specific boiler number ``bBoilerNumber`` and the number of the lead boiler ``bLeadBoiler`` determine whether the boiler is the lead or lag boiler. If both of these numbers are the same, the parameters for the lead boiler will be used. Different startup procedures can apply, depending on the valve being used and the water volume. The following three procedures are possible. 2-way valve with large volume of water: #. Switch on the admixing pump ``xAdmixingPump``. #. Switch on the burner ``xEnableBurner`` (``rY_Burner``

### Fb2LevelBoiler
Function block contains various startup processes based on the valves and pumps used in the specific configuration and also regulates a 2-level boiler.

**Description:**
The boiler is activated either via the ``xManual`` input (Manual mode), or via the two inputs ``xAuto`` and ``xSwitchOnBoiler``. When activated, the minimum boiler supply temperature is output for evaluation of the system supply temperature at the ``rMinBoilerTemperature`` output. The specific boiler number ``bBoilerNumber`` and the number of the lead boiler ``bLeadBoiler`` determine whether the boiler is the lead or lag boiler. If both of these numbers are the same, the parameters for the lead boiler will be used. Different startup procedures can apply, depending on the valve being used and the water volume: 2-way valve with large volume of water: #. Switch on the admixing pump ``xAdmixingPump``. #. Level 1 ``xLevel1`` is activated when the boiler temperature ``rActualBoilerTemperature`` is less than the specified boiler temperature ``rReferenceBoilerTemperature``, plus the defined offset. #. The 2-way valve ``xValve`` is opened when the minimum boiler temperature is exceeded. #. If the boiler temperature fails to reach the minimum boiler temperature within a defined time, condensation protection ``xCondensationProtection`` is activated and this indicated at the ``wStatus`` output. #. The boiler circuit pump ``xBoilerPump`` is switched on when the defined delay period has elapsed, or when a positive edge at the ``xLimitSwitchValve`` input reports the open status of the valve. #. If the 2-way valve fails to reach its final position within the defined runtime, the boiler is switched off and an error message output at the ``wStatus`` output. #. The startup procedure is terminated once the boiler circuit pump has been switched on. If the startup procedure exceeds the maximum defined time, the ``xErrorStartUp`` output is set and a warning issued at the ``wStatus`` output. .. figure:: ../../images/TwoLevelBoiler_ProcessDiagram1.png :align: center :alt: process diagram 2-way valve with large volume of water 2-Way Valve with low water volume: #. Switch on the admixing pump ``xAdmixingPump``. #. Open the 2-way valve ``xValve`` #. The boiler circuit pump ``xBoilerPump`` is switched on when the On-delay for the pump has elapsed, or when a positive edge at the ``xLimitSwitchValve`` input reports the open status of the valve. #. The burner ``xEnableBurner`` is activated when the boiler temperature ``rActualBoilerTemperature`` is less than the specified boiler temperature ``rReferenceBoilerTemperature``. #. The startup procedure is terminated when the minimum runtime for Level 1 elapses. #. If the 2-way valve fails to reach its final position within the defined runtime, the boiler is switched off and an error message output at the ``wStatus`` output. #. The admixing pump is switched off as soon as the minimum return temperature and the minimum supply temperature are exceeded. .. figure:: ../../images/TwoLevelBoiler_ProcessDiagram2.png :align: center :alt: process diagram 2-way valve with low water volume 3-way valve: #. Switch on the admixing pump ``xAdmixingPump``. #. Switch on the boiler circuit pump ``xBoilerPump`` #. Level 1 ``xLevel1`` is activated when the boiler temperature ``rActualBoilerTemperature`` is less than the specified boiler temperature ``rReferenceBoilerTemperature``. #. 3-way valve ``rY_Valve`` is closed (boiler circuit) #. The startup procedure is terminated as soos as the return temperature rises above the minimum return temperature. #. If the minimum return temperature is not reached with the defined time, the ``xErrorStartUp`` output is activated and a warning issued via the ``wStatus`` output. .. figure:: ../../images/TwoLevelBoiler_ProcessDiagram3.png :align: center :alt: process diagram 3-way valve After the startup procedure the boiler remains at the first level for at least the minimum switch-on time. If the boiler fails to reach its specified boiler temperature within the defined time, the boiler is switched to Level 2 ``xLevel2``. When the boiler then reaches its specified boiler temperature, it is switched back from Level 2 to Level 1. The boiler is switched to Level 2 again when the temperature falls below the specified boiler temperature, minus hysteresis. The boiler switches from Level 1 to Level 0 when the specified boiler temperature is maintained for the minimum switch-on time for the Level 1 time. The boiler is switched back to Level 1 if its temperature falls below the specified boiler temperature at Level 0. .. figure:: ../../images/TwoLevelBoiler_ProcessDiagram4.png :align: center :alt: process diagram after start procedure If there is a 3-way valve in the boiler return line, the minimum return temperature is permanently maintained during ongoing operation. A PI controller is used for the minimum return temperature. The admixing pump ``xAdmixingPump`` is switched on during ongoing operation when the temperature falls below the minimum boiler temperature or the minimum return temperature when a 2-way valve is available. If the temperature drops below the minimum boiler temperature, the ``xCondensationProtection`` output is also set. The boiler circuit pump continues to run when the boiler is switched off until the Switch-off delay time elapses and the difference between ``rActualBoilerTemperature`` and ``rActualReturnTemperature`` is less than the defined difference. The valve in the return line is not closed until the boiler circuit pump is switched off. If the ``xFullLoad`` input is set using the strategy module, the boiler module no longer regulates the temperature in line with its specified boiler temperature, but is controlled only by maximum limiting. The necessary information about the boiler is supplied to the strategy module through the ``typStatusBoiler`` structure. The ``xSafetyChain`` input monitors the safety chain for the boiler. As soon as this input is switched to FALSE, the boiler is switched off and a corresponding error message indicated at the ``wStatus`` output. In the event of a malfunction with the boiler circuit pump caused by the motor protection switch ``xMotorProtectionPump`` or the repair switch ``xRepairSwitchPump``, the boiler is switched off and the error indicated at the ``wStatus`` and ``xErrorBoilerPump`` output. In the event of a malfunction of the admixing pump caused by the motor protection switch ``xMotorProtectionAdmixingPump`` or the repair switch ``xRepairSwitchAdmixingPump``, the admixing pump is switched off and the error indicated at the ``xErrorAdmixingPump`` output. The error messages can be acknowledged via a flank at the ``xQuit`` input. When the chimney sweep function ``xChimneySweepFunction`` is activated, the boiler switches on with an elevated reference value (maximum boiler temperature Level 2). The ``xChimneySweep`` output is set as a check-back signal that the chimney sweep function has been activated. The chimney sweep function is canceled when the ``xChimneySweepFunction`` input is deactivated, or when the maximum runtime has elapsed. In the Manual mode ``xManualOperation`` the boiler level is controlled via ``bManualLevelBoiler``, the boiler circuit pump via ``xManualOnBoilerPump``, the admixing pump via ``xManualOnAdmixingPump`` and the valve via ``rManualValueValve``. If the boiler is switched to the Manual mode via an external circuit, a check-back signal should be transmitted to the boiler module via the ``xFeedbackManualOperation`` so that automatic control can be deactivated. The pump or valve can be put through a maintenance run to prevent them from blocking during extended outage periods. Blocking protection must be activated for this. The blocking protection function ensures that the pump and the valve do not remain switched off/closed longer than the specified monitoring period. On expiration of this time period, the pump and the valve are activated one after the other for the maintenance run for the defined time. The output value ``wY_Valve`` has the same meaning as the ``rY_Valve`` output, except that the output has standardized values between 0 – 32767. .. note:: #. The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload. #. The input ``xLimitSwitchValve`` must be set to TRUE when a 2-way valve without a limit switch is used.

### Fb2BoilerStrategy
Function block enables a boiler sequence control be enabling the two boilers in line with current demand.

**Description:**
The lead boiler can be defined for boiler sequence control via the ``bLeadBoiler`` input. Both boilers are controlled simultaneously if a zero is present at the ``bLeadBoiler`` input. In the event of a boiler malfunction, the lead boiler is changed.The current lead boiler is indicated at the ``bLeadingBoiler`` output. The reference system supply temperature is specified at the ``rReferenceSystemSupplyTemperature`` input. This can be determined, for example, via a MAX logic circuit for the requisite supply temperatures for the HVAC circuits linked to the system. The specified boiler temperature is indicated at the ``rReferenceTemperatureBoiler`` and is yielded from the specified system supply temperature, plus the defined offset. If the system supply temperature ``rActualSystemSupplyTemperature`` falls below the specified boiler temperature ``rReferenceTemperatureBoiler``, the lead boiler is enabled via the ``xSwitchOnBoilerX`` output. When the lead boiler reaches it maximum output and the specified system supply temperature is still not achieved, the lag boiler is then enabled ``xSwitchOnBoilerX`` with a defined delay time. At the same time, the lead boiler is put into full load via the ``xFullLoadBoilerX`` output. When operating at full load, the lead boiler is limited by the maximum boiler temperature. The enable function for the lag boiler remains active until the system supply temperature is achieved and the lag boiler is switched off. As soon as the enable function for the lag boiler ``xSwitchOnBoilerX`` is canceled, the full load signal ``xFullLoadBoilerX`` from the lead boiler is also canceled. The enable signal for the lead boiler is canceled when the system supply temperature is reached and the lead boiler is switched off. The boiler sequence control is deactivated when one of the two boilers is in the Manual mode. If the system supply temperature ``rActualSystemSupplyTemperature`` exceeds the defined maximum system supply temperature, the enable signal for both boilers is canceled and the ``xOverheatingProtection`` output activated. Overheating protection is deactivated when the system supply temperature falls below the maximum system supply temperature, minus the hysteresis. The status check-back signal from the boiler modules is given by ``typStatusBoilerX``. The process is displayed below: .. figure:: ../../images/TwoBoilerStrategie_ProcessDiagram.png :align: center :alt: 2 Boiler strategie - process diagram

### FbDampedTemperature
Function block calculates the damped temperature by averaging the temperature values measured up to a defined point (e.g. outside tmperature).

**Description:**
Averaging of the temperature values is enabled via the ``xEnable`` input. When this function block is enabled, the measured values from the ``rTemperature`` input are saved to the buffer and an average calculated from the values contained in the buffer. This average value is output at the ``rDampedTemperature`` output. The scanning interval for the damped outside temperature is calculated as follows: Scanning interval

### FbOptimizedSupplyTemperature
Function block ensures that the specified supply temperature for a heating register is optimized as a function of the valve position.

**Description:**
Supply temperature optimization is enabled via the ``xEnable`` input. After being enabled, the optimization module ensures that the reference supply temperature ``rOptReferenceSupplyTemperature`` is optimized between the ``rReferenceSupplyTemperature`` and the minimum reference supply temperature as a function of the valve position. A PI controller, which determines the necessary reference supply temperature as a function of the current valve position ``rActualValueValve`` and the specified valve position, is used for optimization. The last reference supply temperature that has been established ``rOptReferenceSupplyTemperature`` is ``frozen`` when the ``xLockSupplyTemperature`` input is activated. If ``xEnable`` is not activated, ``rReferenceSupplyTemperature`` is output directly at the ``rOptReferenceSupplyTemperature`` output. The caracteristic can be displayed as follows: .. figure:: ../../images/OptimizedSupplyTemperature_Characteristic.png :align: center :alt: optimized supply temperature - characteristic

### FbMinFreshAir
Using the FbMinFreshAir function block, the minimum fresh air rate can be reduced to 50% at temperatures below 0°C or above 26°C in accordance with DIN 1946 Part 2.

**Description:**
When the outside temperature ``rOutsideTemperature`` is within the defined limits, the set minimum fresh air rate is output at the ``rY_MinFreshAir`` output. Of the outside temperature ``rOutsideTemperature`` above/below the defined limits, the reduced minimum fresh air rate is output at the ``rY_MinFreshAir`` output.

### Fb2PointDriver
The Fb2PointDriver function block is used to control 2-point drivers with optional limit switches.

**Description:**
The driver is opened in the Automatic mode when the system has been enabled via ``xEnable`` and the ``xOpenDriver`` input has been activated. When the Manual mode is activated via the ``xManualOperation``, the driver is controlled via the ``xManualOpen`` input. The driver is controlled via the ``rDriver`` output. The runtime of the driver is monitored when limit switches are provided for each direction of movement. When the maximum runtime is exceeded, the driver is closed and the ``xError`` output activated. The error message can be acknowledged via a flank at the ``xQuit`` input and the function block is enabled again. In order to avoid blocking of the driver after extended outage periods, the driver can be put into operation at least once within a certain period of time. The blocking protection function must be activated for this. The ``xOpen`` and ``xClose`` outputs indicate the status of the driver (opened/closed). The current status for the driver is output via the ``wStatus`` output. .. note:: #. If no limit switch is provided, the driver position is determined over time. #. Blocking protection can also be activated by a timer program, so that a potential driver error message is issued only during a defined time period.

### FbTemperatureOverride
Function block is used for overriding the specified temperature. If the heating unit temperature is too high, this function block can be used for forced dissipation of the heat to the downstream heating circuit. If, on the other hand, insufficient thermal output is available for domestic hot water preparation, forced reduction of the specified temperature for the heating circuit can be induced.

**Description:**
The reference supply temperature from the ``rReferenceTemperature`` input is output directly at the ``rOverrideTemperature`` output as long as no override function is active. Overheating protection is activated via the ``xOverheatingProtection`` input. The reference temperature for overheating protection is signaled at the output ``rOverrideTemperature`` when the overheating protection function is activated. The DHW priority function is activated via the ``xPriorityDHWPreparation`` input. The reference temperature for condensation protection is signaled at the ``rOverrideTemperature`` output when the DHW priority function is activated. The ``xOverride`` output is activated as long as overheating protection of the DHW priority function is activated. At the conclusion of the overheating protection or DHW priority function the reference supply temperature ``rOverrideTemperature`` is re-adjusted to the normal value via a ramp function. As long as it active, the ramp function is indicated at the ``xRamp`` output.

### FbHeatingCharacteristics
The FbHeatingCharacteristics heating characteristic function block calculates the reference value for the supply temperature as a function of the outside temperature. The heating characteristic is defined by slope and curvature.

**Description:**
Calculation of the supply temperature is enabled via the ``xEnable`` input. The ``rReferenceValueRoom`` can also be used for parallel shifting of the heating characteristic. The specified supply temperature ``rReferenceSupplyTemperature`` is calculated using the heating characteristic as a function of the outside temperature ``rOutsideTemperature``. .. figure:: ../../images/CalculatedSupplyTemperature_Characteristic.png :align: center :alt: Calculated supply temperature - characteristic Typical values for the heating curve are: +------------------+--------------+-----------+ | |

### FbEnthalpy
The function block calculates the water content ``rWaterContent``, the saturated water content ``rSaturationWater``, the dew point temperature ``rDewpointTemperature`` and the enthalpy ``rEnthalpy`` of air.

**Description:**
In order to calculate these values it is necessary to know the temperature ``rTemperature`` and the relative humidity ``rRelativeHumidity``. Another input value is the relative pressure ``wAthmosphericPressure``. If the atmospheric pressure is not measured, a constant value can be chosen from the table below. With temperatures below -15 °C the saturated water content is set to 1g/kg, with temperatures above 45 °C, the value is set to 65.4 g/kg. With a water content of less than 1 g/kg the dew point temperature is set to -15 °C, with a water content of more than 55.6 g/kg, the value is set to 42 °C. +--------------------------------+--------------+ |

### FbAveragedOutsideTemperature
Function block measures the outside temperature at 7:00 a.m., at 2:00 p.m. and at 7:00 p.m. The average outside temperature is calculated applying different weighting to the measured temperatures.

**Description:**
The current time is detected via the ``dtActualTime`` input. The measured outside temperature is accepted by the ``rOutsideTemperature`` input for calculation of the average outside temperature when the defined time of day is reached. The number of days over which the outside temperature is to be averaged can be defined at the ``bNumberOfDays`` input. The input/output variable ``rAveragedOutsideTemperature`` indicates the outside temperature averaged over the set number of days. The ``rDailyAveragedOutside Temperature`` output indicates the average outside temperature for the previous day only. The ``xValid`` output is TRUE when measured values for at least one day are available. The measured values can be deleted via the ``xReset`` input. .. note:: The ``rAveragedOutsideTemperature`` variable should be declared as RETAIN PERSISTENT.

## Data Types

### typSequenceController
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbPIDSingleRoomController: FbPIDSingleRoomController;
END_VAR

// Basic function block usage
fbFbPIDSingleRoomController(
    // Configure inputs as needed
);

// Check status
IF fbFbPIDSingleRoomController.xValid THEN
    // Operation successful
END_IF

IF fbFbPIDSingleRoomController.xError THEN
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

