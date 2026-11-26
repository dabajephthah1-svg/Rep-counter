Rep-counter
 Smart RepCounter – IoT Exercise Repetition Counter

An IoT-based Smart RepCounter that uses an **ESP32-S3 microcontroller and MPU6050 motion sensor** to detect physical movements, count exercise repetitions and display workout information through a web-based dashboard.

1. Project Overview

The Smart RepCounter is designed to make exercise tracking easier by automatically detecting repetitive movements using motion-sensing technology.

The MPU6050 measures acceleration and angular velocity during exercise. The ESP32-S3 processes the sensor readings, detects movement cycles and sends workout data over Wi-Fi to a browser-based application.

The dashboard allows users to monitor their repetitions and workout progress in real time.

 2. Project Objectives

- Automatically count exercise repetitions using motion detection.
- Monitor physical movement using an MPU6050 sensor.
- Transfer sensor data wirelessly using ESP32 Wi-Fi.
- Display workout information through a web application.
- Support different exercises and sensor mounting positions.
- Provide a simple and user-friendly workout monitoring interface.

 3. Hardware Components

| Component | Purpose |
|---|---|
| ESP32-S3 DevKitC-1 | Main microcontroller and Wi-Fi communication |
| MPU6050 | Measures acceleration and angular velocity |
| USB cable | Programming and power supply |
| Jumper wires | Hardware connections |

4. Hardware Connections
MPU6050 to ESP32-S3

| MPU6050 Pin | ESP32-S3 Pin |
|---|---|
| VCC | 3.3V |
| GND | GND |
| SDA | GPIO 8 |
| SCL | GPIO 9 |
| AD0 | GND |

The MPU6050 communicates with the ESP32-S3 through the I2C communication protocol.

Its default I2C address is `0x68`.

5. Software and Technologies

- Arduino IDE: ESP32-S3 firmware development.
- C++: Sensor reading and repetition detection.
- HTML: Web dashboard structure.
- CSS:** Dashboard styling and responsive layout.
- JavaScript:** Browser interactions and communication with the ESP32.
- Wi-Fi:** Wireless data transmission.
- HTTP API:** Communication between the ESP32 and browser application.

 6. System Architecture

```text
       MPU6050 Sensor
              |
              | I2C
              |
          ESP32-S3
              |
      Motion Processing
              |
      Repetition Counting
              |
          Wi-Fi
              |
        HTTP API
              |
      Web Dashboard
              |
      Live Workout Data
```

 7. Main Features

- Automatic exercise repetition counting.
- Real-time workout monitoring.
- Wireless communication through Wi-Fi.
- Exercise selection.
- Sensor position selection (Arm or Stomach).
- Workout start, stop and reset controls.
- Workout duration tracking.
- Motion activity monitoring.
- Browser-based dashboard.

8. Supported Exercises

The application is designed to support:

- Push-ups
- Sit-ups
- Squats
- Bicep curls
- Shoulder raises
- Other repetitive exercises

The movement detection algorithm may require calibration and exercise-specific adjustments for reliable counting.
 9. Installation and Setup

 Step 1: Connect the Hardware

Connect the MPU6050 to the ESP32-S3 using the wiring table above.

Step 2: Configure Arduino IDE

1. Install Arduino IDE.
2. Install the ESP32 board package.
3. Select the appropriate ESP32-S3 board.
4. Select the correct COM port.
 Step 3: Configure Wi-Fi

Open the ESP32 firmware and update:

```cpp
const char* WIFI_SSID = "YOUR_WIFI_NAME";
const char* WIFI_PASSWORD = "YOUR_WIFI_PASSWORD";
```

Use a compatible 2.4 GHz Wi-Fi network.

Step 4: Upload Firmware

Upload the ESP32 firmware using Arduino IDE.

Open Serial Monitor at 115200 baud and check the Wi-Fi connection and IP address.

Step 5: Run the Web Application

1. Open the project folder in Visual Studio Code.
2. Open `index.html` using Live Server.
3. Enter the ESP32 IP address in the dashboard.
4. Click Connect.
5. Select an exercise and sensor position.
6. Start your workout.

The computer and ESP32 must be connected to the same local network. The ESP32 firmware must expose the HTTP endpoints expected by the dashboard.

10. Testing and Validation

The project can be tested in stages:

1. Verify MPU6050 detection using an I2C scanner.
2. Confirm that the sensor responds at address `0x68`.
3. Test ESP32 Wi-Fi connectivity.
4. Verify the ESP32 HTTP API.
5. Connect the browser dashboard.
6. Perform controlled exercise movements and compare detected repetitions with manually counted repetitions.

 11. Future Improvements

- Improve repetition detection accuracy using exercise-specific algorithms.
- Add workout history and performance statistics.
- Integrate user profiles.
- Add calorie estimation.
- Introduce cloud-based workout storage.
- Support multiple motion sensors.
- Improve mobile responsiveness.
- Add secure communication between the browser and ESP32.

12. Project Status

Development in progress.

The MPU6050 has been detected successfully through I2C. Wi-Fi connectivity and browser-to-device communication are being tested and integrated.
13. Author

Leslie Foncham Mbunda**
Daba Jephthan Akam
IT / IoT Student  
Savonia University of Applied Sciences

14. License

This project is developed for educational and learning purposes. A license can be added when the project is ready for public distribution.

---

Smart RepCounter – Making Exercise Tracking Smarter Through IoT
We use AI for coding assistance
