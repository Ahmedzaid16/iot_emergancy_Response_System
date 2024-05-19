## Emergency Response System with IoT

### Overview
Our Emergency Response System is designed to monitor and respond to environmental hazards using multiple sensors and a control board. It provides real-time monitoring and alarms for fire, gas, and temperature changes, as well as motion detection.

### System Components
- **DHT-11 Temperature Sensor**
- **MQ-5 Gas Sensor**
- **IR Obstacle Avoidance Sensor**
- **Flame Sensor**
- **Buzzer and LED for Alarms**
- **NodeMcu ESP8266 Control Board**

### Tools & Technologies
- **Flutter**: Mobile application framework.
- **Mosquitto**: MQTT broker for communication.
- **Arduino IDE**: Development environment for NodeMcu.
- **Firebase**: Backend database for data storage and analysis.

### Key Features
1. **Fire Monitoring**: Detects fire hazards in real-time.
2. **Gas Monitoring**: Monitors gas levels continuously.
3. **Temperature Monitoring**: Tracks temperature changes accurately.
4. **Lock Function**: Activates the buzzer when motion is detected by the IR sensor.

### Algorithm Summary

1. **Initialize System Components**:
   - Set up sensors (DHT-11, MQ-5, IR, Flame) and actuators (buzzer, LED).
   - Configure NodeMcu ESP8266 for sensor data collection and communication.

2. **Connect to WiFi**:
   - Connect to the specified WiFi network using the provided SSID and password.

3. **Set Up MQTT Client**:
   - Connect to the MQTT broker.
   - Subscribe to the motion topic to receive lock commands.

4. **Sensor Data Collection and Publishing**:
   - Read data from the sensors (DHT-11, MQ-5, IR, Flame).
   - Publish sensor data to the MQTT broker.
   - Push sensor data to Firebase for storage and analysis.

5. **Handle Incoming MQTT Messages**:
   - Listen for lock commands on the motion topic.
   - Activate or deactivate the buzzer based on the lock command and motion detection.

6. **Real-Time Monitoring (Flutter App)**:
   - Display real-time values for temperature, gas, and fire sensors.
   - Send lock commands to the NodeMcu to control the buzzer.

