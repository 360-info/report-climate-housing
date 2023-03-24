# `/data`

## NatHERS boundaries

The analysis script downloads a map of postcodes to [NatHERS Climate Zones](https://www.nathers.gov.au/nathers-accredited-software/nathers-climate-zones-and-weather-files). It then produces:

- `nathers-zone-names.csv`: a map of zone numbers to names
- `naters-zones.csv`: a map of postcodes to zone names and numbers
- `nathers-boundaries.geojson`: boundaries of zones, with names and numbers attached. This is based on ABS postcode boundaries and the above map of postcodes to zones.

## Star ratings

`star-ratings.xlsx` is a spreadsheet of statistics on the star ratings of houses and apartments in different [NatHERS Climate Zones](https://www.nathers.gov.au/nathers-accredited-software/nathers-climate-zones-and-weather-files).

There are two sheets in the workbook: one on the average energy star rating, another with the proportion of homes in each energy star rating bucket. `star-ratings-average.csv` is a tidied CSV of the Average ratings sheet.

**Note that all figures in this workbook have been redacted where there are fewer than 10 homes.** This particularly affects conclusions in the workbook of proportions, as the raw counts are not available and the proportions appear to be based on the unredacted properties only.

Figures are also provided separately for new builds, renovations and existing dwellings.

New build and renovation data is based on actual certificates issues between 2016 and 2021. Existing dwelling data is simulated by removing energy saving features from the new build and renovation certificate data. Existing dwelling simulations are only available in some areas.

## Survey results

These are aggregated results from the [Australian Housing Condition Data Infrastructure](https://doi.org/10.26193/IBL7PZ)—specifically questions 12 and 13, concerning the proportion of  renters that are able to stay comfortable in summer heat or winter cold. The aggregations are done by NatHERS climate zone.

- `survey-discomfort-summerwinter-wide.csv`: the results of Q12 and Q13 are listed for each NatHERS climate zone. Columns include:
  * `zone`: NatHERS zone number
  * `town`: NatHERS zone name
  * `signif`: whether the difference in proportion between summer and winter is statistically significant
  * `ntotal_Winter`, `ntotal_Summer`: the number of participants in the question who answered either `Yes` or `No`.

  * `n_Winter`, `n_Summer`: the number of people who answered `No`. 
  * `p_Winter`, `p_Summer`: the proportion of people who answered `No`. 
  * `moe_Winter`, `moe_Summer`: the margin of error on the estimate.
  * `nlow_Winter`, `nlow_Summer`: the lower bound on the estimated number of people who answered `No`
  * `plow_Winter`, `plow_Summer`: the lower bound on the estimated proportion of people who answered `No`
  * `nhigh_Winter`, `nhigh_Summer`: the higher bound on the estimated number of people who answered `No`
  * `phigh_Winter`, `phigh_Summer`: the higher bound on the estimated proportion of people who answered `No`
  * `balance`: the significance of the difference between summer and winter.

# Not included with the repository

### Typical and projected climate

`/data/csiro-climate/projections` and `/data/csiro-climate/typical` should contain the unzipped contents of:

- `typical`: [Typical Meteorological Year weather files for building energy modelling](https://agdatashop.csiro.au/future-climate-typical-meteorological-year)
- `projections`: [Projected weather files for building energy modelling](https://agdatashop.csiro.au/future-climate-predictive-weather)

These files are not included in the repository due to their size, but they are freely available from the above links at the CSIRO AgData Shop.

## Survey results

`02_AHCD_Sensitive_Data_File_001469.dta` contains the record-level survey results from the [Australian Housing Condition Data Infrastructure](https://doi.org/10.26193/IBL7PZ). This data cannot be shared without permission. You can apply for permission to download the data, as well as the data dictionary, from the [ADA Dataverse page](https://doi.org/10.26193/IBL7PZ).