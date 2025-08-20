Sentiment Analysis Web Application

This is a simple Sentiment Analysis Web App where users can paste or type any text (such as a tweet, review, or message) and instantly get its sentiment: Positive, Negative, or Neutral.

## Project Overview

- Frontend: A webpage with a text box, an "Analyze" button, and a result area.
- Backend: A Flask API that uses **TextBlob** (a pre-trained sentiment analysis model) to calculate sentiment.
- Deployment: Backend hosted on **Render**, frontend hosted on render using static website

##  Features

- Text input box for users to type/paste text.
- Analyze button to trigger sentiment analysis.
- Sentiment results displayed clearly.
- Color-coded results:
  - 🟢 Positive
  - 🔴 Negative
  - ⚪ Neutral
- API backend that processes text and returns sentiment in JSON format.

## Tech Stack

- Frontend: HTML, CSS, JavaScript
- Backend: Flask (Python)
- ML Model: [TextBlob] (rule-based sentiment polarity)
- Deployment: Render (backend)


1. **Frontend**:
   - User types text into a textarea and clicks "Analyze".
   - A POST request is sent to the backend API with the text.
https://sentiment-app-analysis-frontend.onrender.com


2. **Backend (Flask API)**:
   - Receives the text at the `/analyze` endpoint.
   - Uses TextBlob to calculate sentiment polarity:
     - Polarity > +0.1 → Positive
     - Polarity < -0.1 → Negative
     - Otherwise → Neutral
   - Returns the result as JSON:  
     ```json
     { "sentiment": "Positive" }
     ```
https://sentiment-app-analysis.onrender.com
