# deep-learning-challenge
Module 21 Challenge - UNCC-VIRT-DATA-PT-03-2024-U-LOLC-MTTH

# Overview of the analysis: 
The goal of this project is to create a machine learning classification model that would best predict the best chance of success (with an accuracy above 75%) in their ventures for "The nonprofit foundation Alphabet Soup" (name used in homework prompt; no affiliation).

# Results:

**Data Preprocessing**

**What variable(s) are the target(s) for your model?**
  - All models use the "IS_SUCCESSFUL" as the target: 0 - success  | 1 - failure

**What variable(s) are the features for your model?**

* Module01 - Neural Network
  - As follow: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT
* Module02 - Optimized Neural Networks
  - As follow: NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT
* Module03 - Random Forest
  - As follow: NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT

**What variable(s) should be removed from the input data because they are neither targets nor features?**

* Module01 - Neural Network
  - As follow: EIN and NAME
* Module02 - Optimized Neural Networks
  - As follow: EIN, STATUS, and SPECIAL_CONSIDERATIONS
* Module03 - Random Forest
  - As follow: EIN, STATUS, and SPECIAL_CONSIDERATIONS

# Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?

* Module01 - Neural Network
  - Number of Neurons: 43
  - Number of Layers: 2
  - Activation Functions: relu and sigmoid - relu is commonly used and sigmoid (output layer) is a binary model.
* Module02 - Optimized Neural Networks
  - Number of Neurons: 395
  - Number of Layers: 3
  - Activation Functions: relu and sigmoid - relu is commonly used and sigmoid (output layer) is a binary model.
    
**Were you able to achieve the target model performance?**
Yes, while my first model only reached an accuracy score of ~72.4% (below the 75% threshold), both other modules surpassed that threshold.
Module02 - ~78.7%
Module03 - ~76.9%

**What steps did you take in your attempts to increase model performance?**
- I removed addtional columns that would not benefit the predict output, as they skewed too much against the minority outcome.
- Added additional neural network layers.

# Summary: 
Overall, after the initial neural network was optimized, the desired accuracy threshold was reached (Module02). Trying a diferent classification model (Module03), Random Forest, also produced desireable results, but were sightly less accurate. I recommend Module02 for making predictions within the dataset or with similar data.
