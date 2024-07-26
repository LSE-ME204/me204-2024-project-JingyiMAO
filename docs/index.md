# ME204 Final Project: Comparative Crime Report in North America: Baltimore vs. Vancouver (mainly focus on 2013-2016)


## Introduction
Understanding crime and its patterns is essential for developing effective crime prevention and intervention strategies. Comparing cities with different crime profiles can provide valuable insights into the underlying causes of crime and the effectiveness of various policies and programs. In this report, we aim to compare the crime and patterns between Vancouver, Canada, and Baltimore, United States. Both cities are prominent in their respective countries, yet they differ significantly in terms of safety and crime statistics. 
By collecting, cleansing and visualizing crime data from the two cities, this report aims to provide an intuitive way to analyse and understand the distribution and trends of crime in the cities; By analyzing various crime indicators, we can gain a better understanding of  the social and economic factors that influence these differences.


## Background Information: Crime Statistics Overview
Here is some background information about two cities. Thses background information provides us a rough guess of the data we are about to obtain.

### Vancouver:

- Population: Approximately 675,000
- Crime Rate: Lower compared to many major North American cities.
- Violent Crime: Relatively low, with sporadic incidents.
- Property Crime: More prevalent, particularly in densely populated urban areas.

### Baltimore:

- Population: Approximately 600,000
- Crime Rate: One of the highest in the United States.
- Violent Crime: High, including homicides, assaults, and robberies.
- Property Crime: Also high, with significant rates of burglary and theft.

It seems Baltimore struggling with higher crime rates, encompassing both violent and property crimes, despite its smaller population. In contrast, Vancouver maintains a relatively low overall crime rate with its larger population. 


# Part I: Data Collection

We collected crime data for both cities from Kaggle public sources by generating API. These raw data cover a wide range of crime types including but not limited to, theft, assault, and homicide, and we store them into two separate dataframe for further data cleaning work. The detailed steps are as follows:

1. Create a Kaggle Account
Sign up and log in to your Kaggle account. if you don't have an account, create one first.
2. Generate an API key:
Click on your profile picture in the top right corner, then go to "Account". Scroll down to the "API" section and click on "Create New API Token".
This will download a file named kaggle.json containing your API credentials.
3. Install the Kaggle API
Install the Kaggle API client on your computer using the following command:
`pip install kaggle`
4. Configure the API Key
Place the kaggle.json file in the appropriate location. Usually, this is in the .kaggle directory within your home directory.
5. Now we are able to use the Kaggle API to download a dataset!


# Part II: Data Cleaning

The data collected in its raw form often contains much redundant information, inconsistent data formats, and missing values. To ensure data accuracy and consistency, we performed some data cleaning steps including removing invalid crime records, standardizing crime-time data formats (e.g., date, time, etc.) and reclassifying the crime types.  

When the data cleansing is complete, we merge the two dataframes into one for the next data visualization and analysis.

# Part III: Exploratory Data Analysis (EDA)





## Baltimore
## Vancouver
# Summary

In summary, Vancouver and Baltimore present stark contrasts in terms of crime rates. Vancouver, with its larger population, maintains a relatively low overall crime rate, particularly regarding violent crime, though it does experience a higher incidence of property crime in urban areas. In contrast, Baltimore, despite its smaller population, struggles with very high crime rates, encompassing both violent and property crimes. This significant disparity highlights Baltimore's challenges in managing crime compared to the generally safer environment in Vancouver.

Violent Crime Comparison
Vancouver:

The city's violent crime rate is significantly lower than Baltimore's. In 2023, Vancouver reported a homicide rate of about 2 per 100,000 residents.
Assault and robbery rates are also lower, attributed to effective law enforcement and community programs.
Baltimore:

Baltimore faces a severe violent crime issue, with a homicide rate of approximately 57 per 100,000 residents in 2023.
The city struggles with high rates of assault and robbery, largely driven by socioeconomic disparities and gang violence.
Property Crime Comparison
Vancouver:

Property crime, such as theft and burglary, is more common in Vancouver compared to violent crime. The overall property crime rate is about 45 per 1,000 residents.
Efforts to reduce property crime include community policing and neighborhood watch programs.
Baltimore:

Property crime in Baltimore is also high, with a rate of about 65 per 1,000 residents.
Economic challenges and high poverty rates contribute to the prevalence of property crimes in the city.

Vancouver:

Higher standard of living and lower poverty rates compared to Baltimore.
Strong social support systems and community engagement help mitigate crime.
Baltimore:

High levels of poverty and unemployment contribute to the city's crime rates.
Socioeconomic disparities and lack of resources in many neighborhoods exacerbate the crime problem.
Law Enforcement and Community Programs
Vancouver:

Community policing and proactive law enforcement strategies are key to Vancouver’s lower crime rates.
Programs focusing on youth engagement and crime prevention have been effective.
Baltimore:

Law enforcement faces significant challenges due to the high crime rates and community mistrust.
Efforts are ongoing to improve police-community relations and implement effective crime reduction programs.
Conclusion
Vancouver and Baltimore present a stark contrast in crime statistics and patterns. Vancouver, with its lower crime rates and proactive community programs, offers a safer environment compared to Baltimore, which struggles with high levels of violence and property crime. The differences highlight the impact of socioeconomic factors, law enforcement strategies, and community engagement in shaping the safety and security of a city.

By understanding these dynamics, policymakers and community leaders can develop more effective strategies to combat crime and improve the quality of life in urban environments.


![Title : Amount of Crime in Baltimore by Hour](./figure/Amount of Crime in Baltimore by Hour.html)


