---
layout: post
title: What is R
---

What is R
---------

R is a programming language that was originally thought for statistical
and data analysis, but it has grown to be able to do much more. It can
handle and store data; perform all sort of calculations (also on arrays,
such as matrices or vectors); visualise and plot data. It is free
software and open source! Anyone can collaborate, create something new
and integrate it in R. R allows users to add additional functionalities
(defining new functions) and can be extended (easily) via packages. You
can most likely find a package designed to suit whatever new needs you
came up with! Try and google it! The core functionalities of R are
typically referred to as “base R”. In this course, we will deviate from
base R syntax in many regards, because we will be mostly relying on the
tidyverse, i.e. a collection of packages with a coherent syntax that
focuses on the idea of tidy data \[link to tidy data when we have it\].
However, the basics of R syntax is common to both programming styles, so
let’s briefly discuss them. Because we are linguists and we are
discussing a (programming) language, we can use some metaphors to easily
grasp what we are talking about.

Data types
----------

Natural languages have different word classes (nouns, verbs,
adjectives…) and R has different data types. The three most important
types that you need to know are character, numerical and boolean.
Character elements must be introduced by quotes. Everything that is
within a pair of quotes is one single character element, which means
that in the following example there are three character elements, even
if there are five words.

    "Hello"

    ## [1] "Hello"

    "there"

    ## [1] "there"

    "this is Carlota"

    ## [1] "this is Carlota"

Numeric elements can be either real or decimal (and R calls them
different, so your numeric elements can actually be of the integer type,
the numeric type or the double type, but this is not too relevant for
us!). These must not be introduced by quotes.

    1

    ## [1] 1

    2.13

    ## [1] 2.13

    865473846823

    ## [1] 865473846823

You can also treat numbers as character, as long as they are within
quotes. Compare

    '1' + '1'

with

    1 + 1

    ## [1] 2

R cannot add character elements, but for sure it can add numerical
elements!

Logical elements (or boolean elements in the statistical literature) are
basically binary data types: one value is TRUE and the other one is
FALSE. So they are basically answers to questions. I know this sounds a
bit weird right now, but you’ll understand it better when we start using
them. They can be abbreviated to T and F.

    TRUE

    ## [1] TRUE

    T

    ## [1] TRUE

    FALSE

    ## [1] FALSE

    F

    ## [1] FALSE

Data structures
---------------

Data structures are more complex structures that combine different types
of data types, so in a way they are similar to phrase-level elements in
natural languages. We have unidimensional data structures, such as
vectors and lists, and bidimensional data structures, such as data
frames and matrices.

Vectors are a collection of elements of the same data type and we build
them using the function `c()` (more on functions later). Each element
must be separated by commas.

    c("Hello", "there", "this is Carlota")

    ## [1] "Hello"           "there"           "this is Carlota"

    c(1, 2, 3, 3.141596)

    ## [1] 1.000000 2.000000 3.000000 3.141596

Lists are a collection of elements of different data types (or even a
collection of vectors). We build them through the function `list()`.
They are more complicated to handle and we will be using mostly vectors,
but lists will come up eventually.

    list("Hello", 2, 3, "there", T, "this is Carlota", 1, 3.141596, FALSE)

Matrices and data frames have dimensions: the number of rows and
columns. In everyday language we would normally call them tables, but
incidentally “table” is also an R data type… (Don’t worry about it.)
While matrices have elements of the same data type, data frames have
elements of different types. We will be using almost exclusively the
latter. Every column of a data frame is a… vector! (Or a list.)

Missing data
------------

Missing data are handled in a special way in R. They are represented as
NA. They can appear in all the data structures we covered. We will deal
with them in the course :)

Variables
---------

Variables are like proper nouns in a way. Whenever we want to store an
element in R we need to give it a name. Variables are sequences of
alphanumerical characters that are not within quotes! Variable names
cannot: 1) start by a number, 2) contain - + / \*. Variables name,
however, can contain . \_ Also, it’s probably for the best if you do not
use special characters in your variable names (á ñ ü).

We assign names through the arrow operator:

    two <- 2

Now you can use two to call 2 (which is not very useful, but that’s
because the variable we created is not very complex!) I promise this
will be tremendously useful.

    two + 3

    ## [1] 5

Functions
---------

Functions are pretty much like verbs. They even have arguments! A
function is an instruction to perform a specific task. Functions have
arguments, which specify on which element you need to perform the
instructions (the subject?) and some other requirements (objects and
adjuncts!). This metaphor is great. Arguments have a default order, but
they also have names, that we use when we don’t want to follow the
default order (or when we are not sure about it).

    mean(c(two, 3)) #The function mean() takes a numeric vector

    ## [1] 2.5

    log(3, 2) #The function log() takes the numeric vector for which the logarithm is computed and as its first argument and a positive number which defines the base of the logarithm as the second one. (If you don't remember what a logarithm is, don't worry! This is just an example)

    ## [1] 1.584963

You can check the arguments of a function by calling the help file
(which will appear in the the bottom right window in RStudio).

    ?mean

Some things to keep in mind
---------------------------

1.  In R, lower-case and upper-case letters MATTER.

<!-- -->

    "Carlota" == "carlota"

    ## [1] FALSE

1.  In R, spaces don’t normally matter…

<!-- -->

    mean( c(2, 3 ) )

    ## [1] 2.5

    mean( c(2, 3))

    ## [1] 2.5

    mean(c(2,3 ) )

    ## [1] 2.5

    mean(c(2, 3))

    ## [1] 2.5

…unless they are inside a name or an element):

    "Carlota"  == "Ca rlota"
    t wo <- 2

1.  In R, whatever that is found after the hash (\#) is ignored: it is
    used to write comments. You’ve seen a few examples of this above.
    Comments are crucial to document what you’re doing, that is, to
    explain to yourself (and to others) what you’re doing. It’s
    sometimes boring to keep track of everything on the comments, but it
    is so easy to forget what the code is supposed to mean that your
    future self will thank your present commenting self. I really
    recommend you start using them right away to explain what you’re
    doing!

Keep calm…
----------

You might have found this a lot already. Trust me: you will get the
grasp of it much faster than you think! I recommend that you do a few of
the starting swirl lessons from the R Programming
[course](https://swirlta.github.io/toolsfortextanalysis/program/) in
order to practice these concepts a bit. You might not see the point of
all this at first, because this is like learning inflectional morphology
of a new language. A bit boring and useless unless you can build
sentences! But you can also try and start building sentences right away
by starting with our course first. I still think is a good idea that you
do the basic courses at some point, but you’ll might find more
motivation if you shuffle the order :)

\#\#…and ask for help

When you learn a language, you make mistakes all the time. In natural
languages, mistakes do not necessarily prevent communication, because
the hearer is collaborative (and a nice person). In programming
languages, mistakes make communication fail, because computers are…
quite dumb, actually. They have no idea about Gricean rules or anything
similar.

So what to do if our code is not working? 1) Read the error message R
gives you. You might not understand most of what it says, but you’ll get
better at it. It will give you a clue about where to look. 2) Most
mistakes in your code (especially at the beginning) will be typos: is
there a comma missing? Are all brackets and quotation signs closed (and
where they should be)? Did you use a capital letter where you shouldn’t?
Is everything spelled correctly? Did you run your previous code or
simply write it on the script? 3) Sometimes it’s hard to find the typos
– it helps if someone else looks at it. 4) Grammatical mistakes: maybe
your syntax is wrong, are you sure you’re using that function right? 5)
Run ?function() to get a help file. These files are not always easy to
read, but you’ll get better at it too! 6) If you can’t still figure it
out: just ask! We have a forum here! :) 7) Google it: copy your error
message or write what you were trying to do – there are lots of helpful
forums! You’ll also get used to understanding their answers.

Coding is a lot of fun, but it can also be a source of frustration…
Having someone going through the same process really helps a lot. Try to
convince a pal to do this course with you. Your motivation will be
better and you will find each other extremely helpful! And remember that
you can always ask me!
