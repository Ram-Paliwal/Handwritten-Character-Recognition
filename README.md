[README.md](https://github.com/user-attachments/files/34284886/README.md)

# Handwritten Character Recognition using CNN

A deep-learning project that classifies handwritten digits and letters using a Convolutional Neural Network (CNN) trained on the **EMNIST Balanced** dataset.

## Project overview

The goal is to recognize a single handwritten character from a 28 × 28 grayscale image. The model predicts one of 47 classes: digits, uppercase letters, and selected lowercase letters.

## Dataset

- **Dataset:** EMNIST Balanced
- **Training images:** 112,800
- **Test images:** 18,800
- **Image size:** 28 × 28 pixels
- **Number of classes:** 47

The notebook downloads the dataset files and prepares the images for training.

## Technologies

- Python
- TensorFlow / Keras
- NumPy
- OpenCV
- Matplotlib
- scikit-learn
- Google Colab

## Model

The project uses a CNN with convolutional layers, batch normalization, ReLU activations, max pooling, dropout, and a 47-class softmax output. Data augmentation is used during training to expose the model to handwriting variations.

## Example predictions

The image below shows predictions on ten samples from the EMNIST test set. **9 of the 10 displayed examples are classified correctly**; the sample whose actual label is `q` is predicted as `9`.

![CNN predictions on EMNIST test samples](assets/prediction_results.png)

## Features

- EMNIST Balanced dataset loading
- Image preprocessing and normalization
- CNN training and validation
- Accuracy and loss plots
- Classification report and confusion matrix
- Predictions on test samples
- Custom image upload and single-character prediction
- Saving the trained model and class mapping

## Run the project

1. Open `Handwritten_Character_Recognition.ipynb` in Google Colab.
2. Select a GPU runtime if one is available.
3. Run the notebook cells in order.
4. Allow the EMNIST dataset files to download.
5. Train the CNN and review the evaluation results.
6. Upload an image containing one handwritten character to try custom prediction.

## Repository structure

```text
Handwritten-Character-Recognition/
├── Handwritten_Character_Recognition.ipynb
├── README.md
├── requirements.txt
├── assets/
│   └── prediction_results.png
└── emnist_project/
    ├── emnist_balanced_cnn.keras
    ├── class_names.json
    ├── training_history.csv
    ├── classification_report.csv
    └── test_metrics.json
```

The model and evaluation files are created by the notebook's save/export cells. Include them in the repository if you want others to download and reuse the trained model.

## Notes

- The displayed results are sample predictions, not a substitute for the complete test-set metrics.
- Custom handwriting images can differ from EMNIST samples in stroke thickness, spacing, centering, and writing style. Custom-image accuracy may therefore vary.
- The EMNIST dataset is provided by the National Institute of Standards and Technology (NIST).

## Reference

Cohen, G., Afshar, S., Tapson, J., & van Schaik, A. (2017). *EMNIST: An Extension of MNIST to Handwritten Letters.*
