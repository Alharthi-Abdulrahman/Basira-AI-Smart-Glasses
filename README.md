# Basira — AI-Powered Assistive Smart Glasses

**An Intelligent Wearable Assistive System for Enhanced Mobility, Awareness, and Safety**

<p align="center">
  <img src="assets/images/01-project-logo.jpeg" alt="Basira Project Logo" width="180">
</p>

## Overview

Basira is an AI-powered assistive smart glasses project developed as a collaborative graduation project by a Computer Engineering team at Taif University.

The project explores the integration of Artificial Intelligence (AI), Computer Vision, Embedded Systems, Internet of Things (IoT), and mobile application technologies into a wearable assistive solution designed to support people with visual impairments.

The system combines smart glasses equipped with a camera and embedded sensors with AI-powered processing to provide environmental awareness through object detection, facial recognition, distance estimation, and assistive feedback.

A companion mobile application complements the wearable system by providing interfaces for user interaction and supporting additional safety-related functionality.

## The Problem

People with visual impairments may encounter difficulties navigating unfamiliar environments, identifying people, and detecting obstacles in their surroundings.

Basira explores how AI, computer vision, and wearable technologies can help address these challenges by providing environmental information and assistive feedback.

## Key Features

### 1. AI-Powered Object Detection

Uses computer vision and AI-based processing to identify objects in the surrounding environment and provide information that can support user awareness.

### 2. Facial Recognition

Provides facial recognition functionality to help users identify registered individuals.

### 3. Obstacle Detection and Distance Estimation

Uses camera-based detection and distance-sensing technology to help identify nearby obstacles and estimate their distance.

### 4. Haptic Feedback

Uses vibration motors to provide tactile alerts, offering an additional feedback method when obstacles or relevant environmental conditions are detected.

### 5. Mobile Application

A companion mobile application provides interfaces for system interaction and includes features related to user management and facial registration.

### 6. Safety and Location Monitoring

The project also explores safety-related functionality, including location monitoring and emergency notifications to support additional awareness and assistance.

## Prototype Design

The following image presents the Basira smart glasses prototype from four different views: front, upper, right, and left.

<p align="center">
  <img src="assets/images/02-prototype-design.jpg" alt="Basira Smart Glasses Prototype - Four Views" width="750">
</p>

## System Analysis

This section presents the system analysis and the design considerations behind Basira, illustrating the problem domain and the main requirements addressed by the project.

<p align="center">
  <img src="assets/images/03-system-analysis.jpg" alt="Basira System Analysis" width="850">
</p>

## Overall System Architecture

Basira integrates three main components:

- **Smart Glasses:** The wearable component contains the camera, sensors, and feedback hardware required to collect environmental information and communicate alerts.
- **Embedded Processing and Sensors:** The embedded system integrates the Raspberry Pi and ESP32 platforms with connected sensors and processing components.
- **Mobile Application:** Provides a user interface for interacting with the system and managing supported application features.

<p align="center">
  <img src="assets/images/04-overall-architecture.jpg" alt="Basira Overall System Architecture" width="850">
</p>

## Methods and Requirements

This section presents the development methodology and the functional and technical requirements considered during the design and development of the Basira system.

<p align="center">
  <img src="assets/images/05-methods-requirements.jpg" alt="Basira Methods and Requirements" width="850">
</p>

## System Interfaces

The following image presents the system interfaces designed for the Basira project, illustrating the user-facing interface concepts and application screens.

<p align="center">
  <img src="assets/images/06-system-interfaces.jpg" alt="Basira System Interfaces" width="850">
</p>

## Hardware Components

| Component | Purpose |
|---|---|
| Raspberry Pi 4 | Main embedded computing platform |
| ESP-WROOM-32 (ESP32) | Microcontroller and hardware integration |
| Raspberry Pi Camera Module 2 | Image and video capture |
| TOF10120 | Distance measurement |
| MPU-6050 IMU | Motion and orientation sensing |
| Coin Vibration Motors | Haptic feedback |

## Technologies and Tools

| Technology / Tool | Application |
|---|---|
| Python | AI processing and system development |
| Computer Vision | Image analysis and visual perception |
| Flask | Backend development |
| SQLite | Database management |
| Flutter | Mobile application development |
| Android Studio | Mobile application development environment |
| Arduino IDE | ESP32 programming and hardware integration |
| Figma | UI/UX design and prototyping |
| Visual Studio Code | Development environment |

## Implementation Highlights

The project brings together multiple areas of Computer Engineering:

- Integration of AI-powered computer vision capabilities.
- Development of facial recognition functionality.
- Integration of camera-based object detection.
- Distance measurement using a dedicated sensor.
- Embedded hardware integration using Raspberry Pi and ESP32.
- Implementation of vibration-based assistive feedback.
- Development of a companion mobile application.
- Database integration for supported application functionality.

## Project Objectives

- Explore AI-powered assistive technologies for people with visual impairments.
- Improve environmental awareness through computer vision.
- Support facial recognition and obstacle detection.
- Provide additional feedback through haptic alerts.
- Integrate embedded systems with mobile application technologies.
- Explore safety-oriented features in a connected wearable system.

## Scope and Limitations

Basira is an academic graduation project developed to explore the integration of AI, computer vision, embedded systems, and mobile technologies into an assistive wearable solution.

The described features represent the project's documented functionality and development scope. Performance, reliability, and real-world effectiveness may depend on environmental conditions, hardware limitations, and system integration.

Basira is not intended to replace existing mobility aids or professional assistance.

## Future Development

Potential areas for further development include:

- Improving object detection accuracy and environmental understanding.
- Enhancing facial recognition performance under different lighting conditions.
- Improving distance estimation and obstacle detection.
- Optimizing embedded processing and power consumption.
- Expanding mobile application functionality.
- Further testing and evaluating system performance in real-world environments.

## Project Information

- **Project Name:** Basira
- **Institution:** Taif University
- **Department:** Computer Engineering
- **Project Type:** Collaborative Graduation Project
- **Project Duration:** August 2025 – June 2026

---

**Basira — An Intelligent Wearable Assistive System for Enhanced Mobility, Awareness, and Safety.**
