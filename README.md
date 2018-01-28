# Data sets
Data sets for testing functions or analysis

- **gdata.rds** consists of different data from all states in USA
- **gdata.csv** is csv verion of gdata
- **data.RData** has different data sets and subsets from gdata.rds

You can either download these data sets directly or read the GitHub raw
version of csv file in R. Raw version of this csv file looks like [this](https://raw.githubusercontent.com/ybkamaleri/dataset/master/gdata.csv)

You have different options to read the file directly in R:

## data.table package
`fread` function is needed to read the csv file in R. This is my personal preference and often faster :-)

``` R
library("data.table")
data2 <- fread("https://raw.githubusercontent.com/ybkamaleri/dataset/master/gdata.csv")
```

## readr package
`read_csv` function is used to read the raw csv file directly

``` R
library("readr")
data <- readr::read_csv("https://raw.githubusercontent.com/ybkamaleri/dataset/master/gdata.csv")
```
## RCurl package

`getURL` function is needed to get the URL of the raw csv file before using the base function `read.csv`

``` R
library(RCurl)
dataURL <- getURL("https://raw.githubusercontent.com/ybkamaleri/dataset/master/gdata.csv")
data <- read.csv(text = dataURL)
```
