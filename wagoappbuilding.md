# WagoAppBuilding v1.0.2.16

## Overview
WAGO PLC library providing WagoAppBuilding functionality.

**Key Features:**
- Control functions
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbEvaluateSingleButton_1
The function block evaluates single button presses to double button presses for switching and dimming.

### FbEvaluateShortLongPress_1
The ``FbEvaluateShortLongPress`` function block detects whether binary input signal is set shorter or longer than a specified time.

### FbEvaluateShortLongPress
The ``FbEvaluateShortLongPress`` function block detects whether binary input signal is set shorter or longer than a specified time.

### FbEvaluateSingleButton
The function block evaluates single button presses to double button presses for switching and dimming.

### FbCalculateSunriseSunset
The ``FbCalculateSunriseSunset`` function block is used to calculate the sunrise and sunset by the current time and geographic coordinates.

**Description:**
The UTC time ``dtUTC_Time`` is required to calculate the sunrise and sunset. The calculation with local time can be realized by using the ``rTimeZone`` input. The daylight saving time can be activated by switching the ``xDST`` input to TRUE. The actual position is determined via inputs ``rLatitude`` and ``rLongitude``. Latitude ``rLatitude`` and longitude ``rLongitude`` can also be calculated as follows: Latitude :

### FbControlSunshadeScene
**Description:**
Ten different scenes with position values can be saved. The individual scenes are called up via a rising edge at one of the ``xScene1..10`` inputs. The ``bScene`` output displays the scene currently called up. The function block provides to options for saving scenes. - With the first option, all scenes can be stored directly. The position values for all scenes are entered in the ``atypSunshadeScenes`` input/output variable. This option is suitable for specifications at start-up. - With the second option, the current scene can be changed. The position values of the sunshade must be restored at the ``typLearnSunshadePosition`` input. A rising edge at the ``xLearnScene`` input saves the position values from ``typLearnSunshadePosition`` to the scene ``atypSunshadeScenes[X]`` currently called up. This option is suitable for manually adjust a scene. The ``typSetSunshade`` output variables contain the position commands for the sunshade actuator. The ``typSetSunshade.xMove`` variable is briefly set to TRUE when controlling a scene. .. note:: - To ensure the saved scene values are retained even after a power failure, the ``atypSunshadeScenes`` input/output variable should be declared as RETAIN PERSISTENT. - The set position values must be in the range of 0 – 100%. Otherwise, the sunshade actuator ignores the command. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+-----------------------------------+ |

### FbLightControl_02_Segments
The ``FbLightControl_02_Segments`` function block can be used for segment control or partition wall control of the lighting for 2 segments. Segment control is used to evaluate partition wall information and to transfer set value information to the segments.

**Description:**
The ``xPartition`` input is used to detect if a partition between two segments is open or closed. If open, the ``xPartition`` input is switched to FALSE. The segments are merged and viewed as one large segment. The merged segments are switched together. If closed, the ``xPartition`` input is switched to TRUE. The segments are switched independently. The first partition ``aL_Segment[1]`` is located between segments one and two. The ``aL_Segment`` assigned by the Segment outputs of the lighting function blocks. The switching behavior of the segments is specified by the actuator function blocks. The ``aSwitchActuator`` output signals the digital switching states of the connected actuators. If a percentage dimming value is greater than 0, ``aSwitchActuator[X]`` switches to TRUE. The ``arActuator`` output signals the percentage dimming values. The dimming value is specified by the dimming values of the connected actuators. The ``aActuatorAnalog`` output signals the dimming value as a signal in a range of 0 to 32767. For example, this output can be used for an analog output module.

### FbMacroDaylightDependentLighting
The ``FbMacroDaylightDependentLighting`` function block switches the room lighting depending on presence detection.

**Description:**
The ``FbMacroDaylightDependentLighting`` function block is used for daylight dependent room lighting to ensure the minimum light intensity. Daylight is taken into account. If there is sufficient natural light, the artificial lighting is switched off. If the setpoint is not reached, the lighting is switched on. After the lighting is switched on and the configurable time has elapsed, the switch-off threshold for artificial light is automatically adjusted, so that the minimum light intensity is ensured continuously. The daylight dependent lighting can be overridden by the button inputs or a scene recall. The ``xPresence`` input defines the occupancy status of the room. A change to the occupancy status leads to instantaneous switching. The measured light intensity of the sensor is connected to the ``rSensorLightLevel`` input. The sensor must be calibrated with parameters for the ``typConfigDaylightDependentLighting.typBrightnessMeasurement`` brightness measurement. Calibration is described in :ref:`doc_Calibration`. The ``xOn`` and ``xOff`` button inputs override automatic daylight dependent lighting. A rising edge at the ``xOn`` input switches the lighting on. A rising edge at the ``xOff`` input switches the lighting off. The override is reset after a configurable time. The ``xActuator`` output indicates the digital switching state. If a percentage dimming value is greater than 0, ``xActuator`` switches to TRUE. The ``rActuator`` output indicates the percentage dimming value. The value is specified by the ``typConfigDaylightDependentLighting. typDaylightDependentLighting.rSwitchOnValue`` switch-on-threshold or the ``typL_SCENE.rDimValue`` scene value. In the OFF state, the dimming value is 0. The ``wActuator`` output indicates the dimming value as a signal in a range of 0 to 32767. For example, this output can be used for an analog output module. The ``xManualOverride`` output signals that the automatic function is overridden. The ``typL_Segment`` is used to connect the function block to the segment control. See also typConfigParameters (:ref:`typConfigDaylightDependentLighting`), it contains all parameter values for the function block.

### FbSunshadeControlSegments
The ``FbSunshadeControlSegments`` function block can be used for segment control or partition wall control of the sunshade for 24 segments. Segment control is used to evaluate partition wall information and to transfer set value information to the segments.

**Description:**
The ``aPartition`` input is used to detect if a partition between two segments is open or closed. If open, the ``aPartition[X]`` input is switched to FALSE. The segments are merged and viewed as one large segment. The merged segments receive motion commands together. If closed, the ``aPartition[X]`` input is switched to TRUE. The segments are moved independently. The first partition ``aPartition[1]`` is located between segments one and two. The ``aIN_Segment`` input variable is assigned the input signals of the individual segments. Input signals of the same segments are assigned to the same array index. The ``aOUT_Segment`` output delivers the input signals for the sunshade actuators. Sunshade actuators of the same segments are assigned to the same array index. .. Note:: If a segment increases in size by removing the partition, the positions of the sunshades must be synchronized in the individual segments. This can be realized by starting together.

### FbMacroConstantLightControl
The ``FbMacroConstantLightControl`` function block is used for automatic control of room lighting to a minimum light intensity. Daylight is taken into account. A PID controller controls the lighting internally. The constant light control can be overridden by button inputs or a scene recall.

**Description:**
The ``xPresence`` input is connected to the presence detection. It defines the occupancy status of the room. A change to the occupancy status leads to instantaneous switching. Calibration of the brightness measurement is described in :ref:`doc_Calibration`. The measured light intensity of the sensor is connected to the ``rSensorLightLevel`` input. The sensor must be calibrated with parameters for the ``typConfigContantLightControl.typBrightnessMeasurement`` brightness measurement. The ``xOnAndStepUp`` and ``xOffAndStepDown`` button inputs override the automatic constant light control for a configurable time. The button inputs evaluate short and long button commands. A short button press transmits an ON/OFF command. The switch-on dimming value can be parameterized. A long button press transmits an UP/DOWN command. The dimming value can be dimmed between the dimming value range. The ``xCentralOn`` and ``xCentralOff`` inputs serve to connect central ON/OFF commands. The ``xCentralOn`` input sends an ON command to the maximum dimming value in the case of a rising edge. The ``xCentralOff`` input sends an OFF command in the case of a rising edge. The actuation time of the ``xCentralOn`` and ``xCentralOff`` inputs does not affect the switching behavior. The ``typL_SCENE`` input is used for scene control and can be linked to a scene function block. When an update signal is received, the defined dimming value is transmitted and the automatic constant light control overridden. See also typConfigParameters (:ref:`typConfigConstantLightControl`), it contains all parameter values for the function block. +-------------------------+------------------------+ |

### FbMacroAutomaticLights
The ``FbMacroAutomaticLights`` function block switches the room lighting depending on presence detection. Natural lighting by daylight is ignored. The function block is particularly suited for rooms without direct sunlight, e.g. corridors and restrooms.

**Description:**
The ``xPresence`` input is connected to the presence detection. The light is switched ON when presence detection is enabled. If presence detection is disabled, the light is switched off after the OFF delay has elapsed. The ``xActuator`` output indicates the digital switching state. If a percentage dimming value is greater than 0, ``xActuator`` switches to TRUE. The ``rActuator`` output indicates the percentage dimming value. The value is specified by the ``typAutomaticLights.rSwitchOnValue`` switch-on value. In the OFF state, the dimming value is 0. The ``wActuator`` output indicates the dimming value as a signal in a range of 0 to 32767. For example, this output can be used for an analog output module. See also typConfigParameters (:ref:`typConfigAutomaticLights`), it contains all parameter values for the function block. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+------------------------+ |

### FbDimSingleButton
The ``FbDimSingleButton`` function block can be used to dim a light with a single button.

**Description:**
The ``xButton`` button input evaluates short and long button commands. A short button press transmits an ON/OFF command. The switch-on value can be parameterized. A long button press transmits an UP/DOWN command. The light is dimmed up after switching on. The dimming value can be dimmed between the limiting values. The ``xCentralOn`` and ``xCentralOff`` inputs serve to connect central ON/OFF commands. The ``xCentralOn`` input sends an ON command to the maximum dimming value in the case of a rising edge. The ``xCentralOff`` input sends an OFF command in the case of a rising edge. The actuation time of the ``xCentralOn`` and ``xCentralOff`` inputs does not affect the switching behavior. The ``typL_SCENE`` input is used for scene control and can be linked to a scene function block. When an update signal is received, the defined dimming value is transmitted. The ``rFeedback`` input is used as status feedback when connecting to the segment control. The current dimming value of a segment must be passed to the ``rFeedback`` input. Hence the function block will receive the current dimming value. The ``rRecoveryValue`` input/output variable maps the switching behavior after voltage recovery. The assignment is explained in the table below. The ``xActuator`` output indicates the digital switching state. If a percentage dimming value is greater than 0, ``xActuator`` switches to TRUE. The ``rActuator`` output indicates the percentage dimming value. The possible dimming value in the ON state is limited by the maximum and minimum dimming value. In the OFF state, the dimming value is 0. The ``wActuator`` output indicates the dimming value as a signal in a range of 0 to 32767. For example, this output can be used for an analog output module. The ``typL_Segment`` is used to connect the function block to the segment control. The following behaviors can be defined for the switching behavior after voltage recovery: +------------------------------------------------------------------+---------------------------------------------+--------------------------------------+ |

### FbDimDoubleButton
The ``FbDimDoubleButton`` function block can be used to dim a light with a double button.

**Description:**
The ``xOnAndStepUp`` and ``xOffAndStepDown`` button inputs evaluate short and long button commands. A short button press transmits an ON/OFF command. The switch-on value can be parameterized. A long button press transmits an UP/DOWN command. The dimming value can be dimmed between the limiting values. The ``xCentralOn`` and ``xCentralOff`` inputs serve to connect central ON/OFF commands. The ``xCentralOn`` input sends an ON command to the maximum dimming value in the case of a rising edge. The ``xCentralOff`` input sends an OFF command in the case of a rising edge. The actuation time of the ``xCentralOn`` and ``xCentralOff`` inputs does not affect the switching behavior. The ``typL_SCENE`` input is used for scene control and can be linked to a scene function block. When an update signal is received, the defined dimming value is transmitted. The ``rFeedback`` input is used as status feedback when connecting to the segment control. The current dimming value of a segment must be passed to the ``rFeedback`` input. Hence the function block will receive the current dimming value. The ``rRecoveryValue`` input/output variable maps the switching behavior after voltage recovery. The assignment is explained in the table below. The ``xActuator`` output indicates the digital switching state. If a percentage dimming value is greater than 0, ``xActuator`` switches to TRUE. The ``rActuator`` output indicates the percentage dimming value. The possible dimming value in the ON state is limited by the maximum and minimum dimming value. In the OFF state, the dimming value is 0. The ``wActuator`` output indicates the dimming value as a signal in a range of 0 to 32767. For example, this output can be used for an analog output module. The ``typL_Segment`` is used to connect the function block to the segment control. See also typConfigParameters (:ref:`typConfigDim`), it contains all parameter values for specifying the operator control action The following behaviors can be defined for the switching behavior after voltage recovery: +------------------------------------------------------------------+---------------------------------------------+--------------------------------------+ |

### FbAdvancedLatchingRelay
The ``FbAdvancedLatchingRelay`` function block maps the function of a latched relay. The switching function corresponds to a toggle flip-flop. The function block makes it possible to define a switching value with voltage recovery.

**Description:**
The function block reacts to rising switching signals at the ``xButton`` input. With every positive switching signal at the ``xButton`` input, the latched relay switches its status value at the ``xActuator`` output. The ``xCentralOn`` and ``xCentralOff`` inputs serve to connect central ON/OFF commands. The ``xCentralOn`` input sends an ON command in the case of a rising edge. The ``xCentralOff`` input sends an OFF command in the case of a rising edge. The ``typL_SCENE`` input is used for scene control and can be linked to a scene function block. When an update signal is received, the transmitted switching value will be evaluated. If a scene switching value is greater than 0, ``xActuator`` switches to TRUE. The ``xFeedback`` input is used as status feedback when connecting to the segment control. The current switching state of a segment must be passed to the ``xFeedback`` input. Hence the function block will receive the current switching state. The ``xActuator`` output indicates the switching state of the latched relay. The ``typL_Segment`` is used to connect the function block to the segment control. The following states can be defined for the switching behavior after voltage recovery: - Always switch off after voltage recovery: Initialize the variable ``xRecoveryValue`` with FALSE - Always switch on after voltage recovery: Initialize the variable ``xRecoveryValue`` with TRUE - Always recover the last value after voltage recovery: Declare the variable ``xRecoveryValue`` as RETAIN PERSISTENT without initialization. See also typL_SCENE (:ref:`typLight`), it can be linked to a scene function block. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+------------------------+ |

### FbCalculateSunPosition
The ``FbCalculateSunPosition`` function block is used to calculate the current position of the sun by the current time and geographic coordinates.

**Description:**
The UTC time ``dtUTC_Time`` is required to calculate the position of the sun. The actual position is determined via inputs ``rLatitude`` and ``rLongitude``. Latitude ``rLatitude`` and longitude ``rLongitude`` can also be calculated as follows: Latitude :

### FbLowPassFilterTemp
Function block scales the input value and smoothens noisy input signals. It can also be used to define the upper and lower alarm limits.

**Description:**
The ``iInput`` input signal is divided by ten (°C) and smoothed via a PT1 circuit. The scaled and smoothed value is output at the ``rOutput`` output. If the input signal violates the defined limits for a defined time, an alarm message is output at the ``xAlarm`` output. In this case, the ``rOutput`` output assumes the defined default setting. The alarm can be acknowledged after elimination of the error via a positive edge at the ``xQuit`` input, or by automatic acknowledgement. TypConfigParameters includes all configuration parameter. .. note:: - The parameter ``typConfigParameters.tCycleTime`` musst be smaller than ``typConfigParameters.tT1``.

### FbBasicWeatherProtection
The ``FbBasicWeatherProtection`` function block is used for weather protection by external sunshades against damage caused by wind, rain or icing.

**Description:**
The ``FbBasicWeatherProtection`` function block is used for weather protection by external sunshades against damage caused by wind, rain or icing. The detected sensor values of wind velocity, outside temperature and precipitation detection are evaluated and trigger the safety function of the sunshade actuator when there is a risk of damage. The time-related behavior for the wind alarm and frost alarm is shown below as an example. The ``FbBasicWeatherProtection`` function block combines the functions of the :ref:`FbFrostAlarm` and :ref:`FbWindAlarm`. The explanation of the inputs can be found in the above descriptions. The configuration parameters at the “typConfigWeatherProtection” input also come from the FbFrostAlarm and FbWindAlarm function blocks. The “xSafety” output signals when the safety function of the sunshade is switched on. The output can be connected to the signal output for the safety position of the sunshade actuator. The “xError” output signals a time-out of the wind sensor or incorrect parameterization of the function block thresholds. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+------------------------+ |

### FbAdvanceWeatherProtection
The ``FbAdvanceWeatherProtection`` function block is used for weather protection by external sunshades against damage caused by wind, rain or icing. The detected sensor values of wind velocity, outside temperature and precipitation detection are evaluated and trigger the safety function of the sunshade actuator when there is a risk of damage. .. note:: This function block should only be used together with one wind assessment.

**Description:**
The ``FbAdvanceWeatherProtection`` function block is based on the :ref:`FbBasicWeatherProtection` function block. The explanation of the inputs can be found in the above description. The measured wind direction ``rWindDirection`` is connected to the function block. The wind direction is assigned with a wind sector. The measured wind strength is multiplied by the factor of the wind sector and the calculated wind strength further processed. The ``xSafety`` output signals when the safety function of the sunshade is switched on. The output can be connected to the signal output for the safety position of the sunshade actuator. The ``iWindSector`` output signals the active wind sector. The ``xError`` output signals a time-out of the wind sensor or incorrect parameterization of the function block thresholds. See also typWindAssessment (:ref:`typWindAssessment`), it contains all parameter values for wind assessment. See also typConfigParameters (:ref:`typConfigWeatherProtection`), it contains all parameter values for the function block.

### FbOperatingHours_01
The ``FbOperatingHours_01`` function block determines the operating hours express in minutes.

**Description:**
When the ``xEnable`` input is activated, the minutes of operation ``dwOperatingMinutes`` are counted upward minute by minute. If the counter is to be initialized with values, the variable ``dwOperatingMinutes`` can be directly overwritten. The operating hours calculated from the minutes of operation are indicated at the ``dwOperatingHours`` output. .. Note:: The operating minutes function ``dwOperatingMinutes`` should be defined as RETAIN PERSISTENT so that the set values are retained in the event of a loss of power or after a project upload.

### FbHysteresis
The ``FbHysteresis`` function block permits a switching function with adjustable hysteresis.

**Description:**
Two variations are to be considered during the analysis of the input values: #. rActivate > rDeactivate The output signal ``xOutput`` is set to TRUE, if the condition ``rInput``  ``rActivate`` is fulfilled. The output signal ``xOutput`` is set to FALSE, if the condition ``rInput``  ``rDeactivate`` is fulfilled. The output signal does not change as long as the input value moves between the values ``rActivate`` and ``rDeactivate``. .. image:: ../../Images/Hysteresis_ActDeact.png :align: center :alt: Hysteresis characteristic for Activation bigger than Deactivation #. rDeactivate > rActivate The output signal ``xOutput`` is set to TRUE, if the condition ``rInput``  ``rActivate`` is fulfilled. The output signal ``xOutput`` is set to FALSE, if the condition ``rInput``  ``rDeactivate`` is fulfilled. The output signal does not change as long as the input value moves between the values ``rActivate`` and ``rDeactivate``. .. image:: ../../Images/Hysteresis_DeactAct.png :align: center :alt: Hysteresis characteristic for Deactivation bigger than Activation

### FbLowPassFilterBus
Function block scales the input value and smoothens noisy input signals. It can also be used to define the upper and lower alarm limits.

**Description:**
The ``rInput`` input signal is divided by ten (°C) and smoothed via a PT1 circuit. The scaled and smoothed value is output at the ``rOutput`` output. If the input signal violates the defined limits for a defined time, an alarm message is output at the ``xAlarm`` output. In this case, the ``rOutput`` output assumes the defined default setting. The alarm can be acknowledged after elimination of the error via a positive edge at the ``xQuit`` input, or by automatic acknowledgement. TypConfigParameters includes all configuration parameter. .. note:: - The parameter ``typConfigParameters.tCycleTime`` musst be smaller than ``typConfigParameters.tT1``.

### FbLowPassFilterAI
The ``FbLowPassFilterAI`` function block scales the input value and smoothens noisy input signals. It can also be used to define the upper and lower alarm limits.

**Description:**
The ``wInput`` input signal is scaled using a 4-point characteristic curve and smoothed via a PT1 circuit. The scaled and smoothed value is output at the ``rOutput`` output. If the input signal violates the defined limits for a defined time, an alarm message is output at the ``xAlarm`` output. In this case, the ``rOutput`` output assumes the defined default setting. The alarm can be acknowledged after elimination of the error via a positive edge at the ``xQuit`` input, or by automatic acknowledgement. TypConfigParameters includes all configuration parameter. .. note:: - The parameter ``typConfigParameters.tCycleTime`` musst be smaller than ``typConfigParameters.tT1``.

### FbLowPassFilter
The ``FbLowPassFilter`` function block is used to smooth noisy input signals. It can also be used to define the upper and lower alarm limits.

**Description:**
The ``rInput`` input signal is smoothed via a PT1 circuit and output at the ``rOutput`` output. If the input signal violates the defined limits for a defined time, an alarm message is output at the ``xAlarm`` output. In this case, the ``rOutput`` output assumes the defined default setting. The alarm can be acknowledged after elimination of the error via a positive edge at the ``xQuit`` input, or by automatic acknowledgement. TypConfigParameters includes all configuration parameter. .. note:: - The parameter ``typConfigParameters.tCycleTime`` musst be smaller than ``typConfigParameters.tT1``.

### FbEvaluateMultipleClicks
The ``FbWB_EvaluateMultipleClicks`` function block detects if a certain number of pushbutton signals has been made on the binary input signal.

**Description:**
The number of pushbutton signals can be parameterized at the ``bNumberOfClicks`` input. If fewer pushbutton signals occur during the parameterizable time ``tPeriodToClick``, the ``xFewerClick`` output is set to 1 for the time of one task cycle. If at least ``bNumberOfClicks`` pushbutton signals occur during the period ``tPeriodToClick``, the ``xMultipleClick`` output signals is set to 1 for the time of one task cycle.

### FbSunshadeControl_03_Segments
The ``FbSunshadeControl_03_Segments`` function block can be used for segment control or partition wall control of the sunshade for 3 segments. Segment control is used to evaluate partition wall information and to transfer set value information to the segments.

**Description:**
The ``aPartition`` input is used to detect if a partition between two segments is open or closed. If open, the ``aPartition[X]`` input is switched to FALSE. The segments are merged and viewed as one large segment. The merged segments receive motion commands together. If closed, the ``aPartition[X]`` input is switched to TRUE. The segments are moved independently. The first partition ``aPartition[1]`` is located between segments one and two. The ``aIN_Segment`` input variable is assigned the input signals of the individual segments. Input signals of the same segments are assigned to the same array index. The ``aOUT_Segment`` output delivers the input signals for the sunshade actuators. Sunshade actuators of the same segments are assigned to the same array index. .. Note:: If a segment increases in size by removing the partition, the positions of the sunshades must be synchronized in the individual segments. This can be realized by starting together.

### FbSunshadeControl_02_Segments
The ``FbSunshadeControl_02_Segments`` function block can be used for segment control or partition wall control of the sunshade for 2 segments. Segment control is used to evaluate partition wall information and to transfer set value information to the segments.

**Description:**
The ``xPartition`` input is used to detect if a partition between two segments is open or closed. If open, the ``xPartition`` input is switched to FALSE. The segments are merged and viewed as one large segment. The merged segments receive motion commands together. If closed, the ``xPartition`` input is switched to TRUE. The segments are moved independently. The ``aIN_Segment`` input variable is assigned the input signals of the individual segments. Input signals of the same segments are assigned to the same array index. The ``aOUT_Segment`` output delivers the input signals for the sunshade actuators. Sunshade actuators of the same segments are assigned to the same array index. .. Note:: If a segment increases in size by removing the partition, the positions of the sunshades must be synchronized in the individual segments. This can be realized by starting together.

### FbLightControlSegments
The ``FbLightControlSegments`` function block can be used for segment control or partition wall control of the lighting for 24 segments. Segment control is used to evaluate partition wall information and to transfer set value information to the segments.

**Description:**
The ``typPartition`` input is used to detect if a partition between two segments is open or closed. If open, the ``typPartition[X]`` input is switched to FALSE. The segments are merged and viewed as one large segment. The merged segments are switched together. If closed, the ``typPartition[X]`` input is switched to TRUE. The segments are switched independently. The first partition ``typPartition[1]`` is located between segments one and two. The ``typL_Segment`` assigned by the Segment outputs of the lighting function blocks. The switching behavior of the segments is specified by the actuator function blocks. The ``aSwitchActuator`` output signals the digital switching states of the connected actuators. If a percentage dimming value is greater than 0, ``aSwitchActuator[X]`` switches to TRUE. The ``arActuator`` output signals the percentage dimming values. The dimming value is specified by the dimming values of the connected actuators. The ``aActuatorAnalog`` output signals the dimming value as a signal in a range of 0 to 32767. For example, this output can be used for an analog output module.

### FbLightControl_03_Segments
Function block can be used for segment control or partition wall control of the lighting for 3 segments. Segment control is used to evaluate partition wall information and to transfer set value information to the segments.

**Description:**
The ``aPartition[x]`` input is used to detect if a partition between two segments is open or closed. If open, the ``aPartition[x]`` input is switched to FALSE. The segments are merged and viewed as one large segment. The merged segments are switched together. If closed, the ``aPartition[x]`` input is switched to TRUE. The segments are switched independently. The first partition ``aL_Segment[1]`` is located between segments one and two. The ``aL_Segment`` assigned by the Segment outputs of the lighting function blocks. The switching behavior of the segments is specified by the actuator function blocks. The ``aSwitchActuator`` output signals the digital switching states of the connected actuators. If a percentage dimming value is greater than 0, ``aSwitchActuator[X]`` switches to TRUE. The ``arActuator`` output signals the percentage dimming values. The dimming value is specified by the dimming values of the connected actuators. The ``aActuatorAnalog`` output signals the dimming value as a signal in a range of 0 to 32767. For example, this output can be used for an analog output module.

### FbControlLightScene
The ``FbControlLightScene`` function block can be used to choose between several types of room utilization to adjust room conditions for lighting.

**Description:**
For each scene, five lighting groups can be defined with different brightness values. The individual scenes are called up via a rising edge at one of the ``xScene1..10`` inputs. The ``bScene`` output displays the scene currently called up. The function block provides two options for saving scenes. - all scenes and all groups can be stored directly. The scenes are saved by writing the ``atypLightScenes`` input/output variable. The dimming values are entered for all scenes and all groups. This option is suitable for specifications at start-up. - With the second option, all groups of the current scene can be saved. The dimming values of all lighting groups must be restored at the ``arLearnSceneValues`` input. A rising edge at the ``xLearnScene`` input saves the dimming values from ``arLearnSceneValues`` to the scene ``atypLightScenes[X]`` currently called up. This option is suitable for manually adjust a scene. .. Note:: - The selection of individual groups from the ``atypL_SCENE`` output can be realized with the |FuGetLightSceneValue| function. - To ensure the saved scene values are retained even after a power failure, the ``atypLightScenes`` input/output variable should be declared as RETAIN PERSISTENT. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+-----------------------------------+ |

### FbPresenceSensor
The ``FbPresenceSensor`` function block can be used to evaluate occupancy information transmitted by a presence detector and a manual control element.

**Description:**
The presence detector is connected to the ``xSensorSignal`` input. The manual occupancy status is applied at the ``xManualOccupancy`` input. The presence output immediately responds to switching signals from the ``xManualOccupancy`` status. With the help of an adjustable holding time ``tHoldingTime``, the occupancy status after a falling edge of the presence signal ``xSensorSignal`` can be held for a certain time. With the ``xAND`` input, the logical link control of the ``xSensorSignal`` and ``xOccupancyButton`` inputs for presence detection can be defined. A TRUE signal stands for an AND link, a FALSE signal stands for an OR link. The ``xPresence`` output signals the current presence status. This is the result of the logical combination of the presence inputs. The ``tElapsedTime`` time displays the elapsed time since the last presence detection. With renewed presence detection, the time is reset. If the ``tHoldingTime`` holding time at the ``tElapsedTime`` output has elapsed, the ``xPresence`` present status is set to FALSE. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+------------------------+ |

### FbSunshadeSlatTracking
The ``FbSunshadeSlatTracking`` function block maps the function of the slat tracking. Like the automatic solar control, the slat tracking prevents the impact to the user by incoming sunrays of high intensity by moving to an antiglare position.

**Description:**
In contrast to the automatic solar control, however, the position of the slats is adjusted to the current position of the sun when light intensity is high. In this way, every room receives optimal sunlight while preventing direct sunlight. With decreasing brightness or with the sun out of parameterized angle limits, a parking position is taken. The ``xEnable`` input can be used to disable automatic solar control. The information can be come from the time program or a command from the building management system. The measured intensity of the natural light is applied to the ``rIlluminance`` input. The ``dtUTC_Time``, ``rLatitude`` and ``rLongitude`` inputs are used to calculate the position of the sun. The elevation angle and azimuth angle are calculated and evaluated. The ``rLatitude`` and ``rLongitude`` coordinates are input as following: Value :

### FbSunshadeAutomaticTwilightControl
Function block can be used to position sunshades based on outdoor brightness. The sunshade can be moved during the night to reduce heat loss through the windows or to reduce light emissions.

**Description:**
The ``FbSunshadeAutomaticTwilightControl`` function block maps the function of the automatic twilight control. The automatic twilight control can be used to position sunshades based on outdoor brightness. The automatic control makes it possible, for example, to close the sunshade during the night to reduce heat loss through the windows or to reduce light emissions. The ``xEnable`` input can be used to disable automatic twilight control. The information can be come from the time program or a command from the building management system. The current measured intensity of the natural light is applied to the ``rIlluminance`` input. The parameters are configured using the ``typConfigParameters`` input. The „ xTwilightPosition`` and „ xSunrisePosition`` outputs display the active position. The position command of the twilight position is assigned permanently. The position command of the sunrise position is assigned temporary with a rising edge. The ``typAutomaticSunshade`` output variable contains the position commands for the sunshade actuator.

### FbSunshadeAutomaticSolarControl
The ``FbSunshadeAutomaticSolarControl`` function block prevents the impact to the user by incoming sunrays of high intensity.

**Description:**
The ``FbSunshadeAutomaticSolarControl`` function block maps the function of the automatic solar control. The automatic solar control prevents the impact to the user by incoming sunrays of high intensity by moving the sunshade to a defined antiglare position once the natural light exceeds a defined intensity. With decreasing brightness, a waiting position is taken. If the brightness falls below a defined intensity, a parking position is taken. The ``xEnable`` input can be used to disable automatic solar control. The information can be come from the time program or a command from the building management system. The current measured intensity of the natural light is connected the ``rIlluminance`` input. The parameters are configured using the ``typConfigParameters`` input. The „xAntiGlarePosition``, „xWaitingPosition`` and „xParkingPosition`` outputs display the active position. The position commands of the antiglare and waiting position are assigned permanently. The position command of the parkting position is assigned temporary with a rising edge. The ``typAutomaticSunshade`` output variable contains the position command for the sunshade actuator.

### FbSunshadeHeatingSupport
The ``FbSunshadeHeatingSupport`` function block is used to support heating by the sunshade. Solar thermal energy is allowed specifically in unoccupied rooms to reduce the heat energy expended.

**Description:**
Heating support is activated by a low room temperature or open heating valve. The heating support keeps permanently inactive for a parametrable time after its deactivation. The ``xPresence`` input is connected to the presence detection. If presence is detected, heating support is disabled. A change in the presence detection leads to undelayed switching behavior. The measured intensity of the natural light is applied to the ``rIlluminance`` input. The light intensity must exceed the configured limiting value continuously, so that heating support is activated. If the light intensity is low, heating support is disabled. The measured room temperature is applied to the ``rTemperature`` input. The ``rSetpointHeating`` defines the threshold of the room temperature at which a position command is transmitted to the sunshade for heating support. The ``rHeatingValve`` input is assigned the percentage opening of the heating valve. By opening the heating valve, the position command to the sunshade for heating support can be triggered. The ``typConfigParameters`` input contains the configuration parameters for heating support. The ``xHeatingSupport`` output displays the heating support activity. The ``typAutomaticSunshade`` output variables contain the position commands for the sunshade actuator. The ``tDeactiveTime`` output displays the elapsed time after deactivation of the heating support. If the ``tDeactiveTime`` value reaches the parametrable time „typConfigHeatingSupport.tDelayRestartHeating``, the heating support can be reactivated. .. note:: The set position values must be in the range of 0 – 100%. Otherwise, the sunshade actuator ignores the command. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+--------------------------+ |

### FbSunshadeCoolingSupport
Function block is used to support cooling by the sunshade. Solar thermal energy is prevented specifically in unoccupied rooms to reduce the energy expended.

**Description:**
Cooling support is activated by a high room temperature or open cooling valve. The cooling support keeps permanently inactive for a parametrable time after its deactivation. The ``xPresence`` input is connected to the presence detection. If presence is detected, cooling support is disabled. A change in the presence detection leads to undelayed switching behavior. The measured intensity of the natural light is applied to the ``rIlluminance`` input. The light intensity must exceed the configured limiting value continuously, so that cooling support is activated. If the light intensity is low, cooling support is disabled. The measured room temperature is applied to the ``rTemperature`` input. The ``rSetpointCooling`` defines the threshold of the room temperature at which a position command is transmitted to the sunshade for cooling support. The ``rCoolingValve`` input is assigned the percentage opening of the cooling valve. By opening the cooling valve, the position command to the sunshade for cooling support can be triggered. The ``typConfigParameters`` input contains the configuration parameters for cooling support. The ``xCoolingSupport`` output displays the cooling support activity. The ``typAutomaticSunshade`` output variables contain the position commands for the sunshade actuator. The ``tDeactiveTime`` output displays the elapsed time after deactivation of the cooling support. If the ``tDeactiveTime`` value reaches the parametrable time „typConfigCoolingSupport.tDelayRestartCooling``, the cooling support can be reactivated. ..Note:: The set position values must be in the range of 0 – 100%. Otherwise, the sunshade actuator ignores the command. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+--------------------------+ |

### FbWindAlarm
The ``FbWindAlarm`` function block is used for weather protection by external sunshades against damage caused by wind.

**Description:**
The measured wind velocity is connected to the ``rWindVelocity`` input. The ``typConfigParameters`` input contains the configuration parameters for the wind alarm. The ``xWindAlarm`` switches on in the event of strong wind or a storm. If the limiting value is not reached, the ``tWindThresholdTime`` switch-off delay starts. Once the switch-off delay has elapsed, the ``xWindAlarm`` output is reset. The ``xError`` output signals a time-out of the wind sensor or incorrect parameterization of the function block thresholds.

### FbFrostAlarm
The ``FbFrostAlarm`` function block is used for weather protection by external sunshades against damage caused icing.

**Description:**
The sensor values received are connected to the ``xRain`` input for precipitation detection and ``rTemperature`` input for outside temperature. The ``typConfigParameters`` input contains the configuration parameters for the frost alarm. The ``xFrostAlarm`` output switches on when it falls below the frost temperature and precipitation is detected. When the deicing temperature is reached, the deicing time starts, which is displayed at the ``tDeiceTime`` output. Once the deicing time has elapsed, the ``xFrostAlarm`` output is reset. The ``xError`` output signals incorrect parameterization of the function block thresholds.

### FbSunshadeActuator
The ``FbSunshadeActuator`` function block is used to control conventional sunshade motors.

**Description:**
The sunshade is controlled based on depending on priority. Commands of higher priority override commands of lower priority. For commands of the same priority, the last command made is executed. The priorities listed in descending order are: - 1 – Safety (``xSafety``) - 4 – Maintenance (``typMaintenanceSunshade``, ``xLockPosition``) - 5 – Manual (``xUp`` / ``xDown``, ``typSetPosition``) - 6 – Automatic (``typAutomaticSunshade``) The sunshade is controlled manually be two button inputs ``xUp`` and ``xDown``. An extended button press on one of these inputs is causes the sunshade to move to the upper or lower position. A short button press triggers a STOP command or a command to adjust the slats. The safety position (upper end position) of the sunshade (e.g. on a wind alarm) can be controlled via the ``xSafety`` input. When the sunshade has been moved to the safety position, the sunshade cannot be manually controlled by commands of lower priority until the ``xSafety`` input is set to FALSE. The ``xLockPosition`` input can be used to interlock the sunshade. Motion commands are not canceled. Only the ``xSafety`` input can override the lock. If there is a continuous signal TRUE at ``typMaintenanceSunshade.xMove`` input, the sunshade moves to the position specified at the ``typMaintenanceSunshade`` input and is then locked. This enables the sunshade to be moved to a defined cleaning or maintenance position, for example. A rising edge at the ``typSetSunshade.xMove`` variable initiates a manual motion command to the position specified at the ``typSetSunshade`` input. The ``typAutomaticSunshade`` input is used to move the sunshade to the automatic sunshade position (automatic sunshade function). As long as the ``xAutomaticPosition`` input signal is TRUE, the value changes from the automatic sunshade function input are updated. The automatic sunshade function can be overridden. That means that commands are not evaluated via the ``typAutomaticSunshade`` input. The automatic sunshade function is overridden for the configured time ``typConfigSunshade.tTimeManualOverride`` if: - A command was initiated via one of the ``xUp`` or ``xDown`` inputs. - A position was approached via the ``xSetSunshade`` input. - The ``xSetManualOverride`` input with signal TRUE is connected. It should be noted that the override time only elapses if the ``xSetManualOverride`` is switched to FALSE again. Thus, the automatic sunshade function can be overridden longer than the time set. The reset of the override commands the sunshade to move to the position specified by the sunshade automatic. The automatic sunshade function can be reset before the override time ``typConfigSunshade.tTimeManualOverride`` has elapsed. A TRUE signal at the ``xSafety``, „xLockPosition``, ``typMaintenanceSunshade.xMove`` or ``xResetManualOverride`` input can trigger a reset. After resetting the override, the sunshade moves to the last position specified by the automatic sunshade function. If there was never an automatic sunshade command, the sunshade moves up. The sunshade moves up if there is no previous automatic sunshade command and the parameter ``typConfigSunshade.xAutoMoveUp`` is set TRUE. The ``xManualOverride`` output signals that the automatic sunshade function is overridden by manual commands. The output remains on TRUE for the manual override time. The ``xMoveUp`` and ``xMoveDown`` output signals the current direction of motion. The outputs can be connected to the motor control. The ``bPriority`` output signals the active priority. The coding is as described above. See also typConfigParameters (:ref:`typConfigSunshade`), it contains all parameter values for the function block. See also typSunshadePosition (:ref:`typSunshadePosition`), it includes the current positions of the sunshade. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+------------------------+ |

### FbMacroTwilightControl
The ``FbMacroTwilightControl`` function block switchs the lighting on depending on the outdoor light intensity. With low outdoor lighting the lighting is switched on. Conversely, the lighting is switched off when outdoor lighting is adequate.

**Description:**
The ``xEnable`` input can be used to disable twilight control. The information can be come from the time program or a command from the building management system. The current measured intensity of the natural light is applied to the ``rIlluminance`` input. The ``xActuator`` output indicates the digital switching state. If a percentage dimming value is greater than 0, ``xActuator`` switches to TRUE. The ``rActuator`` output indicates the percentage dimming value. The value is specified by the ``typConfigTwilightControl.rDimValueAtTwilight`` switch-on value. When switched off, the ``typConfigTwilightControl.rSunriseLimit`` switching value is passed. The ``wActuator`` output indicates the dimming value as a signal in a range of 0 to 32767. For example, this output can be used for an analog output module. See also typConfigParameters (:ref:`typConfigTwilightControl`), it contains all parameter values for the function block. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+------------------------+ |

### FbMacroStairwellLightControl
The ``FbMacroStairwellLightControl`` function block maps the function of a stairwell light control. A prewarning can be triggered before switching off.

**Description:**
The lighting is switched on by a positive edge at the ``xButton`` input for a configurable period. Another positive edge at ``xButton`` restarts the elapsed time. The ``xActuator`` output indicates the digital switching state. If a percentage switching value is greater than 0, ``xActuator`` switches to TRUE. The ``rActuator`` output indicates the percentage dimming value. The value is specified by the ``typConfigStairwellLightControl.rSwitchOnValue`` switch-on value. When switched off, the dimming value is 0. When the switch-off prewarning is used, the ``typConfigStairwellLightControl`` switching value is briefly output at the configured time. The ``wActuator`` output indicates the switching value as a signal in a range of 0 to 32767. For example, this output can be used for an analog output module. See also typConfigParameters (:ref:`typConfigStairwellLightControl`), it contains all parameter values for the function block.

### FbMacroLightControl
The ``FbMacroLightControl`` function block applicable to switching ON/OFF switchable and dimmable lighting systems.

**Description:**
The ``xSwitch`` input determines the switching behavior of the function block. A positive edge switches on, and negative edge switches off. The ``xActuator`` output indicates the digital switching state. If a percentage dimming value is greater than 0, ``xActuator`` switches to TRUE. The ``rActuator`` output indicates the percentage dimming value. The value is specified by the ``typConfigLightControl.rSwitchOnValue`` switch-on value. In the OFF state, the dimming value is 0. The ``wActuator`` output indicates the dimming value as a signal in a range of 0 to 32767. For example, this output can be used for an analog output module. See also typConfigParameters (:ref:`typConfigLightControl`), it contains all parameter values for the function block. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+------------------------+ |

### FbLatchingRelay
The ``FbLatchingRelay`` function block maps the function of a latching relay. The switching function corresponds to a toggle flip-flop.

**Description:**
The function block reacts to rising switching signals at the ``xButton`` input. With every positive switching signal at the ``xButton`` input, the latched relay switches its status value at the ``xActuator`` output. The ``xCentralOn`` and ``xCentralOff`` inputs serve to connect central ON/OFF commands for the ``xActuator`` output. The ``xCentralOn`` input sends an ON command in the case of a rising edge. The ``xCentralOff`` input sends an OFF command in the case of a rising edge. The Function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813: +-------------------------+------------------------+ |

## Data Types

### typBrightnessMeasurement
Structure type.

The following section describes how the brightness measurement of a light sensor is calibrated. It is used to adjust the measured light intensity compared to the light intensity at the workstation. .. figure:: ../../images/BrightnessMeasurement_Example.png :align: center :alt: Measured Light Intensity compared to the Light Intensity at the Workstation

### typSlatPosition
Structure type.

Contains parameters for the slat tracking positions.

### typConfigSunshade
Structure type.

Parameters for sunshade actuator.

### typWindAssessment
Structure type.

Contains parameters for the wind assessment. The measured wind strength is multiplied by the factor of the wind sector and the calculated wind strength further processed.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbEvaluateSingleButton_1: FbEvaluateSingleButton_1;
END_VAR

// Basic function block usage
fbFbEvaluateSingleButton_1(
    // Configure inputs as needed
);

// Check status
IF fbFbEvaluateSingleButton_1.xValid THEN
    // Operation successful
END_IF

IF fbFbEvaluateSingleButton_1.xError THEN
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

