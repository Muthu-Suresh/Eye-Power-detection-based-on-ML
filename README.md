Eye Power Detection System using Voice Recognition and Machine Learning:
This project uses speech recognition, audio signal processing, and a neural network model to detect a person's eye power based on their pronunciation of letters from a Snellen chart. It is designed especially for accessibility, helping even illiterate individuals undergo a voice-based vision screening test.

Features:
Voice-based detection using Google Speech Recognition
Alphabet misinterpretation handling with mapping for real-world accuracy
Audio features extracted using MFCCs from Librosa
Trained Neural Network model for letter classification
Calculates LogMAR and eye power using Snellen chart-based analysis
Ideal for developing AI-powered assistive technology for eye testing

Technologies Used:
Python
TensorFlow / Keras
Librosa
SpeechRecognition (Google API)
scikit-learn
NumPy

How It Works:
Prepare Dataset
.wav files named with the first letter as the label (e.g., A1.wav, B2.wav) are loaded and processed using MFCC features.
Train Model
A neural network is trained using Keras to classify the spoken letters.
Live Recognition from Microphone
The user is asked to pronounce each row of letters from a Snellen chart.
Misinterpretation Mapping
Common voice-to-text errors (e.g., "yeah" for "A", "bee" for "B") are mapped to correct letters.
Eye Power Calculation
Based on detected vs actual letters in the Snellen chart, the logMAR and eye power (diopters) are computed.

Eye Power Formula:
logMAR = Total Rows - (Total Errors / 2)
Eye Power (diopters) = 1 - logMAR
If logMAR == 0, perfect vision is assumed (20/20 or 0 diopters)

