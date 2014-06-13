========================================================
# **Peer Assessment 1**, *Reproducible Research*
# *Data Science Specialization* at *Coursera*
## ======================================================
## I. Load and Preprocess Data 
### 1 and 2

```r
dat <- read.csv("activity.csv", quote="", header=T)
```

```
## Warning: cannot open file 'activity.csv': No such file or directory
```

```
## Error: cannot open the connection
```

```r
names(dat)<- c("Steps_in_5_min_interval", "Measurement_Date", "Interval_minute")
```

```
## Error: object 'dat' not found
```

```r
dim(dat)
```

```
## Error: object 'dat' not found
```

```r
head(dat, n=3)
```

```
## Error: object 'dat' not found
```

```r
a <- aggregate(as.numeric(dat[,1])~dat[,2], data=dat,sum)
```

```
## Error: object 'dat' not found
```

```r
names(a) <- c("days", "steps")
```

```
## Error: object 'a' not found
```

```r
dim(a)
```

```
## Error: object 'a' not found
```

```r
head(a, n=3)
```

```
## Error: object 'a' not found
```

## ======================================================
## II. What is mean total number of steps taken per day?  

### 1. Here is a histogram of number of steps per day with breaks at 1000 days for clarity. 


```r
hist(a[,2], main = "STEPS PER DAY", breaks = seq(0,25000,1000),
     xlab = "Per 1000 days", ylab ="Number of steps",
     col="blue")
```

```
## Error: object 'a' not found
```

```r
m <- format(mean(a$steps), digits=2, nsmall=2)
```

```
## Error: object 'a' not found
```

```r
me <- format(median(a$steps), digits=2)
```

```
## Error: object 'a' not found
```














