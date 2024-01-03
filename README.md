# Problem_Set_1
Directions for Problem Set 1

### Purpose
The purpose of this problem set is to continue building your comfort with R data, R Markdown, and R manipulation.

Your problem set should be reported as an R Markdown file (PDF or HTML) with the answers clearly labeled 

# Question 1 - Formatting Assignment (1 point each)

To practice formatting in markdown your completed markdown file should have the following features. 

- Text/comment describing what you are doing
- Two different  heading levels
- __Bolded__ text
- _Italic_ text
- ***Bold and Italic text***
- 

### Step 1
Install R-Markdown in R-studio

```install.packages('rmarkdown')```

Optional - you can also create PDF files if you want but you need to install tinytex

```
install.packages('tinytex')
tinytex::install_tinytex()  # install TinyTeX
```

### Step 2
Create a new R-Markdown file

Make sure to save it in a directory where you can put other files


### Step 3

Create a new r data chunk for importing our sample data

Import the file ```GSE164805_series_matrix_edited.txt``` using the ```read.table()``` command and save it as a new variable

_hint_ Our data has a header, don't forget to set that when you call read.table

This is a modified gene expression dataset.

It has been modified from the following paper: "Inflammation and Antiviral Immune Response Associated With Severe Progression of COVID-19" - Zhang et al 2021. We will use the full dataset in a later lab







### Task 2 

Import the dataset ```GSE164805_series_matrix.txt``` 

This is the complete expression data from the manuscript 
Zhang Q, Meng Y, Wang K, Zhang X et al. Inflammation and Antiviral Immune Response Associated With Severe Progression of COVID-19. Front Immunol 2021;12:631226. PMID: 33679778

It has been slightly edited to remove the headers

The samples correspond to the table below

![image](https://user-images.githubusercontent.com/47755288/202544449-d768440a-cec1-427e-ba37-b0aebed1249a.png)


### Task 3

Answer the following questions (1 point each)

- Which gene has the highest mean expression value across all samples?
- Which gene has the greatest difference in expression between the healthy female sample and the mild-Covid-19 female sample? What is that difference?
- How many genes have a higher expression in the female sample with mild-Covid-19 as compared to the healthy female sample?
- Plot the median healthy sample expression against the median severe-Covid-19 samples
- What percent of genes have higher median expression in Covid-19 samples compared to healthy control? 
- Which gene has a the largest increase in median expression in severe-Covid-19 samples as compared to the control? 
- Use the file ```GPL26963-20921.array_data.txt``` to find and report the gene name associated with the tag found in the above step. 
- Which gene has the largest increase in median expression in healthy control samples as opposed to severe-Covid-19 samples?
- What is the gene name associated with the gene tag found in the above step

### Task 4

Knit your document and upload it to canvas. 




