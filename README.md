#   Applied Mathematics 5300 Project

##  Title
Analyzing E. Coli DNA Structure Using Wavelets

##  Contents
- [Installation](#installation)
- [Sandbox](#sandbox)
- [Description](#description)
  - [Project Presentation Expectations](#project-presentation-expectations)
  - [Project Paper Expectations](#project-paper-expectations)
  - [Project Timeline](#project-timeline)
- [Proposal](#proposal)
- [Artifacts](#artifacts)
- [Team](#team)

##  Installation
Here are two sets of instructions for creating the python virtual environment; one using pip and the other using conda.

### Pip (`requirements.txt`)
Install Anaconda from https://www.anaconda.com/download

```bash
conda create -n math python==3.11.9
conda activate math
pip install -r requirements.txt
```

### Conda (`environment.yml`)
Install Anaconda from https://www.anaconda.com/download

```bash
conda env create -f environment.yml
conda activate math
```

[Back to Top](#applied-mathematics-5300-project)

##  Sandbox
The `sandbox/` directory is a safe place for exploratory work. If you want to experiment with a notebook, try a different analysis path, or make temporary edits without changing the tracked project files, copy the notebook from the project base directory into `sandbox/` and work from there instead.

This is useful when you want freedom to test ideas, generate intermediate outputs, or make messy work-in-progress changes without cluttering the main codebase. The `sandbox/.gitignore` file is configured so files you place there are not uploaded to the repository, which helps keep the shared project history focused on the final versions of notebooks and code.

[Back to Top](#applied-mathematics-5300-project)

## Description
This is the project space for UML's Spring 2026 Math 5300 course. 

### Project Presentation Expectations
Each presentation should be about 20 minutes long. After each presentation we will have a few minutes for questions and discussion. Each team member must contribute something during the presentation, but it is not required for contributions to be equal among team members.

Ordinarily, each team member can expect to receive the same grade for the group presentation.

The presentation should focus on a single, clearly defined goal. The team should meaningfully collaborate to produce a coherent presentation. Avoid trying to fit in too many topics. Instead, focus on one thing and do that well.

A good presentation will not go overtime and answer the following questions or variants of them in a meaningful way:
- What (is it that you are presenting)?
- Why (is it important or relevant or interesting)?
- How (does it work, or why does it work, etc.)? (theoretical or practical focus are both acceptable)

You may choose what the “it” in those questions is. The content should go beyond what was discussed in class – all class content can be assumed to be known to the audience.

The presentation will be graded based on content (it should answer those questions appropriately), correctness and clarity.

### Project Paper Expectations
While it is encouraged that project papers are discussed with the team, the project paper must be prepared and submitted by each team member individually and independently. Do not copy your teammates’ papers and give them credit where credit is due! Plagiarism and other forms of academic dishonesty will not be tolerated under any circumstances. Use of text generators such as ChatGPT must be disclosed.

Each project paper must be at least 4 and at most 8 pages.

The content may be a summary of the presentation, or it could focus on a different aspect of the topic that may or may not have appeared in the presentation.

The paper will be graded by content, correctness and clarity. Length is irrelevant as long as it falls in the prescribed range.

It is strongly recommended that the paper is written in LaTeX (you can use overleaf.com). Papers written by hand or in Word are acceptable if they are clearly legible and submitted as PDF.

If your project involves coding, source code should be submitted with your project paper, but it does not count toward the page count. The source code is allowed to be identical within a team, but you must give proper credit.

You must be able to explain your project paper to me and you may be required to do

### Project Timeline
- Project presentations held on: Wednesday, April 29 (Last day of class)
- Project papers due: Friday, May 1 (Hard deadline, no extensions!)

[Back to Top](#applied-mathematics-5300-project)

##  Proposal

We propose to analyze the E. coli genome with discrete wavelets to identify and characterize frequency patterns across scales in two DNA signal representations: a binary GC-indicator signal and four binary nucleotide indicator signals for A/C/G/T. The goal is to characterize how variability in these signals is distributed across scales and locations, and to determine whether coding and non-coding regions exhibit distinguishable multiscale signatures.  We will start by looking at Haar wavelets since these are the simplest waveform, and they most closely resemble the binary nature of the proposed signals.  If we have time, we **_may_** move on to using a more complex wavelet, such as Daubechies wavelets, in order to study some of the smoother and more complex patterns that may be buried in these signals.

Relevant notes regarding this proposal:
- Nucleotide bases
  - ATCG
    - A: Adenine
    - T: Thymine
    - G: Guanine
    - C: Cytosine
  - A is always paired with T, G always with C
  - A sequence just looks at one strand in the helix (one side of the ladder)
  - Coding sequence (CDS) regions: base pair triplets that encode amino acids, grouped consecutively to specify proteins
  - Non-coding regions: structure, gene expression, RNA, etc
- Dataset: National Center for Biotechnology Information (NCBI) RefSeq Escherichia coli K-12 MG1655
- Why E. Coli? It only has one chromosome and is small (4.6 million base pairs) compared with animal DNA (humans have ~3 billion base pairs and a couple dozen chromosomes), but large enough to find interesting structure (hopefully)

[Back to Top](#applied-mathematics-5300-project)

##  Artifacts
[Exploratory Data Analysis](ecoli_dna_eda.ipynb)
- Signal Wavelet Notebooks
  - GC Haar Wavelets Analysis (**TBD**)
  - [Adenine Haar Wavelets Analysis](wavelets_a_analysis.ipynb)
  - Guanine Haar Wavelets Analysis (**TBD**)
- Powerpoint Presentation (**TBD**)

[Back to Top](#applied-mathematics-5300-project)

##  Presentation Layout
Powerpoint Plan
  Intro
  What are Wavelets?
    -Types of wavelets
    -Wavelet general equation
    -How they are used
  How we applied them
    -Basic DNA info - how we look at DNA as a signal
    -Create a graphic showing what we’re doing
  Our results 
    -Individual signal results
      -Power log quantification
      -Our quantitative results vs analytical
 
  -Comparison between A and G


##  Team
- Advisor: Dr. Joris Roos (Joris_Roos@uml.edu)
- Sam Sprangel (Samuel_Sprangel@student.uml.edu)
- Dan McGonigle (Daniel_McGonigle1@student.uml.edu)

[Back to Top](#applied-mathematics-5300-project)
