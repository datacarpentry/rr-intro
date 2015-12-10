
## Introduce toolkit

- R, RStudio, R Markdown

- Walk through splash screens of R and RStudio (but spend more time on RStudio)

## R Markdown demo

The goal of is to demonstrate how each of the goals of Organization, Documentation, Dissemination, and Automation can be addressed in an R Markdown document.

### Key steps introduced:

**IMPORTANT:** Emphasize that this exercise is NOT about understanding all the R commands,
but rather getting the big picture of how using R in this way facilitates reproducible
analyses.

- Demonstrate "good practice" for organizing data files and analysis
documents (R Markdown)
- How to read data from a file
- How to manipulate the data, and document it in a reproducible way
    - How easy it would be to revert any changes if need be
- How to subset data
- How to make simple plots in ggplot

### Important features of an R Markdown document to discuss:

- YAML on top
- Code in chunks
- R Markdown syntax
    - Human readable!
    - Limited, so not too time consuming to master
- Self contained workspace

### Extend the analysis:

All code included in the template.

Important to emphasize we're using the same subsetting and visualization code,
just with new data. Reproducing old work with new data is easy!

### Take aways:

- The analysis is self-documenting
- It's easy to extend or refine analyses by copying and modifying code blocks
- The results of the analysis can be disseminated by sending R Markdown and
providing data sources, or just simply providing the generated HTML of just
a summary of the analysis is needed

## Reproducibility checklist:

Point them to the checklist (`checklist.md`), don't read the whole list (too long), but can
discuss the documentation part if there is time.
