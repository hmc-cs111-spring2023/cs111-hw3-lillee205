# Free project 1

## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

Creating a yearbook is a lot of design work, but the hardest part is undoubtedly
making sure that everyone is represented fairly. Currently, the yearbook staff
have to tag everyone in photos by hand (which is almost impossible given that
they don't know everybody in the school by face). Furthermore, there is an
uneven distribution of how many times each person shows up in the yearbook, as
well as the number of photos from each person (as the yearbook club takes photo
submissions from students). 

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

Having a DSL could automate a lot of the painful processes that the yearbook
staff have to go through. For example, one vague idea is that someone could
upload a library of photos and cycle through different enumerations of which
photos are included in the yearbook. Then, they can analyze the statistics on
which one has the best distribution of unique students. Having a function that
can help identify faces would also be useful.

### Why you?

_What excites you about this idea? How did you come up with it?_

I'm biased as the president of the yearbook club, but this is a common sentiment
expressed by all the members in the club. The current application that we use to
create the yearbook is rudimentary, to say the least. You can't even stretch
photos, even though it's supposed to act as a design site...

### Domain

_Describe the project's domain in five words._

Managing photos in the yearbook.

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

Since not all yearbook members are coders, it would be good to have an
easy-to-access GUI of some kind. Also, since the task of creating the yearbook
is very visual, having a GUI would be more helpful than not. I imagine that the
actual interface of it might look like a library of photos that you can then
perform certain operations on. There will also be some information available
about the entirety of the yearbook (such as how many people are currently
represented in the yearbook more than 2 times). Additionally, you could perhaps
have a parameter for the number of photos you want on a page, and then cycle
through the different possibilities. Then, you could choose the one which has
the best distribution of unique students. 

### Operation (semantics)

_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program runs, it should connect to Jostens (yearbook avenue) which is
where the yearbook is created. The idea is that the changes made through my
program should be uploaded to the site; this requires for there to be some kind
of "translation phase". 

Errors should be communicated through a graphical popup to match the GUI nature
of this project. 

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be able to get relevant statistics about how many times on average a
person shows up in the yearbook, how many people don't show up more than once,
etc. It should also be easy to select a photo and generate identifiers as to who
is in the photo. You shouldn't be able to edit the actual contents of the photo
itself or edit user data (like changing someone's grade/name). It will also
specifically only work with Jostens; compatability with other yearbook sites
will not be considered.

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are no DSLs directly related to yearbook creation. I tried looking up for
possible synonyms like magazine and zine, but nothing comes up. I would assume
there aren't any because yearbooks are something that only happen up to college,
and most people who develop DSLs are probably doing so for a) grad school b)
past grad school, so they don't fit the age range. 

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Unfortunately, while this idea appeals to me the most because it would save me a
*lot* of time, I'm not sure how suitable it is. I feel like there would be a lot
of technical work with extracting faces from a photo to tag identifiers, and
communicating with Jostens' site which feels like it came out a decade ago will
probably be painful. To downsize the difficulty, I could just focus on the
"cycle through different photos, see which combination gives the largest
diversity in the yearbook" but I'm worried that makes the scope too small... 

### Scope

_How big an idea is this? How ambitious is this project?_

Scope-wise, it is quite specific in its purpose of checking who is in the
yearbook and tagging people accordingly. So in terms of goals, I don't believe
it is too ambitious. 

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

It would be a good idea because it would directly benefit Harvey Mudd('s
yearbooks) but the technical details behind setting it all up might detract from
the language design aspect of the project. 
