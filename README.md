**In progress: being updated**

## Abstract

Mass shooting is an incident of targeted violence carried out by one or more shooters at one or more public places. Gun related deaths and injuries have increased over the few years in the United States [[1, 2](#references)]. Infact, CDC reported 48830 deaths from gun-related injuries in 2021 [[3](#references)]. Crime has become so common place that some even claim it be "an integral part of a healthy society" [[4](#references)]. As an international student in the United States I was concerned about my safety and wanted to analyse the statistics of the victims and identify the locations where gun-related injuries are prevalant.

For this analysis, New York City was shortlisted because I plan to visit the city during my masters since its a short drive from Boston. A potential **stakeholder** for this project could be any NYC recident or someone with travel plans to the city.

The analysis revealed some interesting observations:

1. The major victims were 'Black' while the most impacted age group was '18-45'
2. Brooklyn reported the highest number of incidents followed by Bronx and Queens. To my surprise Manhattan had significantly fewer shooting incidents
3. Over the past 10 years, shooting incidents followed a trend. They increased from Spring to Summer and then decreased
4. Going out at night is particularly unsafe and must be avoid whenever possible
5. Parking lots, playgrounds, and transit are usually safe however, the same is untrue for commercial places
6. Most of the shooting hotspots in Manhattan and Queens are situated around the locations I plan to visit

A detailed code walkthrough can be found in these notebooks:

1. [Visualization with Pandas](https://github.com/singhdivyank/Visualization/blob/main/NYPD_visualization.ipynb)
2. [Visualization with Plotly](https://colab.research.google.com/drive/1Aka5fncNMsWNNFlg9aJqxk2XAQ8ImdCk?usp=sharing)
3. [Visualization with PyGwalker](https://colab.research.google.com/drive/1x4v3W5QHgIDPOwlVpauomx1z2PnjrtFJ?usp=sharing)
4. [Visualization with ggplot (R)](https://colab.research.google.com/drive/1tp7g8b3vf3lTHEFsRCSHixkJ0-rq2SOI?usp=sharing)

## Dataset

For this project, the **NYPD Shooting Incident Data (Historic)** dataset published by the New York Police Department (NYPD) and maintained by NYC OpenData has been explored. The data is extracted manually each quarter and reviewed by the Office of Management Analysis and Planning and provides detailed categorization of the age, gender, and race of the victims as well as the time and location of all shooting incidents reported since 2006. The dataset can be accessed as a CSV from data.gov [[5](#references)] or from this repository ([NYPD_Shooting.csv](https://github.com/singhdivyank/Visualization/blob/main/NYPD_Shooting.csv)).

A description of all the columns is presented in the table below.

| Column name | Description |
| ----------- | ----------- |
| INCIDENT_KEY | Internal NYPD report number |
| OCCUR_DATE | The date the incident was reported |
| OCCUR_TIME | The time of reported the incident |
| BORO | The five regions of NYC- "Manhattan, Queens, Brooklyn, Staten Island, Bronx" |
| LOC_OF_OCCUR_DESC | Description of the location. Whether the incident was reported indoors or outdoors |
| PRECINCT | assigned police precincts (internal to NYC). NYC has 77 precincts in total |
| JURISDICTION_CODE | Internal jurisdiction codes in NYC |
| LOC_CLASSFCTN_DESC | The categorization of the locality where the incident was reported |
| LOCATION_DESC | Description of the locality |
| STATISTICAL_MURDER_FLAG | Boolean value indicating whether its a gun-related murder or suicide |
| PERP_AGE_GROUP | The age group of the offender |
| PERP_SEX | Gender of the offender |
| PERP_RACE | Race of the offender |
| VIC_AGE_GROUP | The age group of the victim |
| VIC_SEX | Gender of the victim |
| VIC_RACE | Race of the victim |
| X_COORD_CD | X coordinate of the incident |
| Y_COORD_CD | Y coordinate of the incident |
| Latitude | Geographical latitude where the incident took place |
| Longitude | Geographical longitude where the incident took place |
| Lon_Lat | Latitude and longitude where the incident took place |

## Methodology

The major step in this project is Data Wrangling [[6](#references)]. The rationale behind wrangling is to prepare data for analysis and visualization by removing flawed and missing items and restructure data. In this analysis, the first step was to clean the given data by dropping the columns that add little value and removing empty values. As the next step, selection and aggregation are performed on the entity to visualise in order to enrich raw data. The final step is to structure the data into a long form or a pivot table (depending on the entity) to plot a graph.

## Human-Centered Considerations

This project could be very useful for someone who plans to move to or visit Nork York City or is already a resident. It could help someone understand the crime statistucs such as the time of the day where these crimes happen, the trend in cases over the year and the most targetted race and gender. Visualizing the reported cases on a map would help make informed decisions about the streets and localities to stay and avoid. Survival instinct is one of the most basic instincts to all kinds of life and hopefully the presented work helps someone improve their chances of getting injured from a gun shot.

**The intent here is just to provide information to make smarter choices in order to stay safe in NYC**.

## Requirements

The analysis was prepared using Python 3.10 running in a Jupyter Notebook environment. References to documentations:

1. [Python](https://docs.python.org/3.10/)
2. [Jupyter notebook](http://jupyter-notebook.readthedocs.io/en/latest/)

The following Python packages were used and their documentation can be found at their accompanying links:
1. [Pandas](https://pandas.pydata.org/)
2. [Jupyter](https://jupyter.org/)
3. [Matplotlib](https://matplotlib.org/)
4. [Numpy](https://numpy.org/)
5. [Datetime](https://docs.python.org/3/library/datetime.html)
6. [Calendar](https://docs.python.org/3/library/calendar.html)
7. [Plotly](https://plotly.github.io/plotly.py-docs/generated/plotly.html)

## References

[1] List of mass shootings in the United States in 2018- https://en.wikipedia.org/wiki/List_of_mass_shootings_in_the_United_States_in_2018

[2] List of mass shootings in the United States in 2019- https://en.wikipedia.org/wiki/List_of_mass_shootings_in_the_United_States_in_2019

[3] What the data says about gun deaths in the United States- https://www.pewresearch.org/short-reads/2023/04/26/what-the-data-says-about-gun-deaths-in-the-u-s/

[4] The Normality of Crime- http://www.d.umn.edu/cla/faculty/jhamlin/4111/Durkheim%20-%20Division%20of%20Labor_files/The%20Normality%20of%20Crime.pdf

[5] NYPD Shooting Incident Data (Historic)- https://catalog.data.gov/dataset/nypd-shooting-incident-data-historic

[6] Data Wrangling- https://courses.cs.washington.edu/courses/cse412/21sp/
