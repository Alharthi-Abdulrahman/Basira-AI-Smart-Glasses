# Basira — Hardware Components

This document describes the main hardware components specified in the Basira project report and explains their roles within the assistive smart-glasses system.

## 1. Main Processing Unit

### Raspberry Pi 4
The Raspberry Pi 4 serves as the primary processing unit for the smart-glasses system.

**Main responsibilities:**
- Processing camera input for computer vision tasks.
- Running the YOLO-based object detection system.
- Supporting facial recognition through OpenCV and the Face Recognition library.
- Running the Flask service for facial registration and video streaming.
- Managing the local facial recognition database.

### ESP32 Microcontroller (ESP-WROOM-32)
The ESP32 handles sensor-related operations and provides wireless communication capabilities.

**Main responsibilities:**
- Reading distance measurements from the Time-of-Flight (ToF) sensor.
- Collecting motion data from the MPU-6050 IMU.
- Controlling the vibration motor for obstacle alerts.
- Providing Wi-Fi connectivity and an HTTP server for sensor data access.
- Exposing sensor readings through a JSON endpoint.

## 2. Camera and Vision Hardware

### Raspberry Pi Camera Module 2
The Raspberry Pi camera provides visual input to the processing unit.

**Main responsibilities:**
- Capturing images and video frames.
- Supplying visual data for object detection.
- Supporting facial recognition and face registration.

## 3. Sensors and Feedback Components

### Time-of-Flight (ToF) Distance Sensor
The ToF sensor measures the distance between the device and nearby objects.

**Main responsibilities:**
- Measuring the distance to potential obstacles.
- Supporting obstacle proximity detection.
- Providing distance readings used by the ESP32 to determine vibration feedback intensity.

**Model clarification:** The hardware specification section identifies the sensor as TOF10120, while the ESP32 implementation section references the VL53L0X. The exact model used in the final hardware configuration requires confirmation.

### MPU-6050 Inertial Measurement Unit (IMU)
The MPU-6050 combines a three-axis accelerometer and a three-axis gyroscope.

**Main responsibilities:**
- Measuring acceleration and rotational movement.
- Providing motion and orientation-related data.
- Supporting movement monitoring through the ESP32.

### Coin Vibration Motor (ERM)
The coin-type vibration motor provides physical feedback to the user.

**Main responsibilities:**
- Delivering vibration alerts when obstacles are detected.
- Adjusting feedback intensity according to the measured distance.
- Providing a non-visual alert mechanism.

## 4. Audio Components

### PAM8403 Audio Amplifier
The PAM8403 is a compact audio amplifier specified in the project hardware documentation.

**Main responsibility:**
- Amplifying audio signals to drive the speaker.

### Mini 3W Speaker
The speaker provides audible information and alerts.

**Main responsibilities:**
- Delivering audio guidance.
- Providing audible notifications to support environmental awareness.

## 5. Power Management Components

### Lithium-Polymer (Li-Po) Battery
The Li-Po battery is specified as the system's rechargeable power source.

**Main responsibilities:**
- Supplying electrical power to the wearable device.
- Supporting portable operation.

### Waveshare UPS Module C
The Waveshare UPS Module C is specified as part of the power management design.

**Main responsibilities:**
- Providing regulated 5V output.
- Supporting battery-powered operation of the Raspberry Pi.
- Providing battery charging and power-management functionality.

## 6. Hardware Integration Overview

The hardware architecture combines processing, sensing, visual input, user feedback, and power management:

| Component | Primary Role |
|---|---|
| Raspberry Pi 4 | Main processing and computer vision |
| ESP32 | Sensor management and wireless communication |
| Raspberry Pi Camera Module 2 | Visual input |
| ToF Sensor | Distance measurement |
| MPU-6050 | Motion sensing |
| Coin Vibration Motor | Haptic feedback |
| PAM8403 Amplifier | Audio amplification |
| Mini 3W Speaker | Audio output |
| Li-Po Battery | Portable power supply |
| Waveshare UPS Module C | Power management |

## 7. Technical Notes

- The Raspberry Pi handles computationally intensive vision and facial recognition tasks.
- The ESP32 handles sensor acquisition, proximity-related feedback, and wireless sensor-data access.
- Audio and vibration feedback provide complementary ways to communicate information to the user.
- The ToF sensor model requires verification because the hardware specification and firmware documentation identify different models.
- Component specifications in this document reflect the project report. They should not be interpreted as independent confirmation that every listed component was integrated and validated in the final physical prototype.

---

**Project:** Basira — AI-Powered Assistive Smart Glasses

**Project Period:** August 2025 – June 2026
