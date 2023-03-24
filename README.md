# Climate and housing

Visualises how heating and cooling needs are changing in Australian homes, and how renters are coping with the changes.

## 🎨 Share the visuals

The visuals created from this analysis are available on Flourish for you to add to a story or to duplicate and edit:

[Average energy star rating map](https://public.flourish.studio/visualisation/13034789)

[![Average energy star rating map](https://user-images.githubusercontent.com/6520659/227407950-d736f2a2-f9bb-46b4-8da1-100e4b9535d9.png)](https://public.flourish.studio/visualisation/13034789)

[Heating and cooling hours: present and future](https://public.flourish.studio/visualisation/13010999)

[![Heating and cooling hours](https://user-images.githubusercontent.com/6520659/227407947-ad656795-da39-4d9a-b413-51e9f105d5af.png)](https://public.flourish.studio/visualisation/13010999)

[Renters struggling in summer heat/winter cold](https://public.flourish.studio/visualisation/13010665)

[![Renters struggling in summer heat_winter cold](https://user-images.githubusercontent.com/6520659/227407942-0da50bb5-c8bc-487b-bc93-62afc228515c.png)](https://public.flourish.studio/visualisation/13010665)

## Use + Remix rights

![[Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0)](https://mirrors.creativecommons.org/presskit/buttons/80x15/png/by.png)

These charts, as well as the analyses that underpin them, are available under a Creative Commons Attribution 4.0 licence. This includes commercial reuse and derivates.

Data in these charts comes from:

- [Typical Meteorological Year weather files for building energy modelling](https://agdatashop.csiro.au/future-climate-typical-meteorological-year), CSIRO
- [Projected weather files for building energy modelling](https://agdatashop.csiro.au/future-climate-predictive-weather), CSIRO
- [Australian Housing Condition Data Infrastructure](https://doi.org/10.26193/IBL7PZ)
- [NatHERS](https://www.nathers.gov.au/nathers-accredited-software/nathers-climate-zones-and-weather-files)

**Please attribute 360info and the data sources when you use and remix these visualisations.**

## Reproduce the analysis

### 💨 Quickstart: use the dev container

This project comes with a ready-to-use [dev container](https://code.visualstudio.com/docs/remote/containers) that includes everything you need to reproduce the analysis (or do a similar one of your own!), including [R](https://r-project.org) and [Quarto](https://quarto.org).

1. [Launch this project in GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=603980423)
2. If you have Docker installed, you can build and run the container locally:
  - Download or clone the project
  - Open it in [Visual Studio Code](https://code.visualstudio.com)
  - Run the **Remote-Containers: Reopen in Container** command

Once the container has launched (it might take a few minutes to set up the first time), you can run the analysis scripts with `quarto render`.

However, some of the scripts require source data that we cannot include in the repository for either size reasons or privacy reasons (see [`/data`](/data)). You may need to add these files to the `data` folder before the scripts will run.

You can, however, do additional analysis on the tidied and aggregated results. Analysis scripts are in `analysis/**/*.qmd`.

### Manual setup

To setup a development environment manually, 

You'll need to:
- [Download and install Quarto](https://quarto.org/docs/get-started)
- [Download the install R](https://www.r-project.org)
- Satisfy the R package dependencies. In R:
  * Install the [`renv`](https://rstudio.github.io/renv) package with `install.packages("renv")`,
  * Then run `renv::restore()` to install the R package dependencies.
  * (For problems satisfying R package dependencies, refer to [Quarto's documentation on virtual environments](https://quarto.org/docs/projects/virtual-environments.html).)

## Help

If you find any problems with our analysis or charts, please feel free to [create an issue](https://github.com/360-info/report-climate-housing/issues/new)!
