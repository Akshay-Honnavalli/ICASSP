# ICASSP 2025 Bed Occupancy Detection Challenge

This repository contains the `.ipynb` files with code to solve the ICASSP 2025 challenge.  
**Authors/Code Owners**: Akshay Prasad, Hrishi Preetham GL, and Gowri Srinivasa.

---

## Abstract

The accurate detection of bed occupancy is crucial in healthcare applications. In this study, we apply **time-frequency analysis** using **Wavelet decomposition** to analyze 3-axis accelerometer data and predict bed occupancy.

- Various **wavelet filters**, **decomposition levels**, and **segment sizes** were tested to identify optimal parameters for maximizing prediction accuracy.  
- Accurate segmentation, followed by feature extraction in the transform domain for each segment, ensures precise detection of transitions between "in-bed" and "not-in-bed" states.

**Results**:  
- **Track 1**: Achieved highest accuracy of **0.98952**.  
- **Track 2**: Achieved highest accuracy of **0.93214**.

---

## Motivation

Sleep monitoring is vital for assessing health and well-being. While wearables like smartwatches track vitals, their contact-based nature can discomfort users during sleep. Non-contact accelerometers embedded in beds offer a user-friendly alternative by detecting mattress deformations from movement and breathing.  

Smart beds can monitor:  
- **Vitals** (e.g., heart rate, respiration rate).  
- **Sleep characteristics** (e.g., quality, posture).  

### Challenges Addressed:
- Differentiating user motion from ambient noise caused by bed vibrations.  
- Avoiding inference of vitals from spurious noise signals when no user is present.

---

## Challenge Tracks

This challenge, organized by ICASSP 2025, includes two tracks:  

### **Track 1**: Person in Bed Segmented Data  
- Classification of pre-chunked accelerometer signals into two categories:  
  - **"Not in Bed"**  
  - **"In Bed"**  

### **Track 2**: Person in Bed Streaming Data  
- Streaming version of a person-detection classifier.  
- **Goal**: Minimize latency and maximize accuracy.

---

## Repository Contents

- **`track1-notebook.ipynb`**: Solution to Track 1 problem statement.  
- **`track2-notebook.ipynb`**: Solution to Track 2 problem statement.

---

## Prerequisites

### **Python Version**
- Python 3.9 or higher.

### **Required Libraries**
- `numpy`  
- `pandas`  
- `matplotlib`  
- `seaborn`  
- `pywavelets`  
- `scikit-learn`  
- Jupyter Notebook (to run `.ipynb` files)

---

## Evaluation Metrics

For both tracks, our model was evaluated based on:  

1. **Accuracy**: Percentage of correctly classified data points.  
2. **Latency**: Time taken to make predictions (important for Track 2).  

---

## Acknowledgments

We extend our gratitude to:  
- **ICASSP 2025 Organizers**: For providing the dataset and challenge framework.  
- **PyWavelets** and **scikit-learn**: For their robust libraries used in this project.
