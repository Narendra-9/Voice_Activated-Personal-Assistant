# Voice-Activated Personal Assistant

This is a Python-based voice-activated personal assistant named Jarvis. It can perform a variety of tasks based on voice commands, such as web browsing, fetching information from Wikipedia, playing music, opening applications, and sending emails. The assistant uses several libraries and APIs to achieve these functionalities.

## Features

- **Voice Recognition**: Uses Google's Web Speech API through the `SpeechRecognition` library to convert speech input to text.
- **Text-to-Speech**: Uses the `pyttsx3` library to convert text responses into speech.
- **Wikipedia Integration**: Fetches summaries of Wikipedia articles using the `wikipedia` library.
- **Web Browsing**: Opens specified websites in the default web browser using the `webbrowser` library.
- **Music Playback**: Plays music from a specified directory using the `os` library.
- **Time Reporting**: Tells the current time using the `datetime` library.
- **Application Launching**: Opens specified applications (e.g., Visual Studio Code) using the `os` library.
- **Email Sending**: Sends emails using Gmail's SMTP server via the `smtplib` library.

## Installation

1. **Clone the Repository**
    ```bash
    git clone https://github.com/your-username/voice-activated-assistant.git
    cd voice-activated-assistant
    ```

2. **Install Dependencies**

   Before installing dependencies, ensure you have Python and pip installed. Then, install the dependencies listed in `requirements.txt`:
   
   ```bash
   pip install -r requirements.txt
   ```

3. **Configuration**

   Before running the script, make the following changes in `assistant.py` according to your setup:

   - **Music Directory**: Update `music_dir` variable to the path where your music files are located.
     ```python
     music_dir = "D:\\Songs\\Favorite songs"
     ```

   - **Email Configuration**: Update the email address and password in the `sendEmail` function with your own Gmail credentials. Ensure that you allow less secure apps to access your Gmail account if you are not using two-factor authentication.
     ```python
     def sendEmail(to, content):
         server = smtplib.SMTP('smtp.gmail.com', 587)
         server.starttls()
         server.login('your_email@gmail.com', 'your_password')
         server.sendmail('your_email@gmail.com', to, content)
         server.close()
     ```

4. **Usage**

   - **Run the Script**
     ```bash
     python assistant.py
     ```

   - **Commands**
     - **Wikipedia Search**: Say "Wikipedia" followed by the search term.
     - **Open Websites**: Say "open YouTube", "open Google", or "open StackOverflow".
     - **Play Music**: Say "play music".
     - **Tell Time**: Say "what's the time".
     - **Open Application**: Say "open code" to open Visual Studio Code.
     - **Send Email**: Say "send email", provide the content, and then the recipient's email address.

## Contributing

Feel free to fork this repository, make changes, and submit pull requests. Any contributions are welcome!
