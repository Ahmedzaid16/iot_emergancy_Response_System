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
## Screenshots

<p align="center">
  <img src="https://github.com/Ahmedzaid16/iot_emergancy_Response_System/assets/84353686/9089011d-0899-4d03-ac91-b0a19071b37e" alt="Screenshot 1" width="45%" style="border-bottom: 1px solid black; margin-bottom: 5px;"/>
  <img src="https://github.com/Ahmedzaid16/iot_emergancy_Response_System/assets/84353686/dcfa2272-4100-44d5-a3f7-37e161d634eb" alt="Screenshot 2" width="45%" style="border-bottom: 1px solid black; margin-bottom: 5px;"/>
</p>

<p align="center">
  <img src="https://github.com/Ahmedzaid16/iot_emergancy_Response_System/assets/84353686/5a5dd136-6f6f-4f7d-b2d1-eca55868c606" alt="Screenshot 3" width="45%" style="border-bottom: 1px solid black; margin-bottom: 5px;"/>
  <img src="https://github.com/Ahmedzaid16/iot_emergancy_Response_System/assets/84353686/512af01d-7c3e-48fb-90b7-0b567a07cb81" alt="Screenshot 4" width="45%" style="border-bottom: 1px solid black; margin-bottom: 5px;"/>
</p>

