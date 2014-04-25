GLanguageServices
=================

Bash scripts for taking advantage of the following Google services on Linux
Speech to Text, Text to Speech, and Language Translation

The executable script names
stt - Speech to Text (requires sox and cUrl are installed)
tts - Text to Speech (requires mplayer)
translate - Language Translation (requires cUrl)


Language codes
http://en.wikipedia.org/wiki/List_of_ISO_639-1_codes


Usage
=====

## stt

stt [-l language] [-f file.flac]
Records voice audio from the microphone, and outputs transcribed text. (requires sox)

-l    Specify a language code. Default is en_US (English).
-f    Transcribe a 16000Hz flac instead of recording from microphone.

Known Bugs:
May output error if it cannot recognize speech.
Google voice recognition doesn't like audio files over 14 seconds.


## tts

tts [-l language] text to speak
Takes text and plays it through the speakers as audio. (requires mplayer)

-l    Specify a language code. Default is en_US (English).

Known Bugs:
None.


## translate

translate [-l languageinput] -o languageoutput text to translate
Translates text from one language to another.

-l    Language of text being input.
-o    Language of text to output.

Known Bugs:
Only accepts one sentence at a time.
