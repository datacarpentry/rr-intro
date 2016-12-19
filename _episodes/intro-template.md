---
title: 'Intro Session: Motivating reproducibility'
output:
  html_document:
    fig_height: 3
    fig_width: 6
---

This RMarkdown file contains R code you can use to complete the exercises from the Intro
session. To see the output simply click on *Knit HTML* above. This might prompt you to 
install and load some required packages, specifically `knitr`. Just click yes, and the a 
document including this narrative, the R code, and figures should pop up.

## Data:

The `read.csv` function is used to read the data into R. Note that the argument provided 
for this function is the complete path that leads to the dataset from your current 
working directory (where this RMarkdown file is located). Also note that this is provided 
as a character string, hence in quotation marks.


```r
gap_5060 <- read.csv("data/gapminder-5060.csv")
```

```
## Warning in file(file, "rt"): cannot open file 'data/gapminder-5060.csv': No
## such file or directory
```

```
## Error in file(file, "rt"): cannot open the connection
```

## Packages:

We will use the `ggplot2` and `dplyr` packages to make the plots for these exercises. 

- `ggplot2` for plotting: This is not the only way to make this plot, but this package 
has some aesthetic defaults that makes it attractive. Find out more about the package
at http://ggplot2.org/.
- `dplyr` for data wrangling: This is not the only way manipulate data in R, but this
package uses piping and a simple set of verbs for most common data wranling tasks which
makes it attractive. See the package vignette at https://cran.rstudio.com/web/packages/dplyr/vignettes/introduction.html.

At this point you should have installed these packages using `install.packages()`.

Now we need to explicitly load the packages:


```r
library("ggplot2")
library("dplyr")
```

#### Task 1: Visualize life expectancy over time for Canada in the 1950s and 1960s using a line plot.

1. Filter the data for Canada only:

```r
gap_5060_CA <- gap_5060 %>%
  filter(country == "Canada")
```

```
## Error in eval(expr, envir, enclos): object 'gap_5060' not found
```

2. Visaualize:

```r
ggplot(data = gap_5060_CA, aes(x = year, y = lifeExp)) +
  geom_line()
```

```
## Error in ggplot(data = gap_5060_CA, aes(x = year, y = lifeExp)): object 'gap_5060_CA' not found
```

#### Task 2: Something is clearly wrong with this plot! Turns out there's a data error in the data file: life expectancy for Canada in the year 1957 is coded as `999999`, it should actually be `69.96`. Make this correction.

- `mutate` for creating a new variables
- `replace` for replacing a data entry in a specific
location as determined by the logical statement `(country == "Canada" & year == 1957)`

```r
gap_5060 <- gap_5060 %>%
  mutate(lifeExp = replace(lifeExp, (country == "Canada" & year == 1957), 69.96)) %>%
  as.data.frame()
```

```
## Error in eval(expr, envir, enclos): object 'gap_5060' not found
```

#### Task 3: Visualize life expectancy over time for Canada again, with the corrected data.

Exact same code as before, but note that the contents of `gap_5060` are different as it 
has been updated in the previous task.

```r
gap_5060_CA <- gap_5060 %>%
  filter(country == "Canada")
```

```
## Error in eval(expr, envir, enclos): object 'gap_5060' not found
```

```r
ggplot(data = gap_5060_CA, aes(x = year, y = lifeExp)) +
  geom_line()
```

```
## Error in ggplot(data = gap_5060_CA, aes(x = year, y = lifeExp)): object 'gap_5060_CA' not found
```

#### Task 3 - Stretch goal: Add lines for Mexico and United States.

- `%in%` for logical operator testing if a country's name is in the list provided
- Same visualization code as before, only difference is the input dataset

```r
gap_5060_NA <- gap_5060 %>%
  filter(country %in% c("Canada", "Mexico", "United States"))
```

```
## Error in eval(expr, envir, enclos): object 'gap_5060' not found
```

```r
ggplot(data = gap_5060_NA, aes(x = year, y = lifeExp, color = country)) +
  geom_line()
```

```
## Error in ggplot(data = gap_5060_NA, aes(x = year, y = lifeExp, color = country)): object 'gap_5060_NA' not found
```

#### Extending your analysis with new data:

Load the new data:

```r
gap_7080 <- read.csv("data/gapminder-7080.csv")
```

```
## Warning in file(file, "rt"): cannot open file 'data/gapminder-7080.csv': No
## such file or directory
```

```
## Error in file(file, "rt"): cannot open the connection
```

```r
gap_90plus <- read.csv("data/gapminder-90plus.csv")
```

```
## Warning in file(file, "rt"): cannot open file 'data/gapminder-90plus.csv':
## No such file or directory
```

```
## Error in file(file, "rt"): cannot open the connection
```

Cobine data frames with `rbind` (**r**ow bind):

```r
gap <- rbind(gap_5060, gap_7080, gap_90plus)
```

```
## Error in rbind(gap_5060, gap_7080, gap_90plus): object 'gap_5060' not found
```

Make the same plots, with the same code, just changing the input data frame:

1. Canada only:

```r
gap_ca <- gap %>%
  filter(country == "Canada")
```

```
## Error in eval(expr, envir, enclos): object 'gap' not found
```

```r
ggplot(data = gap_ca, aes(x = year, y = lifeExp)) +
  geom_line()
```

```
## Error in ggplot(data = gap_ca, aes(x = year, y = lifeExp)): object 'gap_ca' not found
```

2. North America:

```r
gap_NA <- gap %>%
  filter(country %in% c("Canada", "Mexico", "United States"))
```

```
## Error in eval(expr, envir, enclos): object 'gap' not found
```

```r
ggplot(data = gap_NA, aes(x = year, y = lifeExp, color = country)) +
  geom_line()
```

```
## Error in ggplot(data = gap_NA, aes(x = year, y = lifeExp, color = country)): object 'gap_NA' not found
```
