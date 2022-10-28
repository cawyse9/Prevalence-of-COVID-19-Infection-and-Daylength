# Effect of Daylength on the Prevalence of COVID19 in Europe 

## Background
On Christmas Eve 2019, a sample collected from a patient in China with unidentified pneumonia which was later found to contain the first genomic evidence of a novel coronavirus (SARS-CoV-2).  Further patients with viral pneumonia presented to hospitals in Wuhan over the following days, and on New Year’s Eve, the WHO office in China notified its regional point of contact of a case of “viral pneumonia”.  As 2020 dawned, the world was on the brink of a global pandemic that would infect at least 50 million people across the world and kill over 2 million by November 2020 (WHO).  The pandemic initiated an unprecedented global quarantine as authorities struggled to contain the transmission of the disease caused by SARS-CoV-2, COVID19.  

Increasing human population, travel and migration mean that COVID19 is likely to be the first of a succession of 21st century pandemics.  Understanding the complex interaction between host, pathogen and environment that determines susceptibility to infectious disease is now one of the most important challenges for medicine and science. 

Almost all infectious respiratory viruses, including established coronaviruses, cause winter-time infection, (Dowell, 2004), and despite popular belief, temperature is an unlikely cause of this increased prevalence (Eccles, 2015).  For example, viral disease is seasonal in tropical regions where temperature and humidity are constant (Bloom-Feshbach 2013; Tamerius 2011) and outbreaks of influenza occur annually and simultaneously at latitudes that are oceans apart (Lofgren 2007) regardless of variations in local climatic conditions and human behaviour. 

There is increasing evidence that the capacity of the immune system to defend against infection has an endogenous seasonality with reduced function in winter, and that this might drive wintertime disease outbreaks (Dowell 2001; Stevenson, 2005).  In support of this, respiratory viruses can be isolated from human volunteers at all times of the year, even though the diseases they cause occur in winter (Lee 2012).  Seasonality is one of the most predictable aspects of viral infection, and one of the least understood.  Studies of the host and environmental factors that generate seasonality might help curtail transmission of SARS-CoV2 and prevent escalation of the inevitable future outbreaks of novel viral infections to pandemics.  It is not yet known if COVID19 is a seasonal disease, but this is highly likely as all existing circulating coronaviruses cause seasonal disease (Li, 2020). 


##	Objective 
The objective of this study is to investigate if the prevalence of COVID19 infection during the 2020 pandemic was associated with daylength, independent of confounding factors such as temperature, testing, population and economic status.

## Methods
### Data Import and Processing
The data on EU incidence of COVID-19 were checked to confirm csv format, and then processed to generate a single dataset relating cases, tests and deaths per week to changes in outdoor temperature and latitude in European Countries affected by COVID19.  Missing data were detected by searching for a panel of possibilities including 'NA', 'NULL', punctuation mark, and re-coded as missing values.

Unemployment and income status were used as proxy measures of the economic status of each country.  Data on latitude, daylength and outdoor temperature were acquired from information provided by the Global Monitoring Division of the US Government National Oceanic and Atmospheric Administration.  The date recorded for case numbers and deaths, and for environmental data was standardised across all the datasets to average numbers per week.  The unit of time used in all further analysis was week number during 2020, ranging from 1-42.  The variable “income group” and “country code” were recoded as categorical variables, with 5 and 42 levels, respectively.

The codes used to indicate country were standardised across datasets to three-digit (iso3 format.  At this point, it was possible to merge all data with reference to (i) country name and (ii) week number to yield a final table of COVID19 cases and deaths, by country, week and environmental factors (daylength, latitude)

All analyses were implemented using Python 3.8 programming language, using pandas,
Matplotlib, seaborn, linearmodels, and statsmodels libraries.

### Outcome Variable 
It was elected to confine the analyses to times of evidence of ongoing exposure to COVID19, to minimise the modulation of the outcome variable by non-environmental factors linked to disease exposure.  Ongoing exposure was defined as >1 death per week.  The effects of environmental factors such as daylength are more easily assessed by investigating periods of active infection.  In other words, susceptibility to infection can only be assessed while the disease is spreading.  There are no data available on social and travel restrictions in this study, so it was not possible to derive a more accurate measure of the possibility of exposure to SARS-CoV-2. 

### Linear Modelling
Linear regression models were applied to investigate the association between predictor variables and the study outcome (COVID19 cases).  Ordinary least squares linear regression models were applied as follows: 
yi = αi +βxi + ϵi
where y¬i is an outcome variable, and β and ϵi are regression coefficients and error terms, respectively.  Mixed models that incorporated time and country as random effects were also  applied:
yit = αi + γt + β′xit + ϵit
where αi is the country effect and γi is the time effect, β contains the variables of interest, temperature, etc, αi are country-specific components and ϵit are errors that are independent of αi and the covariates xit.  This model allowed for the autocorrelation caused by inclusion of the week number variable in the model (time entity) and for the non-independence induced by including data from multiple countries (entity).
Linearity, equal variance and normality of residuals were investigated to ensure that the data did not violate the assumptions of linear regression.  Data are presented as mean and sd, or median and interquartile range, as appropriate.  Statistical significance was accepted at p<0.05.


