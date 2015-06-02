Reproducible Science Workshop - Intro I
========================================================
font-family: 'Helvetica'
date: 'enter date'


Overview
========================================================

Tagline: Accelerating scientific progress through reproducible science

Mission: To train researchers in the best practices and approaches of reproducible research and accelerate scientific progress.


Schedule
========================================================

Day 1

- 09:00: Introduction to Reproducible Research
- 10:30: Coffee / R&RStudio install catch up
- 12:30: Lunch break
- 13:30: Organizing your project to facilitate Reproducible Research
- 15:00: Coffee
- 17:00: Wrap-up

* * *

Day 2

- 09:00: Automating your workflows
- 10:30: Coffee
- 12:30: Lunch break
- 13:30: Sharing and publishing your research workflow
- 15:00: Coffee
- 16:30: Wrap-up


Intro to Reproducible Research
========================================================

**Before coffee break:**
- Getting to know you
- **Case study**: Recognize the problems that reproducible research helps address via a case study
- **Exercise I**: Identify pain points in getting your analysis to be reproducible

* * *

**After coffee break:**
- Introducing some tools to solve these problems, specifically R/RStudio/RMarkdown
- Revisit Exercise I with new tools
- **Exercise II**: The role of documentation, sharing, automation, and organization in making your research more reproducible


Getting to know you...
========================================================

with respect to reproducibility


Why should we care?
========================================================

Examples of irreproducible research has caused significant issues


Science retracts gay marriage paper without agreement of lead author
========================================================

* Science retracted a study of how canvassers can sway people's opinions about 
gay marriage.

* Science Editor-in-Chief: Original survey data not made available for independent
reproduction of results + Survey incentives misrepresented + Sponsorship statement 
false

* Two Berkeley grad students attempted to replicate the study and discovered that 
the data must have been faked.

* Methods we'll discuss today can't prevent this, but they can make it easier to 
discover such issues.

Source: 
http://news.sciencemag.org/policy/2015/05/science-retracts-gay-marriage-paper-without-lead-author-s-consent


Seizure study retracted after authors realize data got "terribly mixed"
========================================================

From the authors of **Low Dose Lidocaine for Refractory Seizures in Preterm Neonates**:

*"The article has been retracted at the request of the authors. After carefully re-examining the data presented in the article, they identified that data of two different hospitals got terribly mixed. The published results cannot be reproduced in accordance with scientific and clinical correctness."*

Source: http://retractionwatch.com/2013/02/01/seizure-study-retracted-after-authors-realize-data-got-terribly-mixed/


Bad spreadsheet merge kills depression paper, quick fix resurrects it
========================================================

* The authors informed the journal that the merge of lab results and other survey data 
used in the paper resulted in an error regarding the identification codes.

* **Original conclusion:** Lower levels of CSF IL-6 were associated with current 
depression and with future depression [...].

* **Revised conclusion:** Higher levels of CSF IL-6 and IL-8 were associated with 
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

Complete the following tasks and write instructions/documentation for your 
collaborator to reproduce your work starting with the original dataset (`data/gapminder-5060.csv`)

1. Visualize life expectancy over time for Canada in the 1950s and 1960s using 
a line plot.<br>
*Stretch goal:* Add lines for Mexico and US.

2. Visualize the relationship between GDP and life expectancy for countries in 
Europe in 1952.<br>
*Stretch goal:* Add a line for 1967 in another color.

<center>
Put a pink sticky on your laptop <br>
for help with R/RStudio installation
</center>


Exercise 1 - Part 2
========================================================

Introduce yourself to your collaborator and tell them why you're here.

1. Swap instructions/documentation with your collaborator, and try to reproduce their 
work without talking to each oher. If your collaborator does not have the software 
they need to reproduce your work, we encourage you to either help them install it or 
walk them through it on your computer in a way that would emulate the experience.

2. Then, talk to each other about challenges you faced (or didn't face) or why you 
were or weren't able to reproduce their work.


Exercise 1 - Wrap up
========================================================

* What tools did you use (Excel / R / Word / plain text etc.)?

* Was your collaborator successful in reproducing your work?


Exercise 1 - Wrap up
========================================================

* Have you ever tried to reproduce someone else's data analysis before?
* Have you ever tried to reproduce your own work before?
* What tools did you use and were you successful in reproducing your collaborator's work?
* What made it easy/hard for reproducing your parners' work?
* What would have to happen if you had to extend the analysis further?
* If you caught a data error how easy/hard would it be to re-create the analysis?
* What would happen if your collaborator is no longer available to walk you through their analysis?


Coffee break
========================================================

<center>
<br>
![coffee](img/coffee_000000_264.png)
<br>
Put a pink sticky on your laptop <br>
for help with R/RStudio installation
</center>
