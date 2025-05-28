🧠 Melanoma Detection Using Convolutional Neural Networks (CNN)
🔍 Project Overview
Melanoma is a severe form of skin cancer responsible for a significant number of skin cancer-related deaths. Early detection is crucial for effective treatment. This project aims to develop a Convolutional Neural Network (CNN) model to accurately detect melanoma from dermoscopic images, assisting dermatologists in early diagnosis and reducing manual effort.

📁 Dataset
The dataset comprises images of various skin lesions, including:

Melanoma

Pigmented Benign Keratosis

Seborrheic Keratosis

Others

📊 Class Distribution Analysis
Least represented class: Seborrheic Keratosis

Most represented classes: Pigmented Benign Keratosis and Melanoma (approximately 100 more samples than other classes)

This imbalance necessitated data augmentation to ensure model robustness across all classes.

🛠️ Methodology
1. Baseline CNN Model
Optimizers Tested: Adam, RMSprop

Epochs: 20 and 30

Findings:

Training accuracy increased to ~80%

Validation accuracy fluctuated around ~50%

Conclusion: The model exhibited signs of overfitting

2. Data Augmentation
Introduced augmentation layers to enhance generalization

Optimizers Tested: SGD, Adagrad, Adam

Epochs: 30 and 50

Findings:

Overfitting was reduced

Training and validation accuracies were between 45–55%

Conclusion: The model showed signs of underfitting

3. Class Rebalancing
Utilized the Augmentor library to synthetically augment underrepresented classes

Results:

Improved handling of class imbalance

Reduced overfitting

Best Performance: Model with Adam optimizer achieved ~90% training accuracy and ~80% validation accuracy

📈 Results
Model Configuration	Training Accuracy	Validation Accuracy	Observations
Baseline (Adam, 20 epochs)	~80%	~50%	Overfitting observed
With Augmentation (SGD, 30 epochs)	45–55%	45–55%	Underfitting observed
With Class Rebalancing (Adam, 30 epochs)	~90%	~80%	Improved generalization

✅ Future Work
Implement transfer learning with pre-trained models (e.g., ResNet50, EfficientNet)

Explore advanced data augmentation techniques

Utilize stratified K-Fold cross-validation

Experiment with focal loss to address class imbalance

📚 References
Augmentor Documentation

ISIC Skin Lesion Analysis

Transfer Learning for Melanoma Detection
