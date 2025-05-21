# deep-learning-challenge
Module 21 Challenge

## Alphbet Soup Charity Neural Network Model Report

### Overview of the Analysis

The nonprofit organization Alphbet Soup wants to determine which funding applicants are most likely to suceed. To assist in this mission, we developed a binary classification neural network model using Keras and Tensorflow that predicts whether an organization will be sucessful (Is_sucessful = 1) based on features in a dataset of over 34,000 historical funding applications.

The key goal was to train and evaluate a deep learning model tha could predict sucess with a target accuracy of 75% or higher, allowing Alphbet Soup to allocate funding more effectively.

### Data Preprocessing

#### What was the target for the model?

* The target variable was IS_SUCESSFUL, which indicates wheter the applicant sucessfully used the funding (1) or not (0).

#### What are the features?

* Features included: 
    * APPLOCATION_TYPE
    * AFFILATION
    * CLASSIFICATION
    * USE_CASE
    * ORGANIZATION
    * STATUS
    * INCOME_AMT
    * SPECIAL_CONSIDERATIONS
    * ASK_AMT

* What variables were removed?
    * EIN and NAME were removed because they are identifiers, not predictive features.

#### Compiling, Training, and Evaluating the Model

Model Architecture

* Input Features: 116 after one-hot encoding
* Output Layer: 1 neuron, Sigmoid activation (bianry classification)

Training Details

* Epochs: 50
* Loss Function: Binary crossentropy
* Optimizer: Adam
* Metrics: Accuracy
* Checkpointing: Weights saved every epoch using a ModelCheckpoint callback.

Model Evaluation Results

    Metric Value
    Accuracy 72.65%
    Loss 0.5576

THe model acheived an accuracy of 72.65%, just below the 75% target.

#### Summary of Results

While the model shows predictive capability, it falls slightly short of the target accuracy of 75%. It correctly classifies over 72% of applicants, which makes it a solid baseline model, but not yet reliable enough for real-world deployment.

#### Future Imporvements and Alternative Models

What steps could imporve performance?

1. Drop additional unhelpful features to reduce noise.
2. Add more neurons or layers to imporve model capacity.
3. Balance the dataset if class imbalanbce is contributing to bias.
4. Try different activation functions or optimizers.
5. Increase training epochs for deeper learing.

#### What other models coould solve the proble better?

An alternative to deep learning could be a Random Forest Classifier or Gradiant Boosting (e.g., XGBoost).

These models are:

* Highly interpretable 
* Preform well with tanular/ categorical data
* Often require less tuning and training time than neural networks.

Given that the dataset is structured and not too high-dimensional, these models could outpreform a neural network with less risk of overlifting.
