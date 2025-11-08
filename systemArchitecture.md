# System Architecture — Access Lagos

## 1. Overview
**Access Lagos** is a digital transformation of the Lagos State Employment Trust Fund (LSETF), built to make government funding, training, and job opportunities accessible and transparent for every Lagosian.  
It connects users with verified programs through a secure, scalable, and AI-assisted web platform.

---

## 2. Architecture Components

### **Frontend**
- Built with **React** and **Tailwind CSS**.  
- Provides an intuitive interface for discovering programs, applying for loans, and tracking progress.  
- Communicates with backend APIs using **HTTPS (REST)** calls.  
- Deployed on **Vercel** for scalability and automatic updates.

### **Backend**
- Developed with **Node.js (Express framework)**.  
- Handles all business logic: authentication, application review, AI recommendations, and notifications.  
- Integrates with external APIs (e.g., LASRRA for identity verification).  
- Uses **JSON Web Tokens (JWT)** for secure login and role-based access control.  

### **Database**
- **PostgreSQL** database for structured storage of users, programs, mentors, and applications.  
- Indexed queries improve performance with large data volumes.  
- All transactions logged for transparency and audit tracking.  

### **AI Eligibility Engine**
- Uses **LangChain** to recommend suitable programs based on user profiles.  
- Processes simple natural language input (e.g., “I’m a small business owner”) to suggest relevant funding or training.  

### **External Integrations**
- **LASRRA API** for identity verification.  
- **SendGrid** for email notifications.  
- **Google Analytics** for usage tracking and performance metrics.  

---

## 3. Communication Flow
1. User opens the Access Lagos web portal (React frontend).  
2. User fills out a profile and submits an application form.  
3. Frontend sends form data to backend API via HTTPS.  
4. Backend validates and stores information in PostgreSQL.  
5. AI Eligibility Engine processes user data and returns recommendations.  
6. User receives updates and notifications via email (SendGrid).  
7. Admin dashboards display aggregated analytics and impact metrics.  

---

## 4. Feasibility & Technical Justification
- **Scalable:** Node.js handles multiple concurrent users efficiently.  
- **Secure:** Encrypted connections (HTTPS) and JWT authentication protect user data.  
- **Modular:** Each service (frontend, backend, AI, database) can be updated independently.  
- **Cloud-ready:** Containerized using Docker and deployable on AWS or Azure.  

---

## 5. System Diagram (Text Version)
