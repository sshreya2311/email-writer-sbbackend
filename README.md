#  AI Email Writer

An AI-powered **Chrome Extension** that generates professional email replies directly inside **Gmail** using the **Google Gemini API**.

The application combines a Chrome Extension frontend with a **Java Spring Boot REST API backend**, enabling users to generate context-aware email responses quickly and efficiently.

##  Features

*  Generate AI-powered email replies
*  Works directly inside Gmail
*  Generate professional and context-aware responses
*  Spring Boot REST API backend
*  Google Gemini API integration
*  Dockerized backend
*  Backend deployed on Render

##  Tech Stack

### Frontend

* Chrome Extension — Manifest V3
* JavaScript
* HTML
* CSS

### Backend

* Java
* Spring Boot
* Spring Web
* Spring WebFlux
* WebClient

### AI

* Google Gemini API

### Deployment

* Docker
* Render

### Version Control

* Git
* GitHub

##  Architecture

```text
                 ┌─────────────────────┐
                 │       Gmail         │
                 │                     │
                 │  Email Composition  │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │  Chrome Extension   │
                 │                     │
                 │ HTML / CSS / JS     │
                 └──────────┬──────────┘
                            │
                     HTTP POST Request
                            │
                            ▼
                 ┌─────────────────────┐
                 │   Spring Boot API   │
                 │                     │
                 │ Java + WebFlux      │
                 │ WebClient           │
                 └──────────┬──────────┘
                            │
                       API Request
                            │
                            ▼
                 ┌─────────────────────┐
                 │   Google Gemini     │
                 │         API         │
                 └──────────┬──────────┘
                            │
                     Generated Reply
                            │
                            ▼
                 ┌─────────────────────┐
                 │  Chrome Extension   │
                 │                     │
                 │ Generated Response  │
                 └─────────────────────┘
```

##  Project Structure

```text
email-writer-assistant/
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
```

##  API

### Generate Email Reply

**Endpoint**

```http
POST /api/email/generate
```

**Request**

```json
{
  "emailContent": "Thank you for your email.",
  "tone": "professional"
}
```

The backend processes the request, sends the relevant prompt to the Google Gemini API, and returns the generated email response.

##  Local Installation

### Prerequisites

* Java 17+
* Maven
* Google Chrome
* Google Gemini API key
* Git

### 1. Clone the Repository

```bash
git clone https://github.com/sshreya2311/email-writer-sbbackend.git
cd email-writer-sbbackend
```

### 2. Configure Environment Variables

Configure the required Gemini API credentials:

```text
GEMINI_URL=your_gemini_api_url
GEMINI_KEY=your_gemini_api_key
```

> Never commit API keys or other sensitive credentials to GitHub.

### 3. Run the Backend

Using Maven:

```bash
./mvnw spring-boot:run
```

On Windows:

```bash
mvnw.cmd spring-boot:run
```

The Spring Boot application will start on the configured port.

##  Install the Chrome Extension

1. Open Google Chrome.
2. Navigate to:

```text
chrome://extensions
```

3. Enable **Developer Mode**.
4. Click **Load unpacked**.
5. Select the `frontend` directory.
6. Open Gmail and use the extension to generate email replies.

##  Deployment

The Spring Boot backend is containerized using **Docker** and deployed on **Render**.

### Backend

**Live Backend:**
https://email-writer-sbbackend.onrender.com

The backend is a REST API, so opening the root URL directly in a browser may return a **404 response**. The primary functionality is available through:

```http
POST /api/email/generate
```

##  Project Links

### GitHub Repository

https://github.com/sshreya2311/email-writer-sbbackend

### Live Backend

https://email-writer-sbbackend.onrender.com

##  Future Enhancements

* Support for multiple email tones such as friendly, formal, concise, and persuasive
* Email summarization
* Personalized AI-generated responses
* Support for additional email platforms
* User authentication
* Custom user preferences
* Improved prompt engineering
* Production-ready monitoring and logging



