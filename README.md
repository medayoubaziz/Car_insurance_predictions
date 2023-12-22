# Car_insurance-predictions
In this project i want to try and solve a classification problem so i choose this data set from kaggle.com: 
## Car Insurance Data
The company has shared its annual car insurance data , to find out the real customer behaviors i'm going to try and predict if or not the customer could claim the loan .
The data has 19 features from there 18 of them are corresponding logs which were taken by the company.

Here an example of some features and their relation with the target 
![téléchargement (1)](https://github.com/medayoubaziz/Classification-predictions/assets/145483390/d773ba5a-8c2c-4c03-810d-539ba810b5e3)

![téléchargement (2)](https://github.com/medayoubaziz/Classification-predictions/assets/145483390/da0267d0-8649-4ae8-8812-02c2d3f1b01a)

![téléchargement (3)](https://github.com/medayoubaziz/Classification-predictions/assets/145483390/595215fc-ce21-4f35-9d55-c404b0a61864)

![téléchargement (4)](https://github.com/medayoubaziz/Classification-predictions/assets/145483390/77230f59-382e-4550-92ce-7a958efb4923)


![téléchargement (5)](https://github.com/medayoubaziz/Classification-predictions/assets/145483390/4ae3fd6b-d665-43bd-809d-a831167b7672)

## Preprocessing : 
In this section i tried to fill the missing data of course after splitting so we could avoid data leakage : 
![Capture d'écran 2023-12-22 235808](https://github.com/medayoubaziz/Car_insurance_predictions/assets/145483390/5c7d003c-a805-4a9c-94b1-73f858e2dc9f)

## Target : 
Our target is the column 'OUTCOME'

![Capture d'écran 2023-12-22 235541](https://github.com/medayoubaziz/Car_insurance_predictions/assets/145483390/f5ccc2ff-5844-452d-b962-73165c7e33ff)

Our target is not well balanced 68% of the data is 0 and 32% is 1.

## Modeling & Evaluation :
I tried three models in this stage. 

DecisionTreeClassifier : 
![Capture d'écran 2023-12-22 234341](https://github.com/medayoubaziz/Car_insurance_predictions/assets/145483390/2e00832a-3155-4a27-83c4-53270da926e1)

KNN :

![Capture d'écran 2023-12-22 234505](https://github.com/medayoubaziz/Car_insurance_predictions/assets/145483390/fc6a99e2-4e6c-4457-bab7-404a6890591a)

LogisticRegression:

![Capture d'écran 2023-12-22 234639](https://github.com/medayoubaziz/Car_insurance_predictions/assets/145483390/f09f1df1-27d2-4d68-bead-4bafda959411)

After tuning the model with GridSearchCV and PCA , the best production model is the model3 without pca . 

For this data our false positive is when the outcome is 1 but the model predicted as 0 .
And for the false negative is when the outcome is 0 but the model predicted as 1 .

My recomondations for our stackholder is to try to be attentive to the credit score because with higher credit we see that the outcome tend to be 0 . 
But it is the opposite of the annual mileage , as it goes higher the outcome tend to be 1 .



