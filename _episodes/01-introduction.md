---
title: "Introduction"
teaching: 20
exercises: 20
questions:
- "What is reproducible research?"
- "What are the keys to reproducible research?"
objectives:
- "Learn the four facets of reproducibility."
keypoints:
- "There are four facets to reproducibility: Documentation, Organization, Automation, Dissemination"
output:  
      html_document: 
---



## As you arrive, please make sure the following R packages are installed:
- `tidyverse`
- `rmarkdown`
- `knitr`

```r
install.packages("tidyverse")
```

## Motivating Reproducibility
- The sciences have with reproducibility problem. [Nature article](http://www.nature.com/news/1-500-scientists-lift-the-lid-on-reproducibility-1.19970)
- Many published studies cannot be reproduced:
    - **Replication** - when independent investigators use methods, protocols, data, and equipment to confirm scientific claims.
    - **Reproduction** - when data sets and computer code are made available for researchers to verify results.
- Peng (2009) Reproducible research and Biostatistics. [*Biostatistics 10: 405-408*](http://biostatistics.oxfordjournals.org/content/10/3/405.full)


> ## *Science* retracts paper without agreement of lead author.
> - Journal retracted a study of how canvassers can sway people's opinions about gay marriage.
> -[Editor-in-Chief](http://news.sciencemag.org/policy/2015/05/science-retracts-gay-marriage-paper-without-lead-author-s-consent): Original survey data:
>    + not made available for independent reproduction of results
>    + Survey incentives misrepresented
>    + Sponsorship statement false
>
> - Two grad students attempted to reproduce the study and could not. Concluded the data must have been fabricated. [538 story](http://fivethirtyeight.com/features/how-two-grad-students-uncovered-michael-lacour-fraud-and-a-way-to-change-opinions-on-transgender-rights/)
>
> - Methods we'll discuss today can't prevent fraud, but they can make it easier to discover such issues.
{: .callout}

> ## Retracted, but not fraud
> - One researcher had seven papers retracted because of irreproducibility [Retraction Watch](http://retractionwatch.com/2014/11/14/univ-no-misconduct-but-poor-research-practice-in-mgt-profs-work-now-subject-to-7-retractions/#more-23666)
> - Couldn't find the data [Wiley](http://onlinelibrary.wiley.com/doi/10.1111/j.1468-1331.2011.03524.x/abstract)
> - "Extensive" errors force retraction of lymphoma paper [JRO](http://retractionwatch.com/2013/01/14/extensive-errors-force-retraction-of-lymphoma-radiation-paper/)
> - Many, many more [Hackathon](https://github.com/Reproducible-Science-Curriculum/Reproducible-Science-Hackathon-Dec-08-2014/wiki/Irreproducible-Examples)
{: .callout}

> ## Seizure study retracted after authors realized data were "Terribly mixed"
> - From the authors of Low Dose Lidocaine for Refractory Seizures in Preterm Neonates:
> "The article has been retracted at the request of the authors. After carefully re-examining the data presented in the article, they identified that data of two different hospitals got terribly mixed. The published results cannot be reproduced in accordance with scientific and clinical correctness." [IJP](http://retractionwatch.com/2013/02/01/seizure-study-retracted-after-authors-realize-data-got-terribly-mixed/)
{: .callout}

> ## Bad spreadsheet merge kills depression paper, quick fix resurrects it
> - The authors informed the journal that the merge of lab results and other survey data used in the paper resulted in an error regarding the identification codes.
> - **Original conclusion** : Lower levels of CSF IL-6 were associated with current depression and with future depression.
> - **Revised conclusion**: Higher levels of CSF IL-6 and IL-8 were associated with current depression.
{: .callout}

## Exercise: Motivating reproducibility

This is a two-part exercise:

> ## Part 1: Analyze + Document
>
> Complete the following tasks and write instructions / documentation for your collaborator to reproduce your work starting with the original dataset (`data/gapminder-5060.csv`):
> 1. Visualize life expectancy over time for Canada in the 1950s and 1960s using a line plot.
> 
> 2. Something is clearly wrong with this plot! Turns out there's a data error in the data file: life expectancy for Canada in the year 1957 is coded as 999999, it should actually be 69.96. Make this correction.
>
> 3. Visualize life expectancy over time for Canada again, with the corrected data.
>
> *Stretch goal*: Add lines for Mexico and United States.
>
> > ## Solution
> >
> > 1. **Import Data**
> >
> >
> >```r
> > gap_5060 <- read.csv("../data/gapminder-5060.csv")
> >```
> > 
> > 2. **Load required pacakges**
> >
> >```r
> > library("tidyverse")
> >```
> >
> >```
> >## Loading tidyverse: ggplot2
> >## Loading tidyverse: tibble
> >## Loading tidyverse: tidyr
> >## Loading tidyverse: readr
> >## Loading tidyverse: purrr
> >## Loading tidyverse: dplyr
> >```
> >
> >```
> >## Conflicts with tidy packages ----------------------------------------------
> >```
> >
> >```
> >## filter(): dplyr, stats
> >## lag():    dplyr, stats
> >```
> >
> > 3. **Task 1** - Filter the data for Canada only:
> >
> >```r
> > gap_5060_CA <- gap_5060 %>% filter(country == "Canada")
> >```
> >
> > 4. **Task 1** - Visaualize:
> >
> >```r
> > ggplot(data = gap_5060_CA, aes(x = year, y = lifeExp)) +
> >    geom_line()
> >```
> >
> ><img src="figure/task_2_visualize-1.png" title="plot of chunk task_2_visualize" alt="plot of chunk task_2_visualize" style="display: block; margin: auto;" />
> > **Task 2**. Something is clearly wrong with this plot! Turns out there's a data error in the data file: life expectancy for Canada in the year 1957 is coded as `999999`, it should actually be `69.96`. Make this correction:
> > - `mutate` for creating a new variables
> > - `replace` for replacing a data entry in a specific
location as determined by the logical statement `(country == "Canada" & year == 1957)`
> >
> >
> >```r
> > gap_5060 <- gap_5060 %>%
> >   mutate(lifeExp = replace(lifeExp, (country == "Canada" & year == 1957), 69.96)) %>%
> >   as.data.frame()
> >```
> > **Task 3**. Visualize life expectancy over time for Canada again, with the corrected data. Exact same code as before, but note that the contents of `gap_5060` are different as it has been updated in the previous task.
> >
> >
> >```r
> > gap_5060_CA <- gap_5060 %>%
> > filter(country == "Canada")
> > 
> > ggplot(data = gap_5060_CA, aes(x = year, y = lifeExp)) +
> >   geom_line()
> >```
> >
> ><img src="figure/task_3-1.png" title="plot of chunk task_3" alt="plot of chunk task_3" style="display: block; margin: auto;" />
> > **Task 3** - Stretch goal: Add lines for Mexico and United States.
> > - `%in%` for logical operator testing if a country's name is in the list provided
> > - Same visualization code as before, only difference is the input dataset
> >
> >
> >```r
> > gap_5060_NA <- gap_5060 %>%
> >   filter(country %in% c("Canada", "Mexico", "United States"))
> > 
> > ggplot(data = gap_5060_NA, aes(x = year, y = lifeExp, color = country)) +
> >   geom_line()
> >```
> >
> ><img src="figure/more_task_3-1.png" title="plot of chunk more_task_3" alt="plot of chunk more_task_3" style="display: block; margin: auto;" />
> > {: .output}
> {: .solution}
{: .challenge}

> ## Part 2: Swap + discuss
>
> Introduce yourself to your collaborator and tell them why you're here.
>
> 1. Swap instructions / documentation with your collaborator, and try to reproduce their work, first without talking to each other. If your collaborator does not have the software they need to reproduce your work, we encourage you to either help them install it or walk them through it on your computer in a way that would emulate the experience. (Remember, this could be part of the irreproducibility problem!)
>
> 2. Then, talk to each other about challenges you faced (or didn't face) or why you were or weren't able to reproduce their work.
>
> {: .source}
> {: .output}
{: .challenge}


## Reflection
  - What tools did you use (Excel / R / Python / Word / plain text etc.)?
  - Were you successful in reproducing each others' work?
  - What would happen if your collaborator is no longer available to walk you through their analysis?
  - What made it easy / hard for reproducing your partners' work?
  - What would have to happen if:
      - you had to swap out the dataset or extend the analysis further?
      - you caught further data errors and had to re-create the analysis with corrections?
      - you had to revert back to the original dataset?

## Summary
- Everyone struggles with reproducibility and it is a hindrance to moving science forward.
- Evan with a fairly simple analysis challenges were faced in four main areas: organization, documentation, automation, and dissemination
- Over the two day workshop, data analysis tasks will become more complex as we gather more data and ask more complicated questions, so we need better tools and workflows to combat issues arising in these areas


## Why we care
It is vital that scientific research be reproducible. This improves communication, openness, and transparency. We consider that there are four facets required to maximize reproducibility.


## Four facets of reproducibility:

1. **Documentation**: difference between binary files (e.g. docx) and text files and why text files are preferred for documentation.

1. **Organization**: tools to organize your projects so that you don't have a single folder with hundreds of files.

1. **Automation**: the power of scripting to create automated data analyses.

1. **Dissemination**: publishing is not the end of your analysis, rather it is a way station towards your future research and the future research of others.
