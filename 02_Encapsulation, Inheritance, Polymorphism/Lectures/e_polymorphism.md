Please write clear and comprehensive lecture notes and lesson content for this lecture:

00:00:00.140
in this lesson we are going to cover
00:00:03.540
something called poly morphism so last
00:00:08.400
night my wife actually asked me like hey
00:00:10.860
what are you doing tomorrow and I
00:00:12.780
actually told her I'm doing a video
00:00:15.719
um for the students on polymorphism and
00:00:18.300
her immediate response was wow that
00:00:21.000
sounds like a really scary word and you
00:00:24.720
might actually be having the same
00:00:26.580
response it does sound very scary uh
00:00:29.699
polymorphism very similar to higher
00:00:32.700
order functions which we're going to
00:00:34.440
discuss later sounds a lot scarier than
00:00:37.500
it actually is so as with a lot of words
00:00:40.020
that sound really scary
00:00:42.000
um it actually comes from ancient Greece
00:00:44.760
and we could actually break the word
00:00:46.500
down to get a sense of what it means so
00:00:49.140
poly effectively means many so you can
00:00:52.020
even think about something in JavaScript
00:00:54.420
which shares the same name like a poly
00:00:57.719
fill but the word polyfall in
00:01:00.239
programming actually comes from an
00:01:03.600
actual material that is called polyfall
00:01:05.939
um I actually use it around the house
00:01:07.439
quite a bit you can effectively use it
00:01:09.240
to seal any crack in the wall or you
00:01:11.580
know if you're pulling out a nail to
00:01:13.200
fold that hole so effectively it's poly
00:01:15.720
full it allows you to fill various
00:01:18.659
different things it's not you know
00:01:20.340
exclusively for a single purpose and so
00:01:23.400
effectively in JavaScript or in the web
00:01:26.280
when we talk about polyfill which kind
00:01:28.140
of borrows from this if we look on mdn
00:01:30.360
it says effectively a polyfill is a
00:01:32.220
piece of code used to provide modern
00:01:34.680
functionality in other words when we
00:01:37.439
spoke about what exactly is Javascript
00:01:40.140
we spoke about all the different
00:01:41.759
versions of ecmascript so what you can
00:01:44.400
do is if you're using newer features but
00:01:48.240
you also want to support browsers that
00:01:50.700
don't have those features you can use a
00:01:52.439
polyfold so let me show you an example
00:01:54.840
of a polyfold if we go on mdn and we
00:01:58.799
look at pad start or pad end and now you
00:02:02.520
should also understand what this
00:02:03.840
prototype means if you see dot prototype
00:02:07.200
on mdn that effectively means that this
00:02:11.640
is on any string in JavaScript so all
00:02:16.260
strings inherit from this prototype so
00:02:18.959
pad start can be run on any strings so
00:02:21.420
for example if you have a look here you
00:02:24.239
can see you know so string one you can
00:02:26.580
run pad start on that so the previous
00:02:29.280
discussion that we had about prototypal
00:02:31.319
chaining should also help you understand
00:02:33.420
the mdn documentation a bit better as
00:02:36.000
well but the key takeaway here is that
00:02:38.400
there are some browsers that don't
00:02:40.080
support bad start so let's have a look
00:02:42.660
here it is quite widely supported but
00:02:45.239
for example versions of chrome below 57
00:02:49.440
or versions of safari below 10 and don't
00:02:53.220
support it so if we go down you'll see
00:02:55.620
actually a link to where we can get the
00:02:58.260
polyfill from npm we haven't touched on
00:03:00.900
npm just yet so let's just do a quick
00:03:03.780
search in terms of bad start polyfill
00:03:07.379
JavaScript let's have a look here and
00:03:10.379
let's just look at this file here and
00:03:12.239
here you go and you'll see that it
00:03:14.459
actually extends the prototype to add
00:03:17.580
that so is that a good thing or a bad
00:03:19.920
thing this is a bit of a gray area
00:03:21.360
because extending the prototype to add
00:03:23.879
custom Behavior to a browser is a bad
00:03:27.239
thing but this is a bit more nuanced
00:03:29.220
because what happens is this code
00:03:31.800
actually checks if the current browser
00:03:35.819
supports bad start and in other words it
00:03:38.459
says you know if it does support pads
00:03:40.620
don't just use the actual pad start
00:03:42.720
method if not
00:03:45.180
add this actual function in the place of
00:03:47.879
bad start and this function just
00:03:50.340
emulates the behavior with normal
00:03:52.739
JavaScript
00:03:54.180
um that is supported in that browser
00:03:56.040
then repolifers are considered to be a
00:03:59.040
good thing but there is a bit of nuance
00:04:01.019
to it as well and I'll maybe discuss
00:04:03.540
that Nuance at a later point but now if
00:04:07.140
you just want to plug and play way of
00:04:09.360
adding polyfolds you can actually just
00:04:10.920
use polyfold.io and so what polyfill IO
00:04:14.459
does is it's just an actual package or a
00:04:17.820
script that you include and so you if I
00:04:20.339
effectively say what are the things you
00:04:21.959
want to poly for and then you just pull
00:04:24.479
that into your HTML but we will touch on
00:04:26.639
this at a later Point all right so back
00:04:29.280
to polymorphism not to be confused with
00:04:31.979
polyfilling
00:04:33.660
um but I thought it was just worth
00:04:35.040
touching on this really just to point
00:04:36.900
out that these are two different things
00:04:38.699
but they also do share the root word of
00:04:41.820
poly meaning many so this is many any
00:04:45.720
different folds so in other words it can
00:04:49.560
plug a lot of JavaScript functionality
00:04:52.139
that might not be in the browser and
00:04:54.419
here it's many morphism and so morph
00:04:57.840
effectively means shape and ISM
00:04:59.820
effectively means the nature of
00:05:02.220
something directly translated
00:05:04.460
polymorphism effectively means having
00:05:08.180
multiple forms so a good example of this
00:05:12.240
is this classic like optical illusion
00:05:14.460
where either you see the two faces or
00:05:17.280
you see a cup and then that is just
00:05:19.440
because of the interplay between the
00:05:21.060
negative space and the positive space
00:05:23.039
but effectively this has multiple forms
00:05:26.280
it can be two faces or it can be a cup
00:05:30.060
it's effectively a single thing that can
00:05:32.940
take on multiple forms depending on the
00:05:36.360
context and the circumstances it is
00:05:38.759
important to mention that polymorphism
00:05:41.639
is a really wide and Broad concept uh
00:05:45.840
specifically in the world of programming
00:05:48.060
so if they think about polymorphism in
00:05:50.699
the scope of programming itself sure it
00:05:53.940
is going to be a really scary thing to
00:05:56.100
tackle but what we're going to do is
00:05:57.840
we're just going to look at polymorphism
00:06:00.139
specifically related to what we're doing
00:06:02.580
right now and also what we have done up
00:06:05.639
until now and how we can understand what
00:06:07.800
we've done through the lens of
00:06:09.720
polymorphism because as you can see here
00:06:12.479
polymorphism is actually a really
00:06:14.759
important key Concept in programming but
00:06:17.639
I also want you to understand that we're
00:06:19.500
not going to cover the entire scope of
00:06:21.419
polymorphism and polymorphism is
00:06:23.759
effectively a technique to keep the
00:06:26.400
complexity of your code base
00:06:27.900
maintainable and so encapsulation
00:06:30.419
inheritance all these things are very
00:06:32.580
Loosely based on polymorphism if we were
00:06:36.180
to think about a code Pace as a object
00:06:39.600
or a toy or something
00:06:41.880
before we started talking about
00:06:43.620
abstraction like you might have thought
00:06:46.080
about your code base as a single Big
00:06:48.960
Unit almost like this blob of code that
00:06:52.380
is this big singular thing the problem
00:06:55.259
with that is that it's very hard to
00:06:57.900
debug or extend and so forth so a
00:07:01.259
solution to that was to think about our
00:07:04.020
code base as these modular encapsulated
00:07:07.139
units that can be reasoned about on
00:07:10.440
their own and can be completely
00:07:12.180
decoupled from everything else so you
00:07:14.639
can almost if you want to debug it or
00:07:16.979
you want to extend it you can pull all
00:07:18.840
the different pieces out individually
00:07:20.580
instead of treating it as a big thing
00:07:23.039
and you can even extend these pieces so
00:07:25.979
effectively what we looked at is
00:07:28.319
encapsulation so a code base that isn't
00:07:31.199
encapsulated people sometimes talk about
00:07:33.960
a big ball of mud so you know something
00:07:37.139
like this
00:07:38.280
um it's kind of like everything is like
00:07:39.780
this blob and it's very hard to separate
00:07:42.720
out the independent pieces it there's
00:07:45.660
another term for it which is a spaghetti
00:07:48.060
code which you might have heard and a
00:07:50.819
lot of people use the term spaghettiko
00:07:52.860
just for bad code but the meaning of
00:07:55.500
spaghetti code if we were to look at
00:07:57.419
Wikipedia actually refers to code that
00:08:01.979
has complex and Tangled control
00:08:04.139
structure so program flow that is like a
00:08:07.080
bowl of spaghetti and if you remember
00:08:09.180
correctly when we started talking about
00:08:10.800
programming paradigms one thing that all
00:08:13.440
these paradigms do at a minimum is they
00:08:16.860
take away the direct manipulation of
00:08:19.620
control structure so we also spoke about
00:08:21.479
like go-to statements and so forth so at
00:08:24.360
the very least what all these actual
00:08:27.180
paradigms do is they actually Force us
00:08:30.300
to do encapsulation but they just differ
00:08:32.700
in terms of how you should do
00:08:34.559
abstraction and encapsulation oop says
00:08:37.799
that you should encapsulate your data
00:08:40.559
and your behavior together whereas
00:08:43.620
functional programming you should
00:08:45.300
encapsulate your data and your behavior
00:08:48.120
separately but the keys in terms of
00:08:50.220
mutability the ability to actually
00:08:52.740
change data so not only are you actually
00:08:55.980
encapsulating your data and your
00:08:58.019
behavior you're actually encapsulating
00:09:00.240
your data itself from being changed
00:09:02.640
entirely and and we're going to talk
00:09:04.320
about that a bit later but I think it's
00:09:06.300
important to note a key point of
00:09:09.600
everything we've covered up until now
00:09:11.160
since we started about managing
00:09:12.779
complexity is how to get from from this
00:09:16.500
big ball of mud code or spaghetti code
00:09:19.200
to a code-based that is encapsulated and
00:09:22.200
let me just bring in a picture of
00:09:23.399
spaghetti to kind of indicate the
00:09:25.080
principle to you so you can think about
00:09:27.180
this you know like if this is your code
00:09:29.160
it's very hard to figure out where does
00:09:32.160
something begin where does something end
00:09:33.899
what is it connected to if I change this
00:09:36.420
value what else is it connected to what
00:09:39.000
else is going to change if I delete this
00:09:41.279
thing what else is going to break so
00:09:43.019
there's no clear indication of how
00:09:44.940
things are separated from one another
00:09:46.560
which is what we do have here so let's
00:09:49.440
look at the two examples of
00:09:50.700
encapsulation that we have done up until
00:09:52.740
now we've kind of encapsulated our
00:09:54.899
single task itself into a web component
00:09:57.540
and we've also tasked adding so we have
00:10:01.140
created these two encapsulated units but
00:10:04.980
we can take this a step further and this
00:10:07.440
is where polymorphism comes in so
00:10:09.779
instead of creating something for a very
00:10:12.000
specific once-off purpose so effectively
00:10:14.700
you know we create this tire and it is
00:10:17.220
meant to go there we create this this is
00:10:18.959
meant to go there we create the engine
00:10:20.880
and it's meant to go there and we don't
00:10:22.560
and we create the seat and it is meant
00:10:24.420
to go there maybe think about creating
00:10:27.360
things in a broader abstract sense so
00:10:31.200
that they can actually be reused to
00:10:34.440
compose a range of different things what
00:10:37.380
would be an equivalent so let's think
00:10:39.060
about Lego and this is also one of the
00:10:41.580
keys of Lego is that and I can say this
00:10:44.339
to as someone who has a daughter that is
00:10:46.380
kind of approaching the age of two right
00:10:48.120
now beauty of Lego is that you can
00:10:51.660
compose a various range of different
00:10:54.779
things with these very basic Universal
00:10:58.260
units with this you can only build that
00:11:01.260
car there's nothing else you can really
00:11:02.820
build with it and when you're done
00:11:04.440
building that car these things have
00:11:06.480
served their purpose in the story if you
00:11:08.519
want to build something else you need to
00:11:10.260
buy another toy set and the same you
00:11:12.959
know so we can think about the problem
00:11:15.060
here while we do have encapsulation is
00:11:18.540
that as we add more functionality we
00:11:21.060
just keep on creating new web components
00:11:23.040
web components web components web
00:11:24.360
components so effectively there's an
00:11:26.640
infinite ceiling to how many components
00:11:28.860
we can have so let's say like this
00:11:31.320
project has now been going for 10 years
00:11:33.300
how many components are you going to
00:11:35.160
have a hundred a thousand ten thousand a
00:11:38.640
hundred thousand well I guess that
00:11:39.899
depends on how much the product has
00:11:42.120
grown but imagine debug plugging a
00:11:45.540
project that has a hundred thousand
00:11:48.120
different components or trying to learn
00:11:51.060
the code base of a project that has a
00:11:53.640
hundred thousand components so
00:11:55.500
effectively polymorphism is a technique
00:11:57.839
that takes this idea of encapsulation
00:12:00.480
even further and says try and create
00:12:04.279
modular reusable units of abstraction
00:12:08.540
instead of something that's for a very
00:12:11.160
specific purpose and that purpose alone
00:12:13.140
so theoretically you know while you
00:12:15.180
would be able to do something like this
00:12:16.800
good abstractions by mean of
00:12:18.779
polymorphism should be able to scale to
00:12:21.839
a huge degree so a good system a good
00:12:24.779
code base would theoretically allow you
00:12:27.839
to build something of a massive scale
00:12:30.600
only a handful of very reusable
00:12:35.640
components and the reason why I say in
00:12:37.980
theory because there is a balancing act
00:12:39.839
here and it is definitely possible to
00:12:42.360
over abstract and I'm going to talk
00:12:43.740
about that in a second and this is also
00:12:46.440
why we talk about these Concepts
00:12:49.079
theoretically why we dive into the
00:12:52.320
nature of them instead of me just
00:12:54.420
showing you how to do it because almost
00:12:56.760
all the time this is something that you
00:12:59.040
are going to have to exercise your own
00:13:00.540
discretion at there is no one true
00:13:03.060
answer and so by understanding these
00:13:05.279
Concepts and understanding how they get
00:13:06.779
applied that's going to equip you to
00:13:09.839
make more well-informed decisions to
00:13:12.060
understand where to draw this line for a
00:13:15.120
specific instance or a specific code
00:13:17.040
base or for a very specific problem but
00:13:19.500
it's important to understand that there
00:13:21.360
is a balance here and whereas you can go
00:13:23.820
too far to the side in terms of creating
00:13:26.820
things that are too specific like you
00:13:29.220
can also go too far to the side where
00:13:32.040
you over abstract but I'm going to talk
00:13:34.079
about that in a second I just want to
00:13:35.639
touch on what are examples of
00:13:37.380
polymorphism that we actually have
00:13:39.660
demonstrated thus far and you might not
00:13:41.760
even realize that we have looked at
00:13:43.260
examples of polymer autism thus far so
00:13:45.899
when it comes to extending things there
00:13:48.779
are generally two types of polymorphism
00:13:50.700
and the one is called subtype
00:13:53.700
polymorphism and that is effectively
00:13:56.339
what we have discussed with classes and
00:13:58.740
extending classes and so forth and so
00:14:00.720
this is more to do with what something
00:14:02.040
is whereas the other one called
00:14:04.940
structural polymorphism has more to do
00:14:08.579
with not what something is but what it
00:14:12.480
can do or what it has and this is
00:14:15.839
generally called duct typing so
00:14:18.240
effectively what this means is you don't
00:14:21.360
actually care what the thing is so you
00:14:24.060
don't care is it a bird you know is it a
00:14:26.820
worm is it cold-blooded is it warm
00:14:28.980
blooded you actually don't care about
00:14:30.600
the nature of the thing all you care
00:14:32.880
about is what can it do or what does it
00:14:35.700
have you can have three different things
00:14:37.740
you know and can I drive yes can this
00:14:41.279
drive yes a golf club can it drive yes a
00:14:45.180
cup of coffee can it drive no that is
00:14:48.120
all that you care about and so an
00:14:50.519
example of this was the example that we
00:14:53.220
have where we had the plane and we had
00:14:55.860
the duck very thematically and let's say
00:14:58.079
we have something else called a stone
00:15:00.420
all right you don't really care what
00:15:02.459
these things are all you care about is
00:15:05.100
can they fly and a duck in a plane can
00:15:07.980
fly while a stone can't fly but then
00:15:10.740
they also have other properties you know
00:15:12.660
in terms of not what can they do but
00:15:15.000
what do they have and I said the
00:15:16.740
material you know so is a plain soft no
00:15:20.100
it's a duck soft yes it's a stone soft
00:15:23.339
no so this is what you're concerned with
00:15:26.339
and this might seem very abstract to you
00:15:28.440
and I'm going to show a bit later in
00:15:30.959
this lesson how you'd actually do this
00:15:33.540
in practice and if you also remember
00:15:35.579
from the previous lesson generally you
00:15:38.820
should aim for structural polymorphism
00:15:41.639
um because as you can imagine it's a lot
00:15:43.500
more flexible people then subtype
00:15:45.779
polymorphism some languages force you to
00:15:48.420
do subtype polymorphism some languages
00:15:50.639
actually only allow you to do structural
00:15:52.980
polymorphism JavaScript allows you to do
00:15:55.079
both so my personal preference is always
00:15:58.500
for composition then there
00:16:03.839
until now and these are more related to
00:16:07.320
not the nature of something but actually
00:16:10.620
in terms of what you pass to it you get
00:16:13.680
for example ad hoc polymorphism which
00:16:16.620
you can think about you might have three
00:16:19.440
four different functions that accept the
00:16:21.600
same thing or you might have a single
00:16:23.699
function that accepts all four of these
00:16:26.940
and depending on what you pass in it
00:16:29.699
does something different with it so we
00:16:31.800
had an example where when I showed
00:16:34.019
option optional parameters in jstock I
00:16:37.560
think I had an example where we
00:16:38.759
multiplied so we said you know if pass
00:16:41.779
one value it just multiplies it by
00:16:45.660
itself but the same function if you pass
00:16:48.000
two values then multiply first by six so
00:16:53.040
effectively we have a function that is
00:16:55.079
polymorphic insofar that it accepts two
00:16:59.339
different types of arguments and
00:17:01.440
depending on what you pass it does
00:17:03.240
something different and then the last
00:17:05.400
one is polymorphism through coercion we
00:17:09.540
touched on coercion in the very
00:17:11.699
beginning and effectively what so it's
00:17:13.859
very similar to this but instead of
00:17:15.959
actually using logic to change the
00:17:19.859
behavior you actually just turn one type
00:17:22.980
into another type so we can say that an
00:17:26.339
if statement only accepts a Boolean only
00:17:29.340
takes true or false so either it just
00:17:33.000
takes the word true or false or it takes
00:17:35.100
an expression that evaluates to true or
00:17:37.860
false so age is bigger than or equal to
00:17:41.760
18 or whatever but it actually accepts a
00:17:45.600
couple of things that are not true or
00:17:46.860
false it accepts null undefined an array
00:17:51.600
a string hello an empty string and so
00:17:55.559
forth and then it coerces it for us into
00:17:58.980
a Boolean which means that it broadens
00:18:02.100
the use of this and it moves it a bit
00:18:03.960
closer to this than this meaning that we
00:18:07.860
can use it in loads of different
00:18:10.200
configurations there is also a danger of
00:18:13.080
going too far and I actually think
00:18:15.000
JavaScript went a bit too far when it
00:18:17.820
comes to polymorphism through Persian
00:18:21.000
which is why we have the strict equality
00:18:24.179
instead of just normal equality because
00:18:26.400
not like it went a bit too far and it
00:18:29.220
resulted in a lot of bugs and weird
00:18:32.100
Behavior so we can effectively think
00:18:34.559
about coercion or as instead of saying
00:18:38.220
hey this thing doesn't fit in there
00:18:40.980
actually forcing it through so it turns
00:18:44.160
it into a Boolean set it can be forced
00:18:46.679
through and sometimes that use that's
00:18:48.840
useful
00:18:49.880
sometimes that's not useful especially
00:18:52.260
if you're accidentally passing the wrong
00:18:54.120
thing and JavaScript just goes yep cool
00:18:56.460
okay I'll just try and force this
00:18:58.440
through I don't know if you pass it by
00:19:00.299
accident or whether you meant to there
00:19:02.280
is also a balance um and I think
00:19:04.559
JavaScript got this balance wrong it did
00:19:07.020
add the strict equality to make up for
00:19:09.780
that or to recover from over cursing but
00:19:13.260
in your own code you can also get this
00:19:14.700
balance wrong you can over abstract and
00:19:17.940
so let's talk about over abstraction
00:19:19.740
this is something I have been wanting to
00:19:22.980
talk about for a while but it's hard
00:19:25.320
saying that abstraction is really
00:19:27.539
important and you should do abstraction
00:19:29.900
while at the same time saying that
00:19:32.580
sometimes abstraction can be bad because
00:19:34.620
that sounds like it's not very useful
00:19:36.240
information in order to understand that
00:19:38.220
we needed to have a good understanding
00:19:40.020
of like what exactly abstraction entails
00:19:43.200
so let's quickly just recap so if we
00:19:46.559
think about abstraction again in the
00:19:48.480
visual sense you can think about this
00:19:50.400
comic from Scotland Cloud where you have
00:19:53.520
something that has a lot of information
00:19:55.460
but what you do each time you abstract
00:19:58.320
is you remove information to get to the
00:20:02.160
essence of the thing in other words you
00:20:04.860
remove low level noise so in other words
00:20:07.440
things that aren't related to the
00:20:09.720
essence of the thing and you elevate the
00:20:12.360
essence in the world of visual we
00:20:14.220
actually see this used a ton you know by
00:20:16.860
means of something called infographic so
00:20:19.880
effectively you remove a lot of noise
00:20:23.880
and it is information and you use very
00:20:26.460
simple illustrations and so forth and
00:20:29.039
visual devices to communicate or explain
00:20:31.799
very concept ideas so let's find code
00:20:34.919
space on Google Maps Okay so there's a
00:20:37.919
lot of abstracted stuff here so you know
00:20:41.240
railroads are abstracted this is a
00:20:44.400
abstracted version of a highway ocean
00:20:47.520
and so forth and so forth so it's a lot
00:20:50.100
easier for us to understand the
00:20:53.039
structure understand what we're looking
00:20:55.260
at when we interact with it by means of
00:20:58.380
abstractions compared to if we were to
00:21:00.900
switch to the actual satellite mode it
00:21:03.600
becomes a lot more noisy it becomes a
00:21:06.360
lot harder to really actually
00:21:08.700
see what you're looking at even though
00:21:11.100
it does have still highlights these
00:21:13.140
abstractions it's not just a pure
00:21:15.120
satellite image but there's a lot of
00:21:17.400
noise whereas the abstraction takes out
00:21:20.520
the noise the things that are not
00:21:22.020
important and it elevates the essence
00:21:24.600
for us and we see the same happening
00:21:27.179
here and that is exactly what our own
00:21:30.299
abstraction should do so I have a
00:21:32.640
abstraction called multiply and that
00:21:34.740
takes a single value or two values and
00:21:37.679
this one returns 16 it multiplies it by
00:21:40.020
itself this one returns eight I don't
00:21:42.600
need to care about all the low level
00:21:44.159
things I don't need to care how it
00:21:45.780
actually does this all I work with is an
00:21:49.020
abstracted interface and web components
00:21:51.600
allow us to do this very well
00:21:53.760
but there is the danger of over
00:21:56.460
abstraction not just in web components
00:21:59.520
but in general so while we're talking
00:22:01.919
about visuals let's look at an example
00:22:03.960
of the world of art to get a better
00:22:05.760
sense of this so for a very long time
00:22:08.640
the goal of painting was to create
00:22:11.760
something that is as realistic as
00:22:14.460
possible because this
00:22:17.100
or the era of Photography so the only
00:22:19.740
way in which you could see a
00:22:22.020
representation of reality is through
00:22:24.720
someone painting actual super realistic
00:22:28.140
image to express an idea but obviously
00:22:30.780
with the rise of Photography the society
00:22:33.299
as a whole started rethinking what the
00:22:35.820
purpose of painting is if this is the
00:22:38.100
only goal of painting if the only goal
00:22:39.840
of painting is to actually show
00:22:41.880
something in the real world then
00:22:44.480
photography completely replaces that not
00:22:47.280
only does photography replace that but
00:22:49.140
photography can actually do it way more
00:22:51.360
convincing like you could with the
00:22:53.280
painting so you got a lot of artists
00:22:55.020
that really thought about what actually
00:22:57.120
is the goal of painting and so if you
00:22:58.919
look at this painting like what does it
00:23:00.600
mean to convey a lot of artists started
00:23:03.179
thinking about painting not necessarily
00:23:04.799
as showing something but evoking a
00:23:07.140
specific emotion communicating a
00:23:10.080
specific emotion and so this is where
00:23:13.020
you started getting a lot of guys like
00:23:14.640
Pablo Picasso which you might have heard
00:23:16.559
about so so let's say if the goal of
00:23:19.140
this painting is to show the chaos of
00:23:21.900
War he thought that is there a way in
00:23:25.020
which we can show the same principle in
00:23:28.140
a much more abstracted version can we
00:23:31.559
remove all the noise that doesn't
00:23:34.140
necessarily communicate the chaos of War
00:23:36.840
you know so this little window here or
00:23:39.419
that Tower there or the details on this
00:23:42.299
guy's drum or the texture on that flag
00:23:44.880
and we just extract the essence of that
00:23:47.640
chaos and represent that as an
00:23:49.500
abstraction and this is one of the most
00:23:51.840
well-known paintings from that era I'm
00:23:53.880
not even gonna try and pronounce the
00:23:55.620
name of the painting but it is currently
00:23:58.340
exhibited in Madrid in Spain so this is
00:24:02.039
from 1940 and it's a depiction of the
00:24:04.740
Spanish Civil War and you know and so
00:24:06.960
this car was like surrealism and cubism
00:24:09.419
and all of that and then you got this
00:24:11.039
era of artists that try to take this
00:24:14.460
idea even further so can you maybe be
00:24:18.320
expressed this chaos and the chaos of
00:24:21.419
War through an even further abstraction
00:24:24.000
completely removing iconography
00:24:26.760
completely removing pictures and just
00:24:29.880
using the form of paint itself so for
00:24:32.460
example this you know and then there we
00:24:34.620
got kind of impressionism and abstract
00:24:37.260
art and all of that kind of so we kind
00:24:40.260
of got this movement in the art World
00:24:42.059
from this to like almost like seeing how
00:24:46.320
far can we abstract what a painting is
00:24:49.620
meant to communicate and granted art is
00:24:53.100
an extremely subjective experience
00:24:54.900
because the girl of art is multifaceted
00:24:57.960
unlike programming where the goal is to
00:25:01.440
increase readability increase
00:25:02.940
understanding increase maintenance the
00:25:05.700
goal of art isn't much more open we
00:25:07.860
can't definitively say this is what art
00:25:09.960
is meant to do that depends on you as a
00:25:13.320
person what does art do for you do you
00:25:16.740
purely just enjoy boy looking at a super
00:25:18.659
realistic painting or do you find Value
00:25:22.260
in the emotions that it evokes for you
00:25:24.539
or is the enjoyment that you get out of
00:25:26.880
art being how you can express something
00:25:29.760
really complex with as little material
00:25:32.159
as possible so whether this or something
00:25:34.980
like origami or so forth you know this
00:25:37.380
is also an extreme abstraction so the
00:25:40.860
scope of this lesson isn't big enough to
00:25:42.960
really unpack this but I I just wanted
00:25:44.880
to highlight that the criticism that
00:25:48.000
people have of this type of art is that
00:25:50.880
it over abstracts it abstracts so much
00:25:53.760
that it loses all meaning that there's
00:25:56.760
almost nothing of the essence left and
00:25:58.980
it's just this abstracted concept that
00:26:01.980
isn't useful there's a ton of jokes on
00:26:04.740
this you know this is almost like a
00:26:06.360
punchline in itself you know this idea
00:26:08.520
of like for example these little
00:26:09.960
scribbles of this Beast symbolizes a ham
00:26:12.900
and cheese sandwich or or whatever or
00:26:15.539
you know my one year old daughter could
00:26:18.600
paint this so here's an image of Jackson
00:26:21.360
Pollock who actually he is a very famous
00:26:24.720
artist who exclusively kind of did this
00:26:26.820
type of thing and there's like kind of a
00:26:28.020
joke that oh you know even like toddlers
00:26:30.600
can do this or whatever but so it's
00:26:32.880
almost a punch line in itself by this
00:26:34.679
point but we also get over abstraction
00:26:37.700
in in the world of graphic design so you
00:26:40.620
know if you were to look at something
00:26:41.640
like this let's say you want a picture
00:26:43.919
of a hamburger or a restaurant so this
00:26:47.100
is maybe a bit too realistic this is
00:26:49.320
maybe a bit too abstract so if you're
00:26:51.600
looking at a menu and there are icons
00:26:53.400
that are separating the different types
00:26:55.020
of things this is maybe a bit too
00:26:56.580
realistic there's too much noise it's
00:26:58.320
very hard to At a Glance see what it is
00:27:00.360
when you come when you have various
00:27:02.159
types of food that are indicated in this
00:27:04.260
manner and whereas this is too abstract
00:27:06.299
this is maybe this is a good middle
00:27:08.460
ground in terms of if you want to scan
00:27:10.080
the menu and see the different types of
00:27:12.179
foods and so bringing this back to the
00:27:16.080
world of programming we can also say
00:27:18.960
that sometimes things can be a bit too
00:27:21.419
abstracted where you go too far in this
00:27:24.840
direction and it actually makes it
00:27:27.000
harder to read it actually makes it
00:27:28.799
harder to understand it actually makes
00:27:30.600
it harder to debug and that's a very
00:27:32.580
fine balance that you need to actually
00:27:34.740
walk yourself so what I want to do now
00:27:36.900
is I want to talk about what are some
00:27:38.640
things that I generally consider as over
00:27:41.159
abstractions that you should be careful
00:27:43.140
of but as mentioned you know there is no
00:27:45.480
one true Rule and there might actually
00:27:47.039
be instances where these are the right
00:27:49.380
level of abstraction depending on what
00:27:51.120
you want to do and then after all of
00:27:53.100
this I want to come back all the way to
00:27:55.260
web components and talk about how we can
00:27:59.039
use this principle of polymorphism with
00:28:01.980
web components and do it in a way where
00:28:05.279
we where we avoid the dangers of over
00:28:08.220
abstraction
00:28:10.400
so there are a couple of examples that I
00:28:13.799
can speak to when it comes to actual
00:28:15.900
over abstraction in JavaScript although
00:28:18.360
I want to maybe look at one specific one
00:28:20.520
that I actually personally find a lot
00:28:23.279
um when I'm looking at code bases and
00:28:25.260
this is the idea of design patterns so
00:28:28.679
I'm going to be speaking about design
00:28:30.600
patterns and I think there's also a
00:28:33.600
distinction to be made between design
00:28:35.220
patterns as a general concept and design
00:28:39.240
patterns as an actual proper noun okay
00:28:43.140
so let's maybe just say lowercase design
00:28:45.360
patterns and design patterns the thing
00:28:48.900
because I do think there's a ton of
00:28:50.520
value in design patterns in general but
00:28:53.340
let's look at design patterns as a
00:28:55.860
proper noun effectively the goal of this
00:28:59.279
design patterns was to actually solve
00:29:01.559
this problem of design patterns and this
00:29:04.320
is also where things start to get
00:29:05.760
confusing but the goal was effectively
00:29:07.740
to figure out specific solutions that
00:29:11.100
tend to solve the same type of problems
00:29:12.900
in programming so it comes from this
00:29:15.539
book I have mentioned this book before
00:29:17.159
design patterns elements of reusable
00:29:19.440
object orientated software and so I kind
00:29:22.440
of referenced this book when I said the
00:29:24.480
recommended approach is to favor
00:29:26.940
composition over inheritance one of the
00:29:29.640
key takeaways from the book is it
00:29:31.620
actually established a list of patterns
00:29:34.559
that are very common in the world of
00:29:36.419
programming keep in mind this is
00:29:37.860
published in 1994. if you're my age that
00:29:40.860
might not feel very long ago for you
00:29:42.899
that probably sounds very long ago but
00:29:44.580
in fact it is actually very long ago
00:29:46.640
1994 feels like it wasn't that long ago
00:29:49.380
but effectively this is when South
00:29:50.880
Africa became a democracy so that that's
00:29:53.039
how long ago it is this is even a year
00:29:55.740
before this language that we know to
00:29:57.419
today's JavaScript was ever conceived
00:30:00.419
way before it was even called JavaScript
00:30:02.399
it didn't even exist in its precursor
00:30:05.039
state so keep in mind that a lot of
00:30:06.899
these patterns were for problems that
00:30:09.600
existed in programming at that point
00:30:11.640
that mentioned programming has changed
00:30:14.100
quite a bit and also the nature of the
00:30:16.260
things we're building specifically with
00:30:18.179
the development of the web and the
00:30:19.980
concurrency in decentralization that
00:30:22.200
came with the web have kind of
00:30:24.000
reorientated the world of programming a
00:30:25.980
bit there are people out there that
00:30:27.600
would tell me that I'm wrong that these
00:30:29.760
principles are as true today as they
00:30:32.880
were back in that day and they are as
00:30:35.399
universal today as well as they were in
00:30:38.220
that day which my response would be I
00:30:40.200
guess this is just where we differ based
00:30:43.500
on anecdotal experience in my experience
00:30:46.380
I found design patterns in JavaScript to
00:30:49.620
be more harmful than actual helpful so
00:30:52.260
generally I tell people to try and avoid
00:30:54.419
them but I think it warrants just a
00:30:56.940
quick discussion passion on them because
00:30:58.679
I do think there is value you can get
00:31:00.419
from them but you should be careful in
00:31:02.700
terms of what the actual value is that
00:31:05.100
you're looking from them because I do
00:31:07.919
think when we think about this idea of
00:31:09.899
over abstraction I do think that design
00:31:12.659
patterns over abstract it which was fine
00:31:16.320
at that time because there were only a
00:31:19.200
limited number of programming languages
00:31:21.000
and types of things that we're building
00:31:22.740
of software but I think because the
00:31:24.720
world of programming has gotten so
00:31:26.520
diverse having an abstraction at such a
00:31:29.820
far level which abstracts programming
00:31:32.520
principles itself as if they can be
00:31:34.559
applied to any language independent of
00:31:37.140
what that actual language is or that
00:31:39.179
language is idiomatic style which I'm
00:31:41.460
going to talk about as well I think is
00:31:43.440
an over abstraction and so what I see
00:31:45.299
people do a lot is they look at these
00:31:46.799
design patterns and they blindly
00:31:48.659
Implement them in JavaScript the reality
00:31:51.120
is that a lot of the problems that these
00:31:54.240
design patterns solved in other
00:31:55.559
languages are not problems enjoy
00:31:57.299
JavaScript or that specific solution
00:31:59.760
doesn't make sense in JavaScript and it
00:32:01.860
doesn't fit with the broader kind of
00:32:04.200
usage of JavaScript so if there's only
00:32:06.419
one thing to keep in mind here is that
00:32:07.980
those design patterns were conceived
00:32:09.840
even before JavaScript existed but I do
00:32:11.880
think there's value in just kind of
00:32:13.620
reading up about them a bit the two
00:32:16.260
books that I recommend you read if you
00:32:18.840
want to learn a bit more about design
00:32:20.460
patterns the thing is a phenomenal book
00:32:23.580
by the name of dive into design patterns
00:32:27.000
some of it is actually available for
00:32:29.220
free if you go to
00:32:32.600
refactoring.guru so on here so
00:32:35.299
refactoring like that dot Guru some of
00:32:38.220
the content is actually available for
00:32:39.899
free on here you will also see mention
00:32:42.600
of some terms you should know by now
00:32:44.399
like solid and so forth and then the
00:32:46.740
other one is by Addie Osmani he's a very
00:32:49.140
well-known JavaScript developer at
00:32:50.580
Google I also think a lot of his stuff
00:32:53.039
from his book is is available for free
00:32:55.799
online ad patterns dot Dev I think yes
00:32:59.940
but you can also download the book I
00:33:02.039
think the book is free I might be
00:33:03.480
mistaken but it's important to know that
00:33:05.159
in both of these they actually give a
00:33:06.960
couple of warnings about patterns and
00:33:08.880
specifically around a lot of the stuff
00:33:11.039
that I spoke about so in this specific
00:33:14.100
book there's actually a section where
00:33:16.440
they talk about some well-known design
00:33:19.260
patterns May simply not be valuable as
00:33:21.419
they used to be others might have even
00:33:23.220
evolved and changed significantly so
00:33:26.100
which is why I said I think there's
00:33:28.019
value in this there's value in terms of
00:33:30.240
drawing inspiration from these patterns
00:33:32.880
but what I find is a lot of developers
00:33:35.299
approach these patterns as ready-made
00:33:37.980
solutions that they can just copy and
00:33:40.620
Implement in their own code without
00:33:42.059
actually thinking about it so I do find
00:33:45.419
this value in drawing inspiration from
00:33:47.880
these patterns looking at ways in which
00:33:50.340
you can solve problems but within the
00:33:52.140
world of JavaScript I actually don't
00:33:53.519
find Value in treating these patterns as
00:33:56.159
Solutions within themselves and I'm
00:33:58.320
going to show you an example of why even
00:34:00.360
important to note that even on this
00:34:02.340
refactoring Guru if you go to design
00:34:04.200
patterns there's an entire section just
00:34:06.600
on criticism of design patterns with an
00:34:09.599
actual section on can patterns sometimes
00:34:11.639
be harmful so just keep that in mind but
00:34:14.339
I think it's like there's a lot of value
00:34:16.080
in terms that we can get from design
00:34:17.879
patterns I'm not necessarily going to go
00:34:20.159
over
00:34:21.500
adiosmani's book because some of these
00:34:25.139
patterns require a bit of an
00:34:27.480
understanding of Frameworks so here they
00:34:30.060
actually mentioned some of the
00:34:31.320
Frameworks that we're going to be
00:34:32.339
covering in upcoming lessons so view
00:34:34.918
angulus felt lit also react react as
00:34:39.300
well preact and react is very similar if
00:34:41.639
you understand react you probably
00:34:42.899
understand preact so they introduce a
00:34:45.480
couple of patterns that are specific to
00:34:47.699
Frameworks so you know render props
00:34:50.280
pattern which you won't find in
00:34:51.659
traditional design patterns or hooks so
00:34:54.300
it's a good read I encourage you to read
00:34:56.339
it but just leave a lot of room for
00:34:58.560
actually using this as inspiration
00:35:00.300
instead of actual something you you
00:35:02.640
should take as is and implement the same
00:35:05.220
for a dive into design patterns I
00:35:07.859
actually find a lot of the introductory
00:35:09.540
stuff like really really useful so
00:35:12.540
specifically where he talks about like
00:35:14.339
abstraction polymorphism encapsulation
00:35:16.740
inheritance and he actually also talks
00:35:19.680
about how things can stand in relation
00:35:21.900
to one another how you can achieve
00:35:23.880
polymorphism so here he has inheritance
00:35:26.520
and composition and you'll see there's a
00:35:28.500
lot more flexibility with composition
00:35:30.119
than you get with inheritance and
00:35:31.980
there's a section where he talks about
00:35:33.420
you know what makes good abstractions
00:35:35.700
and so forth those I find really helpful
00:35:37.859
but where it actually has examples of
00:35:41.099
specific patterns I do encourage you to
00:35:44.160
tread a bit lightly and not just
00:35:46.320
Implement these as is use them as
00:35:48.960
inspiration for how specific problems
00:35:51.180
are solved in order to solve your own
00:35:53.160
problems but what I see a lot is
00:35:55.200
Javascript developers taking these
00:35:57.240
patterns in terms of the implementation
00:35:59.700
of them and actually just putting them
00:36:01.859
in JavaScript itself and so let me show
00:36:04.260
you an example of this so there's a
00:36:06.180
specific pattern that I see quite a lot
00:36:08.400
that to me is maybe the most blatant
00:36:11.339
example of where you're actually writing
00:36:14.220
worse JavaScript code when you're using
00:36:16.020
the Singleton pattern here's the
00:36:18.060
Singleton so effectively what the
00:36:19.740
Singleton pattern very broadly speaking
00:36:22.500
actually is is you create a class and
00:36:25.500
then you ensure that there can only be a
00:36:28.079
single instance of that class and this
00:36:30.359
makes a lot of sense in languages like
00:36:31.920
Java and c-sharp and so forth so let me
00:36:34.320
show you quickly what that would look
00:36:36.060
like effectively so this is the
00:36:38.220
Singleton pattern so how you would do
00:36:40.740
this in JavaScript is as follows you
00:36:43.560
create a class let's just call that
00:36:45.420
class company so this is all the
00:36:47.339
information about the company and they
00:36:48.900
can only exist a single instance of a
00:36:51.060
company so this is the company for whom
00:36:52.980
the software is so let's just say name
00:36:55.260
the name of the company is Acme
00:36:57.599
Incorporated it was founded in 2007 the
00:37:02.760
CEO is Mr Acme himself and let's maybe
00:37:06.720
add a method where we have you know
00:37:08.400
replace the uh let's just say new name
00:37:11.579
and all that this does is this dot Co
00:37:14.640
equals the new name and maybe we can
00:37:17.520
just cancel log goodbye the currency of
00:37:20.400
first before we reassign them and then
00:37:22.859
usually what you would do is you would
00:37:24.420
create an instance of it so let's say
00:37:26.160
company a new company all right and
00:37:29.040
there is your Singleton whenever you
00:37:31.260
want to read something about this
00:37:32.880
specific company you would go what's a
00:37:34.800
company name uh what's the company CEO
00:37:37.700
replace the current CEO but the problem
00:37:40.680
is at the moment that we can create
00:37:42.839
several of them we can create you know
00:37:44.940
and then the fake company we can replace
00:37:47.220
the CEO so now we have two versions of
00:37:49.800
the company with different information
00:37:51.140
this is the problem that the Singleton
00:37:53.760
pattern tries to solve for us kind of
00:37:55.560
have a single source of Truth for
00:37:57.180
something uh easy way to do this would
00:37:59.940
be to you just say you know constructed
00:38:02.820
is false and then when the Constructor
00:38:05.040
runs you just set constructed true but
00:38:08.579
before that you actually check if this
00:38:11.040
constructed the if it is false and you
00:38:13.260
try and construct it again then you
00:38:15.540
throw new error instance already exists
00:38:19.500
now you might look at this and you might
00:38:21.240
be like cool so like this is going to
00:38:22.980
throw an error company let's just then
00:38:25.260
export company and let's also make it
00:38:27.420
the default export and let's say this is
00:38:30.300
a file called
00:38:32.060
company.js and you might pat yourself in
00:38:34.920
the back and be like well done I've used
00:38:37.140
design patterns I've used the Singleton
00:38:39.060
pattern everyone's going to look at me
00:38:40.680
and see I'm a really good developer I
00:38:43.200
know my design patterns and design
00:38:45.359
patterns are approved good Solutions and
00:38:48.420
let's say you want to really impress
00:38:49.800
people and you actually want to show
00:38:51.720
that you actually know a bit about
00:38:52.859
design patterns implements Singleton
00:38:55.920
pattern of company and you're like hey
00:38:59.099
people are going to look at this and
00:39:00.180
they're going to see like hey I know
00:39:01.560
something about programming I didn't
00:39:02.880
just willy-nilly write code I
00:39:04.740
implemented a specific well-known
00:39:06.119
pattern here and so this is what I find
00:39:07.980
a lot of times the problem with this is
00:39:10.680
that this solves a problem that we don't
00:39:13.320
have a JavaScript it's actually over
00:39:15.180
Engineers it over abstracts something
00:39:17.820
that doesn't need an abstraction so
00:39:20.400
basically and you might have realized
00:39:22.440
this as I was like writing this
00:39:24.300
languages like Java and C shop don't
00:39:27.780
have this concept of object literals in
00:39:31.020
the sense that JavaScript has in his
00:39:33.240
book Douglas crockford actually says in
00:39:35.220
his book JavaScript the good parts he
00:39:37.020
actually says like two of the really
00:39:38.700
good things about JavaScript is object
00:39:41.400
literals and composable functions and
00:39:44.640
we're going to talk about composable
00:39:45.839
functions when you talk about functional
00:39:47.579
programming so we're actually checking
00:39:50.400
something that JavaScript has a really
00:39:52.260
really good solution for compared to
00:39:54.480
other programming languages and we're
00:39:56.339
actually making it worse and taking a
00:39:58.500
worse solution to solve a problem that
00:40:00.780
JavaScript doesn't actually even have
00:40:02.220
because these languages because you
00:40:04.980
can't create an object literal you need
00:40:06.720
to create a class so this is how to
00:40:09.240
emulate object literal-like behavior in
00:40:12.000
JavaScript the problem is Javascript one
00:40:13.740
already has object literals and it's
00:40:15.540
actually much easier to read easier to
00:40:17.460
understand let me show you we could do
00:40:19.619
this exact thing by just straight up the
00:40:22.020
clearing company taking this info not
00:40:24.720
even worrying about whether it's
00:40:26.160
constructed or not and then just
00:40:28.079
chucking this in here and just exporting
00:40:30.660
that object literal there we go we can
00:40:33.119
even take this a step further and just
00:40:35.160
treat the module itself as the
00:40:37.500
abstraction without an actual extra
00:40:39.359
level of abstraction in the module
00:40:41.099
itself and we can actually just export
00:40:43.560
con's name export cons founded export
00:40:46.200
con CEO export funds replace CEO so you
00:40:49.800
effectively take something that can be
00:40:51.839
solved in this manner and you solve it
00:40:53.579
in this way because you're forcing a
00:40:55.740
design pattern into JavaScript this
00:40:58.020
doesn't mean that there aren't design
00:40:59.820
patents here and there that might be
00:41:01.380
useful but my guess isn't so far that a
00:41:05.160
design pattern might be useful in
00:41:06.660
JavaScript you're actually going to end
00:41:08.579
up with that pattern yourself almost by
00:41:10.619
pure accident because it is the best way
00:41:12.540
to solve it um the point being that when
00:41:14.820
I see design patterns being used in
00:41:16.560
JavaScript a lot of times they're being
00:41:19.020
forced in for the sake of design
00:41:21.540
patterns themselves without actually
00:41:23.520
thinking whether it's a good fit or not
00:41:25.440
and not only is this more code but this
00:41:29.760
I actually would say is more idiomatic
00:41:32.099
and this is less idiomatic so what do we
00:41:34.740
mean by idiomatic so you can think about
00:41:36.300
a language you know so you have idioms
00:41:38.460
in a language so an example in English
00:41:40.980
would be you know so this example over
00:41:42.540
here like something like a piece of cake
00:41:44.400
or in the doghouse the point being that
00:41:47.700
there are specific Expressions specific
00:41:49.560
ways of saying or writing things that
00:41:52.500
are that make only make sense if you
00:41:54.540
understand the language itself and a lot
00:41:57.119
of these idioms are aren't directly
00:41:59.460
translatable from one language to
00:42:01.440
another a couple of years ago there was
00:42:03.180
actually this
00:42:05.240
which also has a play on words because
00:42:07.380
in Afrikaans percyaker means for sure
00:42:10.320
but but also means insurance so like the
00:42:14.040
the brand itself is a play on like
00:42:16.500
Afrikaans language but effectively the
00:42:19.079
advert went along the lines of I can't
00:42:21.660
remember exactly I don't think I'll be
00:42:23.400
able to find it online but it went along
00:42:25.800
the lines of I think they were at a
00:42:27.420
braai or something and the guy said like
00:42:30.020
steel and so when you translate that
00:42:33.780
directly to English like it would mean I
00:42:36.660
was robbed rat and naked which in
00:42:39.960
English because in English there isn't
00:42:42.000
an idiomatic expression like that saying
00:42:44.520
something is red like the animal and
00:42:46.859
naked doesn't make any sense and that
00:42:49.380
was kind of like the joke of the advert
00:42:51.240
there's loads of these examples in
00:42:53.099
Afrikaans and English where if you
00:42:55.079
translate something it's super confusing
00:42:56.820
and this is effectively what we're
00:42:59.099
saying here we're seeing some patterns
00:43:01.680
that work really well in specific
00:43:04.200
languages that actually are even more
00:43:06.180
confusing in JavaScript so be careful of
00:43:08.579
this be careful of this also when you're
00:43:10.380
talking with other developers from other
00:43:12.060
languages there are things in languages
00:43:13.980
that are idiomatic to that language
00:43:16.740
itself and the problem with this isn't
00:43:20.040
that they don't work like here we have a
00:43:22.680
working example the problem is that they
00:43:25.260
do work but it's a very inefficient
00:43:27.599
solution even if it works it would have
00:43:29.880
been much different if it just didn't
00:43:31.319
work flat out then you would look for
00:43:33.300
another solution which is why a lot of
00:43:35.280
developers don't realize how problematic
00:43:37.560
this is you know for example if you are
00:43:40.079
using a wrench to hit in Nails it's
00:43:42.900
going to work and it's going to suck and
00:43:45.240
it's going to be painful and but you're
00:43:46.619
going to get it to work eventually and
00:43:48.240
then you might be like that's just how
00:43:49.619
it is likewise you can see I went out of
00:43:52.079
my way to find some great examples you
00:43:54.000
know if your lawn if you're vacuuming
00:43:56.520
your lawn to vacuum up the leaves you
00:43:59.099
might actually think that's just how it
00:44:00.599
is it just sucks it just mind the pun
00:44:03.599
sucks to clean up leaves in your yard
00:44:05.760
you know this would be if you don't know
00:44:07.980
about a rake and you're not familiar
00:44:09.900
with the world of gardening and the
00:44:12.540
tools that are at your disposal and
00:44:13.980
whatever and you think there's a
00:44:15.420
universal tool that does the same thing
00:44:17.760
for your inside the house but when
00:44:19.920
you're in a different environment
00:44:21.079
whereas that thing might give you the
00:44:23.400
same solution it might actually just
00:44:26.040
barely give you what you want whereas
00:44:28.140
there is actually something that's a lot
00:44:29.760
more idiomatic to the context and the
00:44:31.980
environment that you're working in so be
00:44:33.720
mindful of that so just as an aside
00:44:36.300
before we continue I actually made an
00:44:38.579
error here and I forgot to add a static
00:44:42.540
here so this shouldn't change the actual
00:44:45.359
implication and the actual point but
00:44:48.359
just as an aside if you try and run this
00:44:50.940
um I did forget to add a static here so
00:44:52.800
let me just actually check if it
00:44:54.480
actually runs as it should and I
00:44:56.700
obviously just need to remove the
00:44:58.200
exports here because obviously there is
00:45:01.260
no such thing as an export in the
00:45:03.000
browser and we also need to change this
00:45:06.660
to get it from the class itself instead
00:45:10.380
of the instance all right let's check it
00:45:12.900
out okay so that works and then if we
00:45:15.480
try and do it twice cool there we go so
00:45:18.780
let me just update that so it is correct
00:45:21.300
and if anything like the main takeaway
00:45:23.520
here should be there are no Universal
00:45:26.280
always correct Silver Bullet answers in
00:45:28.920
the world of JavaScript if that didn't
00:45:30.720
become clear now I don't know how to
00:45:33.000
make that more clear if anyone tells you
00:45:35.640
they have a 100 bulletproof answer to
00:45:39.480
how to write JavaScript and it can be
00:45:41.640
used in any type of project any type of
00:45:44.099
company any type of team or any type of
00:45:46.920
purpose be suspicious be suspected the
00:45:49.980
reason why there are so many different
00:45:51.599
Frameworks out there and that reason is
00:45:54.420
that we're building so many different
00:45:56.160
things in so many different ways that
00:45:58.619
there is no one true solution and you
00:46:00.720
need to be able to evaluate these things
00:46:02.520
and figure out what is a good fit for
00:46:04.140
what you're building right now which is
00:46:06.000
also in a couple of lessons we're going
00:46:08.040
to be moving into a space where you are
00:46:10.800
going to be required to make a lot of
00:46:12.960
these decisions and Advocate four
00:46:15.240
specific things instead of me I show you
00:46:18.359
what to do and you actually just
00:46:19.800
indicating that you understand how to do
00:46:21.599
it