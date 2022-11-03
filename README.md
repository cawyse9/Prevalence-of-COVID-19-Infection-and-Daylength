# Effect of Daylength on the Prevalence of COVID19 in Europe 

<img align="right" src="https://user-images.githubusercontent.com/29300100/199701088-e4a5b849-e868-48b7-ae50-ee840b2c4121.png" width="400">

## Background
On Christmas Eve 2019, a sample collected from a patient in China with unidentified pneumonia which was later found to contain the first genomic evidence of a novel coronavirus (SARS-CoV-2).  Further patients with viral pneumonia presented to hospitals in Wuhan over the following days, and on New Year’s Eve, the WHO office in China notified its regional point of contact of a case of “viral pneumonia”.  As 2020 dawned, the world was on the brink of a global pandemic that would infect at least 50 million people across the world and kill over 2 million by November 2020 (WHO).  The pandemic initiated an unprecedented global quarantine as authorities struggled to contain the transmission of the disease caused by SARS-CoV-2, COVID19.  

Increasing human population, travel and migration mean that COVID19 is likely to be the first of a succession of 21st century pandemics.  Understanding the complex interaction between host, pathogen and environment that determines susceptibility to infectious disease is now one of the most important challenges for medicine and science. 

Almost all infectious respiratory viruses, including established coronaviruses, cause winter-time infection, and despite popular belief, temperature is an unlikely cause of this increased prevalence.  For example, viral disease is seasonal in tropical regions where temperature and humidity are constant and outbreaks of influenza occur annually and simultaneously at latitudes that are oceans apart regardless of variations in local climatic conditions and human behaviour. 

There is increasing evidence that the capacity of the immune system to defend against infection has an endogenous seasonality with reduced function in winter, and that this might drive wintertime disease outbreaks.  In support of this, respiratory viruses can be isolated from human volunteers at all times of the year, even though the diseases they cause occur in winter.  Seasonality is one of the most predictable aspects of viral infection, and one of the least understood.  Studies of the host and environmental factors that generate seasonality might help curtail transmission of SARS-CoV2 and prevent escalation of the inevitable future outbreaks of novel viral infections to pandemics.  It is not yet known if COVID19 is a seasonal disease, but this is highly likely as all existing circulating coronaviruses cause seasonal disease. 


##	Objective 
The objective of this study is to investigate if the prevalence of COVID19 infection during the 2020 pandemic was associated with daylength, independent of confounding factors such as temperature, testing, population and economic status.

## Data Analysis
Data on COVID19 cases, tests and deaths in Europe over the course of the pandemic in 2020 were matched with data on daylength and outdoor temperature for each week and location. Linear regression analysis was applied to assess the association between COVID19 infection and daylength, while adjusting for potential confounding factors (population, tests, outdoor temperature and economic status). 

Details of the analysis and results are [here](https://github.com/cawyse9/Prevalence-of-COVID-19-Infection-and-Daylength/blob/main/Python%20Code/COVID_daylength_v1.pdf)  

Python notebook is [here](https://github.com/cawyse9/Prevalence-of-COVID-19-Infection-and-Daylength/blob/main/Python%20Code/project211220.ipynb)

## Conclusion
There was some evidence for a negative linear relationship between COVID19 case numbers and daylength, but it was not possible to eliminate strong collinearity with outdoor temperature. The results of this study support an association between COVID19 and daylength, that could be mediated partly through the effects of outdoor temperature.

## Acknowledgements
This project was submitted as part of the coursework required for the module, "Programming in Python" for an a MSc (Data Analytics) course at UCD in 2020.
