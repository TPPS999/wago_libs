# WagoAppWeatherForecast v1.2.0.3

## Overview
WAGO PLC library providing WagoAppWeatherForecast functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbGetWorldWeatherOnline
This function block obtains current weather condition and weather forecasts (5 days or 6h interval (8 elements of 6 hours)) from worldweatheronline.com

**Description:**
In order to use the function block the API key and geographical position of your location is needed: - Register at https://developer.worldweatheronline.com/auth/register to receive personal API key. Copy your personal API key to input parameter ``sApiKey`` - Calculate geographical position data. The website www.mygeoposition.com allows to calculate the positions easily. Copy the calculated data to input parameter ``rLatitude`` and ``rLongitude`` Preconditions: - Make sure Gateway and DNS-Server are properly set in your controller configuration (Check via Ethernet Settings or Web-Based Management) - Setup API key and geographical position (sApiKey, rLatitude, rLongitude) - Increase the size of receive buffer by parameter ``MAX_WEATHER_RESPONSE``:

### FbGetOpenWeatherMap
This function block obtains current weather condition and weather forecasts from openweathermap.org

**Description:**
Forecast mode: | 1. free API version | If a free API version (current weather data or 5 day/3 hour forecast) is used, only the method FORECAST_DETAILED is supported. | Up to forty values can be read out. | The exact number is defined via the variable in the preset input field at the input “aForecast.” | In the following example, eight values should be read out: | aForecastOWM: ARRAY [0..7] OF typForecast_OpenWeatherMap; | 2. fee-based API version | If a fee-based version is used, the variant “16 day / daily forecast” can be used in addition. | To do so, use the method FORECAST_DAILY at the input “eForecastMode.” | Up to sixteen days can be read out. The exact number is determined via the variable “aForecast.” In order to use the function block the API key and geographical position of your location is needed: | - Register at http://openweathermap.org/appid to receive personal API key. | Copy your personal API key to input parameter ``sApiKey`` | - Calculate geographical position data. The website www.mygeoposition.com allows to calculate the positions easily. | Copy the calculated data to input parameter ``rLatitude`` and ``rLongitude`` Preconditions: | - Make sure Gateway and DNS-Server are properly set in your controller configuration (Check via Ethernet Settings or Web-Based Management) | - Setup API key and geographical position (sApiKey, rLatitude, rLongitude) | - Increase the size of receive buffer by parameter ``MAX_WEATHER_RESPONSE``:

### FbGetWeatherstack
This function block obtains current weather information from api.weatherstack.com/current

**Description:**
In order to use the function block an API key is needed: Supported API version: http://api.weatherstack.com/current and http://api.weatherstack.com/forecast?access_key

## Data Types

### eStatus
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbGetWorldWeatherOnline: FbGetWorldWeatherOnline;
END_VAR

// Basic function block usage
fbFbGetWorldWeatherOnline(
    // Configure inputs as needed
);

// Check status
IF fbFbGetWorldWeatherOnline.xValid THEN
    // Operation successful
END_IF

IF fbFbGetWorldWeatherOnline.xError THEN
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

