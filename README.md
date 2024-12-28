# Traffic Light  System

This project uses **Infrared (IR) Sensors** and **Traffic Lights** to simulate a parking system. The system uses IR sensors to detect the presence of vehicles and controls traffic lights accordingly. Additionally, a **buzzer** is triggered if the vehicle exceeds a certain threshold.

### Features:
- **Traffic light system** with 4 sets of Red, Yellow, and Green LEDs.
- **IR Sensors** to detect vehicles.
- **Buzzer** to signal a vehicle presence or an alarm.
- Simulates the basic operation of a parking system with vehicle detection and signal management.

### Components Used:
- **4 IR Sensors** for vehicle detection.
- **LEDs** for traffic lights:
  - Red LED (stop signal).
  - Yellow LED (caution signal).
  - Green LED (go signal).
- **Buzzer** for alerts.
- **Arduino Board** (e.g., Arduino Uno).

### Circuit Connections:
- **IR Sensors** (IR1, IR2, IR3, IR4) connected to digital pins (13, 0, 1, 2 respectively).
- **Traffic Lights**:
  - **R1, Y1, G1** for the first set of traffic lights.
  - **R2, Y2, G2** for the second set of traffic lights.
  - **R3, Y3, G3** for the third set of traffic lights.
  - **R4, Y4, G4** for the fourth set of traffic lights.
- **Buzzer** connected to pin 10.

### Code Overview:
The code controls a basic traffic light system and responds to the input from IR sensors. Based on the sensor values:
1. **IR Sensors** detect vehicle presence:
   - When all sensors detect vehicles, the traffic lights cycle through the green and red signals.
2. **Traffic Light Control**:
   - Each sensor corresponds to a specific traffic light, controlling the sequence of Green, Yellow, and Red lights.
3. **Buzzer**: 
   - When a certain threshold value is reached, the buzzer sounds as an alert.
4. **Sensor Monitoring**:
   - The code continuously reads from the IR sensors to check vehicle presence and controls the traffic lights accordingly.

### Setup Instructions:
1. **Wiring**: 
   - Connect the IR sensors and LEDs to the specified pins on the Arduino.
   - Ensure the buzzer is connected to pin 10.
2. **Install Arduino IDE**: 
   - Download and install the **Arduino IDE** if not already installed.
3. **Upload the Code**: 
   - Upload the provided code to the Arduino board.
4. **Monitor the System**:
   - Open the Serial Monitor in the Arduino IDE to view the status of the IR sensors and traffic light behavior.

### Functionality:
- The system reads the input from the IR sensors to check if a vehicle is present at each parking slot.
- When all sensors are triggered (vehicle detected), the traffic lights cycle through their normal sequence.
- If a sensor value exceeds a threshold (vehicle is detected), the **buzzer** will activate for 5 seconds to alert the user.
- Each IR sensor corresponds to one of the four traffic light sets. If a sensor is triggered, the corresponding set of lights will switch to green.

### Traffic Light Sequence:
1. **Green Light**: Allows vehicles to pass.
2. **Yellow Light**: Caution signal before turning red.
3. **Red Light**: Indicates stop for vehicles.
4. **Buzzer**: Sounds when vehicle detection exceeds a set threshold.

### Code Flow:
1. **Defining Pin Modes**: 
   - The LEDs, IR sensors, and buzzer are initialized in the `setup()` function.
2. **IR Sensor Readings**:
   - The `loop()` function continuously reads values from the IR sensors to determine the vehicle presence.
3. **Traffic Light Control**: 
   - Based on sensor input, the traffic light cycle for each parking slot is controlled using the `def()`, `IR1G()`, `IR1R()`, etc., functions.
4. **Buzzer Activation**: 
   - If the sensor readings exceed the defined threshold, the buzzer sounds for a defined period.

### Notes:
- Adjust the threshold values for the sensors as needed.
- This system is a simulation and can be used for various parking management systems or as a traffic light simulator.

### License:
This project is open-source and available under the [MIT License](LICENSE).
