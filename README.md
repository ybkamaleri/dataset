# dataset
Datasets for testing function or analysis

**gdata.rds** consists of different data from all states in USA
**gdata.csv** is csv verion of gdata
**data.RData** has different datasets and subsets from gdata.rds

You can either download these dataset or read directly the from the GitHub raw
version of csv file in R. Raw version if this csv file looks like [gdata.csv](https://raw.githubusercontent.com/ybkamaleri/dataset/master/gdata.csv)

By using **readr** package

``` R
library("readr")
data1 <- readr::read_csv("https://raw.githubusercontent.com/ybkamaleri/dataset/master/gdata.csv")
```

Using **RCurl** package to get the URL before reading as csv

``` R
library(RCurl)
x <- getURL("https://raw.githubusercontent.com/ybkamaleri/dataset/master/gdata.csv")
y <- read.csv(text = x)
```
