# Style Guide

This document is to outline some general principles for writing manuscripts, code, and other documents. See the 
following sections for specifics on each type of document. First, some general recommendations are provided.

### Project Folder Structure

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

#### Folders

The `code/` folder should contain all scripts used as part of the analysis. As will be mentioned later, code files 
should focus on discrete tasks. Do not create a code file that attempts to do all parts of the analysis.

The `data/` folder should be used to store the data (if it can be stored locally, as is the case with publicly 
available) data. Note that it should contain the raw data file that is *never* overwritten. Any processed data sets 
should be separately saved within this folder. 

The `drafts/` folder should contain the drafts of the manuscript or corresponding sections.

The `outputs/` folder should be used to contain any results output from the code. This includes tables, figures, or log
files.

The `permissions/` folder should contain any relevant documentation for permissions or agreements. Examples include
authorship agreements, data use agreements, and IRB approval documentation. The purpose of this folder is to make it
easy to access these materials (e.g., you don't have to search your email inbox for the IRB submission ID).

#### Files

The `README.md` file should briefly describe the project and its motivation. It should also comment on the general
structure of the project folder. What folders are meant to contain which aspects. This is particularly important for
more complicated projects with nested folders. 

The `NOTEBOOK.md` file is your laboratory notebook that should be continually updated as you work through the project.
This should contain general notes and information regarding decisions that were made. It should track the progress 
through a project's lifecycle. Further recommendations are given below.

The `project_checklist.md` file is a copy of the corresponding file from the `resources/` page. It should be completed
through the lifecycle of the project to mark important milestones. This should be regularly updated.

---

## Manuscript Style Guide

The following are some general recommendations for manuscript writing.

- A formatted title page for manuscripts is provided at `resources/manuscript_title_page.docx`. This compiles general
information used for publications.
- Within your project's `drafts/` folder, I recommend having additional folders. One for the original draft and then
create subfolders for the journal(s) the paper is submitted to in order to store the associated files for submission.
This may include a cover letter and other publishing agreements.
- I recommend the following naming convention for drafts `lastname_ShortTitle_YYYY-MM-DD` where `YYYY-MM-DD` denotes 
the day the draft was created. This will help to manage multiple versions of a manuscript without having to rely on
naming conventions like `Project_v3_FINAL_v3_v8`. Use of your last name will also be helpful for your co-authors to
organize the drafts on their computer. 
- When drafting a manuscript, start by drafting an introduction. This can then be shared with potential co-authors and
shows that you identified the relevant publications in your literature review. 
- At the end of the manuscript, keep a space for general notes. When you have a thought about something you might 
want to put into the paper, write it down in this notes section. This way your notes are always connected to the most
recent draft.
- Know your audience. Writing for a medical journal is different from an epidemiology journal which is different from
a statistics journal.
- Work on developing your own style. This often begins with imitating the style of others (but do *not* plagiarize).

---

## Code Style Guide

The following guidelines are meant to enhance the readability and reproducibility of your code. While underappreciated, 
this is a key aspect of research. Further, you or others might need to review your code in the future. With poorly 
documented code, this can be difficult and require substantial time and effort. The principles here are meant to help 
prevent and alleviate these issues. These are recommended guidelines. These can all be tweaked to some extent, but it 
is better to follow them than not.

The following are general style guidelines and recommendations for the code used to conduct the statistical analyses
in the `code/` folder. Again, these are not necessary to follow exactly, but are strong recommendations.

---

Separate code into discrete files that accomplish a small set of tasks. Rather than having a single file that does all
of the tasks, separate your code into multiple files where each does a defined task. For example, your code might be 
structured like
```
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

Comment your code thoroughly. Each line of code should have at least one comment explaining that step. Further, 
decisions or important notes should be documented as block comments in the script. If you're unsure whether you have 
commented your code enough, the answer is you have not. Writing well-documented code should make you feel like you have
excessively commented it.

Develop a data dictionary. When generating a clean data set, you should also create a data dictionary that accompanies
that clean data. It should describe all the variables included and provide their definitions. This will make it easier 
to draft the paper and allow others to understand your analysis and data cleaning procedure. Doing this while you write
the code will make it seem easier than if you wait until writing all the code.

Use informative variables names. A variable name should clearly communicate that variable whenever possible. For 
example, a variable for age the name `age_years` is preferred over `var1`.

Running a script should be done in full. If you are coding something, someone should be able to run the entire script
and get the same output. Do *not* only run sections of your code only. Variable names may be inadvertently carried over
between sections, leading to inconsistent outputs.

For the outputs of your code, these results files should generally not be overwritten when re-running code from prior
times. As such, it is helpful to include the date a result was generated into the file name, similar to the 
recommendation in the manuscript section.

Develop a code review plan. Identify someone who can review your code (either parts or in full). This should be a 
normal part of research code development. We want to minimize the potential for mistakes and this is an important step.
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

### Code Sharing at Publication

The following are some additional guidance for code sharing with publications. The previous code style guidelines are
expected to be followed in addition to these points. For examples, look at my GitHub linked below.

Use GitHub or some other coding sharing website. I share my code at https://github.com/pzivich/publications-code
where projects live in subfolders. Note the clear documentation of projects in the README. An alternative to this 
structure is to create a separate repository for each project. Either of these options is fine with me.

Record versions of the software program and any packages used. These dependencies are important for others to reproduce 
what you have done. So, the information should be clearly indicated. For example, the `README.md` file might list out 
each dependency and its corresponding version.

Have a FAIR plan. To ensure your code is findable and stored for the long-term, use a service like Zenodo or OSF to
generate a DOI and have secondary storage. In particular, Zenodo is easy to integrate with a GitHub repository. 
