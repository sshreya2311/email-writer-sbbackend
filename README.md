# AI Email Writer Assistant-

An AI-powered Chrome Extension that generates professional email replies directly inside Gmail using the Google Gemini API.

# Features-

-  Generate AI-powered email replies
-  Works directly inside Gmail
-  Professional tone generation
-  Spring Boot REST API backend
-  Dockerized backend
-  Deployed on Render
-  Google Gemini API integration

# Tech Stack-

# Frontend-
- Chrome Extension (Manifest V3)
- JavaScript
- HTML
- CSS

# Backend-
- Java
- Spring Boot
- Spring Web
- Spring WebFlux
- WebClient

# AI-
- Google Gemini API

# Deployment-
- Docker
- Render

# Version Control-
- Git
- GitHub
- 
# Project Structure-
Email-Writer-Assistant
│
├── frontend/
│   ├── manifest.json
│   ├── content-script.js
│   ├── popup.html
│   ├── popup.js
│   └── styles.css
│
├── backend/
│   ├── src/
│   ├── Dockerfile
│   ├── pom.xml
│   └── application.properties
│
└── README.md

# API Endpoint-

# Generate Email Reply

*POST*
/api/email/generate

# Sample Request

json
{
  "emailContent": "Thank you for your email.",
  "tone": "professional"
}

# Installation-

# Backend-

1. Clone the repository
`bash
git clone https://github.com/your-username/your-repository.git


2. Configure environment variables
GEMINI_URL
GEMINI_KEY


3. Run
bash
./mvnw spring-boot:run

# Chrome Extension-

1. Open Chrome
2. Go to `chrome://extensions`
3. Enable **Developer Mode**
4. Click **Load unpacked**
5. Select the extension folder

# Deployment-

Backend deployed on **Render**.

# Demo-

# GitHub Repository-

https://github.com/sshreya2311/email-writer-sbbackend.git

# Backend URL-

https://email-writer-sbbackend.onrender.com

> Note: The backend is a REST API. Opening the root URL in a browser may show a 404 because the primary endpoint is `POST /api/email/generate`.

