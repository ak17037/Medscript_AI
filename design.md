# MedScript AI – System Design Document 

## 1. Design Objectives
- Reduce manual documentation effort.
- Improve clinical note completeness.
- Support multimodal data inputs.
- Maintain ethical and responsible AI usage.

## 2. High-Level Architecture (AWS-Based)

Frontend (Web Application)
- Patient intake forms
- Live consultation interface
- Dashboard and reports

Backend (AWS Cloud)
- Amazon API Gateway for secure APIs
- AWS Lambda for backend logic
- Amazon Transcribe Medical for speech-to-text
- Amazon Bedrock for language understanding and note generation
- Amazon Rekognition for facial and body feature analysis
- Amazon DynamoDB for structured data storage
- Amazon S3 for media storage

## 3. Multimodal AI Design

### Conversational AI
- Processes doctor–patient dialogue.
- Extracts contextual clinical information.

### Visual Analysis
- Amazon Rekognition analyzes facial expressions and posture.
- Detects indicators such as pain, distress, or fatigue.
- Outputs are used as supporting signals, not diagnoses.

### Data Fusion
- AI combines conversational and visual inputs.
- Enhances SOAP note accuracy and completeness.

## 4. Data Model
- Patient Table: Demographics, medical history
- Encounter Table: Conversation metadata
- Notes Table: SOAP notes, confidence scores
- Metrics Table: Productivity analytics

## 5. Human-in-the-Loop Safeguards
- Doctor approval required before storage.
- Visual analysis results shown as suggestions only.
- Clear confidence indicators for AI outputs.

## 6. Security & Ethics
- IAM-based access control
- Consent-driven visual data usage
- No automated clinical decisions

## 7. Scalability & Future Extensions
- Multilingual support
- EHR integration (HL7 FHIR)
- Chronic disease monitoring
- Advanced clinical analytics

## 8. Prototype Limitations
- Visual analysis accuracy limited by camera quality.
- No real hospital integration at prototype stage
