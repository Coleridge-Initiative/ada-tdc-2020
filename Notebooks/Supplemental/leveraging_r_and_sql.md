# Introduction to R and SQL

This document provides an introduction for how we will use leverage the powers of R and SQL together to perform data analyses in this course. By no means should you feel it necessary to memorize this information -- it is meant to provide some background information on how we will use the two languages together to make meaningful conclusions.

## SQL and R Together

As you will see, we will use SQL to often pull in a subset of the data stored in these tables inside our relational database and then further manipulate and visualize the data in R. R provides many ways to load data. It allows users to read data from a local csv or excel file, read directly from a URL (when you have internet access), or pull data from a relational database, which in this case will allow us to directly pull data from our relational database using SQL to load the data into R.

## R Packages

Packages are collections of functions - packets of code created by others - geared toward a specific set of tasks. For example, the `scales` package contains functions for scaling data, as well as those to override default graphing settings. There are hundreds of packages for a range of tasks, from common tasks to highly domain-specific operations. Some packages can even be bundles of other packages - for example `tidyverse` contains `dplyr`, `ggplot`, and others.

For this course, we will primarily use `base` functions (those included when you download R) as well as those from the `tidyverse`, which is a suite of packages that can be used to tackle many of the facets of a data analysis. As you will see, since we cannot use functions from the `tidyverse` suite of packages as soon as we load a new R kernel, and thus not part of `base` R, we will need to load them in using the `library()` function. 

In many analyses in R, you will need to load packages outside of `base` R, and it is commonplace to load all the packages in as your first step in any analysis. We will follow the same practice in the notebooks, as we will rely on a combination of `base` functions and those from additional packages to guide our analysis. 

You will also work with the `DBI` and `RPostgreSQL` packages in this class, which will allow you to interact with the database using SQL queries to pull data into R. For example, a function you will be using to run a SQL query and pull the data into a classic R data frame is `dbGetQuery()`, which is from the `DBI` package. Just like running a SQL query from DBeaver, this function will ask for some information about the database and the query you would like to run, as you will see in the notebooks.