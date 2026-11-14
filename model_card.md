# Model Card

For additional information see the Model Card paper: https://arxiv.org/pdf/1810.03993.pdf

## Model Details
This project uses a Random Forest classifier to predict whether an individual's annual income is greater than $50,000 or less than or equal to $50,000. The model was built using Python and scikit-learn as part of a machine learning pipeline.

## Intended Use
The model is intended to demonstrate how Census income data can be processed and used to train and deploy a classification model. It is designed for educational purposes and should not be used to make real-world employment, lending, or other high-impact decisions.

## Training Data
The model was trained using Census Bureau income data provided with the project. The data includes demographic and employment-related features such as age, education, occupation, marital status, relationship, race, sex, work class, and native country. The dataset was split into training and testing data using an 80/20 split.

## Evaluation Data
Twenty percent of the Census dataset was held out as test data. The test data was processed using the same categorical encoder that was fitted to the training data. The model was evaluated on this test set and was also evaluated across individual categorical data slices.

## Metrics
The model was evaluated using precision, recall, and F1 score.

The model achieved the following results on the test dataset:

Precision: 0.7353
Recall: 0.6378
F1 score: 0.6831

Performance was also evaluated across the individual values of the categorical features. Those results are included in slice_output.txt.

## Ethical Considerations
The Census dataset contains demographic characteristics such as race and sex. Model performance may vary across different groups, and historical patterns in the underlying data may introduce or reflect bias. Because of this, predictions from this model should not be used as the sole basis for decisions that could materially affect an individual.

## Caveats and Recommendations
The model was developed as an educational project and has not been validated for production decision-making. Performance should continue to be evaluated across different data slices to identify differences between groups. Additional data validation, bias analysis, model monitoring, and testing would be necessary before considering this model for a real-world application.