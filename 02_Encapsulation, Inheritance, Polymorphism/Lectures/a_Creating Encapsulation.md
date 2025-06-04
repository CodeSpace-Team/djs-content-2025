00:00:00.000
I spent a lot of time now talking about
00:00:02.580
object oriented programming and you know
00:00:05.460
specifically this idea of an abstraction
00:00:07.880
and how all of these different paradigms
00:00:11.519
actually advise us to create our
00:00:14.940
abstractions in a different way as means
00:00:18.060
to solve a specific problem and all
00:00:20.039
these paradigms consider something
00:00:22.380
different to be the primary problem of
00:00:25.199
programming and in most cases depending
00:00:28.260
on what you're building it might be a
00:00:29.760
different problem I'm going to start by
00:00:31.500
introducing oop uh object orientated
00:00:35.160
programming I have already started
00:00:37.079
introducing it in the previous lesson
00:00:38.820
there's no particular reason why I start
00:00:41.160
with that first apart from the fact that
00:00:44.520
it was kind of the main Paradigm for a
00:00:47.399
very long time 20 years ago 15 years ago
00:00:50.579
leading up to 10 years ago you wouldn't
00:00:54.120
actually have even considered writing
00:00:56.520
your code in any other Paradigm except
00:00:59.219
for object oriented programming and in
00:01:02.699
the last decade we've actually just seen
00:01:04.260
a very big change in terms of that just
00:01:07.200
because some of the actual things that
00:01:10.140
we're building on the web nowadays are
00:01:12.600
traditional oop approach actually
00:01:14.640
struggles with I think at some point
00:01:16.680
point will also have to chat about there
00:01:19.260
are different flavors of oop and I think
00:01:21.960
sometimes that Nuance is lost as well
00:01:24.119
and people come to JavaScript with a
00:01:28.619
class-based oop mindset whereas
00:01:32.040
JavaScript is actually a prototype based
00:01:35.460
language you're not a class-based
00:01:37.320
language which is why I'm not a big fan
00:01:39.299
of this term class and I've kind of been
00:01:41.820
mentioning this a lot of times and
00:01:43.860
hopefully in this lesson I can actually
00:01:45.479
start unpacking a little bit why I
00:01:47.880
actually think loss isn't the best name
00:01:49.979
for what classes actually are in
00:01:52.680
JavaScript but it is what it is and we
00:01:54.659
have to work with it all right so before
00:01:56.640
I start with anything else I want to
00:01:59.659
quickly just write some example code and
00:02:02.520
then we're going to return to tasks and
00:02:04.740
we're going to look at how we can
00:02:06.119
actually use the principles of
00:02:08.758
encapsulation specifically as
00:02:10.979
encapsulation expressed by oop because
00:02:13.920
other paradigms also have opinions about
00:02:16.260
in cap isolation but let's look at it
00:02:18.120
purely from an oop perspective and how
00:02:20.700
we can apply that to create an actual
00:02:23.040
task entity so in the previous lesson we
00:02:26.819
spoke about in oop you have this idea of
00:02:29.160
things that have data and behavior so
00:02:32.580
how can we create a task which is a
00:02:34.860
thing that has data and behavior and
00:02:37.440
what would the other thing things quote
00:02:39.480
unquote be in our app let me just down
00:02:42.959
here create a trusty old
00:02:45.680
example dot JS file and its core I've
00:02:50.760
mentioned this now a couple of times oop
00:02:52.980
is about co-locating your data and your
00:02:57.540
behavior and you do that by means of
00:02:59.940
something called encapsulation in oop
00:03:02.459
let me just show an example of this okay
00:03:05.360
so let's say let's return to the very
00:03:09.300
very very first example we ever did in
00:03:12.000
JavaScript that tally app that we built
00:03:14.580
maybe also is take a moment to reflect
00:03:16.980
on how far you've come since then think
00:03:19.500
about how confusing JavaScript was and
00:03:22.560
how much more you know about JavaScript
00:03:24.659
now but also I often find that think
00:03:27.720
about how easy you thought JavaScript
00:03:29.640
was going to be and now that you're a
00:03:31.620
bit deeper in you actually realize how
00:03:33.300
hard it is
00:03:34.379
hold on to that feeling you're always
00:03:36.300
going to feel that feeling in your
00:03:37.920
career and I can trust you it's gonna
00:03:39.840
get worse give it a year give it two
00:03:42.060
three years get to the point where I am
00:03:44.519
right now and I feel like your
00:03:46.799
JavaScript is so much more complicated
00:03:49.019
than I ever thought five four three two
00:03:52.200
a year ago this is paradox where as you
00:03:55.080
grow you just also start developing an
00:03:57.659
appreciation for how much deeper it goes
00:04:00.360
but the good news there is like you can
00:04:02.459
build your entire career not only on
00:04:04.920
JavaScript but just on one aspect of
00:04:07.080
JavaScript you can build your entire
00:04:08.700
career around a single framework in
00:04:10.799
JavaScript because the rabbit hole ghost
00:04:12.959
goes so deep you can spend your entire
00:04:14.819
life this is just trying to get better
00:04:16.918
at JavaScript and getting better at
00:04:18.418
programming in general right so that out
00:04:21.180
of the way let's talk about that example
00:04:23.759
so in that example we had a value let's
00:04:27.900
say let value because we know it's going
00:04:30.300
to change it's not a const if it was a
00:04:32.520
const we won't be able to change it and
00:04:35.340
then we have two functions so let's just
00:04:37.020
say increase and const decrease which
00:04:41.100
takes value and minuses from it all
00:04:44.580
right I also realized that in the
00:04:46.500
previous session we actually haven't set
00:04:48.660
up eslint and prettier and all those
00:04:51.300
things for this project so let's just
00:04:52.800
quickly do it right now right so by the
00:04:55.380
magic of video editing I've just quickly
00:04:57.660
set up all the eslint stuff I'm
00:04:59.940
obviously not going to cover all of it
00:05:01.320
again if you can't remember how to do
00:05:04.020
that just check out the video again in
00:05:06.780
code style but I quickly just behind the
00:05:10.800
scenes set it up again so I don't have
00:05:12.240
to spend time in this video actually
00:05:13.919
going through it once again so just a
00:05:16.680
reminder if you Contour me about how to
00:05:18.900
do it or if you don't know what I'm
00:05:20.040
talking about
00:05:21.360
um just check out how I set up eslint
00:05:23.460
and prettier and all of those things in
00:05:26.280
the code Style videos all right so task
00:05:30.300
is defined but never used and the reason
00:05:34.020
for that is because we pulled that in
00:05:37.440
purely just for odd types so in this
00:05:41.520
case we might need to ignore that
00:05:43.740
specific rule so just say eslint
00:05:47.000
disable next line but we don't want to
00:05:51.120
disable everything so usually I just
00:05:52.919
type a random character there and I just
00:05:54.720
check no unused bars because you do want
00:05:58.620
to get that notification when that is
00:06:02.039
actually the case again that's also
00:06:03.479
complaining because we're not using this
00:06:05.280
ever but we are going to also
00:06:07.800
complaining that we're not using this
00:06:09.120
also complaining that we're not using
00:06:10.680
changes and so forth okay these make
00:06:12.660
sense they are to be expected so state
00:06:15.900
is still fine helpers is also fine and
00:06:20.160
scripts is going to be a mess because we
00:06:23.580
used it last time for our example so let
00:06:26.340
me just clear scripts okay
00:06:28.319
so let us get into this okay and that is
00:06:31.440
unhappy pipe safety let's add TS check
00:06:34.259
so it automatically just assumes this is
00:06:36.419
a number unless we State otherwise we
00:06:38.819
can run increase decrease increase and
00:06:43.560
then the console and let us run this in
00:06:46.380
the browser cool and that is four so
00:06:48.600
obviously STAR test three we add one we
00:06:51.060
remove one we add one more and that's
00:06:52.860
four so this is pure purely procedural
00:06:55.380
programming you're running these as
00:06:57.720
instructions so how would we actually
00:07:00.539
refactor this into an oop approach so
00:07:03.960
let us get down to what is the basic
00:07:06.720
premise of oop and I think we need to
00:07:09.000
hold on to this because there's a lot of
00:07:10.860
fusing and misleading and just like
00:07:13.139
actually plain incorrect information out
00:07:15.479
there about oop if you just go on
00:07:17.400
YouTube you will see a ton of videos
00:07:19.740
about oop and there's a ton of really
00:07:23.220
really bad information out there like be
00:07:25.139
careful at the Crux always hold on to
00:07:27.840
this because someone will tell you you
00:07:29.520
need to use a class for oop or you need
00:07:32.160
to use inheritance with or extends with
00:07:34.680
oop or it just comes down basically to
00:07:38.340
combine your data and behavior into a
00:07:42.539
single encapsulated unit okay so data so
00:07:46.680
here we have our data up here here we
00:07:48.360
have our Behavior none of this is
00:07:50.880
encapsulated because you can call it
00:07:53.280
from anywhere I can even just go here
00:07:55.259
and directly change it and say no I
00:07:57.660
actually want value to be ABC you know
00:08:00.060
so none of this is encapsulated with if
00:08:02.520
this is encapsulated the interface there
00:08:04.560
would be an interface that controls what
00:08:06.780
we can actually do the the easiest way
00:08:09.780
to do this in JavaScript is with a plain
00:08:13.139
object literal period you can do oop in
00:08:16.319
JavaScript with a plain object literal
00:08:18.120
people have been Gene overp in
00:08:19.560
JavaScript way before classes classes is
00:08:21.599
only classes was only added like five
00:08:23.699
six years ago let's have a constant
00:08:25.919
let's call this counter and what is
00:08:28.319
counter so counter inside it has a value
00:08:31.259
that starts as one it has a method in it
00:08:35.039
that is increase and all this method
00:08:37.080
does it checks counter or this takes the
00:08:40.620
value and does that we have decrease
00:08:43.260
where we just do the opposite and then
00:08:45.660
we just have display which just console
00:08:48.720
logs this and we need to just add some
00:08:52.200
commas there to separate them why am I
00:08:54.839
using this
00:08:55.920
um yeah I did mention you know this
00:08:57.779
sucks try and avoid using this you so
00:09:00.120
you can actually even just do this all
00:09:01.980
right let me just comment all of this
00:09:03.720
out and so now we can do counter and
00:09:06.540
you'll see we actually get Auto
00:09:08.519
completed things and you know let's even
00:09:11.160
take this a step further let's actually
00:09:13.080
add you know some jazz doc so you're not
00:09:15.420
adding anything but you can't say hey
00:09:17.160
this method actually takes something but
00:09:18.779
let's just say increases counter value
00:09:21.959
by one and this is decreases counter
00:09:25.740
value by one logs the counter value to
00:09:29.580
the console obviously the value itself
00:09:31.680
is just the actual tracked value let's
00:09:35.279
do that so let's do counter and then we
00:09:37.440
see oh these are all the things that are
00:09:38.940
encounter so in vs code it'll also show
00:09:41.640
the purple squares an actual method and
00:09:44.399
the blue square is actual value let's
00:09:46.980
say we want to increase it okay and it
00:09:49.200
knows it's a function so it needs we
00:09:50.580
need to call it let's increase it two
00:09:52.680
times and let us just then run display
00:09:55.560
and there we go three so it starts as
00:09:58.080
one we increase increase and display
00:10:00.480
three so there's a couple of things here
00:10:02.519
so the first one being that you don't
00:10:05.399
have full encapsulation here because you
00:10:08.279
can and still go counter dot value
00:10:11.720
equals so if value is something in this
00:10:15.060
object and we don't want people to
00:10:18.000
actually to be able to do this in our
00:10:20.220
code unfortunately we that is just the
00:10:23.100
reality with objects and classes also
00:10:26.279
suffer from this but there are some
00:10:28.080
actual ways to solve that but the
00:10:30.779
simplest way in the way people have been
00:10:32.580
doing this for a very long time since
00:10:35.279
almost the start of JavaScript is to use
00:10:37.260
a closure instead of just having our
00:10:39.720
counter expressed like that let us do
00:10:41.880
the following let's wrap that in a
00:10:44.040
function that creates the counter for us
00:10:46.140
so you remember about closures and
00:10:48.120
Scopes and so forth we can actually use
00:10:49.980
it to hide things because remember a
00:10:53.459
closure or a scope only has access to
00:10:56.519
the things above it not below it and we
00:10:58.920
can use that to our advantage to
00:11:00.420
actually hide things so const and let's
00:11:03.180
just say create counter and this is
00:11:05.339
something called a factory function I
00:11:07.800
usually have the invention that I prefix
00:11:09.899
my factory function functions with
00:11:11.820
create you will see the same thing in
00:11:14.940
reactor and so forth so for example you
00:11:18.120
will see you know for example create ref
00:11:21.180
or whatever and so inside that scope let
00:11:24.779
us create our actual object so we're
00:11:27.600
just wrap setting it directly in an
00:11:29.700
actual object we just handle it in here
00:11:32.040
like we did before so let's just say let
00:11:33.779
value and it starts as one and then we
00:11:36.600
create our functions in here honestly
00:11:38.880
like this is my actual preferred way of
00:11:41.640
oop or working with objects in
00:11:43.980
JavaScript it is nice separating your
00:11:48.360
actual logic from the actual interface
00:11:51.779
that you actually Expose and I'll show
00:11:54.540
you in a second and for example react
00:11:56.519
allows you to do the exact same thing
00:11:58.380
all that this does is value plus plus
00:12:01.200
one and value yeah and let's also just
00:12:03.899
add some extra code here like so there's
00:12:06.600
an optional value it's that actually
00:12:09.240
says well let's just say a melt we have
00:12:11.399
a mount and that is by default the
00:12:14.040
amount otherwise it just falls back to
00:12:17.459
one if you don't specify that and so
00:12:20.399
then we also have our display console
00:12:23.940
log the value itself all right so all of
00:12:26.100
this is encapsulated uh if we for
00:12:28.620
example go just comment all of this out
00:12:31.200
if we for example down here go you know
00:12:33.779
counter and create counter there's no
00:12:36.600
way we can actually access that value
00:12:38.399
from the counter like actually nothing
00:12:40.440
is getting exposed there's nothing like
00:12:42.720
all of this is inside the scope you
00:12:44.700
can't go from outside the scope into the
00:12:47.579
scope of this function physically
00:12:49.260
nowhere in JavaScript so there's no way
00:12:51.540
from outside this function that you can
00:12:53.639
actually get the information inside it
00:12:55.800
unless you actually expose it so I
00:12:57.779
really like Factory functions I actually
00:12:59.399
prefer them much over classes but this
00:13:01.980
is just a personal preference
00:13:03.839
um if you like classes you like working
00:13:05.940
with classes that make sense to you by
00:13:07.980
all means to use classes functionality
00:13:10.260
and Frameworks actually require classes
00:13:13.139
angular is is a big example where
00:13:15.660
everything is a class even native things
00:13:17.820
like web components you need to use a
00:13:20.700
class and this is sometimes a
00:13:22.500
frustrating thing about JavaScript like
00:13:24.360
it's not even consistent in that then
00:13:26.519
there are other things that are exposed
00:13:28.139
through means of a factory so I would
00:13:30.480
say for all intents and purposes proxy
00:13:32.760
is a factory I'm not going to explain
00:13:34.019
how proxy works now but so forth and you
00:13:36.060
know it's all over the place in
00:13:37.079
JavaScript that's one of the reasons why
00:13:38.519
JavaScript sometimes hard to work with
00:13:40.860
yeah so do what makes sense to you
00:13:43.139
um when you're working with something
00:13:44.399
existing do what that thing does if
00:13:47.639
you're working with a team that has a
00:13:49.079
specific convention just do what they do
00:13:51.480
a consistency is key and it's also the
00:13:54.360
differences between these things aren't
00:13:56.040
that critical but if you have a
00:13:57.600
preference and you're writing your own
00:13:58.980
code then go with the one you enjoy
00:14:00.660
working with
00:14:01.680
so as mentioned what I like about this
00:14:03.779
one is then you actually return an
00:14:05.760
object but in that object this is kind
00:14:08.160
of like the package that you actually
00:14:09.720
deliver from this function so you do all
00:14:12.240
your logic and then you decide cool what
00:14:14.100
what am I packaging up in like a little
00:14:15.779
box and like giving back afterwards you
00:14:19.079
can even literally just do it you know
00:14:20.700
like this create your object there and
00:14:22.980
then just return the object or you can
00:14:25.740
just create it in the return itself what
00:14:27.959
I'm doing here right now is I'm just
00:14:29.639
giving display increase and decrease
00:14:31.440
that is all you can do there's no way to
00:14:34.019
get this value because that's all that I
00:14:35.940
return so it creates this object for me
00:14:38.519
with the factory function and I can only
00:14:41.399
decrease display or increase I can't do
00:14:43.800
anything else I can't go value equals
00:14:46.139
10. JavaScript thinks I can and the
00:14:48.660
reason for that is complicated but just
00:14:50.399
to show you guys that I can't actually
00:14:51.720
if I then go if I then run down to
00:14:54.540
display here it's actually not going to
00:14:56.820
log that so let me show you show you one
00:14:58.860
what's that all about and so there's a
00:15:01.199
couple of reasons for this the one is we
00:15:03.720
actually didn't create an interface
00:15:05.579
let's quickly do that and that's going
00:15:07.380
to also prevent this from happening so
00:15:09.240
let's just type def let's create our
00:15:11.279
interface here counter and count as an
00:15:13.680
object I want to effectively just has
00:15:16.260
the following functions on it so once
00:15:18.839
again we can if you like like if you
00:15:21.180
want to do the quick route you can go
00:15:23.339
increase uh decrease display and you
00:15:27.420
know this is a case away down here sorry
00:15:29.339
is where eslint is complaining but we
00:15:32.100
actually know better so and as I saved
00:15:34.500
it actually reformatted this for me as
00:15:36.720
well and so increase so I can actually
00:15:39.300
just so I can write it like this in here
00:15:42.240
you know but let's just stick with
00:15:44.820
jstock proper and here we can actually
00:15:47.639
use a bit of abstraction and reuse Joe's
00:15:51.000
dock so we can actually say we're going
00:15:52.199
to create a function we're just going to
00:15:54.000
call that function modify that just
00:15:56.459
takes a single param which is a number
00:15:59.040
and it's also optional and that param's
00:16:01.260
name is amount and we're indicating it's
00:16:03.600
optional like that and we can just say
00:16:05.760
amount modify the value with and now
00:16:10.500
check this out we can actually oops and
00:16:12.839
I actually made a typo this is one of
00:16:15.300
those classic typos where as you're
00:16:17.100
talking you actually type the right
00:16:18.899
thing because of a saying function but
00:16:20.579
in just doc you actually have to say
00:16:22.500
callback if you remember from the last
00:16:24.540
time and then this is we can also just
00:16:27.600
create another one so it's also once
00:16:29.279
again it's useful to sort of callback
00:16:31.500
and we can just call that just call that
00:16:34.500
empty function in other words it's a
00:16:36.660
function that doesn't take anything it
00:16:37.920
doesn't return anything is we can just
00:16:39.839
say at returns a counter so create
00:16:42.779
counter returns a counter if we hover
00:16:44.880
over that we can even give counter a
00:16:47.160
description if we want and we can say an
00:16:49.380
object that keeps internal State and
00:16:53.639
allows you to increase decrease log the
00:16:57.959
value note that there is no way to to
00:17:02.040
access the value from inside so now
00:17:05.520
it'll actually warn us and say this
00:17:07.260
isn't part of the interface that we
00:17:08.939
provided so counter and that's just
00:17:11.040
unhappy because we don't use it this
00:17:13.020
type of this thing is counter so let's
00:17:14.819
just do counter and what do we want to
00:17:17.040
do we want to increase and if we hover
00:17:20.760
over that okay and let's also just add
00:17:23.459
some uh increases I can't remember what
00:17:25.919
we said previously oh here it is
00:17:27.419
actually so this is actually the type of
00:17:29.580
comments you shouldn't write they're not
00:17:31.799
very I guess they're of value at the
00:17:34.919
release it says what you're going to
00:17:36.419
increase but and I also did this wrong
00:17:38.760
and this should actually be like that
00:17:40.679
I'm obviously just doing these to
00:17:42.840
illustrate a point don't look at this as
00:17:46.080
kind of the best way to write comments
00:17:48.299
All right so now this ground set counter
00:17:51.179
all right and these are the two things
00:17:53.220
we can do at the counter so if you say
00:17:54.840
increase and we hover over it okay
00:17:57.240
increase counter value
00:17:59.039
provider value or we can leave it so
00:18:01.919
let's just leave it and then let's count
00:18:04.260
a decrease by 10 and counter display
00:18:08.640
right so minus eight there you go what's
00:18:11.340
also nice about having Factory functions
00:18:14.460
is that we can actually use it to create
00:18:16.860
different instances of something so
00:18:18.720
let's say you know temperature and let's
00:18:21.240
also just have humidity and so we can go
00:18:24.179
humidity increase by 20 temperature
00:18:28.440
decrease by three temperature increase
00:18:32.240
by by 10 and then we can just display
00:18:36.419
temperature display right there we go
00:18:39.240
but so let's say we actually want to
00:18:42.299
from the start actually Define what
00:18:45.480
these things are when we create them we
00:18:47.820
want to have different information
00:18:49.380
because at the moment they are the exact
00:18:52.140
same thing so what we can do is we can
00:18:53.880
also put something else in here and
00:18:55.919
let's say we pass that through actual
00:18:58.799
parent M so let's say at RAM and that is
00:19:02.160
just a string and we can call it label
00:19:04.260
all right then we can just put a
00:19:05.580
description there the actual value that
00:19:09.240
is being measured okay and it's unhappy
00:19:11.880
because we obviously need to put label
00:19:13.260
in there and label is required and it's
00:19:15.419
also unhappy because we're not using
00:19:16.740
label and so what we can do is let's
00:19:19.740
actually just only place we use the
00:19:21.960
label is when we are outputting like
00:19:24.720
that so now this is unhappy because
00:19:26.280
we're not adding labels so let's say
00:19:28.020
Celsius I don't even know what what do
00:19:30.720
you measure humidity in let's just go
00:19:33.240
with humidity factor I don't even know
00:19:35.520
what you measure I'm not going to Google
00:19:36.900
it now so now when we do that should
00:19:40.140
actually because we're passing in an
00:19:42.059
actual things at when we create them so
00:19:44.340
you can set configurations when you
00:19:46.559
create them with a with a factory
00:19:48.000
function 21 humidity factor and eight
00:19:50.580
Celsius so let's say you should be able
00:19:53.580
to actually get the label at any time
00:19:55.620
you know export it there as well we
00:19:58.740
can't you don't have it in our actual
00:20:01.320
interface so let's just do and this is
00:20:03.360
the string and label so now you can even
00:20:06.059
go let's say we want to see what is the
00:20:08.580
actual humidity label you can grab it
00:20:11.160
and console log it okay so it actually
00:20:12.960
gives us humidity Factor today but the
00:20:15.120
problem is now so let's say you want to
00:20:18.299
be able to go you know temperature label
00:20:21.780
and you want to set it to fahren
00:20:24.480
I think that's how you spell it to say
00:20:27.059
if so let's say you want to do that okay
00:20:29.940
yeah it didn't update it still says
00:20:31.799
Celsius so why is that and then that is
00:20:33.480
because we are actually just exporting A
00:20:35.940
Primitive if you remember one of the
00:20:38.520
things about Primitives and composite
00:20:41.160
types is that uh Primitives are actually
00:20:44.700
immutable you can't actually go and all
00:20:48.780
the way up back through the argument
00:20:50.880
that's being passed and and we shot a
00:20:54.000
couple of examples where this actually
00:20:55.380
happens by accident but generally you
00:20:57.539
want to avoid this but that also means
00:20:59.340
you can't do this because if we can
00:21:00.600
maybe try and do the following so let's
00:21:02.280
do let and let's do inner label and that
00:21:05.460
just comes from the label and then
00:21:07.440
actually what we export here is the
00:21:09.179
inner label and you'll see but okay so
00:21:11.520
there's a couple of things going on here
00:21:12.780
and the one is that Airbnb says it's a
00:21:15.900
const so why are you assigning it to a
00:21:17.640
let it's actually very smart and so far
00:21:20.280
that it knows once we pass it through
00:21:22.020
this object you're not going to be able
00:21:23.520
to change it afterwards what you can do
00:21:26.160
is you can use Getters and Setters and
00:21:28.559
this is what I like where I like Factory
00:21:30.659
functions maybe a bit more than I like
00:21:32.340
classes is because there's a there's a
00:21:34.799
clear separation here that the interface
00:21:37.440
you can't go back and update values
00:21:39.900
through the interface unless it
00:21:41.700
explicitly says you can't updated which
00:21:44.640
is what you don't get with a class if we
00:21:47.220
want to add that functionality so what's
00:21:48.900
nice here is by default it's disabled
00:21:51.120
unless you actually enable it and you
00:21:54.240
can do that by means of Getters and
00:21:55.740
Setters label so again a set is a method
00:21:59.159
generally you always have a good and a
00:22:01.440
Setter you always use them in
00:22:03.000
combination just for me out of habit and
00:22:05.340
like I find it just good to use both of
00:22:08.039
them and they're both so both sides even
00:22:09.960
if the one doesn't do anything or even
00:22:11.760
if the one literally just Returns the
00:22:14.400
actual value itself so in this case it
00:22:16.740
is just going to return Innova in a
00:22:18.600
label okay so this is maybe a bit
00:22:20.520
Overkill and you can probably get around
00:22:22.559
this having to save yourself from
00:22:24.659
writing both together in the setter but
00:22:27.120
usually for me I just out of good
00:22:28.919
practice do both just so I know I have
00:22:30.960
accounted for both so you actually
00:22:32.520
control what happens when Trump someone
00:22:35.100
tries to get a value from this interface
00:22:37.559
or they actually try and set a value to
00:22:40.380
this interface so with the setting you
00:22:42.600
know you can completely just prevent
00:22:43.919
that you can even go so in here you
00:22:46.320
would actually get the value that's
00:22:47.640
trying to be set you can even throw an
00:22:49.799
error if that is not allowed then what
00:22:53.100
we currently have here as someone thinks
00:22:54.960
is being set and then when they log it
00:22:56.820
it actually never updated you can just
00:22:58.799
here say label can not be updated to and
00:23:04.140
it is unhappy because at line 27 we
00:23:07.559
already have value yes so let's just
00:23:10.799
call this new label and in a label is
00:23:14.880
const okay because it never gets updated
00:23:17.340
cool so label cannot be updated to F but
00:23:20.400
let's say we want to do that so now we
00:23:21.900
can actually just put actual logic in
00:23:24.299
here and we can just say take in a label
00:23:26.880
and set it to the new label obviously
00:23:28.799
this is unhappy because it's a const
00:23:30.720
let's make it a let that we actually
00:23:32.700
need to read from in a label here and so
00:23:35.159
we also need to ensure that we're no
00:23:37.080
longer reading from there but actually
00:23:38.700
from the variable there we go it turns
00:23:41.340
it to F actually and you can even do
00:23:43.080
anything you want like you have a lot of
00:23:44.880
power here you can actually say don't
00:23:46.740
actually replace it you can actually say
00:23:48.919
modify it actually before you assign it
00:23:51.780
the changer to is the label boy so we're
00:23:56.580
setting if but it's actually modifying
00:23:59.280
it because of the internal logic and
00:24:01.799
likewise you can actually override the
00:24:04.320
getter as well so you can so let's say
00:24:06.059
we're actually not ever actually
00:24:07.919
reassigning it we just want to check
00:24:09.780
what it is so let's say we've console
00:24:11.340
log it here we go so LCS is the label oh
00:24:13.740
boy you can even just straight up say
00:24:16.320
when they try and get label it's just
00:24:18.780
gonna return hello you're gonna
00:24:21.240
completely override this as well and say
00:24:22.980
you know when they try and said it it
00:24:25.260
doesn't even care about new label it
00:24:27.120
just takes inner label and sets it to
00:24:28.919
you know so like you you have a lot of
00:24:31.080
power here not only that but you can
00:24:33.120
even just like have it return something
00:24:34.740
random every time you call it new math
00:24:36.960
and I need to turn it to a string
00:24:39.240
because it is actually I marked it up as
00:24:41.400
a string up here let's just do console
00:24:43.679
log temperature label and every time we
00:24:47.280
log it it's going to just give us
00:24:48.480
something random because it's just
00:24:50.520
executing this and returning that so
00:24:52.500
this is what I like about Factory
00:24:53.700
functions is so just quickly there's no
00:24:56.640
one other thing I not sure why that I
00:24:58.799
mentioned it before but I I spoke about
00:25:00.480
these structuring you know so for
00:25:02.159
example if you have an array
00:25:04.039
that is you know one two three four you
00:25:08.580
can go into structure uh you know that
00:25:11.700
first button
00:25:14.240
one thing you can also do is you can do
00:25:16.860
the remainder and so if I do you know
00:25:20.299
or whatever or you know remaining or
00:25:23.340
whatever and it's going to take what you
00:25:26.340
didn't destructure so in other words and
00:25:28.860
just provide that as an array
00:25:31.559
uh it's the same with objects as well so
00:25:35.059
if I destructured for example first and
00:25:40.460
second and then whatever's left in the
00:25:43.260
object will just be returned as a new
00:25:45.659
object but you can also do spreading
00:25:47.700
it's just exactly the opposite so inside
00:25:51.120
another array or inside another object
00:25:55.020
you can actually just go props and it's
00:25:59.640
going to spread everything that gets
00:26:01.260
part in the incubus so you might ask
00:26:03.840
okay it's called but what is the
00:26:05.760
difference between object sine if I do
00:26:08.700
this where I combine two objects
00:26:11.820
together and the spread operator that
00:26:14.159
just used and the answer is absolutely
00:26:16.080
nothing I just find a little bit more
00:26:17.760
readable but you know
00:26:20.100
depends on what you prefer personally um
00:26:23.100
I prefer just using the spread operator
00:26:24.960
yeah so we update our HTML task there
00:26:27.779
would be changes and but then we don't
00:26:30.059
do anything of changes in here what we
00:26:32.760
want to do is we want to see if those
00:26:35.760
changes are present and then actually
00:26:37.679
update the HTML and so here we're
00:26:40.559
actually still using the old way so we
00:26:42.900
would actually just go
00:26:44.640
8 HTML which would have the validation
00:26:47.460
Falls in and we would just say pause so
00:26:50.580
that gets rid of all of this code for us
00:26:52.320
so let us restructure all those values
00:26:54.480
here
00:26:55.860
the changes new title but you might say
00:27:00.840
listen like what if we only pass title
00:27:03.179
yeah then urgency due and complete or
00:27:05.340
not it's going to be undefined okay so
00:27:07.740
you might also be tempted to go so if
00:27:10.320
completed in other words if complete has
00:27:13.140
been passed and this is sorry
00:27:16.320
um for the audio quality there guys
00:27:19.200
um it's embarrassing to admit but I I
00:27:21.539
realized my mic was facing the other way
00:27:24.120
around so just heads up sorry about that
00:27:26.340
but here we go now we're back on track
00:27:28.740
um I hope you were able to get that so I
00:27:31.080
was saying that you know if you check if
00:27:33.000
completed is there then kind of make the
00:27:35.100
change the problem here is keep in mind
00:27:36.960
that because of the way truthy and falsy
00:27:39.059
works if you pass completed to be false
00:27:42.419
if you say hey I want completed but I
00:27:44.520
want it to be false it would actually
00:27:46.320
not trigger because it checks if it's a
00:27:48.779
truthy value so you would actually have
00:27:51.120
to check if it's not undefined so if if
00:27:54.179
you're not selling it it's going to be
00:27:56.520
undefined also another thing which I
00:27:58.860
maybe forgot to mention you might have
00:28:00.659
seen that my code editor if I do things
00:28:04.500
like you know this like triple equals or
00:28:07.919
strictly quality of or if I do not
00:28:10.260
equals it does that or greater than or
00:28:14.039
even Arrow functions it actually creates
00:28:17.039
these what's called ligatures so I just
00:28:20.220
actually use so the font that I use in
00:28:22.799
my IDE is something called
00:28:24.799
firear code you can actually just have a
00:28:27.059
look so it's if I are a so like fire but
00:28:31.020
with an A and it's this one here at the
00:28:34.200
top so almost 50 000 as you'll see it
00:28:37.200
kind of does these ligature type things
00:28:38.880
maybe you don't like it maybe you like
00:28:40.620
it I think it actually makes my code
00:28:42.659
more readable so just I actually never
00:28:45.059
mentioned that explicitly but so if
00:28:47.880
you've been curious about that now you
00:28:50.640
know if completed is not undefined do is
00:28:55.740
not undefined so what I would actually
00:28:58.740
do in this case like and it depends on
00:29:01.200
what what works for you I would actually
00:29:03.299
just write it like this has do as title
00:29:07.320
and has urgency and just get that value
00:29:11.039
first
00:29:12.000
um just find it a little bit more
00:29:13.500
readable because this this not checking
00:29:16.980
for a true not State um sometimes it's a
00:29:19.679
bit confusing so I actually just write
00:29:22.320
it like that so then we can say F has
00:29:24.000
completed if has date a has to if has
00:29:28.440
title if has urgency all right so has
00:29:32.100
completed so what we want to do is we
00:29:34.799
want to get the HTML for that and we can
00:29:37.980
just actually write it as follows get
00:29:40.500
HTML and that will be I don't think we
00:29:44.460
actually have set these yet so let's
00:29:46.860
actually do that so that will be data
00:29:49.520
checkbox data table let's actually move
00:29:53.700
this up to the and let's also make this
00:29:55.559
up but because it's something you'll
00:29:58.320
click and let's do data delete all right
00:30:01.980
so now we have our three things there so
00:30:04.440
get HTML checkbox we're not actually
00:30:07.860
doing anything with you or urgency so
00:30:10.980
that's actually just these so we act so
00:30:13.919
we I think we're going to do something
00:30:15.299
with you a bit later so let's just keep
00:30:17.460
this in for now I'll just comment it out
00:30:20.220
you can still pass it here we might want
00:30:22.919
to put a note keep in mind that do can
00:30:27.720
also be passed but we don't do anything
00:30:33.020
with it yet and you'll actually see for
00:30:36.120
regular comments that are not like J
00:30:37.860
stock I just write them like this with
00:30:40.860
the regular forward slashes just to
00:30:43.200
separate them from JS dot comments so
00:30:45.720
let's just remove that the element so we
00:30:48.779
have element which is an HTML element
00:30:50.700
also we're not doing anything with
00:30:52.860
urgency as well keep in mind that
00:30:55.320
urgency e and also be passed but we
00:30:57.840
don't do anything with them yet one
00:31:00.720
thing to keep in mind here so we have
00:31:02.279
this gate HTML but it's going to check
00:31:04.799
against the entire document we just
00:31:06.779
wanted to check inside that specific so
00:31:09.899
what you can do is we can add a third
00:31:11.940
parameter here param and that will be an
00:31:16.080
optional HTML element that you can't
00:31:18.120
pass and that'll just be the target so
00:31:21.240
this will be what where it tries to get
00:31:23.700
that HTML make it as simple as saying
00:31:26.220
Target so in here we can just do scope
00:31:29.940
and that is just Target if there is a
00:31:32.340
target or if there's not just fall back
00:31:34.620
to document all right so it's an
00:31:37.140
optional thing that we can't pass and
00:31:39.720
whatever we pass there is where you
00:31:42.840
select is going to be run on alternative
00:31:45.059
is going to be applied to the document
00:31:46.559
so this is actually an indication of a
00:31:49.919
really good abstraction because we
00:31:52.679
actually change the the behavior quite
00:31:55.260
dramatic practically but we actually
00:31:57.659
needed to do the very minimal changes it
00:32:01.260
literally just okay so obviously the
00:32:02.520
Jazz doc we have to do so we just added
00:32:05.700
this here and we just added this here
00:32:07.620
and now we have like this massive new
00:32:09.960
piece of functionality generally these
00:32:12.299
are signs of like really good
00:32:14.220
abstractions is that when you're
00:32:16.500
changing things like it actually takes
00:32:18.659
very minimal of effort because also now
00:32:20.760
like the likelihood of us us introducing
00:32:22.860
a new bug or breaking something existing
00:32:24.899
on the site actually isn't that big
00:32:27.120
everything else can still be used as it
00:32:29.279
is and you know just with experience you
00:32:31.500
get better at anticipating these type of
00:32:34.080
things or building things in a manner
00:32:36.059
where they can easily be extended like
00:32:38.580
this once again by separating it up into
00:32:41.100
these two things that also make like
00:32:44.100
prevents it from being like a massive
00:32:46.200
change there might be something else
00:32:48.059
that's now also has to be updated over
00:32:50.700
here and so or it might update how we
00:32:53.159
kind of do like now so these by break or
00:32:56.399
whatever so there's a lot of value in
00:32:58.440
keeping things like single
00:33:00.299
responsibility and this is and and the
00:33:02.640
difference here is why we split this up
00:33:04.740
into a separate thing and why we didn't
00:33:07.520
do targeted HTML or whatever just copied
00:33:10.919
that and created a completely new thing
00:33:12.539
is this I like this is still within the
00:33:15.059
same responsibility I would say that
00:33:17.159
checking if something exists or actually
00:33:20.100
getting that thing like these are still
00:33:22.260
the same responsibilities and so we're
00:33:24.360
just adding we're just extending that
00:33:26.880
responsibility we're not changing or
00:33:29.220
adding new types of responsibilities
00:33:31.140
okay so but those things they're very
00:33:33.899
nuanced and it takes a very long time to
00:33:35.580
really get good at them and get a feel
00:33:37.380
for them so this is also a very good
00:33:39.539
example where I actually find props to
00:33:42.240
be better than arguments because now
00:33:44.399
what we need to do is we need to pass
00:33:46.559
them in order we need to pass undefined
00:33:49.019
first all right so let's just also
00:33:51.120
quickly change that to actual props and
00:33:55.140
once I again you know this is going to
00:33:56.820
be a very easy change so let's just
00:33:58.860
replace that with props let's create a
00:34:01.679
single param up here which is an object
00:34:05.120
and let's just call it props and then we
00:34:09.480
just go props dot data attribute
00:34:12.739
props.value
00:34:14.540
props.target
00:34:16.099
destructure them here so let's just do
00:34:18.300
that put them in this but instead of
00:34:20.339
prop and there we go it's as easy as
00:34:23.520
that once again you know like so the
00:34:25.139
sign of a good abstraction is that it's
00:34:27.599
very easy to change and because you
00:34:30.659
don't have a lot of experience with this
00:34:32.339
once again that's going to be very hard
00:34:34.440
for you to preempt but it's just useful
00:34:37.739
to say that that is how you learn as
00:34:40.320
well so be mindful of that if you create
00:34:42.239
abstractions and it's very hard to
00:34:44.159
update them very hard to change them
00:34:46.139
very hard to extend them then you could
00:34:49.619
have probably done it better and that's
00:34:51.300
how you learn like eventually you get a
00:34:53.159
sense for what abstractions are easy to
00:34:55.080
change what is easy to update and extend
00:34:57.540
and so forth and once again like this
00:35:00.420
isn't within the realm of the open close
00:35:02.880
principle because because the type of
00:35:05.520
extension that we're doing here isn't
00:35:07.859
regarding actually adding new things
00:35:10.440
they're actually extending the scope of
00:35:14.640
what the abstraction does so it actually
00:35:17.160
allows you to give it a specific value
00:35:19.140
now as well whereas in the pre previous
00:35:21.359
one because we had that Loop every time
00:35:24.359
we add a new type of thing we're going
00:35:26.339
to have to add that so generally this
00:35:28.800
doesn't violate that because there's no
00:35:31.200
foreseeable reason why we might need to
00:35:33.900
modify that on a recurring basis to
00:35:36.480
maintain this functionality but there
00:35:38.520
are actual people that would say that
00:35:41.700
you need to be able to even that needs
00:35:45.060
to be solved with composition I don't
00:35:48.060
know like honestly I think that's maybe
00:35:49.980
a bit over abstraction at that point you
00:35:52.859
you get to the point where you're just
00:35:54.720
managing abstractions instead of
00:35:56.700
actually writing code actually doing
00:35:58.740
things but I think it's a balancing act
00:36:01.020
but it's just worth actually noting that
00:36:03.480
okay and this is also a static typing is
00:36:06.000
also really helped because now we might
00:36:08.640
very easily miss an example where we now
00:36:11.579
need to update it it's going to give us
00:36:13.320
alerts everywhere and where the
00:36:15.240
interface is being used and we need to
00:36:17.579
update it now and so the new one is data
00:36:20.760
attribute list all right so