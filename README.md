# Salary Convergence
Team Google (Apolline Bertin & Fang-Hsuan Chen)

This project investigates global wage convergence as a lens to better understand economic inequality across countries. Building on the work of Dr. Cashmere Flow, we aim to refine his baseline model which estimates wages in Purchasing Power Parity (PPP) terms using historical data, by incorporating additional macroeconomic and institutional variables that may explain why some countries are closing the wage gap with advanced economies, while others are falling behind.

Our analysis is conducted in two parts:

- Part 1 – Benchmark Estimation (OECD countries): We try to improve the fit between estimated and true OECD wages by testing functional enhancements using relevant country-specific variables (e.g., oil revenue in Norway, tourism receipts in Greece).

- Part 2 – Convergence Enhancement (Non-OECD countries): We explore deeper drivers of convergence or divergence in selected non-OECD countries by integrating explanatory variables such as conflict exposure, foreign investment, inflation and climate indicators.

Our work involves detailed country-level analysis, model building, and statistical evaluation. We compare our enhanced predictions with Dr. Flow’s original baseline using error metrics such as MSE, and visualize wage convergence trends. The goal is to contribute new insights into the mechanisms driving wage inequality and offer a reproducible methodology for future comparative economic research.

All code, data, and visualizations are included in this repository. A video walkthrough of our approach is available here (link to be added). 

## Table of Contents
1. How to Run through the Project
2. How to Use the Project
3. Part 1: Benchmark Estimation
4. Part 2: Convergence Enhancement
5. Future recommendations
6. Credits
7. References (add where we found the data and link to tables)
   
## How to Run through the Project

Everything you need for the project is on this github repository: 
Github link: [Link](https://github.com/adbertin/salaryConvergence). 

Please follow the link to the video: [Link](https://youtu.be/JGLpjJL7K5s). 

For additional information regarding the data we found (e.g. sources), or about our data analysis, please follow the link to our Drive folder: [Link](https://drive.google.com/drive/folders/1rAaQe7x9-qscZJkETNIMwFP33fkr-0br?usp=drive_link).

## How to Use the Project

The data we used mostly come from the following sources:
- it was either already provided in the folder we were given to work on this project,
- from the [Our World in Data](https://ourworldindata.org/) website,
- from the [World Bank Group](https://www.worldbank.org/ext/en/home) database,
- from the [Statista](https://www.statista.com/) dataset,
- or from the [Eurostat](https://ec.europa.eu/eurostat/en/) database.

Exceptionnaly, some additional databases were used in specific cases (e.g. coffee imports data for Colombia), and are referenced in the Drive folder we shared previously.
The .csv files containing the explanatory variables that we found and used are formated under the name "Variables_[countryname].csv" in the main branch of the repository.

For the coding part, we have divided the work into 2 code files that you can directly run via the github repository: 
- [Code for Part 1: Benchmark Estimation](https://github.com/adbertin/salaryConvergence/blob/1922435764739b07a890fd32b49297f4c7131a63/Google_Part1_final.ipynb). 
- [Code for Part 2: Convergence Enhancement](https://github.com/adbertin/salaryConvergence/blob/1922435764739b07a890fd32b49297f4c7131a63/Google_Part2_final.ipynb).

Results of Part 1 were stored in this [updated file](https://github.com/adbertin/salaryConvergence/blob/1922435764739b07a890fd32b49297f4c7131a63/Countries_Wages_Estimates_Finals_GOOD_new.csv), and used in Part 2 of our research.

Finally, all extra material that you can find on our github repository was provided for us by Noé Notter. 

### Part 1: Benchmark Estimation
### Part 2: Convergence Enhancement
### Conclusion 
### Future recommendations
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

