---
title: 'How Not to be Wrong About AI'
teaching: 20
exercises: 10
---

:::::::::::::::::::::::::::::::::::::: questions

- Why are most claims about the impact of AI on productivity not reliable?
- What methods would be more reliable?
- What can we practically do in a classroom setting?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Explain why obvious measures of programming productivity are misleading.
- Describe how standard scientific research methods could provide less ambitious but more reliable answers.
- Explore a practical alternative to those methods that can be used in the classroom.

::::::::::::::::::::::::::::::::::::::::::::::::

<!-- add links please --->

In 2023, GitHub announced their tools made developers 55% faster [Peng2023].
That number appeared in every executive presentation for a year.
This episode teaches you how to tell if you should believe it or not.

## Evaluating Claims

Claims can be evaluated from several angles:

* **Conclusion validity**: Was the sample large enough? Are effect sizes reported?
* **Internal validity**: Was there a control group? Was assignment random? Could novelty or learning effects explain the result?
* **Construct validity**: Does the measurement actually capture the claim?
* **External validity**: Who are the subjects, and are they representative of the population the conclusions address?

This is all Research Methods 101, particularly for people in disciplines like psychology or medicine. However, most undergraduate programs in computer science don't teach research methods, so most programmers don't even know what they don't know. At the same time, most organizations (even ones staffed by scientists) don't have the time or funding to look at themselves this carefully.

## Why Productivity is Hard to Define

Manufacturing productivity means widgets per hour: both terms are measurable.
But software output is not homogeneous: a ten-line bugfix may be worth more than a thousand-line feature.
An entire book basically says "measuring programmers' productivity is really hard" over and over again [Sadowski2019].
One reason is that much of software work is invisible: a field study found developers only spend 25% of their day actually writing code [Meyer2017].
Reading, reviewing, and helping colleagues doesn't show up in simple metrics.

The first question we need to ask is whether the measurement actually capture the concept?
Lines of code written per day fails this test: you can write more lines by making code worse.
Most other simple measures fail as well, but that doesn't stop companies from publishing claims based on them:

* Timing artificial tasks: a 90-minute greenfield task (i.e., one that starts with an empty file and builds something from scratch) does not predict real work, which almost always involves understanding and modifying existing code.
* Measuring only the easy half: AI makes code generation faster, but doesn't count review time, debugging confidently wrong suggestions, and security vulnerabilities.
* Before/after measures with no control group: you cannot separate the effect of AI from the effects of other things that changed (such as hiring new team members, changes to infrastructure, etc.).
* Asking developers if they feel more productive: feeling productive is not the same as being productive, and the **novelty effect** inflates self-reports for weeks.
* Comparing people who volunteer to try a new tool or technique to those who do not: early adopters are usually already higher performers, and again, the novelty effect produces misleading results on a timescale of weeks.

## Minimum Viable Rigour

So what *can* we tell about the impact of AI?
One place to look for an answer is User Experience (UX) research, which has also had to deal with a myriad confounding factors, accelerated timescales, and the need to find something actionable. UX researchers sometimes distinguish two kinds of evaluation:

- **Formative evaluation** means studying something in order to improve it. This can be done effectively with small samples, rapid iteration, and a qualitative focus; "what is wrong?" not "how often?"

- **Summative evaluation** is the assessment of whether something works in general. It requires more participants, controlled conditions, and quantitative metrics.

You may have identified parallels to the distinction between formative and summative evaluation for assessing learning.
User experience groups in industry use the term "guerilla research" for formative evaluation, and have developed rough-and-ready techniques for getting *something* useful with the time and resources they have.
For example, [Nielsen1993] found that a think-aloud session with five participants is typically enough to identify most problems in a specific workflow for a specific user group.

## In the Classroom

As instructors, you have the opportunity to run a formative evaluation session each time you teach with AI coding tools.
For example, you could ask learners to verbalize their thoughts as they work: _"say out loud whatever you are thinking"_.
It is most useful to do this on a concrete task, not open exploration, so that you and learners can compare experiences, and so that there is a direction or purpose to the learner's thinking.
For example, you could tell learners, _"Given this pull request, use the AI assistant to write a one-paragraph summary of the changes."_
When you are doing this:

* Pay particular attention to where participants hesitate, backtrack, or state expectations that turn out to be wrong.
* Do not help when they get stuck: you want to observe their reasoning process before trying to extend or correct it.
* Summarize observations at the end and have other learners compare with their own experience.

::::::::::::::::::::::::::::::::::::::::::::::::: discussion

### Practicing This Exercise

Work in groups of 3.
One person builds a script to find duplicate files (i.e., files with identical content but different names) in or below a directory (searching recursively) - the motivation is that it will be used to detect redundant copies of datasets.
They use an AI coding assistant while thinking aloud for at most 5 minutes. The others watch and take notes.

At the end, compare the observers' notes to each other and to the subject's recollection of what they thought they were doing.

What would you tell the next person to do (in particular, to do differently) based on what you observed?

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: keypoints

- There is no generally-accepted way to measure the productivity of programmers, which makes measuring the impact of AI on productivity problematic.
- Most of the claims being made about AI's impact would not pass scrutiny in an introductory course on research methods.
- Guerilla research methods used by User Experience researchers, such as think-aloud protocols, can reveal opportunities for improvement in specific workflows for specific users.

::::::::::::::::::::::::::::::::::::::::::::::::

