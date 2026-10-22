# CodeAlpha IoT Task 2
## Temperature-Based LED Control Using Arduino and TMP36

### 1. Project Overview
This project demonstrates a temperature-based LED control system using an Arduino Uno and a TMP36 temperature sensor.

The system monitors temperature and automatically controls an LED according to a predefined temperature threshold. The project is simulated using Tinkercad Circuits.

### 2. Objective
To monitor temperature and automatically switch an LED ON when the temperature reaches or exceeds 30°C and OFF when it falls below 30°C.

### 3. Components Used
- Arduino Uno
- TMP36 Temperature Sensor
- LED
- 220-ohm Resistor
- Tinkercad Circuits

### 4. Working Principle
1. The TMP36 sensor measures the temperature.
2. The sensor provides an analog voltage to Arduino pin A0.
3. Arduino reads the analog signal and converts it into voltage.
4. The voltage is converted into temperature in degrees Celsius.
5. The temperature is displayed in the Serial Monitor.
6. The LED turns ON at or above 30°C.
7. The LED turns OFF below 30°C.

### 5. Code Explanation

**Pin Configuration:**
- `sensorPin = A0`: Reads the temperature sensor output.
- `ledPin = 8`: Controls the LED.
- `threshold = 30.0`: Sets the temperature threshold to 30°C.

**Setup Function:**
The `setup()` function configures the LED pin as an output and initializes serial communication at 9600 baud.

**Temperature Reading:**
The `analogRead()` function reads the sensor's analog output. Arduino converts this reading into a value between 0 and 1023.

**Voltage Conversion:**
The analog reading is converted into voltage using a 5 V reference.

**Temperature Calculation:**
The TMP36 sensor voltage is converted into temperature using:

Temperature (°C) = (Voltage - 0.5) × 100

**Serial Monitor:**
The `Serial.print()` and `Serial.println()` functions display the measured temperature in degrees Celsius.

**LED Control:**
The `if-else` condition compares the measured temperature with the 30°C threshold. The LED turns ON when the temperature is at least 30°C and OFF when it is below 30°C.

**Delay:**
The `delay(1000)` function pauses the program for one second before the next measurement.

### 6. Detailed Program Flow
1. Initialize the LED and serial communication.
2. Read the analog value from the TMP36 sensor.
3. Convert the analog value into voltage.
4. Calculate the temperature.
5. Display the temperature in the Serial Monitor.
6. Compare the temperature with the threshold.
7. Control the LED based on the comparison.
8. Repeat the process continuously.

### 7. Simulation Results
The circuit is simulated using Tinkercad Circuits.

- Below 30°C: LED OFF.
- At or above 30°C: LED ON.
- Temperature readings appear in the Serial Monitor.

### 8. Conclusion
This project demonstrates the use of temperature sensors, analog signal processing, serial communication, and conditional programming to achieve automatic temperature-based control.

### 9. Tools Used
- Arduino Uno
- TMP36 Temperature Sensor
- Tinkercad Circuits
- Arduino C/C++ Programming
