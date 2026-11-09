# Basira — Software Design

This document describes the software architecture, development technologies, and main software modules implemented in the Basira AI-powered assistive smart-glasses project.

## 1. Software Architecture Overview

Basira uses a modular software architecture that combines artificial intelligence, embedded firmware, backend services, database management, and mobile application development.

The software is organized into three main subsystems:

1. **Raspberry Pi Software:** Handles computer vision, object detection, facial recognition, and audio guidance.
2. **ESP32 Firmware:** Manages sensor readings, obstacle proximity logic, vibration feedback, and wireless sensor-data access.
3. **Mobile Application:** Provides user management, facial registration interfaces, location tracking, and caregiver monitoring.

## 2. Raspberry Pi Software

The Raspberry Pi runs the primary AI and image-processing operations using Python.

### 2.1 Object Detection

The project uses the YOLO framework to detect and classify objects and potential hazards from camera input.

**Main operations:**
- Capturing visual input from the camera.
- Processing image frames using the trained detection model.
- Identifying objects and relevant environmental hazards.
- Producing object labels for subsequent audio guidance.

The training dataset included 500 training images, 200 testing images, and 100 verification images.

### 2.2 Audio Guidance and Text-to-Speech

A Text-to-Speech (TTS) component converts detected object names into spoken information.

**Main responsibilities:**
- Converting detection labels into audible output.
- Providing voice-based environmental information.
- Using a multithreaded TTS implementation to avoid blocking the main processing workflow.

### 2.3 Facial Recognition

The facial recognition subsystem is implemented in Python using the following technologies:

- **OpenCV:** Supports image and video processing.
- **Face Recognition Library:** Generates facial encodings and supports face identification.
- **PiCamera2:** Provides camera input.
- **Flask:** Hosts the facial recognition service and video-streaming interface.
- **MySQL:** Stores registered facial information in a local database on the Raspberry Pi.

**Face registration workflow:**

1. The mobile application opens the camera interface through the Flask service.
2. The Raspberry Pi provides a live camera stream.
3. The user captures a face image through the registration interface.
4. The system checks that exactly one face is visible.
5. The Face Recognition library generates a numerical facial encoding.
6. The encoding is serialized using Pickle.
7. The facial data, user ID, person's name, and relationship information are stored in the local MySQL database.

The stored facial encodings are subsequently used for face identification.

### 2.4 Flask Backend

Flask provides the web interface between the mobile application and the Raspberry Pi facial recognition subsystem.

**Main responsibilities:**
- Hosting the facial recognition service.
- Providing live camera streaming.
- Supporting face registration requests.
- Connecting the mobile application's camera interface to the Raspberry Pi processing service.

The application uses a WebView interface to access the Flask-based camera service.

## 3. ESP32 Embedded Firmware

The ESP32 firmware is responsible for sensor acquisition, obstacle proximity processing, and vibration feedback.

The firmware is developed using embedded programming and manages the following operations:

### 3.1 Sensor Data Acquisition

The ESP32 reads data from:

- **ToF Distance Sensor:** Measures the distance to nearby obstacles.
- **MPU-6050 IMU:** Provides acceleration and motion-related measurements.

The implementation uses I²C communication for sensor interfacing.

### 3.2 Obstacle Proximity Logic

The firmware continuously reads distance measurements and determines the appropriate vibration response.

According to the documented implementation:

- When an obstacle is detected within 300 mm, vibration intensity is adjusted according to its distance.
- When the distance falls below 30 mm, the vibration intensity reaches its maximum level.
- The MPU-6050 provides acceleration readings, including the vertical Z-axis value.

### 3.3 Wireless Communication

The ESP32 establishes a Wi-Fi connection and runs an HTTP server.

The firmware exposes sensor information through the following endpoints:

| Endpoint | Purpose |
|---|---|
| `/` | Provides a simple webpage with access to sensor information |
| `/data` | Returns the latest sensor readings in JSON format |

The JSON response includes:
- Obstacle distance.
- Vibration intensity.
- Z-axis acceleration.

**Sensor model note:** The hardware specification identifies TOF10120, while the firmware implementation describes VL53L0X. The exact final sensor model requires confirmation.

## 4. Mobile Application Software

The Basira mobile application is developed using Flutter and provides the main interface for users and caregivers.

### 4.1 User Management

The application provides user-management functionality, including:

- User registration and login interfaces.
- Assigning family relationships.
- Viewing linked family members.
- Accessing user profiles and monitoring features.
- Arabic and English language support.

### 4.2 Location Tracking

The application uses GPS location data to support caregiver monitoring.

**Main operations:**
- Retrieving the user's location from the backend database.
- Updating location information periodically.
- Displaying the user's position on an interactive map.
- Allowing caregivers to view location information for linked users.

The report describes location updates at approximately five-minute intervals.

### 4.3 Facial Registration Interface

The mobile application provides a camera interface that connects to the Raspberry Pi Flask service.

**Main operations:**
- Accessing the live camera stream through a WebView.
- Capturing images for face registration.
- Submitting registration information.
- Associating registered faces with names and family relationships.

### 4.4 Caregiver Interface

The caregiver interface provides access to monitoring and user-related features.

These include:
- Viewing linked users.
- Selecting a user for monitoring.
- Accessing location information.
- Using the facial registration and camera interfaces.

## 5. Database Design

The project uses separate data-storage components for facial recognition and mobile application services.

### 5.1 Local Facial Recognition Database

A MySQL database runs on the Raspberry Pi and stores registered facial information.

The stored information includes:
- User ID.
- Registered person's name.
- Relationship information.
- Serialized facial encodings.

This database supports the facial identification subsystem.

### 5.2 Mobile Application Database

The mobile application uses a separate online relational database to manage application information.

The documented database structure includes:

| Table | Purpose |
|---|---|
| `users` | Stores application users and their information |
| `userroles` | Defines user roles and access responsibilities |
| `userlocation` | Stores GPS coordinates and location timestamps |

The location information is used by the application to display users' positions on the map.

**Important distinction:** The local MySQL facial database and the online mobile application database serve different purposes and should not be treated as one database.

## 6. Software Technologies

The following table summarizes the main software technologies documented in the project.

| Technology | Role |
|---|---|
| Python | AI processing and Raspberry Pi development |
| YOLO | Object detection and classification |
| OpenCV | Image and video processing |
| Face Recognition Library | Facial encoding and identification |
| Flask | Backend services and camera streaming |
| Pickle | Facial encoding serialization |
| C++ / ESP32 Firmware | Embedded sensor and hardware control |
| Flutter | Cross-platform mobile application |
| MySQL | Local facial recognition database |
| I²C | Sensor communication |
| HTTP | Communication with the ESP32 and Flask services |
| JSON | Sensor-data exchange format |
| GPS | User location tracking |
| Android Studio | Mobile application development environment |
| Arduino IDE | Embedded development environment |
| Figma | User interface design |

## 7. Software Integration

The software subsystems work together to provide the main assistive functionalities:

- **Object Detection:** Camera input is processed by the Raspberry Pi using the YOLO framework, and detected object labels are converted into spoken guidance.
- **Obstacle Feedback:** The ESP32 reads distance measurements and adjusts vibration intensity according to obstacle proximity.
- **Facial Recognition:** The Raspberry Pi processes camera frames, compares facial encodings against registered data, and supports face registration through Flask.
- **Caregiver Monitoring:** The Flutter application retrieves location information and provides monitoring interfaces for linked users.
- **Sensor Monitoring:** The ESP32 makes sensor readings available through an HTTP endpoint using JSON responses.

## 8. Implementation Scope and Technical Notes

The software architecture described here reflects the implementation and development details documented in the project report.

Some experiments were conducted through simulation, while other functions were demonstrated through practical implementation and application interfaces. These should be distinguished when evaluating the system.

The documented implementation does not establish that every subsystem has undergone comprehensive real-world validation under all operating conditions.

---

**Project:** Basira — AI-Powered Assistive Smart Glasses

**Project Period:** August 2025 – June 2026
