---
title: "machine_learning"
author: "Amit Sanghi"
date: "Sunday, May 24, 2015"
output: html_document
---

The goal of your project is to predict the manner in which they did the exercise. This is the "classe" variable in the training set. You may use any of the other variables to predict with. You should create a report describing how you
built your model, how you used cross validation, what you think the expected out of sample error is, and why you
made the choices you did. You will also use your prediction model to predict 20 different test cases.


```r
library(caret)
library(kernlab)
library(C50)
training<-read.table.url("https://d396qusza40orc.cloudfront.net/predmachlearn/pmltraining.csv",skip=4,header=T)
```

```
## Error in eval(expr, envir, enclos): could not find function "read.table.url"
```

```r
testing<-read.table.url("https://d396qusza40orc.cloudfront.net/predmachlearn/pmltesting.csv",skip=4,header=T)
```

```
## Error in eval(expr, envir, enclos): could not find function "read.table.url"
```
Cleaning the training and testing data set


```
##  [1] "roll_belt"               "pitch_belt"             
##  [3] "yaw_belt"                "total_accel_belt"       
##  [5] "kurtosis_roll_belt"      "kurtosis_picth_belt"    
##  [7] "kurtosis_yaw_belt"       "skewness_roll_belt"     
##  [9] "skewness_roll_belt.1"    "skewness_yaw_belt"      
## [11] "max_yaw_belt"            "min_yaw_belt"           
## [13] "amplitude_yaw_belt"      "gyros_belt_x"           
## [15] "gyros_belt_y"            "gyros_belt_z"           
## [17] "accel_belt_x"            "accel_belt_y"           
## [19] "accel_belt_z"            "magnet_belt_x"          
## [21] "magnet_belt_y"           "magnet_belt_z"          
## [23] "roll_arm"                "pitch_arm"              
## [25] "yaw_arm"                 "total_accel_arm"        
## [27] "gyros_arm_x"             "gyros_arm_y"            
## [29] "gyros_arm_z"             "accel_arm_x"            
## [31] "accel_arm_y"             "accel_arm_z"            
## [33] "magnet_arm_x"            "magnet_arm_y"           
## [35] "magnet_arm_z"            "kurtosis_roll_arm"      
## [37] "kurtosis_picth_arm"      "kurtosis_yaw_arm"       
## [39] "skewness_roll_arm"       "skewness_pitch_arm"     
## [41] "skewness_yaw_arm"        "roll_dumbbell"          
## [43] "pitch_dumbbell"          "yaw_dumbbell"           
## [45] "kurtosis_roll_dumbbell"  "kurtosis_picth_dumbbell"
## [47] "kurtosis_yaw_dumbbell"   "skewness_roll_dumbbell" 
## [49] "skewness_pitch_dumbbell" "skewness_yaw_dumbbell"  
## [51] "max_yaw_dumbbell"        "min_yaw_dumbbell"       
## [53] "amplitude_yaw_dumbbell"  "total_accel_dumbbell"   
## [55] "gyros_dumbbell_x"        "gyros_dumbbell_y"       
## [57] "gyros_dumbbell_z"        "accel_dumbbell_x"       
## [59] "accel_dumbbell_y"        "accel_dumbbell_z"       
## [61] "magnet_dumbbell_x"       "magnet_dumbbell_y"      
## [63] "magnet_dumbbell_z"       "roll_forearm"           
## [65] "pitch_forearm"           "yaw_forearm"            
## [67] "kurtosis_roll_forearm"   "kurtosis_picth_forearm" 
## [69] "kurtosis_yaw_forearm"    "skewness_roll_forearm"  
## [71] "skewness_pitch_forearm"  "skewness_yaw_forearm"   
## [73] "max_yaw_forearm"         "min_yaw_forearm"        
## [75] "amplitude_yaw_forearm"   "total_accel_forearm"    
## [77] "gyros_forearm_x"         "gyros_forearm_y"        
## [79] "gyros_forearm_z"         "accel_forearm_x"        
## [81] "accel_forearm_y"         "accel_forearm_z"        
## [83] "magnet_forearm_x"        "magnet_forearm_y"       
## [85] "magnet_forearm_z"        "classe"
```

Training the model for prediction.


```
## Warning in train.formula(classe ~ ., data = training, method = "glm"):
## Reached total allocation of 2047Mb: see help(memory.size)
```

```
## Warning in train.formula(classe ~ ., data = training, method = "glm"):
## Reached total allocation of 2047Mb: see help(memory.size)
```

```
## Warning in train.formula(classe ~ ., data = training, method = "glm"):
## Reached total allocation of 2047Mb: see help(memory.size)
```

```
## Warning in train.formula(classe ~ ., data = training, method = "glm"):
## Reached total allocation of 2047Mb: see help(memory.size)
```

```
## Error: cannot allocate vector of size 1.0 Gb
```

```
## Error in eval(expr, envir, enclos): object 'modelfit' not found
```

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.


Predict the results using predict

```
## Error in predict(modelfit, newdata = testing): error in evaluating the argument 'object' in selecting a method for function 'predict': Error: object 'modelfit' not found
```

```
## Error in eval(expr, envir, enclos): object 'predictions' not found
```


```
## Warning in train.formula(classe ~ ., data = training, method = "glm"): Reached total allocation of 2047Mb: see
## help(memory.size)
```

```
## Warning in train.formula(classe ~ ., data = training, method = "glm"): Reached total allocation of 2047Mb: see
## help(memory.size)
```

```
## Warning in train.formula(classe ~ ., data = training, method = "glm"): Reached total allocation of 2047Mb: see
## help(memory.size)
```

```
## Warning in train.formula(classe ~ ., data = training, method = "glm"): Reached total allocation of 2047Mb: see
## help(memory.size)
```

```
## Error: cannot allocate vector of size 1.0 Gb
```

```
## Error in predict(modelfir_folds, newdata = testing): error in evaluating the argument 'object' in selecting a method for function 'predict': Error: object 'modelfir_folds' not found
```
