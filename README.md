# dataset
Data sets for testing function or analysis

- **gdata.rds** consists of different data from all states in USA
- **gdata.csv** is csv verion of gdata
- **data.RData** has different data sets and subsets from gdata.rds

You can either download these data sets directly or read the GitHub raw
version of csv file in R. Raw version of this csv file looks like [this](https://raw.githubusercontent.com/ybkamaleri/dataset/master/gdata.csv)

You have to option to read the file directly in R:

## **readr** package
`read_csv` function is used to read the raw csv file directly

``` R
library("readr")
data <- readr::read_csv("https://raw.githubusercontent.com/ybkamaleri/dataset/master/gdata.csv")
```
## RCurl package

`getURL` function is need to get the URL of the raw csv file before using the base function `read.csv`

``` R
library(RCurl)
dataURL <- getURL("https://raw.githubusercontent.com/ybkamaleri/dataset/master/gdata.csv")
data <- read.csv(text = dataURL)
```
