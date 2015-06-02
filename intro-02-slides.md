Reproducible Science Workshop - Intro II
========================================================
font-family: 'Helvetica'
date: 'enter date'


Intro I summary
========================================================

* Everyone struggles with reproducibility and it is a hindrance to moving 
science forward

* Evan with a fairly simple analysis challenges were faced in four main areas:
organization, documentation, automation, and dissemination

* Over the two day workshop, data analysis tasks will become more complex as we 
gather more data and ask more complicated questions, so we need better tools and 
workflows to combat issues arising in these areas


Four facets
========================================================

* Documentation: difference between binary files (e.g. docx) and text files and why 
text files are preferred for documentation, use markdown to document your workflow 
so that anyone can pick up your data and follow what you are doing

* Organization: tools to organize your projects so that you don't have a single 
folder with hundreds of files

* Automation: the power of scripting in the R programming language and how you 
can integrate that into markdown to create automated data analyses

* Dissemination: publishing is not the end of your analysis, rather it is a way 
station towards your future research and the future research of others


Toolkit
========================================================

![R](img/Rlogo-1.png)

* * * 

![RStudio](img/RStudio-Logo-Blue-Gradient.png)


Why R?
========================================================

* Programming language for data analysis
* Free!
* Open source
* Widely used and supported across all disciplines
* Can be used on Windows, Mac OS X, or Linux

* * * 

![RSplashScreen](img/RSplashScreen.png)


Why not language X?
========================================================

* There are a number of other great programming tools out there that can also be 
used to improve the reproducibility of your analysis

* The key is to use some type of language that will allow you to automate and 
document your analysis

* Once you master one language you'll probably find it easier to learn another


Why RStudio?
========================================================

* Runs on top of R
* Gives you a single environment to combine your documentation and your analysis 
with markdown support
* Gives you a bunch of really cool features that we'll explore throughout the workshop

* * * 

![RSplashScreen](img/RStudioSplash.png)


Anatomy of RStudio
========================================================

<center>
![RSplashScreen](img/RStudioSplash.png)
</center>


Anatomy of RStudio
========================================================

* Left: Console
    * Every time you launch RStudio, it will have the same text at the top of the 
    console telling you the version of R that you’re running. 
    * Below that information is the prompt. 
* Upper right: workspace and a history of the commands that you've previously 
entered
* Lower right: Any plots that you generate + access to files, help, packages


R Packages
========================================================

* Packages are the fundamental units of reproducible R code. They include reusable R
functions, the documentation that describes how to use them, and (often) sample data.
(From: http://r-pkgs.had.co.nz)

* We will use the `ggplot2` package for plots in this session. `ggplot2` is a plotting
system for R, based on the grammar of graphics
  
* To install this packages run the following in the Console:

```r
install.packages("ggplot2")
```


Revisit Exercise 1 
========================================================

* Open `intro-01-template.Rmd` 
* Click on *Knit HTML* to compile the document


Goals of the next exercise
========================================================

* Demonstrate "good practice" for organizing data files and analysis 
documents (RMarkdown)
* How to read data from a file
* How to combine data from multiple data frames
* How to subset data
* How to make simple plots in ggplot

**NOT** about understanding all the R commands, but **rather** getting the big 
picture of how using R in this way facilitates reproducible analyses


Exercise 2: Extending your analysis
========================================================

1. Append the new data `gapminder-7080.csv` and `gapminder-90plus.csv` to your 
existing data set. <br>*Be careful* as you do so, as the ordering of columns 
in the data set may not match between the different CSV files!

2. Create line plots of life expectancy over time for Canada, Mexico, and the 
United States that run from 1952 to 2007.<br>
*Stretch goal:* In the same plot, add similar line plots for Cambodia, China, and 
Japan and Uganda, Egypt, and South Africa.

3. Create a scatter plot depicting GDP vs. life expectancy of countries in Europe 
for 2007. <br>
*Stretch goal:* In the same plot, add another scatter of points for Asia, Africa, 
and the Americas, coloring the countries from each region (continent) with the 
same color.


Exercise 2: Resources
========================================================

* Open `intro-02-template.Rmd` 
* Click on *Knit HTML* to compile the document


Exercise 2: Take aways
========================================================

* The analysis is self-documenting
* It's easy to extend or refine analyses by copying and modifying code blocks
* The results of the analysis can be disseminated by sending Markdown and 
providing data sources, or just simply providing the generated HTML of just 
a summary of the analysis is needed


Reproducibility checklist
========================================================

* Serves as a tool to help you think about the reproducibility of your data 
analysis
* Many of the questions can be thought of as having a yes/no answer
* A better approach would be to see the questions as being open ended with 
the real question being, "What can I do to improve the status of my project 
on this bullet point?"
* With that in mind, you'll never get 100% of the bullets right for your project, 
but you'll always be improving


Reproducibility checklist: Documentation (1/2)
========================================================

* Is there a README file that indicates the purpose of the project, who to contact 
with questions, a map of the directory structure, and a description of what software 
and hardware is needed to reproduce your workflow?
* Are there README files in each folder describing the contents of the folder, 
how they were acquired/generated?
* Is there a CITATION file that tells users how to site the project, data, and code?
* Are there instructions on how to obtain the raw data and citations for those data?
* Is there a list of dependencies with the exact version number of every external application used in the process?
* Do you indicate dates that websites were accessed to obtain data?


Reproducibility checklist: Documentation (2/2)
========================================================
* Are there appropriate LICENSE files that specify the license under which you're
distributing your content, data, and code? Have you edited them to include info 
pertinent to your project?
* Have you noted the license(s) for others peoples' content, data, and code used 
in your analysis?
* For analyses that utilize a random number generator, have you noted the underlying 
random seed(s)? Do you state the other seeds that you have tested the results with?
* Is your code well documented?
* Do you use a self-commenting coding practice?
* Do each of your scripts have a header indicating the inputs, outputs, and dependencies?
* Is it documented how files relate to each other?
