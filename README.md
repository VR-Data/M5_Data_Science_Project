# How Global Economic Shocks Impact UK Investing

## Contents
- Project Summary
- GDP vs CPI
- Key Data Points
- Getting Started
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

## Getting Started:

### Analysis of GDP, Inflation, and Market Trends Since 2015

<img src="https://github.com/VR-Data/M5_Data_Science_Project/blob/main/Images/BenchmarkvsGDPCPI2015.png" 
     width="100%" 
     height="auto" 
     alt="Line Chart showing trend of the Market and CIS benchmarks against GDP and CPI since 2015">

Examining the trends since 2015 for the Market and CIS proxies alongside GDP and CPI reveals notable differences. While GDP and CPI exhibit relatively stable trends in normal circumstances, investment returns fluctuate more significantly. The steep GDP drop in 2020 caused by the COVID-19 pandemic heavily impacted investments but returns rebounded strongly as GDP recovered. Small-cap markets, in particular, outperformed during the recovery, with benchmarks showing gains up to 40% higher than the broader market.

Another key observation is the sustained rise in investment returns starting around October 2023, with an average increase of 15% in less than a year. This is particularly striking given the sharp rise in inflation, as indicated by the CPI, since 2021, as well as the known ongoing cost of living crisis. Despite these factors, markets have demonstrated remarkable resilience and growth.





