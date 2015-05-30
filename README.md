rr-intro
========

## People:

**Mine Çetinkaya-Rundel** ([@mine-cetinkaya-rundel](https://github.com/mine-cetinkaya-rundel)), Paul Magwene ([@pmagwene](https://github.com/pmagwene)), Pat Schloss ([pschloss](https://github.com/pschloss)), Kristina Riemer ([KristinaRiemer](https://github.com/KristinaRiemer))

## Lesson synopsis:

In this session we will start by reviewing case studies of (lack of) reproducibility gone wrong. Then participants will work on two reproducibility exercises: first a simple data manipulation and analysis exercise using any software they generally work with and then the same exercise (and extensions to it) using `RMarkdown` in RStudio as a better alternative, highlighting how this approach makes documentation, organization, automation, and dissemination easier.  

## Syllabus:

* Recognize the problems that reproducible research helps address
* Identify pain points in getting your analysis to be reproducible.
* The role of documentation, sharing, automation, and organization in making your research more reproducible.
* Introducing some tools to solve these problems, specifically R/RStudio/RMarkdown.

## Intro sessions:

At the beginning of this workshop, participants should be able to

- use a spreadsheet program to generate a plot
- use a text editor (Word, Google Docs, etc.) to communicate

At the end of the intro sessions students will be able to 

- recognize the problems that reproducible research helps address 
- identify pain points in getting their analysis to be reproducible.

The specific problems to be addresses in each session are as follows:

- Session 1: documentation and sharing
- Session 2: automation and organization

The second session will also introduce them to some tools that can be used to solve these 
problems, specifically R/RStudio/RMarkdown.

## Session 1:

### Pre-workshop

Participants install R+RStudio

See Intro Session 1 materials for email template

### Intro

- Welcome + go over schedule
    * Group discussion: 6 months from now can you or someone else go back to your project and understand what was going on? What types of methods do you use to document a project?
    * Take notes on the board as to tools people use.

- Pick a case study or two from https://github.com/Reproducible-Science-Curriculum/Reproducible-Science-Hackathon-Dec-08-2014/wiki/Irreproducible-Examples

### Ex 1: Motivating reproducibility

Data analysis task + share/reproduce + discuss. Outline is in the instructor notes (`intro-01-instr-notes.Rmd`).

## Coffee break:

Catch everyone up with R/RStudio instructions

## Session 2:

- Provide RMarkdown approach to what's done in Session 1 (intro-01-template.Rmd)

### Ex 2: Extending your analysis

Demonstrate how an approach based on executable scripts and self documenting code makes it easier to automate, organize, and extend our analyses.  Outline can be found in the instructor notes (`intro-02-instr-notes.Rmd`).

- Wrap up with reviewing the reproducibility checklist is at `checklist.md`.

## Data attribution

- [Gapminder data](http://www.gapminder.org/data/). [Gapminder data is licensed CC-BY 3.0](https://docs.google.com/document/pub?id=1POd-pBMc5vDXAmxrpGjPLaCSDSWuxX6FLQgq5DhlUhM#h.ul2gu2-uwathz).

- Processed and subset (population size, life expectancy, GDP per
  capita; only every 5 years only starting 1952, only complete records)
  [Gapminder data as R package](https://github.com/jennybc/gapminder). The [data-raw](https://github.com/jennybc/gapminder/tree/master/data-raw) sub-directory reveals the journey from Gapminder.org's Excel workbooks to increasingly clean and tidy data.
    - clean dataset can be located in R in the following way (after
      installing the package):

        ```R
        pathToTsv <- system.file("gapminder.tsv", package = "gapminder")
        ```