---
title: "Machine Learning Algorithms for Beginners"
description: "An introduction to Machine Learning Algorithms and when to use them."
draft: false
ShowToc: false
TocOpen: false
tags: ["machine learning", "algorithms"]
categories: ["ai"]
author: "Gary Thomas"
date: 2025-05-18
---

## Comparison of Machine Learning Algorithms

Machine Learning algorithms are techniques used to build models that can make predictions or decisions based on data. Choosing the right algorithm depends on the type of data available and the nature of the problem you're aiming to solve.

| Algorithm Name         | Algorithm Type             | Supervision | Typical Use Cases                                      | Key Strengths                                |
|------------------------|---------------------------|-------------|--------------------------------------------------------|----------------------------------------------|
| Linear Regression       | Regression                | Supervised  | House prices, demand forecasting                      | Simple, interpretable                        |
| Logistic Regression     | Classification            | Supervised  | Churn prediction, spam detection                      | Probabilistic output, efficient              |
| Decision Trees          | Classification/Regression | Supervised  | Credit scoring, rule-based modelling                  | Interpretability, works with categorical data|
| Random Forest           | Classification/Regression | Supervised  | Recommendation systems, market prediction             | Robust, handles overfitting well             |
| SVM                     | Classification            | Supervised  | Image and text classification                         | Effective in high-dimensional spaces         |
| Neural Networks         | Classification/Regression | Supervised  | Speech, image, and language tasks                     | Powerful with large and complex data         |
| K-Means                 | Clustering                | Unsupervised| Customer segmentation, social analysis                | Fast, simple clustering                      |
| PCA                     | Dimensionality Reduction  | Unsupervised| Pre-processing, noise reduction                       | Reduces dimensionality, improves efficiency  |
| Hierarchical Clustering | Clustering                | Unsupervised| Taxonomy, market segmentation                         | No need to pre-define clusters               |
| Autoencoders            | Feature Learning          | Unsupervised| Anomaly detection, image reconstruction               | Learns compact representations               |
| Q-Learning              | Reinforcement Learning    | RL          | Grid-based environments, simple agents                | Simple, foundational RL approach             |
| DQN                     | Reinforcement Learning    | RL          | Game playing, real-time systems                       | Combines RL with deep learning               |
| Policy Gradients        | Reinforcement Learning    | RL          | Robotics, continuous control                          | Handles continuous actions                   |
| Actor-Critic            | Reinforcement Learning    | RL          | Resource allocation, adaptive control                 | Balanced learning via value and policy       |
| K-Nearest Neighbours    | Classification/Regression | Supervised  | Price estimation, recommendations                     | Easy to implement, intuitive                 |
| Naive Bayes             | Classification            | Supervised  | Text classification, sentiment analysis               | Fast, works well with high-dimensional data  |
| Semi-Supervised Learning | Hybrid                    | Semi-Supervised | Medical imaging, web classification             | Reduces labelling effort, improves accuracy   |
| Self-Supervised Learning | Representation Learning   | Self-Supervised | Pretraining for NLP/vision models               | Learns features without manual labels         |
| Ensemble Learning        | Meta-Model                | Supervised      | Fraud detection, competitions                   | High accuracy, reduces overfitting            |


## Types of Machine Learning Algorithms

### Linear Regression

Linear Regression is used to predict a continuous value based on one or more input features. It fits a straight line (or hyperplane in multiple dimensions) to model the relationship between variables.

**Common use cases:**
- Predicting house prices based on size and location
- Forecasting stock prices based on historical data
- Estimating temperature variations by time of year
- Demand planning using past sales data

**Further reading:**
- Géron, A. (2019). *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow*. O'Reilly Media.

### Logistic Regression

Logistic Regression is employed for binary classification problems. It estimates the probability that an input belongs to a particular category (e.g. yes/no, true/false).

**Common use cases:**
- Customer purchase prediction
- Churn detection
- Credit default assessment
- Spam email classification

**Further reading:**
- James, G., Witten, D., Hastie, T., & Tibshirani, R. (2021). *An Introduction to Statistical Learning*. Springer.

### Decision Trees

Decision Trees predict values by learning simple decision rules inferred from data features. The process is intuitive and similar to many business decision flows.

**Common use cases:**
- Credit scoring in financial services
- Customer verification and data validation

**Further reading:**
- Mitchell, T. (1997). *Machine Learning*. McGraw-Hill.

### Random Forest

Random Forests are ensembles of decision trees. Each tree votes on the output, improving accuracy and reducing overfitting.

**Common use cases:**
- Stock market trend analysis
- Recommendation engines (e.g. films, books)

**Further reading:**
- Breiman, L. (2001). "Random Forests". *Machine Learning*, 45(1), 5–32.

### Support Vector Machines (SVM)

SVMs separate data points into classes using a decision boundary (or hyperplane) that maximises the margin between them.

**Common use cases:**
- Image classification
- Text categorisation

**Further reading:**
- Cortes, C., & Vapnik, V. (1995). "Support-vector networks". *Machine Learning*, 20(3), 273–297.

### Neural Networks

Neural Networks are inspired by the structure of the human brain. They are composed of layers of interconnected nodes (neurons) and excel at modelling complex non-linear relationships.

**Common use cases:**
- Voice and image recognition
- Natural language processing
- Autonomous vehicles

**Further reading:**
- Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning*. MIT Press.


### K-Means Clustering

K-Means is an unsupervised algorithm that partitions data into clusters based on similarity.

**Common use cases:**
- Customer segmentation
- Market research
- Social media analytics

**Further reading:**
- Jain, A. K. (2010). "Data clustering: 50 years beyond K-means". *Pattern Recognition Letters*, 31(8), 651–666.

### Principal Component Analysis (PCA)

PCA is a dimensionality reduction technique used to transform high-dimensional data into a lower-dimensional form while retaining most of the original variance. It is often a pre-processing step for visualisation or downstream machine learning tasks.

**Common use cases:**
- Visualising high-dimensional datasets (e.g. gene expression, image data)
- Pre-processing to reduce overfitting
- Noise reduction in data
- Speeding up training for other ML algorithms

**Further reading:**
- Jolliffe, I. T., & Cadima, J. (2016). "Principal component analysis: a review and recent developments". *Philosophical Transactions of the Royal Society A*, 374(2065), 20150202.

### Hierarchical Clustering

Hierarchical clustering builds a hierarchy of clusters using either a bottom-up (agglomerative) or top-down (divisive) approach. It does not require specifying the number of clusters in advance and provides a dendrogram for interpretation.

**Common use cases:**
- Customer or product segmentation
- Taxonomy creation in biology or linguistics
- Organising content based on similarity

**Further reading:**
- Murtagh, F., & Contreras, P. (2012). "Algorithms for hierarchical clustering: an overview". *Wiley Interdisciplinary Reviews: Data Mining and Knowledge Discovery*, 2(1), 86–97.

### Autoencoders

Autoencoders are a type of neural network trained to reconstruct their input. They are commonly used for feature extraction, dimensionality reduction, and anomaly detection, especially in cases involving images, sequences, or large tabular data.

**Common use cases:**
- Anomaly detection in industrial systems or cybersecurity
- Image compression and reconstruction
- Feature learning for unsupervised pretraining

**Further reading:**
- Hinton, G. E., & Salakhutdinov, R. R. (2006). "Reducing the dimensionality of data with neural networks". *Science*, 313(5786), 504–507.

### Reinforcement Learning

Reinforcement Learning (RL) is a paradigm where an agent learns to take actions within an environment to maximise cumulative reward. It differs from other learning types because feedback is received in the form of delayed rewards, not direct labels.

#### Key Algorithms in Reinforcement Learning:

**Q-Learning**  
Q-Learning is a model-free, value-based algorithm that learns the value (Q-value) of action–state pairs. It uses a Q-table to store and update values as it explores the environment.

**Common use cases:**
- Maze navigation
- Simple game-playing agents
- Traffic signal control

---

**Deep Q-Networks (DQN)**  
DQN is an extension of Q-Learning that uses deep neural networks to approximate the Q-values for large or continuous state spaces.

**Common use cases:**
- Playing video games (e.g. Atari games from raw pixels)
- Real-time bidding in advertising
- Energy grid optimisation

**Further reading:**
- Mnih, V. et al. (2015). "Human-level control through deep reinforcement learning". *Nature*, 518(7540), 529–533.

---

**Policy Gradient Methods**  
Policy Gradient algorithms directly learn the policy — a mapping from states to actions — by optimising the expected reward. These are well-suited for problems with continuous action spaces.

**Common use cases:**
- Robotic motion control
- Portfolio management
- Dialogue systems in conversational AI

---

**Actor-Critic Methods**  
These algorithms combine the benefits of value-based and policy-based methods. The actor decides the action, while the critic evaluates how good the action was, helping refine the policy.

**Common use cases:**
- Autonomous driving
- Dynamic resource allocation in cloud computing
- Multi-agent coordination tasks

---

**Further reading:**
- Sutton, R. S., & Barto, A. G. (2018). *Reinforcement Learning: An Introduction* (2nd ed.). MIT Press.
- Lillicrap, T. P. et al. (2016). "Continuous control with deep reinforcement learning". *ICLR*.

### K-Nearest Neighbours (KNN)

KNN classifies new data points based on the classes of their nearest neighbours in the training set.

**Common use cases:**
- House price estimation
- Recommendation systems

**Further reading:**
- Cover, T. M., & Hart, P. E. (1967). "Nearest neighbor pattern classification". *IEEE Transactions on Information Theory*, 13(1), 21–27.

### Naive Bayes

Naive Bayes applies Bayes' Theorem with the “naive” assumption of conditional independence between features. Despite its simplicity, it can be highly effective.

**Common use cases:**
- Spam filtering
- Sentiment analysis
- Document classification

**Further reading:**
- Rennie, J. D. M., Shih, L., Teevan, J., & Karger, D. R. (2003). "Tackling the poor assumptions of naive Bayes text classifiers". *ICML*.

---

### Semi-Supervised Learning

Semi-supervised learning bridges the gap between supervised and unsupervised learning by using a small amount of labelled data alongside a large pool of unlabelled data. It improves model performance when labelling data is costly or impractical.

**Common use cases:**
- Classifying web pages with limited human annotations
- Medical image diagnosis with few labelled scans
- Speech recognition in low-resource languages

**Further reading:**
- Zhu, X. (2005). "Semi-Supervised Learning Literature Survey". *University of Wisconsin-Madison*.

---

### Self-Supervised Learning

Self-supervised learning is a type of supervised learning where labels are derived automatically from the data itself. It is widely used in representation learning, particularly in natural language processing and computer vision.

**Common use cases:**
- Pretraining language models (e.g. BERT, GPT)
- Learning visual features without manual labels
- Audio or video representation learning

**Further reading:**
- Liu, J. et al. (2021). "Self-supervised learning: Generative or contrastive". *IEEE Transactions on Knowledge and Data Engineering*.

---

### Ensemble Learning

Ensemble learning combines multiple models to improve predictive performance. Techniques like bagging, boosting, and stacking leverage the strengths of individual models for greater accuracy and generalisation.

**Common use cases:**
- Fraud detection
- Predictive maintenance
- Winning machine learning competitions (e.g. Kaggle)

**Further reading:**
- Zhou, Z.-H. (2012). *Ensemble Methods: Foundations and Algorithms*. CRC Press.

---
