# LearnForge
Introducing a personalized AI-powered learning assistant designed to help users efficiently master any topic. By assessing users' prior knowledge and time availability, the assistant curates a tailored roadmap of top learning resources. It generates a structured schedule, provides explanatory videos, and offers customized tests to evaluate comprehension. With continuous feedback and strategies for deeper understanding, this app fosters an engaging and adaptive learning experience.


This project is designed to generate PowerPoint slides, voice explanations, and video presentations from a given topic and subtopic using the Grok API for natural language processing.

Features
Slide Generation: Automatically create PowerPoint slides on a given topic/subtopic.
Audio Explanation: Generate audio explanations for each slide using the gTTS library.
Video Creation: Convert PowerPoint slides into images and create a synchronized video using the moviepy library.
MCQ Test: Generate multiple-choice questions (MCQs) for testing knowledge on the topic.
Technologies Used
Python
Flask: For web-based interaction and user interface.
Grok: For generating text content (slides and MCQs).
gTTS: For converting text to speech (audio explanations).
moviepy: For combining slides and audio into video.
FPDF: For generating PDFs with explanations.
PowerPoint COM (via comtypes): For converting .pptx slides into images (Windows only).
Installation
Prerequisites
Python 3.x
Required libraries:
bash
Copy code
pip install flask gtts moviepy fpdf comtypes groq
For PowerPoint COM automation, ensure you have PowerPoint installed (Windows only).
Project Setup
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/project-name.git
cd project-name
Install the dependencies:

bash
Copy code
pip install -r requirements.txt
Set up the Grok API by configuring your API key. Replace placeholder keys with your credentials in the code where groq.chat.completions.create() is used.

Usage
Run the Flask Application:

bash
Copy code
python app.py
Generating Slides and Video:

Navigate to the URL path /generate_slides/<topic>/<subtopic>/<level>.
This will generate PowerPoint slides, convert them to images, generate audio explanations, and combine them into a video presentation.
Viewing the Generated Video:

After generating the video, you will be redirected to the /play_video/<topic>/<subtopic> route, where the video will be displayed.
Taking an MCQ Test:

Navigate to /mcq_test/<topic>/<subtopic> to take a test generated from Grok.
Key Functions
generate_slides(topic, subtopic): Generates a list of slide content based on the topic and subtopic using Grok.
create_ppt(slides, output_file): Converts the generated slides into a .pptx PowerPoint file.
convert_pptx_to_images(pptx_path, images_folder): Converts the PowerPoint slides into individual images.
generate_voice_explanations(slide_contents, audio_folder): Generates voice explanations for each slide using gTTS.
create_video(images_folder, audio_folder, output_video): Combines the images and audio into a final video file.
generate_mcq_questions(topic, subtopic): Generates multiple-choice questions for the given topic using Grok.
PDF Roadmap Generation
You can also generate detailed PDF roadmaps for any topic by calling the generate_pdf function.

bash
Copy code
pdf_filename = generate_pdf(subtopic, topic, level)
Notes
Windows Only: PowerPoint COM automation (for converting .pptx slides to images) only works on Windows systems with PowerPoint installed.
Grok API: Ensure that Grok is properly configured for text generation.
Contributing
Feel free to submit issues or pull requests to improve the project.

License
This project is licensed under the MIT License.
