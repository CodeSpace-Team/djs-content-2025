### Major Topics

- **State Machines**: A conceptual framework for managing complexity in applications by defining explicit, mutually exclusive states and transitions.
- **Complexity Management**: The challenge of keeping code understandable and maintainable, especially when adopting specific paradigms like functional programming, OOP, or state machines.
- **Paradigms and Dogmatism**: Discussion on the benefits and drawbacks of strictly adhering to a particular programming paradigm.
- **Team Consensus**: The importance of team agreement on using a paradigm to its extreme for coherence and effectiveness in development.
- **Transition Rules and States**: How state machines formalize the conditions under which transitions between states occur, ensuring predictability and control over application behavior.

### Minor Topics

- **Functional Programming and OOP**: Mentioned as paradigms for managing complexity, alongside state machines.
- **State Machine Examples**: Traffic lights, locks, elevators, and vending machines are provided as everyday examples of state machines.
- **Mathematical Model**: Highlighting state machines as a conceptual, rather than physical, framework rooted in mathematics.
- **Implicit vs. Explicit State Management**: Discussion on how implicit state management can lead to complexity and unpredictability, whereas explicit state management through state machines can make behavior more understandable and controlled.
- **State Charts and Diagrams**: Tools for visually representing state machines and their transitions to aid in understanding and designing system behavior.

By organizing these concepts into major and minor topics, it's easier to see the overarching themes of the lecture: the significance of state machines in managing application complexity, the careful consideration needed when adopting a programming paradigm, and the practicality of explicit state management for team coherence and code maintainability.




00:00:00.920
what I want to do now is take a couple
00:00:04.560
of steps back and have a like broad
00:00:07.919
theoretical look at this idea of State
00:00:10.260
machines and how they can actually help
00:00:13.500
us manage complexity in our apps similar
00:00:17.580
to the discussions we've had about
00:00:20.160
functional programming oop and various
00:00:24.359
paradigms I do find a lot of people out
00:00:27.240
there that are very dogmatic about it
00:00:29.099
and they try and model everything as a
00:00:32.279
state machine and I think similar to
00:00:34.440
functional programming and object
00:00:36.420
orientated programming if you try and
00:00:39.300
pursue a specific Paradigm for the sake
00:00:42.899
of the Paradigm itself I actually find
00:00:45.300
that your code becomes more cryptic it
00:00:47.640
becomes harder for someone to understand
00:00:49.640
and harder to actually reason about the
00:00:52.739
only caveat being is that if you are a
00:00:55.620
team and you say exclusively we are
00:00:58.800
gonna choose super extra stream
00:01:01.320
functional programming we are going to
00:01:03.899
do a super extreme State machine
00:01:07.560
approach if the entire team is in
00:01:10.500
agreement then I actually find it's
00:01:12.960
beneficial to really pursue one of these
00:01:15.840
paradigms in the extreme but Paradox is
00:01:19.860
that if there is not that agreement then
00:01:22.979
I often find that leaning too heavily
00:01:25.979
into a specific Paradigm actually makes
00:01:28.740
your code less readable and harder to
00:01:31.439
reason about because it requires a lot
00:01:34.080
of understanding about that specific
00:01:36.780
Paradigm as maintained you know so we
00:01:38.939
spoke about one plus one equals two and
00:01:41.400
how if you just understand some Basics
00:01:43.500
about mathematics like that is really
00:01:46.259
much more expressive so we get a lot of
00:01:48.479
like almost like easy wins by just
00:01:50.820
leaning into it slightly but for General
00:01:53.880
code I do feel that you can get a lot of
00:01:57.720
really easy wins from just like low
00:02:01.380
level very basic implementation of the
00:02:04.079
ideas and the deeper you go in and you
00:02:07.079
start getting a bit diminishing returns
00:02:09.720
but not only that if the rest of the
00:02:12.360
team isn't familiar with some of the
00:02:14.459
more higher level and deeper concepts
00:02:17.459
with within a specific Paradigm and I
00:02:20.459
find that it actually makes it much
00:02:22.500
harder to read and understand your code
00:02:25.020
and modify your code so with all of
00:02:27.300
these examples I find a lot of value in
00:02:30.120
just leaning into it very like trying to
00:02:33.120
take some of the good parts of it into
00:02:35.400
our own approach and kind of keeping our
00:02:38.160
own approach a little bit eclectic when
00:02:41.160
working within JavaScript if you're
00:02:43.260
working with Haskell or so forth you
00:02:45.000
don't have a choice you need to go full
00:02:47.040
on functional programming and the rest
00:02:49.080
of the team has to as well they don't
00:02:50.940
have a choice but in something like
00:02:52.560
JavaScript that is that open and dynamic
00:02:54.840
I find that I don't necessarily lean
00:02:57.959
into a specific approach all the way I
00:03:00.480
may be just lean a little bit in and try
00:03:03.660
and get some of the good parts of it
00:03:05.760
without requiring too much of an
00:03:08.280
understanding there are some specific
00:03:11.099
things where explicitly say this is a
00:03:13.260
hard concept to learn but it's going to
00:03:15.180
be so beneficial that I think we need to
00:03:17.519
force the team to make sure everyone
00:03:19.319
understands this so for example reduce I
00:03:21.900
often find that it's very hard for
00:03:23.280
people to learn reduce but the benefits
00:03:26.640
are amazing but in general
00:03:28.980
um I don't subscribe to full on leaning
00:03:32.519
into a paradigm to the extreme and state
00:03:35.340
machines are no different let us start
00:03:37.920
talking about State machines most
00:03:40.019
obvious example of a state machine is a
00:03:43.440
traffic light stay State machines are a
00:03:46.920
conceptual thing they're in our brain
00:03:49.319
they're not related to the actual
00:03:51.120
physical thing itself they're actually a
00:03:53.220
mathematical model let me show some
00:03:55.200
other examples of State machines and
00:03:57.000
show why these work by the principles of
00:04:00.239
a state machine so we have a traffic
00:04:02.640
light we have a like a lock we have an
00:04:05.640
elevator we have a vending machine these
00:04:07.500
are all state machines and so there are
00:04:09.480
State machines in so far that all of
00:04:11.819
them have mutually exclusive states
00:04:14.099
there isn't one Big Blob of mixed state
00:04:18.660
there's very clear spaces where it's now
00:04:20.940
it's in this state now it's in that
00:04:22.800
state in the example of the traffic
00:04:24.419
light it's in the raid State it's in the
00:04:27.180
yellow State and it's in the Green State
00:04:28.979
and there's very deliberate actions that
00:04:31.860
take it from one state to another state
00:04:34.440
and it can only go to a specific state
00:04:38.580
from another state so it can't go from
00:04:40.979
red to Yellow so State machines are
00:04:43.860
effectively formalized way of actually
00:04:47.460
expressing how State changes so you can
00:04:50.880
probably already see where this is
00:04:53.100
helpful when working with State and apps
00:04:55.620
as well so there's a lot of like
00:04:57.360
formalized ways to do state machines I
00:05:00.900
prefer to just like in the same as with
00:05:03.479
design patterns I prefer to just draw
00:05:06.120
inspiration from these approaches
00:05:08.699
instead of trying to superimpose them on
00:05:11.160
JavaScript because at some point you're
00:05:13.080
maybe going to start fighting against
00:05:15.240
the language itself the example that's
00:05:17.580
most often used when describing State
00:05:20.160
machines uh is a Turn Style so this type
00:05:24.240
of thing and so generally it's explained
00:05:26.759
as follows so there are two states in a
00:05:30.419
state one and let's call the other one
00:05:32.460
step two and usually I would just give
00:05:35.580
the I would just give the state ID or
00:05:38.940
something or type let's just go type
00:05:41.460
let's just say this is the log State
00:05:43.740
let's also just update and this is the
00:05:46.320
unlocked State both of these states and
00:05:48.539
this is also where there's a bit of
00:05:49.860
overlap between State machines and
00:05:51.720
polymorphism both of these states follow
00:05:54.900
the same shape type def object and let's
00:05:58.919
just say state so these are by means of
00:06:01.919
polymorphism actual implementations of
00:06:05.340
the same shape but just with different
00:06:07.500
data it has the type itself let's just
00:06:10.380
say it's a string and then it has a
00:06:12.660
callback let's just say it's just a
00:06:15.300
basic function on our and let's actually
00:06:18.000
just do that so let's just say you know
00:06:19.979
empty function so callback empty
00:06:22.500
function okay so we have an empty
00:06:24.300
function that is a push so if you try
00:06:28.139
and push the turnstile and then we have
00:06:30.180
another one that is insert coin this is
00:06:33.060
a push Turn Style so both of these by
00:06:36.060
means of polymorphism share that
00:06:38.639
that same base shape so both of these
00:06:41.940
are instances of state and so we have
00:06:45.419
type but then we also need push Turn
00:06:48.000
Style and we also need insert coin all
00:06:51.419
right so in the locked state if you push
00:06:54.000
the Turn Style nothing happens we can
00:06:56.880
maybe just throw new error is locked
00:07:00.780
okay okay so if you try and push it
00:07:02.400
nothing happens it's locked if you
00:07:04.259
insert a coin effectively we just I just
00:07:07.319
could have put a comment in here we
00:07:08.819
change to the unlock state in the unlock
00:07:11.819
state if you push the Turn Style we
00:07:14.160
change to the lock state so you go
00:07:16.680
through and it changes to the locked
00:07:19.020
state if you insert a coin then let's
00:07:21.300
say throw a new error already unlocked
00:07:23.819
so it won't accept the coin if it's
00:07:25.620
already unlocked so you can't unlock it
00:07:27.419
more than once or twice or so forth so
00:07:29.819
let's just create the actual State
00:07:31.620
machine itself here so let's have all
00:07:34.080
the states in there so let's say locked
00:07:36.419
and unlocked and then we maybe just keep
00:07:39.240
track of the phase itself that state is
00:07:42.120
in or the active State and so we say it
00:07:45.240
starts as locked so this is the very
00:07:47.520
basic implementation there are different
00:07:49.319
ways to do this let's say we have our
00:07:51.660
code here and let's you know let's say
00:07:54.180
we have two buttons so we have a push
00:07:57.419
button and we have the insert coin
00:07:59.940
button let to add some event listeners
00:08:02.520
so let's say push and what push
00:08:04.919
effectively does we add event listener
00:08:07.440
so when you click push it effectively
00:08:09.840
just gets the current Act of the machine
00:08:12.300
it gets all the states and then the key
00:08:15.180
it uses is the current active one and
00:08:17.460
then it just runs that and then it just
00:08:19.500
runs push to install on that and the
00:08:22.800
same over here so let's move these just
00:08:25.800
in here so unlocked and we can even type
00:08:28.919
this up if we want we can say type
00:08:31.560
record string and state and let's also
00:08:34.919
add locked okay and so what this does
00:08:37.440
insert coin it just changes the machine
00:08:41.779
active to unlocked and likewise this
00:08:45.959
just changes the machine active to
00:08:48.180
locked so the states themselves allow
00:08:51.420
you to perform certain actions and
00:08:53.700
depending on what the actual state is
00:08:55.860
the result of that action is going to be
00:08:58.080
different
00:08:58.980
States also have the means within them
00:09:02.459
to actually transition to a different
00:09:05.100
state so by that where you also control
00:09:07.760
what state it can go to there's also an
00:09:10.980
entire field of State charts and so
00:09:13.080
forth you'll actually see if you go a
00:09:16.740
mermaid JS it actually provides you with
00:09:20.339
the means to actually create State
00:09:23.160
diagrams and so this is usually how
00:09:25.380
State diagrams are modeled I'll maybe
00:09:27.240
show a bit how we can maybe create a
00:09:30.180
state diagram for our tasks in if we
00:09:33.240
were to do documentation but effectively
00:09:35.700
if we were to express this Behavior as a
00:09:38.580
state diagram it would look something
00:09:39.899
like this okay so you can do push and
00:09:41.940
coin push and coin on both of these
00:09:43.920
states if you try and do lot so you can
00:09:46.980
decide if you want to throw an error
00:09:48.600
here or if you just want to not do
00:09:51.540
anything I prefer to throw errors
00:09:53.880
because generally it would be like okay
00:09:55.860
but there's a reason why you're trying
00:09:57.899
to do this thing in a state you
00:09:59.640
shouldn't so there's something going
00:10:00.959
wrong here this this is an unexpected
00:10:03.839
action in this case that modeled it
00:10:06.360
where if you're locked and you try and
00:10:08.279
push it it stays unlocked if you put a
00:10:11.279
coin it goes to unlocked and then if you
00:10:13.560
try and put a coin again it stays in
00:10:15.300
unlocked and then if you push it goes
00:10:17.700
back to locked so that's how they model
00:10:19.560
this in a state chart so you also get
00:10:22.980
other type of State charts once again
00:10:25.500
like there isn't a strict this is a
00:10:28.740
state chart and this is what a state
00:10:30.180
chart should have so this one very much
00:10:32.940
works on the principle of polymorphism
00:10:35.160
saying that all states have the same
00:10:38.399
shape it's just what happens when you do
00:10:40.800
those actions that are different then
00:10:42.420
you can get State charts like this which
00:10:44.160
are effectively in some way just a
00:10:47.100
flowchart but it's you know like it's
00:10:49.140
also viable the the key with State
00:10:51.660
charts is that you know instead of
00:10:54.060
thinking about your state just as kind
00:10:56.399
of like this Big Blob of connected
00:10:58.200
things you know and this action here
00:10:59.700
this action here this piece of data here
00:11:01.440
this piece of data here
00:11:03.180
um you kind of split up your state into
00:11:05.640
the mutually exclusive phases that can
00:11:08.579
be in so you can't be asleep and awake
00:11:11.880
at the same same time you can't be at
00:11:13.920
the cafe or at work or at home at the
00:11:16.740
same time you need to be one of these
00:11:18.540
states and that really helps us reason
00:11:20.160
about our code much better as well
00:11:22.200
instead of having like big object that
00:11:26.040
has like all these things and you don't
00:11:28.860
know what's going to happen when you
00:11:30.360
press any of them where this where did
00:11:32.880
this idea of State charts come from so
00:11:35.640
there's this well-known mathematician
00:11:38.040
called David Harrell effectively he did
00:11:42.360
work for the Israeli government
00:11:45.180
um building fighter planes we can reason
00:11:47.339
about whether building fighter planes or
00:11:49.560
Machines of war is a worthy Pursuit like
00:11:52.019
anything else you know State charts
00:11:54.360
State machines and so forth can be
00:11:56.220
applied for any purpose whether good bad
00:11:58.140
or neutral so they ran into a problem
00:12:01.500
where the the complexity of modern day
00:12:04.920
fighter planes you know compared to if
00:12:07.680
we think about some of the very early
00:12:09.480
planes you know like this like in terms
00:12:11.339
of controls uh you maybe had like a
00:12:14.220
Rudder that you could pull up and down
00:12:15.959
and maybe one switch or another switch
00:12:19.140
and you know this is maybe the extent of
00:12:21.360
it maybe a pedal down here and a pedal
00:12:24.300
down there or maybe both pedals on this
00:12:26.940
side or whatever you know this is the
00:12:28.500
extent of the controls how does this
00:12:31.019
play into this plane
00:12:32.880
um is called the IAL lovey here is a
00:12:37.620
photo of the inside of the cockpit you
00:12:40.079
can definitely see in the same way when
00:12:42.600
we talk about software and web apps and
00:12:45.180
so forth there's also been a massive
00:12:47.100
jump in terms of complexity they ran
00:12:49.440
into a problem where the amount of time
00:12:52.139
it took to train Pilots kept on getting
00:12:55.320
longer and longer and longer Pilots were
00:12:58.019
finding themselves in more and more
00:13:00.120
instances where they didn't know what to
00:13:03.000
do or how to react to a situation so
00:13:05.339
they tried various approaches and one of
00:13:07.380
the ideas that David Harrell came up
00:13:10.380
with it was this idea of State charts so
00:13:13.500
just to get a direct quote from him so
00:13:16.260
effectively he said you know so he would
00:13:18.420
get asked about a question like what
00:13:20.399
happens when this button on the stick is
00:13:22.800
pressed and like he would say that in
00:13:25.980
order to respond you would have to go to
00:13:27.959
a two-volume document written in
00:13:30.180
structured natural language each volume
00:13:32.220
containing like 900 or a thousand pages
00:13:35.220
and it would say and even then he would
00:13:37.980
have to say yes like we found the answer
00:13:40.980
there are all these other conditions
00:13:42.959
like okay is this thing true is a
00:13:45.420
infrared missile locked on the ground
00:13:47.519
Target because then it would behave
00:13:49.320
differently and so forth to which they
00:13:51.660
would respond oh no in volume a on page
00:13:54.000
whatever whatever is this Clause so you
00:13:56.639
can think almost like as if this is
00:13:58.079
software documentation so you know your
00:14:00.180
documentation just grows and grows and
00:14:01.680
grows and it's so hard just keeping
00:14:03.720
track of complexity this is effectively
00:14:06.120
what your software has become you have
00:14:07.860
no idea what if you change this thing
00:14:09.899
what's going to happen here and what
00:14:11.220
happens here if you change this thing
00:14:12.720
and this ended up being so successful
00:14:15.300
that NASA actually started using it in
00:14:18.959
their Rockets because as mentioned you
00:14:21.300
know like maybe one of the other thing
00:14:23.399
that is kind of close to software is
00:14:25.440
rocket science and it's also being used
00:14:28.139
in biology in video games as well and
00:14:31.079
I'll maybe talk about games as well
00:14:32.459
because I think games is a good
00:14:33.959
reference for us as well in terms of
00:14:36.300
interfaces so there's actually a really
00:14:38.459
great book by someone called Ian
00:14:40.980
Horrocks that is titled constructing
00:14:44.100
user interfaces of State charts so this
00:14:46.860
book it is quite an old one you can
00:14:48.480
probably tell from the cover and so you
00:14:50.519
probably already also have some
00:14:52.560
experience of State machines so when you
00:14:54.300
think about games so games are actually
00:14:57.420
one of the most basic examples of State
00:15:00.360
machine so when you think about
00:15:01.440
something like Monopoly you're thinking
00:15:03.480
about something like hide and seek the
00:15:05.579
game is always in a specific State and
00:15:09.060
depending on what that state is
00:15:11.180
influences what can happen let's say in
00:15:14.519
hide and seek the person is counting and
00:15:16.500
so everyone's hidings that's the hiding
00:15:18.360
phase then there's the phase where it's
00:15:21.000
he's looking for them and so forth and
00:15:23.639
then it's kind of the end of the game
00:15:24.959
the game is now done same with Monopoly
00:15:27.000
you can think about this as turn so it's
00:15:28.620
player one's turn player two's turn and
00:15:31.079
then it kind of transitions from state
00:15:32.699
to state to state there's actually a guy
00:15:34.740
called Jesper Jewel who actually writes
00:15:37.139
a lot of design Theory and so forth will
00:15:39.300
actually follow him quite a bit because
00:15:41.040
I am also a bit involved in kind of the
00:15:43.500
the space of game design and and so
00:15:46.440
forth and so yeah effectively says a
00:15:48.839
game is actually what in computer
00:15:50.519
science is described as a state machine
00:15:53.399
it's a system that can be in different
00:15:55.199
states it contains input and output
00:15:57.720
functions and you're saying like hey
00:15:59.459
this start is starting to sound a lot
00:16:01.440
like functional programming and yeah
00:16:03.660
like State machines actually fit really
00:16:06.660
well with functional programming you can
00:16:09.240
even like write your state machines in a
00:16:12.180
way where it never gets rid of a state
00:16:14.339
so it always keeps the state so you can
00:16:16.500
go back into previous States as well
00:16:18.839
when you play a game you are interacting
00:16:21.540
with a state machine effectively so in a
00:16:24.600
board game the state of the board game
00:16:27.120
is actually stored in the position of
00:16:29.040
the pieces on the board so obviously
00:16:30.959
income in computers the state is stored
00:16:33.300
in memory which is what we're working
00:16:34.740
with so let me go back to if you
00:16:37.620
remember I had that example when we
00:16:39.420
spoke about throwing errors and so forth
00:16:41.459
where we spoke about this problem with
00:16:44.699
FaceTime and this bug with FaceTime and
00:16:47.459
at that point I mentioned one way that
00:16:50.399
bug could have been prevented is by
00:16:52.139
using a state machine to model our
00:16:54.839
interactions and so let me return to
00:16:57.240
this article and this is actually what
00:16:58.860
that article is about something that's
00:17:00.839
doesn't use a stake machine effectively
00:17:02.880
has implicit state so there's no
00:17:05.459
explicit state that something is in the
00:17:08.160
state can kind of be inferred so I'll
00:17:10.980
maybe Show an example of how we would do
00:17:13.380
our tasks with implicit State and then
00:17:16.260
how we would actually do it with
00:17:17.339
explicit state with the state machine
00:17:19.500
so let's just quickly read this article
00:17:21.780
first we covered this already where it
00:17:23.939
said you know if though if you're in a
00:17:25.919
video and you swipe up to add person
00:17:27.900
before the call is answered you could
00:17:30.540
actually listen in on their phone
00:17:32.280
without them actually being in the phone
00:17:34.020
and so then the question is how did this
00:17:36.360
actually get past testing the response
00:17:38.760
to how did this get fast testing is
00:17:40.679
effectively software is much more
00:17:42.299
complex than the average person thinks I
00:17:44.940
can 100 understand how something like
00:17:46.799
this could happen and it's not because
00:17:48.419
of someone not doing their job or
00:17:50.940
someone being an idiot it is just
00:17:53.100
software is really really hard and my
00:17:55.679
hope is that in your career you'll also
00:17:57.360
develop an appreciation for this
00:17:59.160
everyone is just trying to manage the
00:18:01.620
complexity of software day in day out
00:18:04.140
that is the primary job of a software
00:18:07.020
developer and so he actually says you
00:18:08.820
know so we can make assumptions about
00:18:10.260
how good their testing process is and he
00:18:12.960
says you know like he assumes given the
00:18:15.600
how big FaceTime is that they're testy
00:18:18.299
their quality and assurance team is
00:18:20.400
probably pretty great but what he says
00:18:22.200
is it doesn't really matter because you
00:18:24.000
know the complexity of software doesn't
00:18:26.340
require something to go wrong everything
00:18:28.380
can go right and the software can still
00:18:30.360
just be so complex that we can't account
00:18:32.760
for everything and he says you know
00:18:34.440
because no matter how thoroughly you
00:18:36.419
manually test your software or follow
00:18:38.520
best programming practices there are
00:18:41.280
certain types of bugs that are really
00:18:43.260
really difficult to detect until it's
00:18:45.660
too late and so we looked at some of
00:18:47.640
these and we looked at ways of
00:18:49.080
mitigating it and the ways you mitigated
00:18:51.600
It Is by proactively reducing the
00:18:54.240
complexity of your code by means of
00:18:56.400
things like abstraction encapsulation
00:18:58.559
polymorphism documenting your code
00:19:01.740
um using oop principles using functional
00:19:04.320
principles writing pure functions
00:19:07.760
reducing side effects using abstractions
00:19:10.860
like JavaScript Frameworks and so forth
00:19:12.600
all of those help us keep the complexity
00:19:14.700
of the things that we're building under
00:19:16.080
control so he actually links to a couple
00:19:18.179
of Articles where they're actually
00:19:19.440
speculate on how this could have
00:19:21.240
happened and you'll see that most of the
00:19:23.760
speculation was around State and
00:19:25.860
specifically around State machines
00:19:28.500
obviously we don't know for sure what
00:19:30.780
caused the bug unless Apple actually
00:19:33.539
makes it public which if you know
00:19:35.580
anything about Apple there's no way
00:19:36.960
they're going to make it public but
00:19:38.460
regardless of all of the speculation we
00:19:40.500
can summarize this as the following
00:19:42.720
something happened in a state of the app
00:19:45.780
where it wasn't supposed to happen so in
00:19:49.020
other words while you weren't in the
00:19:51.900
calling phase you were in a phase that
00:19:54.000
wasn't busy in an active call you
00:19:56.940
shouldn't have been able to receive
00:19:58.799
audio from someone's phone it's as
00:20:01.200
simple as that answer an easy fix would
00:20:03.660
have been to check the actual State and
00:20:05.520
if you try and actually receive audio or
00:20:08.940
if audio comes through and you're not in
00:20:11.100
an active call phase throw an error and
00:20:13.320
just crash that up it's better for that
00:20:15.539
to crash the app than accidentally
00:20:17.820
listen in on someone without them
00:20:20.160
actually knowing that you can hear the
00:20:21.660
microphone on their phone so he kind of
00:20:23.880
effectively goes and he you know tries
00:20:25.919
and recreate it in JavaScript in terms
00:20:28.020
of how it would have looked like and
00:20:29.460
this is very similar to some of the
00:20:30.780
examples that we did when when I spoke
00:20:33.000
about managing complexity in software
00:20:34.919
and so he talks here a bit about what
00:20:37.380
are State machines yeah you also hear
00:20:39.600
State machines being referred to as
00:20:41.039
finite State machines some people also
00:20:43.919
talk about them as automata and so forth
00:20:46.559
there are a couple of names for them
00:20:47.940
there's a different type of State
00:20:49.679
machines there's like a moer machine
00:20:51.299
there's a melee machine you can
00:20:52.799
disregard these like as I said don't go
00:20:55.080
too deeply into State machines try and
00:20:58.140
just use some of the principles and some
00:21:00.780
of the benefits of how you can think
00:21:02.940
about your state through the lens of a
00:21:04.679
state machine in your code and so he
00:21:06.480
talks about this maybe four different
00:21:08.160
states there's idle there's loading
00:21:10.080
there's success there's error and you
00:21:12.120
can only be in one of these states at a
00:21:14.760
time you can't be in all four of these
00:21:16.440
states so you can't be in a success and
00:21:18.780
an error state 8 at a time and you
00:21:20.760
always start in a specific State and you
00:21:22.919
move from state to state or the world in
00:21:25.500
the world of State machines you talk
00:21:28.020
about transitions based on events events
00:21:30.659
would be calling a function and so here
00:21:32.700
he just goes like he shows a basic
00:21:35.520
example of how you would actually create
00:21:37.200
a state machine in JavaScript obviously
00:21:39.480
this is a bit more complicated than the
00:21:41.760
example that we created the example we
00:21:43.679
created was a very simple
00:21:46.020
um and but you also see this actually
00:21:47.340
starts looking a bit like a Redux and
00:21:49.679
jar Redux definitely has State machine
00:21:52.200
elements to it it's not a full on state
00:21:54.360
machine but it definitely has a lot of
00:21:57.360
overlapping concepts with State machines
00:21:59.460
because in Redux only one action at a
00:22:02.820
time can't interpret it and that action
00:22:05.039
only does a single it changes the state
00:22:07.380
in a specific Manner and only in that
00:22:09.960
manner it can't fire side effects and so
00:22:12.419
yeah he just uses a state chart to kind
00:22:14.700
of show like how that is modeled and so
00:22:17.400
here he talks about kind of you know
00:22:19.380
like this idea of implicit state so he
00:22:22.380
actually mentions that you know a big
00:22:24.419
the biggest gain you get from State
00:22:26.220
machines is just coming up with explicit
00:22:29.640
states that are mutually exclusive and
00:22:31.799
so he says you know State machines are
00:22:33.900
extremely important part of designing
00:22:35.880
software and he says you are actually
00:22:37.679
creating State machines in every bit of
00:22:39.900
code that you write whether you realize
00:22:42.179
it or not the thing is if you if you're
00:22:44.640
not deliberately thinking about your
00:22:46.740
your state as a state machine you are
00:22:49.500
doing what's called implicit State
00:22:50.820
machines so in implicit State machines
00:22:53.340
the notion of program State and events
00:22:56.520
are scattered through your code base and
00:22:59.580
hidden in event listeners and if
00:23:01.620
statements and other abstractions
00:23:03.120
another aspect of State machines is you
00:23:05.100
kind of centralize that state you you
00:23:07.679
split up these distinct phases and
00:23:10.440
everything related to that phase is
00:23:12.840
centralized in a single place so it's
00:23:14.460
not split across your entire app and so
00:23:17.039
he says and once again you can probably
00:23:18.720
see a lot of parallels with functional
00:23:20.640
programming here and he says you know if
00:23:23.159
we don't exercise discipline we are
00:23:26.520
effectively going to create implicit
00:23:29.340
statement C machines just from our
00:23:32.400
natural impulses so he says you can
00:23:35.039
think about an implicit State machine
00:23:36.740
effectively as a room that have doors
00:23:40.140
leading to every single other room from
00:23:42.960
the house so he say like you would for
00:23:45.419
example be in the kitchen you'd be like
00:23:46.740
oh I actually want to go to the bathroom
00:23:48.539
so I can go through the passage and
00:23:50.640
through this and this and this and this
00:23:51.900
and then get to the bathroom but hey you
00:23:53.640
know what would actually be much quicker
00:23:55.080
if I just have a door that goes from the
00:23:57.000
kitchen directly to the bathroom and
00:23:59.159
then like at a later Point you're kind
00:24:00.960
of outside and you want to go into the
00:24:02.580
bedroom and you're like hey I should
00:24:04.559
actually just have a door that goes
00:24:05.940
directly from outside into the bedroom
00:24:07.440
so you just create these connections
00:24:09.299
between all these rooms because you're
00:24:11.220
just following what makes sense to you
00:24:13.080
so what he says is when you take an
00:24:15.360
explicit State machine approach you
00:24:16.919
decide beforehand what are the what are
00:24:19.679
the different states of the different
00:24:21.000
groups and what are the ways that you
00:24:23.280
can get from one to another and what are
00:24:25.559
ways that you're not supposed to go from
00:24:27.419
one to another even if it means you like
00:24:29.940
more work it means you need to go
00:24:31.799
through other phases to get to that
00:24:33.539
because similar to functional
00:24:35.700
programming what this does is it gives
00:24:38.760
us a predictable almost pipe that things
00:24:42.600
happen through and it isn't this web of
00:24:45.539
connected things that are just connected
00:24:47.880
to everything else you can very
00:24:49.679
explicitly see when you are busy adding
00:24:52.500
a task what are the where can you go
00:24:54.659
from here there's only one place you can
00:24:56.460
go and that is back to the list of tasks
00:24:59.280
you can't go anywhere else so you might
00:25:01.559
add a you might add a shortcut there to
00:25:03.600
maybe go oh you can maybe directly go to
00:25:06.480
settings from while you're adding a task
00:25:08.700
and so forth and so forth and so forth
00:25:10.380
and then you're creating all this web of
00:25:12.720
connections and it's very hard to test
00:25:14.580
so yeah he just continues with his
00:25:16.620
metaphor of rooms and so he says
00:25:18.780
implicit State machines are dangerous
00:25:21.299
because the application logic implied by
00:25:24.240
the state machine is scattered around
00:25:25.740
the code base so it's not clear not only
00:25:28.620
where one state begins and the other one
00:25:30.720
ends is also not clear how a user or the
00:25:35.159
code itself is expected to get from one
00:25:37.980
state to another just because there is a
00:25:40.200
door from outside the house straight
00:25:42.120
into the the bedroom not only is that
00:25:45.179
now another thing you need to test but
00:25:47.220
that might have just been a once all
00:25:48.840
thing you might never use that door ever
00:25:51.000
again but now it's always there in your
00:25:52.860
app and it's a possible interaction that
00:25:54.659
should always be tested and where a bug
00:25:56.580
can actually come in so here he just
00:25:58.559
continues talking about some of the
00:25:59.820
technical aspects of it so what also
00:26:02.159
happens when we don't follow actual
00:26:04.620
explicit slate machines as we get into
00:26:06.679
something called combinatory explosion
00:26:09.419
I've also heard this referred to as
00:26:11.460
state explosion effectively combinatory
00:26:13.980
explosion is you can effectively think
00:26:16.740
about this as compounding complexity and
00:26:19.919
that is you know if something is small
00:26:21.659
and you add one extra thing it's not
00:26:23.700
that much more complex add one more
00:26:25.679
thing it's not that extra complex and so
00:26:27.659
forth and then eventually reach a point
00:26:29.159
where if you add one more thing the
00:26:30.840
complexities just explodes and if you
00:26:33.179
then add one more thing the complexity
00:26:35.520
almost becomes completely unmanageable
00:26:37.679
so you kind of get to a point where all
00:26:39.419
of a sudden you just find your app is
00:26:41.279
just unmanageable okay so here he talks
00:26:43.620
about about it more I maybe encourage
00:26:45.480
you to read this article if this is
00:26:47.100
something you find interesting and he
00:26:48.960
says this isn't something specific to
00:26:50.700
JavaScript this isn't even something
00:26:52.140
specific to certain
00:26:54.059
um programming language
00:26:55.799
um it's not even something related to
00:26:57.360
programming it's it's a general concept
00:26:59.340
of thinking about interactions So within
00:27:02.279
the world of JavaScript probably the
00:27:04.799
biggest player in the world of State
00:27:06.360
machines is something called x-state
00:27:08.760
um so it is a JavaScript library it's
00:27:10.559
similar to Redux mob X any of those
00:27:14.400
other Global State Frameworks but it
00:27:17.279
allows you to model your State uh by
00:27:19.799
means of a state machine so if you go to
00:27:21.779
the documentation and you'll see this
00:27:23.880
even like specific plugins there's one
00:27:25.620
for svelte one for view react and so
00:27:28.919
forth we're going to be covering these
00:27:30.480
Frameworks
00:27:32.400
um and I'm not necessarily going to show
00:27:33.600
how to use xstate with them I think
00:27:36.299
almost X state is like a module on its
00:27:38.279
own but just no x-state exists if you
00:27:40.860
really want to go deeply into State
00:27:42.779
machines the only caveat being that make
00:27:47.220
sure that whoever you're working with or
00:27:49.740
who might someone who might possibly
00:27:51.840
take over the project after to you
00:27:54.320
whether you want that dependency in
00:27:57.779
terms of they need to First learn
00:27:59.520
x-state before they can join the team or
00:28:02.159
take on the project after you but if
00:28:04.440
that's a given and you're like hey I
00:28:06.360
like this and I'm going to enforce that
00:28:07.799
then xtat is a phenomenal tool for me
00:28:11.039
personally I just actually draw some
00:28:13.200
inspiration from it I didn't go full on
00:28:16.080
in this extremely formalized like way of
00:28:19.080
doing State machines because you will
00:28:21.539
see there's a lot of terminology you
00:28:23.700
know so there's like States there's
00:28:25.559
State nodes this hierarchical state
00:28:28.559
nodes parallel State nodes effects
00:28:30.779
actions guarded transitions models
00:28:34.140
context invoking Services actors and so
00:28:37.860
forth and so forth so it is almost like
00:28:40.799
the thing you need to really spend time
00:28:42.960
learning by itself so we're not going to
00:28:44.880
cover it but it is you it's maybe a
00:28:47.640
useful skill to have if you want to
00:28:50.340
spend some time learning X state so
00:28:52.740
there is another tool as well related to
00:28:56.279
kind of formalized state charts and
00:28:57.960
formal State machines called sketch
00:29:00.240
systems it's not a library or whatever
00:29:02.100
it's just a tool for you to help sketch
00:29:04.020
out your state machine and they have
00:29:06.120
some actual examples where you can see
00:29:08.720
examples of State machines so they maybe
00:29:11.520
have an example here of a simple search
00:29:13.320
bar the iPhone lock screen so let's look
00:29:16.860
at the symbols so this is basically how
00:29:19.200
how it works so you map out your States
00:29:21.240
like this and so you're in the inactive
00:29:22.860
State there's only one thing you can do
00:29:24.539
you can just start focusing when you're
00:29:26.700
focusing you can cancel or you can start
00:29:28.799
typing and that's all you can do so
00:29:30.899
let's say we cancel so we go back to
00:29:32.580
inactive we focus again we start typing
00:29:35.520
and then it takes us to text entered and
00:29:37.919
we can submit that and get the results
00:29:39.539
they have a video a description of it
00:29:42.000
I'll just super quickly scan over it so
00:29:44.520
they show here how they actually go
00:29:46.140
about mapping that state cool so you
00:29:49.020
know so you're in the in the Sleep phase
00:29:51.000
you can press the home button press
00:29:52.740
aside so these are the only things you
00:29:54.720
can do in that phase so let's say you
00:29:56.760
press the home button okay then it takes
00:29:58.440
you to this phase there's only one thing
00:30:00.120
you can do in this phase and that is
00:30:01.559
swipe up okay and you see your older
00:30:03.419
notifications oh sorry you can also do
00:30:05.399
all of these so states are also nested
00:30:07.980
but I'm not going to go into nested
00:30:10.380
States once again like that is almost an
00:30:12.659
entire course on its own but I think
00:30:15.360
there's just value in drawing
00:30:16.799
inspiration from State machines in terms
00:30:19.200
thinking about our apps and specific
00:30:21.980
components or part of the app in
00:30:24.899
mutually exclusive States instead of
00:30:27.240
just an implicit state but let me super
00:30:29.279
quickly go back over here and let's
00:30:31.620
actually think about our task and I'll
00:30:34.200
show you how we would maybe create it in
00:30:37.020
with implicit state so let's say here's
00:30:39.360
our task okay so let's figure out what
00:30:41.460
we can do so there's a check box so you
00:30:43.559
can check that there's a name and then
00:30:46.500
there's a possible delete pin that can
00:30:49.080
show up
00:30:50.299
if it is checked okay so if it's not
00:30:53.340
checked then it just shows the text and
00:30:56.580
in both those cases you should be able
00:30:58.440
to press this and it shows a modal for
00:31:01.620
us overlaying this and in the modal I
00:31:04.620
just gives some information and we can
00:31:06.899
click close or we can click edit okay so
00:31:10.679
this is close this is edit when we say
00:31:13.200
edit it brings up another screen for us
00:31:16.020
where it has this information as text uh
00:31:19.140
inputs and we can update it and then we
00:31:21.240
can say or we can say you know save
00:31:24.000
let's map this out in implicit state so
00:31:26.940
let's just say we have one big state
00:31:28.620
let's just grab some stuff from our
00:31:31.020
previous fig Jam file in terms of you
00:31:34.080
know what can all the things be in the
00:31:36.840
actual task then it has some actual
00:31:39.539
actions that you can perform so we can
00:31:41.580
toggle completed which needs completed
00:31:44.760
oh there's also a ton of other things
00:31:46.620
here like created which can just be new
00:31:49.980
date I think there were some other ones
00:31:52.260
as well completed created we have
00:31:55.140
urgency title ID is there anything else
00:31:57.539
I missed no I think so and so maybe
00:32:00.980
remove task show information show info
00:32:05.700
and then we can have start edit and we
00:32:10.260
may we have maybe toggle info and we
00:32:12.480
have toggle edit save edit and then we
00:32:15.960
obviously need a way for the HTML to
00:32:18.419
know so we can have in here you know can
00:32:23.100
delete which is false is editing which
00:32:26.940
is false we have is showing which is for
00:32:30.000
is viewing which is false yeah and I
00:32:33.179
think that's about it so this doesn't
00:32:34.679
seem that bad and also
00:32:37.440
um the key being as well that I'm
00:32:39.840
obviously using a very basic example
00:32:41.640
because if we get into some of these
00:32:43.860
more complex examples
00:32:45.899
um it's obviously going to get so you
00:32:47.700
know something like this it's going to
00:32:49.200
be much harder to explain the concepts
00:32:51.299
without getting hung up on what is
00:32:53.880
actually happening maybe show you
00:32:56.760
um how we can actually model this
00:32:59.940
Behavior through a state chart and then
00:33:02.460
actually how we can actually write our
00:33:05.640
JavaScript logic in a manner that
00:33:08.700
respects kind of this idea of explicit
00:33:11.039
States add the behavior here to update
00:33:14.340
the states so what we can do is and
00:33:17.640
let's just do it in a non-functional
00:33:19.140
always so let's just go when your toggle
00:33:22.080
completed all it does is it takes
00:33:24.240
completed it sets it to whatever the
00:33:27.059
opposite is of completed but we also
00:33:30.179
then need to toggle whether you can
00:33:32.519
delete so we can remove the task itself
00:33:35.519
and one like this actually doesn't make
00:33:38.399
sense in the context that we have here
00:33:40.260
but just for illustration purposes you
00:33:42.419
know let's just say what this does is it
00:33:44.460
just remove it says state to knowledge
00:33:46.500
in other words it removes the component
00:33:48.419
this doesn't make sense but I just want
00:33:50.460
to illustrate the principle toggle info
00:33:53.399
it sets state is viewing to the opposite
00:33:58.320
of state is viewing and then toggling
00:34:02.399
edit it just takes state is editing and
00:34:05.760
let's actually get rid of can delete
00:34:07.500
let's just say this is based off
00:34:09.960
completed that it is editing is set to
00:34:13.500
State the opposite of state is editing
00:34:15.839
and save edit so what we then do is
00:34:18.839
let's just you know say we get the
00:34:21.119
response update you know like the title
00:34:23.760
to response title we update the
00:34:28.440
urgency to response urgency and we also
00:34:31.800
need to say state is editing is false
00:34:35.460
and let's say we also want to update uh
00:34:38.339
due to response so over here we have we
00:34:41.580
have implicit States in other words we
00:34:43.619
are not thinking about State as
00:34:45.719
something that has mutually exclusive
00:34:48.599
instances we are thinking about it as
00:34:51.179
one Big Blob and we're just changing
00:34:52.918
things on that blob so how would we
00:34:55.139
actually do this as explicit State okay
00:34:58.800
so let's figure out so this so this is a
00:35:01.380
very straightforward example so at a
00:35:03.060
glance I can just see the R4 States and
00:35:05.940
so what are these states is Idols in
00:35:08.160
other words it's not doing anything then
00:35:10.440
there is completed then there is viewing
00:35:13.140
and then there is editing first and
00:35:15.720
foremost what I would do is let's just
00:35:17.040
grab everything that is not related and
00:35:20.760
sometimes in-state machines the things
00:35:23.460
that are not related to the machine
00:35:25.140
itself is sometimes called context what
00:35:29.220
I generally do is I just call it data
00:35:31.380
you'll see I changed some of the terms
00:35:33.839
that gets used in state machines a bit
00:35:36.420
purely just because they're a bit
00:35:38.520
confusing in terms of how I maybe use
00:35:40.500
things so this is all the data that's
00:35:42.839
not relevant to the actual state that
00:35:45.119
it's in so this is persistent no matter
00:35:47.220
what state you're in you're going to
00:35:48.540
have access to this created okay so we
00:35:50.880
get rid of all these is editing all of
00:35:52.920
that stuff so at the top we have phase
00:35:55.560
so obviously in a state machine you talk
00:35:57.960
about the state I generally just talk
00:36:00.240
about phase
00:36:01.680
um just to not confuse it with kind of
00:36:03.660
the way Frameworks usually talk about
00:36:05.640
this idea of state and the starting
00:36:07.320
state is Idle then I usually have
00:36:10.079
something called actions okay and here I
00:36:13.020
specify what actions can be performed in
00:36:16.800
what states I map out the actual
00:36:18.900
possible states that a thing can be in
00:36:20.900
you generally use polymorphism there are
00:36:24.000
other ways to like sometimes I don't do
00:36:26.940
this especially if there's a lot of
00:36:28.680
States so in this example over here
00:36:31.140
there's a lot of various different
00:36:32.820
states then I tend to not do it because
00:36:35.820
like it's going to be insane if every
00:36:38.099
single thing allows you to do so it
00:36:41.400
every possible thing it just gets
00:36:44.400
confusing but in a super basic state
00:36:46.200
like this one or just in the task where
00:36:48.660
there's just a couple of things you can
00:36:50.040
do I actually just do it like this let's
00:36:54.960
just map that out so type def so the
00:36:58.800
actual data itself object and so I'm not
00:37:02.280
going to map that out right now
00:37:04.740
um because I like we've done this so
00:37:06.599
many times now already I'm just going to
00:37:09.060
keep it as object and then actions first
00:37:12.180
let me do phase okay so what can phase
00:37:15.240
be in so type div phase can be idle can
00:37:20.640
be completed can be viewing and can be
00:37:23.460
editing all right so then our actual
00:37:25.859
actions so they kind of share all
00:37:28.140
actions share the same state and a lot
00:37:30.900
of times I actually just move my actions
00:37:33.300
out of the state itself generally
00:37:35.280
depends on kind of what approach you use
00:37:37.320
but I like to keep my actions separate
00:37:40.440
from the state
00:37:42.119
um because if you're looking at the ACT
00:37:43.980
you're probably looking at either the
00:37:45.960
actions you want to figure something out
00:37:47.220
about actions or you want to look at
00:37:49.260
something around the data or whatever
00:37:50.760
and to me these are two different things
00:37:53.000
so I find it helpful to just split them
00:37:55.920
up sometimes usually even in different
00:37:57.960
files actions is type record and actions
00:38:03.480
oops string there we go not actually
00:38:06.960
string phase okay so you can use phase
00:38:09.480
as the key so these need to correspond
00:38:11.400
with actual phases so let's just do
00:38:14.700
state up here and that is an object and
00:38:18.180
that object has props so it has you know
00:38:22.320
phase obviously assigned to the phase
00:38:24.480
and then DOTA sine to data and you can
00:38:28.260
also put these kind of at the same level
00:38:30.660
it doesn't really matter once again as
00:38:33.240
mentioned I don't for me personally I
00:38:35.520
just draw inspiration I don't
00:38:37.079
necessarily follow any hard rules when
00:38:39.660
I'm splitting my code up into explain
00:38:41.280
illicit phases okay so action so let's
00:38:44.400
figure out what actions do we have clear
00:38:47.640
these actions actually separately
00:38:49.140
because sometimes you want to be able to
00:38:50.880
because there are cases where you
00:38:52.440
actually want to perform an action
00:38:55.440
um in two places you want to like so
00:38:57.599
then you don't want to really clear it
00:38:58.980
you just want to link to the same one
00:39:00.480
again the one though that I will replace
00:39:03.300
is where we actually transition between
00:39:05.839
poses and actually let's get rid of
00:39:09.839
completed let's actually just say
00:39:11.700
there's three phases okay so idle
00:39:14.160
viewing and editing so we have save in
00:39:17.940
it we have remove task and we have
00:39:22.440
toggle completed and then the other one
00:39:25.440
that we have is transition it's a
00:39:28.619
transition just takes you to a different
00:39:31.079
phase it accepts a phase as the ram
00:39:35.339
phase and it just takes you to that
00:39:38.640
phase so all it does is it goes state
00:39:41.220
days and it just sets it to the phase
00:39:44.160
that you passed so the base shape of
00:39:47.280
action and actions object should have
00:39:50.420
and what I sometimes do when there's a
00:39:54.420
kind of a very linear flow in other
00:39:56.040
words you can go from this to this to
00:39:59.400
this and you can go backwards so you can
00:40:01.320
just go forwards or backwards you can't
00:40:02.880
go from completed to this unless you
00:40:06.720
actually set it unless you save then I
00:40:09.839
actually sometimes just actually have
00:40:11.640
two actions back and proceed and let's
00:40:13.920
just make these empty functions for now
00:40:15.599
empty function up here and then we can
00:40:18.240
actually assign we can actually say
00:40:19.500
toggle completed is empty function
00:40:23.520
remove Tire task also empty function and
00:40:28.079
then save edit is not it actually has a
00:40:32.220
callback save and that actually just
00:40:35.099
takes a param let's just say anything
00:40:37.200
for now you know and we can just say
00:40:39.119
this is type save save change is a prop
00:40:42.599
this is just also an empty function
00:40:44.640
which is just a toggle completed all
00:40:47.640
right so this shape so all of these need
00:40:50.040
that let's bring this into vs code so
00:40:52.680
and it can actually show this to you so
00:40:55.140
let me just open a example JS file we're
00:40:59.099
not going to be building all of this out
00:41:00.599
now I just want to show the principle to
00:41:02.760
you hey I think that's all of it and
00:41:05.880
state we can say okay what is missing
00:41:09.060
data oh it's expecting that okay we need
00:41:11.940
to remove that that's in the wrong place
00:41:14.640
this is unhappy because we need to do
00:41:17.480
state.data state.data let's just set the
00:41:20.400
data to null doesn't really make sense
00:41:22.380
but I just want to show the principle
00:41:23.940
all these need to be set to data and
00:41:27.780
this is unhappy because we need to close
00:41:30.300
that this is unhappy okay yeah because
00:41:32.760
now we actually need to add all right so
00:41:35.700
if it's idle and you try and go back
00:41:37.920
there's absolutely no reason why you
00:41:40.140
should try and go back so we have our
00:41:42.540
transition let's also just do uh all
00:41:45.900
right so let's also just do a const
00:41:48.980
invalid that just takes a message and we
00:41:54.060
just throw new error message in both
00:41:57.119
these cases we want to carry these so
00:41:59.700
that they get returned as an actual
00:42:02.960
function so we don't actually call it
00:42:05.520
otherwise let's just write it like this
00:42:07.619
so it's maybe just easier for you to
00:42:09.780
follow same here okay we just throw
00:42:11.780
right so back we can just say invalid
00:42:15.540
it's actually not do message let's
00:42:17.220
actually say task and state again phase
00:42:20.460
can't perform task in current phase
00:42:24.599
phase is required to be there we go all
00:42:28.320
right so we can just say okay what is
00:42:29.700
the task the task is back and this state
00:42:34.260
is Idle okay that's invalid save changes
00:42:38.160
is also invalid but you can't toggle
00:42:40.680
complete and so we can just pause toggle
00:42:42.720
complete and you can also proceed and
00:42:45.000
what proceed is going to do it is going
00:42:47.700
to transition to viewing back over here
00:42:52.020
is going to transition you back to idle
00:42:54.900
both of these because we're carrying
00:42:56.940
they're actually turning a function so
00:42:58.619
back is then going to be a function we
00:43:00.359
see it is then going to be a function
00:43:02.220
takes you to editing you can't save any
00:43:06.060
changes in the viewing State and toggle
00:43:09.540
completed you can't toggle completed in
00:43:12.359
the viewing State and oops we have this
00:43:14.520
the wrong way around so it should
00:43:16.440
actually be idle and this should be save
00:43:18.599
changes we can go back it just takes you
00:43:21.480
back to viewing you can't proceed
00:43:24.359
transition because there is nothing to
00:43:26.700
proceed to you also can't toggle
00:43:29.040
completed if you want to update
00:43:30.300
completed you need to do it as part of
00:43:32.099
save changes and save changes all right
00:43:36.420
so this is much easier to reason about
00:43:38.579
and we can even let's move all or type
00:43:42.060
declarations up here and it keeps track
00:43:44.640
of the phase and this is the data that
00:43:47.160
is available to All Phases doesn't
00:43:49.500
matter what phase you're in and then
00:43:51.839
there is an action to toggle completed
00:43:54.780
um there's an action to remove tasks we
00:43:56.700
actually never added remove tasks so
00:43:59.460
let's actually add it to our action and
00:44:01.260
this is also what's really cool about
00:44:02.520
this approach if you now add you know
00:44:04.500
remove task now it's going to ask you to
00:44:07.140
consider for every phase what is the
00:44:09.119
implication so this like this oh it's
00:44:11.339
such a I can't express to you guys how
00:44:13.440
elegant this approach is because if you
00:44:15.300
if you didn't have it in this manner you
00:44:17.099
might not consider what way someone can
00:44:20.520
actually remove and if someone else
00:44:22.200
looks at your code they might not
00:44:24.180
realize that you can only remove a task
00:44:26.220
in the idle mode you can't from the
00:44:28.440
editing mode so it's also very
00:44:30.200
self-documenting in that sense so we
00:44:32.640
know that you know in both these cases
00:44:34.319
you can't remove the task when you're
00:44:36.000
viewing can only remove it over here so
00:44:39.119
this is very self-documenting and also
00:44:41.400
the other cool thing is ironically
00:44:43.859
enough actually reduce the amount of
00:44:45.839
like actual functions we have
00:44:47.760
um there's just like these two functions
00:44:49.500
which are related to the state machine
00:44:51.240
itself and the only three functions now
00:44:53.700
is you know toggle completed remove task
00:44:55.800
and save changes we're not bothering
00:44:58.079
with actually you know how like an
00:45:00.660
individual task for going to viewing
00:45:03.839
going to editing going back canceling
00:45:07.440
editing canceling viewing and so forth
00:45:10.200
okay so this is a very elegant way to
00:45:12.359
express it but first and foremost this
00:45:14.520
might not make sense in all components
00:45:16.920
some components might not actually
00:45:19.260
benefit from a state machine approach to
00:45:21.540
it and the other thing is as well it's
00:45:22.980
up to you to decide like how strictly do
00:45:26.220
you want to actually adhere to the way
00:45:28.619
State machines are actually formalized
00:45:30.480
by our like State charts and so forth so
00:45:33.359
the last thing I want to show you is how
00:45:35.220
we would actually now document this in
00:45:37.500
markdown so let me just also open an
00:45:39.300
example in a markdown file here let me
00:45:42.180
just pull in mermaid and let's open the
00:45:45.240
preview on the side here and obviously
00:45:47.040
it's unhappy because this isn't valid
00:45:49.440
mermaid let's just go to mermaid.js and
00:45:52.260
let's just get a basic like State
00:45:54.900
diagram so you can read this if you want
00:45:58.260
to
00:45:59.339
um I'm not going to cover all the ins
00:46:01.260
and outs of it like actually a good read
00:46:04.319
in terms of just actually understanding
00:46:07.020
um State machines you know so I would
00:46:09.359
actually encourage you to read this so
00:46:11.579
the first thing we want to do let us
00:46:13.740
just Define all possible States and you
00:46:16.200
can actually do a shorthand like this
00:46:18.060
and usually I actually use a acronym for
00:46:22.200
a state it's just easier to write it
00:46:24.960
like that so let's just use I for idle V
00:46:28.260
for viewing and then e for editing if
00:46:31.680
you have for example two things that you
00:46:33.720
can do like EA or EF or or whatever this
00:46:36.960
is just my personal approach because
00:46:38.700
then it's a lot easier just to write it
00:46:40.380
out like here so what we can say is we
00:46:42.599
can say I can go to V but V can also go
00:46:47.040
to I okay V can also go to e but e can
00:46:52.740
also go to V so this effectively means
00:46:55.260
there's no way from E to get to idle or
00:46:57.540
from idle to get to editing okay and we
00:46:59.819
can also give them names so we can say
00:47:02.760
you know this is forward this is
00:47:05.520
backward is that what we called it a
00:47:07.980
proceed in back this is proceed this is
00:47:10.079
back and the same over here so we also
00:47:12.599
indicate the starting state so you can
00:47:14.940
just go like that and say that you know
00:47:17.579
it starts in idle so like that you can
00:47:20.339
also specify an end State and that is
00:47:22.079
when the state machine stops responding
00:47:24.060
maybe we can actually have the in state
00:47:26.880
B and remove task and you can only do
00:47:29.700
that in idle so we can say from idle you
00:47:32.400
can also stop the machine so you can
00:47:34.319
also stop the machine from idle but if
00:47:37.079
you're in here you can still move around
00:47:38.700
so but if you remove task and we can
00:47:40.859
actually just say you know let's just
00:47:42.300
remove task completely stops the machine
00:47:44.760
all right start and end composite States
00:47:47.700
I'm not going to cover composite States
00:47:49.619
I think
00:47:50.940
um that requires a bit more State
00:47:52.800
machine logic and Theory I'm not going
00:47:55.440
to go into that but check it out if you
00:47:58.020
find this interesting then there's also
00:48:00.599
if you want to be able to go to two
00:48:03.599
distinct States so this is we maybe need
00:48:06.480
to make a choice yeah so forking and
00:48:08.640
then you can come back to a specific
00:48:10.500
State as well if you want and you can
00:48:12.960
also add some notes there's also
00:48:15.180
concurrent States but once again I think
00:48:17.760
this is maybe a bit too advanced and you
00:48:21.599
can add comments as well so the comments
00:48:24.180
don't show up in the diagram itself and
00:48:26.640
you can apply specific Styles so this is
00:48:29.220
very straightforward very basic options
00:48:32.760
when we're documenting our code
00:48:35.060
so I just want to add some notes we
00:48:38.099
don't have to specify all the actions
00:48:40.140
that you can take once again I try and
00:48:43.319
not formalize it too much I take a very
00:48:45.300
loose approach otherwise it gets too
00:48:47.700
hard to actually manage and update and
00:48:50.099
we can even write our notes in a
00:48:51.780
separate place so we can write our note
00:48:53.099
so let's say right of e okay let's just
00:48:55.560
bring it in oh we need to add endnote as
00:48:58.560
well I usually add my notes at the
00:49:00.300
bottom as well and I okay so let's put
00:49:02.280
our notes on the left side here only
00:49:04.560
phase where task can be toggled based
00:49:08.940
where task can be updated so these notes
00:49:12.240
might actually make it harder for you to
00:49:14.220
read it so I do think in this case it
00:49:17.339
does I don't know you can keep it if you
00:49:18.960
want I would go for example you know
00:49:21.020
task component and then just down here
00:49:25.380
say like you know the actions All Phases
00:49:28.680
have the following actions and then I
00:49:31.560
can even write the description if I want
00:49:33.300
so I can say use to move phase backwards
00:49:37.800
use to move phase forwards and you can
00:49:40.740
imagine like this idea of also
00:49:43.339
thinking about phases as linear things
00:49:46.200
is really helpful in terms of something
00:49:49.200
like signing up or creating an account
00:49:51.480
where you move forwards or backwards and
00:49:54.359
you know save changes we can say can
00:49:56.460
only be done in editing and you know
00:50:01.260
these as well we can say you know can
00:50:02.819
only be done in idle and so forth and so
00:50:05.400
forth so this really helps us actually
00:50:08.040
document our code and document our
00:50:10.020
behavior in a in a meaningful Manner and
00:50:12.660
I find it actually works very nicely
00:50:15.420
with functional programming because the
00:50:18.119
focus is on interaction as opposed to
00:50:20.420
objects so it's a very nice way to
00:50:23.700
actually Express interaction as well so
00:50:25.920
you know so now we already have a lot of
00:50:27.660
documentation here if you look at this
00:50:29.460
and you just understand some Basics
00:50:31.500
about State machines you understand this
00:50:33.839
means where it starts this means it ends
00:50:36.420
it stops like it you can no longer
00:50:38.220
interact with it and you understand okay
00:50:40.020
so from idle you can proceed to viewing
00:50:42.119
from viewing you can proceed to editing
00:50:43.800
but you can only proceed back from
00:50:46.020
editing and you can only proceed back
00:50:47.579
from idle is basically State machines
00:50:51.359
I think they there was a lot of Concepts
00:50:54.900
um I wanted to cover and I I tried to
00:50:57.480
only do the parts of lit and the actual
00:51:00.480
writing of code where we had to I think
00:51:03.599
I think it was more important to me that
00:51:05.040
can't we cover all the concepts
00:51:07.260
um and then we can focus when we now get
00:51:09.839
to Frameworks from the following list on
00:51:12.240
to actually show how you would actually
00:51:15.240
write the code associated with those
00:51:18.300
so in the following lessons we are going
00:51:20.400
to cover six Frameworks so we're gonna
00:51:22.079
we are going to start with one called
00:51:24.359
Alpine then we're gonna then we're gonna
00:51:27.780
come back to LIT
00:51:29.880
um and just dive deeper into that we are
00:51:32.700
going to look at one called view we're
00:51:35.160
going to look at one called svelt
00:51:37.680
um we can look at one called angular and
00:51:39.660
one called react and we're also going to
00:51:42.000
be looking a lot more at node and npm
00:51:44.700
each time we cover one of these new
00:51:46.740
Frameworks what I'm going to do is I'm
00:51:48.000
going to build that very first tally app
00:51:50.220
that we build at the very beginning and
00:51:52.260
show you how you build it build
00:51:53.760
something like that with the framework
00:51:55.319
and then what I'm also going to do I'm
00:51:57.059
going to actually build this to do app
00:51:58.920
in that framework and we should actually
00:52:00.839
be able to do that in a single lesson
00:52:02.700
just because the Frameworks allow us to
00:52:04.920
do a lot of these things really quickly
00:52:06.839
and so today I'm going to show you like
00:52:08.760
how all the pieces come together and how
00:52:11.160
you can actually get the studio app out
00:52:13.079
like really really quickly because we
00:52:14.880
understand all the underlying Concepts
00:52:16.980
now and then after after that we're
00:52:18.960
going to talk a bit more about other
00:52:20.819
things like the fetch API like
00:52:23.040
asynchronous code promises a lot of
00:52:25.859
those things we like I I've mentioned
00:52:28.040
and also you know test driven
00:52:30.900
development as well which is part of uh
00:52:33.960
behavioral driven development and and so
00:52:36.420
forth at the end of that like you'd
00:52:39.599
basically know the majority of things I
00:52:42.300
would expect someone who calls
00:52:44.220
themselves a software developer to
00:52:46.079
actually know from that so then we're
00:52:49.140
going to be doing a big practical
00:52:50.760
project where you can either decide to
00:52:54.420
take that book connect project that
00:52:56.280
we've done up until now and build
00:52:58.260
further on that or I'm gonna also give
00:53:00.780
you the ability I'm going to give you
00:53:02.640
data for a podcast app and you can
00:53:04.920
decide I want to design and build my own
00:53:07.079
app from the ground up and then I'm
00:53:09.059
going to give you that podcast
00:53:09.960
information and you can figure out how
00:53:12.300
you want to approach that yourself with
00:53:14.700
all the knowledge you've gained through
00:53:16.680
all the lessons up until that point but
00:53:19.140
I will see you in the next lesson and
00:53:21.780
there we're going to get into actual
00:53:23.460
JavaScript Frameworks and then we're
00:53:26.160
going to be actually writing a lot of
00:53:27.839
code we're going to be building a lot of
00:53:29.400
really cool stuff awesome I will see you
00:53:31.980
guys there