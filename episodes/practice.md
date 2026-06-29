---
title: 'Building Skill with Practice'
teaching: 10
exercises: 25
---

:::::::::::::::::::::::::::::::::::::: questions 

- What are the implications of genAI tool use for guided practice among novice learners?
- How good are current genAI tools at producing solutions to the exercises in Carpentries lessons?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Explore the capabilities of genAI tools in the context of Carpentries lessons.
- Discuss how genAI tool use could impact skill acquisition for novice learners.
- Discuss how widespread use of genAI tools for code generation might affect the relative importance of the skills we teach.

::::::::::::::::::::::::::::::::::::::::::::::::

[Guided practice is a central principle in Carpentries Instructor Training](https://carpentries.github.io/instructor-training/02-practice-learning.html#the-carpentries-pedagogical-model).
We provide learners with guided practice during a workshop and equip them with sufficient expertise to continue guiding their own practice after they leave.
Novices need this initial guided instruction because they do not have sufficient expertise to know what they do not know or to articulate what they want to do.

GenAI chatbots may be unhelpful to novices who want to learn a new topic because:

* They may produce responses that [do not account for the learner's lack of expertise](https://carpentries.github.io/instructor-training/04-expertise.html#switching-language).
* They often over-cater to the prompt they were given: providing additional information, taking additional steps, and suggesting next steps that may be jumping too far ahead.
* They can reliably generate correct snippets of code, including solutions to most if not all of the exercises in our lessons.

However, novices are unable to assess the quality of a generated solution.
Are there other ways that they could be encouraged to use genAI tools, to better support their learning?

::::::::::::::::::::::::::::::::::::: challenge

### How Good is GenAI at Solving Carpentries Exercises?

Choose one of the suggested lessons in the spoiler below. 
Try passing the text of some of the exercises from your chosen lesson to [duck.ai](https://duck.ai/) or another genAI chatbot of your choice. 

- How many exercises from the lesson was the chatbot able to solve?
- Did you find any exercises that the chatbot could not solve?

When reporting your results, include details of any custom settings you used on the chatbot. 
How might those have affected the output you received?
Similarly, did you need to provide any additional information to the chatbot? E.g. upload example data, paste extra content from elsewhere in the episode, etc.

::::::::::::::::::::::::::: spoiler

### Suggested Lessons

General notes: 

- At the time of writing, some chatbots do not support uploading of csv files (e.g. duck.ai). For lessons with csv datasets, you could try describing the dataset, pasting in the first several lines of data, or using a chatbot that supports csv uploads (e.g. Claude.ai).
- Some lessons don't work well for this exercise because they require more specialized set-up than there is time available for this exercise. However, many exercises in these lessons can still be completed by genAI tools once the setup is accomplished. If you have extra time, feel free to test them, and think about whether an additional steps you needed to take could realistically be expected of learners in a workshop.

The following lessons work well for this exercise: 

- Data Carpentry:
	- [Data Analysis and Visualization in R for Ecologists](https://datacarpentry.github.io/R-ecology-lesson/)
	- [Data Analysis and Visualization in Python for Ecologists](https://datacarpentry.github.io/python-ecology-lesson/)
	- [Análysis y visualización de datos usando Python](https://datacarpentry.github.io/python-ecology-lesson-es/)
	- [Project Organization and Management for Genomics](https://datacarpentry.github.io/organization-genomics/)
	- [Introduction to R for Geospatial Data](https://datacarpentry.github.io/r-intro-geospatial/)

- Library Carpentry: 
	- [Introduction to Regular Expressions](https://librarycarpentry.github.io/lc-data-intro/)
	- [The Unix Shell](https://librarycarpentry.github.io/lc-shell/)

- Software Carpentry: 
	- [The Unix Shell](https://swcarpentry.github.io/shell-novice/)
	- [Version Control with Git](https://swcarpentry.github.io/git-novice/)
	- [Programming with Python](https://swcarpentry.github.io/python-novice-inflammation/)
	- [Plotting and Programming in Python](https://swcarpentry.github.io/python-novice-gapminder/) - after the first episode.
	- [Programming with R](https://swcarpentry.github.io/r-novice-inflammation/)
	- [R for Reproducible Scientific Analysis](https://swcarpentry.github.io/r-novice-gapminder/)

- HPC Carpentry:
    - [HPC Workflow Management with Snakemake](https://carpentries-incubator.github.io/hpc-workflows/)
 

The following lessons don't work as well for this exercise: 

- Data Carpentry:
	- [Foundations of Astronomical Data Science](https://datacarpentry.github.io/astronomy-python/)
	- [Data Organization in Spreadsheets for Ecologists](https://datacarpentry.github.io/spreadsheet-ecology-lesson/)
	- [Data Organization in Spreadsheets for Social Scientists](Data Organization in Spreadsheets for Social Scientists)]
	- [Data Cleaning with OpenRefine for Ecologists](https://datacarpentry.github.io/OpenRefine-ecology-lesson/)
	- [Data Cleaning with OpenRefine for Social Scientists](https://datacarpentry.github.io/openrefine-socialsci/)
	- [Introduction to the Command Line for Genomics](https://datacarpentry.github.io/shell-genomics/)
	- [Data Wrangling and Processing for Genomics](https://datacarpentry.github.io/wrangling-genomics)
	- [Introduction to Cloud Computing for Genomics](https://datacarpentry.github.io/cloud-genomics/)
	- [Introduction to Geospatial Concepts](https://datacarpentry.github.io/organization-geospatial/)
	- [Introduction to Geospatial Raster and Vector Data with R](https://datacarpentry.github.io/r-raster-vector-geospatial/)

- Library Carpentry: 
	- [Tidy data for librarians](https://librarycarpentry.github.io/lc-spreadsheets/)
	- [OpenRefine](https://librarycarpentry.github.io/lc-open-refine/)
	- [Introduction to Git](https://librarycarpentry.github.io/lc-git/)

- HPC Carpentry: 
	- [Introduction to High-Performance Computing](https://carpentries-incubator.github.io/hpc-intro/)

:::::::::::::::::::::::::::::::::::::


::::::::::::::::::::::::::::::::::::::::::::::::


The above exercise has demonstrated that chatbots will often provide correct responses to the types of challenges we pose to learners during our workshops.
We might also wonder how consistent these responses are - in other words, if all the learners in your workshop enter the same prompt, will they reliably receive the same answer?
Does that depend on whether everyone is using the same genAI tool? 

::::::::::::::::::::::::::::::::::::: challenge

### How Consistent are GenAI Answers?


Copy the following prompt into your genAI chatbot of choice. 

```markdown
In bash how would you write a loop that echoes all 10 numbers from 0 to 9?
```

Share your results in the Etherpad, along with information about the tool and model you used.

- How many different responses were provided?
- How many of the responses were correct?
- Were the correct responses all useful for novices?

For comparison, the solution provided in the [Software Carpentry Unix Shell lesson](https://swcarpentry.github.io/shell-novice/) is: 

```bash
$ for loop_variable in 0 1 2 3 4 5 6 7 8 9
> do
>     echo $loop_variable
> done
```

::::::::::::::::::::::::::: solution

Some responses obtained might be: 

```bash
$ for i in {0..9}; do
>    echo "$i"
> done
```

The two examples below are quite similar to one another, but differ in whether quotation marks are placed around the variable.

```bash
$ for ((i=0; i<10; i++)); do
>    echo "$i"
> done
```

```bash
$ for ((i=0; i<10; i++)); do
>  echo $i
> done
```

The example below will only work if the learner has initiated the bash program (or zsh or similar) in their terminal.

```bash
$ i=0
> while [ $i -lt 10 ]; do
>  echo $i
>  ((i++))
> done
```

```bash
$ for i in $(seq 0 9); do
>  echo $i
> done
```

The example below assumes the learner is writing a shell script, rather than working interactively within the terminal. 

```bash
#!/bin/bash

for i in {0..9}; do
	echo "$i"
done
```

:::::::::::::::::::::::::::::::::::::


::::::::::::::::::::::::::::::::::::::::::::::::

We've demonstrated that chatbots are able to generate correct solutions for many Carpentries-style exercises, but that the responses generated are not consistent.
Not only are they not consistent, but each example above introduces new pieces of syntax that haven't been covered in the lesson yet. 
We will discuss more the challenges this can cause with cognitive load later in this training. 


::::::::::::::::::::::::::::::::::::::::::::::::: discussion

### What Does This Change?
How does the ability of genAI tools to generate source code influence the relative importance of the following different skills to a novice learning to program?

* Writing a syntactically valid for loop.
* Tracing the order of execution.
* Choosing descriptive names for variables.
* Debugging, e.g., interpreting error messages.

Referring back to your answers, what is one approach you could take as an Instructor during a workshop to (de)emphasise the importance of one or more of the skills listed above?

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::::: challenge

### How Much Expertise Do You Need?
Prompt your chatbot with a coding task.
You can choose an exercise from a lesson (Carpentries or otherwise), or come up with your own task. 
Consider the output produced: How much knowledge of programming concepts do you think you would need to have to be able to understand or validate what the output is doing?

On this chart (FIXME: add link to tldraw chart), mark your result based on your judgement of how complex your coding task was and how much expertise would be needed to understand the response.

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::



::::::::::::::::::::::::::::::::::::: keypoints 

- Novices using chatbots in a workshop are less likely to benefit from guided practice.
- Current chatbot tools can produce functioning solutions to many exercises in Carpentries lessons.

::::::::::::::::::::::::::::::::::::::::::::::::

