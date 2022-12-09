---
title: "CA3_DAIE"
author: "Conor Crean & Peter Leary"
date: "`r Sys.Date()`"
output: html_document
---

#Descriptive Statistics

```{r}

library(readr)
daie_ca3_data_10 <- read_csv("daie_ca3_data_10.csv")
#View(daie_ca3_data_10)

head(daie_ca3_data_10,10)

summary(daie_ca3_data_10)

tail(daie_ca3_data_10,5)

static_data<-c(6.1434,5.4312,6.161,5.4158)
CPSSOR<-c("Pre Trial CPSS","Post Trial CPSS","Pre Trial OR","Post Trial OR")

barplot(static_data,xlab="Static VR Group",ylab="Trial Scores Mean", main="Static Group - Pre and Post Trial CPSS and OR Scores", names.arg=CPSSOR, col="Orange", border="Blue", ylim=c(0,10))


animated_data<-c(6.1636,5.8508,6.1956,5.8608)
CPSSOR<-c("Pre Trial CPSS","Post Trial CPSS","Pre Trial OR","Post Trial OR")

barplot(animated_data,xlab="Animated VR Group",ylab="Trial Scores Mean", main="Animated Group - Pre and Post Trial CPSS and OR Scores", names.arg=CPSSOR, col="Red", border="Blue", ylim=c(0,10))


control_data<-c(6.1592,5.173,6.1666,5.3524)
CPSSOR<-c("Pre Trial CPSS","Post Trial CPSS","Pre Trial OR","Post Trial OR")

barplot(control_data,xlab="Control Group",ylab="Trial Scores Mean", main="Control Group - Pre and Post Trial CPSS and OR Scores", names.arg=CPSSOR, col="Green", border="Blue", ylim=c(0,10))

```
#Inferenial Statistics

##Histograms

```{r}



hist(daie_ca3_data_10$pre_trial_cpss,
main = "Pre Trial CPSS",
xlab = "Score",
ylab = "Frequency",
breaks = 8)


hist(daie_ca3_data_10$post_trial_cpss,
main = "Post Trial CPSS",
xlab = "Score",
ylab = "Frequency",
breaks = 8)


hist(daie_ca3_data_10$pre_trial_or,
main = "Pre Trial OR",
xlab = "Score",
ylab = "Frequency",
breaks = 8)


hist(daie_ca3_data_10$post_trial_or,
main = "Post Trial OR",
xlab = "Score",
ylab = "Frequency",
breaks = 8)



```

## QQ Plots

```{r QQ Plot - daie_ca3_data_10 }

qqnorm(daie_ca3_data_10$pre_trial_cpss,
       pch = 2, frame = FALSE)

qqline(daie_ca3_data_10$pre_trial_cpss,
       col = "darkorchid", lwd = 1)



qqnorm(daie_ca3_data_10$post_trial_cpss,
       pch = 2, frame = FALSE)

qqline(daie_ca3_data_10$post_trial_cpss,
       col = "darkorchid", lwd = 1)




qqnorm(daie_ca3_data_10$pre_trial_or,
       pch = 2, frame = FALSE)

qqline(daie_ca3_data_10$pre_trial_or,
       col = "darkorchid", lwd = 1)



qqnorm(daie_ca3_data_10$post_trial_or,
       pch = 2, frame = FALSE)

qqline(daie_ca3_data_10$post_trial_or,
       col = "darkorchid", lwd = 1)



```


