# MultiEffects_AirPollutants
This project is created as part of DSBA-6010: Bayesian Statistics class. It observes the causal effects of air pollutants across US States based on electricity consumption and generation

## Goal:
The goal of this project is to find causal inference between Electricity Generation, Consumption and Ruling Government with the Carbon dioxide emissions across different states of America.
Additionally, using causal inference as a guideline, this project aims to choose the best predictive model using partial pooling and multi-effects models.

## Data:
The data of this project is taken from https://github.com/nthammadi-uncc/electricity_usage_analysis which is originally from https://www.eia.gov/electricity/data/state/

The data has been summarized and consolidated to include Electricity Energy Sources as Not Sustainable(Coal, Petroleum, Wood and Wood Derived Fuels) and Sustainable(Natural Gas, Geothermal and Other Biomass Gases)

<a href="https://www.eia.gov/electricity/data/state/#:~:text=by%20Energy%20Source1-,XLS,-2001%E2%80%93Present">Electricity Generation</a> is measured in Kilo Watt Hour and has been converted to Million Mega Watt Hour to crunch the numbers

<a href="https://www.eia.gov/electricity/data/state/#:~:text=Type%20and%20State2-,XLS,-See%20also%3A%0AElectric">Electricity Consumption</a> is measured in different units for individual Energy Source and each of these have been converted into Million Mega Watt Hour to maintain consistency and to crunch numbers.

