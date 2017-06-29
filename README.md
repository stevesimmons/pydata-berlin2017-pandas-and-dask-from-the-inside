# Pandas and Dask from the Inside

Tutorial session from PyData Berlin, Friday 30 June 2017.  
Presented by Stephen Simmons  
(mail@stevesimmons.com, stephen.e.simmons@jpmorgan.com)    
GitHub repo: <https://github.com/stevesimmons/pydata-berlin2017-pandas-and-dask-from-the-inside>


## Tutorial contents

This is meant for all levels of Python/Pandas users:
accessible to beginners plus some new insights for experienced users.

#### Part I - Pandas from the Inside

Learn how to make your Python data analysis easier, faster and more efficent 
with Pandas, while avoiding common pitfalls.

We follow a typical Python data analysis task from start to finish,
looking inside Pandas Series, DataFrames and other objects to discover
what really happens.

We will see that many Pandas operations are essentially function calls on numpy arrays. 
Our Pandas code, if we do it right, can benefit from the full speed of numpy's 
highly optimized C routines. Equally, if we do it wrong, our Pandas code
can be 1000x slower.

The examples here Australian Rules football results.
If you aren't familiar with Aussie Rules, watch this 9 minute
[introduction](https://youtu.be/zxhqXzVBen4).

    
#### Part II - Dask from the Inside - "Big Pandas" 

This second part looks at Pandas analysis when our data sets can't fit in local memory. 
The examples here use the _On-Time_ domestic flight arrival/departure data 
from the US Bureau of Transportation Statistics. The monthly
[BTS On-Time Performance](https://www.transtats.bts.gov/TableInfo.asp?Table_ID=236&DB_Short_Name=On-Time&Info_Only=0) 
dataset started in December 1987 and currently has details on
173 million individual flights. Each monthly extract is 
a 220MB csv file, zipped to 23MB, covering the 450,000 or so 
flights by major US carriers.

We try two approaches to process this csv data:
* Plain Pandas, which quickly runs out of memory.
* Dask, whose distributed/deferred DataFrames are a near drop-in replacement for Pandas.

Through seeing how Dask works "from the inside", we can make better architectural
decisions on local versus distributed data processing.


## Before the tutorial

#### Python packages

If you want to follow along the examples on your own laptop, please 
have the latest versions of Python3, Pandas, Jupyter and IPython installed.
Part II will need Dask and optionally graphviz to visualize Dask dependency graphs.

If you don't have Python already, the easiest route is via the full Anaconda 
Python distribution (300MB). Details are at <http://conda.pydata.org/docs/installation.html>. 
Alternatively download the "miniconda" version and install just the packages you need.


#### Tutorial files

Clone this repo for a local copy of the presentation materials, source code, 
sample Jupyter notebooks and test data. 

If you just want to follow along the tutorial slides, download just the PDFs.

Please update your local copies on the morning of the tutorial to make 
sure your version matches the final ones I am presenting. 

The main files for Part I are:

* `slides-1-pandas-from-the-inside.pdf` or `slides-1-pandas-from-the-inside.pdf`- Presentation slides. 
As some slides are quite detailed, you may want to download these to 
follow along on your own laptop/tablet.

* `pandas-from-the-inside.ipynb` - Jupyter notebook 
with code from the slides plus some further explanation. 
Download this if you have Jupyter installed on your laptop. 
Otherwise you can view the rendered notebook here on GitHub.

* `pfi.py` - Code in the Jupyter notebook.

* `bg3.txt` - Sample data file from http://afltables.com/afl/stats/biglists/bg3.txt. 
A copy is included in this repo for your convenience.

The main files for Part II are:

* `slides-2-dask-big-pandas.pdf` or `slides-2-dask-big-pandas.pdf`- 
* `nb1-setup.ipynb`
* `nb2-preparing-sample-data.ipynb`
* `nb3-pandas-with-large-csvs.ipynb`
* `nb4-parquet.ipynb`
* `nb5-dask-graphs.ipynb`

Prepared sample data is available here:
* http://www.stevesimmons.com/pydata-ams2017/flights-201601-201701-csv-xz.tar (151MB)
* http://www.stevesimmons.com/pydata-ams2017/flights-201601-201701-parq.tar (158MB)



## About the presenter

Stephen Simmons has been programming in Python since 2000. 
For the last 6 years, he has been a front-office developer at JPMorgan in London, 
where he leads the Precious Metals technology team, building 
trading and risk applications in JPMorgan's Python environment, Athena. 
He is about to move to the bank's Equities division, 
to lead a new Data and Analytics Engineering team.

