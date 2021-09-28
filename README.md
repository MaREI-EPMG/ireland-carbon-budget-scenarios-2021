<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

# Carbon Budget Scenarios for Ireland's Energy System, 2021-50

[![Frictionless](https://github.com/MaREI-EPMG/ireland-carbon-budget-scenarios-2021/actions/workflows/frictionless.yaml/badge.svg)](https://repository.frictionlessdata.io/report?user=MaREI-EPMG&repo=ireland-carbon-budget-scenarios-2021&flow=frictionless)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5517363.svg)](https://doi.org/10.5281/zenodo.5517363)

This repository constains energy system scenarios for Ireland meeting decarbonisation targets for 2030 and 2050 using the TIMES-Ireland Model (TIM).

## Exploring the Scenarios

Various tools can be used to explore the scenarios in this data package. These include a dedicated [web app][TIM Carbon Budgets 2021 SPA], [pyam][pyam github repository] package, [Friendly data][friendly_data github repository] and spreadsheet software (e.g. MS Excel).

### TIM Carbon Budgets 2021 Web App

The [TIM Carbon Budgets 2021 Web App][TIM Carbon Budgets 2021 SPA] visualises most of the scenarios included in this data package. Up to two scenarios can be selected for comparisson and the difference can be computed. Please note that **About**, **Scenarios** and **Documentation** pages are pending update.

### pyam

[pyam][pyam github repository] provides a suite of tools and functions that can be used to analyse and visualise scenario data included in this data package. A brief pyam-tutorial is included in this repository (many thanks to [@danielhuppmann](https://github.com/danielhuppmann/) for contributing) and the rendered version can be accessed [here][rendered pyam-tutorial].

### Friendly data

[Friendly data][friendly_data github repository] allows easy conversion of a frictionless data package to standard Python data structures e.g., pandas DataFrame. For instance the following code snippet can be used to convert the data package to a list of pandas DataFrame (many thanks to [@suvayu](https://github.com/suvayu/) for providing an example):
```
from friendly_data.dpkg import read_pkg
from friendly_data.converters import to_df

pkg = read_pkg("datapacakge.json")

dfs = [to_df(r) for r in pkg.resources]   # data package as a list of pandas.DataFrame
``` 

[TIM Carbon Budgets 2021 SPA]: https://tim-carbon-budgets-2021.netlify.app/results
[pyam github repository]: https://github.com/IAMconsortium/pyam
[friendly_data github repository]: https://github.com/sentinel-energy/friendly_data
[rendered pyam-tutorial]: https://github.com/MaREI-EPMG/ireland-carbon-budget-scenarios-2021/blob/main/pyam-tutorial.ipynb