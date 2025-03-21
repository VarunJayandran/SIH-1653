# Smart India Hackathon Workshop
# Date: 21/03/2025
## Register Number: 212224240179
## Name: VARUN J C 
## Problem Title
SIH 1653: Web based Selector-Applicant Simulation Software
## Problem Description
Background: Recruitment and Assessment Centre (RAC) under DRDO, Ministry of Defence carries out interviews for applications received against advertised vacancies and for promotion to next higher grade for scientific manpower inducted within DRDO. Description: The process of interviewing is a challenging task. An unbiased objective interviewing process helps identify the right talent. The basic process of an interview involves posing a set of questions by an interviewer and thereafter evaluating responses from candidates. Thus, the questions asked should be relevant and match the area/ expertise of the applicant and the responses should also be of relevance w.r.t. the question asked. Expected Solution: The proposed solution should provide experts as well as candidates a real life Board Room experience, starting with initial ice-breaking questions leading to in-depth techno-managerial (depending on the level of candidate) questions. It shall also be able to provide a quantifiable score for experts as well as the candidate for the relevancy of questions w.r.t. the area/ expertise of the applicant. Similarly, candidate responses should also be graded for relevancy w.r.t. the question asked, finally assisting in arriving at an overall score for the subject knowledge of the candidate and thus his/ her suitability against the advertised post.

## Problem Creater's Organization
Ministry of Defence

## Idea:

The core idea is to create a web-based, AI-enhanced simulation platform that emulates the DRDO RAC interview process, providing objective and quantifiable assessments of candidates. This platform aims to:

Standardize the interview process: Ensure consistency and fairness across all interviews.
Improve efficiency: Reduce the time and resources required for manual assessments.
Enhance objectivity: Minimize bias through automated relevancy and scoring.
Provide valuable data: Generate insights into candidate performance and interview effectiveness.
## Proposed Solution / Architecture Diagram:

Code snippet

graph LR
    A[User (Candidate/Expert)] --> B(Web Browser);
    B --> C(Load Balancer);
    C --> D{API Gateway};
    D --> E[User Service];
    D --> F[Interview Service];
    D --> G[NLP Service];
    D --> H[Scoring Service];
    E --> I[User Database];
    F --> J[Interview Database];
    G --> K[NLP Models];
    H --> L[Scoring Algorithm];
    F --> M[Real-time Communication Server];
    B --> M;
    K --> G;
    L --> H;

    subgraph Databases
        I;
        J;
    end

    subgraph Services
        E;
        F;
        G;
        H;
    end

    subgraph Infrastructure
        C;
        D;
        M;
    end

Explanation:

User (Candidate/Expert): Interacts with the platform through a web browser.
Web Browser: Provides the user interface.
Load Balancer: Distributes traffic across the API Gateway.
API Gateway: Routes requests to the appropriate microservices.
User Service: Manages user authentication, authorization, and profile data.
Interview Service: Handles interview creation, scheduling, and management.
NLP Service: Processes text data for relevancy assessment and sentiment analysis.
Scoring Service: Calculates scores based on relevancy and other factors.
User Database: Stores user profiles and credentials.
Interview Database: Stores interview questions, responses, and scores.
NLP Models: Contains pre-trained and custom NLP models.
Scoring Algorithm: Implements the logic for calculating scores.
Real-time Communication Server: Manages video and audio communication.

![Screenshot 2025-03-21 103147](https://github.com/user-attachments/assets/34962a44-f9b2-4e26-9fc0-b45937a31edc)

## Use Cases:

Candidate Registration:
Candidates create profiles with personal information, qualifications, and areas of expertise.
Expert Registration:
Experts create profiles with their areas of expertise and experience.
Interview Creation:
Experts create interview sessions, defining job roles and required skills.
The system suggests relevant questions based on the job role and candidate profiles.
Simulated Interview:
Candidates participate in real-time video/audio interviews.
Experts ask questions, and candidates provide responses.
Relevancy Assessment:
The system analyzes question and response relevancy using NLP.
Automated Scoring:
The system calculates scores based on relevancy, response quality, and other factors.
Report Generation:
The system generates reports with candidate scores and interview analysis.
Feedback and Improvement:
Experts and administrators can provide feedback on questions, and candidate responses to improve the systems accuracy.
Promotion Interviews:
The system can be used to perform promotion interviews for internal DRDO staff.


## Technology Stack:

Front-End:
React/Angular/Vue.js (JavaScript frameworks)
HTML5, CSS3
Back-End:
Python (Django/Flask) or Node.js (Express.js)
RESTful APIs
Database:
PostgreSQL or MySQL (relational)
MongoDB(Non-relational)
NLP:
Python (NLTK, spaCy, Transformers from Hugging Face)
Real-Time Communication:
WebRTC or WebSocket
Cloud Platform (Optional):
AWS, Azure, or Google Cloud Platform
Containerization:
Docker, Kubernetes.

![Screenshot 2025-03-21 103622](https://github.com/user-attachments/assets/f9d35ae9-fc24-4dac-a633-d15cdef12a21)

## Dependencies:

Operating System: Linux (Ubuntu, CentOS)
Programming Languages: Python, JavaScript
Web Servers: Nginx or Apache
Message Queue (Optional): RabbitMQ or Kafka
Machine Learning Libraries: TensorFlow or PyTorch
Cloud provider SDKs if cloud is used.
Third party API's for video and audio communication.


![Screenshot 2025-03-21 105226](https://github.com/user-attachments/assets/4d86511d-72b9-4564-9fbd-6efbc1842a61)
![Screenshot 2025-03-21 105245](https://github.com/user-attachments/assets/8a279860-7720-443b-8a7e-9b95527131c2)


## Key Considerations:

Security: Implement robust security measures to protect sensitive data.
Scalability: Design the system to handle a large number of users and interviews.
Usability: Ensure the platform is user-friendly for both candidates and experts.
Accuracy: Continuously improve the accuracy of NLP models and scoring algorithms.
Integration: Design the system for potential integration with other DRDO systems.
Compliance: Adhere to all relevant data privacy and security regulations.

