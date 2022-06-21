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
R: `10+10`

Output: `[1] 20`

R: `100 *     100`

Output: `[1] 1000`
```

In the examples above, when you type 10 + 10 in the console, R computes this and gives you an output 20, so is 100 * 100 when you press enter. From this, we can infer a few things:
- R is not space sensitive unlike other programming languages. That is, `10+10, 10   +  10 = 20`
- Pressing enter runs your code
- The output has a [1] sign at the beginning. This means that your output lines are indexed, and this helps to tell you the beginning of a new output line from previous lines
- R can take different arithmetic operators such as division (/), addition (+), subtraction (-), multiplication (*)*, integer division (%/%), power (^), modulus (%%), among others

### 2.2 Data structures and data types
R gives you the ability to store pieces of information (data) with lables or tags. This is called creating variables

#### variable assignment
Variables are created using assignment operators `"=" or "<-"`. The latter is referred to as a conventional assignment operator

Examples:
```
R: `distance = 50`
or
R: `distance <- 50`
```
Note that, R did not return any output after running the above command. However, it is important to note that it computed and created a variable with the name "distance" and assigned it a value 50. You can confirm this by calling the variable "distance"

Example:
```
R: `distance`
Output: `[1] 50`
You can also achieve this by using the function "print ()"
R: `print(distance)`
Output: `[1] 50`
```
**N/B: You can as well do calculations using variables**







