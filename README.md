---
title: "Survey Weights with School Dataset"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
Just get rid of missing values first, then try to find a function that has only @ in its maybe need to use SQL.
```{r}
library(data.table)
setwd("~/Google Drive/CSCY/SWAGGER")
cscyMain = read.csv("CommunityResources.csv", header = TRUE, na.strings = c("")); head(cscy)
cscy = cscyMain
head(cscy)
sum(is.na(cscy))
cscy = as.data.frame(na.omit(cscy)); head(cscy)
cscy = data.table(cscy)
cscy = as.data.frame(cscy[like(email, "@")])
write.csv(cscy, "cscy.csv", row.names = FALSE)
cscyEmail = as.character(cscy$email)
strsplit(cscyEmail, " ")
df <- data.frame(x = c(NA, "a.b", "a.d", "b.c")); df
df %>% separate(x, c("A", "B"))

df <- data.frame(x = c("a", "a b", "a b c", NA)); df
df %>% separate(x, c("a", "b"))

4806.60+400.55*3+14000+1200
```

