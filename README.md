Crime Analysis Dashboard
An interactive Power BI dashboard analysing crime patterns across countries, time of day, months, years and crime types, with a focus on resolution performance.
 

Objective
To understand where, when and what kind of crimes occur, and how effectively they are resolved, in order to support data-driven decisions on resource allocation and prevention.
Dataset
•	Records: 2,500 crimes
•	Countries: 13 (Austria, Finland, United Kingdom, Denmark, Norway, Sweden, Germany, Italy, Spain, Netherlands, France, Belgium, Switzerland)
•	Period: 2021 to 2023
Tools Used
•	Power BI Desktop
•	Power Query (data cleaning and transformation)
•	DAX (measures)
Dashboard Features
•	KPI cards: Total, Resolved and Unresolved crimes, and Resolution Rate %
•	Slicers: Crime Year, Crime Month, Country
•	Visuals:
•	Total crimes by month (trend)
•	Count of crime by time of day
•	Resolved vs unresolved crimes by year
•	Crime distribution by country
•	Crime type distribution
Key Insights
1.	Overall resolution rate is 70%: 1,751 of 2,500 crimes were resolved and 749 remain unresolved.
2.	Night is the riskiest period: 1,324 crimes (about 53%) occurred at night, far ahead of morning (461), evening (403) and afternoon (312).
3.	Violence and Sexual Offences dominate: 959 cases (about 38%), followed by Anti-Social Behaviour (473, about 19%).
4.	October is the peak month: 309 crimes, against a monthly range of roughly 175 to 209 for most other months.
5.	Resolution rate varies by year: about 69% in 2021, 72% in 2022 and 68% in 2023.
6.	Austria has the highest count: 879 crimes (about 35% of records), followed by Finland (331) and the United Kingdom (219). This may reflect how the data was collected rather than true crime levels.
Recommendations
•	Increase patrols and surveillance during night hours, particularly in high-volume countries.
•	Prioritise prevention and response strategies for violent and sexual offences.
•	Investigate the October spike (seasonal events, reporting patterns) before planning resources.
•	Review why unresolved cases remain high in certain years and crime types.
How to Use
1.	Download the .pbix file from the dashboard/ folder.
2.	Open it in Power BI Desktop (free).
3.	Use the slicers (Year, Month, Country) to explore the data.
Sample DAX Measures
Update these to match the table and column names in your model.
DAX
Total Crimes = COUNT(Crime[Crime ID])

Resolved Crimes = CALCULATE([Total Crimes], Crime[Status] = "Resolved")
Unresolved Crimes = [Total Crimes] - [Resolved Crimes]
Resolution Rate % = DIVIDE([Resolved Crimes], [Total Crimes])
Limitations
•	Counts are absolute and not normalised per capita, so country comparisons should be read with caution.
•	2021 appears to contain fewer records than 2022 and 2023, which may indicate partial data.
•	The dataset size is small (2,500 records), so findings are indicative rather than conclusive.

