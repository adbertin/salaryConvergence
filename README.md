# Salary Convergence
Team Google (Apolline Bertin & Fang-Hsuan Chen)

This project investigates global wage convergence as a lens to better understand economic inequality across countries. Building on the work of Dr. Cashmere Flow, we aim to refine his baseline model which estimates wages in Purchasing Power Parity (PPP) terms using historical data, by incorporating additional macroeconomic and institutional variables that may explain why some countries are closing the wage gap with advanced economies, while others are falling behind.

Our analysis is conducted in two parts:

- Part 1 – Benchmark Estimation (OECD countries): We try to improve the fit between estimated and true OECD wages by testing functional enhancements using relevant country-specific variables (e.g., oil revenue in Norway, tourism receipts in Greece).

- Part 2 – Convergence Enhancement (Non-OECD countries): We explore deeper drivers of convergence or divergence in selected non-OECD countries by integrating explanatory variables such as conflict exposure, foreign investment, inflation and climate indicators.

Our work involves detailed country-level analysis, model building, and statistical evaluation. We compare our enhanced predictions with Dr. Flow’s original baseline using error metrics such as MSE, and visualize wage convergence trends. The goal is to contribute new insights into the mechanisms driving wage inequality and offer a reproducible methodology for future comparative economic research.

All code, data and visualizations are included in this repository. A video walkthrough of our approach is available below. 

## Table of Contents
1. How to Run through the Project
2. How to Use the Project
3. Part 1: Benchmark Estimation
4. Part 2: Convergence Enhancement
5. Future recommendations
6. Credits
7. References
   
## How to Run through the Project

Everything you need for the project is on this [github repository](https://github.com/adbertin/salaryConvergence). 

Please follow the link to the [video](https://youtu.be/ZUA_vm66vlg?si=Uo8XMwyFV0dcycOU). 

For additional information regarding the data we found (e.g. sources), or about our data analysis, please follow the link to our [Drive folder](https://drive.google.com/drive/folders/1rAaQe7x9-qscZJkETNIMwFP33fkr-0br?usp=drive_link).

## How to Use the Project

The data we used mostly come from the following sources:
- it was either already provided in the folder we were given to work on this project,
- from the [Our World in Data](https://ourworldindata.org/) website,
- from the [World Bank Group](https://www.worldbank.org/ext/en/home) database,
- from the [Statista](https://www.statista.com/) dataset,
- or from the [Eurostat](https://ec.europa.eu/eurostat/en/) database.

Exceptionnaly, some additional databases were used in specific cases (e.g. coffee imports data for Colombia), and are referenced in the Drive folder we shared previously.
The .csv files containing the explanatory variables that we found and used are formated under the name "Variables_countryname.csv" in the main branch of the repository.

For the coding part, we have divided the work into 2 code files that you can directly run via the github repository: 
- [Code for Part 1: Benchmark Estimation](https://github.com/adbertin/salaryConvergence/blob/1922435764739b07a890fd32b49297f4c7131a63/Google_Part1_final.ipynb). 
- [Code for Part 2: Convergence Enhancement](https://github.com/adbertin/salaryConvergence/blob/1922435764739b07a890fd32b49297f4c7131a63/Google_Part2_final.ipynb).

Results of Part 1 were stored in this [updated file](https://github.com/adbertin/salaryConvergence/blob/1922435764739b07a890fd32b49297f4c7131a63/Countries_Wages_Estimates_Finals_GOOD_new.csv), and used in Part 2 of our research.

Finally, all extra material that you can find on our github repository was provided for us by Noé Notter. 

## Part 1: Benchmark Estimation

In Part 1 of the project, we aimed to improve the baseline model developed by Dr. Cashmere Flow by enhancing the estimation of hourly-wages using macroeconomic and institutional variables. For this part, we worked on Costa Rica, Colombia, Greece, Mexico, and Luxembourg. We thought of different variables as hypotheses, by performing a country-level analysis for each country of the basket. Before adding our new variables to the existing code, we had to verify that each series ran cleanly from 2000–2020, check its coverage and quality, as indicated. 

### Country Level Analyses

#### 1. Costa Rica

**Step-by-Step Analysis**

Costa Rica's economy is primarily driven by agriculture, tourism, technology and IT services, customer service operations, and manufacturing. Its stable political environment and steady economic performance continue to attract immigrants, mainly from neighboring countries. Although empirical evidence shows that immigration has had no significant short-term effect on wages for either native workers or previously settled migrants, the increasing presence of migrant labor is contributing to shifts within the labor market. Native workers gradually move into roles emphasizing communication and interpersonal skills, while firms are adopting more technology-intensive and skill-oriented production processes (Silva et al., 2023). These adjustments suggest that, while wages have remained relatively stable in the short term, immigration may catalyze structural transformations that could influence wage dynamics over time.
Another notable feature of Costa Rica's labor market is its tiered minimum wage system, which categorizes workers into eight groups based on their education and experience levels (Garita, 2021). Research indicates that this framework contributes to a dual labor market structure, where the formal, higher-wage sector is more sensitive to policy changes (Gindling et al., 2005). In particular, increases in the minimum wage can deter the formation of new firms within the formal sector, potentially resulting in adverse, longer-term impacts on aggregate employment (Garita, 2021).

**Data Collection and Challenges**

One of the key variables identified (the number of immigrants) suffers from data limitations, including incompleteness and inconsistency across sources. Additionally, no official dataset is available for Costa Rica's tiered minimum wage system. To address this gap, we included educational attainment as a proxy to capture wage-related dynamics. Throughout the data collection process, we aimed to ensure that each core category in our analysis included at least one variable with consistent coverage over the 20-year research period. At the same time, we were careful not to overinterpret findings from the literature or introduce loosely related variables when direct and relevant data were unavailable.

**Variable Selection and Impact**

* **Air Passenger Volume**: Reflects the level of economic connectivity and tourism activity, where higher volumes can drive up demand for service-sector jobs and support wage growth.
* **Net Tourism Flow Ratio**: This ratio indicates whether Costa Rica is a net tourism destination. Higher ratios suggest increased foreign spending that can boost employment and wages in tourism-related industries.
* **Value Added per Agricultural Worker**: Measures productivity in agriculture, where improvements may lead to higher rural wages and reduce overall wage disparities across sectors.

#### 2. Mexico

**Step-by-Step Analysis**

Mexico has long faced a widening income gap, and unlike in other countries with similar trends, this growing inequality has been accompanied by a decline in average wages over the long term. According to Cortez (2001) and Robertson (2007), trade liberalization and foreign direct investment (FDI) have been major contributors to rising income inequality. In addition, declining unionization rates and other institutional changes in the labor market have exacerbated wage disparities. Given that education tends to reduce inequality, and real-world data show a downward pressure on average wages, we exclude educational expansion as a primary explanatory factor.

Although the mining industry accounts for only about 2% of Mexico's GDP, the country is the world's largest producer of silver and a major global supplier of gold, copper, and zinc. As noted by Arezki and Matsumoto (2017), fluctuations in metal prices can have significant macroeconomic impacts. Therefore, it is reasonable to assume that movements in the precious metals market may partially influence wages in Mexico, particularly in regions or sectors linked to mining activity.

**Data Collection and Challenges**

Since our focus is limited to international trade, income inequality, and the mining industry, data from 2000 to 2020 is relatively accessible. The main challenge lies in selecting the most relevant variables, as multiple indicators can reflect our focused area. Additionally, we faced limitations in data acquisition due to restricted access to specific high-quality datasets, particularly those measuring trade openness, which often require paid subscriptions or memberships.

**Variable Selection and Impact**

* **Unionization Rate**: Represents the proportion of the workforce affiliated with trade unions. A lower rate suggests weaker collective bargaining power, often linked to greater wage inequality.
* **Income Share - Top 10%**: Measures the pre-tax income held by the wealthiest 10% of the population. A rising share indicates increasing income concentration at the top.
* **Income Share - Bottom 50%**: Captures the pre-tax income that the lower half of the population earns. A declining share reflects growing income inequality.
* **Mining Sector GDP (Local Currency)**: Tracks the economic output of the mining sector using domestic currency to avoid exchange rate distortions. This allows a more straightforward analysis of the sector's direct impact on national wages.

#### 3. Greece

**Step-by-Step Analysis**

**Economic Context:** Greece has undergone substantial economic turbulence over the past two decades. The financial crisis that began in 2009 triggered a prolonged recession, leading to steep wage cuts, public sector contraction and record-high unemployment. Wages in Greece peaked in 2009 (24,005 EUR) but fell sharply, hitting a low in 2014 (18,809 EUR). During this period, the economy shrank by 25%, and unemployment peaked at nearly 28% in 2013. These macroeconomic shocks had a profound impact on wage formation, and their effects lingered into the recovery phase.

From 2018 onward, Greece has entered a period of moderate economic rebound. However, wage levels remain affected by debt burdens, international oversight, and policy limitations. The labor market continues to be shaped by structural reforms enacted under austerity programs, which significantly altered wage-setting mechanisms, especially in the public sector.

We explored a set of economic and institutional indicators to supplement the baseline wage model. These included government debt levels, unemployment rates, social protection expenditure, tourism revenue, and exports. Our goal was to capture the unique combination of fiscal, labor, and external drivers influencing wage dynamics in the Greek context.

**Data Collection and Challenges**

Data availability for added variables was a significant constraint. Many candidate variables were either unavailable in continuous annual format, lacked standardized definitions, or were only available in short periods. To maintain a clean and interpretable model, we opted for variables that were relevant, accessible and consistently defined throughout the time range.

**Variable Selection and Impact**

* **Government Debt:** Included due to its structural role in wage suppression, especially in the public sector.
* **Tourism Spending:** Used as a proxy for external demand and service sector income.
* **Unemployment Rate:** Reflects labor market slack and wage bargaining power.

#### 4. Colombia

**Step-by-Step Analysis**

Informal Employment Levels: Colombia’s labor market is characterized by persistently high levels of informality, particularly outside of agriculture. This has major implications for wage measurement, as informal workers often earn less, lack job protection, and are underrepresented in official wage statistics.

Real Exchange Rates and Terms of Trade: Colombia’s economy is highly sensitive to changes in its real exchange rate and ToT, due to its reliance on commodity exports. When ToT improves (i.e. when export prices rise relative to imports), it boosts national income and, in turn, wages.

Exports: Wages in Colombia are closely tied to external demand. The country’s top exports (crude petroleum, coal, coffee, and gold) make it vulnerable to global price swings. Coffee remains a key wage-linked sector in rural areas.

Unemployment Rates: Colombia’s high structural unemployment (NAIRU: 9–11%) dampens wage growth even during periods of economic expansion.

**Data Collection and Challenges**

The first challenge we faced was to find the missing data for the annual average wage in Colombia between 2000 and 2004, included. We computed the missing values by finding the Real hourly wage in Colombia for 2000-2004 from a Continuous Household Survey, DANE, period 2000-2004, and we multiplied it by the number of Working Hours from the data set we were provided with. We had to read the hourly wage on a graph, which makes the data approximative, and we had to use a different calculation method than the one that was used on  the OECD data website, which can bias the data, and with it, the results.
Data availability for added variables was also a significant constraint. Many candidate variables (e.g., gasoline index, terms of trade, informal sector breakdowns, or real exchange rates) were either unavailable in continuous annual format, lacked standardized definitions, or were only available in short periods.
To maintain a clean and interpretable model, we opted for variables that were relevant, accessible and consistently defined throughout the time range. 

**Variable Selection and Impact**

* **Foreign Direct Investment (FDI)**: FDI was included as a proxy for external investment confidence and job creation potential
* **Goods exports**: represent external demand and reflect production capacity tied to wage growth
* **Coffee exports**: were uniquely important given Colombia’s economic dependency on this sector, and the strong historical connection between coffee prices and rural income.

Once integrated into the regression, these three variables significantly improved the model’s predictive accuracy. The updated wage estimates showed a much tighter fit to the OECD benchmark, with a notably lower mean squared error (MSE). 

#### 5. Luxembourg

**Step-by-Step Analysis**

Luxembourg’s economic model is heavily shaped by its role as a global financial hub and by generous foreign investment inflows. Around 95% of foreign direct investment in Luxembourg passes through holding or intra-group financing entities. Although their direct contribution to employment and production is modest, they generate approximately 3% of GDP in tax revenue and support high-skill, high-wage jobs in finance and legal services. This inflow of capital and related fiscal policy measures is deeply intertwined with wage structures.
From a supply-side perspective, Luxembourg’s wage formation is affected by a combination of employer labor taxes, employee income taxes, indirect taxation (such as VAT), and consumer price inflation. 
To adapt the wage estimation model to this unique context, we explored a range of variables that capture tax structure, price inflation, financial sector performance and labor market composition. After evaluating data availability, correlation, and interpretability, we selected four macro-institutional indicators to enhance the baseline wage model: tax revenue, Harmonized Index of Consumer Prices, net migration, and proportion of seats held by women in parliament.

**Data Collection and Challenges**

Luxembourg provides high-quality macroeconomic data, but some fiscal and financial sector indicators were not fully harmonized or available in annual time series formats. Certain indicators relevant to financial services (like net interest income or intra-group investment flows) were omitted due to complexity or incomplete time coverage.
We prioritized variables that were both economically meaningful and available over a sufficiently long period (2000–2020). Gender representation in politics was included as a proxy for institutional inclusiveness and policy evolution.

**Variable Selection and Impact**

* **Tax Revenue (as % of GDP)**: reflects the aggregate effect of Luxembourg’s fiscal model, including its corporate tax base and reliance on financial inflows.
* **Harmonized Index of Consumer Prices**: measures inflation in living costs. It adjusts for wage purchasing power and may inform wage indexation mechanisms.
* **Net Migration**: tracks demographic expansion and labor supply pressure from both foreign workers and EU mobility.
* **Women’s Representation in Parliament**: was included as an institutional variable, offering insight into governance trends and their social and policy consequences.

These variables, once added to the model, improved wage estimation accuracy significantly. The enhanced model produced closer alignment to the OECD wage benchmark with a lower mean squared error (MSE).

### Model Enhancement

Following the Country Level Analysis for ach country, the original model we were provided with was refined through Ordinary Least Squares (OLS) regression, comparing the original estimated wages to the true OECD benchmark using relevant context-specific variables.
The results of the regression can be found in the table below:

| Country     | Old Estimate MSE | New Var-Adjusted Estimate MSE | R-squared (New Model) |
|-------------|------------------|-------------------------------|----------------|
| **Luxembourg**  | 1229.191| 0.188                        | 0.738    |
| **Greece**      | 15.773 | 0.084                         | 0.461    |
| **Colombia**    |60.499 | 0.046                         | 0.677    |
| **Costa Rica**  | 21.126| 0.250                         | 0.913     |
| **Mexico**     | 10.383 | 0.076                         | 0.702     |



The results show a global improvement in model fit after adding explanatory variables. These enhancements reduced the mean squared error (MSE) in each case, particularly in Costa Rica and Luxembourg, where trade and investment variables showed strong correlation with wage outcomes.

However, we also acknowledge limitations. The regressions were based on approximately 20 years of data, which increases the risk of overfitting, especially given the small sample sizes. Several of the selected variables are highly collinear or trend strongly over time. Future work should incorporate out-of-sample validation or regularization techniques to ensure robustness.

## Part 2: Convergence Enhancement

In the Convergence Enhancement part, the focus shifts from estimating wages in relatively data-rich OECD countries to analyzing wage convergence trends in less developed countries. The central goal is to enhance Dr. Cashmere Flow’s baseline wage convergence model by incorporating macroeconomic and institutional variables that may influence wage evolution in fragile or transitioning economies. 

In Part 2, we are trying to improve the model’s ability to predict wage convergence for countries that face unique structural challenges, including political instability, climate shocks, inflation volatility, and economic dependency on single sectors (like oil or agriculture). Dr. Flow’s original model is based on historical wage data alone. However, in many less developed countries, historical wage data is either unreliable or incomplete, and external factors often drive wage dynamics more than past trends. Therefore, our objective is to construct enhanced country-specific models by adding custom-selected explanatory variables (e.g., conflict presence, FDI, inflation, or labor force participation). These variables help better explain how and why wages evolve in each country and whether convergence toward OECD benchmarks is feasible or not, in a near furture.

To ensure our models are specific to context and data-driven, we begin with a qualitative and quantitative country-level analysis for each assigned country. Only after we proceed to build the convergence enhancement model using regression that integrates these chosen factors.

### Country Level Analyses

#### 1. Central African Republic

**Step-by-Step Analysis**

The Central African Republic faces profound structural barriers to wage development due to ongoing security concerns, political instability, and persistent humanitarian crises. Our initial review focused on identifying macro and institutional-level indicators that capture the fragile state of the economy. Inflation was a key candidate, as it erodes real income in a context where price volatility is frequent and wage indexation is weak. We also considered the role of armed conflict and water-related environmental stress, given their importance to economic stability and agricultural livelihoods. Aspects such as conflict type and military personnel percentages serve as proxies for national stability, while environmental variables like annual precipitation and water stress relate to climate change, and with it, agricultural productivity, a major wage source in rural areas.

**Data Collection and Challenges**

Gathering data for the Central African Republic was challenging due to sparse time-series coverage (for the period 1993–2023) and the country’s limited statistical infrastructure. While many macroeconomic datasets exist, few are consistently reported for the entire study period. Key wage-relevant indicators, like employment structure, government social spending, or sector-specific wages, were either missing or non-standardized. We ultimately retained variables with reliable and long-term availability: inflation (consumer prices), armed forces employment share, conflict type, FDI inflows, water stress, and precipitation. Although these variables are broad, they capture the systemic pressures on income and employment in a fragile, agriculture-based economy.

**Variable Selection and Impact**

We chose to work with a dummy variable that indicates whether or not a conflict took place in the country in a given year. This variable significantly affected the regression, as it directly impacts political and economic stability. We also tested climate-related variables (e.g. water stress), but found their influence on the results to be limited.

#### 2. Burkina Faso

**Step-by-Step Analysis**

Burkina Faso’s economic development and wage patterns are shaped by competing forces: strong agricultural and service-sector growth on one hand, and instability from terrorism, climate shocks, and political volatility on the other. Our analysis began by identifying key drivers of wage formation in this dual environment. Inflation and security were immediate considerations, but we also incorporated indicators of climate vulnerability, such as water stress and precipitation levels, as agriculture remains a primary employer. Additionally, FDI and military personnel shares were considered to assess the effects of external investment and internal instability on economic opportunity and labor income.

**Data Collection and Challenges**

Burkina Faso’s data environment presents both strengths and gaps. Some indicators, like FDI, inflation, and armed forces employment, were readily available from international databases. However, social and institutional indicators such as sectoral wage data, conflict intensity, or social protection were either missing or not granular enough. Climate variables posed challenges in consistency, though we were able to source annual precipitation and water stress figures for the full period. Ultimately, a limited dataset was constructed, focused on inflation, conflict presence, water access, and external capital flows, suitable proxies for understanding wage evolution in this particular context.

**Variable Selection and Impact**

We selected precipitation as a climate-related variable with strong ties to the country’s agricultural sector, and by extension, its wage dynamics. The impact of precipitation on wages was more pronounced than other tested indicators like FDI.


#### 3. Argentina

**Step-by-Step Analysis**

Argentina’s wage dynamics have been driven by persistent macroeconomic instability, marked by inflation volatility, debt restructuring, and recessionary cycles. Our wage modeling began with an emphasis on disinflation trends and monetary stability, as these directly impact real wage growth and consumer purchasing power. We also considered structural drivers of growth and employment, such as participation in the labor force and the contribution of agriculture and mining to GDP. FDI and oil rents were included to reflect sectoral investment and natural resource dependence, while political stability served as an institutional factor that influences investor confidence and economic planning.

**Data Collection and Challenges**

Argentina has a comparatively rich data environment, with access to detailed macroeconomic indicators and sectoral breakdowns. Nevertheless, harmonizing data across institutions and over long time periods posed challenges, potentially due to changes in measurement practices during economic crises. Political variables were also challenging to standardize, though we found annual estimates for political stability through global governance indicators. Ultimately, we retained variables with full coverage and policy relevance: inflation (GDP deflator), FDI inflows, oil rents, agricultural share of GDP, political stability, and labor force participation, that hopefully reflect Argentina’s structure.

**Variable Selection and Impact**

We selected inflation (GDP deflator) as the most explanatory variable for Argentina, given its high macroeconomic salience and direct relationship with purchasing power and wage erosion.


#### 4. Lesotho

**Step-by-Step Analysis**

Lesotho’s wages and labor dynamics are shaped by structural dependence on South Africa, frequent political turnover and vulnerability to environmental shocks. In developing a wage model, we focused on indicators tied to Lesotho’s economic volatility and employment trends. Inflation was a starting point given its influence on real income. Given Lesotho’s exposure to drought and climate volatility, we included measures of freshwater resources per capita. Labor force participation was used to track employment trends over time, and FDI served as a proxy for external capital inflows supporting domestic production and wages.

**Data Collection and Challenges**

Data collection for Lesotho was limited by the little availability of institutional variables and high-resolution employment data. In particular, access to sectoral data on mining, manufacturing, or trade dependence with South Africa was sparse. Social indicators such as social transfers or household consumption were also difficult to obtain. However, we were able to compile a reliable panel with FDI, GDP deflator inflation, water availability, and labor participation, all of which are broadly relevant to the country’s wage environment. These selections allowed us to capture both macroeconomic forces and climate-linked stressors influencing household income.

**Variable Selection and Impact**

For Lesotho, we first tried to use the inflation variable, but we did not see a significant influence on the results. We therefore chose to work with the 'Labor force participation rate’; which gave us more satisfactory results.

#### 5. Azerbaijan

**Step-by-Step Analysis**

Azerbaijan’s labor and wage trends are undergoing a structural transition from a hydrocarbon-dependent economy to a more diversified one. The government’s recent “Enhancing Social Welfare” decree and minimum wage reforms were important contextual factors in our analysis. We began by identifying indicators tied to fiscal and sectoral transformation: oil rents and fuel exports reflect the traditional resource base, while employment ratios and agricultural value added capture diversification. Inflation and FDI were included to reflect broader economic conditions, and we also monitored conflict-related impacts via annual death statistics.

**Data Collection and Challenges**

Despite better institutional capacity than some of its regional peers, Azerbaijan presented some unique data challenges. Social policy impacts (like welfare expansion) were not directly quantifiable in time-series format. Similarly, gender and regional wage disaggregation were not available. However, macroeconomic variables, including inflation, oil rents, fuel exports, FDI and employment ratios, were consistently reported and suitable for long-term analysis. We focused on variables that linked sectoral transformation and wage outcomes, creating a framework that could assess both past petroleum-led wage structures and future wage potential in the non-oil economy.

**Variable Selection and Impact**

For Azerbaijan, we chose to work with a variable that reflected the impact of the climate risks on the country’s economy. We therefore chose the “Agriculture, forestry, and fishing, value added (% of GDP)” as a proxy for water stress, and we witnessed an improvement in the model.


### Coding the Convergence Enhancement Model

After completing the country-level analysis for our assigned non-OECD basket, the next step is to integrate the selected macroeconomic and institutional variables into a convergence enhancement model. The goal of this phase is to go beyond Dr. Cashmere Flow’s baseline wage estimates and assess how well additional country-specific variables can improve wage prediction accuracy.

In the analysis, five countries (Lesotho, Argentina, Azerbaijan, Burkina Faso, and the Central African Republic) are treated as special cases because additional contextual variables are available. The wage forecasting models for these countries include both time and a country-specific variable as explanatory inputs. Including these variables must meet strict coverage requirements, specifically covering the period from 1991 to 2023. Due to the complexity of handling multivariate inputs in nonlinear models, these countries are modeled exclusively using linear and quadratic regressions, where the structure can accommodate multiple predictors more reliably.

In contrast, all other countries adhere to the original modeling framework, using time as the sole independent variable to predict log-transformed estimated wages. These cases are evaluated using a broader suite of models, allowing for more flexible curve fitting based purely on historical wage trajectories without additional data.

The graph below illustrates the performance of our enhanced convergence models across the five non-OECD countries. While the inclusion of macroeconomic and institutional variables provided promising results in select cases (e.g., Argentina), the overall outcomes were mixed. It is important to highlight that the integration of additional variables did not consistently improve convergence accuracy. In some instances, such as Lesotho, the enhanced model performed worse than the baseline, diverging from the benchmark rather than approaching it. These inconsistencies underscore a key point: while some context related variables can offer valuable explanatory power, their inclusion must be rigorously validated. Its is therefore important to acknowledge that the forecasting models aren't perfect. Plus, the data of the variable has to cover the period of 1991 to 2023 without any missing values, and some of the important factors were not directly quantifiable in time-series format. The results reflect the best possible outcomes given the data limitations at this stage. The lack of quantified prediction changes is another limitation of our work, because we can only spot differences by visually comparing the old and new graphs.

<p align="center">
  <img src="https://github.com/adbertin/salaryConvergence/blob/6b80f24ed12a7b7a2c456d2ddf2b08db875343b6/Part2_Results.png" width="500"/>
</p>

Based on our country-level analysis, several context-specific variables show strong potential to improve wage estimates and convergence forecasts. Adding these variables can make models more insightful and accurate. However, the biggest challenges remain data availability and quantifying their impact, which limited our current work. Going forward, it's crucial to carefully select and validate any additional variables to ensure they genuinely improve the model’s predictive power.
To conclude for this part, the convergence enhancement framework shows strong potential, but future work should maybe place emphasis on variable selection, multicollinearity checks and robustness testing. The quality and relevance of additional data will ultimately determine the model's effectiveness in improving wage prediction and understanding convergence dynamics.

## Future recommendations
Based on our country-level analysis, several context-specific variables demonstrate strong potential to enhance wage estimation and improve the accuracy of wage convergence forecasts. As demonstrated in the analysis, incorporating additional country-specific variables can enrich the model's explanatory power and offer more nuanced insights into wage dynamics. Expanding this approach to include additional relevant variables for other countries could further strengthen predictive performance.

However, it's important to note that the inclusion of additional variables in our current implementation did not consistently lead to improved convergence outcomes. In fact, for some cases (such as Lesotho), the revised model diverged more from the benchmark than moving closer to it. While the approach has high potential, selecting and integrating additional variables must be carefully validated to ensure they contribute meaningfully to forecasting objectives.

## Credits

We would like to thank Mr. Noé Notter for his work and guidance during this project. We also would like to thank Mr. Michalis Vlachos, our teacher, for his classes.

## References
* [Silva, A. R. C., Pavez, L. R. D., & Martínez-Zarzoso, I. (2023). The impact of migration on wages in Costa Rica. *Migration Studies*, 11(1), 23–51.](https://doi.org/10.1093/migration/mnac041)
* [Garita, J. (2021). Minimum wages and firm dynamics: evidence from Costa Rica’s Occupation-Based System.](https://jggarita.github.io/files/MW_firmdynamics.pdf)
* [Gindling, T. H., & Terrell, K. (2005). The Effect of Minimum Wages on Actual Wages in Formal and Informal Sectors in Costa Rica. *World Development*, 33, 1905–1921.](http://dx.doi.org/10.1016/j.worlddev.2005.04.017)
* [Cortez, W. W. (2001). What is behind increasing wage inequality in Mexico? *World Development*, 29(11), 1905–1922.](https://doi.org/10.1016/S0305-750X%2801%2900068-7)
* [Robertson, R. (2007). Trade and Wages: Two Puzzles from Mexico. *World Economy*, 30(9), 1378–1398.](https://doi.org/10.1111/j.1467-9701.2007.01048.x)
* [Arezki, R., & Matsumoto, A. (2017). Chapter 5. Metal Prices Signal Global Economic Shifts. *Shifting Commodity Markets in a Globalized World*.](https://doi.org/10.5089/9781484310328.071.ch005)
* [Banco de la República. Distribución del ingreso laboral y efectos de la informalidad en Colombia.](https://repositorio.banrep.gov.co/server/api/core/bitstreams/6db78584-da96-4f8b-a0c9-fb5a306cdffc/content)
* [International Labour Organization (ILO). (2022). Global Wage Report 2022–2023.](https://www.ilo.org/sites/default/files/wcmsp5/groups/public/@ed_protect/@protrav/@travail/documents/publication/wcms_862569.pdf)
* [Solís, L., & Esquivel, G. (2009). El empleo formal y la informalidad en México: evolución y determinantes. *Investigación Económica*, 68(269), 13–58.](https://www.scielo.org.mx/pdf/ineco/v68n269/v68n269a5.pdf)
* [de Mooij, R., Hebous, S., Hines Jr., J. R., & Olbert, M. (2020). International taxation and Luxembourg’s economy (IMF Working Paper No. 2020/249).](https://www.imf.org/en/Publications/WP/Issues/2020/11/26/International-Taxation-and-Luxembourgs-Economy-49879)
* [Guarda, P., Jeanfils, P., & Turtelboom, B. (2000). Wages, prices and employment: The Luxembourg supply side.](https://www.researchgate.net/profile/Paolo-Guarda/publication/259465820_Wages_prices_and_employment_the_Luxembourg_supply_side/links/02e7e52bdb2d7da64e000000/Wages-prices-and-employment-the-Luxembourg-supply-side.pdf)
* [Why the Central African Republic should invest now in its human capital to give itself a future. World Bank Blog.](https://blogs.worldbank.org/en/africacan/why-central-african-republic-should-invest-now-its-human-capital-give-itself-future)
* [Coface for Trade – Central African Republic Risk Assessment.](https://www.coface.com/news-economy-and-insights/business-risk-dashboard/country-risk-files/central-african-republic)
* [The World Bank in Burkina Faso (2025). Country Overview.](https://www.worldbank.org/en/country/burkinafaso/overview#1)
* [Burkina Faso Economic Outlook – African Development Bank.](https://www.afdb.org/en/countries/west-africa/burkina-faso/burkina-faso-economic-outlook)
* [African Economic Outlook 2024 – Country Notes.](https://www.afdb.org/sites/default/files/2024/06/06/aeo_2024_-_country_notes.pdf)
* [The World Bank in Lesotho – Country Overview.](https://www.worldbank.org/en/country/lesotho/overview)
* [JAMnews (2024). Azerbaijan to increase minimum wage by 16% in 2025.](https://jam-news.net/azerbaijan-to-increase-minimum-wage-by-16-in-2025/)
* [Humay Aghajanova (2024). Wages, social benefits to rise in 2025.](https://en.trend.az/azerbaijan/society/3949080.html)
* [Aghakazim Guliyev (2024). Azerbaijan sees significant growth in employment with 70,000 new jobs in 2024.](https://caliber.az/en/post/azerbaijan-sees-significant-growth-in-employment-with-70-000-new-jobs-in-2024)

