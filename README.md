# ShivMani-Echo
This is my personal AI Desktop voice assistant using python and speech Recognition

First, make sure you have all the requirements listed in the "Requirements" section.

The easiest way to install this is using pip install SpeechRecognition.

Otherwise, download the source distribution from PyPI, and extract the archive.

In the folder, run python setup.py install.


Requirements
To use all of the functionality of the library, you should have:

Python 2.6, 2.7, or 3.3+ (required)
PyAudio 0.2.11+ (required only if you need to use microphone input, Microphone)
PocketSphinx (required only if you need to use the Sphinx recognizer, recognizer_instance.recognize_sphinx)
Google API Client Library for Python (required only if you need to use the Google Cloud Speech API, recognizer_instance.recognize_google_cloud)
FLAC encoder (required only if the system is not x86-based Windows/Linux/OS X)
The following requirements are optional, but can improve or extend functionality in some situations:

On Python 2, and only on Python 2, some functions (like recognizer_instance.recognize_bing) will run slower if you do not have Monotonic for Python 2 installed.
If using CMU Sphinx, you may want to install additional language packs to support languages like International French or Mandarin Chinese.

Python
The first software requirement is Python 2.6, 2.7, or Python 3.3+. This is required to use the library.

PyAudio (for microphone users)
PyAudio is required if and only if you want to use microphone input (Microphone). PyAudio version 0.2.11+ is required, as earlier versions have known memory management bugs when recording from microphones in certain situations.

If not installed, everything in the library will still work, except attempting to instantiate a Microphone object will raise an AttributeError.

The installation instructions on the PyAudio website are quite good - for convenience, they are summarized below:

On Windows, install PyAudio using Pip: execute pip install pyaudio in a terminal.
On Debian-derived Linux distributions (like Ubuntu and Mint), install PyAudio using APT: execute sudo apt-get install python-pyaudio python3-pyaudio in a terminal.
If the version in the repositories is too old, install the latest release using Pip: execute sudo apt-get install portaudio19-dev python-all-dev python3-all-dev && sudo pip install pyaudio (replace pip with pip3 if using Python 3).
On OS X, install PortAudio using Homebrew: brew install portaudio. Then, install PyAudio using Pip: pip install pyaudio.
On other POSIX-based systems, install the portaudio19-dev and python-all-dev (or python3-all-dev if using Python 3) packages (or their closest equivalents) using a package manager of your choice, and then install PyAudio using Pip: pip install pyaudio (replace pip with pip3 if using Python 3).
PyAudio wheel packages for common 64-bit Python versions on Windows and Linux are included for convenience, under the third-party/ directory in the repository root. To install, simply run pip install wheel followed by pip install ./third-party/WHEEL_FILENAME (replace pip with pip3 if using Python 3) in the repository root directory.

PocketSphinx-Python (for Sphinx users)
PocketSphinx-Python is required if and only if you want to use the Sphinx recognizer (recognizer_instance.recognize_sphinx).

PocketSphinx-Python wheel packages for 64-bit Python 2.7, 3.4, and 3.5 on Windows are included for convenience, under the third-party/ directory. To install, simply run pip install wheel followed by pip install ./third-party/WHEEL_FILENAME (replace pip with pip3 if using Python 3) in the SpeechRecognition folder.

On Linux and other POSIX systems (such as OS X), follow the instructions under "Building PocketSphinx-Python from source" in Notes on using PocketSphinx for installation instructions.

Note that the versions available in most package repositories are outdated and will not work with the bundled language data. Using the bundled wheel packages or building from source is recommended.

See Notes on using PocketSphinx for information about installing languages, compiling PocketSphinx, and building language packs from online resources. This document is also included under reference/pocketsphinx.rst.

Google Cloud Speech Library for Python (for Google Cloud Speech API users)
Google Cloud Speech library for Python is required if and only if you want to use the Google Cloud Speech API (recognizer_instance.recognize_google_cloud).

If not installed, everything in the library will still work, except calling recognizer_instance.recognize_google_cloud will raise an RequestError.

According to the official installation instructions, the recommended way to install this is using Pip: execute pip install google-cloud-speech (replace pip with pip3 if using Python 3).
