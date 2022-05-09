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

## Directed Acyclic Graph (DAG):

<img width="372" alt="Screen Shot 2022-05-09 at 3 29 45 AM" src="https://user-images.githubusercontent.com/77910160/167409718-6ffa8086-6304-494f-a138-5e35867f3ab7.png">

- C(t-1) is Consumption of electricity in the previous year
- G(t) is Generation of electricity in the current year
- E(t) is Carbon Emissions in the current year
- RP(t) is Ruling Party of current year
- S is state in the U.S

Also available to view <a href="http://dagitty.net/dags.html?id=pmuci5">here</a>

## Causal Inference:

Causal Inference of Ruling Party on Emissions shows Republican states tend to have a higher mean of carbon emissions.

![image](https://user-images.githubusercontent.com/77910160/167410365-22086453-0eb9-4c6a-bc4d-6002a6963c43.png)
![image](https://user-images.githubusercontent.com/77910160/167410456-a550e993-80d4-49d5-b94a-b006c04d3574.png)

## Predictive Modeling:

### Linear Regression with random effects(Frequentist approach)

<img width="451" alt="Screen Shot 2022-05-09 at 11 23 38 AM" src="https://user-images.githubusercontent.com/77910160/167443537-637b0359-0833-4fb3-aff2-39c0afbf6675.png">

![image](https://user-images.githubusercontent.com/77910160/167443584-f0a05a23-3254-4cd6-8819-7bb1f6840cbb.png)

### Mixed Effects Model with random effects(varying intercept) and partial pooling(Bayesian approach)

<img width="665" alt="Screen Shot 2022-05-09 at 11 26 23 AM" src="https://user-images.githubusercontent.com/77910160/167443708-dc26c0a1-74af-4682-bddf-6309e4f49743.png">

![image](https://user-images.githubusercontent.com/77910160/167443785-248d8bd6-a4c8-46df-a1ae-8caa9924b200.png) ![image](https://user-images.githubusercontent.com/77910160/167443850-ad398166-8fa6-4ed5-88d9-dfe57e4b02a3.png)

![image](https://user-images.githubusercontent.com/77910160/167444004-246636fc-1db9-4db2-89c6-01129495858d.png)

### Mixed Effects with Varying effects on Ruling Party

<img width="666" alt="Screen Shot 2022-05-09 at 11 30 20 AM" src="https://user-images.githubusercontent.com/77910160/167444502-b67599bb-aa12-4ab9-a326-f388991b67d5.png"> 

![image](https://user-images.githubusercontent.com/77910160/167444537-44578254-1b5c-4351-a59d-901ea13537c3.png)

### Additional variables to Mixed Effects with Varying effects on Ruling Party

<img width="662" alt="Screen Shot 2022-05-09 at 11 32 13 AM" src="https://user-images.githubusercontent.com/77910160/167444783-1f643bdb-601d-4fc2-b8e6-c56aa99302a2.png">

![image](https://user-images.githubusercontent.com/77910160/167444830-d14c52f7-78cd-47d1-96ae-4e1cfdc3488b.png)


Predictive Modeling notebook can be found <a href="https://github.com/nthammadi-uncc/MultiEffects_AirPollutants/blob/main/Notebooks/AP_Multi_Effects_Model_for_Air_Pollutant_Analysis.ipynb">here</a>
