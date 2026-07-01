# chatter-detection-using-accoustic-approach-and-once-per-revolution-variance
A program for detecting chatter using accoustic processing data approch and statistic

# 🛠️ CNC Milling Chatter Analysis & Optimization

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![DSP](https://img.shields.io/badge/Domain-Digital_Signal_Processing-success.svg)]()

## 📌 Project Overview
This repository contains an advanced acoustic analysis tool designed to detect, analyze, and mitigate **machining chatter** in CNC milling processes. By leveraging **Digital Signal Processing (DSP)** techniques on raw microphone recordings (`.wav`), the algorithm identifies asynchronous chatter frequencies and automatically recommends optimal spindle speeds (RPM) and feed rates based on **Stability Lobe Theory**.

## ✨ Key Features
- **Time-Domain Analysis**: Raw acoustic waveform visualization.
- **FFT Spectrum Analysis**: Frequency domain extraction using Hann windowing.
- **Tooth Passing Frequency (TPF) Comb Filter**: Algorithmically filters out synchronous forced vibrations (cutting harmonics) to isolate true chatter.
- **Ridge Line Thresholding**: Uses a stable baseline cut to filter out background and machine noise.
- **STFT Spectrograms**: Time-frequency domain visualization to verify chatter persistence and energy consistency.
- **Once-Per-Revolution (OPR) Variance Analysis**: Statistical approach to distinguish between stable cuts (low variance) and unstable chatter (high variance).
- **Smart Parameter Recommendation**: Automatically calculates the optimal Stable RPM and Feed Rate without compromising the feed-per-tooth ratio.

## 📁 Repository Structure
- `Audio_Analysis.ipynb` : The main Jupyter Notebook containing all DSP algorithms and visualizations.
- `Chatter.wav` : Audio sample of an unstable milling cut (high chatter).
- `Stable.wav` : Audio sample of a stable, chatter-free milling cut.
- `Idle Sound.wav` : Audio sample of the machine running without cutting (baseline noise).

## 🚀 How to Run
1. Clone this repository.
2. Install the required dependencies:
   ```bash
   pip install numpy matplotlib scipy jupyter
   ```
3. Open `Audio_Analysis.ipynb` using Jupyter Notebook or VS Code.
4. Run all cells sequentially to generate the signal graphs and view the automated RPM recommendations.

## 📈 Engineering Impact
By utilizing sound wave analysis to pinpoint the exact chatter frequency, this project eliminates trial-and-error in CNC tuning. It demonstrates a theoretical calculation that closely mirrors real-world stability, enabling increased material removal rates (MRR) and extended tool life.
