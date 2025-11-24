# JARVIS
Jarvis is a Python script that provides desktop voice control. It uses pyttsx3 for audio output and speech_recognition for voice commands. Functions include checking time, opening websites (Google, YouTube), performing Wikipedia searches, and basic email sending via SMTP. It offers simple, hands-free interaction.
Jarvis - Personal AI Voice Assistant
This is a basic, desktop-based voice assistant script written in Python. It is capable of performing simple tasks like speaking, greeting, searching Wikipedia, opening common websites, playing local music, and sending emails via voice commands.
✨ Features
•	Voice Output: Uses the pyttsx3 library for text-to-speech conversion.
•	Voice Input: Uses the speechrecognition library to process microphone input and convert speech to text.
•	Contextual Greeting: Greets the user (Good Morning/Afternoon/Evening) based on the time of day.
•	Wikipedia Search: Fetches and reads a 2-sentence summary from Wikipedia.
•	Web Browsing: Opens YouTube, Google, and Stack Overflow in the default web browser.
•	System Interaction: Displays the current time and opens local applications (e.g., VS Code) and files (e.g., music).
•	Email Functionality: Sends emails using smtplib (requires configuration).
________________________________________
💻 Prerequisites
You must have Python installed on your system.
Installation
Install the required Python libraries using pip:
Bash
pip install pyttsx3 speechRecognition wikipedia webbrowser
(Note: datetime, os, and smtplib are built-in Python modules.)
⚠️ Operating System Dependencies
•	pyttsx3: On Windows, it uses the SAPI5 voice API, which is usually pre-installed.
•	speech Recognition: This library requires the PyAudio library to handle microphone input. Depending on your OS, installing PyAudio can be tricky.
o	Windows/Linux: You may need to install system dependencies (like build tools) before successfully installing PyAudio.
________________________________________
⚙️ Configuration
Before running the script, you need to make the following adjustments to the code:
1. Email Configuration (Mandatory for Email Feature)
The sendEmail function requires your email credentials and access settings:
•	Replace Placeholders:
Python
server.login('youremail@gmail.com', 'your-password') # Replace with your actual email and password/App Password
server.sendmail('youremail@gmail.com', to, content) # Replace with your actual email
•	Security: Using your direct password is highly discouraged for security reasons. For Gmail, you must:
1.	Enable 2-Factor Authentication on your Google Account.
2.	Generate an App Password for your Python application and use that instead of your main password.
2. File Path Configuration
The script uses hardcoded local file paths for music and the VS Code application. You must update these paths to match your system's directory structure:
Feature	Code Line	Action Required
Play Music	music_dir = 'D:\\Non Critical\\songs\\Favorite Songs2'	Update this path to the directory where your music files are stored.
Open VS Code	codePath = "C:\\Users\\Haris\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe"	Update this path to the location of the executable for VS Code (or any other application you wish to open).
________________________________________
▶️ How to Run
1.	Save the code as a Python file (e.g., jarvis.py).
2.	Open your command line or terminal.
3.	Navigate to the directory where you saved the file.
4.	Run the script:
Bash
python jarvis.py
The script will greet you ("I am Jarvis Sir...") and start listening for your commands.
________________________________________
🎤 Voice Commands
Here are the commands Jarvis is programmed to recognize:
Command Phrase	Action Performed
"Wikipedia [topic]"	Searches and speaks a summary of the topic.
"open youtube"	Opens YouTube in the default browser.
"open google"	Opens Google in the default browser.
"open stackoverflow"	Opens Stack Overflow in the default browser.
"play music"	Starts playing the first song in the configured music_dir.
"tell me the time"	Speaks the current system time.
"open code"	Launches the application specified by codePath (default is VS Code).
"email to shiv"	Prompts for content, then sends an email to the hardcoded recipient (harryyourEmail@gmail.com).
________________________________________
🛑 Stopping the Assistant
Since the script uses an infinite while True: loop, you must manually stop it:
•	Press Ctrl + C in the command line/terminal window where the script is running.

