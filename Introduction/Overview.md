# Overview - Introduction

![](data-science-tools.png)  

### Data Manipulation

- **Import:** taking data stored in a file, database, or API and loading it into a data frame.
- **Tidy:** Storing the data into a consistent form matching the semantics of the dataset with the way it is stored (each column is a variable, each row is an observation). Tidy data ensures focus is towards questions about the data not fighting the data structure.
- **Transform:** Creating new variables that are functions of existing variables and calculating summary statistics to narrow in on observations of interest.
- **Wrangling:** Commonly used when referring to importing + tidying + transforming data.

### Knowledge Generation

- **Visualize:** Can provide unexpected insight or raise new questions about the data. May also hint that you are asking the wrong questions or need to collect different data. Does not scale well as it needs a human to interpret.
- **Model:** Complementary to visualizations, requires precise questions and assumptions. Does not question its assumptions so it cannot fundamentally surprise you. Mathematical/computational (usually scalable).

### Important Qualities

- **Communicate:** Critical part of any project. Visualizations + models mean nothing if you can't communicate the results to others.
- **Programming:** Allows you to automate common tasks and solve new problems with greater ease.

# What is missing from this book?

- **Big data:** With care, the tools found in this book can handle datasets up to 1-2Gb. For larger data (10-100Gb) you should learn more about [data.table](https://github.com/Rdatatable/data.table). Work considering if big data problem may be a small data problem in disguise. As in, data needed to answer a specific questions is small.
- **Other programming languages:** Data science teams use multiple languages, but it is best to master one tool (language) at a time. R is great as it is an environment designed from the ground up to support data science.
- **Non-rectangular data:** Images, sounds, trees, and text...
- **Hypothesis confirmation:** Book focuses on hypothesis generation (data exploration). Compliment to this is hypothesis confirmation. Confirmation is hard as you need a precise mathematical model and a preregistered analysis plan. 

# Prereqs
- Download R (https://cloud.r-project.org/)
- Download RStudio (http://www.rstudio.com/download)


