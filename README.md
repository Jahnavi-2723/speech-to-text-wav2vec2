

# 🎤 Speech-to-Text with Wav2Vec2.0

This project demonstrates **automatic speech recognition (ASR)** using Facebook's **Wav2Vec2.0** pre-trained model.  
Given an input `.wav` audio file, the model transcribes the spoken content into text.

---

## 📋 Problem Statement and Objective

- **Problem Statement:**  
  Develop a speech-to-text transcription system using the Wav2Vec2.0 model.
  
- **Objective:**  
  Accurately convert spoken audio into written text using a pre-trained deep learning model.

---

## 🛠️ Experimental Setup and Methodology

- **Environment:**  
  - Python 3.x
  - Jupyter Notebook

- **Libraries Used:**  
  - `torch`
  - `torchaudio`
  - `librosa`
  - `transformers`

- **Steps Followed:**
  1. Load the pre-trained `facebook/wav2vec2-base-960h` model and processor.
  2. Load the input `.wav` file and resample it to 16kHz.
  3. Preprocess the audio data for the model.
  4. Perform inference to generate logits.
  5. Decode logits to get the final transcribed text output.

---

## 🔍 Model Architecture

```mermaid
graph TD;
    A[Raw Audio Input (.wav)] --> B[Feature Encoder (CNN layers)];
    B --> C[Transformer Encoder (Self-attention layers)];
    C --> D[CTC Decoder (Greedy / Beam search)];
    D --> E[Text Transcription Output];
```

- **Model Used:** `facebook/wav2vec2-base-960h`
- **Core Components:**
  - **Feature Encoder:** Extracts features from raw audio.
  - **Transformer Layers:** Capture long-range dependencies in speech.
  - **CTC Decoder:** Maps encoded features to text sequences.

---

## 🧪 Results and Observations

- **Tested Audio:**  
  Recorded simple voice samples like:
  > "Hello, this is a test recording for Wav2Vec2"

- **Observations:**
  - Accurate transcription for clean and clear speech.
  - Minor errors when the audio has heavy background noise.
  - Best results with 16kHz, mono-channel `.wav` files.

---

## 🗂️ Repository Structure

```
speech-to-text-wav2vec2/
│
├── code/
│   └── speech_to_text.ipynb         # Full code for inference
│
├── data/
│   └── recordings/
│       └── your_recorded_file.wav   # Audio samples
│
├── README.md                        # Project documentation
│
├── requirements.txt                 # Python dependencies

```

---

## 📥 Setup Instructions

1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/speech-to-text-wav2vec2.git
   cd speech-to-text-wav2vec2
   ```

2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Open the `speech_to_text.ipynb` notebook and run all cells.

---

## 🏆 Conclusion

The Wav2Vec2.0 model provides an effective solution for automatic speech recognition (ASR) tasks with minimal data preprocessing and high transcription accuracy.

---

