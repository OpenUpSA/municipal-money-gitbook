# Potential improvements

## Splitting data portal and scorecard into separate projects

* Move 'geography' data to data portal application
* Create separate repositories
* Present the scorecard site as an example of what can be done using data from the data portal
* Provide easy access to code and queries used to compile indicators
* Provide an API for Scorecard data

## Improve modularity of municipal profile compilation code

* ApiData object can be reused when compiling profiles
* Make targeted indicators dynamic for each compilation (currently hard coded)
* Collect queries required for indicators dynamically
* Improve testing (made possible by modularisation)
