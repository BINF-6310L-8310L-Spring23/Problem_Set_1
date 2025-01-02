# Problem_Set_1
Directions for Problem Set 1

**Be sure to answer the Questions in the associated Canvas Quiz**

## Purpose
The purpose of this problem set is to continue building your comfort with R data, R Markdown, and R manipulation.

Your problem set should be reported as an R Markdown file (PDF or HTML) with the answers clearly labeled 

### Question 1 - Formatting Assignment (1 point each)

_There is no section in the quiz to put these_

To practice formatting in markdown your completed markdown file should have the following features. 

- Text/comment describing what you are doing
- Two different  heading levels
- __Bolded__ text
- _Italic_ text
- ***Bold and Italic text***
- 

## Step 1 - Install R-Markdown
Install R-Markdown in R-studio

```install.packages('rmarkdown')```

Optional - you can also create PDF files if you want but you need to install tinytex

```
install.packages('tinytex')
tinytex::install_tinytex()  # install TinyTeX
```

## Step 2 - Create new R-Markdown file
Create a new R-Markdown file

Make sure to save it in a directory where you can put other files


## Step 3 - Import the data

Create a new r data chunk for importing our sample data

Import the file ```GSE164805_series_matrix_edited.txt``` using the ```read.table()``` command and save it as a new variable

_hint_ Our data has a header; don't forget to set that when you call ```read.table```

This is a modified gene expression dataset.

It is from the following paper: "Inflammation and Antiviral Immune Response Associated With Severe Progression of COVID-19" - Zhang et al 2021. We will use the full dataset in a later lab

### Question 2 

How many rows are in the dataset? The function for this is ```nrow()```

### Question 3

How many columns are in the dataset? The function for this is ```ncol()```

### Question 4

Is the object storing our data a data frame or a matrix? You can check this using the Environment tab or the function ```str()```

### Question 5 

Are there any NAs in our dataset? 

### Question 6

Is the column ID_REF a factor? You can check this with the function ```is.factor()```

### Question 7

What is the line of code you would use to set the column ID_REF as a factor? 


## Step 4 - Subset the data frame 

We are interested in only the following data

The genes (ID_REFs) 
- ASHG19AP1B100028737V5
- ASHG19AP1B100017453V5
- ASHG19AP1B100004705V5

For the individuals (columns)
- GSM5019817
- GSM5019827
- GSM5019828

Subset your data frame to include only those genes for only those individuals. 
There are lots of ways to do this. Some examples are listed here: https://sparkbyexamples.com/r-programming/r-subset-data-frame-with-examples/

### Question 8

What is the mean expression across the three genes for GSM5019827?

## Step 5 - Learn about wide to long format

Our data is currently in **wide** format. In the wide format, each ID_REF appears only once and is associated with many variables (columns), each having its own value. 

Each row, therefore, contains many different observations that fall in the same group

Many times (like for visualization in ggplot) we need to have the data in **long** format where each row is a singular observation belonging to a specific variable. 

For more information on wide and long format see this summary https://www.statology.org/long-vs-wide-data/

There are two main functions to transition between long and wide - **tidyr** and **reshape2**

Read about how to use these functions here: http://www.cookbook-r.com/Manipulating_data/Converting_data_between_wide_and_long_format/ 

## Step 6 - Change the subset dataset to long format

Add either tidyr or reshape2 to your small subset data. 

Use ```gather()``` or ```melt()``` to transform you dataframe to long format

The commonly used figure-making package ggplot requires the data to be in long format. 

To install ggplot use ```install.packages("ggplot2")```

If you are new to ggplot you can read a basic introduction here: https://ggplot2.tidyverse.org/articles/ggplot2.html 
If you are new to the ```geom_boxplot``` ggplot then you can refer to this tutorial https://www.sthda.com/english/wiki/ggplot2-box-plot-quick-start-guide-r-software-and-data-visualization 


### Question 9

Create a boxplot in ggplot2 showing the variation in gene expression (x-axis) across the different individuals. 
Paste the figure into the canvas question. 








