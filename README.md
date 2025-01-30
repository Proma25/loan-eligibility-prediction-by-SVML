# loan-eligibility-prediction-by-SVML
**INTRODUCTION:**  A loan is a sum of money that one or more individuals or companies borrow from banks or other financial institutions so as to financially manage planned or unplanned events, and the core business of banks. But when it comes to deciding whether the applicant’s profile is relevant to be granted with loan or not, banks have to look after many aspects. Using Machine Learning algorithm, using Python, it would be predicted whether a candidate’s profile is relevant or not using certain features.  As main profit comes directly from the loan’s interest. repayment of loans becomes crucial.


**PROPOSED METHODOLOGY**:
Data lays the foundation of the project. 
The dataset contains 13 attributes, and Loan_ Status is the target variable,
**Feature Selection:**
	Loan:	A unique id 
	Gender:	Gender of the applicant Male/female
	Marital status:	Marital Status of the applicant, values will be Yes/ No
	Dependence:	It tells whether the applicant has any dependents or not.
	Education:	It will tell us whether the applicant is Graduated or not.
	Self_Employed:	This defines that the applicant is self-employed i.e. Yes/ No
	ApplicantIncome:	Applicant income
	CoapplicantIncome:	Co-applicant income
	LoanAmount:	Loan amount (in thousands)
	Loan_Amount_Term:	Terms of loan (in months)
	Credit_History:	Credit history of individual’s repayment of their debts
	Property_ Area:	Area of property i.e. Rural/Urban/Semi-urban 
	Loan_status:	Status of Loan Approved or not i.e. Y- Yes, N-No 

 **** ALGORITHMS USED:******
  Machine is trained using labelled data
 The algorithm learns from labelled training data and predicts outcomes for unseen data.

 Importing Libraries and Dataset:
  
•	Pandas – To load the Dataframe
•	Matplotlib – To visualize the data features i.e. barplot
•	Seaborn – To see the correlation between features using heatmap


Comparing two variables to see how the target variable is affected by different factors##

number of people who take loan as group by Credit history:
Credit_History
1.0    475
0.0     89

number of people who take loan as group by marital status:
Married
Yes    398
No     213
That is, MArital status affects the loan eligibility in apostive way. More married people are eligible for loan.

number of people who take loan as group by dependents:
Dependents
0     345
1     102
2     101
3+     51
Lesser the number of dependents , more the people are eligible.

**Challenges faced:**
1) The data for loan amount contains a few outliers and the data appears right skewed. To fix this challenge, the logarithmic values of the loan amount would be useful.
2) Also, there appears some missing values. The categoriacal values which appears to be missing, are replaced by modal values and the numerical data is replaced by mean values.
**Supervised MAchine learning algorithm:**
According to the need of the data, we need to classify whether or not a person is eligible for loan, we need to specify classification algorithms, and check their accuracy.
To start with, 
	DECISION TREE ALGORITHM: This is actually a classifier. But the accuracy is 70%, it is required to look for some better means.
        K Nearest Neighbours: The accuracy come out to be 80%, there re scopes of better accuracy.
	Naive Bayes: The accuracy comes out to be 83%, the best among the three.


**Final Outcome:**
 result_df = pd.DataFrame({'Loan_ID': df['Loan_ID'], 'Prediction': pred})
print(result_df),,,,,,,,,,,,,,,,, The final Outcome : The loan_id s showing 1 are the ones which are eligible for loan and loan_id s showing 0 are the ones which are ineligible for loan.
After the completion, it is still advisable to check each of the eligible applicants hitory and background before the final approval.






 
