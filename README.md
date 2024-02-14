# Lab Assignment for Week 06
## EDA using a massive airline dataset
## Due on [Canvas](https://psu.instructure.com/courses/2306358/assignments/15965265) on Fri., Feb. 23 at 11:59pm

**On this and all labs for the rest of the semester: When you have a choice between the [datascience package](https://www.data8.org/datascience/) and the [pandas library](https://pandas.pydata.org/docs/), you are free to use either method to complete your work. HOWEVER, on Lab 6, we recommend using the datascience package, as the file management required here is already tricky.**

Much of this lab consists of file management since one of the files involved is huge.  A [supplementary jupyter notebook](https://github.com/DS200-SP2024-Hunter/Week06-DueFeb23/blob/main/Lab06SupplementaryNotebook.ipynb) helps with this. **The supplementary notebook uses the datascience package rather than pandas.**

EDA stands for "exploratory data analysis," a commonly-used abbreviation in statistics and data science.
The main objective of today's lab is to load a massive dataset and then illustrate a few statistical concepts related to sampling and exploratory data analysis (EDA).

**Objective**:  Load the dataset represented by the `flights.csv` file (as a `Table` object if you use the `datasciences` library) and use it to answer some questions about flight delays using descriptive statistics and graphics.  Later in the course, we'll use this lab as a way to discuss some inferential statistics, mostly based on hypothesis tests.

**Your assignment** is as follows:

1. In a new Jupyter notebook, create a `Table` object that consists of the 5.8-million-row dataset in the `flights.csv` file. Don't forget to begin your Jupyter notebook by loading in needed python resources.  Insert a text box after your code for this step that briefly describes how you got the `flights.csv` file into your google drive space.

2. Select a systematic sample of somewhere between 500 and 1000 rows.  Since the dataset has 5.82 million rows, you'll need to enter an appropriate value of `gap` in the code to get an appropriate sample size.  (You'll need to think a bit about what value of `gap` to use.) Insert a text box after your code for this step that explains how a systematic sample (usually good) differs from a simple random sample (the gold standard of sampling) and a convenience sample (bad!).  You might find it helpful to refer to the intro to Chapter 10 for this explanation.

3. Join your sample with the airports dataset containing latitude/longitude information on the origin airports.  Keep only the columns relating to the date, origin and destination airports, scheduled departure time, and delay.  Notice that the number of rows in your sample after the join operation is smaller than the number beforehand.  Insert a text box after your code for this step that explains how the 'join' method can result in a new table that has fewer rows than the original table.

4. Create a new column called `DAY_OF_YEAR` that produces an approximate day of year from the `MONTH` and `DAY` columns.  There are better ways of doing this than supplied in the sample code, but a simplistic method will suffice here.  Feel free to improve on the code supplied if you wish.

5. A scatterplot is a good way to depict the relationship between two quantitative variables.  Produce a scatterplot of `LATITUDE` vs. `DELAY`.  In deciding which variable to plot on the horizontal and vertical axes, we often take the horizontal axis to be the variable that may be viewed as explaining the other, if such a choice makes sense.  Based on this fact, insert a text box after your code for this step that explains why we've chosen `LATITUDE` as the horizontal axis variable for this plot.  Also comment on whether you notice anything interesting on your plot.  

6. Produce a scatterplot of `LONGITUDE` vs. `DELAY`.  Insert a text box after your code for this step that explains whether you notice anything interesting on your plot.

7. Produce a scatterplot of `DAY_OF_YEAR` vs. `DELAY`. Insert a text box after your code for this step that explains whether you notice anything interesting on your plot.

When you've completed this, you should select "Print" from the File menu, then save to pdf using this option.  The pdf file that you create in this way is the file that you should upload to Canvas for grading.  We have found that if you can select the "A3" paper size from the advanced options, this seems to solve the problems that are sometimes encountered in this step.

