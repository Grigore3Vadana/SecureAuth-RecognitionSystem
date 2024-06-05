**SecureAuth-RecognitionSystem
**SecureAuth is an innovative security application that utilizes facial and voice recognition for user authentication. It allows users to register with their personal information, record a video of their face, and an audio file of their voice, and then authenticate using these recordings. This system provides a high level of security, ensuring that only authorized users can access the server.

Features

User Registration: Users can enter their first name, last name, and password, which are saved in a JSON file.
User Video Registration: Users can record a 3-second video, saved locally with a unique name.
User Audio Registration: Records a 5-second audio file, converted to text for authentication.
User Authentication: Authentication is performed through facial and voice recognition.
Server Connection: Authentication messages are sent to the server for confirmation.
Technologies Used

Python 3
Tkinter
OpenCV
PyAudio
SpeechRecognition
JSON
Installation
Ensure you have the following libraries installed:

bash
Copy code
pip install numpy opencv-python-headless tkinter speech_recognition
Running the Application

Save the application code in a client.ipynb file and run it using Jupyter Notebook or Jupyter Lab.
To run the authentication server, use the code from server.ipynb in a suitable Python environment.
Technical Details

Facial Recognition Model Training

We use the LBPHFaceRecognizer model from OpenCV, trained with frames extracted from the recorded video, converted to grayscale.
Facial Recognition

The trained model is used to predict the user's identity, with a confidence threshold set at 70% for successful authentication.
Voice Recognition

We use Google Speech Recognition to convert the recorded audio into text, which is then compared to the stored password.
License
This project is protected by copyright and is not available under any public license. All rights are reserved. No part of this project may be reproduced, distributed, or transmitted in any form or by any means, without prior written permission from the author.
