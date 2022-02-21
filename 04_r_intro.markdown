---
layout: page
title: R-intro
permalink: /r-intro/
---

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

![swirl screenshot](../pictures/swirl_intro.png)
