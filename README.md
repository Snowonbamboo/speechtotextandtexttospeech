# speechtotextandtexttospeech

The first goal is to implement a speech to text program. To accomplish this I use pygsr, a Google speech to text API for python. Below are the installation steps. I used terminal on Mac. These are the steps I took to get it working on Mac. Some of the steps may not be necessary

Reference link for steps 1 and 2: https://people.csail.mit.edu/hubert/pyaudio/

STEP ONE: Open Virtual environemnt in the terminal 

1) cd 
2) venv
3) virtualenv env
4) cd env
5) source ./bin/activate
6) pip install SpeechRecognition
7) python
8) import speech_recognition
9)^D

Step two: install speech recognition 
1) pip install pyaudio
2) pip install pygsr

Step three: test in the virtual environment 
1) touch 1.py
2) vi 1.py
3) python 1.py 

10. Run the script from the http://people.csail.mit.edu/hubert/git/pyaudio.git website.
The following code was found on the Python Tutorial Website.

<pre><code>
#!/usr/bin/env python3
# Requires PyAudio and PySpeech.

import speech_recognition as sr

# Record Audio
r = sr.Recognizer()
with sr.Microphone() as source:
    print("Say something!")
    audio = r.listen(source)

# Speech recognition using Google Speech Recognition
try:
    # for testing purposes, we're just using the default API key
    # to use another API key, use `r.recognize_google(audio, key="GOOGLE_SPEECH_RECOGNITION_API_KEY")`
    # instead of `r.recognize_google(audio)`
    print("You said: " + r.recognize_google(audio))
except sr.UnknownValueError:
    print("Google Speech Recognition could not understand audio")
except sr.RequestError as e:
    print("Could not request results from Google Speech Recognition service; {0}".format(e))
</pre></code>

