# Credit Risk Model

In this repo, we will be exploring dataset contains all available data for more than 800,000 consumer loans issued from 2007 to 2015 by Lending Club: a large US peer-to-peer lending company. There are several different versions of this dataset. We have used a version available on kaggle.com.  
You can find it here: https://www.kaggle.com/wordsforthewise/lending-club

For loan business, repaymment of the debt(together with interest rate) is the main revenue stream. However, it comes with the risk that the borrowers are not able to repay debt(default) which will cause losses to the company. Hence, credit risk modeling has to be taken to minimize the risk.

## Expected Loss
In this model, we are going to estimate `Expected Loss`(Amount of the lender might lost) from a given amount of loan

```
Expected Loss = PD*EAD*LGD
```
Where 
1. __Probability Default(PD)__ is the probability of a given loan to default.  
2. __Exposure at Default(EAD)__ is the total value that a lender is exposed to when a borrower defaults.  
3. __Loss Given Default(LGD)__ is the proportion of the total exposure that cannot be recovered(cannot cover by collateral) once a default has occured.

Here we will do 3 models to predict `PD`,`EAD` and `LGD`.  

### Example
If a loan amount is $400,000, probability default = 0.25. At the time of default, the borrower has repaid $40,000, so the outstanding balance is $360,000. Also, the lender can sell the borrower's house(collateral) for $342,000.

In this case, PD will be 0.25, EAD will be $360,000 and LGD will be ($360,000-$342,000)/$360,000 = 0.05

```
Expected Loss = PD*EAD*LGD = 0.25*$360,000*0.05 = $4,500
```
