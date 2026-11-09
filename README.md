# Basira — AI-Powered Assistive Smart Glasses

<p align="center">
  **An Intelligent Wearable Assistive System for Enhanced Mobility, Awareness, and Safety**
</p>

Basira is a graduation project developed by a Computer Engineering team at Taif University. It explores the integration of artificial intelligence, computer vision, embedded systems, IoT, and mobile application technologies into a wearable assistive solution designed to support people with visual impairments.

The system combines smart glasses, embedded sensing modules, AI-powered processing, and a companion mobile application to help users understand their surroundings, recognize familiar people, and access safety-related monitoring features.

---

## Project Overview

Navigating unfamiliar environments and recognizing familiar people can present significant challenges for individuals with visual impairments.

Basira addresses these challenges through an integrated assistive platform that combines:

- **Computer Vision:** Object detection and facial recognition.
- **Smart Sensing:** Distance and motion sensing for obstacle awareness.
- **Audio and Haptic Feedback:** Voice guidance and vibration-based alerts.
- **Mobile Application:** User management, face registration, and location monitoring.
- **Connected Systems:** Communication between wearable hardware and mobile software.

## Key Features

### 1. AI-Based Object Detection
- Analyzes visual input to identify objects in the surrounding environment.
- Uses trained AI models to detect and classify objects.
- Provides audio feedback to communicate detected information.

### 2. Facial Recognition
- Identifies familiar individuals using registered facial data.
- Supports face registration and management through the companion application.
- Uses a Raspberry Pi-based facial recognition service.

### 3. Obstacle Detection
- Uses distance sensing to measure the proximity of nearby obstacles.
- Adjusts vibration intensity according to measured distance.
- Combines sensor readings with visual information to improve environmental awareness.

### 4. Audio and Haptic Feedback
- Delivers spoken information through audio output.
- Provides vibration alerts to indicate nearby obstacles.
- Offers complementary feedback through different output methods.

### 5. Companion Mobile Application
- Supports user and family relationship management.
- Provides facial registration and monitoring interfaces.
- Displays user location through an interactive map.
- Supports communication with the wearable system and its services.

### 6. Safety and Location Monitoring
- Supports location monitoring for caregivers and family members.
- Includes emergency-related notification capabilities described in the project design.
- Provides access to sensor information through connected services.

---

## System Architecture

Basira consists of three main integrated components:

| Component | Responsibility |
|---|---|
| Smart Glasses | Capturing visual information and delivering user feedback |
| Embedded Processing and Sensors | Object processing, distance measurement, motion sensing, and vibration control |
| Mobile Application | User management, face registration, location monitoring, and system interaction |

The components communicate through connected services and network interfaces to provide an integrated assistive experience.

---

## Hardware Components

The project report documents the use of the following hardware components:

- Raspberry Pi 4
- ESP32 Microcontroller
- Camera Modules
- VL53L0X Time-of-Flight Distance Sensor
- MPU6050 Accelerometer and Gyroscope
- Vibration Motor
- Audio Amplifier and Speakers
- Li-Po Battery and Power Management Module

## Technologies and Tools

**Artificial Intelligence & Computer Vision**
- Python
- OpenCV
- Face Recognition
- AI-Based Object Detection

**Embedded Systems & IoT**
- ESP32
- Sensor Integration
- Wi-Fi Communication
- HTTP and JSON-Based Data Exchange

**Backend & Database**
- Flask
- MySQL

**Mobile Development**
- Flutter

---

## Implementation Highlights

The project implementation includes several interconnected modules:

- A Raspberry Pi-based object detection and facial recognition system.
- A facial recognition service using camera input, OpenCV, Flask, and MySQL.
- An ESP32-based sensing module integrating distance and motion sensors with vibration feedback.
- An HTTP server exposing sensor readings through JSON endpoints.
- A Flutter mobile application supporting user management, face registration, and location monitoring.

The object detection model was trained and evaluated using separate training, testing, and verification datasets. The project report documents precision and recall results above 0.80 across the evaluated classes.

---

## Project Objectives

Basira was developed with the following objectives:

- Improve environmental awareness for people with visual impairments.
- Support safer movement through obstacle detection and proximity sensing.
- Facilitate recognition of familiar individuals.
- Provide accessible audio and haptic feedback.
- Enable caregivers to access location and monitoring features.
- Demonstrate the practical integration of AI, embedded systems, and mobile technologies.

---

## Project Scope and Limitations

Basira is an academic graduation project and an assistive technology prototype. Its capabilities and performance should be understood within the scope of the implementation and evaluation documented by the project team.

It is not a certified medical or safety device and should not be considered a replacement for established mobility aids or appropriate supervision.

---

## Future Work

Potential areas for further development include:

- Optimizing AI models for real-time edge processing.
- Improving detection performance in challenging lighting conditions.
- Enhancing multi-sensor fusion.
- Reducing power consumption and improving battery efficiency.
- Improving wearable design, comfort, and usability.
- Expanding system testing in real-world environments.

---

## Academic Project

**Project Name:** Basira — AI-Powered Assistive Smart Glasses  
**Project Type:** Computer Engineering Graduation Project  
**Institution:** Taif University  
**Project Completion:** 2026

Developed collaboratively by a Computer Engineering graduation project team.

---

<p align="center">
  **Basira — Technology That Helps People See Beyond Sight.**
</p>
