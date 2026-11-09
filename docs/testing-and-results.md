# Basira — Testing and Results

This document summarizes the experiments, implementation evidence, and results documented during the development of the Basira AI-powered assistive smart-glasses project.

It distinguishes between software evaluation, practical implementation evidence, and simulation results. The reported outcomes should not be interpreted as comprehensive validation of the complete wearable system under all real-world conditions.

## 1. Testing Overview

Testing and evaluation activities covered several project components:

- YOLO-based object detection.
- Object detection using the Raspberry Pi.
- Facial detection and recognition.
- ESP32 sensor acquisition and vibration-control logic.
- Mobile application interfaces and GPS tracking.
- Initial facial detection simulation using Proteus.

The project report presents both simulation results and practical implementation evidence.

## 2. Object Detection Model Evaluation

The project used a trained YOLO-based model to detect and classify environmental objects and potential hazards.

The model evaluation included the following reported results and visualizations:

| Evaluation Evidence | Description |
|---|---|
| F1 Score | Evaluation of the balance between precision and recall |
| Precision | Assessment of correct positive detections |
| Recall | Assessment of detected relevant objects |
| Confusion Matrix | Visualization of classification performance |
| Final Model Results | Visual results from the trained model |
| Batch Detection | Detection examples from two evaluation batches |

The report includes the following figures:

- Figure 5-3: F1 Score for Trained Model.
- Figure 5-4: Precision for Trained Model.
- Figure 5-5: Recall for Trained Model.
- Figure 5-6: Confusion Matrix for Trained Model.
- Figure 5-8: Final Results for Trained Model.
- Figures 5-9 and 5-10: Batch Detection Results.

These visualizations provide evidence of the model evaluation process and its object-detection results.

## 3. Raspberry Pi Object Detection

The trained object-detection model was also demonstrated on the Raspberry Pi.

The project report includes:

- An object-detection result in Figure 5-1.
- An object-detection implementation result from the Raspberry Pi in Figure 5-11.

These figures document the use of the Raspberry Pi processing unit for camera-based object detection.

The implementation combines image input, YOLO-based processing, and object classification as part of the assistive system.

## 4. Facial Recognition Evaluation

The facial recognition subsystem was documented through an initial simulation and practical software implementation.

### 4.1 Proteus Simulation

An initial facial detection experiment was conducted using Proteus.

The simulation included:

- A Raspberry Pi-based facial detection setup.
- The Haar Cascade frontal-face detection model.
- A TFT display interface.
- Visual identification results displayed on the simulated screen.

The report presents the simulation results in Figure 4-13.

**Testing scope:** This experiment represents a software and hardware simulation. It should not be considered proof of complete physical smart-glasses performance.

### 4.2 Practical Facial Recognition Implementation

The practical implementation used a Raspberry Pi camera, OpenCV, and the Face Recognition library.

The documented registration workflow included:

1. Opening the camera interface through the mobile application.
2. Accessing the live video stream provided by the Flask service.
3. Capturing an image for facial registration.
4. Checking that exactly one face is visible.
5. Generating a numerical facial encoding.
6. Saving the registered facial information in the Raspberry Pi MySQL database.

The report provides the following implementation evidence:

| Figure | Evidence |
|---|---|
| Figure 5-12 | Face registration through the mobile emulator |
| Figure 5-13 | Facial database stored on the Raspberry Pi |

These results demonstrate the documented registration workflow and database integration.

## 5. ESP32 Sensor and Vibration Implementation

The ESP32 subsystem was programmed to acquire sensor readings and control vibration feedback according to obstacle distance.

The documented firmware includes:

- Distance measurements using a Time-of-Flight sensor.
- Acceleration readings from the MPU-6050.
- Obstacle proximity processing.
- Vibration intensity adjustment.
- Wireless sensor-data access through an HTTP server.

### 5.1 Documented Obstacle-Response Logic

The firmware describes the following distance thresholds:

| Distance Condition | Documented Response |
|---|---|
| Obstacle within 300 mm | Distance-based vibration adjustment |
| Obstacle closer than 30 mm | Maximum vibration intensity |

The firmware also makes sensor information available through the `/data` endpoint in JSON format.

The report documents the firmware implementation and its sensor-processing logic. These thresholds describe programmed behavior and should not be interpreted as independently measured detection accuracy.

## 6. Mobile Application Evaluation

The mobile application was developed using Flutter and demonstrated through application interfaces and emulator screenshots.

The report includes evidence of the following functions:

| Figure | Documented Result |
|---|---|
| Figure 5-2 | Mobile emulator tracking interface |
| Figure 5-12 | Facial registration interface |
| Figure 5-14 | Mobile application login interface |
| Figure 5-15 | Map interface |
| Figure 5-16 | Mobile application database |
| Figures 5-17 and 5-18 | Parent and user application interfaces |

The documented application functions include:

- User login and management interfaces.
- Family relationship management.
- Facial registration access.
- GPS location display on an interactive map.
- Location information stored with timestamps.

The report describes location updates at approximately five-minute intervals.

These screenshots and implementation descriptions provide evidence of the application's interfaces and documented functionality.

## 7. Results Summary

The project report provides implementation evidence across the main subsystems.

| Subsystem | Reported Evidence |
|---|---|
| YOLO Object Detection | Model evaluation figures, confusion matrix, and detection batches |
| Raspberry Pi | Object-detection implementation result |
| Facial Recognition | Proteus simulation, face registration, and local database |
| ESP32 | Sensor acquisition, distance-based vibration logic, and HTTP JSON endpoint |
| Mobile Application | Login, tracking, map, registration, and user interfaces |

The results demonstrate the development and integration of several key Basira components. However, the available evidence does not establish comprehensive end-to-end performance under all real-world operating conditions.

## 8. Limitations and Future Testing

The project report identifies several limitations and areas requiring further evaluation.

### 8.1 Environmental Limitations

- Camera-based detection may be affected by lighting conditions.
- Low-light performance requires further improvement.
- False detections may affect the reliability of environmental awareness.

### 8.2 Practical Testing Limitations

The report identifies the absence of sufficient practical testing as an important limitation.

Further evaluation is needed to assess the system under different real-world conditions, including:

- Indoor and outdoor environments.
- Different lighting conditions.
- Various obstacle distances and positions.
- Different user movement patterns.
- Long-duration operation and battery performance.

### 8.3 Recommended Improvements

The report recommends several potential improvements:

- AI model optimization for edge processing.
- Model quantization and pruning.
- Improved multi-sensor fusion.
- Enhanced low-light image processing.
- More standardized testing and evaluation procedures.
- Improved power efficiency and hardware integration.

These items represent recommendations and future work, not completed project results.

## 9. Conclusion

The Basira project demonstrated the development of an AI-powered assistive wearable system combining object detection, facial recognition, embedded sensing, vibration feedback, and mobile application functionality.

The project report documents model evaluation results, Raspberry Pi implementation evidence, facial recognition workflows, ESP32 firmware functionality, and mobile application interfaces.

Although these results demonstrate progress across the individual subsystems, further standardized and real-world testing is required to evaluate the reliability, performance, and safety of the complete integrated system.

---

**Project:** Basira — AI-Powered Assistive Smart Glasses

**Project Period:** August 2025 – June 2026
