# Programming_with_R
Notes on Introduction and fundamentals of R

## 1.0 Introduction
R is a programming tool/language that is widely used by statisticians, data scientists and other users. It is widely used in computational genomics because it provides a wide variety of statistical (linear and nonlinear modeling, classical statistical tests, time-series analysis classification, clustering, etc) and graphical techniques, and is highly extensible.

This tutorial will focus on two fundamental aspects of R.

i. Basic statistics

ii. Genomic analysis

### 1.1 Installing R and R studio
R is the *backbone* statistical language that uses a Graphical User Interface (GUI) called R studio. For one to use R, they must have R studio installed

### R
For efficiency, you need to install the latest versions of R (4.0.3 and above). R is a free access software that can be downloaded [here](https://cran.rstudio.com/)

### R studio
You can download and install R studio using this [link](http://www.rstudio.com/). Upon installation, you can start using R by opening/starting R studio which gives you an interactive medium called the console. You can access the [documentation](https://support.rstudio.com/hc/en-us/categories/200035113-Documentation) on the layout of R studio

## 2.0 Basic statistics in R
### 2.1 Using R as a simple calculater
We can start by using R as a simple arithmetic calculator. The console has a ">" sign which is refered to as the command prompt. This sign tells the user when to start typing.

For instance:
```
R: 10+10

Output: [1] 20

R: 100 *     100

Output: [1] 1000
```

In the examples above, when you type 10 + 10 in the console, R computes this and gives you an output 20, so is 100 * 100 when you press enter. From this, we can infer a few things:
- R is not space sensitive unlike other programming languages. That is, `10+10, 10   +  10 = 20`
- Pressing enter runs your code
- The output has a [1] sign at the beginning. This means that your output lines are indexed, and this helps to tell you the beginning of a new output line from previous lines
- R can take different arithmetic operators such as division (/), addition (+), subtraction (-), multiplication (*)*, integer division (%/%), power (^), modulus (%%), among others

### 2.2 Data structures and data types

#### 2.2.1 Creating variables

R gives you the ability to store pieces of information (data) with lables or tags. This is called creating variables

#### variable assignment
Variables are created using assignment operators `"=" or "<-"`. The latter is referred to as a conventional assignment operator

Examples:
```
R: distance = 50
or
R: distance <- 50
```
Note that, R did not return any output after running the above command. However, it is important to note that it computed and created a variable with the name "distance" and assigned it a value 50. You can confirm this by calling the variable "distance"

Example:
```
R: distance
Output: [1] 50

You can also achieve this by using the function "print ()"

R: print(distance)
Output: [1] 50
```
**N/B: You can as well do calculations using variables**

#### 2.2.2 Data types

To effectively work with R, it is paramount that you understand the basic data types and structures and they they are operated/manupulated. Data structures, for example, are key when working with R because you will be interacting with them daily when doing analysis in R. 
There are six common data types in R:

- character eg "b", "abcd"
- Logical eg TRUE, FALSE
- Numeric eg 7, 10.1
- integers eg 3L (where L makes the 3 to be stored as an integer)
- complex: complex numbers with real and imaginery parts eg 3 + 7i

There are many user-friendly functions that are used in examining different features of vectors and objects in R.
There are:

- class() - what kind of object is it (high-level)?
- typeof() - what is the object’s data type (low-level)?
- length() - how long is it? What about two dimensional objects?
- attributes() - does it have any metadata?

Examples:
```
Var1 <- FALSE
sample_number <- 1
sample_id <- "1594abcde11"

R: class (Var1)
Output: [1] "logical"

R: class (sample_number)
Output: [1] "numeric"

R: class (sample_id)
Output: [1] "character"
```

N/B To create character data type, the value(s) assigned to the variable must be enclosed in double quotes:

`sample_id <- "1594abcde11"`

***Exercise 1: Explore the usage of the other functions***

#### 2.2.3 Vectors

A vector is a variable with the ability to store multiple variables. For instance, a tutor wants to grade an assignment from a class of 12 students with the following grades: 

`100, 0, 90, 92, 94, 94, 94, 100, 0, 90, 98, 98`

#### Creating a vector

The combine function `c ()` is used when creating vectors. You pass the values you want to be stored in a vector to the `c ()` function, separated by commas. To view the vector, call the variable name.

Example:
```
R: grades <- c(100, 0, 90, 92, 94, 94, 94, 100, 0, 90, 98, 98)
R: grades
Output:  [1] 100   0  90  92  94  94  94 100   0  90  98  98
```
#### Single out information in vectors

In the event where you would like to know the grade for the first student, you just reference the first element in the vector.
```
R: grades[1]
Output: [1] 100
```
Note that, the number in the square brackets is the index of the items in the vector. If you wanted the 12th item, you would write `grades[12]`. It is also important to note that other programming languages begin indexing at `0 not 1`.

#### Altering elements in a vector

Suppose you need to do some changes on the vector, there are two approaches:
1. recreating the entire vector while making the changes
2. just replacing those values that you are intrested in
Option is the easiest.
Example:
```
Assuming you want to do away with the zeros in the vector, that means it is element 2, and 9. Therefore, replace through reassignment

R: grades[2] <- 80
R: grades[9] <- 75
R: grades
Output: [1] 100  80  90  92  94  94  94 100  75  90  98  98
```
It is also easier to add 2 points throughout the entire elemnts in the vector by just running:

```
R: grades +2
Output: [1] 102  82  92  94  96  96  96 102  77  92 100 100

However, the values won’t be updated. For example, if you call grdes:

R: grades
Output: [1] 100  80  90  92  94  94  94 100  75  90  98  98

You’ll notice that the command grades+2 didn’t update. It just calculated the results but did not update the vector.

To update the vector, type

R: grades = grades +  2
R: grades
Output: [1] 102  82  92  94  96  96  96 102  77  92 100 100
```

#### Counting elements in a vector

If you wanted to know how many grades were recorded, you can achieve this by using the function `length ()`

```
R: length (grades)
Output: [1] 12
```







