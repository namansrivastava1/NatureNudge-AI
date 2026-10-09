# 🌿 NatureNudge AI — Less Scrolling, More Living

**An AI-powered outdoor adventure planner designed to help people disconnect from their screens and reconnect with nature.**

NatureNudge AI transforms free time into meaningful outdoor experiences. By combining personalized activity planning with open-weight AI models, the project aims to encourage people to explore their surroundings, observe nature, develop healthier digital habits, and spend more time in the real world.

> **Our philosophy:** Let technology inspire the adventure, then put the phone away and live it.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Problem Statement](#-problem-statement)
- [Our Solution](#-our-solution)
- [Key Features](#-key-features)
- [How It Works](#-how-it-works)
- [Technology Stack](#-technology-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Current Implementation](#-current-implementation)
- [Open-Source AI Integration](#-open-source-ai-integration)
- [Why Open Innovation Matters](#-why-open-innovation-matters)
- [Privacy and Data Handling](#-privacy-and-data-handling)
- [Future Roadmap](#-future-roadmap)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌱 Overview

NatureNudge AI is a nature-focused web application built around one simple idea: technology should help us experience more of the world, not keep us trapped in front of a screen.

Users can select their available time, surroundings, preferred interests, and desired activity intensity. The application then suggests an outdoor mission that fits their preferences.

Activities may include discovering different leaf shapes, observing birds from a respectful distance, finding natural patterns, exploring a safe walking route, or spending time caring for plants.

The project is being developed using HTML, CSS, JavaScript, Java, and open-weight AI technologies.

**Project theme:** Touch Grass — Build something with open-source AI that gets people off the screen and into the world.

## 🎯 Problem Statement

Digital devices are an important part of modern life, but spending too much time on screens can leave people with fewer opportunities to explore their surroundings and participate in outdoor activities.

Many people want to spend more time outside but struggle with simple questions:

- What can I do outdoors today?
- How can I make use of just 10–30 minutes of free time?
- What activities are possible in my immediate surroundings?
- How can I make outdoor time interesting without buying equipment?
- How can I develop a habit of exploring the real world?

Traditional activity planners may offer generic suggestions without considering an individual's time, interests, or environment.

NatureNudge AI aims to make outdoor exploration easier by turning these questions into personalized, actionable missions.

## 💡 Our Solution

NatureNudge AI acts as a personal outdoor adventure companion.

Instead of encouraging users to spend more time browsing an application, it helps them choose an activity, understand what to do, and head outside.

The intended experience follows four simple steps:

1. **Choose:** Select available time, surroundings, interests, and difficulty.
2. **Generate:** Receive an outdoor mission tailored to those preferences.
3. **Explore:** Complete the mission in the real world.
4. **Reflect:** Mark the adventure complete and track outdoor progress.

The goal is to make the digital interaction short, useful, and purposeful.

---

## ✨ Key Features

### 1. Personalized Adventure Generator

Users can customize their outdoor experience using a simple preference form.

Available settings include:

- **Time:** 10, 20, 30, or 60 minutes.
- **Environment:** Park or garden, neighborhood, college campus, backyard or balcony, or nature trail.
- **Interests:** Nature discovery, wildlife observation, outdoor photography, mindful walking, gardening, and outdoor creativity.
- **Difficulty:** Easy or moderate.

The current prototype selects activities from predefined examples. Integration with an open-weight language model is planned to enable dynamic mission generation.

### 2. Outdoor Mission Cards

Each mission is displayed in a dedicated card containing:

- Mission title
- Short description
- Suggested location
- Estimated duration
- Difficulty level
- Step-by-step instructions
- Mission completion control

The structured format makes activities easy to understand and complete without repeatedly checking the screen.

### 3. Outdoor Progress Dashboard

The application includes a progress dashboard designed to track:

- Total outdoor minutes logged
- Number of completed adventures
- Consecutive days with recorded adventures

Progress is stored using the browser's local storage, allowing it to persist across refreshes in the same browser.

These values represent user-recorded activity rather than independently verified outdoor time.

### 4. Nature-Inspired Interface

The website uses a nature-inspired visual design featuring:

- Earthy green and cream colors
- Clean layouts and rounded cards
- An illustrated landscape
- Responsive layouts for smaller screens
- Clear calls to action
- Accessible text-based mission instructions

The interface is designed to make planning feel simple rather than turning outdoor activity into another screen-heavy experience.

### 5. Local-First Experience

The frontend prototype does not require a database server or user account.

Mission history is stored locally in the browser. The planned AI architecture uses a locally running model to support privacy-conscious, offline mission generation.

Full offline AI support will depend on completing the backend integration and downloading the required model.

---

## 🔄 How It Works

### Planned system architecture

```text
              USER
                |
                v
       HTML / CSS / JavaScript
                |
                v
        Java Spring Boot API
                |
                v
          Ollama Runtime
                |
                v
       Open-Weight AI Model
                |
                v
       Generated Outdoor Mission
                |
                v
        Mission Card in Browser
                |
                v
      Real-World Outdoor Activity
                |
                v
       Local Progress Tracking
```

### Workflow explanation

**Step 1 — User input**

The user selects their time, environment, interest, and activity intensity.

**Step 2 — Request processing**

The Java backend will receive these preferences through an HTTP API endpoint and validate the submitted values.

**Step 3 — AI inference**

The backend will send a structured prompt to a locally running model through Ollama.

**Step 4 — Mission generation**

The model will generate an appropriate mission with a title, description, duration, and actionable steps.

**Step 5 — Frontend rendering**

JavaScript will display the generated mission in the existing interface.

**Step 6 — Outdoor exploration**

The user completes the activity away from the screen.

**Step 7 — Progress tracking**

The user confirms completion, and the application updates the local progress dashboard.

*Note: Steps involving the Java backend and AI inference describe the planned architecture; they are not connected in the current frontend-only prototype.*

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Website structure and semantic elements |
| CSS3 | Styling, responsive design, and layout |
| JavaScript | User interactions, mission rendering, and progress tracking |
| Java | Planned backend language |
| Spring Boot | Planned REST API framework |
| Ollama | Planned local model runtime |
| Qwen2.5 | Candidate open-weight language model |
| Browser localStorage | Local progress persistence |
| Git and GitHub | Version control and project collaboration |

### Why these technologies?

The frontend uses standard web technologies to keep the interface lightweight and easy to run.

Java and Spring Boot provide a structured way to build the backend and connect the interface to an AI model.

Ollama simplifies running supported open-weight models locally. Qwen2.5 is one candidate for generating outdoor missions, although the final model should be selected according to hardware requirements, output quality, and licensing.

---

## 📁 Project Structure

The initial frontend prototype uses the following structure:

```text
NatureNudge/
│
├── index.html
│   └── Main webpage and interface structure
│
├── style.css
│   └── Visual design and responsive layouts
│
├── script.js
│   └── Demo missions and frontend interactions
│
└── README.md
    └── Project documentation
```

The planned full-stack structure can later evolve into:

```text
NatureNudge/
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── backend/
│   ├── pom.xml
│   └── src/
│       └── main/
│           ├── java/
│           │   └── com/naturenudge/
│           │       ├── NatureNudgeApplication.java
│           │       ├── controller/
│           │       ├── service/
│           │       └── model/
│           └── resources/
│
├── README.md
└── .gitignore
```

The backend directory is a proposed future structure and must be created when the Java implementation begins.

---

## 🚀 Getting Started

### Prerequisites

For the current frontend prototype, you need:

- A modern web browser such as Chrome, Firefox, or Edge.
- A code editor such as Visual Studio Code.
- Git, if you want to clone and version the repository.

You do not need Java, Maven, Spring Boot, or Ollama to run the current demo.

### Installation

**1. Clone the repository**

Replace `YOUR_USERNAME` with your GitHub username.

```bash
git clone https://github.com/YOUR_USERNAME/NatureNudge.git
```

**2. Open the project directory**

```bash
cd NatureNudge
```

**3. Open the website**

Open `index.html` directly in your browser.

Alternatively, use the Live Server extension in Visual Studio Code for convenient local development.

**4. Generate your first mission**

- Select your available time.
- Choose your surroundings.
- Select an outdoor interest.
- Choose the activity intensity.
- Click **Generate my mission**.
- Review the instructions and try the activity outdoors.
- Mark it complete to update your progress.

### Testing progress persistence

After completing an adventure, refresh the browser.

Your recorded progress should remain available because the prototype uses browser local storage.

Clearing the browser's site data or switching to a different browser profile may remove or hide the saved progress.

---

## 🧪 Current Implementation

The project is currently at the frontend prototype stage.

| Component | Status |
|---|---|
| Responsive landing page | Implemented |
| Outdoor preference form | Implemented |
| Interest selection | Implemented |
| Demo mission generator | Implemented |
| Mission instruction cards | Implemented |
| Completion confirmation | Implemented |
| Local progress persistence | Implemented |
| Outdoor-minute tracking | Implemented using logged missions |
| Daily streak calculation | Implemented |
| Java Spring Boot backend | Planned |
| Ollama integration | Planned |
| Open-weight AI-generated missions | Planned |
| Verified activity tracking | Not implemented |

The current generator chooses from predefined mission examples. The interface includes a demo-mode indicator so that users do not mistake these examples for live AI output.

---

## 🤖 Open-Source AI Integration

The planned AI component will replace the predefined mission selection with dynamically generated activities.

### Proposed model

**Runtime:** Ollama

**Candidate model:** Qwen2.5 3B Instruct

Qwen2.5 is an open-weight language model family that can be used for instruction-following and structured text generation. Check the specific model's license and distribution terms before deployment.

A small model is a reasonable starting point for experimentation on a personal computer, but performance and memory requirements depend on the device.

### Example prompt

```text
You are NatureNudge AI, an outdoor activity planner.

Create one safe and engaging outdoor mission.

Available time: 20 minutes
Environment: College campus
Interest: Wildlife observation
Difficulty: Easy

Requirements:
1. Provide a short, engaging title.
2. Include a concise description.
3. Provide exactly three actionable steps.
4. Avoid activities that disturb wildlife or damage plants.
5. Do not require purchasing equipment.
6. Respect the user's available time.
7. Return a structured JSON response.
```

### Example response format

```json
{
  "title": "The Quiet Observer",
  "description": "Discover local wildlife without disturbing it.",
  "duration": 20,
  "difficulty": "Easy",
  "steps": [
    "Choose a safe place to observe from a distance.",
    "Watch for birds or insects without approaching them.",
    "Notice how wildlife interacts with its surroundings."
  ]
}
```

This is an illustrative response, not output from a connected model.

### Planned integration steps

1. Install Ollama and download a compatible open-weight model.
2. Create a Java Spring Boot application.
3. Build a REST endpoint that accepts validated activity preferences.
4. Send prompts to the local Ollama API.
5. Parse and validate the model response.
6. Return structured JSON to the browser.
7. Replace the demo generator with a JavaScript `fetch()` request.
8. Test model behavior, error handling, and offline operation.

Model output should be treated as untrusted input. The backend should validate generated JSON, constrain duration and instructions, and avoid exposing the local model service to untrusted networks.

---

## 🌍 Why Open Innovation Matters

Open innovation is a central design principle of NatureNudge AI.

### 1. Privacy and user control

Running inference locally can keep personal preferences and prompts on the user's own device instead of sending them to a third-party AI provider.

The current prototype also stores progress in browser local storage rather than a remote database.

### 2. Offline potential

After installing the application and downloading the required model, local inference can generate missions without an internet connection.

This is particularly useful in parks, gardens, and nature trails where connectivity may be unreliable.

The current frontend demo can run locally, but its Google Fonts import requires internet access for the external fonts. The full offline AI version remains a planned feature.

### 3. Model flexibility

An open-weight architecture makes it possible to experiment with compatible models, compare generation quality, adjust prompts, and customize behavior.

Different models can be evaluated for instruction quality, speed, hardware requirements, and licensing.

### 4. Reduced dependence on paid APIs

Local inference avoids commercial per-request AI API charges. However, running a model still consumes computing resources
