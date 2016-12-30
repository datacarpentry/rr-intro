rr-intro
========

## Lesson synopsis:

In this session we will start by reviewing case studies of (lack of) reproducibility gone wrong. Then participants will work on two reproducibility exercises: first a simple data manipulation and analysis exercise using any software they generally work with and then the same exercise (and extensions to it) using `RMarkdown` in `RStudio` as a better alternative, highlighting how this approach makes documentation, organization, automation, and dissemination easier.  

## Syllabus:

- Recognize the problems that reproducible research helps address
- Identify pain points in getting your analysis to be reproducible.
- The role of documentation, sharing, automation, and organization in making your research more reproducible.
- Introducing some tools to solve these problems, specifically `R`/`RStudio`/`RMarkdown`.

## Goals:

At the beginning of this session, participants should be able to

- use a spreadsheet program to generate a plot
- use a text editor (Word, Google Docs, etc.) to communicate

At the end of the session students will be able to

- recognize the problems that reproducible research helps address
- identify pain points in getting their analysis to be reproducible

The specific problems to be addressed in each session are as follows:

- First half (01): motivating reproducibility
- Second half (02): introduce R Markdown as a reproducible data analysis tool

The first half of the intro session is language agnostic. If  a workshop uses programming language other than R, only intro-02 will need to be modified.

## Pre-workshop:

Participants install `R` + `RStudio`.

See [email template](https://github.com/Reproducible-Science-Curriculum/rr-intro/blob/master/preworkshop-email.md).

## First half (01):

See instructor notes (`intro-01-instr-notes.Rmd`) for details.

- Welcome + go over schedule
- Motivating reproducibility slides
- Group discussion about current tools people are using for documentation / reproducibility
- Ex 1: Motivating reproducibility

## Second half (02):

See instructor notes (`intro-02-instr-notes.Rmd`) for details.

- Provide `RMarkdown` approach to what's done in Session 1 (`intro-template.Rmd`)

- Wrap up with pointing participants to the [reproducibility checklist](https://github.com/Reproducible-Science-Curriculum/rr-intro/blob/master/checklist.md).

## Data attribution

- [Gapminder data](http://www.gapminder.org/data/). [Gapminder data is licensed CC-BY 3.0](https://docs.google.com/document/pub?id=1POd-pBMc5vDXAmxrpGjPLaCSDSWuxX6FLQgq5DhlUhM#h.ul2gu2-uwathz).

- Processed and subset (population size, life expectancy, GDP per capita; only every 5 years only starting 1952, only complete records) [Gapminder data as `R` package](https://github.com/jennybc/gapminder). The [data-raw](https://github.com/jennybc/gapminder/tree/master/data-raw) sub-directory reveals the journey from Gapminder.org's Excel workbooks to increasingly clean and tidy data.
    - clean dataset can be located in R in the following way (after installing the package):

        ~~~
        pathToTsv <- system.file("gapminder.tsv", package = "gapminder")
        ~~~
        {: .r}

## People and credits

This lesson was first created at the [1. Reproducible Science Curriculum Hackathon]. The corresponding author is **Mine Çetinkaya-Rundel** ([@mine-cetinkaya-rundel]). See the commit log for other contributors.

Please post feedback and issues with the lesson on the repository's issue tracker. For instructor questions about teaching this lesson, you can also contact the corresponding author directly.

[@mine-cetinkaya-rundel]: https://github.com/mine-cetinkaya-rundel
[1. Reproducible Science Curriculum Hackathon]: https://github.com/Reproducible-Science-Curriculum/Reproducible-Science-Hackathon-Dec-08-2014
