# 🧠 P300 Speller BCI System

A Brain-Computer Interface (BCI) project that decodes real EEG signals to detect P300 responses and simulate a classical 6×6 character speller. This system demonstrates how users can communicate through brain signals using visual stimuli and machine learning models.

## Overview
This project was developed for the **CSAI 463 - Computational Intelligence** course at New Giza University (Spring 2025). It features:

- Real EEG data processing
- Signal filtering and feature extraction using CSP (Common Spatial Pattern)
- Classification using LDA (Linear Discriminant Analysis)
- Character prediction from P300 responses
- GUI simulation of the speller matrix
- Output of decoded sentences to a `.txt` file

## Features
- ✅ Bandpass filtering (1–15 Hz) to isolate P300 signals
- ✅ CSP feature extraction for dimensionality reduction
- ✅ LDA classifier for P300 detection
- ✅ GUI-based speller with flashing row/column stimuli
- ✅ Sentence prediction written automatically to `output_real.txt`

## Dataset
- Real EEG data (from `dataset.zip`) is used for both training and testing
- EEG epochs are grouped into 12-flash cycles corresponding to characters
- Predictions are made by detecting the row and column with the highest P300 scores

## GUI Demo
The GUI simulates the speller experience with the following capabilities:

1. Displays a 6×6 character matrix
2. Flashes rows/columns sequentially
3. Predicts letters and builds the output sentence in real-time

> ⚠️ Note: The GUI is a simulation and does **not** operate on live EEG signals in real time.

## 📂 Files
| File | Description |
|------|-------------|
| `code.ipynb` | Main Jupyter notebook implementing the full pipeline |
| `output_real.txt` | Output file containing the final predicted sentence |
| `README.md` | This documentation file |
| `dataset.zip` | EEG training and testing data (not included here) |

## How to Run
1. Clone the repo:
   ```bash
   git clone https://github.com/zeina-abdelaziz/P300-system.git
   cd P300-system
  2.	Unzip the dataset and place it in the working directory.
	3.	Run code.ipynb in Jupyter Notebook.
	4.	Press SPACE in the GUI to simulate flashes and watch the decoded sentence build in real time.
## Technologies Used
- Python
- NumPy, SciPy, scikit-learn
- Matplotlib, PyQt5/Tkinter (for GUI)
- CSP and LDA (predefined implementations)

## License
This project is for academic and non-commercial educational use only.
