# Basira — AI-Powered Assistive Smart Glasses

<p align="center">
  <strong>An Intelligent Wearable Assistive System for Enhanced Mobility, Awareness, and Safety</strong>
</p>

<p align="center">
  A Computer Engineering Graduation Project | Taif University | 2026
</p>

<p align="center">
  <img src="assets/images/basira_glasses_front_view.png" alt="Basira Smart Glasses Prototype" width="600">
</p>

---

## Overview

**Basira** is an AI-powered wearable assistive system developed as a Computer Engineering graduation project at Taif University.

The project explores the integration of Artificial Intelligence (AI), Computer Vision, Embedded Systems, and Internet of Things (IoT) technologies into a smart wearable solution designed to support people with visual impairments.

Basira combines camera-based environmental analysis, facial recognition, distance estimation, and haptic feedback with a companion mobile application. The system aims to improve environmental awareness, support safer mobility, facilitate social interaction, and provide additional safety-related features.

## The Problem

People with visual impairments face challenges when navigating unfamiliar environments independently. Recognizing familiar individuals, identifying nearby obstacles, and responding to potential hazards can make everyday movement more difficult.

Existing assistive approaches may not provide an integrated experience that combines environmental awareness, person recognition, and connected safety features.

**Basira explores an integrated wearable approach to address these challenges through AI-powered perception, smart sensing, and mobile connectivity.**

## Key Features

### 1. AI-Based Object Detection

- Analyzes camera input to identify objects in the surrounding environment.
- Uses an AI-based detection model to recognize and classify objects.
- Supports audio guidance to communicate detected information to the user.

### 2. Facial Recognition

- Recognizes familiar individuals using registered facial information.
- Supports facial registration through the companion mobile application.
- Integrates camera input with a Raspberry Pi-based processing system.

### 3. Distance Estimation

- Uses a TOF10120 laser distance sensor to estimate the distance to nearby objects.
- Provides distance-related information to support obstacle awareness.
- Integrates distance sensing with the wearable feedback system.

### 4. Haptic Alerts

- Uses vibration motors to provide tactile notifications.
- Supports obstacle-related alerts through vibration feedback.
- Complements audio guidance with a non-visual feedback method.

### 5. Companion Mobile Application

- Provides interfaces for user interaction and system management.
- Supports facial registration and recognition-related functionality.
- Includes location display and monitoring interfaces.
- Connects the mobile application with the wearable system.

### 6. Safety and Location Features

- Incorporates GPS-based location tracking as part of the system.
- Includes emergency alert functionality in the project design.
- Aims to provide additional awareness and peace of mind for caregivers.

---

## System Architecture

Basira is designed around three interconnected components:

| Component | Main Responsibilities |
|---|---|
| Smart Glasses | Capturing visual information and delivering audio and haptic feedback |
| Embedded Processing & Sensors | AI processing, distance estimation, motion sensing, and hardware control |
| Mobile Application | User interaction, facial registration, location display, and monitoring |

These components work together to provide an integrated assistive system combining wearable hardware, intelligent processing, and mobile connectivity.

### System Architecture Diagram

<p align="center">
  <img src="assets/images/system_architecture_diagram.png" alt="Basira System Architecture" width="850">
</p>

---

## Hardware Components

The project incorporates the following hardware components:

| Component | Purpose |
|---|---|
| Raspberry Pi 4 | Embedded processing platform |
| ESP-WROOM-32 | Microcontroller for embedded sensing and connectivity |
| Raspberry Pi Camera Module 2 | Visual input and image capture |
| TOF10120 Laser Range Sensor | Distance estimation |
| MPU-6050 IMU | Motion and orientation sensing |
| Coin Vibration Motors | Haptic feedback and alerts |

---

## Technologies & Development Tools

### Artificial Intelligence & Computer Vision
- Python
- OpenCV
- AI-Based Object Detection
- Facial Recognition

### Embedded Systems & IoT
- ESP32
- Arduino IDE
- Sensor Integration
- Wi-Fi Communication

### Backend & Data Management
- Flask Framework
- SQLite
- HTTP Communication
- JSON Data Exchange

### Mobile Application Development
- Flutter
- Android Studio

### Design & Development
- Figma
- Visual Studio Code

---

## Prototype & Application

### Smart Glasses Prototype

The wearable prototype integrates embedded hardware, sensing components, and user feedback mechanisms into a smart glasses design.

<p align="center">
  <img src="assets/images/basira_glasses_front_view.png" alt="Basira prototype front view" width="32%">
  <img src="assets/images/basira_glasses_side_view.png" alt="Basira prototype side view" width="32%">
  <img src="assets/images/basira_glasses_top_view.png" alt="Basira prototype top view" width="32%">
</p>

### Mobile Application Interfaces

The companion application provides interfaces for interacting with the Basira system.

<p align="center">
  <img src="assets/images/mobile_app_dashboard_screen.png" alt="Basira mobile application dashboard" width="30%">
  <img src="assets/images/mobile_app_face_screen.png" alt="Basira facial recognition interface" width="30%">
  <img src="assets/images/mobile_app_map_screen.png" alt="Basira location map interface" width="30%">
</p>

---

## Project Development

The project followed the **Waterfall Software Development Model**, progressing through structured development stages.

The work covered:

- Requirements analysis and system planning.
- Hardware and software specification.
- System architecture and component integration.
- AI and computer vision development.
- Embedded sensing and feedback mechanisms.
- Mobile application development.
- System integration and prototype evaluation.

---

## Project Objectives

The main objectives of Basira are to:

- Improve environmental awareness for people with visual impairments.
- Support obstacle awareness through object detection and distance estimation.
- Facilitate the recognition of familiar individuals.
- Provide accessible audio and haptic feedback.
- Integrate wearable technology with mobile application services.
- Explore additional safety features through location tracking and emergency alerts.

---

## Future Development

Potential areas for future improvement include:

- Enhancing object detection accuracy and real-time performance.
- Improving facial recognition under different lighting conditions.
- Advancing sensor integration and environmental awareness.
- Optimizing processing efficiency and power consumption.
- Improving wearable ergonomics and user experience.
- Expanding real-world testing and system evaluation.

---

## Project Information

| Item | Details |
|---|---|
| Project Name | Basira — AI-Powered Assistive Smart Glasses |
| Project Type | Computer Engineering Graduation Project |
| Institution | Taif University |
| Academic Year | 2025–2026 |
| Development Team | Computer Engineering Graduation Team |
| Project Domain | Artificial Intelligence, Computer Vision, Embedded Systems, IoT, and Mobile Development |

This project was developed collaboratively by a Computer Engineering graduation team.

---

## Scope & Disclaimer

Basira is an academic engineering project and assistive technology prototype. The features described in this repository reflect the project's design and documented development.

The system is not a certified medical device or a replacement for established mobility aids, guide dogs, or other safety practices. Its use should not be relied upon as the sole means of navigation or emergency response.

---

<p align="center">
  <strong>Basira — Technology That Helps People See Beyond Sight.</strong>
</p>
