# Interview project

## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

Unit testing is a very helpful tool that aids both students and professors
alike. It is especially useful when used in conjunction with Gradescope. This is
fairly simple to do with Racket and Java because Gradescope has modules specific
to these languages, but it does not support Racket. This makes CS60 grading more
tedious. Currently, Racket's unit testing prints out the results in a text
format, and it is parsed with Python into a Gradescope format, and then sent to
Gradescope. 

However, this process gets bogged down because it's just a lot of text
processing which makes the code cumbersome to read. Furthermore, there are
currently limitations with customizability (assigning a different amount of
points for each test case, for example). Additionally, it's apparently pretty
difficult to readjust point distribution after the autograder has already been
set up. I could create something that is more flexible and readable to assist
those working on the autograder for the CS department.

This doesn't need to necessarily just focus on the Racket issue; I could branch
out more by just making the autograder a more pleasant experience to use.

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

Having a more readable language for working with the autograder will make it
easier to work with. Eliminating the confusing regexes that try to parse the
Racket output and replacing it with more understandable functions will not only
help readability, but also allow for an easier debugging/customization feature
if in the future you want to edit it.

### Why you?

_What excites you about this idea? How did you come up with it?_

I work with Kevin Herrera frequently, who is in charge of the autograder and
also who I interviewed for this part of the homework. He often is working on the
autograder when I drop by his office so I understand that the autograder is a
cumbersome thing to deal with.

### Domain

_Describe the project's domain in five words._

Increasing autograder's flexibility and readability.

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

You would probably be working with the code files directly (since the autograder
is mostly used for coding aspects, we can assume that users will be proficient
enough with code that they feel comfortable writing in source
files). However, the DSL will ensure that they have an easy experience with
managing the autograder itself.

### Operation (semantics)


_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program runs, it should generate a Gradescope-parseable file that
summarizes the results of running the test cases, and then sent to Gradescope so
that the students can see it on their end.

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

You should basically only be able to work with the autograder; to do other
things would be kind of silly. It should hopefully be relatively simple to
switch from grading one language to another (Python -> Racket, for example)
since classes use a variety of different languages. 

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There's a whole github repo on the current autograder system but I don't think
it's public. The most admirable part is how it's pretty well documented; though
there are slightly unclear pieces of code, the overall intention behind the code
shines through nicely. It's just that parsing through a text file through regex
isn't the most clear, sometimes, and also the aforementioned issues with
inflexbility. 

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

### Scope

_How big an idea is this? How ambitious is this project?_

I think limiting it to the scope of just the autograder isn't too bad,
especially if we choose to focus on only a few questions in the beginning. 

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

This might be a good idea because it has relevance to me personally and others
at Mudd. It already has pre-existing work which would be valuable to draw on, as
well as easy access to a domain expert (Kevin Herrera). However, I think Kevin
might actually have me working on this for my job so I'm not sure if I'm
ethically allowed to be paid for my final project (in my defense, he mentioned
this after I said I wanted to interview him). 


### Interview notes
	
	* what frustrates you about auto grader
		* racket doesn't have integration w/ gradescope
		* in python, you can just run unit tests. available classes
		* gives you helpful text and results
			* can see which tests failed and which passed
			* catch only a certain type of test
		* gradescope expects things to be formatted a certain way so they have
		their own module called gradescope utils
			* you have your unit testing for python.
			* you weight the tests with "scores" and other attributes using
				gradescope util
	* racket has unit testing which is similar to python. racket actually spits
	out more info than python
		* it says you failed at this spot, this is what it was, etc
	* issue is that we can't link the tests accordingly to the one on gradescope
    * like unit testing because you can figure out stuff that you didn't
	  necessarily think of 
			
	* streamlines process
