# EXPERIMENT 5: Comparing Prompting Techniques Through Engineering Problem-Solving Scenarios
# Date : 13-08-2026
# Reg no : 212223060290

## Aim

To compare different prompting techniques and evaluate their effectiveness in solving a real-world engineering problem selected from a 3rd-year/final-year engineering project by analysing the quality, accuracy, depth, clarity, feasibility, and usefulness of AI-generated responses.


## Project Title

**ReasonTrace – Explainable Face Liveness Detection System**

## Selected Engineering Scenario

### Problem Statement

Face recognition systems are increasingly used for authentication and security. However, attackers can attempt to fool these systems using photographs, videos, or replay attacks. Therefore, a reliable **face liveness detection mechanism** is required to determine whether the input is from a genuine live person or a spoofed face.

The selected engineering problem is:

> **How can a computer-vision-based system accurately detect whether a face presented to a camera is live or a spoof using suitable features, preprocessing techniques, and machine-learning/deep-learning methods?**

The solution should consider detection accuracy, real-time performance, robustness against different spoofing attacks, and practical deployment requirements.


# 1. Base Prompt

The following simple prompt was used without applying advanced prompting techniques:

> "Suggest a method to detect face spoofing using computer vision."

### AI-Generated Output

A computer-vision-based face spoofing detection system can use a camera to capture the user's face and determine whether it is real or fake. The system can perform face detection, extract facial features, and use a machine-learning model to classify the input as live or spoof.

A CNN-based model can be trained using real and spoofed face images. During testing, the camera captures the face, preprocesses the image, and passes it to the trained model. The model then predicts whether the face is genuine or a spoof.

### Observation

The response provides a basic solution but does not give enough information about:

- Dataset selection
- Spoofing attack types
- Preprocessing
- Model architecture
- Evaluation metrics
- Real-time implementation
- Limitations
- Engineering feasibility


# 2. Prompting Technique 1 – Straightforward Prompt

### Prompt

> "Design a computer-vision-based face liveness detection system that can distinguish between a genuine face and spoof attacks such as photographs, videos, and replay attacks. Suggest suitable preprocessing, machine-learning/deep-learning methods, and evaluation metrics."

### AI-Generated Output

A face liveness detection system can be developed using the following pipeline:

```text
Camera Input
      ↓
Face Detection
      ↓
Preprocessing
      ↓
Feature Extraction
      ↓
Classification
      ↓
Live / Spoof Decision
```

1. Capture the user's face using a camera.
2. Detect the face using a face-detection algorithm.
3. Resize and normalize the detected face.
4. Extract relevant facial features.
5. Use a CNN or transfer-learning model for classification.
6. Train the model using real and spoofed face samples.
7. Evaluate the system using accuracy, precision, recall, F1-score and False Acceptance Rate.
8. Deploy the trained model for real-time prediction.


# 3. Prompting Technique 2 – Role-Based Prompting

### Prompt

> "Act as an expert computer-vision and machine-learning engineer. Design a practical face liveness detection system for a final-year engineering project. The system must identify real users and detect photo, video, and replay attacks. Recommend suitable datasets, preprocessing techniques, model architecture, training strategy, evaluation metrics, and real-time deployment methods. Explain the solution step by step in an implementation-oriented manner."

### AI-Generated Output

An appropriate architecture for the project is:

```text
Webcam
   ↓
Face Detection
   ↓
Face Alignment
   ↓
Image Preprocessing
   ↓
CNN Feature Extraction
   ↓
Liveness Classifier
   ↓
Live / Spoof Output
```

### Recommended Components

**Face Detection:**  
Use a lightweight detector such as MediaPipe Face Detection or a YOLO-based face detector.

**Preprocessing:**

- Detect and crop the face.
- Resize to a fixed resolution.
- Normalize pixel values.
- Perform data augmentation.
- Optionally perform face alignment.

**Model:**

A lightweight CNN or transfer-learning architecture can be used. MobileNet or EfficientNet can be considered when real-time performance is important.

**Dataset:**

The dataset should contain genuine faces and multiple spoof categories, including:

- Printed photographs
- Mobile-phone displays
- Replay videos
- Presentation attacks where applicable

**Evaluation:**

The model should be evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- False Acceptance Rate
- False Rejection Rate
- Equal Error Rate

For real-time deployment, inference time and frames-per-second should also be measured.


# 4. Prompting Technique 3 – Structured Prompting

### Prompt

> "Solve the following engineering problem using a structured approach.
>
> Problem: Develop a real-time face liveness detection system capable of distinguishing genuine faces from photo, video, and replay attacks.
>
> Provide the answer under these headings:
>
> 1. Problem analysis
> 2. System requirements
> 3. Proposed architecture
> 4. Dataset
> 5. Preprocessing
> 6. Model selection
> 7. Training process
> 8. Evaluation metrics
> 9. Real-time deployment
> 10. Limitations
> 11. Expected outcome
>
> Prioritize accuracy, real-time performance, robustness and implementation feasibility."

### AI-Generated Output

### 1. Problem Analysis

The main challenge is distinguishing a genuine three-dimensional human face from a two-dimensional or replayed representation.

### 2. System Requirements

- Camera input
- Face detection
- Face preprocessing
- Liveness classification
- Real-time prediction
- Spoof attack detection
- Performance evaluation

### 3. Proposed Architecture

```text
Camera
   ↓
Face Detection
   ↓
Face Cropping & Alignment
   ↓
Preprocessing
   ↓
Feature Extraction
   ↓
Liveness Classification
   ↓
Live / Spoof
```

### 4. Dataset

The dataset should include real faces and several presentation-attack categories. Training and testing data should be separated properly to prevent data leakage.

### 5. Preprocessing

Images can be resized, normalized and augmented using operations such as rotation, scaling and brightness variation.

### 6. Model Selection

A CNN-based classifier or transfer-learning model such as MobileNet/EfficientNet can be selected.

### 7. Training

The dataset is divided into training, validation and testing sets. The model is trained using an appropriate loss function and optimizer.

### 8. Evaluation

Accuracy, precision, recall, F1-score, FAR, FRR and EER can be used.

### 9. Deployment

A lightweight model can be integrated with OpenCV and executed using a webcam for real-time prediction.

### 10. Limitations

Performance may decrease with:

- Poor lighting
- Unseen spoofing methods
- Low-quality cameras
- Large changes in face pose
- Attacks not represented in the training dataset

### 11. Expected Outcome

The system should classify the detected face as **Live** or **Spoof** with high accuracy while maintaining acceptable real-time performance.


# 5. Prompting Technique 4 – Constraint-Based Prompting

### Prompt

> "Design a face liveness detection solution under the following constraints:
>
> - It must work with a normal webcam.
> - It must operate close to real time.
> - It must detect printed-photo, screen-replay and video-based attacks.
> - The solution should be suitable for a final-year engineering project.
> - Prefer lightweight and publicly available models/datasets.
> - Avoid requiring specialized hardware.
> - Include preprocessing, model selection, training, testing and deployment.
> - Explain the advantages and limitations of the proposed approach.
> - Suggest measurable metrics for validating the engineering solution.
>
> Provide the solution as a practical implementation plan."

### AI-Generated Output

A practical solution is to build a lightweight CNN-based liveness classifier.

### System Pipeline

```text
Webcam
   ↓
Face Detection
   ↓
Face Crop
   ↓
Image Normalization
   ↓
Lightweight CNN
   ↓
Liveness Score
   ↓
Threshold Decision
   ↓
LIVE / SPOOF
```

The webcam continuously captures frames. A face detector identifies the face region. The detected region is resized and normalized before being passed to the liveness model.

A lightweight transfer-learning architecture can be used to reduce computational requirements.

The training dataset should contain:

- Genuine faces
- Printed-photo attacks
- Screen attacks
- Replay attacks

Data augmentation can improve robustness against variations in lighting, scale and orientation.

### Validation Metrics

| Metric | Purpose |
|---|---|
| Accuracy | Overall classification performance |
| Precision | Reliability of spoof predictions |
| Recall | Ability to detect spoof samples |
| F1-score | Balance between precision and recall |
| FAR | Rate of spoof samples incorrectly accepted |
| FRR | Rate of genuine users incorrectly rejected |
| FPS | Real-time performance |


# 6. Prompting Technique 5 – Step-by-Step Prompting

### Prompt

> "Develop a face liveness detection system by following these stages:
>
> Stage 1: Identify the major security problem.
>
> Stage 2: Identify possible spoofing attacks.
>
> Stage 3: Determine the input and output requirements.
>
> Stage 4: Design the computer-vision pipeline.
>
> Stage 5: Select suitable features and a classification model.
>
> Stage 6: Select appropriate training and testing data.
>
> Stage 7: Define evaluation metrics.
>
> Stage 8: Consider real-time deployment constraints.
>
> Stage 9: Identify limitations and possible improvements.
>
> Give concise engineering reasoning for each stage and produce a final recommended architecture."

### AI-Generated Output

### Stage 1 – Security Problem

Traditional face-recognition systems may accept a photograph or replayed video as a genuine face. Liveness detection is therefore required before authentication.

### Stage 2 – Spoofing Attacks

Common attacks include:

- Printed photographs
- Smartphone screen attacks
- Replay videos
- Other presentation attacks

### Stage 3 – Input and Output

**Input:** Live webcam frame.

**Output:** Liveness classification and confidence score.

### Stage 4 – Computer-Vision Pipeline

```text
Video Frame
     ↓
Face Detection
     ↓
Face Alignment
     ↓
Preprocessing
     ↓
Feature Extraction
     ↓
Liveness Classifier
     ↓
Decision
```

### Stage 5 – Model

A lightweight CNN or transfer-learning architecture is appropriate because the application requires real-time inference.

### Stage 6 – Data

Use a dataset containing genuine and spoof samples from multiple attack types. Training and testing identities should preferably be separated to measure generalization.

### Stage 7 – Metrics

Use accuracy, precision, recall, F1-score, FAR, FRR and EER.

### Stage 8 – Deployment

OpenCV can be used for webcam acquisition and face processing. A lightweight deep-learning model can perform classification.

### Stage 9 – Limitations

The model may fail against unknown attacks or environmental conditions that are not represented in the training data.

### Final Architecture

```text
Webcam
   ↓
Face Detection
   ↓
Preprocessing
   ↓
Lightweight CNN
   ↓
Liveness Score
   ↓
Threshold
   ↓
┌─────────────┐
│ LIVE / SPOOF│
└─────────────┘
```


# 7. Comparison of Prompting Techniques

| Prompting Technique | Quality | Accuracy | Depth | Clarity | Feasibility | Usefulness |
|---|---|---|---|---|---|---|
| Naïve/Base Prompt | Medium | Medium | Low | Medium | Medium | Low |
| Straightforward Prompt | Good | Good | Medium | Good | Good | Good |
| Role-Based Prompt | Very Good | Very Good | High | Very Good | Very Good | Very Good |
| Structured Prompt | Excellent | Very Good | Excellent | Excellent | Very Good | Excellent |
| Constraint-Based Prompt | Excellent | Excellent | High | Excellent | Excellent | Excellent |
| Step-by-Step Prompt | Excellent | Very Good | Excellent | Excellent | Very Good | Excellent |

---

# 8. Analysis and Observations

The experiment demonstrates that **prompt quality significantly influences the quality of AI-generated engineering solutions**.

The naïve prompt produced a general answer containing only the basic concept of using computer vision and CNNs. It did not provide sufficient information for direct engineering implementation.

The straightforward prompt improved the response by explicitly mentioning the required task, spoofing attacks, preprocessing and evaluation.

The **role-based prompt** produced a more domain-oriented response because the AI was instructed to behave as a computer-vision and machine-learning engineer.

The **structured prompt** produced one of the most useful responses because the required answer format was clearly specified.

The **constraint-based prompt** was particularly effective for practical engineering design. By specifying webcam usage, real-time requirements, lightweight models, publicly available datasets and hardware limitations, the AI generated a solution that was more realistic for a student project.

The step-by-step prompt helped organize the reasoning process and resulted in a systematic engineering pipeline.


# 9. Naïve vs Improved Prompts

| Aspect | Naïve Prompt | Improved Prompt |
|---|---|---|
| Problem Definition | General | Specific |
| Context | Very Limited | Project-Specific |
| Technical Requirements | Not Specified | Clearly Defined |
| Output Structure | Unspecified | Structured |
| Constraints | None | Explicit |
| Model Selection | Generic | Justified |
| Evaluation | Limited | Multiple Metrics |
| Deployment | Not Discussed | Included |
| Engineering Feasibility | Moderate | High |
| Overall Usefulness | Low | High |


# 11. Final Selected Prompting Technique

## Constraint-Based Structured Prompting

This technique was selected because the engineering problem requires:

- Specific hardware constraints
- Real-time operation
- Multiple spoofing attacks
- Suitable model selection
- Dataset requirements
- Evaluation metrics
- Deployment considerations
- Engineering feasibility

Combining **structure + constraints** generated the most practical and project-oriented response.


# 12. Refined / Final Prompt

> **Act as an expert computer-vision and machine-learning engineer and design a practical real-time face liveness detection system for my final-year engineering project, "ReasonTrace".**
>
> **Problem:** The system must distinguish a genuine live person from spoofing attacks such as printed photographs, mobile-screen attacks, and replayed videos using a normal webcam.
>
> **Requirements:**
>
> 1. Use only a normal webcam and commonly available computing hardware.
> 2. The system should operate close to real time.
> 3. Recommend suitable face-detection and liveness-detection approaches.
> 4. Suggest suitable publicly available datasets containing genuine and spoof samples.
> 5. Explain preprocessing and data augmentation.
> 6. Recommend a lightweight CNN/transfer-learning architecture and justify the choice.
> 7. Describe the training, validation and testing process.
> 8. Include accuracy, precision, recall, F1-score, FAR, FRR and EER as evaluation metrics.
> 9. Explain the complete deployment pipeline using appropriate computer-vision tools.
> 10. Discuss possible limitations, security weaknesses and improvements.
>
> **Present the answer using these sections:**
>
> - Problem Analysis
> - Objectives
> - System Architecture
> - Dataset
> - Preprocessing
> - Model Selection
> - Training
> - Testing
> - Evaluation Metrics
> - Real-Time Deployment
> - Limitations
> - Future Improvements
> - Expected Result
>
> Ensure that the proposed solution is technically realistic, implementable by an engineering student, and suitable for experimental validation.


### Validation Table

| Test Condition | Expected | Actual | Result |
|---|---|---|---|
| Genuine Face | LIVE | LIVE | Correct |
| Printed Photo | SPOOF | SPOOF | Correct |
| Mobile Screen | SPOOF | SPOOF | Correct |
| Replay Video | SPOOF | SPOOF | Correct |
| Low Light | LIVE/SPOOF | — | — |
| Unseen User | LIVE | — | — |


# RESULT

**The prompt for the above-mentioned engineering problem was executed successfully. Different prompting techniques were applied and compared. The results demonstrated that improved prompts produced better quality, accuracy, depth, clarity and engineering usefulness than the naïve prompt. The constraint-based structured prompting technique was selected as the most effective technique, and the final refined prompt was validated through an engineering-oriented evaluation plan.**
