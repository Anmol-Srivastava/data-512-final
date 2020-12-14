# The Prison "Boom"

This repository hosts my final project for DATA 512 (Human-Centered Data Science), which is intended to be a reproducible, useful, and user-friendly body of research and analysis. My proposed project is the use of US Census Data and US Bureau of Justice statistics to investigate the increasing number of people swallowed up by the American prison system. In my project, I will track the geographical and time-wise points of interest for this increase. 

# Abstract

This research studies the expansion of prison populations in the US, over time. Two central research questions are posed; firstly, does the time series growth of prison populations (nation-wide) prove to be anomalous or excessive (in comparison with overall populations)? Can major historical events that are oriented around incarceration be shown to coincide with anomalies? Secondly, does the growth of prison counts over time differ among states? Is there any grouping of states that can explain emergent differences in incarceration rates from 1977 to 2010? Anomalous years of prison populations are determined by Isolation Forest; it is determined that Isolation Forest predictions are too erratic and inconsistent to be well-explained by historical events. However, predicted anomalies do occur around visually-observed spikes in prison counts, which in turn do coincide with notable policies like the War on Drugs, 1994 Crime Bill, etc. One-Way ANOVA (using incarceration increase as a function of region and Senate election results) is used to group states and test for differences in growth. Two-Way ANOVA using both region and political results (with interaction) is also performed. In all tests, there is a failure to reject the null hypothesis of no difference in growth rates among "bins" of states. However, it is observed in all experiments that absent data quality (specifically, granularity) is a major obstacle in accepting these results. It is concluded that prison growth has been sharp since 1970, and disturbing patterns of 2x/3x growth in Eastern and coastal states are appearing (though statistically insignificant). Further data acquisition and more detailed studies are advised.

# Repository Structure

- `figures/`, all images included in this repository, including screenshots, charts, and results from analyses
- `data/`, all data files used in the analyses
    - `raw/`, the raw data files accessed online as outlined in [Data.ipynb](./Data.ipynb)
    - `clean/`, the sanitized, Python-ready version of downloaded files
- `proposals`, the inital and late-stage proposals for this project (*__note__*: both of these will differ significantly from the final product, as issues in data quality, time availability, and analytical potential arise)
- `Data.ipynb`, a Jupyter Notebook containing all steps for accessing and cleaning relevant data for analysis
- `Main.ipynb`, the complete Jupyter Notebook containing project descriptions, analysis code, results, discussions, and resources
- `LICENSE`, the MIT-style license for this repository

# Data Licensing

The [Communicating With Prisoners](https://www.acrosswalls.org) project compiled counts of [Prisoners By State And Sex](https://www.acrosswalls.org/datasets/prisoners-us-state-sex-panel/) from 1880 to 2010. This is a count from federal and state correctional facilities, itself coming from the [US Bureau of Justice Statistics Prisoner Series](https://www.bjs.gov/index.cfm?ty=pbse&tid=0&dcid=0&sid=40&iid=0&sortby=&page=paging&curpg=4). Under the CCO 1.0 Universal Public Domain Dedication license, free use and distribution thereof is permitted. [See this description](https://creativecommons.org/publicdomain/zero/1.0/).

US population data comes primarily from the US Census Bureau: via the decennial Census, which filled decades with constant-growth estimates until 1960, and the yearly American Community Survey thereafter. The aggregator here is the international [World Bank Group](https://www.worldbank.org/). Specifically, its [World Development Indicators](https://datacatalog.worldbank.org/dataset/world-development-indicators) project collects vast development data for several countries. Its [aggregation of population over time in the US](https://data.worldbank.org/indicator/SP.POP.TOTL?locations=US) is cited as a direct combination of the Census Bureau data. Under the Creative Commons Attribution 4.0 International License, use, distribution, and adaptation of this resource is permitted. See the aggregator [Terms of Use](https://data.worldbank.org/summary-terms-of-use).