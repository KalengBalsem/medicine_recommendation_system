# Medicine Recommendation System
![inference](https://github.com/user-attachments/assets/afbc01fe-fa20-46a7-ac5e-ff4af16cc5a3)

## Background
![background](https://github.com/user-attachments/assets/b457b314-1039-4366-9050-7d07bc0b4fa8)

## Proposed Solution
Creating a base model (advanced search) for information providers facilitates literacy and has the potential to be developed into a personalized recommendation system, making it easier to choose the right medication quickly and accurately. With the promising results of this model, it can help the health workforce to obtain and study medication recommendations. This model is a basic model which, if developed and integrated with patient data (medical history), can result in a personalized medicine recommendation system.

"Improved performance of healthcare workers is expected to enhance the quality of service and the hospital's reputation as a healthcare provider."

## Model Specifications
![modelling](https://github.com/user-attachments/assets/0f566d1f-1449-4a26-be11-af190f853b5e)

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
![evaluation](https://github.com/user-attachments/assets/2b6b7c98-fe46-4c61-a401-2345406416f3)

The model used autoencoder + cosine similarity to calculate the similarity of medication characteristics. This model achieved an accuracy of 92.2% for k=5 (5 alternative medication recommendations).
![accuracy](https://github.com/user-attachments/assets/03e7fc4e-cec4-4fa0-b4de-d76a9be0a33f)

