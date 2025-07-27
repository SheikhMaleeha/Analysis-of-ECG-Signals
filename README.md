# Analysis-of-ECG-Signals
<!-- ECG Signal Classification Using XResNet1D -->

This project implements a deep learning pipeline to classify ECG signals into five diagnostic categories using the PTB-XL dataset. Leveraging the XResNet1D architecture, the model efficiently processes raw 1D time-series ECG signals and identifies key cardiovascular conditions.

![ECG Sample](https://github.com/user-attachments/assets/sample-ecg-classification.png)

## Features and Implementation

1. **Data Preprocessing**  
   - Stratified patient sampling to balance classes across training, validation, and test sets.  
   - Label extraction and multi-hot encoding of diagnostic classes.

2. **Feature Extraction & Utilities**  
   - Utilizes WFDB and SCP code mapping to load and structure raw ECG data.  
   - Signal normalization and label aggregation for training readiness.

3. **Deep Learning Model**  
   - Implements a 1D Convolutional Residual Network (XResNet1D).  
   - Enhanced with Squeeze-and-Excite, AdaptiveConcatPool1d, and attention layers.

4. **Training & Evaluation**  
   - Uses FastAI to train with `fit_one_cycle` and learning rate tuning.  
   - Achieved training accuracy of **92.5%** with predictions and AUCs saved in `.npy` and `.csv` formats.

## Classification Categories

- **Normal ECG**  
- **Myocardial Infarction**  
- **ST/T Changes**  
- **Conduction Disturbances**  
- **Hypertrophy (Left & Right Ventricular)**

## Design and Tools

- **Platform**: Visual Studio Code  
- **Languages & Libraries**: Python, PyTorch, FastAI, OpenCV, WFDB, NumPy, Matplotlib  
- **Dataset**: [PTB-XL ECG Dataset](https://physionet.org/content/ptb-xl/1.0.3/)

## Results and Visualizations

- Learning rate optimization and training loss curves plotted to assess convergence.
- Accuracy vs Epoch plots show consistent performance across datasets.

![Learning Rate Plot](https://github.com/user-attachments/assets/lr-plot.png)  
![Training Accuracy](https://github.com/user-attachments/assets/train-accuracy.png)

## Conclusion

This project demonstrates effective classification of ECG signals using XResNet1D. It opens up possibilities for real-time ECG analysis and integration with wearable device outputs for health monitoring.
