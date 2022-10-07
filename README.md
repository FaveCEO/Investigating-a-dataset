# Investigating a Dataset(TMDb Data)
## About Data
The data set is gotten from <a href="https://www.google.com/url?q=https://d17h27t6h515a5.cloudfront.net/topher/2017/October/59dd1c4c_tmdb-movies/tmdb-movies.csv&sa=D&ust=1532469042115000">The Movie Database (TMDb)</a> which has 10868 rows and 21 variables(columns) 

Certain columns, like ‘cast’ and ‘genres’, contain multiple values separated by pipe (|) characters and the final two columns ending with “_adj” show the budget and revenue of the associated movie in terms of 2010 dollars, accounting for inflation over time
 
## Analysis Process
**Must have**

* <a href="https://numpy.org/">numpy</a>
* <a href="https://pandas.pydata.org/">pandas</a>
* <a href="https://matplotlib.org/">matplotlib</a>

If you do not have any of these, you can start by downloading <a href="https://www.datacamp.com/tutorial/installing-anaconda-windows">anaconda</a> and then run the following on anaconda prompt 

* `pip install pandas`
* `pip install numpy`
* `pip install matplotlib`

Read the CSV using `pd.read_csv`('***filename***')
>Assessing data
Build intuition on the data by running codes like `df.info`, `df.shape`, `df.duplicates`, `df.isnull`

### Cleaning
Columns that were dropped are imdb_id, homepage, tagline, overview, release date, keywords and cast

Data cleaning is achieved by <a href="https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.drop_duplicates.html">dropping duplicates</a>, <a href="https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dropna.html">dropping null values</a> 

Split production companies that were joined together
# Summary of Findings
Investigation was tailored towards what genre of movie gets good vote count and how budget is affected

First off, more drama movies have been produced over the years but Sci-Fi, Action, Adventure and Fantasy had higher vote count when compared to Drama.

How long a movie runs(runtime) is not a determing factor for the cost of a movie or the love for a movie as Historic movies have the longest runtime but low vote count and low cost.
