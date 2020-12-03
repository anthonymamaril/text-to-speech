# text-to-speech

import io
import pygame
from gtts import gTTS

def speak (text):
    with io.BytesIO() as file:
        gTTS(text=text, lang="en").write_to_f(file)
        file.seek(0)

        pygame.mixer.init()
        pygame.mixer.music.load(file)
        pygame.mixer.music.play()
        while pygame.mixer.music.get_busy():
            continue

if _name_ == '_main_':
    print("what should I say?")
    text = input("  >> ")
    speak(text)
import io
import pygame
from gtts import gTTS

def speak (text):
    with io.BytesIO() as file:
        gTTS(text=text, lang="en").write_to_f(file)
        file.seek(0)

        pygame.mixer.init()
        pygame.mixer.music.load(file)
        pygame.mixer.music.play()
        while pygame.mixer.music.get_busy():
            continue

if _name_ == '_main_':
    print("what should I say?")
    text = input("  >> ")
    speak(text)
