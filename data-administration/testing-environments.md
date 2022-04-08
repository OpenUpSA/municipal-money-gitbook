# Testing environments

Municipal Money is hosted in three environments, each with a specific purpose.

## Production

Production is where the public visits. This should always represent data that is approved for publication.

* Scorecard site ([municipalmoney.gov.za](https://municipalmoney.gov.za))
* Data explorer and API ([municipaldata.treasury.gov.za](https://municipaldata.treasury.gov.za))

## Sandbox

The sandbox is where data management can be practiced or checked before updates in production, and where new data maintainers can be trained. Email the hosting company to request for the database to be reset if something goes wrong.

The software running the sandbox site should usually exactly match the software running the production site. Both should normally be upgraded at the same time.

* Scorecard site ([sandbox.municipalmoney.gov.za](https://sandbox.municipalmoney.gov.za))
* Data explorer and API ([sandbox.data.municipalmoney.gov.za](https://sandbox.data.municipalmoney.gov.za))

## Staging

The staging site is where code changes are checked with more realistic data before being deployed to sandbox and production.

* Scorecard site ([staging.municipalmoney.gov.za](https://staging.municipalmoney.gov.za))
* Data explorer and API ([staging.data.municipalmoney.gov.za](https://staging.data.municipalmoney.gov.za))
