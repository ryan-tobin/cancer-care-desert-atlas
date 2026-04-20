# Bridging the Gap: Identifying Spatial and Economic Access Deserts for Oncology Care in Philadelphia

#### **Author:** Ryan Tobin

#### **Date:** April 2026

## Executive Summary

Despite housing some of the nation's premier oncology and genomics research centers, Philadelphia exhibits profound disparities in cancer care access. This spatial analysis evaluates geographic accessibility to specialized oncology centers—including CHOP, Penn Medicine, Jefferson Health, Temple Health, Einstein, and the VA Medical Center—against neighborhood-level socioeconomic data. The findings identify critical "access deserts" where lower-income populations are functionally isolated from advanced cancer care by transit barriers.


## Background

Advances in oncogenomics and precision medicine are rapidly transforming cancer survivorship. However, the efficacy of these clinical breakthroughs is fundamentally limited by a patient's physical ability to access treatment. Philadelphia is deeply stratified by race and income, with a poverty rate of approximately 20.3% and a demographic makeup that is roughly 43.6% Black, 34.3% White, and 15.2% Hispanic/Latino. In this landscape, spatial barriers to healthcare exacerbate existing clinical inequalities. When a 15-minute commute turns into an hour-long, multi-transfer ordeal, preventative screenings and consistent outpatient treatments drop off, often leading to delayed diagnoses that present as late-stage emergencies. This project bridges spatial epidemiology and clinical realities to quantify these transit-based exclusion zones.

## Methodology

This analysis utilized Python-based geospatial tools (GeoPandas, OSMnx, and NetworkX) to model the physical street network of Philadelphia. Drive-time and walk-time isochrones were computed to simulate maximum travel thresholds (e.g., 10-minute and 15-minute intervals) originating from six major oncology hubs.

By calculating true network distance rather than simple straight-line distance, the model accurately accounts for urban infrastructure barriers like rivers and highways. These spatial access polygons were subsequently overlaid onto a demographic base map generated using the US Census API, which stratified the city's census tracts by Median Household Income.

## Key Findings

The spatial overlay reveals distinct disparities in healthcare access. The network geometry of the isochrones heavily favors the city's wealthier, centrally located neighborhoods. Conversely, large swaths of North, West, and Southwest Philadelphia—areas characterized by significantly lower median household incomes and higher proportions of minority residents—fall completely outside the optimal 10-minute and 15-minute driving catchments.

These neighborhoods represent distinct "access deserts." For patients in these zones, the compounding burdens of transit time, fuel costs, and lacking infrastructure present severe barriers to receiving longitudinal cancer treatment, such as daily radiation or regular infusion therapies.

## Policy Recommendations
1. **Decentralized Outpatient Services:** Health systems should utilize this spatial data to target the establishment of satellite infusion centers and oncology clinics within identified access deserts, specifically in North and Southwest Philadelphia.

2. **Subsidized Medical Transit:** City policymakers and healthcare administrators must collaborate to implement point-to-point, subsidized non-emergency medical transportation (NEMT) for oncology patient residing outside the 15-minute access zones.

3. **Targeted Screening Initiatives:** Public health outreach, including mobile genomics screening and preventative oncology services, should be aggressively prioritized in these geographically isolated census tracts to catch high-risk patients before intensive, centralized emergency intervention is required.