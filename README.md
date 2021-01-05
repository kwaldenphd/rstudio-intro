# Intro to R Studio

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Lab Goals

This lab provides a very brief introduction to `RStudio`, its user interface, some basic `R` programming, and a publishing extension known as `RMarkdown`.

## Acknowledgements

This lab procedure is adapted from and based on Ryan Miller's ["A Crash Course in R" tutorial](https://remiller1450.github.io/s230f19/Intro_to_R.html) (Fall 2019, Intro to Data Science STA 230 course, Grinnell College).

# Table of Contents

- [R/RStudio Overview](#rrstudio-overview)
  * [What is `R`?](#what-is-r)
  * [What is `RStudio`?](#what-is-rstudio)
- [Getting Started With `RStudio`](#getting-started-with-rstudio)
  * [Accessing `RStudio`](#accessing-rstudio)
  * [RStudio's Layout](#rstudios-layout)
- [Using `R`](#using-r)
  * [`R` as a Calculator](#r-as-a-calculator)
  * [Help Documentation](#help-documentation)
  * [Including Comments](#including-comments)
- [Objects and Assignments](#objects-and-assignments)
  * [Indexing](#indexing)
- [Reading in Data](#reading-in-data)
  * [Subsetting Data](#subsetting-data)
  * [Logical Conditions and Subsetting](#logical-conditions-and-subsetting)
- [Summarizing Data](#summarizing-data)
  * [Tables, Bar Charts, and Histograms](#tables-bar-charts-and-histograms)
  * [Numeric Summaries](#numeric-summaries)
- [Packages](#packages)
- [R Markdown](#r-markdown)
  * [More on R Markdown](#more-on-r-markdown)
- [Lab Notebook Questions](#lab-notebook-questions)  

# R/RStudio Overview

## What is `R`?

1. "R is a programming language and free software environment for statistical computing and graphics supported by the R Foundation for Statistical Computing. The R language is widely used among statisticians and data miners for developing statistical software and data analysis...as of September 2020, R ranks 9th in the TIOBE index, a measure of popularity of programming languages. A GNU package, the official R software environment is written primarily in C, Fortran, and R itself...and is freely available under the GNU General Public License...Although R has a command line interface, there are several third-party graphical user interfaces, such as RStudio, an integrated development environment, and Jupyter, a notebook interface" ([Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))).

2. `R` is based on the `S` programming language, which is based on/inspired by programming language `Scheme`.

3. The `S` programming language was developed by Bell Labs in the late 1970s.

4. University of Auckland researchers Ross Ihaka nad Robert Gentleman developed an alternative implementation of `S` in the early 1990s that by 1995 was the first open-source release of `R` (under a GNU license).

5. `R` is supported and maintained by the Comprehensive R Archive Network (CRAN), which formed in 1997. 

6. CRAN released the first stable, beta version of `R` (1.0) in 2000.

7. Visit the R project's ["Introduction to R"](https://www.r-project.org/about.html) to learn more about `R`.

## What is `RStudio`?

8. "RStudio is an integrated development environment (IDE) for R, a programming language for statistical computing and graphics" ([Wikipedia](https://en.wikipedia.org/wiki/RStudio)).

9. What is an IDE? "An integrated development environment (IDE) is a software application that provides comprehensive facilities to computer programmers for software development. An IDE normally consists of at least a source code editor, build automation tools and a debugger" ([Wikipedia](https://en.wikipedia.org/wiki/Integrated_development_environment)).

10. An IDE can include features like syntax highlighting, code completion, version control, and debugging.

11. There are a WIDE range of IDEs that are proprietary or open-source, tailored to a specific language or able to work across languages.

12, Some common IDEs include Eclipse, Geany, Brackets, Atom, PyCharm, Spyder, RStudio, etc. For more on IDEs, visit Wikipedia's ["Comparison of integrated development environments"](https://en.wikipedia.org/wiki/Comparison_of_integrated_development_environments) page.

13. `RStudio` is written in `C++` and `Java`, with some `JavaScript`. It uses the `Qt` framework for its graphical user interface.

14. The first public version of `RStudio` (v0.92) was released in 2011. Version 1.0 was released in 2016.

15. The `RStudio` IDE is supported and maintained by a team of developers collectively known as RStudio.

16. Visit [RStudio's website](https://rstudio.com/about/) to learn more about the developer team and user community.

# Getting Started With `RStudio`

## Accessing `RStudio`

17. For this class, you can access RStudio two ways, through downloading and installing on your local computer or through running RStudio in a web browser using RStudio Cloud.

18. To run `R`/`RStudio` on your personal computer:
- Download and install `R` from http://www.r-project.org/
- Download and install `RStudio` from http://www.rstudio.com/

19. To use RStudio Cloud:
- Navigate to https://rstudio.cloud/ in a web browser
- Create a free account

## RStudio's Layout

20. When you open `RStudio` (on a personal computer or via RStudio Cloud) for the first time, you will see three default windows or panels.

21. The ***Console*** (left side of the window) is similar to the command line or terminal. It can run program files or execute commands typed directly into the console.

22. Your ***Environment*** (top right) shows you the names of datasets, variables, and user-created functions that have been loaded into your workspace and can be accessed by your code.

23. The ***Files/Plots/Help Viewer*** (bottom right) will display graphics generated by your code (Plots), Files that are part of your project (Files), or additional documentation or support (Help).

24. This default layout gives us the option to execute commands using the console, but we don't actually have a blank program file we can use to write, test, and save programs.

25. We can create a new RScript file by clicking `File -> New File -> RScript`.

26. We now see the blank `.R` file as a fourth panel in the top-left hand side of our window.

27. Save the blank file and you should see the new `.R` file show up in your `Files` panel.

<blockquote>Q1: Create a blank R Script and save it as “Lab1_[LastName]”, where [LastName] is replaced by your last name. Use this R Script to record your answers to this lab’s questions. You can also use this script to try out all of the example code shown throughout the lab, but the lab notebook only needs to include answers to the question prompts.</blockquote>

# Using `R`

28. `R` is an interpreted language, which allows you to have the computer execute any piece of the code in your RScript at any time.

29. To run a piece of code, simply highlight it and hit Ctrl-Enter. You should see the code that you ran appear in the Console, along with the response generated by the code.

30. You can also move your cursor to a specific line and run that section of code.

## `R` as a Calculator

31. At its most basic level, `R` can be used to perform arithmetic operations.

32. Try running these examples in the Console or using your new R Script.

```R
4 + 6 - (24/6)
```

```R
5 ^ 2 + 2 * 2
```

33. Basic arithemtic operators in `R` include:

Operator | Description
--- | ---
`+` | addition
`-` | subtraction
`*` | multiplication
`/` | division
`^` or `**` | exponentiation
`%%` | modulus operator, i.e. `5%%2` is `1`
`%/%` | integer division, i.e. `5%/%2` is `2`

34. Some arithmetic operations require the use of functions. 

35. In the example below, the function “exp” raises the number e to the power you provide as an input to the function. 

36. The number “2” is given as an input into the function `exp`:
```R
exp(2)
```

37. The `sqrt` function finds a square root:
```R
sqrt(4)
```

38. The `abs` function takes the absolute value:
```R
abs(-1)
```

39. A function’s ***inputs*** are called ***arguments*** in `R` documentation. 

40. For complex functions, the arguments should be specified using names which are internally defined within the function. 

41. The example below takes the base two logarithm of the number 4 using the `log` function and appropriate inputs to the arguments `x` and `base`.

```R
log(x = 4, base = 2)
```

## Help Documentation

42. `R` contains thousands of functions, each potentially containing many different arguments. 

43. When using an unfamiliar function for the first time, it can be useful to refer to that function’s documentation.

44. The documentation which will describe the function’s uses and arguments. 

45. You can pull up a function’s documentation by typing `?` before the function’s name in the console. 

46. For example, if we wanted to see the documentation for the `log` function:
```R
?log
```

## Including Comments

47. When coding, it is good practice to include comments that describe what your code is doing. 

48. In `R` the `#` character is used to start a comment. 

49. Everything on the same line to the right of the `#` will not be executed when that line is submitted to the console.

```R
# This entire line is a comment and will not be executed as part of the program
```

```R
1:6 # The command "1:6" appears before this comment
```

50. In your RScript, comments appear in green. 

51. Remember that the `#`” starts a comment only for a single line of your RScript, so long comments that requiring multiple lines should each begin with their own `#`.

<blockquote>Q2: In the R Script created for Q1, add a comment with the text “Q2” on your script’s first line. Then, in the second line, write code that finds the square root of the absolute value of negative four.</blockquote>

# Objects and Assignments

52. `R` stores data in containers called ***objects***. 

53. Data is ***assigned*** to an object using `<=` or `=`.

54. After assignment, data can be referenced using the object name.

55. This is similar to how a programming language like Python interacts with named variables.

56. The simplest objects are called ***scalars***, or a single ***element***.

```R
x <- 5 # Assigns the integer value to an object labeled x

x^2 # Performs an arithemtic operation using the value assigned to x
```

57. `R` stores sequences of elements in objects called ***vectors***.

```R
x <- 1:3 # the sequence (1, 2, 3) is assigned to the vector named x
print(x) # prints the sequence assigned to x vector
```

```R
y <- c(1, 2, 3) # the function 'c' concatenates arguments separated by commas into a vector
print(y)
```

```R
z <- c("A","B","C") # vectors can contain many different kinds of characters- not just numbers
print(z)
```

58. There are three different types of vectors in `R`:
- Numeric vectors: `x = c(1, 2, 3)`
- Character vectors: `x = c("A","B","C")`
- Logical vectors: `x = c(TRUE, FALSE, TRUE)`

59. A vector's type is important, because many functions will only execute on a certain type of input.

60. A function will return an error message is given an input of the wrong type.

61. We can check an object type using the `typeof` function.

```R
chars <- c("1","2","3") # creates a character vector
typeof(chars)
```

```R
nums <- c(1,2,3) # creates a numeric vector
typeof(nums)
```

```R
mean(chars) # this command will produce an error, because mean() only works for numeric vectors
```

```R
mean(nums) # this will work because nums is a numeric vector
```

62. Many `R` functions are vectorized, meaning they can accept a scalar input and return a scalar output. 

63. Or, they can accept a vector input and return a vector.

64. The `sqrt` function is vectorized:
```R
nums <- c(1,2,3,4)
sqrt(nums)
```

65. Datasets are usually stored in objects called ***data.frames*** which are composed of several vectors of the same length.
```R
DF <- data.frame(x = x, y = y, z = z) # creates a data.frame object DF
print(DF)
```

<blockquote>Q3: In your R Script, on a new line add the comment “Q3” and on the line(s) below this comment create a data.frame object named “dfn” containing a vector named “number” that is the integers from 1 to 10, and a vector named “number_squared” which is the integers from 1 to 10 squared.</blockquote>

## Indexing

66. Suppose we setup a vector `x` and would like to extract the element in its second position and assign it to a new object called `b`:
```R
x <- 5:10
b <- x[2]
b
```

67. The square brackets are used to access a certain position (or multiple positions) within an object.

68. In this example, we access the second position within the object `x`.

69. NOTE: `R` begins counting at 1 (one). This contrasts with a programming language like Python that starts counting at 0 (zero).

70. Some objects, such as data.frames, have multiple dimensions, requiring indices in each dimension to describe an element’s position.
```R
DF <- data.frame(x = x, y = y, z = z)
DF[2,3] # this command accesses the element in row 2, column 3
```

# Reading in Data

71. There are many ways to get data into `R`. 

72. If a data set is stored somewhere on your computer as a `.csv` file, you can load it using the R function `read.csv`.

73. NOTE: You will need to provide the full file path to the data file, if the file is not located in your current working directory.
- Consult RStudio's documentation to learn more about [how to set your working directory](https://support.rstudio.com/hc/en-us/articles/200711843-Working-Directories-and-Workspaces)

74. NOTE: If working in RStudio Cloud, you would need to upload the file from your local computer into the RStudio Cloud project environment. Once uploaded, you can load the data using its file name--no path needed since the file is in your working directory.

75. Example for loading a `.csv` file in your working directory:
```R
my.data <- read.csv("sample_file.csv")
```

76. Example for loading a `.csv` file NOT in your working directory;
```R
my.data <- read.csv("H://path_to_my_data/my_data.csv")
```

77. `read.csv` can also read `.csv` files stored on the web. 
```R
my_data <- read.csv("https://raw.githubusercontent.com/kwaldenphd/rstudio-intro/main/IowaCityHomeSales.csv")
```

78. We can use the `head` function to see the first few rows of our newly-loaded data.
```R
head(my_data) # this function prints the first several rows of an object
```

79. You can explore a newly-loaded dataset using a few key functions.
```R
dim(my_data) # prints the dimensions of my.data

nrow(my_data) # prints the number of rows for my.data

ncol(my_data) # prints the number of columns for my.data

colnames(my_data) # prints the names of the variables or columns for my.data
```

<blockquote>Q4: In your R Script, on a new line add the comment “Q4” and on the line(s) below write code that reads and stores the data located at https://raw.githubusercontent.com/kwaldenphd/rstudio-intro/main/IowaCityHomeSales.csv as “election_data”. Then write code that finds dimensions of this data.frame.</blockquote>

## Subsetting Data

80. Suppose we want to access a single variable in our data set.

81. We can express that programatically.
```R
sale_price1 <- my_data$sale.amount # The $ accesses the variable named 'sale.amount' within 'my.data'
sale_price2 <- my_data[,1] # We can also use indexing to access 'sale.amount'

# Notice how we specified second dimension of 'my.data' (its columns)
head(sale_price1)

head(sale_price2)
```

82. Suppose we wanted to access a single entry or row in our dataset:
```R
first_house <- my_data[1,] # This stores the entire first row
head(first_house)
```

83. Suppose we want a range of entries or rows:
```R
firstfive_houses <- my_data[1:5,] # This stores the first five rows
head(firstfive_houses)
```

## Logical Conditions and Subsetting

84. Suppose we want to know which elements of `sale.amount` are larger than $200,000:
```R
my_data$sale.amount > 200000 # Logical vector for the condition "> 200000"
which(my_data$sale.amount > 200000) # Positions of elements where the condition is "TRUE"
```

85. `R` includes a few useful logical operators:

Operator | Description
--- | ---
`<` | less  than
`<=` | less than or equal to
`>` | greater than
`>=` | greater than or equal to
`==` | exactly equal to
`!=` = not equal to

86. Logical conditions are particularly useful for subsetting objects.

87. We could create a new object containing all homes that sold for more than $500,000 and have living areas over 3,000 square feet.
```R
large_and_expensive <- my_data[my_data$sale.amount > 500000 & my_data$area.living > 3000,]
```

88. We could create a new object containing all homes that don't have a basement ***or*** don't have air conditioning.
```R
nobsmt_or_noac <- my_data[my_data$bsmt == "None" | my_data$ac != "Yes",]
dim(nobsmt_or_noac)
```

89. We could create a new object containing homes that don't have a basement ***and*** don't have air conditioning.
```R
nobsmt_and_noac <- my_data[my_data$bsmt == "None" & my_data$ac != "Yes",]
dim(nobsmt_and_noac)
```

<blockquote>Q5: In your R Script, on a new line add the comment “Q5” and on the line(s) below write code that create a new data.frame called “election_losers” that subsets “election_data” (which you created in Q4) to include only rows where the result was “Lost”.</blockquote>

# Summarizing Data

## Tables, Bar Charts, and Histograms

90. One-way frequency tables summarize a single categorical (factor) variable, while two-way frequency tables summarize the relationship between two categorical variables. 

91. Both of these summaries can be created by the `table` function:
```R
table(my_data$style) # A one-way frequency table of 'style'
```

```R
table(my_data$bedrooms, my_data$bsmt) # A two-way frequency table of 'bedrooms' and 'bsmt'
# Notice that 'bedrooms' is stored as a numeric variable, but it still can be used in the table function
```

92. Tables are their own type of object.

93. They can be used by functions like `barplot`:
```R
my_table <- table(my_data$bsmt) # Tables can be stored as objects
barplot(my_table) # Creates a bar plot from a table
```

94. We can construct basic visuals of numeric variables too:
```R
hist(my_data$sale.amount) # histograms are for numeric variables
```

95. Later on we will cover how to produce more elagant visuals, but these functions are useful for quick exploratory analyses.

## Numeric Summaries

96. `R` has a few built-in functions that can calculate common summary statistics.
```R
mean(my_data$sale.amount) # mean

sd(my_data$sale.amount) # standard deviation

min(my_data$sale.amount) # minimum

max(my_data$sale.amount) # maximum

quantile(my_data$sale.amount, .35) # the 35th percentile
```

97. The `summary` function provides all of these descriptive statistics at once.
```R
summary(my_data$sale.amount)
```

<blockquote>Q6: In your R Script, on a new line add the comment “Q6” and on the line(s) below write code that finds the range of the variable “Approval” using the data.frame “election_losers” (which you created in Q5).</blockquote>

# Packages

98. To facilitate more complex tasks in `R`, many in the user community develop their own sets of functions known as packages. 

99. To install packages:
```R
install.packages("PACKAGE NAME")
```

100. For example, to install the visualization package `ggplot2`:
```R
install.packages("ggplot2")
```

101. Once a package has been installed, we still need to load it using the `library` function.
```R
library(PACKAGE_NAME)
```

102. NOTE: You'll need to ***load*** a package every time you open RStudio but you only need to ***install*** it once. This applies to those working in a local RStudio installation or in RStudio Cloud.

103. Best practice is to comment out the `install.packages` lines at the start of an R Script, and to include the `install.packages` lines for any packages you need to load.

104. What this looks like in practice:
```R
# install.packages("ggplot2") # commented out line that would install the needed package

library(ggplot2) # executable command that loads the installed package; if someone running the program does not have the package installed, all they would have to do is uncomment the previous line
```

105. We'll have an entire lab on `ggplot2` later in the semester, but a quick example of how it can generate data visualizations:
```R
qplot(my_data$ac) # qplot is a function in the package ggplot2
```
# R Markdown

106. At the beginning of this document you were instructed to open a file called an “R Script”. This type of file is designed to contain only `R` code and comments.

107. `RStudio` also supports many other types of files, some of which utilize an authoring framework known as “R Markdown”. 

108. In `RMarkdown`, you can save and execute `R` code AND ALSO generate narrative text that goes along with your executable code and its output.

109. Authoring in `RMarkdown` requires the `rmarkdown` package:
```R
install.packages("rmarkdown")
library(rmarkdown)
```
110. Once the package is installed and loaded, you can create RMarkdown files by selecting "File -> New File -> R Markdown."

111. Go ahead and try this, hitting "Ok" to use the default options.

112. Your new RMarkdown file should look a lot like an RScript. 

113. The first thing you should notice is the header, which is initiated by three `-` characters and closed by another three `-` characters. 

114. The header contains information that will appear at the top of your compiled report.

115. The second thing you’ll see is a block of code initiated by ` ```{r setup}` and closed by ` ``` `.

116. This just sets up some options used when executing your R code when your report is built, for now you can ignore it.

117. Next you’ll see section headers defined by the `#` character. 

118. The number of `#` characters determines the level (size) of the header.

119. Finally you’ll see some blocks of code initiated by ` ```{r} ` and closed by ` ``` `.

120. These are bits of `R` code that can be executed by clicking on the green arrow in the upper right corner of the code box. 

121. You can execute smaller pieces of code within these blocks by highlighting them and hitting Ctrl-Enter.

122. To compile your R Markdown file into a polished report you need to “Knit” the file. 

123. You can do this by clicking on the `Knit` button (the yarn ball icon) located towards the upper left of screen.

124. You can export an R Markdown file in a variety of formats. 

125. Two common formats for exporting an `.rmd` file include:
- `.html` which will display as a webpage
- `.pdf` which will display as a PDF document

126. Download the `.rmd` file in this repository and open it in RStudio.
- [Link to download from Google Drive (ND users only)](https://drive.google.com/drive/folders/1V7F-chL0D3H-PGTURuYj-iMSBa38KjvP?usp=sharing)

127. Explore how the file runs, as well as how it differs from your experience working through this lab using an RScript file or the Console.

## More on R Markdown

128. The information in the prior section provides a very brief introduction R Markdown.

129. The lessons created by RMarkdown’s developers at https://rmarkdown.rstudio.com/lesson-1.html are a great way to learn more about this authoring framework. 

130. These lessons include numerous screen shots, videos, and more detailed explanations of exactly how RMarkdown works and what it is capable of.

# Lab Notebook Questions

You can submit your lab notebook as an R Script (`.r`) file or as an R Markdown (`.rmd`) file.

Q1: Create a blank R Script and save it as “Lab1_[LastName]”, where [LastName] is replaced by your last name. Use this R Script to record your answers to this lab’s questions. You can also use this script to try out all of the example code shown throughout the lab, but the lab notebook only needs to include answers to the question prompts.

Q2: In the R Script created for Q1, add a comment with the text “Q2” on your script’s first line. Then, in the second line, write code that finds the square root of the absolute value of negative four.

Q3: In your R Script, on a new line add the comment “Q3” and on the line(s) below this comment create a data.frame object named “dfn” containing a vector named “number” that is the integers from 1 to 10, and a vector named “number_squared” which is the integers from 1 to 10 squared.

Q4: In your R Script, on a new line add the comment “Q4” and on the line(s) below write code that reads and stores the data located at https://raw.githubusercontent.com/kwaldenphd/rstudio-intro/main/IowaCityHomeSales.csv as “election_data”. Then write code that finds dimensions of this data.frame.

Q5: In your R Script, on a new line add the comment “Q5” and on the line(s) below write code that create a new data.frame called “election_losers” that subsets “election_data” (which you created in Q4) to include only rows where the result was “Lost".

Q6: In your R Script, on a new line add the comment “Q6” and on the line(s) below write code that finds the range of the variable “Approval” using the data.frame “election_losers” (which you created in Q5).
