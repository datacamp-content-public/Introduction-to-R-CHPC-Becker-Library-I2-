---
title: Chapter 1 Manipulating Data
description: >-
  Introduce R objects and classes, provide an overview of some popular data structures (vectors, matrices, and data frames), and touch on basic ways to manipulate data


---
## Ex 1.1

```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: d1416bace7
```

This exercise will help you get familiar with using R as a calculator by using basic arithmetic operators, assigning names to objects, and calculating the area of a triangle.

Feel free to experiment with your own calculations as well.

R has a variety of arithmetic operators such as addition "+", multiplication "*",  division "/", exponentiation "^", and more.

Additional information on arithmetic operators in R is available using the help() function  by putting any of the arithmetic operators in quotes.

Check out the help documentation using the sample code below.

`help("*")`

`@instructions`
##### 1. Basic Arithmetic operations

Add 8 and 4 and print out the result.

Multiply 7 by 9 and print out the result.

Raise 6 to the power of 4 and print out the result.

Divide 12 by 6 and print out the result.

##### 2. Calculate the area of a triangle

The area of a triangle = base * height / 2.

Assign the value of 2.48 to the object base and print it out.

Assign the value of 3 to the object height and print it out.

Calculate the area of the triangle, assigning the value to an object named area, and print out area.

`@hint`
To raise "x" to the power of "y", you need to use "x^y".


`@sample_code`
```{r}
### Add 8 and 4 and print out the result.


### Multiply 7 by 9 and print out the result.


### Raise 6 to the power of 4 and print out the result.


### Divide 12 by 6 and print out the result.


### Assign the value of 2.48 to the object base and print it out.


### Assign the value of 3 to the object height and print it out.


### Calculate the area of the triangle, assigning the value to an object named area, and print out area.
```
`@solution`
```{r}
8 + 4
7 * 9
6 ^ 4
12 / 6
base <- 2.48
base
height <- 3
height
area <- base * height / 2
area
```






---
## Ex 1.2

```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 6c8bd21914
```

This exercise will help you get familiar with basic R data types and ways to store variables in R. 

This includes vectors, matrices, and data frames.

`@instructions`
##### 1. Vectors

Create a numeric vector with the values in parentheses (74, 70, 63, 69, 67, 71, 64, 66, 71, 68) and assign it to the object Height.

When finished, print out Height.

Next, create a character vector with the values in parentheses (A, B, C, D, E, F, G, H, I, J) and assign it to an object named ID.

When finished, print out ID.

Use the length() function to find the number of members in each of the vectors above.

##### 2. Data frames

Use the data.frame() function to generate a data frame with the vectors, ID and Height, that you created above.

Name the data frame ClientInforData.

##### 3. Matrices

In this exercise, you will use the matrix() function to create 2 matrices, each with 2 rows (nrow = 2) and 3 columns (ncol = 3),
using the vector c(2, 4, 6, 8, 1, 3).

Fill Matrix1 by rows and fill Matrix2 by columns.

Print out Matrix1 and Matrix2 when finished.

`@hint`
When creating character vectors, you should put double quotes around the letter or strings treated as characters. 

When fill matrices by rows, you need to use "byrow = TRUE".


`@sample_code`
```{r}
### Create a numeric vector Height, and print it out.


### Create a character vector ID, and print it out.


### Use the length() function to find the number of members in each of the vectors above.


### Create a data frame with the vectors, ID and Height, created above and name it ClientInfoData.


### Create Matrix1 by rows and Matrix2 by columns.



### Print out Matrix1 and Matrix2.
```
`@solution`
```{r}
Height <- c(74, 70, 63, 69, 67, 71, 64, 66, 71, 68)
Height

ID <- c("A", "B", "C", "D", "E", "F", "G", "H", "I", "J")
ID

length(Height)
length(ID)

ClientInfoData <- data.frame(ID, Height)

Matrix1 <- matrix(c(2, 4, 6, 8, 1, 3), nrow = 2, ncol = 3, byrow = TRUE)
Matrix2 <- matrix(c(2, 4, 6, 8, 1, 3), nrow = 2, ncol = 3)

Matrix1
Matrix2
```






---
## Ex 1.3

```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: fa22992604
```

This exercise will use R to explore tabular data in data frames. This includes getting 
data into R and looking at an overview of what the data looks like.  You will use the 
tabular data example from the workshop slide presentation (study\_data.csv) for this 
activity.

Before you can read study_data.csv into R, you need to figure out where R is going to 
look for data on your computer by default. Run getwd() to determine this default location. 
Once you determine where R is going to be looking for the data, make sure you put the 
study\_data.csv file in that location.

In this activity, we preload study\_data.csv in the current repository, and you can simply
run the read.csv() function.

`@instructions`
##### 1. Load data from study_data.csv

When running the read.csv() function from the slides, you're reading in the study\_data.csv file
and creating a data frame named study\_data.

Print out study\_data.

##### 2. Functions

In the lecture we used the str() function to look at the structure of study\_data.
We also used the head() and tail() functions to look at the first and last several rows of study\_data.
In this exercise, you will use additional functions that will help give an overview of study\_data.

First, use the help() function to read more about the head() and tail() functions.

Then generate and run code that will return the first 10 lines of study\_data, the last 8 lines of study\_data,
all of study\_data except the first 8 lines, and all of study\_data except the last 8 lines.

Next, run the nrow() and ncol() functions to get the number of rows and columns in study\_data.

Lastly, run the summary() function to get a variety of summary statistics for study\_data.

The class of study\_data is data.frame, but note that the variables in study\_data also have classes.
To determine the class of each of the variables, you can use the class() function and the $ operator.
The syntax is class(study\_data$column\_name), where you'll replace column_name
with the specific column name that you're interested in.
Run the class() function on each of the columns in study\_data and see what comes out

`@sample_code`
```{r}
### Print the default location that R looks for input files.
getwd()

### Using read.csv() function to load data from study_data.csv and create a data frame named study_data, and print it out.
study_data <- read.csv(url("https://assets.datacamp.com/production/course_7304/datasets/study_data.csv"))


### Use help() function to read more about the head() and tail() functions.



### Return the first 10 lines of study_data.


### Return the last 8 lines of study_data.


### Return all of study_data except the first 8 lines.


### Return all of study_data except the last 8 lines.


### Run the nrow() and ncol() functions to get the number of rows and columns in study_data.


### Run the summary() function to get a variety of summary statistics for study_data.



```
`@solution`
```{r}
study_data <- read.csv(url("https://assets.datacamp.com/production/course_7304/datasets/study_data.csv"))
study_data
help(head)
help(tail)
head(study_data, n = 10L)
tail(study_data, n = 8L)
tail(study_data, n = -8L)
head(study_data, n = -8L)
nrow(study_data)
ncol(study_data)
summary(study_data)
class(study_data$ID)
class(study_data$Height)
class(study_data$Weight)
class(study_data$BMI)
class(study_data$Exercise)
class(study_data$Diet)
```





---
## Ex 1.4

```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: d274139165
```

Sometimes, it may be useful to run test analyses on a small portion of your data before analyzing the whole dataset.

In this exercise, you will practice subsetting data frames in R, making use of the study_data data frame.


`@instructions`
Using subsetting, select the third element in column 3 in study\_data.

Using subsetting, select all of the elements in column 2 in study\_data.

Using subsetting, select all of the elements in row 5 in study\_data.

Using subsetting, select the first 2 rows and all of the columns in study\_data. 

In addition to the forms of subsetting demonstrated in the slides, you can also use 
subsetting to select non-contiguous portions of data. To select non-contiguous portions 
of data from a data frame, you'll use the following syntax, 
my_dataframe[c(rows),c(columns)]. 
Use this syntax to select rows 3 and 5 and columns 2 and 4 in study\_data.

`@sample_code`
```{r}
### Load study_data
study_data <- read.csv(url("https://assets.datacamp.com/production/course_7304/datasets/study_data.csv"))

### Select the third element in column 3 in study_data.


### Select all of the elements in column 2 in study_data.


### Select all of the elements in row 5 in study_data.


### Select the first 2 rows and all of the columns in study_data.


### Select rows 3 and 5 and columns 2 and 4 in study_data.


```

`@hint`


`@solution`
```{r}
#study_data[3,3]
#study_data[,2]
#study_data[5,]
#study_data[1:2,]
#study_data[c(3,5),c(2,4)]
```








---
## Ex 1.5

```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 1e066c06d7
```

This exercise will help you become familiar with functions that add or delete rows and columns in data frames.
You will also learn to export data frames from R using the write.csv() function.


`@instructions`


`@sample_code`
```{r}

```

`@hint`


`@solution`
```{r}

```








