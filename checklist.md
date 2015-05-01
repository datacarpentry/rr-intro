# Checklist Questions to stimulate thought about a Project's Reproducibility

The following checklist serves as a tool to help you think about the reproducibility of your data analysis. Many of the questions can be thought of as having a yes/no answer. A better approach would be to see the questions as being open ended with the real question being, "What can I do to improve the status of my project on this bullet point?". With that in mind, you'll never get 100% of the bullets right for your project, but you'll always be improving.

## Documentation
* Is there a README file that indicates the purpose of the project, who to contact with questions, a map of the directory structure, and a description of what software and hardware is needed to reproduce your workflow?
* Are there README files in each folder describing the contents of the folder, how they were acquired/generated?
* Is there a CITATION file that tells users how to site the project, data, and code?
* Are there instructions on how to obtain the raw data and citations for those data?
* Is there a list of dependencies with the exact version number of every external application used in the process?
* Do you indicate dates that websites were accessed to obtain data?
* Are there appropriate LICENSE files that specifies the license under which you're distributing your content, data, and code? Have you edited them to include informations pertinent to your project?
* Have you noted the license(s) for others peoples' content, data, and code used in your analysis?
* For analyses that utilize a random number generator, have you noted the underlying random seed(s)? Do you state the other seeds that you have tested the results with?
* Is your code well documented?
* Do you use a self-commenting coding practice?
* Do each of your scripts have a header indicating the inputs, outputs, and dependencies?
* Is it documented how files relate to each other?


## Organization
* Are all data, code, results, and documentation housed within a monophyletic folder structure?
* Is this folder structure under version control?
* Is the project's repository publicly avaialable?
* Are there assurances that this repository will remain accessible?
* Is your project folder structured to separate your data, code, documentation, and results?
* Does your code run from the project's home directory and output to the appropriate directory?
* Are your raw and processed data files separated?
* Is your raw data truly raw or has it been manipulated?
* Are files that store manually-entered data structured to be easily read by a computer?
* Do files use a consistent naming scheme that indicates what they contain?
* Is there a mechanism in place to archive large files?
* When using other people's data, are you defensive against tarbombs?


## Automation
* Is the project under the control of a makefile? Could one run `make clean; make`?
* How long would it take to rebuild your directory system if your hard drive failed?
* Is manual manipulation of data kept to a minimum?
* If manual manipulation is required, is there sufficient documentation to re-do the manipulation
* Does data processing make use of open software code
* How sensitive are results to differences in operating system, dependency versions?
* Is code written to be flexible enough to the addition of new data?
* Does code include unit tests to confirm that it does what you think it does?
* Does your repository make use of continuous integration tools to insure internal reproduciblity?


## Publication
* Are papers and reports from the project generated using literate programming tools so that results are not hard-coded?
* Did you include a reproducibility statement or declaration at the end of your paper(s)?
* Did you archive preprints of resulting papers in a public repository?
* Did you release the underlying code and new data at the time of submitting a paper?
* What mechanisms are in place to insure your project remain accessible and reproducible in 5 years?
