Reproducible Science Workshop - Intro I
========================================================
font-family: 'Helvetica'


Overview
========================================================

Tagline: Accelerating scientific progress through reproducible science

Mission: To train researchers in the best practices and approaches of 
reproducible research and accelerate scientific progress.


Intro to Reproducible Research
========================================================

- Getting to know you
- Recognize the problems that reproducible research helps address 
via a case studies
- **Exercise**: Identify pain points in getting your analysis to be reproducible
- Introduce tools that address these pain points
- **Demo**: R / RStudio / RMarkdown toolkit for reproducibile data analysis


Getting to know you...
========================================================

with respect to reproducibility


Why should we care?
========================================================

Examples of irreproducible research has caused significant issues


Science retracts gay marriage paper without agreement of lead author
========================================================

- Science retracted a study of how canvassers can sway people's opinions about 
gay marriage.

- Science Editor-in-Chief: Original survey data not made available for independent
reproduction of results + Survey incentives misrepresented + Sponsorship 
statement false

- Two Berkeley grad students attempted to replicate the study and discovered that 
the data must have been faked.

- Methods we'll discuss today can't prevent this, but they can make it easier to 
discover such issues.

Source: 
http://news.sciencemag.org/policy/2015/05/science-retracts-gay-marriage-paper-without-lead-author-s-consent


Seizure study retracted after authors realize data got "terribly mixed"
========================================================

From the authors of **Low Dose Lidocaine for Refractory Seizures in Preterm Neonates**:

*"The article has been retracted at the request of the authors. After carefully 
re-examining the data presented in the article, they identified that data of two 
different hospitals got terribly mixed. The published results cannot be reproduced in accordance with scientific and clinical correctness."*

Source: http://retractionwatch.com/2013/02/01/seizure-study-retracted-after-authors-realize-data-got-terribly-mixed/


Bad spreadsheet merge kills depression paper, quick fix resurrects it
========================================================

- The authors informed the journal that the merge of lab results and other survey 
data used in the paper resulted in an error regarding the identification codes.

- **Original conclusion:** Lower levels of CSF IL-6 were associated with current 
depression and with future depression [...].

- **Revised conclusion:** Higher levels of CSF IL-6 and IL-8 were associated with 
current depression [...].

Source: 
http://retractionwatch.com/2014/07/01/bad-spreadsheet-merge-kills-depression-paper-quick-fix-resurrects-it/


Exercise 1: Motivating reproducibility
========================================================

This is a two-part exercise:

**Part 1:** Analyze + document

**Part 2:** Swap + discuss


Exercise 1 - Part 1
========================================================

Complete the following tasks and **write instructions / documentation** for your 
collaborator to reproduce your work starting with the original dataset 
(`data/gapminder-5060.csv`).

1. Visualize life expectancy over time for Canada in the 1950s and 1960s using 
a line plot.

2. Something is clearly wrong with this plot! Turns out there's a data error 
in the data file: life expectancy for Canada in the year 1967 is coded
as `999999`, it should actually be `69.96`. Make this correction.

3. Visualize life expectancy over time for Canada again, with the corrected data.<br>
*Stretch goal:* Add lines for Mexico and US.


Exercise 1 - Part 2
========================================================

Introduce yourself to your collaborator and tell them why you're here.

1. Swap instructions / documentation with your collaborator, and try to reproduce 
their work, first **without talking to each oher**. 
If your collaborator does not have the software they need to reproduce your work, we 
encourage you to either help them install it or walk them through it on your computer in a 
way that would emulate the experience. (Remember, this could be part of the 
irreproducibility problem!)

2. Then, talk to each other about challenges you faced (or didn't face) or why 
you were or weren't able to reproduce their work.


Exercise 1 - Reflection
========================================================

- What tools did you use for the data analysis? For documentation?
- Were you successful in reproducing each others' work?
    - What would happen if your collaborator is no longer available to 
    walk you through their analysis?
- What made it easy / hard for reproducing your partners' work?
- What would have to happen if 
    - you had to swap out the dataset or extend the analysis further?
    - you caught further data errors and had to re-create the analysis
    with corrections?
    - you had to revert back to the original dataset?


Coffee break
========================================================

<center>
<br>
![coffee](img/coffee_000000_264.png)
<br>
Put a sticky on your laptop <br>
for help with software set up
</center>
