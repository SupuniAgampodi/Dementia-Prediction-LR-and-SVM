# Dementia Prediction

Dementia is a neurodegenerative disorder characterized by a decline in cognitive function and memory loss. It is a significant public health issue, particularly among the elderly population, as it affects their daily activities, independence, and quality of life. Early detection and diagnosis of dementia are crucial for timely intervention and support for affected individuals. 

## Dataset 
The dataset used in this project was collected from mobile health care services provided in collaboration with elderly care centers operated by local non-governmental organizations. These health care services were offered to elderly individuals residing in different districts of Hong Kong. The services were provided free of charge over a ten-year period, specifically from 2008 to 2018. The dataset likely contains information related to the health status, demographics, and other relevant factors of the community-dwelling elderly population in Hong Kong during that time frame.

## EDA
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/c334477f-a70b-4351-b06d-74804a2841aa" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/f1d97cf8-68b7-430d-a662-56fa2695d583" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/fca78eaa-ca88-45b7-94ca-fa9a633715f0" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/601f4fbd-2754-4317-b6f4-c0fdacaf9486" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/3bb4f614-d694-48f1-b3c1-cbad80c1ba1b" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/395c9ed8-e508-46eb-9c75-f4940ac23b14" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/bb2be159-6df9-4712-8bc3-fd2a015f3f93" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/169ddc71-6920-418b-ad79-e2b47300d661" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/8599d2ae-e81b-4aca-bece-5daf96689bcb" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/7bdcd7d7-7885-49ef-a073-1fc5c02d588b" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/2bf23840-3c5d-489e-86e7-8e4e38aafff4" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/d742f22c-cd18-4614-9e41-2890e1096fa9" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/58fa6f2a-b55b-4c29-b491-281197ddbb02" />
<img width="750" height="450" alt="image" src="https://github.com/user-attachments/assets/ef695dca-ef48-4d04-8705-1d5f5750a8fe" />

## Correlation Analysis
Based on the analysis of the correlations between various factors and the MMSE, several observations can be made:
Age exhibits the strongest positive correlation with the MMSE. This suggests that as individuals get older, there is an increased likelihood of higher risk of dementia. GDS value, which measures the severity of depression, also shows a positive correlation with the MMSE. A higher GDS value implies severe depression, and the positive correlation suggests that higher GDS values are associated with an increased risk of dementia. The financial status of individuals shows a positive correlation with the MMSE. This indicates that higher financial status may be associated with a lower risk of dementia.
Education level demonstrates the strongest negative correlation with the MMSE score. This implies that as the education level decreases, the risk of dementia increases. The MNA scores, specifically MNAa_tot and MNAb_tot, exhibit a weak negative correlation with the MMSE. Lower MNA scores indicate a higher risk of malnutrition. The negative correlation suggests that as MNA scores decrease and the risk of malnutrition increases, the risk of dementia also increases.
These findings highlight the importance of considering age, depression severity, education level, financial status, and nutritional status when assessing the risk of dementia or cognitive impairment. They provide valuable insights into the potential risk factors associated with dementia and the need for interventions targeting these factors to promote cognitive health and well-being among elderly individuals.

## Prediction Modelling
For this case study we will be utilizing two classification models. 

## Logistic Regression
Logistic regression is a statistical model for binary classification, predicting the probability of an event occurring or not. It's popular for its interpretability, efficiency, and ability to handle various types of variables. By using the sigmoid function, it maps predictions to probabilities between 0 and 1. Logistic regression offers interpretability through coefficients, handles large datasets, provides probabilistic predictions, detects outliers, and determines feature importance. However, it's most effective when the relationship between predictors and the outcome is approximately linear. Nonlinear relationships or complex interactions may require other algorithms like decision trees or neural networks.

## Support Vector Machine
Support Vector Machines (SVM) is a powerful algorithm for classification and regression tasks. It finds optimal decision boundaries and handles complex data using the kernel trick. SVM is robust, versatile, and widely applied in various domains. However, it lacks direct probabilistic outputs and requires careful feature selection and hyperparameter tuning.

## Scaling
Centering and scaling were applied to continuous variables, resulting in their mean being adjusted to 0 and standard deviation set to 1.
## Partitioning
The preprocessed data underwent a random split, where 70% of the data was allocated to the training dataset and the remaining 30% to the testing dataset. The split was performed using a specific seed number to ensure reproducibility.


## Results
The logistic regression classifier and SVM classifier were trained and used to generate predicted classes and probabilities. The performance metrics were computed based on the confusion matrix. ROC curves of the models were compared.

## Logistic Regression 
<img width="940" height="296" alt="image" src="https://github.com/user-attachments/assets/8b9e1e01-58cb-4474-a661-9a2bd86087e4" />
<img width="550" height="529" alt="image" src="https://github.com/user-attachments/assets/bb45009e-1535-42c7-8564-7d4069e9d9a5" />

One unit increase in Age (OR = 2.461) was associated with more than 2 times higher probability that the individual will have a dementia risk. Compared with GDS (OR = 1. .188) has nearly 18% higher chance of having a risk for dementia. 

## Support Vector Machine
<img width="514" height="553" alt="image" src="https://github.com/user-attachments/assets/f5faf884-2c97-4f16-ad25-ff7e9fa5ae08" />

## Performance Matrix
![image](https://github.com/user-attachments/assets/21484a75-fca7-4bb1-9b39-d4477801cbbd)

![image](https://github.com/user-attachments/assets/f96c73da-7255-4b86-8fb9-aeb9e731039d)

Based on the above performance metrics we can gain the following insights of the two models.
•	Accuracy: The accuracy metric measures the overall correctness of the model's predictions. In this case, LR has a slightly higher accuracy than SVM, indicating that LR is better at making correct predictions overall.
•	Kappa: The kappa coefficient measures the agreement between the predicted and actual values, considering the possibility of agreement by chance. A higher kappa value indicates a better agreement between the model's predictions and the true values. LR has a higher kappa than SVM, suggesting that LR performs better in capturing agreement beyond chance.
•	Sensitivity and Recall: Sensitivity, also known as true positive rate, measures the ability of the model to correctly identify positive instances. A higher sensitivity indicates a lower chance of missing positive cases. SVM has a slightly higher sensitivity than LR, implying that SVM is better at correctly identifying positive instances.
•	Specificity: Specificity measures the ability of the model to correctly identify negative instances. A higher specificity indicates a lower chance of misclassifying negative cases. LR has a higher specificity than SVM, indicating that LR is better at correctly identifying negative instances.
•	Precision and Positive Predictive Value (Pos Pred Value): Precision represents the proportion of correctly predicted positive instances out of all predicted positive instances. Pos Pred Value, also known as precision or positive predictive value, measures the proportion of true positive instances out of all predicted positive instances. LR and SVM have similar precision and Pos Pred Value, suggesting that both models are equally good at correctly predicting positive instances.

Overall, these metrics imply that LR outperforms SVM in terms of accuracy, capturing agreement beyond chance (kappa), and specificity. On the other hand, SVM performs slightly better than LR in terms of sensitivity. However, it's important to consider the specific context of the problem and the relative importance of these metrics to determine which model is more suitable for the given task.

## Conclusion
This report analyzes a ten-year dataset from mobile health care services in Hong Kong to gain insights into the health profiles of the elderly population. Logistic Regression outperforms Support Vector Machine in accuracy, kappa, and specificity, while SVM shows better sensitivity. The findings inform policymakers and healthcare providers for targeted interventions. The study provides a foundation for further research to enhance elderly well-being in the region.
