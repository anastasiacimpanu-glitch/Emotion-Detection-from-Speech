# Emotion-Detection-from-Speech

## 📌 Overview
Emotion recognition plays an important role in **Human–Computer Interaction (HCI)**, enabling machines to understand human emotional states through speech signals. Speech Emotion Recognition (SER) analyzes vocal attributes such as tone, pitch, and intensity to classify emotions.

This project explores emotion classification using **machine learning and deep learning techniques** on two widely used datasets:

- **RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)**
- **TESS (Toronto Emotional Speech Set)**

The workflow includes:

1. Audio preprocessing and augmentation  
2. Feature extraction from speech signals  
3. Training multiple machine learning models  
4. Evaluating performance using standard classification metrics  

The study compares the performance and characteristics of the two datasets and evaluates different algorithms for emotion classification.


# 🎯 Objectives

- Detect and classify emotions from speech signals.
- Extract meaningful acoustic features from audio.
- Train multiple machine learning and deep learning models.
- Compare model performance on different datasets.
- Analyze dataset characteristics and their influence on results.


# 📚 Datasets


## 1️⃣ RAVDESS Dataset

The **Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS)** is widely used in speech emotion recognition research.

### Characteristics

- 24 professional actors (12 male, 12 female)
- 8 emotional categories
- 7356 audio/video files
- High quality recordings (48kHz)
- Two emotional intensity levels: *normal* and *strong*

### Emotions included

- Neutral
- Calm
- Happy
- Sad
- Angry
- Fearful
- Disgust
- Surprised


## 2️⃣ TESS Dataset

The **Toronto Emotional Speech Set (TESS)** is another popular dataset for emotion classification tasks.

### Characteristics

- 2 actresses (ages 26 and 64)
- 2800 audio files
- 7 emotions
- Based on spoken word recordings

### Emotions included

- Anger
- Disgust
- Fear
- Happiness
- Sadness
- Neutral
- Pleasant surprise


# ⚙️ Methodology

## 1. Data Preprocessing

Preprocessing prepares the audio data for machine learning.

Techniques used:

- Noise injection (data augmentation)
- Feature normalization
- Train–validation–test split (70% – 20% – 10%)

## 2. Feature Extraction

Audio features capture the characteristics of speech signals.

### Features used

- **MFCC (Mel Frequency Cepstral Coefficients)**  
  Represents vocal tract characteristics.

- **Chroma Features**  
  Capture pitch information.

- **Mel Spectrogram**  
  Represents short-term power spectrum of audio.

- **Spectral Contrast**  
  Enhances speech modulation.

- **Tonnetz**  
  Captures tonal relationships in audio.

Total extracted features: **~120**


# 🤖 Machine Learning Models

Several classification models were implemented and compared:

- Support Vector Machine (**SVM**)
- Decision Tree
- Random Forest
- Multilayer Perceptron (**MLP**)
- Convolutional Neural Network (**CNN**)


### CNN Architecture

The CNN model includes:

- Input Layer
- Convolution Layers
- Max Pooling Layers
- Flatten Layer
- Dropout
- Output Layer

CNN automatically learns relevant features from the audio representations.


# 📊 Performance Metrics

Models are evaluated using:

- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**
- **Confusion Matrix**

These metrics measure the ability of the model to correctly classify emotional states.


# 📈 Results

| Algorithm | Accuracy | F1 Score | Precision | Recall |
|-----------|----------|----------|-----------|--------|
| SVM | 0.78 | 0.79 | 0.75 | 0.78 |
| Decision Tree | 0.78 | 0.79 | 0.80 | 0.84 |
| Random Forest | **0.85** | **0.88** | **0.87** | **0.89** |
| MLP | 0.81 | 0.82 | 0.83 | 0.82 |
| CNN | 0.82 | 0.84 | 0.82 | 0.84 |

**Random Forest achieved the best performance among traditional models.**


# 🔍 Dataset Comparison

| Feature | RAVDESS | TESS |
|------|------|------|
| Accuracy range | 80% – 97.2% | 99% – 100% |
| Speakers | 24 actors | 2 actresses |
| Gender diversity | Balanced | Female only |
| Audio length | Longer | Short (~2s) |
| Emotion categories | 8 | 7 |

### Observations

- **TESS produces higher accuracy** due to controlled conditions and fewer speakers.
- **RAVDESS is more realistic** because of higher speaker diversity and emotional intensity variation.

# 🛠️ Technologies Used

- **Python**
- **Librosa** – audio processing and feature extraction
- **Scikit-learn** – machine learning algorithms and evaluation
- **NumPy / Pandas** – data processing
- **Matplotlib / Seaborn** – visualization
- **TensorFlow / Keras** – deep learning models

# 🚀 Future Work

Possible improvements include:

- Using **transformer-based models** such as **Wav2Vec 2.0** or **HuBERT**
- Improving cross-dataset generalization
- Training hybrid architectures (CNN + BiLSTM)
- Using larger and more diverse datasets
- Implementing real-time emotion recognition systems

# 📖 References

- Akçay, M.B.; Oğuz, K. *Speech Emotion Recognition: Emotional models, databases, features, preprocessing methods, and classifiers.*
- AlHanai, T.; Ghassemi, M. *Predicting latent narrative mood using audio and physiologic data.*
- Eom, Y.; Bang, J. *Speech emotion recognition based on 2D CNN and MFCC features.*
- Bhavan, A.; Chauhan, P. *Support Vector Machines for emotion recognition from speech.*
- Dupuis, K.; Pichora-Fuller, M. *Toronto Emotional Speech Set (TESS).*

---
