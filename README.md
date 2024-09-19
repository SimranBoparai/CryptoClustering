# CryptoClustering


# Overview
This project aims to use unsupervised learning techniques, specifically K-Means clustering and Principal Component Analysis (PCA), to analyze and cluster cryptocurrencies based on their 24-hour and 7-day price changes. By clustering the cryptocurrencies, we aim to discover whether 24-hour and 7-day price fluctuations influence the groupings of different coins.


# Table of Contents

- [CryptoClustering](#cryptoclustering)
- [Overview](#overview)
- [Table of Contents](#table-of-contents)
- [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Repository Setup:](#repository-setup)
  - [Git Bash Command Example](#git-bash-command-example)
- [Repository Structure](#repository-structure)
- [Challenge Instructions](#challenge-instructions)
- [Data Preparation Example Code](#data-preparation-example-code)
- [Acknowledgements](#acknowledgements)
- [Author](#author)


# Prerequisites

Crypto Clustering Challenge, ensure you complete the following requirements:

## Installation 
- Install VS Code, and Python on your machine (can use Jupyter Notebook)
- Install the Pandas, Scikit-learn, and HvPlot libraries
- Create a new repository called 'CryptoClustering' in GitHub with README and .gitignore file.

## Repository Setup:
  - Create a new repository called 'CryptoClustering' in GitHub with a README file
  - Copy the SSH key in GitHub
  - Clone SSH key in directory
    - Import the StarterCode and Resources files into the directory
  - Git add, commit, and push changes into the repository


## Git Bash Command Example
Navigate into a working directory. 
```
git clone (add you ssh key)
cd 'CryptoClustering'
git add .
git commit -m "Pushing challenge work"
git push 
```


# Repository Structure
- CryptoClustering
    - Resources 
      - crypto_market_data
    - gitignore
    - Crypto_Clustering.ipynb
    - README.md


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


# Data Preparation Example Code 

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
