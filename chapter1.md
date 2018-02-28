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
height <- 3
area <- base * height / 2
```





