# Pre-trained Model Artifacts

Due to GitHub's file storage limitations, all trained model weights, serialized scalers, label encoders, and prediction matrices are hosted externally on Kaggle. 

To run the local Jupyter notebooks or inference scripts, please download the assets from the links in the root `README.md` and place them in their respective subdirectories below.

## Directory Structure & Targets

Place the downloaded files into these subfolders inside `models/`:

### 1. `models/ann_multiclass_model/`
* `best_threat_detector_model.h5` - Multi-class ANN weights.
* `label_encoder.pkl` - Serialized label encoder for the 14+ threat classes.
* `scaler.pkl` - Serialized StandardScaler object.

### 2. `models/final_tuned_model/`
* `best_model.h5` - Time-Series LSTM + Multi-Head Attention binary classifier weights.
* `intrusion_detection_model.keras` - Keras model configuration & weights.
* `label_encoder.pkl` - Serialized label encoder for binary labels (Benign/Attack).
* `scaler.pkl` - Serialized MinMaxScaler/StandardScaler for temporal features.

### 3. `models/meta_model_artifacts/`
* `meta_model.pkl` - Serialized Logistic Regression meta-learner.
* `aligned_true_labels.npy` - Prediction validation alignment labels (optional).
* `ann_predictions.npy` - Out-of-fold ANN predictions for meta-model training (optional).
* `lstm_predictions.npy` - Out-of-fold LSTM predictions for meta-model training (optional).
