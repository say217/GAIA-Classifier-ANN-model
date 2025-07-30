# Neural Network Approach to Stellar Classification Using Gaia Astrometric Data

<!-- Row 1 -->
<p float="left">
  <img  width="45%" alt="image" src="https://github.com/user-attachments/assets/329f95e3-377b-46d0-9a91-b2c155291d3b" />
  <img width="45%" alt="image" src="https://github.com/user-attachments/assets/66b6e3a2-8ab4-4ff7-8c59-12a931faf907" />

</p>

<!-- Row 2 -->
<p float="left">
  <img  width="45%" alt="image" src="https://github.com/user-attachments/assets/6e9d9078-dd47-4efc-a758-cf7af9619443" />
  <img width="45%"  alt="image" src="https://github.com/user-attachments/assets/83b1e43f-6182-436b-bf00-2376ad0ac828" />


</p>

##  Dataset

- Source: [GAIA Sky Datasets](https://gaiasky.space/resources/datasets/)

The Star Classification Project processes the Gaia dataset to categorize stars into Main Sequence, Giants, and White Dwarfs using a machine learning pipeline centered on an Artificial Neural Network (ANN) model. The workflow involves loading and exploring the dataset, preprocessing features (e.g., Teff, Radius, Mass) through cleaning, outlier removal, and standardization, and applying KMeans clustering to generate initial labels. A fully connected ANN (StarClassifier) with 18 input features, four hidden layers (256, 128, 64, 32 units), and a 3-unit output layer is trained using cross-entropy loss and the Adam optimizer to classify star types. The pipeline evaluates model performance with accuracy and confusion matrices and assesses feature importance via permutation. The system enables predictions for new stars, leveraging astrophysical features to achieve robust classification, suitable for astronomical research and analysis.
#### ANN Equation

- $$h_1 = \text{ReLU}\left(\text{BN}\left(\text{Dropout}\left(W_1 x + b_1, p=0.3\right)\right)\right)$$
- $$h_2 = \text{ReLU}\left(\text{BN}\left(\text{Dropout}\left(W_2 h_1 + b_2, p=0.3\right)\right)\right)$$
- $$h_3 = \text{ReLU}\left(\text{BN}\left(\text{Dropout}\left(W_3 h_2 + b_3, p=0.3\right)\right)\right)$$
- $$h_4 = \text{ReLU}\left(W_4 h_3 + b_4\right)$$

- $y = W_5 h_4 + b_5$
- 
#  Clone the repo
```
git clone https://github.com/say217/GAIA-Classifier-ANN-model.git
cd GAIA-Classifier-ANN-model
