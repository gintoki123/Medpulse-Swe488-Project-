# MediPulse 2.0: Advanced AI Healthcare Companion

## Project Overview

**MediPulse 2.0** is an advanced, AI-powered healthcare companion designed to provide users with quick, accurate, and helpful health-related information. It features a chat interface for health Q&A, integrated health tools (like a BMI calculator and water tracker), and a focus on user privacy by storing data locally.

This project was developed as a demonstration of modern front-end web development combined with powerful external Language Model APIs.

## Features

*   **AI-Powered Chat:** Instant answers to health queries using a large language model.
*   **Integrated Health Tools:** BMI Calculator, Water Intake Tracker, Health Tips, First Aid instructions, and a Symptom Checker.
*   **User Interface:** Clean, responsive design with dark mode and sound toggles.
*   **Local Storage:** User settings and chat history are stored locally in the browser for privacy.

## Technologies Used

*   **Frontend:** HTML5, CSS3, JavaScript (ES6+)
*   **Styling:** Custom CSS (`css/style.css`)
*   **External API:** OpenRouter (using an OpenAI-compatible endpoint) for the core AI functionality.

## Setup and Installation

Follow these steps to get a copy of the project up and running on your local machine.

### 1. Clone the Repository

If you are using Git, clone the repository to your local machine:

```bash
git clone [YOUR_REPOSITORY_URL]
cd medipulse_project
```

If you received the project as a ZIP file, simply extract the contents to a folder named `medipulse_project`.

### 2. API Key Configuration

The application requires an API key to function. We have configured the project to use the **OpenRouter API** due to its reliability and compatibility.

1.  **Get an OpenRouter API Key:** Sign up for an account on [OpenRouter](https://openrouter.ai/) and generate a new API key.
2.  **Update `script.js`:** Open the file `js/script.js` in a text editor.
3.  Locate the following lines (around line 31) and replace the placeholder key with your actual OpenRouter API key:

    ```javascript
    // js/script.js
    const API_KEY = "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"; // REPLACE THIS WITH YOUR KEY
    const API_URL = "https://openrouter.ai/api/v1/chat/completions";
    ```

    *Note: The key provided above is a placeholder and will not work. You must use your own valid key.*

### 3. How to Run the Project (Required for University Submission)

Since this is a static web application, you must run it using a local web server to ensure all files (especially the JavaScript API calls) load correctly.

#### Option A: Using VS Code Live Server (Recommended)

1.  Install the **Live Server** extension by Ritwick Dey in Visual Studio Code.
2.  Right-click on the `index.html` file.
3.  Select **"Open with Live Server"**.
4.  Your default browser will open the application at a local address (e.g., `http://127.0.0.1:5500/index.html`).

#### Option B: Using Python's Simple HTTP Server

If you do not use VS Code, you can use Python's built-in web server:

1.  Open your terminal or command prompt.
2.  Navigate to the project directory: `cd medipulse_project`
3.  Run the server command:
    ```bash
    python3 -m http.server 8000
    ```
4.  Open your web browser and navigate to: `http://localhost:8000`

## Project Structure

The project follows a standard structure for a simple web application:

```
medipulse_project/
├── index.html          # Main application file
├── README.md           # This file
├── css/
│   └── style.css       # All custom styles
├── js/
│   ├── script.js       # Core application logic and API calls
│   ├── api_optimizations.js
│   ├── text_to_speech.js
│   ├── pdf_export.js
│   └── language_support.js
└── assets/
    ├── medipulse-icon.png
    └── robot-icon.png
```

## Disclaimer

MediPulse is not a substitute for professional medical advice, diagnosis, or treatment.** Always seek the advice of your physician or other qualified health provider with any questions you may have regarding a medical condition. The information provided by this application is for informational purposes only.
