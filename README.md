# Store Sales - Time Series Forecasting
## Aim of the project
<p>This project is for a Kaggle competition: https://www.kaggle.com/competitions/store-sales-time-series-forecasting </p>
<p>The purpose of this project is to use time-series forecasting with Python to forecast store sales on data from a large grocery retailer in Ecuador. Specifically, I will build a model that accurately predicts the unit sales for thousands of items sold at different stores. This is important because the data could help the store ensure they are adequately stocked with appropriate numbers of items for their customers. </p>

### Model evaluation
<p>I will evaluate different time-series models using the Root Mean Squared Logarithmic Error (RMSLE).</p>
<p>The best model will predict "sales" with the lowest RMSLE.</p>

### Output file
<p>For each "id" in the test set, I will use the best model to predict "sales".  The output file should contain a header and have the following format: <p>
id,sales<br>
3000888,0.0<br>
3000889,0.0<br>
3000890,0.0<br>
3000891,0.0<br>
3000892,0.0<br>
Etc.

## How to get started with this project:
<p>This repository contains an ipynb file containing the analytical code in Python, the data files (.csv) used in the analysis, a data description file (.txt), and a license file (.txt).</p>
<p>There are several data files available:</p>
<ul>
<li>train.csv - the training data contains a time series of features: "date", "store_nbr" (identifies the store at which the products are sold), "family" (identifies the type of product sold), "onpromotion" (the total number of items in a product family that were being promoted at a store at a given date), and target "sales" (the total sales for a product family at a particular store at a given date). </li>
<li>test.csv - The test data has the same features as the training data. I want to predict the target "sales" for the dates in this file. The dates in the test data are for the 15 days after the last date in the training data.</li>
<li>stores.csv - metadata for each "store_nbr", including "city", "state", "type", and "cluster" (cluster is a grouping of similar stores).</li>
<li>oil.csv - includes daily oil price values ("dcoilwtico") on each "date" during both the train and test data timeframes. (Ecuador is an oil-dependent country whose economic health is highly vulnerable to shocks in oil prices.)</li>
<li>holidays_events.csv - metadata for important dates ("date"), including "type", "locale", "locale_name", "description, and "transferred". NOTE: the "transferred" column indicates that a holiday that officially falls on that calendar day but was moved to another date by the government. The "date" that the holiday was actually celebrated is indicated when "type" = Transfer. When "type" = Bridge this means that extra days that are added to a holiday (e.g., to extend the break across a long weekend). When "type" = Additional this means that holidays are days added to a regular calendar holiday.</li>
<li>transactions.csv - contains "date", "store_nbr", and "transactions" (the number of transactions on that date).</li>
</ul>
<p>Other important aspects related to the data:</p>
<ul>
<li>Wages in the public sector are paid every two weeks on the 15 th and the last day of the month. </li>
<li>A magnitude 7.8 earthquake struck Ecuador on April 16, 2016. People rallied in relief efforts donating water and other first-need products which greatly affected supermarket sales for several weeks after the earthquake.</li>
</ul>

## Further info:
<p>This project is maintained by Thomas Solomon.</p>
