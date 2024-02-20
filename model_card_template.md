# Model Card

For additional information see the Model Card paper: https://arxiv.org/pdf/1810.03993.pdf

## Model Details
This model was created for census.csv data. It was used to develop a classification model. A random forest classifier is used as a classifier. Default configurations were used for training.

## Intended Use
This model should be used to predict the "workclass" based on the "education". It can be run by using "python train_model.py" in the cli.

## Training Data
The source of the data is publicaly available Census Bureau data. 80% of the data is used for training. 

## Evaluation Data
The source of the data is publicaly available Census Bureau data. 20% of the data is used to validate the model. Transformation was applied on the categorical features and the target label using the One Hot Encoder and label binarizer fitted on the train set.

## Metrics
_Please include the metrics used and your model's performance on those metrics._
The model was evaluated using Precision, Recall, and FBeta. The overall performance on these metrics was:
    Precision: 0.7419, Recall:  0.6384, FBeta:  0.6863
Model saved to model/model.pkl. Model saved to model/encoder.pkl

## Ethical Considerations
The model performance was calculated on data slices. This causes concerns that the model may potentially be bias.This study is for educational purposed and further investigation may be needed.

## Caveats and Recommendations
Data imbalance in some of the the features may need further investigation because it causes feature bias.
