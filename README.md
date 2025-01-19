# PitchHack-Chatbot

This project leverages Google Colab and the Gemini API to create an interactive learning experience. It combines video course content, PDF materials, and AI to answer student questions and generate quiz questions for instructors.

## Features

- **AI Tutor:** Answers student questions based on the provided course script and PDF material.
- **Quiz Generator:** Creates quiz questions with varying difficulty levels for instructors to assess student understanding.
- **Integrated Environment:** Utilizes Google Colab for seamless execution and collaboration.

## How it Works

1. **Data Input:** The project takes a video course script (extracted using Gladia.io API from a vide), a PDF document, and a user question as input.
2. **AI Processing:** It uses the Gemini API to understand the context and generate relevant answers and quiz questions.
3. **Output:** Provides answers to user questions and suggests quiz questions with answers, difficulty levels, and assessment value.

## Setup and Usage

1. **Google Colab:** Open the provided Colab notebook.
2. **API Keys:**
    - Obtain a Gladia.io API key for audio transcription and store it in Colab userdata under the key 'Gladia.io'.
    - Obtain a Google Gemini API key and store it in Colab userdata under the key 'GOOGLE_API_KEY'.
3. **Data Upload:** Upload your video course (MP4 format) and PDF document to your Google Drive. Update the `video_path` and `pdf_path` variables in the notebook with the correct file paths.
4. **Execution:** Run the notebook cells sequentially. The code will:
    - Extract text from the PDF using PyPDF2.
    - Convert the video to audio (MP3 format) using pydub.
    - Transcribe the audio using the Gladia.io API.
    - Query the Gemini API with the course script, PDF text, and user question to generate an answer.
    - Generate quiz questions using the Gemini API based on the course content.
5. **Results:** View the AI tutor's response to the user question and the suggested quiz questions in the output.

## Dependencies

- Python 3
- PyPDF2
- pydub
- requests
- openai
- google-generativeai

You can install these dependencies using `pip install` within the Colab notebook. Refer to the notebook for specific installation commands.

## Notes

- Ensure you have the necessary permissions to access the Google Drive files.
- This project is intended for educational purposes and research.
- Refer to the API documentation for usage limits and terms of service.
