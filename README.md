# Audio Speech Recognition with OpenAI Whisper

This project demonstrates the development and evaluation of an Automatic Speech Recognition (ASR) model using OpenAI Whisper, focusing on two datasets: Gramvaani and Kathbath. The objective is to evaluate Whisper's performance on these datasets, with specific attention to Hindi speech recognition.

## 1. OpenAI Whisper
OpenAI Whisper is a pre-trained speech recognition model developed by OpenAI. It supports multiple languages and various model sizes (base, small, medium, and large), allowing users to balance accuracy and computational resources. Whisper's versatility makes it suitable for evaluating speech recognition capabilities on different datasets, particularly those focusing on Hindi speech.

## 2. Datasets
### 2.1 Gramvaani Dataset
The Gramvaani dataset is a large-scale open-source dataset designed for Indian languages. It contains audio recordings and corresponding text transcripts in Hindi, serving as a benchmark for evaluating Whisper's performance on Hindi speech recognition.

- **Content**: Audio recordings and corresponding text transcripts in Hindi.
- **Structure**: 
  - Audio files in WAV format.
  - Transcripts in text files.
- **Availability**: Publicly available on Zenodo [here](https://asr.iitm.ac.in/Gramvaani/NEW/GV_Eval_3h.tar.gz).

### 2.2 Kathbath Dataset
The Kathbath dataset contains audio recordings and transcripts in Hindi. It might focus on a specific domain or topic, providing an opportunity to evaluate Whisper's performance on targeted speech data.

- **Content**: Audio recordings and corresponding text transcripts in Hindi.
- **Structure**: 
  - Audio and transcript folders, with data in multiple Indian languages.
- **Availability**: [Google Drive Link](https://drive.google.com/drive/folders/1veTfb45_jG1JItYyE_tkc6M7Lk98ic3J?usp=share_link).

## 3. Code Walkthrough
This project includes code snippets demonstrating key operations for developing and testing the ASR model.

### 3.1 Importing Libraries
The code imports necessary libraries for interacting with the operating system, using the Whisper model, displaying progress bars, and calculating Word Error Rate (WER).

### 3.2 Defining Paths
Defines file paths for the audio data and reference transcripts. These paths should be updated according to the actual data location in Google Colab.

### 3.3 Load OpenAI Whisper Model
Loads the appropriate OpenAI Whisper model for transcription. You can choose the model size depending on your resources and performance requirements.

### 3.4 Transcribe Audio Files
Transcribes audio files from the defined Google Drive paths. Transcription results are stored in text files.

### 3.5 Calculate Word Error Rate (WER)
Calculates the Word Error Rate (WER) by comparing transcriptions with the corresponding reference text files to evaluate Whisper's performance.

## 4. Results
### 4.1 Gramvaani Dataset
The basic OpenAI Whisper model achieved a WER score of 112.2050 on the Gramvaani dataset. This result serves as a benchmark for evaluating Whisper's baseline performance on Hindi speech recognition.

### 4.2 Kathbath Dataset
Due to computational constraints, the Kathbath dataset was reduced in size for training and evaluation. Truncation of missing lines in the reference transcripts was required to ensure alignment with the hypothesis. The tiny Whisper model achieved a WER score of 3.4416 on the reduced Kathbath dataset.

## 5. Future Prospects
Potential future directions for this project include:
- **Training on the Kathbath Dataset**: With additional computational resources, further training of the Whisper model on Kathbath could lead to better performance.
- **Hyperparameter Tuning**: Adjusting learning rates, optimizers, and other parameters for optimal performance.
- **Ensemble Learning**: Combining predictions from multiple models to improve overall performance.
- **Language Model Integration**: Integrating Whisper with a language model to handle complex sentence structures and ambiguities.
- **Error Analysis**: Analyzing errors in the Kathbath dataset to identify weaknesses and inform further improvements.

## 6. Conclusion
This project provided an evaluation of the OpenAI Whisper model on the Gramvaani dataset and attempted training on the Kathbath dataset. Although training on Kathbath was limited by computational constraints, the project successfully demonstrated Whisper's capability in Hindi speech recognition.

## 7. Project Availability
The code for this project is available on GitHub [here](https://github.com/diptarup794/AudioSpeechRecognition). This allows for transparency, reproducibility, and potential collaboration on the project's development.
