# Credit Risk Analysis

## Overview of the loan prediction risk analysis
The main goal of this analysis is to evaluate the performance of different machine learning models applied to a credit card data set from the LendingClub in order to predict the credit risk for clients. 
As part of the analysis, we will employ different techniques and models to compare the results and confirm what model can be considered as the most appropriate to obtain an accurate prediction

## Results
After execute the different models, here is a table as summary of the result including some screenshot as reference. 

|                    |     Oversampling   |        SMOTE       |    Undersampling   |     Combination    |    Random Forest   |      AdaBoost      | 
|--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|
| Balanced Accuracy  |        0.661       |        0.658       |        0.544       |        0.644       |        0.788       |        0.931       |
|        pre         |        0.99        |        0.99        |        0.99        |        0.99        |        0.99        |        0.99        |
|        rec         |        0.60        |        0.69        |        0.40        |        0.57        |        0.87        |        0.94        |
|        spe         |        0.72        |        0.62        |        0.69        |        0.72        |        0.70        |        0.92        |
|        f1          |        0.75        |        0.81        |        0.56        |        0.72        |        0.93        |        0.97        |

- Oversampling images
  <p align="center"><img src="https://user-images.githubusercontent.com/88695570/146699700-bfe82972-81f8-4a3b-9bbd-cdd994f3e1ed.png">

- SMOTE images 
  <p align="center"><img src="https://user-images.githubusercontent.com/88695570/146700008-028d2e1d-e264-424a-b48e-80327ee97a86.png">
  
- Undersampling images
  <p align="center"><img src="https://user-images.githubusercontent.com/88695570/146700033-a674f082-7980-4136-96f9-27991da12ce7.png">
  
- Combination images
  <p align="center"><img src="https://user-images.githubusercontent.com/88695570/146700039-35c700ff-9e08-4b4d-ab83-5e3e077c6d13.png">

- Random Forest images
  <p align="center"><img src="https://user-images.githubusercontent.com/88695570/146700373-1c2403e0-d26e-4880-9f5c-83a92e799fae.png">

- AdaBoost images
  <p align="center"><img src="https://user-images.githubusercontent.com/88695570/146700385-6f48cace-900e-46fc-9358-6e2409e65cfd.png">

## Summary

- Based on the results displayed on the table above, AdaBoost obtained the best average result in all the categories in comparison with the other models. This model would be the most appropriate for the credit card prediction.  
- The model with the lowest results in all the categories was "Undersampling". We don't recommend using this model for the credit risk prediction. 
- The second model which can be considerable as appropriate for the credit score analysis is the Random Forest. Despite of having the third highest values for specificity (70% still a considerable value to not erroneously classify anyone with a good credit score), the results justify the election of this model as a second best technique.
- Something additional to keep in mind for the model selection is the cost of misclassifying a person with a "bad" score as "good" score is larger than the cost of misclassifying someone with "good" credit as "bad" credit, that???s why precision is important. Considering the f1 (combining precision and recall) as parameter to rank the models, the third option could be the SMOTE. However, I still consider we should go for the AdaBoost as our more secure alternative.
