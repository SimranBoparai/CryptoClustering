# CryptoClustering


# Table of Contents

- [CryptoClustering](#cryptoclustering)
- [Table of Contents](#table-of-contents)
- [Challenge Overview](#challenge-overview)
- [Prerequisites](#prerequisites)
  - [Required Tools](#required-tools)
  - [Windows Installation Process](#windows-installation-process)
  - [Repository Setup:](#repository-setup)
- [Repository Structure](#repository-structure)
- [Challenge Instructions](#challenge-instructions)
- [Data Preparation Code Example](#data-preparation-code-example)
- [Acknowledgements](#acknowledgements)
- [Author](#author)


# Challenge Overview
This project aims to use unsupervised learning techniques, specifically K-Means clustering and Principal Component Analysis (PCA), to analyze and cluster cryptocurrencies based on their 24-hour and 7-day price changes. By clustering the cryptocurrencies, we aim to discover whether 24-hour and 7-day price fluctuations influence the groupings of different coins.


# Prerequisites

Crypto Clustering Challenge, ensure you complete the following requirements:

## Required Tools
- Install VS Code, and Python on your machine (can use Jupyter Notebook)
- Install the Pandas, Scikit-learn, and HvPlot libraries

## Windows Installation Process
- Open your terminal or command prompt and run the following commands:

  ```
     pip install pandas
     pip install scikit-learn
     pip install hvplot
   ```

## Repository Setup:
  - Create a new repository called ```CryptoClustering``` in GitHub with a README file
  - Clone the repository to your local machine: ```git clone https://github.com/your_username/CryptoClustering.git```
  - Navigate into the repository folder and add the starter file and Resources folder containing ```crypto_market_data.csv``` to this folder 
  - Rename the start file ```Crypto_Clustering_starter_code.ipynb``` to ```Crypto_Clustering.ipynb``` 
  - Clone SSH key in directory
  - Push the changes to your GitHub repository
```
git add .
git commit -m "Pushing ypdated notebook"
git push origin main
```

# Repository Structure
```
  - CryptoClustering
    - Resources
      - crypto_market_data.csv
    - .gitignore
    - Crypto_Clustering.ipynb
    - README.md
```


# Challenge Instructions

Ensure you have downloaded the starter code and files to start the challenge.


Complete the following setps:

  1. Data Preparation: Scaling and Reducing Dimensionality 
  2. Find the Best Value for k Using the Original Scaled DataFrame
  3. Cluster Cryptocurrencies with K-means using the Original Scaled Data
  4. Optomize Clusters with Principle Component Analysis
  5. Find the Best Value for k Using the PCA Data
  6. Cluster Cryptocurrencies with K-means Using the PCA Data
  7. Visualize and Compare the Results 


# Data Preparation Code Example

```VS Code
# Use the `StandardScaler()` module from scikit-learn to normalize the data from the CSV file

scaled_market_data = StandardScaler().fit_transform(df_market_data[['price_change_percentage_24h', 'price_change_percentage_7d',
       'price_change_percentage_14d', 'price_change_percentage_30d',
       'price_change_percentage_60d', 'price_change_percentage_200d',
       'price_change_percentage_1y']]
)

# Create a DataFrame with the scaled data

scaled_market_data_df = pd.DataFrame(
scaled_market_data,
columns=['price_change_percentage_24h', 'price_change_percentage_7d',
       'price_change_percentage_14d', 'price_change_percentage_30d',
       'price_change_percentage_60d', 'price_change_percentage_200d',
       'price_change_percentage_1y']
)
```


# Acknowledgements

I want to mention the following individuals and resources for their assistance and support throughout this assignment: 
- Study group members
- Xpert Learning Assistant and ChatGPT
- Class Activities 


# Author

For any questions or feedback, please contact:
- Name: Gursimran Kaur (Simran)
- Email: kaursimran081999@gmail.com
