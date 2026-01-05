[![hacs_badge](https://img.shields.io/badge/HACS-Default-41BDF5.svg)](https://github.com/hacs/integration)
[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://github.com/hacs/integration)

![ExRates Logo](images/logo-exrates.png)

# HomeAssistant Exchange Rates
Currency Exchange Rates integration

Features:
- [x]  displaying configurable list of currency pairs based on ECB daily rates (e.g. EUR/CZK, EUR/USD, EUR/JPY, ...)
- [x]  calculation and displaying of currency pairs not directly avaiable in ECB rates (e.g. CZK/USD, CHF/NOK, PLN/AUD, ...)

Limitations:
- [x]  works only for currencies available in daily updated ECB reference rates XML file https://www.ecb.europa.eu/stats/eurofxref/eurofxref-daily.xml

### Installation
Manually add this repository to HACS as custom repository using the "three-dots-menu" at the top right in HACS

### Configuration
Configure the sensor(s) in ``configuration.yaml``. 
```
sensor
  - platform: exchange_rates
    currency_pairs:
      - USD/CZK
      - CZK/USD
      - EUR/CZK
      - CZK/EUR
      - EUR/USD
      - USD/EUR
     
    update_interval: 6  # (optional) data refresh every 6 hours, but ECB publish data only every 24 hours during working days
    precision: 4        # (optional) number of decimal places
```
