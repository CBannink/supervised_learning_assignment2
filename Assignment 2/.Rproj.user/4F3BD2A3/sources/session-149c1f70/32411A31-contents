# Assignment 2, In this assignment we use the wine quality dataset. In this dataset we will model wine quality based on physiochemical properties. 
# In this assignment we will use the following packages
library(tidyverse)
library(rpart)
library(ggplot2)
red_wine <- read.csv("wine+quality/winequality-red.csv", sep = ";")
white_wine <- read.csv("wine+quality/winequality-white.csv", sep = ";")

str(white_wine)
box_chl
boxplt <- function(variable, yname){
  white_wine %>% 
    ggplot(aes(y = variable))+ 
    geom_boxplot(fill = "sea green")+
    facet_wrap(white_wine$quality, ncol = 7)+
    labs(ylab = yname,
         title = "Effect of alcohol % on white wine quality")+
    theme_minimal()
}
boxplt(white_wine$fixed.acidity, "Fixed acidity")

white_wine <- white_wine %>% 
  mutate(group = ifelse(quality < 5, "Bad", ifelse(quality <8, "Neutral", "Good")))
head(white_wine)
View(white_wine)