# ZETA Lab Notebook

These are instructions and guidelines for creating and maintaining a laboratory notebook throughout the lifecycle of a
project. It is expected that each research group member will maintain a notebook for each project. It should be stored 
for your records. As I am ultimately responsible for the scientific work as a PI/supervisor/academic mentor, I may ask 
that you share your laboratory notebook with me.

**Purpose**: the intention behind a lab notebook is for record maintenance throughout a project. This material records
your decisions throughout the process. It can help to serve as a reminder behind key decisions in a project. It also
serves as a place to store meta-data about a project for you and others. 

---

## Format

A lab notebook should be created for each project you are working on and should be stored in the corresponding
project folder. Use of a markdown file is recommended for its interoperability and simple structure. Another option is
to use Obsidian (see `software.md`), which allows for more structured note-taking.

Regardless, the header of the file should provide a title and brief description of the project. A suggested format is 
provided below

```
# Project Title

A brief project description. No more than 5 sentences.

Author: Paul Zivich

Start date: 2026/07/21

----
```

## Guidance

The laboratory notebook should be updated continually while working on the project. In particular, I recommend updating
the notebook on each day a project is worked on. For example, your lab notebook might look like
```
## 2026/07/21

Started the pre-project checklist in the `project_title/` folder. Identified a set of potential co-authors: Dr Seuss,
Stephen Hawking, and Albert Einstein. Reached out to Albert about being second author, with the idea that he replicates
the analysis in Python.

Started drafting the IRB materials. Given this is secondary de-identified data, the initial submission will be NHSR.

## 2026/07/22

Albert agreed to replicating the code for second author. Have saved the confirmatory email under 
`project_title/permissions`. Spoke with Dr Seuss and he mentioned some interesting papers recently published in Whoville
related to this topic. Need to read these to check for overlap

## 2026/07/29

Began data analysis. Some key decisions made during this process
- Modeling age with cubic splines. Knots were chosen based on X, Y, Z.
- The variable for income was recoded based on a paper by Newton et al. (1665).

Also discussed journal options. Thoughts were to submit to: [...], [...], or [...]. No strong preferences from anyone.

During the laboratory group meeting, presented the preliminary results. Marie Curie pointed out a discrepancy in the
descriptive table. Need to go back to check if that issue arose from one of the variable definitions.
```
In particular, we should be recording key decisions, future steps, problems encountered that require resolution, and 
major revisions needed in code.

Do *not* overwrite previous days. The laboratory notebook should be a running document that only becomes longer. It 
should never have items being deleted. Also please date the laboratory notebook.

