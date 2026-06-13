---
title: 'Memory and Cognitive Load'
teaching: 10
exercises: 45
---

:::::::::::::::::::::::::::::::::::::: questions 

- How could learners' use of chatbots influence considerations of cognitive load in a workshop?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Assess the suitability of chatbot responses to a novice learner's understanding.
- Articulate a personal view of what chatbot use should be encouraged in a workshop.

::::::::::::::::::::::::::::::::::::::::::::::::

Sweller’s model describes three categories of cognitive load: intrinsic, germane, and extraneous.
Our goal as Instructors (and Lesson Developers) is to eliminate extraneous cognitive load. 
But intrinsic and germane cognitive load remain. 
That is, some cognitive load is unavoidable and essential for learning.
This is desirable cognitive load, but the friction can feel difficult for learners.

GenAI tools offer a tempting alternative, giving learners the opportunity for “cognitive offloading”. 
But if this eliminates or reduces germane cognitive load, the learner is less likely to retain the relevant information required for learning.

Similarly, and referring back to the previous episode, if they offload parts of the process that promote learning, they will benefit very little from participating in the workshop.
Exercises are a great example: 
practicing new skills and applying new concepts facilitates the transfer of this information from learners' working memory to their long-term memory.
Completion of exercises also promotes metacognition: a learner's awareness that they are learning, which itself promotes further learning.
If learners feed the exercises straight into a chatbot, they are much less likely to learn what is being taught.

Carpentries lessons and the exercises within them have been carefully designed to help Instructors manage learners’ cognitive load throughout a workshop.
In many cases, there will be more than one possible way to solve an exercise.
But learners cannot be expected to be have all of the conceptual knowledge required to devise some of these possible solutions.

For example, a Python exercise might be solved in one line with a list comprehension or a lambda function, but the lesson uses neither because a more easily interpretable solution is required for novice learners.

:::::::::::::::::::::::::::::::::::::::::::::::::: challenge

### Chatbot Responses and Cognitive Load
Refer back to an earlier exercise, where you tried to solve an exercise from one of our lessons with a chatbot. 
Consider the code that the chatbot produced.

* What strengths and weaknesses do you observe in the chatbot’s solutions?
* What reasoning are you using to evaluate or classify them?
* Would a novice learner be able to use the same reasoning to evaluate the response?
* Does the solution produced by the chatbot include additional complexity, concepts, etc that could be distracting (introducing extraneous cognitive load) for a novice learner?

::::::::::::::::::::::::: hint

An example, using an exercise [in the Software Carpentry Programming with R lesson](https://swcarpentry.github.io/r-novice-inflammation/04-cond.html):

> Write a function `plot_dist` that plots a boxplot if the length of the vector is greater than a specified threshold and a stripchart otherwise.
> To do this you'll use the R functions `boxplot` and `stripchart`.

The solution provided in the lesson:

```R
plot_dist <- function(x, threshold) {
  if (length(x) > threshold) {
    boxplot(x)
  } else {
    stripchart(x)
  }
}
```

A solution produced by duck.ai:

```R
plot_dist <- function(x, threshold = 30, main = NULL, xlab = NULL, ylab = NULL, ...) {
  if (!is.numeric(x)) stop("x must be numeric")
  if (is.null(main)) main <- deparse(substitute(x))
  if (is.null(xlab)) xlab <- ""
  if (is.null(ylab)) ylab <- ""
  n <- length(x)
  if (n > threshold) {
    boxplot(x, main = main, xlab = xlab, ylab = ylab, ...)
  } else {
    stripchart(x, method = "jitter", vertical = TRUE, pch = 16,
    main = main, xlab = xlab, ylab = ylab, ...)
  }
}

```

::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::::: discussion

### Chatbot Responses and Cognitive Load, Continued
Now try repeating the same prompt used above, but add 

> I am a novice learning to program for the first time.

What effect, if any, did this have on the complexity of the solution produced?
If the response is still too complex, can you adjust the prompt further to make it more helpful to a novice?

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::::: discussion

### Copy-Paste vs Peeking at the Solution
Several of our exercises have been concerned with learners copy/pasting exercises to produce solutions with a chatbot.
However, our lessons are publicly and freely available to visit online, and many exercises on these pages include solutions. 
In your opinion, what if any difference is there between a learner pasting the text of an exercise into a chatbot and trying out the code that is produced in response, and the learner expanding the solution box on the lesson webpage and pasting the code they find there into their environment?

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::::: discussion

### What is Acceptable?
**Think**: take a few minutes to think about your answer to the following questions:

* Is it possible for novice learners to use a genAI chatbot in a workshop, without threatening their ability to learn the skills we aim to teach? 
* If so, what would that use look like?

Make some notes, then **pair** with a partner.
Compare your answers, and discuss any points where you disagree.

Finally, **share** the key points of your discussion with the rest of the group. 
Did you reach a consensus?
If not, on what points did you disagree?

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: keypoints 

- Chatbot use that removes germane cognitive load may impede learning.

::::::::::::::::::::::::::::::::::::::::::::::::

