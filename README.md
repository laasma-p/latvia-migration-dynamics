# Migration Dynamics in Latvia (2016-2025)

Public discussions about migration often revolve around gross arrival and departure numbers, or whether more people of certain ethnicities arrive in Latvia for long-term stays than others. The objective of this project is to analyze official Latvian migration statistics from 2016 to 2025 to determine the net impact of migration on the country's population and identify the patterns behind the data by age, sex, country group, and ethnicity.

## Analytical Questions

1. Is net migration positive or negative overall across the given time period?
2. Which age groups show the largest net migration losses?
3. How have migration flows changed across country groups over time?
4. Are there noticeable differences in migration volumes and migration balances between men and women?
5. Which ethnicities have the largest recorded arrivals and departures?

## Data Sources

Data is retrieved from [Oficiālās statistikas portāls](https://stat.gov.lv/lv). Three datasets are used, stored in the `data/raw` folder: `ibe010-migration-by-country-groups-2016-2025-raw.csv`, `ibe030-migration-by-age-groups-and-sex-2016-2025-raw.csv` and `ibe040-migration-by-ethnicity-2016-2025-raw.csv`.

The first dataset details immigration and emigration volumes, categorized by various country groups. The second dataset contains immigration and emigration counts broken down by age groups and sex. The third dataset captures the ethnicity of immigrants and emigrants.

## Tools and Technologies

- **Language**: Python
- **Python Libraries**: Pandas, Matplotlib, Seaborn
- **Version Control System**: Git
- **Interactive Dashboards**: Power BI Desktop
- **Environment**: IntelliJ IDEA, Jupyter Notebook

## Planned Methodology

1. **Data Cleaning**: Melting wide-format datasets into long format, standardizing column names and data types, handling missing values, and preserving Latvian character encoding.
2. **Transformation**: Calculating net migration across all datasets.
3. **Exploratory Data Analysis**: Identifying historical trends, anomalies, and imbalances by sex, age, and ethnicity across years.
4. **Data Visualization**: Building interactive Power BI dashboards to present key findings visually.

## Limitations

The following limitations apply to `ibe010-migration-by-country-groups-2016-2025-raw.csv` and should be considered when interpreting trends over time:

- The population size at the beginning of 2023 and 2024 was recalculated using a new estimation method. This affects the migration estimates and results in a methodological break in the time series.
- Migration data for 2022 were not recalculated, therefore that data is not fully comparable with the population size at the beginning of 2023.
- Since 2019, Ukraine is no longer a member of NVS country group.
- Since 2021, Moldova is no longer a member of NVS country group.
- Until 2018, `Pārējās valstis` has been calculated without the UK.
- Since 2019, `Pārējās valstis` has been calculated with the UK.

The following limitations apply to `ibe030-migration-by-age-groups-and-sex-2016-2025-raw.csv` and should be considered when interpreting trends over time:

- The population size at the beginning of 2023 and 2024 was recalculated using a new estimation method. This affects the migration estimates and results in a methodological break in the time series.
- Migration data for 2022 were not recalculated, therefore that data is not fully comparable with the population size at the beginning of 2023.
- The population estimate published on June 2 was revised on October 2, 2025, and the usual resident population nw includes foreign students.
