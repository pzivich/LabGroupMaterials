# Code Style Guide

This document is to outline some general principles for analytic code. These guidelines are meant to enhance the 
readability and reproducibility of your code. While underappreciated, this is a key aspect of research. Further, you
or others might need to review your code in the future. With poorly documented code, this can be difficult and require
substantial time and effort. The principles here are meant to help prevent and alleviate these issues.

Note that these are recommended guidelines. These can all be tweaked to some extent, but it is better to follow them
than not.

---

## Project Folder Structure

Each project should have a consistent folder structure. This makes it easy to find files across different projects and
have documents readily accessible for meetings. Below is a recommended structure that I continue to use

```
project_name/
    code/
    data/
    drafts/
    outputs/
    permissions/
    README.md
    NOTEBOOK.md
    project_checklist.md
```

### Folders

The `code/` folder should contain all scripts used as part of the analysis. As will be mentioned later, code files 
should focus on discrete tasks. Do not create a code file that attempts to do all parts of the analysis.

The `data/` folder should be used to store the data (if it can be stored locally, as is the case with publicly 
available) data. Note that it should contain the raw data file that is *never* overwritten. Any processed data sets 
should be separately saved within this folder. 

The `drafts/` folder should contain the drafts of the manuscript or corresponding sections. I recommend the following
naming convention for drafts `lastname_ShortTitle_YYYY-MM-DD` where `YYYY-MM-DD` denotes the day the draft was created.
This will help to manage multiple versions of a manuscript. For managing submissions to different journals, I recommend 
subfolders that identify the journal and store the associated files for submission.

The `outputs/` folder should be used to contain any results output from the code. This includes tables, figures, or log
files. In general, these results files should not be overwritten when working with different versions. As such, it is 
helpful to include the date a result was generated into the file name, similar to the recommendation in `drafts/`.

The `permissions/` folder should contain any relevant documentation for permissions or agreements. Examples include
authorship agreements, data use agreements, and IRB approval documentation. The purpose of this folder is to make it
easy to access this materials (e.g., you don't have to search your email inbox for the IRB submission ID).

### Files

The `README.md` file should briefly describe the project and its motivation. It should also comment on the general
structure of the project folder. What folders are meant to contain which aspects. This is particularly important for
more complicated projects with nested folders. 

The `NOTEBOOK.md` file is your laboratory notebook that should be continually updated as you work through the project.
This should contain general notes and information regarding decisions that were made. It should track the progress 
through a project's lifecycle. Further recommendations are given below.

The `project_checklist.md` file is a copy of the corresponding file from the `resources/` page. It should be completed
through the lifecycle of the project to mark important milestones. This should be regularly updated.

---

## Code Style

The following are general style guidelines and recommendations for the code used to conduct the statistical analyses
in the `code/` folder. Again, these are not necessary to follow exactly, but are strong recommendations.

Separate code into discrete files that accomplish a small set of tasks. Rather than having a single file that does all
of the tasks, separate your code into multiple files where each does a defined task. For example, your code might be 
structured like
```commandline
C1_data_clean.*
C2_descriptive.*
C3_analysis.*
C4_sensitivity_analysis.*
```
where the first script cleans the raw data, the second generates the descriptive tables and figures, the third conducts
the main analysis, and the fourth applies sensitivity analyses. Your files do not need to be organized exactly like 
this, but they should make sense for the research project you are doing.

Each file should have a header that contains key details, like a title, creator (and editors) of the code, and the
last modification date. For example,
```
#################################################################
# Project Title
#   Details about what this script does for the analysis
#
# Author (DATE: YYYY/MM/DD)
#################################################################
```

Comment your code thoroughly. Each line of code should have a comment explaining that step. Further, decisions or 
important notes should be documented as block comments in the script. If you're unsure whether you have commented your
code enough, the answer is you have not. It should feel excessive.

Develop a data dictionary. When generating a clean data set, you should also create a data dictionary that accompanies
that clean data. It should describe all the variables included and provide their definitions. This will make it easier 
to draft the paper and allow others to understand your analysis and data cleaning procedure. 

Use informative variables names. A variable name should clearly communicate that variable whenever possible. For 
example, a variable for age the name `age_years` is preferred over `var1`.

Running a script should be done in full. If you are coding something, someone should be able to run the entire script
and get the same output. Do *not* only run sections of your code only. Variable names may be inadvertently carried over
between sections, leading to inconsistent outputs.

Develop a code review plan. Identify someone who can review your code (either parts or in full). This should be a 
normal part of research code development. We want to minimize the probability of mistakes and this is an important step.
Preferred over code review is double-coding, particularly independent double-coding where a person separate codes the 
analysis using only written instructions (no code is shared).

Adhere to any specific language conventions for your program of choice. These meta-language features help others to
understand your code.

Prefer readability over efficiency. Whenever possible, the human-readibility of the code should be preferred over 
computational efficiency. Note that this may not always be possible. When it is not possible, write the human-readable
version as a comment near the other code. Also be sure to use extensive comments to explain how the more efficient
code works.

Use version control. This can help to catch bugs that might be introduced when editing code. It allows one to restore
the code to a previous version, which is particularly important for larger projects. Version control software, like git,
should be used instead of renaming files by versions or dates.

Develop unit tests. We should verify each non-trivial part of our code operates as intended. This can be validated 
through the use of unit-tests or through simulation experiments. This should be done whenever coding a new estimator.

---

## Code Sharing at Publication

The following are some additional guidance for code sharing with publications. The previous code style guidelines are
expected to be followed in addition to these points. For examples, look at my GitHub linked below.

Record versions of the software program and any packages used. These dependencies are important for others to reproduce 
what you have done. So, the information should be clearly indicated. For example, the `README.md` file might list out 
each dependency and its corresponding version.

Use GitHub or some other coding sharing website. I share my code at https://github.com/pzivich/publications-code
where projects live in subfolders. Note the clear documentation of projects in the README. An alternative to this 
structure is to create a separate repository for each project. Either of these options is fine with me.

Have a FAIR plan. To ensure your code is findable and stored for the long-term, use a service like Zenodo or OSF to
generate a DOI and have secondary storage. In particular, Zenodo is easy to integrate with a GitHub repository. 

