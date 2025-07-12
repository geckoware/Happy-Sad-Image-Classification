```markdown
# Happy-Sad Facial Expression Classification 🎭

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.12-orange)
![License](https://img.shields.io/badge/License-MIT-green)

A lightweight **Convolutional Neural Network (CNN)** model that classifies facial expressions into "Happy" or "Sad" with **94.3% validation accuracy**. Designed for emotion detection in psychology research, customer feedback analysis, or interactive applications.

---

## ✨ Highlights
- **High Accuracy**: 94.3% validation accuracy with minimal overfitting
- **Optimized Architecture**: 3-layer CNN with Dropout regularization
- **Production-Ready**: Includes serialized `.h5` model for easy deployment
- **Visual Insights**: Training/validation metrics tracked and visualized
- **Scalable**: Handles 128x128 RGB images with batch processing

---

## 🛠 Technical Implementation
### Model Architecture
- **Input Layer**: 128x128x3 RGB images
- **Feature Extraction**: 
  - 3x Conv2D layers (32 → 64 → 128 filters) with ReLU
  - MaxPooling2D for dimensionality reduction
- **Classification Head**: 
  - Flatten → Dense (128 neurons) → Dropout (0.5)
  - Sigmoid output for binary classification

### Training Protocol
- **Optimizer**: Adam (default parameters)
- **Loss Function**: Binary Cross-Entropy
- **Early Stopping**: Monitors validation loss with 2-epoch patience
- **Hardware**: GPU-accelerated via Google Colab (T4)

---

## 📂 Dataset
- **Total Images**: 608 (555 training + 53 validation)
- **Class Balance**: 50.1% Happy, 49.9% Sad
- **Preprocessing**:
  - Resized to 128x128 pixels
  - Normalized (1./255 pixel values)
  - Batch-processed (size=32)

Directory structure:
```
HAPPYSAD/
├── train/
│   ├── happy/
│   └── sad/
├── val/
│   ├── happy/
│   └── sad/
└── test/
    ├── happy/
    └── sad/

```

---

## 📊 Performance Metrics
| Metric          | Training | Validation |
|-----------------|----------|------------|
| Accuracy        | 98.9%    | 94.3%      |
| Loss           | 0.028    | 0.221      |

![Training Progress](assets/training_metrics.png)

---

## 🚀 Getting Started
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/geckoware/Happy-Sad-Classification.git
   ```

2. **Set Up Environment**:
   Install dependencies via `pip install -r requirements.txt`.

3. **Run the Model**:
   - Execute the Jupyter Notebook for training/evaluation
   - Use the pre-trained `happysad_model.h5` for inferences

4. **Predict Emotions**:
   Load the model and pass 128x128 RGB images for instant classification.

---

## 📬 Connect
For collaborations or questions:
- [LinkedIn Profile](https://www.linkedin.com/in/fevzihan-alkan-282963337/)
- [Email](alkanfevzihan@gmail.com)
```
