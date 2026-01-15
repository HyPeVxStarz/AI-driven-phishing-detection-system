# AI-driven-phishing-detection-system
Contains a machine learning pipeline designed to detect phishing and spam messages using NLP. Project compares a traditional probabilistic baseline agaisnt an advanced deep learning architecture yo evaluate performance in a cyber security context.

KEY RESULTS
The final optimized LSTM model achieved near-perfect scores after resolving significant training instabilities:

Final accuracy - 98.57%
Spam recall - 0.91
Spam precision - 0.98
Ham recall - 1.00

TECHNICAL CHALLENGES
This project involved significant iterative development to overcome common AI pitfalls: 
Environment Conflicts: Resolved TensorFlow 2.16+ and Keras 3 dependency issues by standardizing import paths and utilizing legacy backends. 
The Accuracy Paradox: Addressed a class imbalance (86% Ham / 14% Spam) where the model initially defaulted to predicting only the majority class. 
Model Collapse: Documented a failure state where aggressive class weighting led to 13.45% accuracy. This was resolved by tuning the learning rate to 0.0005 and utilizing a Bidirectional LSTM to capture dual-directional semantic context.

ARCHITECTURE
Preprocessing: Tokenization, Porter Stemming, and Sequence Padding. 
Embedding Layer: 64-dimensional word vectorization. 
Bidirectional LSTM: 32 units to capture long-term dependencies.
Regularization: Dropout (0.4) to prevent overfitting. 
Optimizer: Adam with custom learning rate tuning.

