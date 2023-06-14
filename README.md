# Post-release Mortality Analysis of Coho Salmon (Machine Learning)

## Introduction

In recreational fisheries, a significant proportion of fish are released following capture, known as catch-andrelease fishing. This statistical project aims to identify the factors that influence fish survival after a catch-and-release event and make some suggestions on fishing to minimize the mortality rate following the release.

We adressed the following two statistical questions:
1. Assess logistic regression models, as well as alternative models and model selection approaches
2. Determine if condensing some measurements into scores is the optimal strategy

## Setup

Requires **R** and **RStudio**. Required libraries:
```
knitr::opts_chunk$set(echo = TRUE)
knitr::opts_chunk$set(error = TRUE)
library(tidyverse)
library(readxl)
library(ggplot2)
library(Amelia)
library(caret)
library(corrplot)
library(glmnet)
```

## Main Project

Run the R Markdown file **4-salmon-mortality.Rmd**, which includes the code and detailed step-by-step instructions and explanations.

### Some plots and tables you might get if the project works properly:

![Alt text](/plots_and_tables/year.png "Figure 1. Frequency of each response variable level for each year")
![Alt text](/plots_and_tables/eyeinjury.png "Figure 2. Frequency of each response variable level for whether the fish has eye injury")
![Alt text](/plots_and_tables/scaleloss.png "Figure 3. Frequency of each response variable level for different scale loss extent")
![Alt text](/plots_and_tables/airexposure.png "Figure 4. Parallel box plots for detection status versus air exposure time")

![Alt text](/plots_and_tables/table1.png "Table 1. Summary of Some Representative Models Trained")
![Alt text](/plots_and_tables/table2.png "Table 2. Interpretations of Representative Models stated before")

### Some conclusions

1. The results suggest that eye injury, hook location, fin damage, and reflex score (or orientation reflex in detail) are likely to be the key factors.
2. Logistic regression is appropriate to identify the significant factors and outperforms other models.
3. Using model selection approaches such as AIC alone is unsuitable and probably dangerous. We suggest applying k-fold cross-validation.
4. Condensing several measurements into scores (injury score and reflex score) might not be helpful in this study.

## Acknowledgement

1. Collaborated with three groupmates: Xiaotong(Olivia) Liu, Andy Lin and Weihao Qiu.
2. Our client, Emma Cooke, for giving us this opportunity to work with real data in a professional environment.
3. Our supervisors, Melissa Lee, Nancy Heckman and Estella Qi, for helping and guiding us through this project.
