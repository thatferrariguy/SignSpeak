## **Overview**  
This project, *Sign Language Gesture Recognition to Speech using Machine Learning*, focuses on recognizing **static sign language inspired hand gestures** and converting them into text and speech output. The system is designed as an assistive and educational tool to demonstrate real time hand gesture recognition using computer vision and machine learning techniques.

The project primarily supports **static alphabet gestures**, along with control gestures such as space and full stop. It does not aim to represent full sign language grammar or dynamic gesture interpretation.

---

## 🎯 Features

- **Real-Time Gesture Recognition**: Recognizes hand gestures from a live webcam feed.
- **Stabilized Prediction**: Uses temporal stabilization to reduce flickering and improve recognition accuracy.
- **Word and Sentence Formation**: Forms words and simple sentences using predefined control gestures such as space and full stop.
- **Text-to-Speech Conversion**: Converts recognized text into audible speech for better accessibility.
- **Interactive GUI**: Displays the live camera feed, detected hand landmarks, and recognized characters in real time.

---

## **Project Highlights**

- **Custom Dataset Creation**  
  A custom dataset was created using static hand gesture images inspired by sign language alphabets. The dataset includes alphabet gestures, digits, and control gestures such as **space** and **full stop**.

  Dynamic gestures that require motion based interpretation, such as J and Z, are considered outside the current scope of this system due to its static gesture based approach.

- **Pretrained Model Included**  
  A pretrained machine learning model is provided to allow users to immediately run and test the system.

- **Custom Training Support**  
  Users can create and train their own gesture datasets using the provided scripts to improve personalization and accuracy.

---

## 🔧 Tech Stack

- **Programming Language**: Python  
- **Libraries**: MediaPipe, OpenCV, Tkinter, pyttsx3, scikit-learn  
- **Machine Learning Model**: Random Forest Classifier (landmark based)

---

## **Usage**

### **Option 1: Use the Pretrained Model**

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/sign-language-to-speech.git
   cd sign-language-to-speech
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   python main.py
   ```

4. Ensure a working webcam and that the **model.p** file is present in the project directory.


---

### **Option 2: Train Your Own Model**

1. **Dataset Collection**
   - Run `collectImgs.py` to capture gesture images using a webcam.
   - Adjust dataset size and number of classes as required.

2. **Dataset Processing**
   - Use `createDataset.py` to extract hand landmarks and generate a feature dataset.

3. **Model Training**
   - Train a new classifier using `trainClassifier.py`.
   - The newly trained model will replace the existing model file.

---

## **How the Project Was Built**

1. **Dataset Collection**
   - Gesture images were collected using a webcam under varying lighting and angles.
   - The dataset includes multiple static gesture classes representing alphabets, digits, and control gestures.

2. **Feature Extraction**
   - MediaPipe was used to extract **21 hand landmarks** per frame.
   - Each landmark was represented as normalized 2D coordinates, resulting in **42 features per sample**.

3. **Model Training**
   - A Random Forest Classifier was trained using the extracted landmark features.
   - The dataset was split into training and testing sets to evaluate performance.

4. **Real-Time Inference**
   - The trained model was integrated into a real time system using OpenCV.
   - A stabilization buffer was implemented to reduce misclassification.
   - Text to speech functionality was added using pyttsx3.
   - A graphical user interface was developed using Tkinter.

---

## **Future Enhancements**

- Support for **dynamic gesture recognition** using sequence based models.
- Integration of deep learning architectures for improved accuracy.
- Expansion to additional sign language variations.
- Deployment as a web or mobile application.

---

## **Suggestions and Collaboration**

Suggestions, improvements, and contributions are welcome. Feel free to open issues or submit pull requests to help extend the capabilities of this project.

---

## **AI Capstone Project**

This project was developed as part of our **Artificial Intelligence Capstone Project**, with the objective of applying machine learning and computer vision techniques to build an assistive sign language inspired gesture recognition system with text and speech output.

---

## **Team Members and Roles**

- **R. Keshav**  
  *Project Leader, Data Expert, Prototype Builder / Coder*  
  Responsible for project planning and task coordination, AI model selection, dataset preparation, model training, system integration, and core prototype development.

- **S. Keerthana**  
  *Information Researcher, Designer*  
  Responsible for researching relevant information and sources, assisting in documentation, and designing the user experience and interface for the prototype.

- **S. Keerthiga**  
  *Marketing and Communications Lead*  
  Responsible for preparing project documentation, coordinating submission materials, selecting appropriate project titles, and managing communication related to project presentation.

- **S. Aliza Ayman**  
  *Tester*  
  Responsible for testing the prototype with users, collecting feedback, identifying issues, and assisting in improving system reliability.

- **M.S. Kamaljith**  
  *Video Producer*  
  Responsible for recording demonstrations, documenting project progress through video, and preparing visual material for project submission and presentation.

---

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

