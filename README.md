# AI Facial Identity Matching System 🛡️

A high-precision, browser-based biometric verification application powered by **face-api.js** and **TensorFlow.js**. This system automates the identity verification process by comparing a static reference document (ID photo) against a live webcam feed using deep learning neural networks.

## 🔗 Live Deployment
Experience the live application here:  
[**AI Facial Identity Matching System**](https://script.google.com/macros/s/AKfycbxWSs8WlyGourFrt4xh_2vTw6W0ML-C9sw6QeIc6X9wFMoTYHVIJJ9VKJpX7mv82dA/exec)

---

## 🚀 Overview

This project provides a "hands-free" biometric authentication experience. Unlike traditional systems that require manual captures, this system uses intelligent face-alignment logic to detect when a user is correctly positioned before automatically triggering the verification process.

### **Core Procedure:**
1.  **Reference Enrollment:** User uploads a clear portrait photo (ID/Source).
2.  **AI Initialization:** The system activates the webcam and loads the neural network weights.
3.  **Face Alignment:** The user aligns their face within the on-screen biometric guide.
4.  **Auto-Capture:** Once stable alignment is detected, a 3-second countdown triggers a biometric scan.
5.  **Matching:** The system compares the live descriptor against the reference descriptor and returns a match/mismatch result based on Euclidean distance.

---

## 🛠️ Tech Stack

* **Frontend:** HTML5, Tailwind CSS (Modern, responsive UI).
* **AI Engine:** [face-api.js](https://github.com/justadudewhohacks/face-api.js) (A JavaScript wrapper for TensorFlow.js).
* **Deep Learning:** TensorFlow.js (Runs neural network inference directly in the browser).
* **Icons:** FontAwesome 6.

---

## 🧠 Technical Deep Dive

The system utilizes three primary Deep Neural Networks (DNNs):

1.  **SSD MobileNet V1:** For robust face detection.
2.  **68-Point Face Landmark Detection:** For mapping facial structures.
3.  **Face Recognition Net:** Based on a ResNet-34-like architecture to compute a 128-float feature vector (descriptor) for any given face.



### **The Matching Logic**
The system calculates the similarity between the two faces using the **Euclidean Distance** formula. A strict threshold of **0.55** is applied:
* **Distance < 0.55:** Match Confirmed (High Confidence).
* **Distance > 0.55:** Access Denied.

---

## 🔮 Future Scope & Integrations

This project is designed as a modular biometric core. It can be easily integrated into larger architectures such as:
* **AI Facial Attendance Systems:** Automating employee check-ins without physical contact.
* **Secure Exam Proctoring:** Ensuring the identity of students during remote online testing.
* **Two-Factor Authentication (2FA):** Adding a biometric layer to web-based login portals.
* **Visitor Management Systems:** For smart offices and restricted area access.


---

## 🛡️ Privacy Note
All biometric processing occurs **locally in the user's browser**. No facial data or images are uploaded to any server, ensuring total user privacy and compliance with data protection standards.

---
**Developed by Earth Kumar Roy** *Built with passion for AI and Web Security.*
