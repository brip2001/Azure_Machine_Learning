Optimizing an ML Pipeline in Azure
Overview
This project is part of the Udacity Azure ML Nanodegree. In this project, we build and optimize an Azure ML pipeline using the Python SDK and a provided Scikit-learn model. This model is then compared to an Azure AutoML run.

Useful Resources
ScriptRunConfig Class
Configure and submit training runs
HyperDriveConfig Class
How to tune hyperparameters
Summary
This dataset contains data about bank marketing campaigns and client interactions. We seek to predict whether a client will subscribe to a term deposit based on various attributes.

The best performing model was a Logistic Regression model optimized using HyperDrive, achieving an accuracy of approximately 91%. The AutoML run produced a Voting Ensemble model with a slightly higher accuracy.

Scikit-learn Pipeline
The pipeline uses the bank marketing dataset, which is cleaned and preprocessed to handle categorical variables and missing data. The classification algorithm used is Logistic Regression. Hyperparameter tuning is performed using Azure HyperDrive, varying the regularization strength C and max_iter to find the optimal model.

Benefits of the parameter sampler chosen: A RandomParameterSampling strategy was chosen because it efficiently explores the hyperparameter space without exhaustively searching all possibilities. It allows for a good balance between exploration and computational efficiency.

Benefits of the early stopping policy chosen: A BanditPolicy was used as the early stopping policy, which terminates underperforming runs early based on their performance relative to the best run. This saves computational resources and speeds up the hyperparameter tuning process by focusing on promising configurations.

AutoML
AutoML experimented with various algorithms and hyperparameters and selected a Voting Ensemble model as the best performing model. This ensemble combines multiple models to improve predictive performance and achieved an accuracy slightly higher than the HyperDrive-tuned model.

Pipeline comparison
The AutoML model slightly outperformed the HyperDrive-tuned Logistic Regression model in terms of accuracy. While the Logistic Regression model is simpler, the AutoML's Voting Ensemble captures more complex patterns in the data. The difference in performance suggests that ensemble methods can provide better generalization by combining the strengths of multiple models.

Future work
Future improvements could include experimenting with additional algorithms or ensemble methods in the HyperDrive run. Incorporating feature engineering techniques, such as creating interaction terms or using dimensionality reduction, might also enhance model performance. Additionally, tuning more hyperparameters or using a different sampling strategy could yield better results.
