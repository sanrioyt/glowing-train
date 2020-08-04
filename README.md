# glowing-train
## Repo for data science Clustering analysis of stocks

Unsupervised Learning

## Project Overview:

* The goal ofthe project is to see from a list of 52 stocks, which
stocks are similar.
* Used proprieter API to get stock information using Python
* Engineered one feature from the data that shows stock movements in
one day.
* Build K-Means Clustering model
* Also, used Dendogram from sciPy for hierchical clustering
* Used t-SNE to give us a map of the stock market

## Code and Resources Used
### python Version: 3.6
### Packages: pandas, numpy, sklearn, sciPy, matplotlib, seaborn

## Data

The data in history.csv contain historic market analysis
for a collection of 55 stocks. 
The date was from 2009/12/31 till 2013/10/29.

  * Ticker
  * Date
  * High
  * Low
  * Open
  * Close
  * Volume
  * oi: Open Interest
  * extra
  
The file stocks.csv contain the ticker and company names

## Data Cleaning

I needed to clean the data, so that was usable for the model.

* Dropped out extra column
* Checked for null value. Drop those as there were only 2 NaN.
* Merge the history dataframe with stock dataframe to get one dataframe
* Engineered a new field called movement which is the difference
between close and open
* Pivot the dataframe, leaving the ticker/company Name as indices and
dates as columns (for better readability)

## Model Building

Used k_means cluster with 10 clusters for best result. 
I tried different clusters and settled on 10 as the best one.
 
* Build a pipeline with normalizer and kmeans clustering. Used
normalizer to normalized the entire row
* Get the labels after fitting and predicting. The same label denotes
that the companies are similar. 
* Used ScipPy to do hierchical clustering
* Used t-SNE features to give us a map of the stock market.

