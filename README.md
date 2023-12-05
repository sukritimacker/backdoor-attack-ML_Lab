# ML Lab Submission: Backdoor Attack and Channel Pruning Defense for BadNets on YouTube Face Dataset

Name: Sukriti Macker
<br>
NetID: sm11017
---

## Dependencies
- Required Libraries: 
  - numpy
  - pandas
  - sklearn
  - tensorflow
  - keras
  - h5py
  - os
  - sys
- Python Version: 3.8 or higher.

## Introduction
This project aims to develop a mechanism for detecting backdoors in BadNets that are trained on the YouTube Face dataset. BadNets are neural network classifiers that are vulnerable to backdoor attacks, where malicious triggers are secretly embedded to manipulate their outputs. The goal is to create a defense mechanism that can distinguish between clean inputs and backdoored inputs, and repair the neural network to reduce these vulnerabilities.

We implemented a strategy to create different versions of the neural network that respond to varying levels of accuracy decline. This involved saving distinct models at specific benchmarks where the accuracy dropped by predetermined percentages: 2%, 4%, and 10%. Each model was named according to the extent of accuracy reduction it represents. For example, the models were labelled as model_withDrop_2.h5, model_withDrop_4.h5, and model_withDrop_10.h5, indicating the degree of decline in accuracy associated with each respective model.

## Installation & Setup
After installing or meeting the dependency requirements, load the jupyter notebook ML_Lab4.ipynb. The notebook is structured to automatically generate the accuracy and attack success rate corresponding to every pruned model level.

### Loading the Model 
Retrieve the BadNet model stored in the file bd_net.h5. 

### Pruning Operation
Execute the pruning technique on the model's last pooling layer at different levels (2%, 4%, 10%). 

### Evaluation of Models
Evaluate the performance of each pruned model concerning both clean and backdoored test datasets. To assess the integrity of the compromised model, run eval.py: python3 eval.py

### Storing/Saving the Model 
Save the pruned models for potential future utilization or reference.
