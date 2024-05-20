# ANA-515-WEEK-1
---
title: "Diamond sizes"
author: Pin-Chieh Huang 
date: 2024/05/20
output: word_document
---

``` {r, echo = FALSE}
#Note, Each gray box below is a code chunk. You need to insert a code chunk and put your R code in it. By setting echo = FALSE. this comment and any code will not show in my output document. If it were TRUE, the comment and code would appear. 
```

```{r setup, include = FALSE}
#The include = FALSE function hides both the code and output in my output document

#You need to install these packages first to be able to use the functions within them. You can install them from the Tools tab or write a new code chunk: install.packages("package_name"). 
#install.packages("ggplot2")
library(ggplot2)
#install.packages("dplyr")
library(dplyr)
```

```{r, include = FALSE}
#this next line is creating a subset called 'smaller' of the diamonds data
smaller <- diamonds %>% 
  filter(carat <= 1)
```

```{r, echo = FALSE}
#This next chunk is inline code. Inline code puts the text with the output of the function in my document.
```

We have data about `r nrow(diamonds)` diamonds. Only 
`r nrow(diamonds) - nrow(smaller)` are larger than
1 carat. The distribution of the remainder is shown
below:

``` {r, echo = FALSE}
#This next code chunk will make a plot in our output doc
```

```{r, echo = FALSE}
smaller %>% 
  ggplot(aes(carat)) + 
  geom_freqpoly(binwidth = 0.01)
```

```{r, echo = FALSE}
#Once all of my code has been written, I click on the Knit button in the tool bar above to produce my document.
```
