# Non-Contact-Glaucoma-Detection-Device-for-IOP-Prediction




Selected for Smart India Hackathon 2024 | Team: Atomic Minds | PS ID: SIH1550  
Developed a portable, AI-enabled, non-invasive device designed for early detection of glaucoma by predicting Intraocular Pressure (IOP) using a combination of optical sensing technologies and machine learning algorithms. The device offers a novel, home-based screening solution integrated within a VR headset form factor, enabling accessible and continuous eye health monitoring without the need for specialized clinical equipment.

---

## 🌟 Key Features
- **Non-contact, portable glaucoma screening** enabling early detection without patient discomfort  
- **Multimodal sensor fusion** using IR camera, ADPD144RI reflectance sensor, and optical pachymeter for comprehensive 3D eye data acquisition  
- **Machine learning-based IOP prediction** utilizing convolutional neural networks and regression models for high accuracy  
- **Embedded in VR headset housing** providing compactness, ease of use, and immersive patient experience  
- **Robust performance** under varying lighting and patient motion conditions, ensuring reliability in diverse environments  
- **Real-time risk assessment and feedback** to users and healthcare providers for prompt interventions  

---

## 🔧 Hardware Components & Pinouts

### Microcontroller & Processing Unit: Raspberry Pi 5

| Component              | Sensor/Module               | Connection Type        | Pin / Interface          |
|------------------------|-----------------------------|-----------------------|-------------------------|
| Infrared (IR) Camera   | IR Camera Module            | CSI or USB            | CSI Connector / USB Port |
| Reflectance Sensor     | ADPD144RI (Optical Sensor) | I2C                   | SDA, SCL (GPIO2, GPIO3)  |
| Optical Pachymeter     | Custom Optical Sensor       | GPIO / Analog Input   | GPIO pins / ADC Input    |
| VR Headset             | Enclosure + Optics          | Mechanical Integration| N/A                     |
| Power Supply           | 5V DC Power                 | USB-C or Barrel Jack  | Power Input             |

> **Note:** Sensor data is collected synchronously via I2C and CSI interfaces. The Raspberry Pi 5 handles sensor data acquisition, pre-processing, ML inference, and user interface management.

---

## 🧠 Machine Learning Model

- **Input Data:**  
   - IR eye images capturing ocular features  
   - Reflectance sensor signals indicating tissue response  
   - Corneal motion data for biomechanical assessment  
- **Model Architecture:**  
   - Convolutional Neural Networks (CNN) for image feature extraction  
   - Regression models (e.g., Random Forest, Gradient Boosting) for numerical IOP estimation  
- **Output:**  
   - Predicted Intraocular Pressure (IOP) value  
   - Risk classification levels (Normal, Elevated, High Risk) for glaucoma  

---

## 📊 Data Pipeline

1. **Sensor Data Acquisition:**  
   - Continuous capture of IR images and reflectance signals  
   - Synchronized timing with optical pachymeter data for 3D eye profiling  
2. **Data Preprocessing:**  
   - Image normalization and enhancement to improve feature clarity  
   - Signal filtering to remove noise and artifacts  
   - Feature extraction using edge detection and texture analysis  
3. **Machine Learning Inference:**  
   - Real-time data fed into trained CNN and regression models  
   - IOP values predicted and glaucoma risk classified  
4. **User Interface & Alerts:**  
   - Results displayed on embedded UI or mobile/cloud dashboards  
   - Alerts triggered for abnormal IOP readings, prompting user or caregiver action  
5. **Data Logging & Model Updates:**  
   - Secure storage of anonymized sensor and prediction data for ongoing training and refinement  
   - Periodic model updates deployed via OTA (over-the-air) or manual updates  

---

## 🚀 Deployment & Usage

- Prototype packaged within a lightweight VR headset, allowing patients to comfortably wear the device during screening  
- User initiates test via simple interface; system captures and processes data in under 2 minutes  
- Results can be shared directly with ophthalmologists or health systems remotely  
- Ideal for early detection in remote or resource-limited settings  

---

## 🔧 Technologies Used

- Raspberry Pi 5 (processing and sensor integration)  
- IR Camera Module (ocular imaging)  
- ADPD144RI Optical Reflectance Sensor (tissue characterization)  
- Custom Optical Pachymeter Sensor (corneal measurements)  
- Python for sensor control and data processing  
- TensorFlow / PyTorch for machine learning model development  
- Flask / FastAPI for cloud dashboard and alert system  
- VR headset enclosure for ergonomic device form factor  

---

## 📁 Repository Structure

