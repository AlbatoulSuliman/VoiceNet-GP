# VoiceNet: A Deep Learning-Based Framework for Biometric Recognition Using Voice

An intelligent speaker verification system developed in MATLAB that provides secure, contact-free authentication using unique voiceprints.

---

## Project Artifacts & Links
* **Live Web Interface**: [VoiceNet App](https://voice-net-v0-2.vercel.app/)
* **Documentation**: [Google Drive Folder](https://drive.google.com/drive/folders/1SE4EYQOL9g5Fw2L6KfSXe-b09WWkEw1v?usp=drive_link)

---

## Core Functionality & Workflow
* **Feature Extraction**: Transforms 1D raw audio signals into 2D representations using Short-Time Fourier Transform (STFT) Spectrograms and Mel-Frequency Cepstral Coefficients (MFCC) to isolate unique speaker formants and timbre.
* **Deep Learning Framework**: Uses a modified Convolutional Neural Network (CNN-VGG16) architecture as an embedding generator to yield a highly specific 128-dimensional feature vector.
* **Template Protection**: Saves feature embeddings as non-invertible secure templates in the database, ensuring raw audio waveforms cannot be reconstructed.
* **Verification Logic**: Employs Cosine Similarity matching to calculate the real-time mathematical distance between live audio embeddings and stored references to evaluate authentication claims.

---

## Performance Evaluation & Metrics
The model was rigorously cross-tested across **443 evaluation samples against 20 identities** to evaluate system reliability
* **Optimal Decision Threshold**: 0.92
* **Overall System Accuracy**: 97.20%
* **System Precision**: 0.97
* **False Acceptance Rate (FAR)**: 0.08% (Successfully meets global biometric security targets $\le 0.1\%$ to prevent identity spoofing)
* **False Rejection Rate (FRR)**: 54.40%

---

## Environmental Stress Testing Results
* **Baseline (Clear Environment)**: `0.9741` -> **Access Granted** (Immediate user recognition).
* **Café Shop Background Noise**: `0.9806` -> **Access Granted** (Resilient to ambient distraction due to robust data augmentation).
* **Whispering Level Input**: `0.9443` -> **Access Denied** (Filtered out by signal quality metrics due to low formant frequency levels).
* **Loud Level / Shouting Input**: `0.9222` -> **Access Denied** (Rejected because over-amplification distorts authentic vocal patterns).
* **Imposter Validation Attempt**: `0.8852` -> **Access Denied** (Successfully blocked unauthorized access).

---

## Development Team
* Albatoul Aljuhani
* Raneem Almousa
* Joury Khalid
* **Academic Supervisor**: Dr. Rania Ghoniem

---

## Project Keywords
`Biometric Recognition` `Deep Learning` `Speaker Verification` `MATLAB` `CNN` `VGG16` `MFCC` `Spectrogram` `Biometric Security` `Template Protection` `Cosine Similarity` `Signal Processing`
