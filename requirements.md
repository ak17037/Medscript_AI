# MedScript AI – Requirements Specification

## 1. Overview
MedScript AI is an AI-powered clinical documentation and decision-support assistant designed to reduce the documentation burden on doctors while improving the accuracy and completeness of patient records. The system combines conversational AI, structured data capture, and multimodal analysis to support real-world clinical workflows.

## 2. Functional Requirements

### FR1: Patient Registration & Intake
- The system shall provide an introductory patient intake page.
- The system shall collect patient details including:
  - Name, age, gender, address
  - Contact information
  - Past medical history
  - Ongoing medications
  - Allergies
  - Lifestyle factors (smoking, alcohol, activity level)

### FR2: Conversation Capture
- The system shall capture live or recorded doctor–patient conversations.
- The system shall support both audio and text-based inputs.

### FR3: Medical Transcription
- The system shall transcribe conversations using a medical-grade speech-to-text model.

### FR4: Multimodal Symptom Analysis
- The system shall optionally capture patient facial and body data (with consent).
- The system shall analyze visual cues such as facial expressions, posture, and visible discomfort.
- The system shall combine visual signals with conversation context to improve documentation accuracy.

### FR5: AI Processing & Understanding
- The system shall extract medical entities (symptoms, vitals, diagnoses, medications).
- The system shall generate structured SOAP notes using AI.

### FR6: Human-in-the-Loop Review
- The system shall allow doctors to review, edit, and approve AI-generated notes.
- No clinical record shall be finalized without explicit doctor approval.

### FR7: Data Storage & Retrieval
- The system shall store patient profiles, encounters, notes, and reports.
- The system shall provide searchable access to patients and reports.

### FR8: Dashboard & Analytics
- The system shall display dynamic metrics:
  - Patients handled
  - Notes generated
  - Estimated time saved
  - AI confidence score

## 3. Non-Functional Requirements
- Security: Patient data must be protected and access-controlled.
- Scalability: The system should support multiple concurrent sessions.
- Usability: The interface should mirror real clinical workflows.
- Ethics: Explicit patient consent is required for visual analysis.

## 4. Constraints
- Prototype uses simulated or synthetic data.
- The system does not provide autonomous diagnosis.

## 5. Assumptions
- Doctors validate all AI outputs.
- Visual analysis is assistive, not diagnostic.
