# Paper_Climate_Eta
It presents the two databases used to plot all the Figures and the Table 1 in the paper 

## Databases.xls
It presents the two databases used to plot all the Figures and the Table 1 in the paper "Inequality aversion for climate policy", Del Campo, S., Anthoff A., Kornek, U.

Sheet 1: "DB1.eta"
It gathers information used to plot the Figures with R.
"Sample_time" is either the year of the estimation or the mean (rouded up) of the period of estimation.
We used the World Bank database for the three following items. Zero values have been deleted for readability.
-Gini coefficents are from the database "API_SI.POV.GINI_DS2_en_excel_v2_1562753.xls" downloaded on 10/29/2020 at https://data.worldbank.org/indicator/SI.POV.GINI
-Gross Domestic Products per capita in Purshasing Power Parity, constant intl dollar 2017, are from the database "API_NY.GDP.PCAP.PP.KD_DS2_en_excel_v2_1562658.xls"
 downloaded on 10/29/2020 at https://data.worldbank.org/indicator/NY.GDP.PCAP.PP.KD
-Gross Domestic Products per capita, constant US dollar 2010, are from the database "API_NY.GDP.PCAP.KD_DS2_en_excel_v2_1563165.xls" downloaded on 10/29/2020 at
 https://data.worldbank.org/indicator/NY.GDP.PCAP.KD
GDPs are only available from 1990 onward, and several Gini coefficients are missing. We only use values for samples from single countries.
Sheet 2: "DB2.leakage.rate"
It gathers information used to build the Table 1.
Donor and Recipient consumptions per capita are own calculations from consumption expenditures and population data - https://unstats.un.org/unsd/snaama/CountryProfile?ccode=894
Eta is computed as: log(Leackage_rate)/log(Donor_consumption/Recipient_consumption)


## R_code_for_figures.R
It presents code to replicate all the Figures in the paper. It was built under Rstudio version 1.4.1106.
All figures are exported in TIFF format.
Limits of unbounded ranges have been arbitrarily set at zero for the lower and four for the upper.
For Figure 2: If a study finds a range for inequality aversion, we represent the finding through the mean of the range.
