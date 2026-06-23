# Netra Lens
<<<<<<< HEAD
A Native Android Application 
=======
Netra Lens is a native Android application designed to bridge the visual gap for visually impaired users. It utilizes a hybrid AI architecture, combining the low-latency speed of Google's ML Kit for real-time object detection with the deep reasoning capabilities of the Gemini API for detailed scene description.

## Key Features

- Real-Time Object Detection: Instant feedback on objects in the camera frame (e.g., "Chair," "Cup," "Person") using on-device processing.
- Generative Scene Description: Users can capture a scene to receive a rich, context-aware description (e.g., "A busy street crossing with a red traffic light") powered by the Gemini Vision model.
- Text-to-Speech (TTS) Integration: All visual data is instantly converted to audio feedback, ensuring full accessibility.
- Offline Capability: Basic object detection works without an internet connection using on-device models.
- Gieger Counter: User can use phone's camera to navigate towards light by implementing luma sensor to beep when near a light source
- Fall detection and SOS: Phone automatically detects if a user has fallen and sends an sos message along with location to chosen contact
- Emotion detector: Can count number of people in camera stream and detect emotions

# Tech Stack
This project is built using modern Android development practices and strict MVVM (Model-View-ViewModel) architecture.
- Language: Kotlin
- UI Framework: Jetpack Compose (Material 3 Design)
- On-Device ML: Google ML Kit (Object Detection & Tracking)
- Cloud AI: Google Gemini API (Multimodal Generative AI)
- Asynchronous Processing: Coroutines & Flow
- State Management: StateFlow & Sealed Classes (UI State)
- Dependency Injection: Hilt / Dagger
- Networking: Retrofit & OkHttp

# How It Works
### NetraLens solves the "Speed vs. Accuracy" trade-off by using two distinct AI pipelines:

1. **The Fast Path (The Reflex):**
- Input: Continuous Camera Stream (ByteBuffer)
- Engine: ML Kit (On-Device)
- Latency: < 50ms
- Role: Tells the user where things are and what they roughly are to prevent collisions.

2. **The Deep Path (The Brain):**
- Input: Single Captured Frame (Bitmap converted to Base64)
- Engine: Gemini Pro Vision (Cloud)
- Latency: ~2-5 seconds
- Role: Tells the user context—reading signs, describing expressions, or identifying complex scenarios.

# Screeenshots
![IMG-20251207-WA0012](https://github.com/user-attachments/assets/12caed4b-69db-4268-ab34-c8293d741c47)
![WhatsApp Image 2025-12-07 at 22 13 54_b5740374](https://github.com/user-attachments/assets/3f20e9e2-635f-41a1-9ee3-7e6fb0e24ef6)
![IMG-20251207-WA0010](https://github.com/user-attachments/assets/1242229d-980e-4e12-aaae-34d57543f9f0)
![IMG-20251207-WA0009](https://github.com/user-attachments/assets/f7d6d7be-ca93-43ea-ab1c-790042585091)
![IMG-20251207-WA0013](https://github.com/user-attachments/assets/cc40960c-01e6-43ea-b525-3e423dc71d3d)

### Developed by Nikhil Mahajan Information Science Student & Android Developer
>>>>>>> 66609b2d5f1fcee4a1d668353b5f376c2eb13163

