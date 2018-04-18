# PHBS_TQFML/Factors affecting bank competitive power---Evidence from emerging countries
王迪雅 Wang Diya 1701213099 <br>
王锦烽 Wang Jinfeng 1701213103 <br>
颜鹏 Yan Peng 1701213130 <br>
朱存正 Zhu Cunzheng 1701213170 <br>
## Project Description
Along with the rapid development of nearly thirty years of China financial business, more and more people started to realize the importance of the banking market. Bank, a financial institution which operates monetary credit businesses and is established in accordance with the law, is the product that commodity money economy develops to a certain stage. In our project, we will find out several factors that determine the competiveness of a bank in the emerging countries. At the same time, we will figure out which is the best features to measure the competitiveness of a bank and the accuracy of our predictions. <br>
See the [Proposal](https://github.com/diyawang/PHBS_TQFML/blob/master/Project/Project_proposal.pdf)
## Features
Features | Description | Data
---------|------|-------
LC| Personnel expenses (thousand $) |BankScope
TotIntC|Total interest expense (thousand $)	|BankScope
IntCR|	Interest expense/average interest-bearing liability	|BankScope
TotD|	Total deposits, money market and short-term funding (thousand $)	|BankScope
OtherC|	Other operating expenses (thousand $)	|BankScope
FixA|	Fixed assets (thousand $)	|BankScope
LiqA|	Liquid assets (thousand $)	|BankScope
TotCap|	Total capital (thousand $)	|BankScope
TotNonIntC|	Total non-interest expense (thousand $)	|BankScope
Overheads|	Overheads (thousand $)	|BankScope
IntR|	Gross interest & dividend income (thousand $)	|BankScope
NonIntR|	Total non-interest operation income (thousand $)	|BankScope
NI|	Net income (thousand $)	|BankScope
GDPG|	% change in real GDP, over previous year	|EIU Countrydata
Inflation|	Percentage change in consumer price index in local currency (period average) (thousand $)	|EIU Countrydata
r|	Money market interest rate (%)	|EIU Countrydata
GDPper|	GDP at purchasing power parity (PPP), divided by population (thousand $)	|EIU Countrydata
FP_A|	Foreign bank penetration_assets (thousand $)	|Jeon et al. (2016)
FP_N|	Foreign bank penetration_number	|Jeon et al. (2016)
share|	Market share	|BankScope
HHI|	Herfindahl-Hirschman Index, defined as the sum of the squared shares of bank assets to total banking sector assets within a country in a year	|BankScope
TotA|	Total assets (thousand $)	|BankScope
Liquidity|	Liquid assets/ total deposits & borrowing	|BankScope
ROAA|	Average ROA	|BankScope
Efficiency|	Non-interest expense/ average assets	|BankScope
Risk|	Loan loss reserve/ gross loan	|BankScope
competition|	The competitive level of a bank based on the Lerner index (1 represents good competitive ability, and 0 represents poor competitive ability)	|BankScope and our classification
## Methods
Step1: Building good training sets and data preprocessing.                                      
Step2: Dimensionality reduction to figure out the best features.<br> 
Step3: Using Preceptron/Logistic Regression/(Kernel) SVM/Decision Tree/Random Forest/KNN/Majority Voting to predict the competitiveness of a bank.<br> 
Step4: Using holdout cross-validation and k-fold cross-validation to select the best model for our predictions.<br> 
Step5: Obtaining our results and the accuracy of our prediction.<br> 
## Data soures
We use annual data of 35 emerging countries in Eastern and Central Europe, Latin America and Asia during the period of 2001-2014 from Bankscope Database, which contains the financial information of most banks in the world, provides us most of the bank-level data. Bankscope Database is also the most frequently cited database in many early works. We also collected macroeconomic data of each country from EIU Countrydata, which provides macroeconomic and historical data for more than 200 countries and regions.
