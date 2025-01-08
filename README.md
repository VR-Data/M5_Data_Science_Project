# A Review of the Effect of Global Economic Shocks on the UK Economy and Investment Market

## Contents
- Project Summary
- GDP vs CPI
- Key Data Points
     - Macroeconomic data
     - Proxies for the UK investment market
     - Proxies for the UK CIS market
- Getting Started
	- Analysis of GDP, Inflation, and Market Trends Since 2015
     - Using Linear Regression to Compare Benchmarks
     - Comparing the Market to GDP
- Time Series Analysis
     - CPI Prediction vs Actual
     - GDP Prediction vs Actual
     - GDP Prediction vs Actual (Finincial Crisis)
     - FTSE All Share Prediction vs Actual
     - FTSE Smaller Companies Prediction vs Actual
- Final Thoughts
- References

## Project Summary:

The UK economy is currently facing unprecedented challenges as the ripple effects of recent global shocks, such as the COVID-19 pandemic and the Ukraine War, redefine the economic landscape. Inflation has increased beyond anything that we have seen in recent history, and GDP has all but come to a standstill as a result. These crises have also disrupted UK investment dynamics, causing significant fluctuations in investment returns UK sectors, increasing investment risk and lowering investor confidence.

This project seeks to unravel the complexities of how these shocks impact the UK economy and to investigate which macroeconomic factors have the greatest influence on UK investment. By examining these drivers, this report aims to identify their implications for investment strategies, risk management, and long-term growth prospects within the UK.

In an era of uncertainty, understanding these indicators is critical to navigating the ongoing challenges of a volatile global economy and safeguarding the resilience of the UK investment sector. This study aspires to provide actionable insights that empower investors, policymakers, and financial institutions to adapt and survive this shifting economic climate. It will also focus on the UK Collective Investment Scheme (CIS) market, examining the effects of macroeconomic indicators on two key types of investment: direct investments in individual stocks and indirect investments through CIS vehicles such as Open-Ended Investment Companies (OEICs) and Unit Trusts. This distinction highlights the varying ways investors can access the market, either by purchasing shares of individual companies or by pooling their money into professionally managed funds that diversify across multiple assets.

## GDP vs CPI:

When discussing macroeconomic indicators, the first two likely to come to mind for most people are Gross Domestic Product (GDP), which measures the size of a country’s economy[1], and the Consumer Price Index (CPI), which is used as a measure of inflation[2]. It is important to note, that often when citing figures for GDP, the Office for National Statistics (ONS) refer to what is called the “Real GDP”[3], which takes inflation into account. Let’s put this information into perspective with the following figures:

<img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/GDPvsCPIChart2000.png" 
     width="100%" 
     height="auto" 
     alt="GDP vs CPI Trend Chart Since 2000">

This chart shows the trend for both GDP (real) and inflation via the CPI. There are three areas on this chart that stand out:
1.	GDP readjustment in 2008 – A significant drop in GDP that did not recover back to its previous trendline.
2.	GDP drop in 2000 – A unprecedented drop in GDP, however unlike the 2008 drop, GDP returned relatively close to its trendline.
3.	Rapid inflation from 2021 onwards – CPI growth by over 20% in 3 years, essentially causing GDP to stagnate.

These coincide with the three most impactful global economic shocks in recent history:
1.	The 2007-2008 Global Financial Crisis – Despite beginning in 2007, causing the collapse of Northern Rock in the UK, it wasn’t until the collapse of the Lehman Brother investment back on 15 September 2008[4] that the global economy felt the full weight of this shock. 
2.	COVID-19 Pandemic – GDP fell by “More than twice as much as the previous largest annual fall on record” according to the ONS via the BBC[5], following lockdown in 2020 as a result of the COVID-19 outbreak.
3.	The Ukraine War – Following the Russian invasion of Ukraine, global oil prices rose by 11%, meanwhile UK wholesale gas prices rose by 40%[6]. Along with other underlying factors and the combination of an already unstable economic condition in the UK following Brexit and COVID-19.

Due to the complex nature of the subject, especially given the combined effects of the recent events, this report will limit its research to the past 5 years, to investigate and discuss macroeconomic indicators and their effect on the UK investment sector.

## Key Data Points:

**Macroeconomic data:**
1.	GDP Data – Monthly GDP figures provided by ONS, available at: https://www.ons.gov.uk/economy/grossdomesticproductgdp/datasets/monthlygdpandmainsectorstofourdecimalplaces
2.	CPI Data – Monthly CPI figures provided by ONS, available at: https://www.ons.gov.uk/economy/inflationandpriceindices/datasets/consumerpriceinflation

**Proxies for the UK investment market:**
1.	FTSE All-Share Index – This index captures nearly all companies listed on the London Stock Exchange’s (LSE) main market and will be used to indicate how UK companies are performing.
2.	FTSE SmallCap Index – This index captures companies listed on the LSE’s main market that are ranked outside the top 350 largest companies by market capitalisation.

**Proxies for the UK CIS market:**

The Investment Association (IA) provides broad categories for UK domiciled CIS and provides data based on how these investment vehicles perform in their category as a whole. To mirror the above FTSE benchmarks, the following IA sectors will be used:
1.	IA UK All Companies – Similar to FTSE All-Share, this category includes CIS that have focus on investing directly into UK companies of any market capitalisation.
2.	IA UK Smaller Companies – Similar to FTSE SmallCap, this category includes CIS that have focus on investing directly into UK companies with market capitalisation under £100m.
   
To learn more about these IA sectors, please visit the IA website[7].

Data for UK investment market and UK CIS market provided by Morningstar.

## Getting Started:

### Analysis of GDP, Inflation, and Market Trends Since 2015

<img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/BenchmarkvsGDPCPI2015.png" 
     width="100%" 
     height="auto" 
     alt="Line Chart showing trend of the Market and CIS benchmarks against GDP and CPI since 2015">

Examining the trends since 2015 for the Market and CIS proxies alongside GDP and CPI reveals notable differences. While GDP and CPI exhibit relatively stable trends in normal circumstances, investment returns fluctuate more significantly. The steep GDP drop in 2020 caused by the COVID-19 pandemic heavily impacted investments but returns rebounded strongly as GDP recovered. Small-cap markets, in particular, outperformed during the recovery, with benchmarks showing gains up to 40% higher than the broader market.

Another key observation is the sustained rise in investment returns starting around October 2023, with an average increase of 15% in less than a year. This is particularly striking given the sharp rise in inflation, as indicated by the CPI, since 2021, as well as the known ongoing cost of living crisis. Despite these factors, markets have demonstrated remarkable resilience and growth.

### Using Linear Regression to Compare Benchmarks

The line chart highlights a clear correlation between the FTSE All Share and IA UK All Companies benchmarks, which follow similar trends. Conversely, the FTSE Small Cap and IA UK Smaller Companies benchmarks trend differently, but closely align with each other.

This alignment makes sense given the context: the returns of CIS investments closely mirror those of the broader market, as represented by FTSE benchmarks. To quantify this relationship, linear regression was applied to compare monthly returns for FTSE indices and their corresponding IA benchmarks.

<div align="center">
  <img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/AllshVSUKAllComps.png"
       width="49%" 
       alt="Scatter Chart of FTSE All Share against IA UK All Companies, showing a strong positive trend line and R squared value of 0.9235">
  
  <img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/SmallCapVSUKSmallComps.png"
       width="49%" 
       alt="Scatter Chart of FTSE All Share against IA UK All Companies, showing a strong positive trend line and R squared value of 0.8623">
</div>

The scatter chart confirms a strong correlation between the market and CIS benchmarks, validating the hypothesis that market trends significantly influence UK CIS investments. With R-squared values of 0.9235 and 0.8623, the data strongly supports this relationship.

### Comparing the Market to GDP

Based on these findings, future comparisons will focus on the Market benchmarks, with CIS data revisited later in the analysis to validate conclusions. The next step involves examining the relationship between Market benchmarks and GDP. Real GDP, which accounts for inflation and reflects the overall strength and health of an economy, might be expected to correlate with investment market performance. However, linear regression analysis reveals that this is not the case.

<div align="center">
  <img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/AllshVSGDP.png"
       width="49%" 
       alt="Scatter Chart of FTSE All Share against GDP, showing weak correlation and R squared value of 0.0023">
  
  <img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/SmallCapVSGDP.png"
       width="49%" 
       alt="Scatter Chart of FTSE All Share against GDP, showing weak correlation and R squared value of 0.0028">
</div>

The charts indicate a weak correlation, though interpretation is complicated by significant outliers, primarily from 2020, when GDP experienced an unprecedented drop. To better understand the relationship under normal circumstances, extreme outliers (monthly changes exceeding 5%) were excluded. 

<div align="center">
  <img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/AllshVSGDPminusoutliers.png"
       width="49%" 
       alt="Scatter Chart of FTSE All Share against GDP minus outliers, showing weak correlation and R squared value of 0.0103">
  
  <img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/SmallCapVSGDPminusoutliers.png"
       width="49%" 
       alt="Scatter Chart of FTSE All Share against GDP minus outliers, showing weak correlation and R squared value of 0.011">
</div>

This adjustment increased the R-squared value, but the correlation between GDP and market performance remained weak. This finding is consistent with a report by C. Wilson on GOV.UK[8], which calculated an R-squared value of 0.0174 for GDP between 1994 and 2018, comparable to the 0.0103 value derived from the adjusted data in this analysis.

## Time Series Analysis

In this section, we analyse the time series data for key economic indicators; inflation, GDP, and the FTSE indexes, focusing on their trends and variability prior to the recent economic shocks. Using historical data from 2010 to 2020, a five-year forecast starting at the beginning of 2020 has been generated using PowerBI's forecast function to project their expected performance in the absence of shocks. This forecast is then compared to the actual observed values to evaluate deviations and assess whether the impacts of recent shocks align with or diverge from pre-existing trends. The charts created in PowerBI visually illustrate these comparisons, helping to contextualize the magnitude and nature of these disruptions.

### CPI Prediction vs Actual

<img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/CPI_TimeSeries.PNG" 
     width="100%" 
     height="auto" 
     alt="CPI Trend since 2010, with forecast from 2020 showing a sharp rise in inflation but a steady growth on the forecast">

This chart displays the trend of inflation (CPI), which remained steady until around March 2021, at which point it experienced a sharp increase of over 20% since 2010. The forecast, however, anticipated a steady growth trajectory, with the upper limit of the 95% confidence interval predicting no more than a 12% increase. This substantial deviation from the forecast suggests that inflation during this period significantly exceeded normal circumstances. Moreover, the continued upward trajectory indicates that inflation shows no immediate signs of returning to the expected levels, marking a departure from historical patterns.

### GDP Prediction vs Actual

<img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/GDP_Timeseries.PNG" 
     width="100%" 
     height="auto" 
     alt="GDP vs CPI Trend Chart Since 2000">

This chart illustrates the performance of GDP, which experienced an unprecedented decline during the initial COVID-19 lockdown. This sharp fall was followed by a swift recovery, initially below the predicted levels, but subsequently meeting expectations, bringing GDP within the forecast range. GDP then remained within the forecasted bounds until June 2024, at which point it dropped below the lower limits of the prediction. This decline is attributed to stagnancy in economic growth, suggesting a slowdown after the initial recovery phase.

### GDP Prediction vs Actual (2008 Financial Crisis)

<img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/GDP2008_Timeseries.PNG" 
     width="100%" 
     height="auto" 
     alt="GDP vs CPI Trend Chart Since 2000">

In contrast to the previous chart, this chart compares GDP during the 2008 financial crisis, where a significant decline in economic output was followed by a shift to a new trend line, as opposed to the return to form presented following the recent economic shocks. This new trend line was, on average, 5% lower than the lower bound of the forecast. This suggests that the economic recovery post-crisis was not only slower but also sustained at a level lower than originally predicted, reflecting the long-term structural impacts of the financial crisis on the economy.

### FTSE All Share Prediction vs Actual

<img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/FTSEAllShare_Timeseries.PNG" 
     width="100%" 
     height="auto" 
     alt="GDP vs CPI Trend Chart Since 2000">

The next chart focuses on the FTSE All Share index with forecasts generated since 2020 based on data from 2010 to 2020. In contrast to the UK economy, the actual data for the FTSE initially fell below the predicted values but quickly rebounded, returning well within the forecasted lines. This highlights the resiliency of the investment market, which demonstrated a swift recovery and continued to perform within expectations, even amidst the severe economic conditions caused by the COVID-19 pandemic and subsequent shocks.

### FTSE SmallCap Prediction vs Actual

<img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/FTSESmallCap_Timeseries.PNG" 
     width="100%" 
     height="auto" 
     alt="GDP vs CPI Trend Chart Since 2000">

The final chart presents the FTSE SmallCap index, which not only rebounded more quickly than the FTSE All Share index but also briefly exceeded the predicted forecast before stabilizing close to the predicted trend line. This suggests that, despite the challenging economic conditions, small companies were able to outperform expectations, highlighting their ability to adapt and succeed even in times of hardship.

## Final Thoughts

In conclusion, this project has highlighted the resilience and adaptability of the UK investment market during periods of economic upheaval. By comparing the performance of CPI and GDP, we identified clear signs of change during economic shocks, underscoring the vulnerability of the economy. However, when juxtaposed with the UK CIS market, a stark contrast emerged, showing much stronger trends in market performance. Linear regression analysis further demonstrated that while GDP does not strongly correlate with market movements, as evidenced by a low R-squared value and supported by C Wilson's report on GDP and investment decisions, FTSE performance emerges as a strong indicator of UK domiciled CIS performance. With a 90% confidence correlation established between the FTSE and IA sectors, this analysis reinforces the idea that investment markets often outperform national economic trends. Lastly, time series analysis revealed that while the economy is recovering from recent shocks, it remains outside predicted trends, contrasting with the robust recovery observed in the investment market. Overall, these findings suggest that, even amid economic challenges, investment markets, particularly those tracked by indices such as FTSE, show a remarkable ability to recover and thrive, offering valuable insights for future investment strategies.

## References:
1.	What is GDP? (2019) Bank of England. Available at: https://www.bankofengland.co.uk/explainers/what-is-gdp (Accessed: December 2024). 
2.	Fernando, J. (2024) What is the consumer price index (CPI)?, Investopedia. Available at: https://www.investopedia.com/terms/c/consumerpriceindex.asp (Accessed: December 2024). 
3.	GDP monthly estimate, UK: October 2024 (2024) Office for National Statistics. Available at: https://www.ons.gov.uk/economy/grossdomesticproductgdp/bulletins/gdpmonthlyestimateuk/october2024 (Accessed: December 2024).
4.	The financial crisis – 10 years on (2018) Bank of England. Available at: https://www.bankofengland.co.uk/news/2018/september/the-financial-crisis-ten-years-on (Accessed: December 2024).
5.	Islam, F. (2021) UK economy suffered record annual slump in 2020, BBC. Available at: https://www.bbc.co.uk/news/business-56037123 (Accessed: December 2024).
6.	Ukraine´s war impact in the UK economy and financial system, Santander. Available at: https://www.santander.com/en/press-room/insights/ukraines-war-impact-in-the-uk-economy-and-financial-system (Accessed: December 2024).
7.	Fund Sector Definitions, The Investment Association. Available at: https://www.theia.org/industry-data/fund-sectors/definitions (Accessed: December 2024).
8.	Wilson, C., Smith, A. and Jinks, A. (2019) GDP and investment decisions, GOV.UK. Available at: https://assets.publishing.service.gov.uk/media/5c6c1db0e5274a72b55d58ea/Jan_2019_update.pdf (Accessed: December 2024).

