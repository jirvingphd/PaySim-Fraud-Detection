# practicing-fraud-detection
 
<!-- ![.webp](images/banner-image.webp) -->

<center><img src="images/banner-image.webp" width=400px></center>

## Introduction

Detecting fraud in financial systems, particularly within the realm of mobile money transactions, is a significant challenge. Access to datasets in this field is limited, largely due to the private and sensitive nature of financial data. In response to this, **PaySim**, a simulator, was developed to generate synthetic transaction data that closely mirrors real-world mobile money transactions. This synthetic dataset introduces fraudulent behavior, making it a valuable resource for developing and testing fraud detection algorithms.

The data used in this project is a scaled-down simulation of real transactions sourced from a mobile money service operating across 14 countries. PaySim replicates transactions over a 30-day period (equivalent to 744 hours), simulating typical user behaviors while injecting fraudulent activities. The dataset comprises approximately 24 million records across five transaction types: **CASH-IN, CASH-OUT, DEBIT, PAYMENT**, and **TRANSFER**.

### Key Dataset Details:

>- Kaggle Link: https://www.kaggle.com/datasets/ealaxi/paysim1

- **step**: Represents an hour in the simulation (1 step = 1 hour).
- **type**: Defines the category of the transaction (CASH-IN, CASH-OUT, etc.).
- **amount**: The value of the transaction in the local currency.
- **nameOrig**: Identifier for the customer initiating the transaction.
- **nameDest**: Identifier for the recipient of the transaction.
- **isFraud**: Denotes whether the transaction was identified as fraudulent.
- **isFlaggedFraud**: Marks any attempts to transfer amounts over 200,000, which are deemed illegal by the system.

One important consideration is that transactions flagged as fraudulent are canceled. Consequently, the balance-related fields (e.g., `oldbalanceOrg`, `newbalanceOrig`, `oldbalanceDest`, `newbalanceDest`) should be excluded from fraud detection models.

The goal of this project is to utilize this synthetic data to build and evaluate machine learning models that can accurately identify fraudulent transactions. This research is part of a broader initiative to enhance fraud detection techniques in mobile money services.

### Acknowledgements
This dataset originates from a project funded by the Knowledge Foundation in Sweden and was first introduced in the paper:

- Lopez-Rojas, E. A., Elmir, A., & Axelsson, S. (2016). PaySim: A financial mobile money simulator for fraud detection. *The 28th European Modeling and Simulation Symposium (EMSS)*, Larnaca, Cyprus.
