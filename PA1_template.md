---
title: "Reproducible Research: Peer Assessment 1"
output: 
  html_document:
    keep_md: true
---

# Reproducible Research: Peer Assessment 1



## Loading and preprocessing the data

Read the CSV data from the raw file:

```r
data <- read.csv("activity.csv")
```


## What is mean total number of steps taken per day?

Use the tapply function to get the total number of steps for each day: 

```r
StepsPerDay <- tapply(data$steps, data$date, sum)
```


Calculate the mean steps using the mean function, and setting na.rm = TRUE to exclude any "NA" values:

```r
MeanStepsPerDay <- mean(StepsPerDay, na.rm = TRUE)
```

The resulting mean is 1.0766189 &times; 10<sup>4</sup>. 


Calculate the median steps using the medain function, and setting na.rm = TRUE to exclude any "NA" values:

```r
MedianStepsPerDay <- median(StepsPerDay, na.rm = TRUE)
```

The resulting median is 10765. 
    
  
  
  

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
