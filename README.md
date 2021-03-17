### Human-Resources-Retention
#### Purpose: Figuring out which employees may quit using Machine Learning and Deep Learning

#### Step 1- Load the Main HR Database Records

#### Step 2- Load the Evaluation and Employee Satisfaction Data

#### Step 3- Join the datasets on Employee id

main_df = hr_df.set_index('employee_id').join(emp_satis_eval.set_index('EMPLOYEE #'))

main_df = main_df.reset_index()

#### Step 4- Replace the missing values in columns 'satisfaction_level'	and 'last_evaluation' with mean

#### Step 5- Remove the columns insignificant to our target variable 'left'

#### Step 6- Perform One Hot Encoding on Categorical Data- 'department','salary'

#### Step 7- Preparing dataset for Machine learning

-Split the dataset in 70:30 ratio 

-Normalize the data using StandardScalar

X_train = sc.fit_transform(X_train)
X_test = sc.transform(X_test)

### LOGISTIC REGRESSION MODEL

#### Accuracy, Confusion matrix and Classification report
![image](https://user-images.githubusercontent.com/80466173/111455285-9e161680-873b-11eb-9106-bdf27ddb7408.png)

### RANDOM FOREST CLASSIFIER

#### Accuracy, Confusion matrix and Classification report
![image](https://user-images.githubusercontent.com/80466173/111455345-aff7b980-873b-11eb-857f-61b61cd55a5d.png)


### DEEP LEARNING

#### Loss chart

![1](https://user-images.githubusercontent.com/80466173/111454186-622e8180-873a-11eb-8f54-c95fab948876.PNG)

#### Accuracy chart
![2](https://user-images.githubusercontent.com/80466173/111454194-65297200-873a-11eb-86a6-8ef018dd4c5f.PNG)

#### Confusion matrix and Classification report

![image](https://user-images.githubusercontent.com/80466173/111455648-154baa80-873c-11eb-93eb-66621946eadf.png)

