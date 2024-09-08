# Medicine Recommendation System
## Background
Based on data from the World Health Organization from 2017 to 2023, it was found that the largest cause of patient deaths in hospitals (24.8%) was medication errors, with 58% of these cases being caused by administration errors. Various surveys conducted in several hospitals in Europe, America, India, and Africa revealed that the primary factor contributing to administration errors was the poor quality of healthcare workers, due to a lack of training, work experience, and medication administration guidelines.

Therefore, a system is needed that can improve the performance of healthcare workers, which is expected to have a positive impact on the overall quality of healthcare personnel.

## Proposed Solution
Creating a base model (advanced search) for information providers facilitates literacy and has the potential to be developed into a personalized recommendation system, making it easier to choose the right medication quickly and accurately. With the promising results of this model, it can help the health workforce to obtain and study medication recommendations. This model is a basic model which, if developed and integrated with patient data (medical history), can result in a personalized medicine recommendation system.

"Improved performance of healthcare workers is expected to enhance the quality of service and the hospital's reputation as a healthcare provider."

## Model Specifications
A Recommendation System using the concept of content-based filtering is used to provide alternative medications with similar characteristics. Components include:
- Autoencoder generates embeddings;
- Cosine Similarity calculates similarity based on the embeddings.

### Autoencoder architecture
#### Parameters:

Input Layer: input dimension = 33 (number of features post feature engineering)

Encoding Layer

- First Dense Layer: 64 neurons, activation function ReLU
- Second Dense Layer: 32 neurons, activation function ReLU
- Latent Layer: 8 neurons, activation function ReLU

Decoding Layer

- First Dense Layer: 32 neurons, activation function ReLU
- Second Dense Layer: 64 neurons, activation function ReLU
- Output Dense Layer: input dimension = 33, activation function Sigmoid

#### Hyperparameters:
- Loss function: Mean Squared Error (MSE)
- Optimization: Adam optimizer
- Epochs: 10
- Batch size: 64
- Validation split: 0.2

## Evaluation
The model used autoencoder + cosine similarity to calculate the similarity of medication characteristics. This model achieved an accuracy of 92.2% for k=5 (5 alternative medication recommendations).
