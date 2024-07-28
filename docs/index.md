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

When the data cleansing is complete, we merge two dataframes into complete one for the next data visualization and analysis. For better storing, retrieving, managing and ensuring data security, we create a SQLite crime database and stored our crime data into a table inside crime database.


# Part III: Exploratory Data Analysis (EDA)

EDA is crucial in the data analysis process as it helps in making sense of data, guiding further analysis, and providing a foundation for building predictive models. Since I am still in the initial stages of learning and becoming familiar with the process, I will only do some simple EDA and will mainly focus on data visualization and comparison in this report. Here are three main themes I am going to explore:
- Crime Count by Hour
- Different Types of Crimes
- Geographic Distribution of Crime Incidents

The crime data used for EDA comes from the years 2013 to 2016 for both cities, since these four years represent the only period during which the cirme data overlapping in timeframe for two cities. By restricting our analysis to this overlapping timeframe, we ensure that the temporal alignment of the datasets mitigates the potential for bias and inconsistency that could arise from disparate data collection periods. This approach enhances the validity of our findings by enabling a robust and equitable comparison of crime trends and patterns across the two cities.

## Crime Count by Hour

Here is the histogram of crime count by hour of Baltimore and Vancouver:

<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Total_Amount_of_Crime_by_Hour(2013-2016).html"></iframe>

Overall, crime is more frequent in Baltimore compared to Vancouver, which aligns with our previous guess in Background Information session. The hourly distribution of crime counts in Vancouver and Baltimore reveals significant patterns that are critical for understanding the temporal dynamics of criminal activity in these two cities. In both Vancouver and Baltimore, crimes rates tend to peak during the late evening and early morning hours, with a noticeable decline during the early morning hours around 4 AM to 6 AM. However, Baltimore exhibits a more pronounced spike in criminal activity between 10 PM and 2 AM, potentially indicating higher levels of nighlife-related incidents or reduced law enforcement visibility. In contrast, Vancouver shows a relative smoother distribution with smaller peaks and troughs throughout the day. These patterns suggest that while boh cities experience heightened criminal activities during nighttime hours, the intensity and specific timing of these peaks vary, reflecting differences in local socio-economic factors, law enforcement practices and community behaviors. Further exploration and analysis are anticipated, but our report is limited to this scope.


## Different Types of Crimes

Next, I will attempt to compare the differences in crime types between two cities. Pie charts can clearly and intuitively display different types of crimes and their proportions, making them very useful for comparison and analysis. However, since 'ggplot' is not well-suited for displaying pie charts, we will use bar charts instead to represent the crime types in the two cities.
I also attempted to change the bar chart colors to be more colorblind-friendly using `scale_fill_viridis_d()`, but after several attempts, I was still unsuccessful. Therefore, I had to use custom-defined colors to achieve the goal of colorblind accessibility.

Here is my initial attempt at plotting the comprehensive range of crime types in both cities over the period from 2013 to 2016:
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Overall_Crime_Type_Count.html"></iframe>
From this chart, it is evident that there is a significant disparity in the total number of different types of crimes, with those types having lower total counts being nearly indiscernible in the visualization. To facilitate a clear comparison, the y-axis (crime amount counts) of the bar chart will be modified to a logarithmic scale.

After rescaling the y-axis to a logarithmic scale, we obtained a more informative bar chart.
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Overall_Crime_Type_Count_log.html"></iframe>

By generating the same bar chart plot for both Baltimore and Vancouver, we produced the two charts shown below:
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Type_Count_in_Baltimore.html"></iframe>

<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Type_Count_in_Vancouver.html"></iframe>

The types of crimes in Baltimore and Vancouver exhibit many similarities and differences.Both cities report several distinct crime types, with theft being the predominant crime in each. This highlights a shared challenge in property-related offenses that require targeted interventions in both cities. However, the analysis reveals that Baltimore exhibits a more complex and broader spectrum of crime types, with a significantly higher total crime count compared to Vancouver. The city reports a significant presence of violent crimes, such as assault and robbery, in addition to theft. This complexity suggests a more varied criminal activity landscape that may require multifaceted law enforcement strategies. The sexual offense in Baltimore equally merits substantial attention, since it not only cause immediate physical and psychological trauma but also have long-term consequences that can affect the victims' mental health, social relationships, and overall well-being. The total number of crimes in Baltimore far exceeds that in Vancouver, indicating a higher overall crime rate in Baltimore, necessitating more robust and comprehensive crime prevention and reduction measures.


## Geographic Distribution of Crime Incidents

Finally let's have a look at the geographic distribution of crime incidents in Baltimore and Vancouver:

### Baltimore

#### Crime map of  Baltimore(2013-2016)
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Map_in_Baltimore_(2013-2016).html"></iframe>

#### Crime map of Baltimore(2013)
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Map_in_Baltimore_(2013).html"></iframe>

#### Crime map of Baltimore(2014)
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Map_in_Baltimore_(2014).html"></iframe>

#### Crime map of Baltimore(2015)
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Map_in_Baltimore_(2015).html"></iframe>

#### Crime map of Baltimore(2016)
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Map_in_Baltimore_(2016).html"></iframe>

### Vancouver

#### Crime map of  Vancouver(2013-2016)
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Map_in_Vancouver_(2013-2016).html"></iframe>

#### Crime map of Vancouver(2013)
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Map_in_Vancouver_(2013).html"></iframe>

#### Crime map of Vancouver(2014)
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Map_in_Vancouver_(2014).html"></iframe>

#### Crime map of Vancouver(2015)
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Map_in_Vancouver_(2015).html"></iframe>

#### Crime map of Vancouver(2016)
<iframe  frameborder="0" style=" width: 100%; height: 600px;" src="figures/Crime_Map_in_Vancouver_(2016).html"></iframe>


# Summary

In summary, this report provides an initial cursory exploration of crime time periods, crime types, and geographic distribution of crime in Baltimore and Vancouver through data processing and analysis. Despite the geographical distance between Baltimore and Vancouver, both cities face significant crime challenges owing to their unique socio-economic contexts. However, owing to differences in socio-economic development, urban planning and comprehensive social services, the two cities exhibit markedly different patterns of crime. In order to reduce the incidence of crime and improve urban policing, a targeted approach is needed to address the root causes of crime in each city.


