# k-Means Clustering Analysis - COVID-19 Infection Rate, Digital Propensity and Access to Amenities
## Executive Summary
### Findings

The model successfully identified 5 distinct clusters within the data, where meaningful analysis and further research can be applied. Crucially, there is a strong relationship with higher Digital Propensity and lower covid infection rates, even when access to amenities (such as supermarkets and sport centers) was limited.</br>
</br>
This translates to "Individuals with limited access to remote working and reported a lower digital literacy/confidence were dispropotionally effected during the Covid-19 Pandemic.".</br>
</br>
However, known bias such as job type, income, deprivation and demographic/personal data will have some explanitory power when looking at the results and application of this analysis. </br>

### Purpose
The objective of this analysis is to understand how patterns of COVID infection relate to digital capability and access to physical amenities, by identifying distinct types of places rather than analysing individual variables in isolation.</br>
</br>
<b>Data & Method</b></br>
Data used is area-level data containing:</br>

  - Digital propensity scores
  - COVID-19 infection rates
  - Counts of supermarkets
  - Counts of sports and leisure facilities

To reduce dimensionality and minimise multicollinearity, the input features were first transformed using Principal Component Analysis (PCA). k-Means clustering was then applied to group areas into clusters with similar underlying characteristics.</br>
This approach allows for identification of place-based typologies rather than single-factor explanations.</br>
All data used is publically available.</br>

### Potential Application
This analysis can be used as a basis to help develop prioritisation zones in the event of a pandemic, as well as focus area's for digital literacy skill training or availability. </br>
</br>
Fundamentally, it can be used at a base line to build up patterns and distinct groups based on places and not people. </br>
</br>
It is scaleable and easy to add additional data for further analysis.</br>

### Bias & Other Research
It has been well researched that COVID infection and mortality rates affected people from an ethnic minority group, disabed and women (etc...) disproportiantaly. </br>
</br>
Therefore, it is reasonable to assume that this will be reflected in the projects base data. This could be represented by:
  - Income & Job type
  - Neighbourhood deprivation
  - Age, Gender, Ethnicity, Disability
</br>
[Link to Public Health research](https://www.local.gov.uk/health-inequalities-deprivation-and-poverty-and-covid-19#:~:text=The%20unequal%20impact%20of%20the,Storm%20report%2C%20published%20April%202021.) -- Need to look at how to Oxford reference this correctly here. </br>
</br>
[Link to IMD 2025](https://www.gov.uk/government/statistics/english-indices-of-deprivation-2025/english-indices-of-deprivation-2025-statistical-release) -- Need to look at how to Oxford reference this correctly here. </br>

### Encyclopedia
LSOA = Lower Layer Super Output Area, which represents a group of postcodes in an area.</br>
MSOA = Middle Layer Super Output Area, which represents a group of LSOA area's and a larger cohort of postcodes.</br>
DPS = Digital Propensity Score. </br>
PCA = Principal Component Analysis.</br>

## Approach

Data was collected from publically available sources and pre-processed before analysis into the required shape via Excel and Python.</br>
The shape used in this analysis is MSOA level data.</br>
Tools used:
  - Python 3.11
  - Excel
</br>
Python dependencies:
  - ydata-profiling
  - kneed
  - seaborn
  - geopandas
  - pandas
  - matplotlib
  - sklearn
  - numpy
  - imageio.v2
  - IPython.display
</br>
```python
!pip install ydata-profiling
!pip install kneed
!pip install seaborn
!pip install geopandas
!pip install pandas
!pip install matplotlib
!pip install sklearn
!pip install numpy
!pip install imageio.v2
!pip install IPython.display
```
</br>
Users will need to download the msoa_geo_data.geojson from [Insert link here](draft sorry) and add it to the 'Files' directory. 