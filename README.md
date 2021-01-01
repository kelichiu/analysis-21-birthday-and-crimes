# 21st birthdays come with more Assault, Rape, and Murder arrests
In collaboration with [diegoarmaca](https://github.com/diegoarmaca) and Sharon Allman

## Summary of Findings
Through the replication data from The Minimum Legal Drinking Age and Crime by Christopher Carpenter and Carlos Dobkin (2015), we sought to elaborate on the findings of Billings (2014) in their research on the age-prohibition of alcohol and potentially increased propensity for crime.  We found that the most alcohol-consumption-related crimes of assault, rape, and murder all had statistically significant increases at age 21, while arson did not have a statistically significant increase. 

## Data: The Minimum Legal Drinking Age and Crime
The dataset is the replication data of The Minimum Legal Drinking Age and Crime by Christopher Carpenter and Carlos Dobkin (2015), which can be retrieved [here](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/27070#__sid=js0). The dataset contains 2922 observations and 144 variables. The observation is arrestee’s age in days relative to 21 on the day being arrested ranging from 17 to 24. For example, -30 indicates that the arrestee is a month away from turning 21, 60 indicates that the arrestee is 21 and two months old and 0 means the arrestee is arrested on their 21st birthday. The original crimes data was retrieved from California’s Monthly Arrest and Citation Register dated from 1979 to 2006, containing major crime types categorized by FBI: violent crime, alcohol-related offenses, property crime, illegal drug possession or sale, and all other offenses. The dataset contains the counts of arrests as well the arrest rates per 10,000 person-years for each crime for each observation. For our study, we followed the bandwidth of two years Carpenterr and Dobkin used; we sliced the dataset to include observations of people age 19 to 22 inclusive (from day -730 to day 729).  

An additional binary variable called mlda_and_over was created based on the days_to_21 variable, classifying MLDA and over as 1, and under MLDA as 0. Finally, the dataset was filtered by the columns with the high-alcohol usage crimes under analysis (Assault, Rape, Murder, and Arson). 

## Method: Regression Discontinuity Design (RDD)
Because the purpose of this paper is to validate the effect of the Minimum Legal Drinking Age (MLDA) over the most alcohol-influenced crimes, we conducted a Regression Discontinuity Design (RDD). The RDD estimates impact around the eligibility cutoff, in our case MLDA, as the difference between the average outcome for units on the treated side (MLDA and over) of the eligibility cutoff and the average outcome of units on the untreated (under MLDA) side of the cutoff (MLDA). 

According to the researchers of our reference study (Billings, 2014), after applying their research through several surveys to inmates and other techniques, they found the fifteen most affected crimes by alcohol consumption. For this investigation, we focused on the crimes classified as high-alcohol usage from that paper. These are Assault, Rape, Arson, and Murder, based on the role alcohol plays when an offender commits a given crime. 

### See the [PDF file](21_and_crimes.pdf) for R code, data visualization and full analysis
