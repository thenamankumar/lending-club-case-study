# Problem Statement

The Lending Club data given contains information about past loan applicants and whether they ‘defaulted’ or not. The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc.

# Summary
The Lending Club dataset contains a lot of variables which tells us about the kind of loan taken and borrower's past transactions. In our analysis we have used this data to find what variables out of all creates an impact on whether the loan is fully repaid or defaulted.

We started from clearning the data, picking the right columns, filling null values and more. For the selected variables we performed univariate analysis by analyzing the spread of quantitative metrics and forming bands for each of them. For qualitative variables we did frequency plotting.

After analysing the spread of variables we performed Bivariate analysis to find relation between various variables and charged off loan percentages. Based on the initial results we did further detailed study in multivariate analysis.

We also did correlation study and pair plotting and found interesting insights.

## Variables Impacting Loan Default Percentage
- Loan Ammount
- Annual Income
- Interest Rate
- Instalment Amount
- Loan Purpose
- Debt to Income
- Inquiries in Last 6 Months
- Employment Length

### Loan Amount
- Higher the loan amount, higher the charged off loan percentage. Upto 27% for 25k+ loans.
- 75% of applications apply for loan amounting < 15K
- Most of the borrowers take loans upto 1-3 months of their income. Loans amounting to > 6 months of borrowers income has a much higher charged off loan percentage i.e. 32%.
- Most defaulters do not pay 50-85% of the loan principal amount.
- Strongly co-related with annual income. higher amounts are funded to people with higher annual income.o

### Annual Income
- Annual income in the range of 20K-40K has the most charged off loans percentage i.e. 17.75%.
- Contained a lot of outliers having very large amount of annual income which skewed all the plottings due to which they were removed based on IQR.
- Most borrowers have income in the range of 40K-70K.
- It slightly co-relates with the employment length.
- Higher loan amount at lower annual income has higher charged off loan percentage.

### Interest Rate
- Charged off loans percentage increases rapidly with increase in interest rates. Loans with 17%+ interest rates have 33% defaulter rate.
- Charged off loan percentage at higher interest rates is high irrespective of all other factors.
- Most of the loans are funded at the interest rate of 8-14%, while the interest rate goes as high as 24%.
- Higher amount loans have higher interest rates.
- Educational, House, Car, Debt Consolidation, and Moving loans are highly risky when the interest rates > 17%.

### Instalment Amount
- For most people instalment amount is < 300.
- Most people pay 4-9 percent of their monthly income as instalments.
- Loans with monthly instalment amount > 600 are at a higher risk of delinquency with charged off loan percentage being 18.88%.
- The charged off loan percentage increases linearly with increase in monthly installment amount.
- Borrowers paying 15-20 percent of their monthly income as instalment are more likely to not be able to repay their loans with charged off loan percentage being 21.69%.

### Loan Purpose
- Small business loans have the higher defaulter rate i.e. 28.5% irrespective of all other factors.
- For defaulted loans, house, small business and wedding loans have the higher percentage of principal amount not paid back.
- Medical and educational loans are risky when the borrowers are already paying 20-30 percent of monthly income on debt obligations other than the LC loan.
- The most popular purpose for loans is debt consolidation followed by credit card. While small business, house, debt consolidation loans have the highest average loan amount overall.

### Debt to Income
- Most borrowers spend 8-18% of their monthly income into debt obligations other than the LC loan.
- Borrowers having already paying 20-30 percent of their monthly income as other debt obligations are slightly at more risk of defaulting.
- The charged off loan percentage increases slightly with increase in debt to income.
- People with higher debt to income takes loans of slightly higher amount.
- People spend 30-40 percent of their monthly income into debt obligations including LC loan are at high risk of deliquency.
- Higher loan amount at higher debt to income ratio has higher charged off loan percentage.

### Employment Length
Assuming null records have 0 years of employment length
- Most borrowers have 1-3 years of employment length.
- Employment length slightly co-relates with annual income.
- People with 0 years of employment have the highest charged off loan rate i.e. 21.77%.
- Borrowers having no employment length record are known to be highly risky even when it can be seen that they are provided small amount loans at lower interest rates than others.
- Educational, credit card, wedding and debt_consolidation loans for borrowers having no or <1 year employment length record are highly risky.

### Inquiries in Last 6 Months
- Most people do 1 or fewer inquiries.
- People who do more than 2 inquiries have a much higher defaulter rate at 21%.

# Recommendations
For lowering the defaulter ratio following are the recommendations.

- Loan amounts greater than 6 months of borrower's income when their monthly income is more than 20K are highly risky. It is recommended not to provide such loans at all as the defaulter rate for such loans is up to 36%.
- Small Business loans funded at an interest rate of more than 8% are highly risky. The ones given at 5-8% interest rate have a healthy defaulter rate. It is recommended to give business loans at lower rates so that borrowers can focus and grow their business and have the ability to repay the loans.
- Educational loans where the total amount is more than 3 months of the borrower's monthly income are highly risky with a defaulter rate of 20%. It is recommended to fund smaller amounts of loans for education purposes.
- Borrowers who have made 2+ times inquiries in the past for loans amounting to more than 20K are at high risk of not repaying the loan. It is recommended to give lower amounts of loans to such people.
- When the debt to income for the borrowers is already 20-30 per cent, the loans amounting to 3+ months of borrowers’ monthly income are highly risky as the defaulter rate goes up to 33.73%. It is recommended to only give small amounts of loans to such people.
- Medical and educational loans are risky when the borrowers are already paying 20-30 per cent of monthly income on debt obligations other than the LC loan. It is recommended to give small loans in such cases.
