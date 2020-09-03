## AzureResourceSchema

These settings apply only when `--azureresourceschema` is specified on the command line.

### AzureResourceSchema multi-api

``` yaml $(azureresourceschema) && $(multiapi)
# include the azure profile definitions from the standard location
require: ../../../profiles/readme.md

output-folder: $(azureresourceschema-folder)/schemas

# all the input files across all versions
input-file:
  - Microsoft.Capacity/preview/2019-07-19/quota.json
  - Microsoft.Capacity/preview/2019-04-01/reservations.json
  - Microsoft.Capacity/preview/2018-06-01/reservations.json
  - Microsoft.Capacity/stable/2017-11-01/reservations.json

```