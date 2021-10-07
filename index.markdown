---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

### About the course

This online course was created during the pandemic and designed specifically for the set of University of Zurich students that enrolled in Autumn 2020. Besides the swirl courses, the course consists of a number of accompanying videos that introduce some of the most relevant concepts as well as the data used in the swirl lessons. You can find the videos [here](https://tube.switch.ch/channels/f6786b32 ) – as you will see, these videos were thought only for being used within that specific course. They will be renewed soon, but for now we appreciate your understanding… And we hope you get a laugh with them!

### Overview

In this swirl course you will learn the basics of the programming language R and will apply it to the computational analysis of language and text, including text mining, regular expressions and data cleaning, analysis and visualisation. The goal of this course is twofold: 
1. To learn how to digitally obtain different kinds of information from large quantities of texts, and 
2. To learn how to digitally clean, analyse and visualise data. 
While the examples used will most often be applied to linguistics, all the techniques are applicable to literary analysis.

Some of the skills that we'll learn are:
1. Basics of R programming language.
2. Basic data analysis and data visualization with the "tidyverse".
3. Calculating some basic data of a text: how many words/sentences/n-grams does it have? Which are the most frequent ones?
4. Designing and searching regular expressions.
5. Automatic anguage recognition.
6. Basic lemmatization of a text.
7. Topic modelling and sentiment analysis.

We will analyse different kinds of texts: literary texts, tweets, Whatsapp chats…

### Program 
The classes in the swirl course and the acoompanying videos are grouped into thematic blocks. Here you can see which video goes with which course.

### How to get set for the course

#### R

In this course we're going to learn how to use the R programming language for textual analysis. For that we need to install R ([MacOS](https://cran.r-project.org/bin/macosx/) / [Windows]( https://cran.r-project.org/bin/windows/base/)). Because we will work with an editor that will make our life easier and our work prettier, we will also need to install [RStudio](https://www.rstudio.com/products/rstudio/download/).

#### swirl

For this course you will also need to install swirl. It is an R library for teaching and learning R programming. It is interactive and very easy to use. Once you have R and RStudio installed and running in your computer, you can intall swirl() easily. Go to [swirl's website](https://swirlstats.com/students.html) and follow the steps that are listed there.

Once installed, the console in R will start "talking to you" – follow the instructions there. It will ask you for a name and it will offer you some courses already. The course you want to attend ist called "Tools for text analysis". So simply follow the instructions to download and follow the course!

Go to the [swirl help page](https://swirlstats.com/help.html) if you need more information or check out the [course forum](https://github.com/swirlTA/Tools_for_text_analysis/issues).

### Are you new to R?

#### Running the code

To run a line of code, press ctrl + enter (Windows) or cmd + return (Mac) while the cursor is placed anywhere in that line.
If you want to run only a part of a line or serveral lines, simply select them first and then press the same keyboard shortcuts.

#### The assignment arrow

Press alt + - (Windows) or option + - (Mac). Trust me, you want to get used to this shortcut as fast as possible :)

#### Attempt completion 

To get suggestions for completing a function or variable name that you already started writing, press the Tab (both in Windows and Mac).

#### Paired signs

RStudio will write the first and last element of a paired sign (like parentheses, quotation marks and brackets) and place your cursor inside. This is great but takes time getting used to.

#### Installing libraries

Please install the tidyverse and the swirl packages right away, you'll need them all the time! Note the quotation marks in the code:

```
install.packages("tidyverse")
install.packages("swirl")
```

The installed packages do not normally need to be reinstalled, unless you want to update them. However, you will have to update swirl fairly often, because I will be adding new lessons.

#### Loading libraries

Libraries, on the contrary, must be loaded everytime you start a new session in RStudio/R. (Quotations are not needed here, but are also possible.)

```
library(tidyverse)
library(swirl)
```

#### Installing swirl courses

When you open swirl for the first time, it offers you some preloeaded courses (after asking for your name… every time, sorry about that). We'll be using one of them, the R Programming course.
However, we will also be using courses designed by me, that you'll have to install from github. This is the code you'll need (note that the package swirl needs to be loaded, because the ``install_course_github()`` function is found in that package):

```
library(swirl)
install_course_github(
  "Carlotadbm", 
  "Tools_for_text_analysis")
swirl() #to begin
```

Sometimes swirl doesn't offer you the preloaded courses, maybe because it detected that you had installed another course and thinks you're over them… I don't know exactly why, but it happens. Anyway, you can easily install the R programming course from github too, with the following code:

```
install_course_github(
  "seankross", 
  "R_programming")
```

***Try it out… and enjoy!***

![swirl screenshot](/img/swirl_intro.jpg)

### Course forum

You can post questions or difficulties you have in this [forum](https://github.com/swirlTA/Tools_for_text_analysis/issues). Some general difficulties and issues have already been discussed so you might find the solution to your personal problem there. Keep in mind that this is a public GitHub repository so restrain from sharing personal information (like private email adresses).  


### Downloads
For some classes in the swirl course you need .csv or .txt archives. Click on the download button to get them.
