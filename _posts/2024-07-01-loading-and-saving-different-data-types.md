---
layout: post
title: Loading and Saving Different Data Types
gh-repo: David-Manning/david-manning.github.io
gh-badge: [star, fork, follow]
tags: [data formats, json, csv, parquet, xlsx, R, python, pandas, tidyverse, data.table, data wrangling]
comments: true
---

This post is a reference for loading and saving data of various types into R and Python.

## R
Only the basic functionality is given - use `?function_name` for details on loading specific parts.

### CSV
```r
# Base R
df <- read.csv(file = "/home/david/Documents/Temp/test.csv")
write.csv(x = df, file = "/home/david/Documents/Temp/test.csv", row.names = FALSE)

# Tidyverse
library(readr) # or library(tidyverse)
df <- readr::read_csv(file = "/home/david/Documents/Temp/test.csv")
readr::write_csv(x = df, file = "/home/david/Documents/Temp/test.csv")

# data.table
library(data.table)
df <- data.table:: fread(file = "/home/david/Documents/Temp/test.csv")
data.table::fwrite(x = df, file = "/home/david/Documents/Temp/test.csv")
```

### JSON
```r
library(jsonlite)
df <- jsonlite::fromJSON(txt = "/home/david/Documents/Temp/test.json")
jsonlite::write_json(x = df, json = "/home/david/Documents/Temp/test.json")
```

### Parquet
```r
library(arrow)
df <- arrow::read_parquet(file = "/home/david/Documents/Temp/test.parquet")
arrow::write_parquet(x = df, file = "/home/david/Documents/Temp/test.parquet")
```

### Excel (xlsx)
```r
library(openxlsx)
openxlsx::read.xlsx(xlsxFile = "/home/david/Documents/Temp/test.xlsx")
openxlsx::write.xlsx(x = df, file = "/home/david/Documents/Temp/test.xlsx")
```

### Bulk Read
This loads multiple files in one directory (can include subdirectories). Any function or file type can be used as long as the first input is the file name.

```r
library(readbulk)
readbulk::read_bulk(
	directory = "/home/david/Documents/Test/",
	extension = ".csv",
	verbose = FALSE,
	fun = data.table::fread,
	data = df, # Add to an existing dataframe
	subdirectories = TRUE # FALSE to only include top level folder
	)

```

### S3
R does not have basic S3 functionality so this function needs to be used.

```r
library(aws.s3)
aws.s3::s3read_using(FUN = fread, bucket = "", object = "")
aws.s3::s3write_using(x = df, FUN = fwrite, bucket = "", object = "")
```

## Python

For files on S3, pandas works out of the box using S3 URI, which is in the format "s3://bucket_name/folder_name/file.csv" - this should be given as though it were a file name.

### CSV
```python
import pandas as pd
df = pd.read_csv("/home/david/Documents/Temp/test.csv")
df.to_csv("/home/david/Documents/Temp/test.csv", index = False)
```

### JSON
```python
import pandas as pd
df = pd.read_json("/home/david/Documents/Temp/test.json")
df.to_json("/home/david/Documents/Temp/test.json")
```

### Parquet
```python
import pandas as pd
df = pd.read_parquet("/home/david/Documents/Temp/test.parquet")
df.to_parquet("/home/david/Documents/Temp/test.parquet")
```

### Excel
```python
import pandas as pd
df = pd.read_excel("/home/david/Documents/Temp/test.xlsx")
df.to_excel("/home/david/Documents/Temp/test.xlsx", index = False)
```
