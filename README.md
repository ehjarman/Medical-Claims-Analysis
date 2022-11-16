# Medical-Claims-Analysis

### Overview of Project
#### Purpose
The goal of this project is to look deeper into the descriptive statistics of beneficiaries of Medicare. 
This analysis uses public to use, synthetic medical claims data (SynPUFs) generated from a 5% population of real Medicare medical claims data from 2008-2010.
This data was obtained from https://www.cms.gov/Research-Statistics-Data-and-Systems/Downloadable-Public-Use-Files/SynPUFs/DE_Syn_PUF.
This data set contains data from over 100,000 beneficiaries claims and 800,000 inpatient / outpatient claims. Summaries of data included in these claims can be seen below.
This data was extracted, organized, and cleaned before beginning to analyze the data.

### Analysis
To better understand the populations of beneficiaries included in the data, descriptive statistics of the data were found. 
The distribution of the number of claims per beneficiary in inpatient and outpatient settings was found.
A summary of the gender, race/ethnicity, and birth years of beneficiaries per inpatient and outpatient claims was found,
as well as the ratio of beneficiaries with reported chronic illnesses. 
Asummary of the reimbursement costs per source for inpatient and outpatient claims was generated.

Secondly, an investigation of the relationship between the age of the beneficiary and the number of chronic illnesses reported was completed.
A scatter plot was created to visualize the relationship between age and number of chronic illnesses, and a linear regression was fit.
The model was evaluated. 
To investigate this further, one specific condition was selected (Alzheimer's Disease). 
The relationship between age and the presence of Alzheimer's Disease was visualized with a scatter plot and was evaluated.

### Results
#### First look into the data:
Inpatient claims data size: (66773, 81)

Outpatient claims data size: (790790, 76)

Beneficiary claims data size: (116352, 32)

#### Distrbution of Number of Claims per Beneficiary in Inpatient and Outpatient Settings (2008-2010)
<img width="388" alt="Screen Shot 2022-11-16 at 10 42 15 AM" src="https://user-images.githubusercontent.com/103863038/202265877-929b84a8-88d4-45f0-865f-bb9f8d28e0b9.png">

#### Summary of Gender and Race/Ethnicity Percentages in Beneficiary Population
<img width="350" alt="Screen Shot 2022-11-16 at 10 42 49 AM" src="https://user-images.githubusercontent.com/103863038/202265967-5bbfa08f-39a5-489e-8e90-2ec0a3fd613c.png">

#### Distribution of Year of Birth of Beneficiaries for Inpatient and Outpatient Claims
<img width="456" alt="Screen Shot 2022-11-16 at 10 43 40 AM" src="https://user-images.githubusercontent.com/103863038/202266123-0c7e68da-abd8-4641-9922-d55e2d85a7e4.png">

#### Summary of Reimbursement Costs per Source for Inpatient and Outpatient Claims
<img width="511" alt="Screen Shot 2022-11-16 at 10 44 30 AM" src="https://user-images.githubusercontent.com/103863038/202266295-2147aa9e-1c9b-40c1-a82b-fb2c7fe8430d.png">

#### Prevalence of Reported Chronic Illnesses in Beneficiary Population and Mean Ages for Each Illness
<img width="766" alt="Screen Shot 2022-11-16 at 10 45 48 AM" src="https://user-images.githubusercontent.com/103863038/202266533-af0c55a5-45a3-4a37-9877-a704a79cf5f6.png">

#### Plot of Chronic Illness Distribution in Beneficiary Population
![image](https://user-images.githubusercontent.com/103863038/202266769-36d7e2b4-1f2b-45e3-8517-fed7e0f403fa.png)

#### Scatter Plot of Age of Beneficiary vs Number of Chronic Illnesses Reported
![image](https://user-images.githubusercontent.com/103863038/202266992-931ff5ad-9224-48d8-a7ed-fca701866aac.png)

#### Evaluation of Linear Regression Model (Fit to Age vs Number of Chronic Illnesses)
<img width="333" alt="Screen Shot 2022-11-16 at 10 49 19 AM" src="https://user-images.githubusercontent.com/103863038/202267280-31dae9f5-1328-479b-8039-a546b754a749.png">

#### Scatter Plot of Age of Beneficiary vs Presence of Alzheimer's Disease
![image](https://user-images.githubusercontent.com/103863038/202267410-71d8871c-09ff-46f5-80ff-a1af1bbf9067.png)

#### Average Age of Beneficiaries with Alzheimer's Disease
<img width="525" alt="Screen Shot 2022-11-16 at 10 51 02 AM" src="https://user-images.githubusercontent.com/103863038/202267661-0da905c8-f132-4a0f-ad91-d927ffc339ae.png">


### Discussion
Which program resulted in a higher weight increase / week?
Looking at the data, the sample size was rather small unfortunately. 
There were only 3, 4, and 3 deadlift, squat, and bench training days recorded in program 2.
Thus it was unlikely to get accurate comparisons between program 1 and program 2. 
However, the average weight increase / week was higher in program 1 for all lifts. 
This may have been due to cofounding variables; strength increases very quickly initially followed by a slow in progression. 

#### Initial look into the data
A summary of the data was first created. 
The data includes nearly 70M data points across over 100k beneficiaries.
Most of these beneficiarys' claims come from outpatients settings, 
with the population having a majority of white females. 
The birth year of the beneficiaries is even distributed from 1924 to 1943.

The mean total reimbursement cost per inpatient and outpatient claims was found to be $2562.38 and $845.45, respectively. 
This spans across billable procedures / services.
The majority of this reimbursement was paid by Medicare, followed by the beneficiary, then 3rd Party Payers.

#### Anaylsis of The Presence of Chronic Illness in Beneficiaries
An analysis was conducted on the relationship between age and the number of chronic illnesses present in beneficaries.
First the percentage of beneficiaries with 11 of the most relevant chronic illnesses was generated.
The frequently occuring illness was found to be ischemic heart disease at 42% of the population, 
followed by diabetes (37%), heart failure (28%), depression (21%), and Alzheimer's disease (19%).
This ranking is not suprising considering the mean elderly age of the population represented in beneficiaries dataset.

A scatterplot was generated and a linear regression was fit the assess the relationship between age of the beneficiary and total number of reported chronic illnesses.
Observing the scatterplot, no immediately identifiable relationship between the variables. 
Furthermore, evaluating the linear regression yielded that there was no strong relationship between age and total number of chronic illness.
The regression score was nearly zero (0.008) and the root mean squared, mean squared error, and mean absolute error were all indicated the model was not a good fit.

This was further investigated to potentially find a reason no relationship was observed between age and total number of chronic illnesses.
The age of beneficiaries vs the presence of Alzheimer's disease was analyzed to investigate this relationship on a closer level.
No logistic relationship was observed in the scatter plot.
This was interesting, as the data was reporting the presence of Alzheimer's disease in beneficiaries as young as 28 years old.
According to the NIH, the average age of onset for Alzheimer's disease is in the mid-60's.
This difference may be due to the generation of synthetic medical claims data may lead to inconsistencies with authentic data.

#### What's next?
It would be interesting to look deeper into the relationship between chronic illness and age.
Though no relationship was observed between age and the total number of chronic illnesses,
specific illnesses may have a relationship with age that could be used to predict the probability of that illness.
Furthermore, it would be intriguing to examine the breakdown of costs / reimbursement sources per demograph of the beneficiary population, 
and the locations in which these beneficiaries are treated. 
Examining this relationship could shed light into the finacial burden on certai populations,
how certain demographics are treated,
and how socioeconomic status can affect the healthcare received.




