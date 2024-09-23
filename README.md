# Note:
We have used win32 for this project but later realised that it only supports windows but not macOS. So for now our project does not support macOS. However as its easy to implement for macOS, we will release it after midsems.

# LearnForge
Introducing a personalized AI-powered learning assistant designed to help users efficiently master any topic. By assessing users' prior knowledge and time availability, the assistant curates a tailored roadmap of top learning resources. It generates a structured schedule,provides best resources from the web, provides explanatory videos, and offers customized tests to evaluate comprehension. With continuous feedback and strategies for deeper understanding, this app fosters an engaging and adaptive learning experience.

YouTube link : https://youtu.be/21PAZAvpKEw

This project is designed to generate PowerPoint slides, voice explanations, and video presentations from a given topic and subtopic using the Groq API for natural language processing.

# Features:

1)Slide Generation: Automatically create PowerPoint slides on a given topic/subtopic.

2)Audio Explanation: Generate audio explanations for each slide using the gTTS library.

3)Video Creation: Convert PowerPoint slides into images and create a synchronized video using the moviepy library.

4)MCQ Test: Generate multiple-choice questions (MCQs) for testing knowledge on the topic.

5)PDF Generation: Generate detailed explanation and example and stores it to local disk as a PDF for in depth learning.

# Technologies Used:

-Python

-Flask: For web-based interaction and user interface.

-Groq: For generating text content (slides and MCQs).

-gTTS: For converting text to speech (audio explanations).

-moviepy: For combining slides and audio into video.

-FPDF: For generating PDFs with explanations.

-PowerPoint COM (via comtypes): For converting .pptx slides into images (Windows only).

# Installation:

1)Clone the repository:https://github.com/YashGupta2106/LearnForge

2)Install the required dependencies:  pip install -r requirements.txt

3)Ensure that you have Microsoft PowerPoint installed for slide generation.


# Prerequisites

Python 3.11

# Required libraries:

-pip install flask gtts moviepy fpdf comtypes groq

(For PowerPoint COM automation, ensure you have PowerPoint installed (Windows only)).

# Project Setup:

1)Clone the repository using :

git clone https://github.com/YashGupta2106/LearnForge

2)cd project-name

3)Install the dependencies:

pip install -r requirements.txt

4)Set up the Groq API by configuring your API key. Replace placeholder keys with your credentials in the code in line number 35 in place of your_api_key.

# Usage:

1)Run the Flask Application:

python app.py

2) Navigate to the local host link generated in the terminal.

# Key Functions:

1) generate_slides(): Generates a list of slide content based on the topic and subtopic using Groq.

2) create_ppt(): Converts the generated slides into a .pptx PowerPoint file.

3) convert_pptx_to_images(): Converts the PowerPoint slides into individual images.

4) generate_voice_explanations(): Generates voice explanations for each slide using gTTS.

5) create_video(): Combines the images and audio into a final video file.

6) generate_mcq_questions(): Generates multiple-choice questions for the given topic using Groq.

7) generate_pdf(): You can also generate detailed PDF Explanation for any topic by calling the generate_pdf function.

# Notes:

Windows Only(For now): PowerPoint COM automation (for converting .pptx slides to images) only works on Windows systems with PowerPoint installed.

Groq API: Ensure that Groq is properly configured for text generation.

# Contributing:
Feel free to submit issues or pull requests to improve the project.

# Contributors:
Aaryan Antala, Ramya Parsania, Ansh Gupta, Yash Gupta


