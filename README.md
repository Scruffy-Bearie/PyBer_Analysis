# An Analysis of PyBer Data From Urban, Suburban and Rural Cities

## Overview
A ridesharing company generally uses websites and/or mobile phone based applications to match passengers with private vehicles for hire that, unlike traditional taxis, can not be legally hailed from the street.  Although ridesharing companies have been criticized for their potentially disruptive effect on existing taxi services, they have gained traction through also operating in the traditionally underserviced suburban and rural markets.  The client for this project, a Python-based ridesharing company called “PyBer”, initially requested an analysis of their ridesharing data to examine the affordability of improving access to their services in underserviced neighborhoods.  Upon examining the results of the aforementioned analysis, decision makers at PyBer requested further analysis to examine the relationship(s) between city type - urban, suburban and rural - and the number of drivers operating, the number of rides delivered and the total weekly fares collected.  The following report represents an attempt to address these requests.

## Results
### (i) Summary of Ride Share Data
The first steps in the analysis were to merge the existing data frames – those containing ride and city data - and then clean the resulting data frame by searching for and removing any records containing missing data points which might interfere with analysis.  Using this merged data frame - in conjunction with “groupby”, “sum” and division operations – it was possible to determine the total number of rides, drivers and fares as well as the average fare per ride and fare per driver for each city type.  The figures were placed in a summary data frame which, following some adjustments to, and formatting of, the columns, was a suitable way to examine and compare the results of the analysis (See Figure 1: Summary of Ride Share Data).

![](https://github.com/Scruffy-Bearie/PyBer_Analysis/blob/main/Analysis/PyBer_data_summary.png)

A quick examination of the data in Figure 1 reveals an intriguing relationship – as city size decreases (from urban to suburban to rural), the number of drivers operating and number of rides decreases but the average fare increases.  Ultimately, and as the data demonstrates, this means that the average fare per driver in rural cities is greater than in both suburban and urban cities.

### (ii) Total Fare by City Type
To further examine the relationships described above, “groupby” and “sum” operations were used on the merged data initially used to create a new data frame containing the total fares collected on each date in each city type.  By transforming this data frame into a pivot table, transforming the date information into the datetime data type and grouping by week, it became possible to display the total fares collected per week by city type in graphical format (See Figure 2: Total Fare by City Type).

![Figure 2: Total Fare by City Type](https://github.com/Scruffy-Bearie/PyBer_Analysis/blob/main/Analysis/PyBer_fare_summary.png)

The graphical representation that is Figure 2 evidences three key features of the data set: (1) total weekly fares (or revenues) generated on a weekly basis is consistently highest in urban settings and lowest in rural settings with suburban settings consistently in between; (2) there is considerable variation in total weekly fares within a given month across all city types; (3) there was a local maximum in total weekly fares for all city types towards the end of February.

### (iii) Average Weekly Fares per Driver
In the interests of making the analysis more thorough, data acquired/produced during the previous steps was combined to provide a little more insight (See Figure 3: Summary of Weekly Averages).

![](https://github.com/Scruffy-Bearie/PyBer_Analysis/blob/main/Analysis/PyBer_weekly_averages.png)

The data in Figure 3 demonstrates that although average weekly fares in urban cities may be the highest as compared to suburban and rural cities, the average weekly fare/driver is actually the lowest.  Moreover, the data demonstrates that although average weekly fares (and revenues) in rural cities may be the lowest, the average weekly fare/driver is approximately 3x greater than in urban cities.  

## Analysis and Summary
Assuming that the long-term interests of PyBer lay with achieving a fine balance between increasing total revenues and employee/driver satisfaction, the analysis conducted thus far suggests the following:

•	In urban markets, the total weekly fares are high but, owing a large number of drivers and low average fare/ride, the average weekly fare/driver ( 0.91 $/Driver) is lower than might be expected.  Given that these trends are likely a result of shorter trip lengths in urban settings and a large number of drivers working part-time hours, greater revenues for PyBer could be achieved through taking steps to increase fare/ride (increasing average trip length though incentivising longer trips) and, depending on the driver compensation model in use, by incentivising drivers to work longer shifts/accept more rides.

•	In rural markets, total number of rides, and as a result total weekly fares, are low but, owing to a comparatively small number of drivers and a high average fare/ride, the average weekly fare/driver (2.95$/Driver) is higher than might be expected.  As such, PyBer could likely achieve an increase in revenues through initiating an ad campaign to (further) promote their services to consumers (in the interests of increasing the total number of rides within a given time frame) and by using existing data (and projected earnings) to recruit additional drivers in rural settings.

•	In suburban markets, it would seem that a fine balance between number of drivers, average fare (or trip length) and total trips has been achieved such that PyBer is achieving decent revenues and the average weekly fare/driver is respectable (2.15 $/Driver).  That said, the best approach for PyBer to increase revenues in the market, or, at least, resulting “from” these markets is simply to operate in more of them – to engage in driver recruitment and advertising such that they can offer services in a greater number of suburban settings.

Wherein the researcher stands by their analysis and findings, it is worth pointing out that Pyber’s net revenues will always be impacted by the specifics of their driver compensation model.  Without knowing if driver’s are paid a flat rate per ride, a percentage of each ride or an hourly wage, it’s difficult to know which of the strategies discussed above would be most beneficial for both PyBer and it’s driver’s.  As such, further analysis including the specifics of driver compensation should be conducted before committing to any course of action aimed at increasing revenues.
