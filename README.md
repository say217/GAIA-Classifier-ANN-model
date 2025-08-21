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

```mermaid
flowchart TD
    A["Gaia Dataset (.csv)"] --> B["1. Data Loading & Exploration"]
    B --> C["2. Preprocessing"]
    C --> D["3. Clustering (KMeans)"]
    D --> E["Cluster Labels"]
    C --> F["Processed Data"]
    F --> G["4. Neural Network Training"]
    G --> H["Trained Model"]
    H --> I["Predictions"]
    G --> J["5. Evaluation & Feature Importance"]
    J --> K["Metrics & Visualizations"]
    
    %% Cross-links
    B --> L["Visualizations"]
    F --> L
    E --> G
    J --> L
```

#  Clone the repo

```
git clone https://github.com/say217/GAIA-Classifier-ANN-model.git
cd GAIA-Classifier-ANN-model
```
