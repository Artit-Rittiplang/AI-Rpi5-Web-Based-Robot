## 🌟 Key Features

### 🎮 Low-Latency Control
This project utilizes a custom **Async/Await JavaScript loop** to handle motor commands. Unlike standard timer-based approaches, this ensures that:
- **No Command Buffering:** The browser synchronizes with the robot's processing speed.
- **Instant Response:** The robot stops the millisecond the user releases the control.

### 🛑 Safety Mechanisms
Safety is a priority in this control system:
- **Fail-Safe Stopping:** Uses a "Double-Stop" redundancy method (sends stop command twice) to handle potential packet loss.
- **Touch Guard:** Implements `ontouchcancel` events to prevent "runaway" scenarios if a finger slips off the controls on mobile devices.

### 📱 Interface
- **3-Axis Servo Control:** Sliders for controlling 3 separate servos.
- **Mobile Optimized:** CSS prevents zooming/selecting during rapid tapping.
- **Live Telemetry:** AJAX fetch calls provide real-time updates for encoders and sensor data.

step1: how to connect ESP32 wiring before upload "ros2_bridge_esp32" code
<img width="1026" height="620" alt="image" src="https://github.com/user-attachments/assets/6e16b48b-c210-473b-b5a7-f2717535e943" />
step2: Rpi5 is a web-server to control ESP32
<img width="1889" height="859" alt="image" src="https://github.com/user-attachments/assets/42a3c3e1-1f7a-4693-abb5-d2c181710319" />
