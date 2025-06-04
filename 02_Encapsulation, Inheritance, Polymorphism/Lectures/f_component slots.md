Please write clear and comprehensive lecture notes and lesson content for this lecture:

00:00:00.060
and so I quickly just want to show how
00:00:03.240
this idea of polymorphism tying this all
00:00:06.660
the way back to what we started with up
00:00:09.120
here how this concept of polymorphism is
00:00:12.179
actually going to help us in terms of
00:00:13.799
how we do our web components so let's
00:00:16.139
return to our original example and let
00:00:18.180
me just copy this so we can discuss it
00:00:19.740
down here as well at the very least we
00:00:21.960
have this agreed idea treating your code
00:00:24.779
base as one Big Blob is a bad idea and
00:00:27.960
that we should strive for encapsulation
00:00:30.000
and bringing this back to the world of
00:00:32.820
you know kind of a model car or
00:00:34.380
something the fact that if we get a flat
00:00:36.600
tire we don't need to actually replace
00:00:40.500
the entire car to fix the problem we can
00:00:43.739
decouple the actual part that is giving
00:00:46.200
the problem and look at that and figure
00:00:48.960
out what's going on in that little scope
00:00:51.300
as opposed to looking at the entire app
00:00:54.180
going through all the lines of codes all
00:00:56.520
the line of code all the logic we can
00:00:58.079
extract that little independent piece
00:00:59.820
that function on its own and just debug
00:01:02.280
that or if we want to add another wheel
00:01:04.319
we can just duplicate this little piece
00:01:06.360
instead of rebuilding or changing on our
00:01:09.299
entire app but then we also saw that you
00:01:12.119
know at some point you need to make
00:01:14.159
these things a bit more general purpose
00:01:16.020
so that you can reuse them otherwise
00:01:18.180
you're going to end up with thousands
00:01:20.520
and thousands of these independent
00:01:22.979
little pieces and that at the end of the
00:01:25.619
day is just going to be a ton of noise
00:01:27.180
I'm going to make it even worse that you
00:01:29.580
build your discrete units with enough
00:01:32.340
genericness that they can be reused in
00:01:35.759
other circumstances but there is a
00:01:38.100
danger to over abstracting these for
00:01:41.040
example you know creating a factory
00:01:43.200
function that is do anything and you can
00:01:46.079
pause anything into it and it can do
00:01:48.240
anything because the the problem there
00:01:50.220
is that it's going to have an if
00:01:51.960
statement that it's going to be like
00:01:53.640
thousands and thousands of lines of
00:01:55.619
possible if conditions okay so be
00:01:58.320
careful as well that you don't over
00:01:59.939
abstract and a tool that helps us
00:02:02.399
actually avoid over abstraction is is
00:02:05.520
literally the first letter of solid
00:02:07.680
which is single responsibility principle
00:02:09.780
so think about what is the purpose of
00:02:12.180
this thing once you get to something
00:02:14.459
like do anything you're breaking the
00:02:16.800
single responsibility and it can do
00:02:18.599
loads of different things the goal isn't
00:02:20.580
to have a do loads of different things
00:02:22.440
the goal is to solve a specific
00:02:25.319
responsibility that comes up in several
00:02:28.260
places in your app because you will have
00:02:30.599
elements that are once-off elements but
00:02:33.720
the goal is not to treat everything as a
00:02:36.239
once auth but when there is an
00:02:38.040
opportunity to create a more General
00:02:39.780
abstraction you do that I've mentioned
00:02:42.180
this before that video by NC Dodds I
00:02:45.060
will link it in the resources and the
00:02:47.400
article by Sandy mix the wrong
00:02:50.160
abstraction these provide General good
00:02:53.760
guidelines in terms of how to avoid over
00:02:56.580
abstraction and there's a couple of
00:02:58.260
General guidelines um the one that's the
00:03:01.319
most common I find is that the rule of
00:03:03.300
three if you are doing something for a
00:03:05.519
third time then it's probably worth
00:03:07.739
looking at an abstraction given this
00:03:09.840
isn't a hard rule sometimes I have
00:03:12.060
enough foresight to actually know when
00:03:13.920
something is going to be used at least
00:03:15.659
three times so let's say for example a
00:03:17.159
button you know I know that there's
00:03:18.599
going to be various different forms of a
00:03:20.459
button in my app I don't need to create
00:03:22.379
three different buttons to know to
00:03:24.900
actually see that sometimes you need to
00:03:27.180
see that physically happen sometimes you
00:03:29.459
know but be careful of what you think
00:03:31.379
you know sometimes you actually create
00:03:32.879
abstractions that you only use once and
00:03:34.920
you're like and the whole point of over
00:03:36.599
abstraction is like that is bad so let's
00:03:38.940
look at a specific example and let's
00:03:40.739
look at an example within the world of
00:03:43.319
web components here is a real world
00:03:46.080
example of all the buttons that Amazon
00:03:49.019
currently uses on their website so if
00:03:52.019
you go on amazon.com it's a massive site
00:03:54.599
so here the buttons look very similar
00:03:56.819
but as you go deeper into the site in
00:03:58.680
various places they they use different
00:04:00.840
buttons the point here is that even big
00:04:03.420
companies get this wrong but I also
00:04:05.819
think Amazon specifically is generally
00:04:07.739
mocked how bad their UI design is and
00:04:10.739
this might be a case where you might
00:04:12.900
create one button for one purpose
00:04:14.580
another one and you get to the third one
00:04:16.560
and you're like hey maybe I can actually
00:04:18.540
abstract this into something that uses
00:04:21.298
the principle of polymorphism that can
00:04:23.400
be reused instead of having 50 different
00:04:26.280
buttons so how would you do this so
00:04:28.919
let's say this is an act these are all
00:04:31.199
different web components that you create
00:04:32.880
here is our HTML and let's say this is
00:04:35.940
what the web components would look like
00:04:37.500
so we have a green button we have a
00:04:41.280
orange button we have a blue button we
00:04:45.120
have a big button but then we also need
00:04:47.880
to account for all of these so we have a
00:04:49.919
big green button but also a small green
00:04:52.860
button but then we also need a disabled
00:04:55.380
state so small green button disabled but
00:04:59.580
then we also need a small green button
00:05:02.940
that redirects to Google and so forth
00:05:06.720
and so forth then you can imagine how
00:05:08.340
you're going to end up at thousands and
00:05:10.320
thousands of components using the
00:05:12.180
principle of polymorphism what we can
00:05:14.100
instead do we can do something like
00:05:16.139
custom button but we can probably take
00:05:18.300
it a step further and think about what
00:05:20.220
is the responsibilities a single
00:05:21.840
responsibility their user action so this
00:05:24.419
is the web component that just controls
00:05:26.759
a user action whether that is triggering
00:05:29.820
something of a button click or
00:05:31.080
redirecting and so forth and it's
00:05:33.900
generally surfaced in this manner what
00:05:35.580
can we pass to it so we use attributes
00:05:37.919
so let's say we pass color as an
00:05:40.259
independent thing so color is green or
00:05:42.780
color is red we pass whether it's
00:05:45.720
disabled or not as an independent thing
00:05:48.300
by default it fires a click event but we
00:05:51.840
can actually even have it let's say
00:05:53.759
color blue tell it to go somewhere
00:05:55.860
instead of actually firing a click event
00:05:57.660
so go to google.com and then let's say
00:06:01.560
we want a big or a small version of it
00:06:03.419
so we can maybe do size and we can maybe
00:06:05.940
just do s m and L or we can just write
00:06:08.639
out large like that cool so you can see
00:06:11.699
how the principle of polymorphism helps
00:06:14.340
us actually if you think about that Lego
00:06:16.380
block compared to this how this actually
00:06:19.199
helps us keep our complexity more
00:06:22.139
maintainable so we're creating the
00:06:24.000
single thing that that serves a specific
00:06:26.220
responsibility that just accepts
00:06:28.500
different attributes instead of creating
00:06:30.600
a new thing from scratch every time so
00:06:32.880
this is also something that's a lot
00:06:34.440
easier to reason about because you you
00:06:36.780
might need to read a massive page of
00:06:39.000
documentation to understand what the
00:06:40.800
purpose of each of these are as opposed
00:06:43.319
to something like this where you just
00:06:45.180
map out the different permutations so
00:06:47.819
there's three types of buttons there's a
00:06:49.500
full button there's an outline button
00:06:50.940
there's a ghost button and these are the
00:06:53.460
actual states that can be passed so you
00:06:55.440
can imagine how having 20 components
00:06:57.419
that work in this manner as opposed to
00:06:59.639
300 components that are all once off
00:07:02.639
like this how this is going to be a lot
00:07:04.979
easier to control the complexity but the
00:07:07.319
key being you shouldn't over abstract
00:07:09.300
and this is something you just learn
00:07:11.039
from experience I I honestly my guess is
00:07:14.699
you are going to feel the pain at some
00:07:16.740
point you are going to over abstract
00:07:18.419
that's unavoidable prepare yourself
00:07:19.919
emotionally for that and that's
00:07:21.780
unfortunately how you learn it is
00:07:23.400
something that you learn from just
00:07:24.539
burning your fingers and realizing oh
00:07:26.400
I've over abstracted now or I didn't
00:07:28.560
abstract enough but the problem with
00:07:30.479
over abstraction is it's much harder to
00:07:32.220
go back from over abstraction than it is
00:07:34.740
to add more abstraction then and beat
00:07:36.840
yourself up if you get it wrong it takes
00:07:38.880
a lot of practice and practice and
00:07:40.560
practice to get it right so we
00:07:42.360
highlighted four types of polymorphism
00:07:44.639
that we have covered thus far but there
00:07:48.300
is a fifth type that we haven't and now
00:07:50.759
it's going to become really relevant as
00:07:52.500
we talk about web components
00:07:54.060
specifically in web components this idea
00:07:56.520
of slots and this isn't something that's
00:07:58.800
unique to web components we find it in
00:08:00.720
all Frameworks as well and these operate
00:08:03.419
by a principle called parametric
00:08:06.479
polymorphism so let me show you this in
00:08:09.240
principle what this looks like we've
00:08:11.039
shown how we can use some of the
00:08:14.120
polymorphic principles that we've
00:08:16.080
learned up until now to actually create
00:08:17.940
things like this which helps us manage
00:08:19.800
the complexity a lot better but as your
00:08:22.199
app grows and grows and grows you might
00:08:24.360
actually start getting more attributes
00:08:26.879
okay so you might be getting let's say
00:08:29.280
icon and let's say you know it has an
00:08:31.379
arrow icon in it in other words a button
00:08:33.539
something like this okay you know here's
00:08:35.458
the text and then now there's Arrow but
00:08:37.860
then you might get a situation where you
00:08:39.419
want a button that is just an icon and
00:08:42.240
no text so like that so let's say a play
00:08:44.940
button and then you might get an example
00:08:47.580
where you want it to be on the other
00:08:50.100
side of the icon so you maybe want to
00:08:52.320
see your profile so you want the picture
00:08:54.180
of the profile to be at the start of the
00:08:56.580
button whereas this makes things
00:08:58.980
meaningfully better than if we didn't
00:09:01.800
use attributes to control this at some
00:09:04.500
point even with attributes themselves
00:09:06.240
you're going to reach a point where your
00:09:08.040
even your attributes are going to start
00:09:09.300
getting out of control so let's say you
00:09:11.279
have a left icon Arrow left icon color
00:09:16.820
green lift icon size small right icon
00:09:22.980
Circle right icon color orange right
00:09:27.839
icon size large label color purple and
00:09:33.420
so forth and so forth so you know we're
00:09:35.160
going to reach a point where this is
00:09:36.180
going to be become a reality and as our
00:09:38.339
app keeps growing and growing and
00:09:39.779
growing we're just going to be adding
00:09:41.160
more and more and more and more stuff to
00:09:42.779
our components and effectively it's
00:09:44.760
going to end up looking like this so we
00:09:46.980
can use parametric polymorphism to
00:09:49.620
actually solve this in a meaningful
00:09:52.380
manner as follows and this is also the
00:09:54.600
principle on which higher order
00:09:55.860
components are based and at this point I
00:09:58.019
I truly believe that once we start
00:09:59.519
talking about higher order components
00:10:01.019
similar to classes that you're going to
00:10:03.000
be like this guy's been talking about
00:10:04.440
higher order components now for what
00:10:06.360
feels like years and I still don't know
00:10:08.220
what this damn thing is there's a lot of
00:10:10.200
ideas that we need to discuss before we
00:10:12.480
can actually look at higher order
00:10:14.220
components in a meaningful manner so
00:10:16.680
okay so but it works on the exact same
00:10:19.140
principle parametric polymorphism is how
00:10:22.440
we actually do higher order components
00:10:24.600
so effectively what we do is we pass
00:10:28.700
abstractions into other abstractions so
00:10:32.279
we say we're going to put an abstraction
00:10:35.279
here this thing wraps other abstractions
00:10:38.880
we don't know what those abstractions
00:10:41.160
are there can be any abstraction and
00:10:43.860
we're going to build the thing that
00:10:45.420
takes those abstractions in a way that
00:10:47.700
it can handle any abstraction but you
00:10:49.920
know this is where things start getting
00:10:51.300
complicated like once you start passing
00:10:53.640
abstractions into abstractions things
00:10:56.220
start getting really complicated
00:10:57.740
especially in terms of how you usually
00:11:00.720
think about things there's so generally
00:11:03.060
what I find within JavaScript there's
00:11:04.920
two types of things that are hard for
00:11:06.660
people to get their head around the one
00:11:08.640
is recursion and you might have
00:11:10.440
encountered recursion before I think it
00:11:12.300
is covered in the free code Camp
00:11:13.680
material recursion is tricky because
00:11:15.959
there's nothing in the real world that
00:11:18.300
is a good metaphor or recursion so
00:11:21.360
oftentimes what people do is they talk
00:11:23.040
about like the branches on a tree
00:11:24.660
effectively the the example would go
00:11:27.120
like what is a branch made of well a
00:11:29.100
branch is made of other branches but
00:11:31.079
what are those branches made of other
00:11:32.820
branches so you kind of have the
00:11:34.200
structure it's just like branching
00:11:35.579
branching branching going outwards you
00:11:37.380
know and like here's your tree with like
00:11:39.240
all these branching structures why that
00:11:41.760
is insufficient is because even that
00:11:44.339
example has a stopping point it has a
00:11:47.459
point where physically you can't have a
00:11:49.440
tree that has infinite branches at some
00:11:52.140
point those that branching logic needs
00:11:54.360
to stop recursion as a concept can go on
00:11:56.940
infinitely this is why it's hard for our
00:11:59.459
brains to understand then the other one
00:12:01.920
is like higher order abstractions so in
00:12:04.440
other words abstractions that take
00:12:06.480
abstractions that can't take
00:12:07.920
abstractions that can take abstractions
00:12:09.540
that can take abstractions and so a good
00:12:12.120
example is once again how this is
00:12:14.339
usually explained is through a metaphor
00:12:16.860
of these kind of Russian nested dolls so
00:12:19.260
you might know about them so you have
00:12:20.399
these doll and you open that doll and
00:12:22.260
inside that doll is another doll and
00:12:23.880
another doll and another doll and
00:12:25.320
another all so you have these
00:12:27.180
abstractions that are nested inside one
00:12:28.980
another and you can actually put
00:12:30.600
anything in there you don't need to put
00:12:32.519
another doll in there you can put for
00:12:34.079
example a golf ball or a piece of paper
00:12:36.060
or a coin or whatever so not only can
00:12:39.120
you put another doll in it but you can
00:12:40.920
put anything in it so you have these
00:12:43.380
levels of abstractions that can continue
00:12:46.980
indefinitely once again like this also
00:12:49.500
this example Falls flat because at some
00:12:51.720
point like you physically can't put any
00:12:53.459
more dolls in or you can't like wrap any
00:12:56.579
more dolls and this is
00:12:58.500
Frameworks I actually find the
00:13:01.019
the hardest to learn are react and
00:13:02.940
angular compared to like svelt and View
00:13:05.100
and lit and so forth the reason I think
00:13:07.079
why angular is harder to learn is
00:13:09.300
because angular is massive in scope so
00:13:12.600
it has all these different things and
00:13:15.240
Concepts you need to learn whereas react
00:13:17.220
is really small in scope um it only has
00:13:20.279
a couple of things you can do with it
00:13:21.660
which is also why people a lot of times
00:13:23.459
say react as a library and not a
00:13:25.980
framework you might hear that what's
00:13:27.959
what makes react I think hard for people
00:13:30.000
to learn is because react really Builds
00:13:33.300
on this concept so effect actively your
00:13:35.880
entire app is just these nested levels
00:13:39.120
you're just composing abstractions
00:13:41.279
inside abstractions inside abstractions
00:13:43.320
which is also why react has this I think
00:13:46.440
called hoc Which is higher order
00:13:49.560
components so so we spoke about higher
00:13:51.839
order functions before but in react it
00:13:54.839
even treats the components themselves as
00:13:57.899
higher order in other words components
00:13:59.700
can take components and those components
00:14:01.560
can further take components and so forth
00:14:03.360
and so forth and so forth so we can even
00:14:05.279
we can do this with web components as
00:14:07.320
well that sounds really complex
00:14:09.300
sometimes it can get really complex so
00:14:11.459
I'm obviously going to do a very simple
00:14:12.720
example and the simple example is just
00:14:14.820
to show how powerful the principle is
00:14:16.800
but the type of complexity is different
00:14:19.740
from the type of complexity that you get
00:14:22.200
with this this is complex in terms of
00:14:25.620
it's unmanageable to work with there's
00:14:28.139
too many things you don't have the brain
00:14:30.540
capacity to consider all of this at once
00:14:32.940
the notion of higher order function in
00:14:35.339
higher order components are hard in a
00:14:38.160
different way they're hard because it's
00:14:39.480
a hard concept to understand but once
00:14:41.880
you understand the concept it's easy to
00:14:44.339
work with so also it's important to keep
00:14:46.620
that distinction in mind so it's a type
00:14:48.779
of complexity that is easy to manage as
00:14:52.380
opposed to this complexity which is very
00:14:54.420
hard to manage so you trade this type of
00:14:56.880
complexity for a different type of
00:14:58.199
complexity that's much easier to manage
00:15:00.360
so let's say we have our user action and
00:15:03.180
so at the core this is what it does okay
00:15:05.760
and into that let's also just make a
00:15:08.459
singular user action you can't pass any
00:15:11.880
other component to get the same
00:15:13.740
functionality we have a icon component
00:15:16.680
and we have a label component so let's
00:15:19.680
just say visual icon okay and then we
00:15:22.320
have a text label and visual icon again
00:15:25.740
and so let's say the label purple I'm
00:15:28.560
going to try and replicate the above I
00:15:30.120
hope I don't miss anything size large
00:15:32.699
and so then the right one is size large
00:15:36.120
as well and the color is orange and the
00:15:40.079
image is circle and then this one is
00:15:43.800
size small and the color I think was
00:15:46.800
green yeah and the image is Arrow I
00:15:49.740
think
00:15:50.399
you might be like hey this looks
00:15:51.899
actually very familiar and you are right
00:15:54.240
it is very similar to what we have in
00:15:57.120
HTML so and this is the value of web
00:15:59.760
components in terms of treating your
00:16:01.920
behavior as a little bundled unit of
00:16:05.519
HTML CSS and all of that because it
00:16:07.980
actually mirrors how we think about HTML
00:16:10.500
very nicely you know so you can do the
00:16:12.660
exact same principle but it's much more
00:16:14.940
limited in actual HTML so there's like
00:16:17.639
you can do a lot more advanced stuff
00:16:19.740
with full on parametric polymorphism and
00:16:23.459
it's because but this at your parametric
00:16:25.800
polymorphism actually comes from the
00:16:27.899
world of mathematics so if you have a
00:16:29.519
look on the Wikipedia article of
00:16:31.079
parametric polymorphism you'll actually
00:16:33.360
see a lot of you know mathematical
00:16:35.519
examples here and there are actually
00:16:37.259
languages that go much deeper into this
00:16:39.600
than JavaScript for example Haskell
00:16:41.519
where your code actually starts looking
00:16:43.980
a bit like this almost like mathematical
00:16:46.680
Expressions JavaScript is a nice Middle
00:16:49.199
Ground where it doesn't require you to
00:16:52.019
go as deep into the concept in order to
00:16:55.019
actually use it in a meaningful way
00:16:56.579
obviously things like Haskell and so
00:16:58.920
forth are much more powerful than
00:17:01.019
JavaScript in terms of expressiveness
00:17:03.120
like you can express something like this
00:17:05.220
in a much more concise way but the
00:17:08.220
trade-off is it's much more complicated
00:17:10.919
to learn that to actually get to a point
00:17:13.439
where you actually understand what
00:17:14.640
you're reading and I think JavaScript is
00:17:17.099
a has a very nice middle ground in terms
00:17:20.220
of allowing you to leverage this
00:17:22.619
principle without going full on category
00:17:25.559
Theory which is what some languages like
00:17:27.720
Haskell and so forth are based on and so
00:17:30.000
this is also pretty straightforward
00:17:31.679
because the order that we pass it in we
00:17:33.780
can just assume that's the order in
00:17:35.220
which it should be shown so you know
00:17:36.539
Left Right label so this also allows us
00:17:39.660
to do other things like even this
00:17:41.460
example up here assumes that the label
00:17:43.980
is always going to be in the middle and
00:17:46.200
also that there's only a single label
00:17:47.760
but but let's say what you want is you
00:17:49.440
want two labels and an actual icon in
00:17:52.140
the middle this doesn't even allow for
00:17:54.120
that so it also gives us a lot more
00:17:56.640
flexibility and this is a very simple
00:17:58.860
example because the component itself has
00:18:01.140
kind of a linear order in terms of where
00:18:03.059
the things should be shown in more
00:18:05.160
complex examples we we can actually
00:18:08.100
designate it a specific place where it
00:18:10.620
should be used so we can go for example
00:18:12.720
slot overlay or plot primary or slot
00:18:17.220
ball back and I think this is where it
00:18:19.020
starts getting complicated is that now
00:18:21.120
we're actually not only talking thinking
00:18:23.820
about like hey these are actual things
00:18:25.919
that should be shown and it should be
00:18:27.840
shown in this order we can actually pass
00:18:29.720
abstractions as things that should be
00:18:32.640
used so this might not even show unless
00:18:35.940
this for some reason doesn't show and it
00:18:38.520
falls back to this and so forth so you
00:18:40.559
can actually do a lot of advanced things
00:18:42.539
in a very concise and readable manner
00:18:45.179
right so but in the next video we're
00:18:47.160
going to touch on this we're going to
00:18:48.539
really cover like how can we use slots
00:18:50.760
to leverage this principle when we are
00:18:53.700
building uis make our abstractions much
00:18:57.179
more generic and reusable alright so
00:19:01.260
let's take what we learned now about a
00:19:04.320
parametric polymorphism and also slots
00:19:07.280
to actually show you how we would
00:19:10.140
actually use that knowledge to further
00:19:12.539
build out our to-do app and so if you
00:19:15.780
remember correctly because we swap these
00:19:18.059
out to be web components last time add
00:19:20.640
task no longer works instead it just
00:19:23.340
logs it to the console for us so if I
00:19:26.220
bring that in here you will see it
00:19:27.780
actually logs it to the console for us
00:19:30.179
so let us actually
00:19:32.280
split out this task view into reusable
00:19:36.419
components to kind of illustrate how we
00:19:38.460
can use slots and illustrate this
00:19:40.500
concept of make generic reusable
00:19:42.900
components so I already created a user
00:19:46.380
action here let's create another one
00:19:49.679
which is a user input JS and then lastly
00:19:54.840
let's do screen
00:19:57.440
overlay.jit and maybe form wrapper all
00:20:01.679
right so let's start building out user
00:20:04.200
input so we can grab everything that we
00:20:06.960
have with buttons thus far and let's
00:20:09.419
also in our actual HTML add those where
00:20:13.320
needed so at the moment we have this
00:20:15.900
button here but we want to swap that out
00:20:17.940
to be user action and similar to what I
00:20:21.840
showed last time you might be tempted to
00:20:23.640
go label and that would for example be
00:20:26.039
the label of the button but you can
00:20:29.039
actually leverage composition and slots
00:20:32.220
as a means to make this much more
00:20:34.440
flexible and extendable so let's say you
00:20:37.080
actually just pass in there what you
00:20:39.059
want inside the button and so in this
00:20:41.640
case we just want the text task but we
00:20:44.100
can maybe but we can pause an image we
00:20:45.960
can pause anything in there let's just
00:20:47.820
create all of this again so let's just
00:20:49.559
say const and let's create template and
00:20:51.660
that would be document create element
00:20:54.299
template and then the template inner
00:20:57.240
HTML is as follows well now it's just a
00:21:00.900
simple button and so how do you
00:21:02.940
determine where what you put inside it
00:21:05.400
goes you actually just do slot like this
00:21:09.720
and so at the moment we only have a
00:21:12.720
single slot so that means that we don't
00:21:15.840
need to designate this whatever gets
00:21:19.020
passed in here it's just going to go
00:21:20.280
directly into that slot and you'll see
00:21:21.780
here it actually gets added so let's
00:21:24.660
also add some styling here as well style
00:21:27.960
so we can grab the previous button
00:21:30.720
styling and now we're encapsulating
00:21:32.159
loading it in the component itself very
00:21:34.679
simply it's just this but let's just
00:21:37.919
keep it button and let's just add the
00:21:40.080
class button we can straight up just
00:21:42.419
Target the element yeah I guess we can
00:21:44.580
it's much of the sameness I'll just do
00:21:48.179
this and so let us also just create the
00:21:51.659
class so user input extends HTML we only
00:21:56.280
want connected callback for now and what
00:21:58.980
we also want is we also want to create
00:22:00.780
our shadow Dom and we want that to be
00:22:02.640
private so we can say inner equals
00:22:05.520
attach this attach Shadow and the mode
00:22:09.900
is just closed and you might be seeing
00:22:12.840
that I'm getting these type of
00:22:14.760
recommendations again this is just
00:22:16.740
because I switched on copilot it's just
00:22:19.140
going to help me write this a bit
00:22:20.400
quicker I'm not necessarily going to
00:22:22.200
interfere with me trying to explain
00:22:24.299
principles but it's obviously just the
00:22:26.400
quality of life thing like a bit
00:22:28.020
expensive but it is part of my normal
00:22:29.820
workflow so obviously I can move much
00:22:31.799
faster if it is enabled but it shouldn't
00:22:34.620
affect actually me showing the principle
00:22:37.679
showing how I would do it it just saves
00:22:39.720
me a bit of typing here and there you
00:22:41.100
still need to have the Insight you know
00:22:43.080
when it's like absolutely just giving
00:22:44.760
you random crazy stuff and when it's
00:22:47.400
actually a good estimation of what you
00:22:49.500
want to type so what we want to do in
00:22:50.940
here is we want to say this in a pain
00:22:53.220
child template content clone okay and
00:22:56.460
let's just wrap it like that okay so we
00:22:59.039
take the template we take the content
00:23:00.539
and we clone it we can even split this
00:23:02.880
up into separate things write it like
00:23:05.220
this for readability because I am zoomed
00:23:08.159
in quite a ton and so let's just pass in
00:23:10.799
the node okay so we create a duplicate
00:23:13.020
of the template and then we just want to
00:23:15.480
do custom elements Define user input and
00:23:19.320
the user input class I actually see we
00:23:21.960
are working the wrong thing it should
00:23:23.880
actually be in the user action not user
00:23:25.980
input okay so let me just copy that and
00:23:28.260
let's just wipe this okay so now we're
00:23:30.059
in the right file and all of this seems
00:23:34.260
okay right so let's give it a go so we
00:23:37.260
need to import that into our scripts let
00:23:39.539
me just make this full screen so we're
00:23:41.700
not doing anything with the class itself
00:23:44.159
as we are with task adding over here
00:23:47.240
so let's pull in user action so what we
00:23:51.120
can also actually do is we can store
00:23:53.280
whether it's a custom element or not it
00:23:55.799
still extends basic HTML we can still
00:23:58.200
add the data attribute here so let's
00:24:00.120
have a look data add button and it
00:24:02.159
should still work whether it is a custom
00:24:04.080
element or our own one and we Define
00:24:07.020
user input uh user action there we go
00:24:09.900
all right and there's our styling now if
00:24:12.299
we click it still opens that so you see
00:24:13.740
we can even attach the event listener to
00:24:16.140
this and so let's say we want a
00:24:18.059
different style of Button as well okay
00:24:20.940
so let us create a setup for that just
00:24:23.940
create the internal value so let's say
00:24:25.559
importance and importance by default is
00:24:29.460
secondary and then we want to set down a
00:24:31.740
getter so set importance value and all
00:24:35.460
that does is it overrides importance but
00:24:38.520
we also want to include side effects
00:24:40.080
here so what we want to do is let's add
00:24:42.299
a second style here that is I think we
00:24:44.760
actually don't even have a hover effect
00:24:46.080
so that might even be worth doing so
00:24:48.120
let's do obviously on mobile we don't
00:24:49.919
get hover it's just for now do something
00:24:51.960
like this okay just a very slight hover
00:24:54.179
effect but then we also want a modifier
00:24:56.220
so we can set button and here like I
00:24:58.740
maybe still use Bim it's not as
00:25:01.140
important to use Bim specifically
00:25:03.299
anymore but I don't know just a habit
00:25:07.080
so when it is primary we want to make
00:25:10.260
the background black but by default and
00:25:13.020
we want to make the text white but by
00:25:14.940
default it's the other way around so the
00:25:17.640
text is white and the color is black and
00:25:21.659
we also want a border that is one pixel
00:25:24.419
solid black and so while we're at it
00:25:26.940
let's actually make our buttons blue
00:25:28.200
instead and I also want to show you
00:25:29.580
another thing so this is variables can
00:25:32.580
actually pierce the actual Shadow Dom so
00:25:35.880
what we can do is let us create some
00:25:38.580
variables up here and let's just say
00:25:40.559
color primary and let's just get a nice
00:25:43.500
blue so I just use something like
00:25:45.860
hoolers and I just press until I get
00:25:49.500
something nice let's go with this
00:25:51.539
turquoise color so there we go so let's
00:25:54.240
take this one let's maybe make it a bit
00:25:57.360
darker so let's go with something like
00:26:00.299
so let's also get a hex to rgba
00:26:03.659
converter so just take this one and put
00:26:06.840
it them there and here we go rgbn so the
00:26:09.900
reason why I do this is because then I
00:26:12.179
would go like 100 opacity and the last
00:26:15.059
one indicates opacity so I'm just going
00:26:16.919
to create four versions of this so a
00:26:19.740
version that is 100 a version that is 75
00:26:22.140
version that is 50 and a version that is
00:26:25.020
25. so I have at least four different
00:26:27.740
gradations of this color so for hover
00:26:30.779
effects and and all of that stuff all
00:26:32.880
right so let's actually bring this in
00:26:35.279
here also close this for now just super
00:26:38.159
quickly just so you can see a bit better
00:26:40.140
so let's say the border is VAR color
00:26:43.679
primary but we want color primary a
00:26:46.140
hundred so you can't see it there uh the
00:26:49.320
line might be a bit too thin but and
00:26:51.600
also over here you might be able to see
00:26:54.720
it super slightly and it might even be
00:26:56.940
worth pumping up the font weight a bit
00:26:59.039
and the font size they just make it a
00:27:01.679
bit more pronounced and then the primary
00:27:03.960
version is just the full color and white
00:27:07.559
so what happens when you actually toggle
00:27:11.100
it let's mark this up so importance can
00:27:15.779
either be primary or secondary so we can
00:27:18.840
then say if let's also do a get
00:27:21.860
importance and that is just going to
00:27:24.240
return the private value the importance
00:27:27.539
like that let me just spell return right
00:27:29.580
and it should also be a method like that
00:27:32.039
so we can say if value is primary so
00:27:35.340
here we have the assignment but then
00:27:37.440
after that we actually do the side
00:27:39.179
effects so the side effects are that if
00:27:42.179
it is important let's say else and we
00:27:44.940
also what we also want to do maybe up
00:27:46.620
there is we want to say if you're trying
00:27:48.000
to set it to what it already is so if
00:27:51.059
value equals this importance just return
00:27:55.260
don't do anything okay stop the function
00:27:58.140
right here return the function okay
00:27:59.700
otherwise continue down here so if it is
00:28:01.980
primary then let's also just make a new
00:28:05.039
value for readability if it is primary
00:28:07.799
then what we want to do is we want to
00:28:10.380
add a class to this button here so just
00:28:14.820
because this component is so small let
00:28:16.919
me actually just show you how you would
00:28:18.360
do it even you know without something
00:28:20.159
like this so we just Target the button
00:28:21.840
directly and we just have a primary
00:28:24.600
class if your components get too big
00:28:27.179
don't do this because even components
00:28:30.059
themselves can get unwieldy but I just
00:28:32.159
want to show you like if you want to
00:28:33.900
just straight up use the element in a
00:28:35.580
component because it's encapsulated you
00:28:38.100
can do that without too many problems
00:28:40.080
because that also means that we can go
00:28:41.940
this so in the shadow Dom query selector
00:28:45.000
button so let's also just as last time
00:28:48.779
after we actually connect the component
00:28:52.020
let's just create an element and for now
00:28:54.360
elements just has button and it starts
00:28:57.600
as null so type HTML button element or
00:29:01.500
null and then over here we obviously
00:29:03.480
just do this element and we just set
00:29:06.419
button in a query selector button all
00:29:08.880
right so that means we should have
00:29:11.159
access to it over here if you try and
00:29:13.919
set it so we can go this elements button
00:29:17.820
and class list add primary otherwise we
00:29:21.480
remove it just add and remove that class
00:29:23.760
so what we then also do after this has
00:29:26.460
been done we just manually set
00:29:29.039
importance so remember not the private
00:29:31.440
one the public one so we can get the
00:29:33.539
side effects and we can say this get
00:29:36.120
attribute otherwise fall back to
00:29:38.220
secondary but it should already be
00:29:40.860
secondary so we don't need to worry
00:29:42.720
about that so why do we get this error
00:29:44.820
because we don't have a guarantee that
00:29:46.679
it is either of these what we can do is
00:29:49.080
let's get the attribute first let's just
00:29:51.659
say
00:29:52.520
importance so what we can say is we can
00:29:55.919
say if importance is not primary and
00:30:00.360
it's not secondary but another thing we
00:30:03.059
also need to add we need to add a
00:30:04.380
fallback here that says a secondary so
00:30:07.080
in other words if if it doesn't get get
00:30:09.720
anything just fall back to secondary all
00:30:11.820
right so at this point we should be
00:30:14.100
confident in terms of that importance
00:30:16.320
should be primary or secondary there we
00:30:18.720
go so then you can just say this
00:30:20.760
importance just the public one equals
00:30:23.520
importance and it is automatically going
00:30:26.220
to fire that side effect so let's have a
00:30:28.740
look and let's see if we go here and we
00:30:31.679
just set importance to primary there we
00:30:34.799
go that toggles it out oh this doesn't
00:30:36.840
seem right okay we can have a look at
00:30:38.100
that in a second oh it's because there's
00:30:39.899
no text in hello there we go and that's
00:30:43.320
maybe an error state that you might want
00:30:45.360
to embed in your actual user action so
00:30:48.480
you might even go check if nothing is
00:30:51.120
passed in as a slot then throw an error
00:30:54.059
and we can even do this in the
00:30:55.500
Constructor already we don't need to
00:30:57.000
wait for it to connect and also another
00:30:59.760
thing is I say I mentioned super briefly
00:31:03.679
and so effectively what super does is
00:31:07.380
super just calls the Constructor on
00:31:11.820
um the the inherited class so like the
00:31:16.320
Constructor on HTML element it's not
00:31:18.539
needed specifically for HTML element but
00:31:21.120
it is a good practice to just call Super
00:31:23.159
when you are extending things so you
00:31:25.860
generally want to have a Constructor
00:31:27.120
that has super in it if you create a
00:31:29.580
Constructor so what we can do is we can
00:31:32.760
actually check the inner child the inner
00:31:34.740
HTML of this actual component and so
00:31:37.679
let's just say you know if there is no
00:31:39.240
inner HTML or if the inner HTML is an
00:31:42.059
empty string then throw an error so
00:31:44.279
let's just quickly see golf so these
00:31:46.260
both have you know HTML so we can say if
00:31:48.960
this inner HTML is a string and we also
00:31:52.440
want to trim it so at least there needs
00:31:54.419
to be a character in there or there is
00:31:56.100
no inner HTML then just throw an error
00:31:59.159
that says throw new error user action
00:32:02.159
must have content so we have hello and
00:32:04.500
we have add task and add task triggers
00:32:06.480
that all right so let us just remove
00:32:09.000
this hello from here so let us just set
00:32:12.360
this maybe two important primary
00:32:14.899
effectively because we have now bundled
00:32:17.820
this little user action thing here we
00:32:22.140
can actually just pull that into another
00:32:24.659
project so I want to show you something
00:32:26.760
really cool so I just created a
00:32:29.279
completely new blank project here and
00:32:32.100
this is the magic of encapsulation so
00:32:34.679
let me just do that for you the only
00:32:37.020
thing we do is let's add two buttons so
00:32:39.179
let's say user action and this is just
00:32:42.059
secondary by default hello and the other
00:32:44.880
one is primary user action importance
00:32:48.240
primary and world all right and so let's
00:32:52.740
pull in that little Javascript file for
00:32:55.440
that so let's just have our script
00:32:57.179
Source up here and we're just pulling in
00:32:59.580
user action and if fur and type although
00:33:02.880
we're not doing any Imports and it just
00:33:04.740
just as a good habit let's just say type
00:33:06.600
module and let us have a look let's open
00:33:09.419
this up okay so something interesting is
00:33:11.700
happening here
00:33:13.320
um this seems to be like some type of
00:33:16.080
styling
00:33:17.580
um and the reason is one of the problems
00:33:20.039
here is that we actually
00:33:23.100
um these are hard-coded so for example
00:33:25.980
so these are the default Styles and also
00:33:28.679
like for example the white that we
00:33:31.019
didn't get from a CSS variable that we
00:33:34.140
actually just set the word white there
00:33:36.120
but you can see it brings everything
00:33:38.100
else in and it's just because we don't
00:33:40.320
have those variables so let me show you
00:33:41.940
if we add the variables actually in here
00:33:44.480
it should work and we also need to
00:33:47.640
remember to bring in this into our CSS
00:33:51.600
okay so there we go Styles like that and
00:33:55.320
let's have a look now hey all right they
00:33:57.720
are our Styles so there is an entire
00:34:00.240
world of people just publishing web
00:34:03.120
components that you can actually just
00:34:04.860
pull into your project directly like
00:34:07.260
this
00:34:08.580
um but if we want to for example do that
00:34:10.859
we might need to just give it some basic
00:34:12.899
styling so that this isn't needed so not
00:34:15.719
only do we want to do that we also want
00:34:17.580
to give people a bit of control so that
00:34:19.560
they can actually set it themselves so
00:34:22.020
let's say and I'm just going to do
00:34:23.820
inline style here
00:34:25.379
you can actually Target user action
00:34:27.719
itself and then actually pass CSS set
00:34:31.859
the CSS on it in the same way you would
00:34:33.839
maybe set the CSS on a div or an H1 or
00:34:36.960
whatever but you can create your own
00:34:38.399
custom CSS that you can set so you can
00:34:41.159
pause your own custom actual variables
00:34:44.219
in there so in the same way that we did
00:34:47.219
you know root like that and set
00:34:50.460
variables to the root of a document you
00:34:52.859
can actually set variables for a
00:34:55.560
specific element like this as well so
00:34:57.660
let's maybe give these a bit more
00:34:59.880
General names so if we go in here let's
00:35:03.839
say that you actually let's do color
00:35:06.540
primary like that and let's just replace
00:35:09.300
the white with actual secondary so you
00:35:11.460
can actually set anything you want and
00:35:13.440
then the hover effect for the hover
00:35:15.599
effect by default let's say what it does
00:35:18.720
it sets the background to primary
00:35:22.160
but it sets the opacity to that and then
00:35:27.060
for if it is actual primary then it just
00:35:30.240
sets the opacity let's just set the
00:35:32.280
opacity bit lighter over there so this
00:35:34.380
is not prettier styling but it gets the
00:35:36.660
job done and we just need to say when it
00:35:38.579
is primary let me just set this to
00:35:40.740
primary this is actually redundant we
00:35:43.680
don't actually need this so let's just
00:35:45.839
move it over here and so let's set these
00:35:49.079
so we can do in user action color
00:35:52.079
primary is purple and color secondary is
00:35:56.520
yellow cool check that out all right
00:35:58.920
right so you can actually announce
00:36:01.140
completely encapsulated if you pull in
00:36:03.180
this file you have everything you need
00:36:04.940
and you have this little component that
00:36:07.380
you can do with what you want the
00:36:08.940
question is given that you can do this
00:36:11.339
can you actually publish your component
00:36:13.859
for other people to use and the answer
00:36:15.900
is yes and here is where we're going to
00:36:18.480
start relying on third body things we're
00:36:21.359
going to actually start pulling in some
00:36:23.040
third-party JavaScript libraries so if
00:36:26.280
you go to web components so
00:36:28.700
webcomponents.org there's a big
00:36:30.660
repository of actual things you can get
00:36:34.440
so let's say we want actual pop-up here
00:36:37.619
is a list of actual pop-ups that have
00:36:40.140
been published you can even publish your
00:36:41.760
own element up here but generally what I
00:36:44.940
prefer to do is to use an actual design
00:36:48.180
system of components so my preferred one
00:36:52.320
is material design so material design
00:36:54.960
web components the material design is
00:36:58.440
the design design system that Google
00:37:00.119
uses internally YouTube and so forth
00:37:02.700
actually has a lot of like web
00:37:04.980
components actually running and so to
00:37:07.440
kind of show you if we for example go to
00:37:09.859
settings I'm pretty sure if we inspect
00:37:13.020
this should be some web components here
00:37:14.940
and here you see YT guide manager ytmdx
00:37:19.619
manager YT history YT mini player so you
00:37:23.280
know if I click there like if this is a
00:37:24.900
component you know manager like this is
00:37:27.540
a component and you'll see they actually
00:37:30.060
mix this in with like regular stuff so
00:37:32.460
for example they still have a div here
00:37:34.680
and so forth
00:37:36.119
um you know they have mastered but in
00:37:37.980
mastered is you know this actual
00:37:40.320
component so Google is using web
00:37:42.720
components uh someone else is also using
00:37:45.359
web components quite a bit as GitHub so
00:37:47.460
if we have a look on GitHub
00:37:49.380
um you'll see there are a couple of
00:37:50.880
things here like turbo frame and you
00:37:53.160
know they actually have a template in
00:37:54.599
here so and they have for example
00:37:56.640
notification shelf Watcher so the cool
00:37:58.800
thing about web components is you can
00:38:00.660
mix and match it with regular HTML as
00:38:03.480
you go so you can pull them into the
00:38:05.400
extent that you want to or you can just
00:38:06.780
leave them entirely and just use regular
00:38:09.060
HTML given that this is the case given
00:38:11.220
that there are a lot of companies out
00:38:12.420
there using web components
00:38:14.400
um they've actually published some of
00:38:16.200
this for people to use and say hey if
00:38:18.180
you want kind of like this element
00:38:19.380
yourself just use our actual design
00:38:21.660
system and there are actually tools for
00:38:23.880
building Design Systems with web
00:38:25.380
components so for example stencil.js is
00:38:28.859
a very well known one
00:38:30.660
um used by like Amazon and so forth so
00:38:33.359
it is a much more advanced tool but it
00:38:35.579
allows you to build web components so
00:38:38.220
once we get to the actual Frameworks
00:38:41.400
um these do kind of their own
00:38:42.599
implementation of components some of
00:38:45.839
these components are actually built on
00:38:48.119
top of web components so for example
00:38:49.920
like svelt and View and so forth but
00:38:53.520
regardless you can still use web
00:38:55.500
components in actual Frameworks and one
00:38:58.440
of the better benefits of web components
00:39:00.480
even if you're using a framework is that
00:39:03.359
you can actually use them between
00:39:05.099
different Frameworks so you can create a
00:39:07.920
web component and use it in any
00:39:09.839
JavaScript framework and this is kind of
00:39:12.000
what something like stencil does but so
00:39:14.220
let's look at the Google one so we can
00:39:17.040
go over here so they have a lot of like
00:39:19.740
cool things here some of it isn't 100
00:39:22.320
stable just yet so you can use it just
00:39:26.520
keep in mind that they are still working
00:39:28.200
on it they are still improving it and
00:39:31.020
then here are a couple that they have
00:39:32.760
actually planned for the future so
00:39:35.160
um let's just Google a list of web
00:39:37.740
component Design Systems so this
00:39:41.540
component.gallery is amazing and like
00:39:43.859
they actually have a list of things that
00:39:45.300
you can use so you know let's say you
00:39:46.920
want to Avatar and then you can actually
00:39:48.839
just fold to buy Web components okay
00:39:50.640
here are all the different avatars that
00:39:53.280
you can use so one that I really enjoy
00:39:56.700
working with is a shoelace
00:39:59.339
um and it's the shoelace dot style over
00:40:02.460
here and so they have some cool stuff so
00:40:04.500
you know here's a button and so forth
00:40:06.119
and you might prefer something else but
00:40:08.220
I'm just going to continue working with
00:40:09.839
shoelace
00:40:10.980
um just as an example of how you would
00:40:13.320
actually use a third-party design system
00:40:16.500
so what you need to do is you just need
00:40:19.680
to add these two files to your HTML so
00:40:23.520
this brings in the components so if we
00:40:26.460
add it to the top of our file so let's
00:40:29.280
just delete all of this over there and
00:40:31.800
let's pull that in and let's give it a
00:40:34.920
try so let's try SL button so you'll see
00:40:37.859
they're actually prefix prefixed it with
00:40:40.200
slsl being shoelace in this case let's
00:40:42.900
do an SL button down here click me and
00:40:46.020
let us look at our site there we go
00:40:49.140
there is a nicely formatted button and
00:40:51.420
whatever and let's see what select let's
00:40:54.180
look at the shoelace site and let me
00:40:56.579
just zoom in a bit more for readability
00:40:58.079
and you even even theme it yourself you
00:41:00.359
can even you know change the colors and
00:41:02.220
so forth similar to what we did with our
00:41:03.960
components there's even a dark theme and
00:41:05.940
so forth you can create your own theme
00:41:07.920
and so forth there's a lot of really
00:41:10.320
great documentation on here go into the
00:41:13.200
components themselves and like apply
00:41:16.140
specific styling with kind of this part
00:41:18.599
I'll show you in a second what this part
00:41:20.579
is as well but let's just maybe assemble
00:41:23.700
a super quick dialogue so and you can
00:41:26.940
have a look here and you can just open
00:41:28.260
the source and see how they did it let's
00:41:30.780
just pull all of that in here okay so
00:41:33.540
currently that doesn't do anything and
00:41:35.220
it's because we still need to wire up
00:41:36.960
the behavior this just gives us the
00:41:38.820
components but they do have an example
00:41:41.160
here of how they wire it up so let's
00:41:42.839
just use what they have as an example so
00:41:46.200
let's just put it in here I'm also just
00:41:47.579
going to do an inline script here and so
00:41:49.920
what they do is they grab the dialogue
00:41:53.160
by means of dialogue Focus but we can
00:41:56.040
even just go back to our data attribute
00:41:59.280
example so we can just say data
00:42:02.780
dialogue open and we can just select
00:42:05.940
that because for all intents and
00:42:07.560
purposes web components are just plain
00:42:09.660
HTML the input let's just leave that for
00:42:12.359
now let's leave all these things for now
00:42:14.460
we just want to be able to open the
00:42:16.079
dialog so we can just say on this
00:42:18.960
element add an event listener let's also
00:42:21.900
just go this SL button down here so
00:42:24.839
let's just say and this should actually
00:42:26.520
be the dialog itself it shouldn't be the
00:42:28.800
so this is just data let's do dialog and
00:42:32.280
down here let's do data okay so we just
00:42:35.820
have data dialog and data button and on
00:42:39.900
that button let's add an event listener
00:42:41.820
let's also just do a quick data close
00:42:44.339
here and you'll see here that actually
00:42:46.380
specify the slot that it should go to so
00:42:48.900
I'm going to talk very quickly about
00:42:50.160
Parts I'm quickly going to talk about
00:42:51.480
slots named slots in a second so up
00:42:54.300
until now we've just passed it directly
00:42:56.160
as slots you can actually set a named
00:42:59.760
slot and this is where slots get really
00:43:01.740
powerful but so let's do data close and
00:43:04.560
that is just the close button so data
00:43:06.960
close and let's add an event listener to
00:43:09.060
that add event listener click dialog I
00:43:11.819
guess it Targets this and it shows it
00:43:13.260
and it hides it so if we look at the
00:43:15.660
shoelace documentation if you read the
00:43:17.760
documentation and it's full you know
00:43:19.319
like they give some tips here's an
00:43:21.000
example scrolling so they give loads of
00:43:23.819
other things for you and then down here
00:43:26.099
they actually give you what are the
00:43:27.480
slots so there's a label slot there's a
00:43:29.280
header action slot there's a footer slot
00:43:31.319
they even have a section in terms of
00:43:33.599
where they explain slots a bit and then
00:43:35.880
attributes what are some attributes that
00:43:37.380
you can set you can set it to open you
00:43:38.880
can set the label you can set no header
00:43:41.280
and these are events that fired so you
00:43:43.859
know you can listen for when it opens
00:43:45.480
you can listen for you know when it
00:43:47.640
closes you can listen for these events
00:43:49.319
and then methods that these are actually
00:43:50.760
these are actually things that you can
00:43:52.140
call on the element itself and then you
00:43:54.660
can even pass CSS properties uh like the
00:43:57.720
width you know let's say you want to
00:43:59.040
make it wider and CSS Parts as well so
00:44:02.460
there's a ton of stuff here and this is
00:44:04.920
so flexible that you can build an entire
00:44:07.079
site just using this and never creating
00:44:09.839
your own actual CSS or HTML and all that
00:44:13.859
you do is you use these ready-made
00:44:15.599
components and Geo users write the logic
00:44:18.300
you just write what should happen but
00:44:20.339
you use their input you use their
00:44:22.020
buttons you use their dialogue and so
00:44:23.700
forth and that saves you a ton of time
00:44:25.500
and once we're going to be talking about
00:44:26.880
like Frameworks like I'm also going to
00:44:29.579
introduce some of these so one that I
00:44:31.859
use day in day out is one called mui and
00:44:35.640
it is for react I mostly write react
00:44:39.780
code and you can see this is really
00:44:42.359
extensive in terms of the things that it
00:44:44.220
gives you you know so if you look at the
00:44:45.960
buttons you know like these are the
00:44:47.520
buttons it gives you stuff like you know
00:44:49.380
check boxes it gives you like a rating
00:44:51.420
thing a toggle button uh chips like this
00:44:57.300
um tooltips so for for example if I
00:44:59.940
hover over this you know like that type
00:45:01.980
of tool tip different types of alerts
00:45:04.079
and so forth this really helps speed up
00:45:06.660
development and a lot of these it is
00:45:08.700
this exact principle of polymorphism
00:45:11.000
that actually allow us to extend these
00:45:14.819
and actually build on top of them to the
00:45:18.180
extent that it almost becomes completely
00:45:19.980
custom but you're using these as a base
00:45:22.440
to build on top on and that's generally
00:45:24.960
how we want to be using libraries we
00:45:27.300
want to be using libraries to extend our
00:45:30.060
own code to show you an example material
00:45:33.180
design actually has this part where they
00:45:35.460
actually show you water that a couple of
00:45:37.500
different sites and these are all built
00:45:40.020
with material design components but if
00:45:42.180
you look at them they look vastly
00:45:44.579
different you can barely tell that it
00:45:46.560
uses the same underlying actual
00:45:49.200
components so they look vastly different
00:45:51.599
but it's up to you how much you want to
00:45:53.880
actually customize it and in our example
00:45:55.920
I'm not going to customize it too much
00:45:57.599
because I actually want you to guys to
00:46:00.420
get better at JavaScript so I'm going to
00:46:02.099
be spending more time here going forward
00:46:04.200
talking about JavaScript and maybe less
00:46:05.700
time talking about HTML and CSS if you
00:46:08.579
feel confident with HTML and CSS or if
00:46:12.119
you want to actually add a bit of your
00:46:13.859
own styling a bit of your own design you
00:46:16.440
can extend these components if you just
00:46:19.380
read the documentation or if you want to
00:46:21.660
go all out maybe create your own
00:46:23.460
components and it's you know it's not
00:46:25.319
that cut and dry maybe you can pull in a
00:46:27.660
couple of third-party components maybe
00:46:29.760
you can create some of your own
00:46:31.440
components in between and so forth so it
00:46:34.200
gives you a lot of space to kind of
00:46:36.060
figure out how much of your own styling
00:46:38.280
do you want to bring in but a lot of
00:46:41.099
these libraries actually give us a lot
00:46:43.200
of Base components to start working with
00:46:45.240
and speed up our development time all
00:46:47.640
right so just super quickly before we
00:46:50.280
end this author I just want to quickly
00:46:52.079
chat about two things so firstly I'm
00:46:54.660
just going to remove these that I
00:46:56.220
created here because in the next video
00:46:59.160
um I actually want to show you how we
00:47:01.260
can actually replace all of this even
00:47:04.079
including our user action that we just
00:47:06.119
created now with actual third-party uh
00:47:09.960
components from shoelace or maybe just
00:47:12.720
do a quick example where I also show how
00:47:14.700
you can use Google material design
00:47:17.520
components as well but yeah so then we
00:47:20.220
can just focus on the logic and leave
00:47:22.260
the presentation and the HTML and the
00:47:24.000
CSS up to the actual design system that
00:47:27.060
we're using so what I want to do now is
00:47:29.819
if we just choose our user action here I
00:47:31.920
just super quickly want to show
00:47:34.140
um how we can actually use slot in a
00:47:37.560
more specific way so at the moment we
00:47:41.040
only have a single slot and whatever we
00:47:42.720
pass goes here so this is obviously a
00:47:45.540
very contrived example
00:47:48.300
um but I just want to show the principle
00:47:49.920
so we can go slot and let's just say
00:47:54.480
name start and Slot name end and let's
00:48:00.060
just keep this as is so this one over
00:48:03.000
here let us just put
00:48:05.160
um in Brackets you know let's just end
00:48:07.140
so this is what it's going to be unless
00:48:09.480
you pass something to the slot
00:48:12.000
um this is going to show nothing unless
00:48:14.339
you pass something to the slot and
00:48:16.619
anything that's not named is going to be
00:48:19.020
passed to just the unnamed slot so let
00:48:21.839
me show you quickly what that looks like
00:48:23.520
so if we go here so let me also just
00:48:26.040
remove all of this while we're at it and
00:48:29.760
so we have this data button importance
00:48:32.060
and we are adding task let's just say
00:48:35.700
you know that this is a span but then
00:48:38.579
what we want to do is we want to maybe
00:48:40.560
pause a link and that link goes to http
00:48:44.400
s you know google.com you know and
00:48:47.700
Target blank and let's just say click
00:48:50.460
here obviously a really bad idea to pass
00:48:52.680
a link into an actual button but it is
00:48:54.839
what it is then we need to actually on
00:48:57.420
this itself say you know slot start and
00:49:01.200
then it's going to assign this element
00:49:02.940
to the start slot and this to the other
00:49:06.060
one and let us have a look and see how
00:49:08.280
that looks and here we go obviously
00:49:10.680
styling is a nightmare but this is just
00:49:13.020
to show the principle all right
00:49:15.480
um and just to show if we then assign it
00:49:17.460
to end so at the moment it just puts the
00:49:21.359
actual placeholder one there so if we
00:49:24.359
just rename this to end it's going to
00:49:26.280
override the placeholder one that we
00:49:28.800
have but it's going to leave this here
00:49:31.920
and if you can't see it you know there
00:49:33.599
is the click here and so you might be
00:49:35.940
like okay cool big deal this is very
00:49:37.500
similar to attributes uh but so here's
00:49:40.020
the thing you can pause anything in
00:49:41.700
there we can like if we really wanted to
00:49:44.099
we can pause an image you know so let's
00:49:46.200
just say let's get Lauren pick some so
00:49:48.359
let's just grab a random lorem pick some
00:49:50.339
image and let's just say that's the
00:49:52.200
default and for end we can even go and
00:49:55.920
pass like user action into user action
00:49:59.099
itself so this is where it gets crazy so
00:50:01.800
you know user let's pause user action
00:50:04.200
two times into itself and then you know
00:50:07.560
inside that let's have an unordered list
00:50:09.720
but this is obviously slot all right and
00:50:13.260
let's have a look look at this this is
00:50:15.300
absolute crazy stuff but you know it
00:50:17.940
just shows how powerful it is you can
00:50:19.680
actually pause the thing into itself
00:50:22.440
several times
00:50:24.119
um you can pass entire structures entire
00:50:27.000
abstractions into it this isn't merely
00:50:29.760
just setting a specific string value and
00:50:32.819
so by using this efficiently we can
00:50:35.640
really create we can create super
00:50:38.220
maintainable and easy to read actual
00:50:41.040
coding logic and we can even intercept
00:50:43.680
it and do things with it before we spit
00:50:46.260
it back out almost like a center and a
00:50:48.180
ghetto all right but we're going to dive
00:50:49.800
much more into the power that an
00:50:52.559
approach like this unlock unlocks for us
00:50:55.079
and specifically when we get to some
00:50:57.900
Frameworks we're also going to look at
00:50:59.160
jsx which further Builds on this and
00:51:02.819
actually treats these things as actual
00:51:05.579
functions and we can actually bind it to
00:51:08.160
a specific function so let's just do a
00:51:10.619
much more conservative one again let's
00:51:13.020
just go our task and so now I'm quick
00:51:15.960
just want to show how part Works part is
00:51:19.319
related but it's not exactly the same so
00:51:22.920
let's say in my user action I have
00:51:26.640
something that is always there which is
00:51:28.980
let's say you know a actual Arrow so let
00:51:32.520
me just get an ASCII Arrow let's just
00:51:34.500
say something like that okay so this is
00:51:36.420
always in my component all right so we
00:51:38.280
have that arrow and let's say we want to
00:51:40.319
allow people to actually be able to
00:51:42.300
style that specific arrow and all that
00:51:45.420
we do then is we do part equals and we
00:51:49.079
can call it anything and then in CSS you
00:51:52.079
can Target that specifically so let's do
00:51:54.780
some inline style here again let's say
00:51:57.599
let's target this specific one let's
00:51:59.400
just say class example okay and we're
00:52:02.220
going to Target example we can do things
00:52:05.220
like oh we want the background to be red
00:52:07.800
okay so let's have a look first and
00:52:10.079
foremost that doesn't do anything
00:52:11.400
because the Dom you can't actually
00:52:14.700
change the CSS from outside of it but
00:52:18.839
what we can do is we can grab a specific
00:52:21.300
part and style that so what we can do is
00:52:24.000
we can say like that part and what part
00:52:27.540
we want arrow and maybe the arrow we
00:52:30.480
want to make the color red and there we
00:52:32.940
go awesome so it allows you to like
00:52:34.740
Target specific things yeah and that
00:52:37.680
isn't about it so slot spots obviously
00:52:40.559
these are very straightforward examples
00:52:43.200
it gets very complex you can build
00:52:45.240
really complex things a lot of advanced
00:52:47.940
things with just these basic tools and
00:52:50.760
we're going to be showing a bit more of
00:52:52.380
that as we go ahead but in the next
00:52:54.900
lesson what I'm going to do is I'm going
00:52:56.339
to bring in some of these shoelace
00:52:58.920
components and then I'm going to be
00:53:01.020
talking a bit about functional
00:53:02.819
programming and we've spoken a lot about
00:53:05.099
object orientated programming up until
00:53:06.960
now and I'm not going to rewrite the
00:53:09.780
entire app in a functional style but I'm
00:53:12.000
going to be showing how we can use
00:53:14.099
functional programming here and there
00:53:16.200
and functional principles to actually
00:53:19.099
solve problems in our app actually make
00:53:21.599
our app more resilient so I will see you
00:53:24.000
guys in that video