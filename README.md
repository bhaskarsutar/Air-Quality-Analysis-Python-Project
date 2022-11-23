# Air-Quality-Analysis-Python-Project

# Air Quality Analysis Project - Is containing 6 sub projects these are

1.   **Time Series Data**
2.   **The datetime Module**
3.   **Data Cleaning**
4.   **Grouping & Aggregation**
5.   **Customised matplotlib Plots**
6.   **Bivariate Bar Plots**

In this project we have to analyse data on air quality in one of the cities in Italy. We need to determine whether the concentration of air pollutants increase or decrease over time.

In the process, we will also learn how to work with time-series data, i.e, how to work with date and time values. Towards the end of the project, we need to create time-series plots such as line plots, bar plots and multivariate boxplots to observe the trend of air pollution concentration over time.

Now, skim through the data description to understand the kind of features and corresponding values we have in this data set on air quality.



### Data Description

The dataset contains 9358 instances of hourly averaged responses from an array of 5 metal oxide chemical sensors embedded in an Air Quality Chemical Multisensor Device.

The device was located on the field in a significantly polluted area, at road level, within an Italian city. Data were recorded from March 2004 to February 2005 (one year) representing the longest freely available recordings of on field-deployed air quality chemical sensor devices responses. A co-located reference certified analyzer provided **Ground Truth (GT)** hourly averaged concentrations for Carbon Monoxide (CO), Non-Methane Hydrocarbons (NMHC), Benzene (C6H6), total Nitrogen Oxides (NO) & Nitrogen Dioxide (NO2}) and Ozone (O3). These chemical compounds are commonly occurring air pollutants.

|Index|Columns|Description|
|-|-|-|
|0|Date|Date (DD/MM/YYYY)|
|1|Time|Time (HH.MM.SS)|
|2|CO(GT)|True hourly averaged concentration $\text{CO}$ in $\frac{mg}{m^3}$ (reference analyzer)|
|3|PT08.S1(CO)|PT08.S1 (tin oxide) hourly averaged sensor response (nominally $\text{CO}$ targeted)|
|4|NMHC(GT)|True hourly averaged overall Non-Methane Hydrocarbons concentration in $\frac{\mu g}{m^3}$|
|5|C6H6(GT)|True hourly averaged Benzene concentration in $\frac{\mu g}{m^3}$||
|6|PT08.S2(NMHC)|PT08.S2 (titania) hourly averaged sensor response (nominally $\text{NMHC}$ targeted)|
|7|NOx(GT)|True hourly averaged $\text{NO}_x$ concentration in Parts per billion (ppb)|
|8|PT08.S3(NOx)|PT08.S3 (tungsten oxide) hourly averaged sensor response (nominally $\text{NO}_x$ targeted)|
|9|NO2(GT) |True hourly averaged $\text{NO}_2$ concentration in $\frac{\mu g}{m^3}$|
|10|PT08.S4(NO2)|PT08.S4 (tungsten oxide) hourly averaged sensor response (nominally $\text{NO}_2$ targeted)|
|11|PT08.S5(O3) |PT08.S5 (indium oxide) hourly averaged sensor response (nominally $\text{O}_3$ targeted)|
|12|T|Temperature in Â°C|
|13|RH|Relative Humidity (%)|
|14|AH|AH Absolute Humidity|

The above dataset contains missing (or null) values and `-200` as garbage value.





### About Air Pollutants

**Carbon Monoxide** (CO)

It is a poisonous gas. It reacts with haemoglobin because of which it is unable to supply oxygen to the human body. At very high concentrations of carbon monoxide, up to 40% of the haemoglobin can bind with carbon monoxide which is enough to certainly kill humans. Carbon monoxide is also known as the silent killer because it has no colour, taste or smell.


**Benzene (C6H6)**

It is a colorless or light yellow liquid at room temperature. It has a sweet odour and is highly flammable. It evaporates into the air very quickly, but its vapour is heavier than air and may sink into low-lying areas. Outdoor air contains low levels of benzene from tobacco smoke, gas stations, motor vehicle exhaust, and industrial emissions. Indoor air generally contains levels of benzene higher than those in outdoor air. The benzene in indoor air comes from products that contain benzene such as glues, paints, furniture wax, and detergents. The air around hazardous waste sites or gas stations can contain higher levels of benzene than in other areas. Tobacco smoke is also a major source of benzene.

People who breathe in high levels of benzene may develop drowsiness, dizziness, rapid or irregular heartbeat, headaches, tremors, confusion,  unconsciousness and death (at very high levels)

**Nitrogen Oxides (N2) & Nitrogen Dioxide (N2)** 

Nitrogen dioxide and nitric oxide together are referred to as oxides of nitrogen (NO).

Nitrogen dioxide is an irritant gas. When nitrogen is released during fuel combustion, it combines with oxygen atoms to create nitric oxide ($\text{NO}$). This further combines with oxygen to create nitrogen dioxide (N$\text{NO}_2$). Nitric oxide is not considered to be hazardous to health at typical ambient concentrations, but nitrogen dioxide can be. 

$\text{NO}_x$ gases react to form smog and acid rain as well as being central to the formation of fine particles (PM) and ground level ozone, both of which are associated with adverse health effects.

**Ozone (O3)**

Ozone is a colourless and odourless gas. Ground-level ozone forms when pollutants from cars and trucks, power plants, factories, and other sources come in contact with each other in heat and sunlight. Ground-level ozone is one of the biggest parts of smog, and it is usually worse in the summer months.

Many scientific studies have linked ground-level ozone contact to such varied problems as

- asthma, bronchitis, and emphysema

- pneumonia or bronchitis

- lung and throat irritation


**Non-Methane Hydrocarbons ($\text{NMHC}$)**

All the hydrocarbons except for methane (CH4) are collectively called Non-Methane Hydrocarbons. The elevated ambient concentration of NMHCs in an urban environment has a significant impact on climate change and human health.

Hydrocarbons (or organic compounds) are naturally occurring substances that can be found in all living things. The solvents being emitted from manufacturing processes are considered Volatile Organic Compounds (VOC). The hydrocarbons are considered volatile since they produce a vapour at room temperature and normal atmospheric pressure. VOCs are contributors to the formation of ozone and smog.  

The mechanism for ozone production is:

$$\text{VOC}  +  \text{NO}_x  +  \text{sunlight (UV)} \longrightarrow  \text{O}_3$$

Hydrocarbons are the main component of crude oil, natural gases, and most pesticides. All of these substances contribute to the greenhouse effect, and the depletion of the ozone layer. They also reduce the photosynthetic ability of plants, increase cancer rates in humans and animals, and increase the risk of respiratory illness. 
