00:00:00.000
in this video I am going to start
00:00:02.820
talking about functional programming in
00:00:06.180
a previous lesson we spoke about
00:00:08.480
functional programming is one of the
00:00:11.880
three paradigms alongside object
00:00:14.340
orientated programming and also
00:00:16.859
procedural programming so just to Super
00:00:19.680
quickly recap we can say effectively
00:00:23.100
that procedural programming and oop if
00:00:28.260
we compare these three the with one
00:00:30.900
another they are primarily concerned
00:00:33.660
with how you do abstractions what are
00:00:36.660
your primary abstractions so we started
00:00:39.660
off with procedural programming where
00:00:42.059
our primary abstraction was functions as
00:00:46.200
nestable instructions what does this
00:00:49.379
mean this means that I might have three
00:00:52.559
abstractions that are watch TV and buy
00:00:57.180
groceries okay so these are high level
00:00:59.399
abstraction and then Within These high
00:01:02.640
level abstractions or several nested
00:01:04.799
abstractions but all of them are treated
00:01:07.020
as nested levels of instruction so watch
00:01:09.479
TV what I need to do is I need to switch
00:01:12.659
on TV and I need to sit on couch all
00:01:17.100
right and then even in those
00:01:18.659
instructions or nested instructions so
00:01:21.659
this would be find remote press red
00:01:25.020
button on remote confirm image is on TV
00:01:29.939
and then sit on couch would maybe be
00:01:32.400
something like find couch check if couch
00:01:35.340
is clean and so forth and so forth and
00:01:38.400
you know under buy groceries we might
00:01:40.680
have you know get in car and so so you
00:01:44.280
have these high level abstractions that
00:01:47.640
abstract all the way down by means of
00:01:50.820
treating everything as nestable
00:01:52.860
functions and this almost entirely
00:01:55.979
relies on something called side effects
00:01:59.880
in other words you call the function and
00:02:03.360
then it does something else in your code
00:02:05.520
somewhere so it's a side effect of the
00:02:07.920
function so you can think of this almost
00:02:09.899
like a button that you press and
00:02:11.280
something happens so some way oop bolds
00:02:14.760
on this approach and it says instead of
00:02:17.900
primary means of abstraction being
00:02:20.160
functions as nestable instructions your
00:02:22.739
primary means of abstractions are
00:02:25.200
objects that contain both data and
00:02:29.459
behavior if we were to go back here you
00:02:32.160
might have a couple of things here you
00:02:34.020
might have t your TV and your couch and
00:02:38.160
yourself and each of these has
00:02:42.000
information and can perform actions on
00:02:45.599
themselves and they might even be
00:02:48.500
encapsulated by a bigger object which is
00:02:52.260
you know living room so let's put
00:02:54.239
yourself there outside and you know car
00:02:57.840
obviously this is a very basic example
00:03:00.660
there is a bit more Nuance to this I'm
00:03:02.459
just trying to explain the high level
00:03:04.200
principle in terms of how it thinks
00:03:06.420
about abstraction so yourself has
00:03:08.700
behavior and it has data so in in data
00:03:12.840
we might have location location accepts
00:03:16.379
either outside or it accepts living room
00:03:19.560
and then there's maybe a method that is
00:03:22.560
interact and through the principle of
00:03:24.840
polymorphism yourself doesn't need to
00:03:27.300
know in what location it is to actually
00:03:30.900
be able to execute interact so both of
00:03:34.739
these living room and outside have an
00:03:37.319
interact and when you run into act
00:03:39.300
living room maybe runs you know fine
00:03:42.360
couch or find on couch or find on car
00:03:46.440
you don't treat this as instructions
00:03:49.159
basically you have these this mapping of
00:03:52.680
objects and the way that these objects
00:03:55.920
interact with one another either through
00:03:57.959
data or behavior so let's also indicate
00:04:01.080
this abstraction over here so they talk
00:04:03.299
to one another and that is how things
00:04:05.280
happen in your app but yourself for
00:04:07.379
example doesn't know what goes on inside
00:04:09.540
here or inside here yourself does
00:04:11.819
doesn't even know what location it is it
00:04:14.519
just knows what it can do and then when
00:04:17.220
you call like a method on it it just
00:04:19.738
runs something on the location without
00:04:22.560
even knowing what the location is and
00:04:24.900
then the location handles that so this
00:04:27.600
means for all theoretical purposes you
00:04:29.820
should be able to completely pull out
00:04:32.220
put something else inside yourself so we
00:04:35.580
have you know living room we have
00:04:36.840
outside it's so your bathroom or
00:04:39.720
whatever and
00:04:41.340
I'm obviously not gonna well in the
00:04:43.860
details here but you get the you get the
00:04:45.419
idea you know so that outside should not
00:04:47.759
know anything about what goes on here it
00:04:50.880
shouldn't even know if there are others
00:04:53.100
like it so for all intents and purposes
00:04:55.680
all of these units can be reasoned about
00:04:58.740
on their own you can almost think about
00:05:00.660
those web components we created or even
00:05:03.060
if you go on
00:05:05.060
webcomponents.org so let's for example
00:05:07.560
look at a carousel web component so here
00:05:12.479
there's an action so you should be able
00:05:14.820
to pop this into your code and it
00:05:16.500
doesn't need to know anything about
00:05:19.020
whether there is anything else on the
00:05:21.360
page or what's next to it or above it or
00:05:24.240
so forth let's look at the HTML so you
00:05:26.639
can just pop it in like smart Carousel
00:05:28.620
like that and maybe feed it some images
00:05:30.900
and so forth but it shouldn't make
00:05:33.360
decisions it shouldn't do anything based
00:05:36.419
on anything around it or outside it it
00:05:39.180
doesn't know anything about the context
00:05:41.400
around it okay so now that is
00:05:43.740
essentially oop very broadly speaking
00:05:46.680
obviously there's a lot more Nuance to
00:05:48.479
it and this is why I didn't just cover
00:05:52.500
it in this way why we spent maybe four
00:05:54.600
or five videos on it unpacking all the
00:05:57.060
Nuance so we can say procedural
00:05:58.860
programming
00:06:00.139
treats your main abstraction as nestable
00:06:03.660
instructions oop treats your primary
00:06:07.860
abstraction as you know so the O in
00:06:10.320
object so the O in oop objects are
00:06:13.440
objects are your primary instruction
00:06:15.440
functional programming obviously no
00:06:18.479
surprise here treats functions as your
00:06:21.539
primary abstraction you might say okay
00:06:23.639
so how is this different from procedural
00:06:26.940
programming the key here being that
00:06:31.080
functional programming says side effects
00:06:34.319
are not allowed it says the thing that
00:06:38.280
really makes code unmanageable is side
00:06:42.180
effects side effects obviously this is
00:06:45.300
almost entirely built on side effects
00:06:47.360
oop also relies on side effects so in
00:06:50.699
other words when you call interact
00:06:52.800
interact it does things outside of
00:06:55.919
itself so you know for example here or
00:06:58.979
for example here or even within itself
00:07:01.380
it maybe changes the data functional
00:07:03.720
programming says that side effects are
00:07:06.240
not allowed a function cannot change
00:07:09.419
anything outside of itself and so this
00:07:11.940
sounds insane like how do you actually
00:07:14.220
do anything meaningful okay so there's
00:07:16.440
there's two things here this is a common
00:07:18.139
misconception about functional
00:07:20.400
programming and like I also fell into
00:07:22.620
that trap now by saying it doesn't allow
00:07:25.199
side effects functional code doesn't
00:07:28.380
allow side effects but functional
00:07:30.479
programming says you should try and make
00:07:33.240
as much of your code functional as you
00:07:35.880
actually can so that means that you
00:07:38.520
should have the bulk of your code here
00:07:40.199
which has no side effects and then you
00:07:43.860
have this little bit over here that are
00:07:46.680
actually where you have your side
00:07:48.240
effects so the the majority of your code
00:07:50.759
should not have side effects why would
00:07:53.520
you want to do that and so in the
00:07:55.740
upcoming videos we're going to unpack a
00:07:57.300
bit more about what are the benefits of
00:07:59.460
having as little side effects as
00:08:01.740
possible functional programming and oops
00:08:04.860
share a lot in common this is the one
00:08:07.680
area where they differ and the one area
00:08:09.539
where they are mutual exclusives because
00:08:12.720
oop requires side effects you you can't
00:08:16.199
do anything in oop if you don't have
00:08:18.900
side effects so let me show that example
00:08:21.300
with a let's just go full on and let's
00:08:23.460
build our tally up with a with a class
00:08:25.319
so let's just say class and it's a soup
00:08:28.259
counter okay an encounter is value and
00:08:31.860
it starts as one and then this increase
00:08:34.099
and decrease and then there is log so we
00:08:38.700
did those Setters and Getters and all of
00:08:40.620
that last time I'm just gonna keep all
00:08:42.539
of this public just because I want to
00:08:44.159
show the principle so we can say this
00:08:45.959
dot Value Plus One this dot value minus
00:08:50.880
one okay and log is just cancel log this
00:08:54.540
dot value all right so how would we
00:08:57.180
interact with this so we would go let's
00:08:59.760
create an instance and let's say new so
00:09:03.300
what we can do is we can do instance
00:09:05.220
increase instance decrease and instance
00:09:10.440
log all right so where are our side
00:09:13.560
effects over here so increase is a side
00:09:16.860
effect because it actually influences
00:09:19.860
something outside of it so when we call
00:09:22.740
it it actually changes this thing the
00:09:25.080
same with decrease both of these have
00:09:27.120
side effects so they change that value
00:09:29.339
log has two side effects not only does
00:09:32.459
it rely on something out like itself but
00:09:35.700
it actually targets something outside
00:09:38.279
itself so it actually like even targets
00:09:40.440
the browser and this is where this
00:09:42.120
notion that the problem with
00:09:44.339
object-orientated languages is that
00:09:46.500
you've got all this implicit environment
00:09:48.360
so he jokes and he says you wanted a
00:09:50.339
banana but what you got was a gorilla
00:09:52.500
holding the banana and the entire jungle
00:09:55.140
so this is obviously a very basic
00:09:56.700
example so it might not seem like a big
00:09:58.620
a big problem here but let's say you
00:10:01.800
just want one of these you need to pull
00:10:03.779
in all of this logic okay that's fine
00:10:06.720
you might be like okay
00:10:08.339
um it's going to be result in a bit of a
00:10:10.260
bigger file size and that should not be
00:10:12.980
underestimated let me show you an
00:10:15.660
example so
00:10:17.220
um for a very long time people use this
00:10:19.740
Library called moment.js to handle
00:10:23.240
time-based information in JavaScript and
00:10:26.100
it is it's a great library and like
00:10:29.160
pretty old now very much kind of the
00:10:32.160
same era as jQuery but you'll see even
00:10:35.100
up here they say consider using moment
00:10:37.620
they may be better Alternatives so even
00:10:40.440
moment JS recommends that you don't
00:10:43.019
don't use a moment anymore and one of
00:10:46.200
the recommended ones date FNS this is
00:10:48.420
the one that I actually use and I'll
00:10:50.339
show you the difference in a second so
00:10:52.820
effectively dead F and S is a completely
00:10:56.100
functional Library so it's a it's a
00:10:58.440
library that's written with functional
00:11:01.200
programming principles and and we spoke
00:11:03.060
in the previous video about libraries
00:11:04.620
libraries or these third-party things
00:11:06.420
that you can actually enter your code to
00:11:09.720
like extend your code and to help so it
00:11:12.060
allows you to give things like oh you
00:11:13.680
want to take a date and you want to
00:11:15.000
subtract three days or you want to
00:11:17.220
format a date in a very specific way it
00:11:19.320
even has an entire section here on using
00:11:22.019
composition and functional programming
00:11:24.060
with date FNS whereas for example with
00:11:28.019
moment the way you use moment you'll see
00:11:31.260
here's like Getters and Setters and
00:11:32.940
stuff is that you instantiate this
00:11:35.640
moment object and everything is inside
00:11:38.820
that moment so let's say you just want
00:11:41.040
to convert the date from second 30
00:11:43.320
minutes whatever you need to pull in
00:11:45.480
this entire Library just to do that
00:11:48.300
because it's so reliant on side effects
00:11:50.700
you can't just pull in something out
00:11:53.399
without everything else around it
00:11:55.740
there's a couple of well-known
00:11:57.240
screenshots of actual projects out there
00:12:00.300
that use moment J is where they actually
00:12:02.760
show how much of the code is actually
00:12:06.680
moment.js let's have a look here at an
00:12:09.959
actual angular project that uses
00:12:11.820
moment.js and you can see so this is how
00:12:15.660
like all the code is split up this is
00:12:18.180
done by a webpack bundle analyzer so
00:12:21.420
this is actually something you can run
00:12:22.680
on your code base that actually shows
00:12:24.660
you how it like splits up your code base
00:12:27.240
to show you know what accounts for what
00:12:29.880
oh this blue part over here is all the
00:12:32.220
polyfills honestly I think they're maybe
00:12:34.500
adding too many polyfolds because
00:12:36.540
they're polyfilling all the way down to
00:12:39.240
es2015 it depends on what type of
00:12:41.700
project you're building so the in this
00:12:43.680
brown tan color over here this is the
00:12:46.440
actual code itself so the project itself
00:12:48.839
and then this entire section over here
00:12:51.540
is moment there is this is insane this
00:12:55.139
is my massive it's almost it's almost
00:12:57.600
the size of a third of the entire code
00:12:59.760
base and for all you know they might
00:13:02.220
just be actually converting a date from
00:13:05.339
something like seconds to hours or
00:13:07.260
whatever but now they need all this
00:13:09.660
other logic along for the ride so
00:13:12.300
there's definitely a case to be made
00:13:14.399
that oop generally results in actual
00:13:18.959
bigger file sizes and more code
00:13:21.860
especially when it comes to third-party
00:13:24.300
libraries because you need to pull in
00:13:26.279
everything because you don't know what
00:13:28.800
side effects are going to be required we
00:13:30.540
can't just let's say we want the
00:13:32.639
decrease functionality we can't just
00:13:35.459
pull out the decreased functionality and
00:13:37.620
only use that then another thing is
00:13:40.200
testing this is very hard to test
00:13:42.480
compared to functional programming so
00:13:45.120
before we go ahead let me show you how
00:13:47.160
you would do this in functional
00:13:48.720
programming I did mention that you you
00:13:51.120
need side effects somewhere you want to
00:13:53.579
use as little side effects as possible
00:13:55.920
and you also want to keep all your side
00:13:57.899
effects together in a single place it's
00:14:00.720
impossible to not have side effects
00:14:02.339
because at the end of the day your code
00:14:04.019
should change something but you don't
00:14:06.600
want those side effects spread out all
00:14:08.579
over your entire system
00:14:10.260
so what we would do is we would maybe
00:14:12.360
just do const State and State just has
00:14:16.079
value and this is the extent of our side
00:14:18.240
effects all our side effects happen here
00:14:20.639
so all our side effects happen here and
00:14:22.380
we also split out our behavior and our
00:14:24.540
and our data so all our data is here as
00:14:27.060
well and your side effects are usually
00:14:28.800
where your data resides but the behavior
00:14:31.980
itself doesn't have side effects we
00:14:34.200
would create an increase function and we
00:14:36.839
would create a decrease function we
00:14:39.120
would create a log function so increase
00:14:42.000
takes State and it returns a new state
00:14:44.820
okay so what we would do is we would
00:14:47.760
return the current state and we would
00:14:49.980
just destructure to create a new object
00:14:52.800
so we create a new blank object and we
00:14:55.079
take everything from this state and we
00:14:56.820
Destructor it into this you can even do
00:14:59.639
if you want object assign and just an
00:15:03.120
empty object and then combine it with
00:15:05.880
state to create a new object or what you
00:15:08.459
can also do is you can just Go full on
00:15:11.339
you know result new object and then go
00:15:14.639
result value equals State Value Plus one
00:15:19.380
and then just return the result so the
00:15:21.600
key being that every time you need to
00:15:24.360
create a new object you can't modify the
00:15:27.839
existing one because then you're
00:15:29.399
creating a side effect so it takes
00:15:31.380
something and it splits something new
00:15:32.760
out okay but the easiest way is just to
00:15:36.000
destructure it directly in here and then
00:15:38.880
we just say so we destructured and then
00:15:40.920
we override value after the D structure
00:15:43.740
and we just say that is State Value Plus
00:15:46.560
one and then we do the exact same for
00:15:48.720
decrease and it just minuses it and then
00:15:51.660
log takes the state and it also takes a
00:15:54.600
callback we just pass State value to the
00:15:58.560
Callback so none of these have side
00:16:00.480
effects so what this means is we can
00:16:02.940
actually pull any of these out and use
00:16:05.399
it on any state so that means whereas
00:16:07.680
over here if we want three different
00:16:09.240
counters we we need to instantiate all
00:16:12.300
of this Behavior three times you know so
00:16:14.579
we have for example temperature humidity
00:16:17.279
and let's just say wind or whatever so
00:16:20.459
you bring all this Behavior along each
00:16:22.380
time over here let's just actually put
00:16:25.260
those as three things in our actual
00:16:28.019
state so we have these functions and
00:16:30.540
then if we want to do something like
00:16:31.740
this we can add something that is a lens
00:16:33.720
and we would actually even use a lens
00:16:35.820
for this I would actually not do it this
00:16:38.279
way so I would actually let's just say
00:16:40.380
get so get is an actual function and so
00:16:43.079
you just pass State and you say what you
00:16:45.240
want to get here so this is something
00:16:47.399
called the lens so you use this instead
00:16:50.759
of Getters and Setters in functional
00:16:52.500
programming and then you just return so
00:16:54.839
then what we can do is if we up here let
00:16:57.240
me just move this to the side in our
00:16:59.399
state we have wind which you know has
00:17:02.639
value and we have temperature which has
00:17:05.939
value one and we have humidity which has
00:17:10.380
value one okay so then if we want to
00:17:13.619
modify this so here's our data here is
00:17:16.919
our behavior and then let's just put our
00:17:19.380
logic down here over here we have our
00:17:22.500
data and our Behavior together and then
00:17:24.959
we have a logic just a split between our
00:17:27.299
data and behavior and then the logic
00:17:30.840
down here here we actually have three
00:17:32.660
splits so let's actually then put our
00:17:35.460
logic down here so so before we get to
00:17:38.700
our functional code Behavior it's also
00:17:41.340
important to talk about probably one of
00:17:43.620
the most common patterns that you find
00:17:45.840
in functional programming within
00:17:48.120
JavaScript is this idea of a store
00:17:50.700
because as you can imagine here and the
00:17:53.580
benefit that we get with this separation
00:17:55.559
here is that because our our state is no
00:17:59.940
longer co-located with our actual
00:18:02.220
Behavior the benefit is that we can keep
00:18:04.620
all of our data together in a single
00:18:06.840
place so you can see the entirety of the
00:18:09.780
App State in a single place compared to
00:18:13.020
here where we actually have the state of
00:18:15.179
the app split across three different
00:18:17.640
entities so what I'm gonna do in this
00:18:20.400
video is I'm going to add some of those
00:18:22.500
shoelace components to my to-do app and
00:18:25.440
then I'm going to show how we can
00:18:27.660
actually save the tasks in the to do app
00:18:30.480
so if you close your browse and you open
00:18:32.160
it again how you can get the same tasks
00:18:34.679
again and we're going to be doing that
00:18:36.780
through functional programming through
00:18:38.640
kind of the store pattern and we're
00:18:40.260
going to use something called middleware
00:18:42.240
to do that and then I'm going to show
00:18:44.400
why it would be really really hard to do
00:18:46.860
something like that and to actually save
00:18:49.679
our data locally if we're exclusively
00:18:52.260
just using an oop approach alone and
00:18:55.679
this is one of the areas in JavaScript
00:18:57.360
where something like oop and functional
00:18:59.760
programming play really nicely together
00:19:01.740
so we control our objects we control our
00:19:05.460
elements through oop by creating web
00:19:08.760
components because that is the mod model
00:19:10.799
that HTML elements follow under the hood
00:19:13.620
they are actually just objects a lot of
00:19:16.200
the high level logic we can actually
00:19:18.299
control through functional programming
00:19:20.820
principles because I do and I find that
00:19:22.679
functional programming is really useful
00:19:25.620
when you are actually handling something
00:19:28.679
as interactive as the entire App State
00:19:31.980
specifically when changes to that state
00:19:34.460
happens as actual side effects so by
00:19:37.919
means of button clicks or you hitting a
00:19:40.679
server and getting something back from a
00:19:42.299
server and that is for these reasons
00:19:43.919
that most asynchronous things in
00:19:47.160
JavaScript are actually handled in a
00:19:50.640
functional programming way I'm going to
00:19:52.260
show you super quickly once we get to
00:19:55.020
promises and the fetch API at the very
00:19:57.960
end of the JavaScript stuff that we're
00:20:00.179
covering and we're really going to go
00:20:02.220
into this and and this functional
00:20:03.960
programming idea of a monad but I'm just
00:20:06.419
going to show you very quickly so let's
00:20:08.760
say we want to get something from
00:20:10.440
google.com we would go fetch and we
00:20:14.400
would say where https
00:20:16.460
google.com and let's just say slash user
00:20:20.280
okay so we get a user there and then we
00:20:23.700
can say all right so when that comes in
00:20:26.280
check if the API response is okay so
00:20:29.280
what we can do is we can say you know
00:20:31.740
response and we just check if response
00:20:35.880
is not okay so new error invalid
00:20:39.299
response and then the next step we say
00:20:41.760
all right and then we just return the
00:20:44.160
response again and then the next step
00:20:46.020
that we want to do is we want to turn
00:20:47.580
that response into actual Json data so
00:20:50.100
we go response response dot Json all
00:20:54.240
right and so when that is done let's get
00:20:56.820
data and let's just get DOTA dot ID okay
00:21:01.880
and then we'll just console log that
00:21:04.799
okay so you chain your behavior with
00:21:08.640
these higher order functions so at no
00:21:11.820
point is anything being saved this is
00:21:14.700
all just data that's getting piped
00:21:16.860
through functions so it does this then
00:21:18.840
it does this then it does this then it
00:21:20.640
does this and then it cancel logs the
00:21:22.200
result so nothing is getting saved
00:21:24.419
nothing is getting mutated in in the way
00:21:27.240
that if we were to have you know for
00:21:28.980
example late response and you assign
00:21:31.320
into that and then you pull and you
00:21:33.120
assign back and so forth but this is
00:21:35.700
some pretty high level functional
00:21:37.440
programming I just want to show that
00:21:39.539
JavaScript has functional programming
00:21:41.520
built into it as well in the same way
00:21:44.400
that it has you know like class built
00:21:47.700
into it so JavaScript supports both
00:21:49.919
functional programming and object or
00:21:51.780
object orientated programming but for
00:21:54.059
some things you do require to use oops
00:21:57.240
so anything with a Dom you need to do
00:21:59.520
oop anything with asynchronous functions
00:22:02.880
and so forth you need to do functional
00:22:05.700
programming so you need to understand
00:22:06.960
both but as mentioned like it's possible
00:22:09.179
that you can enjoy one more more than
00:22:11.159
the other one while still realizing that
00:22:13.620
both are required to write JavaScript
00:22:16.140
and for me personally I really like this
00:22:18.539
like there's something really cool to me
00:22:20.760
about just passing data through these
00:22:22.620
pipes and not actually saving it
00:22:24.900
anywhere and it comes out in the form
00:22:27.419
that you wanted to at the end as opposed
00:22:30.000
to something like this where we create
00:22:31.320
all these structures and whatever but so
00:22:33.600
with that out of the way
00:22:35.460
um generally you create a store and a
00:22:38.940
store handles all the side effects for
00:22:41.400
you we can say that this is the initial
00:22:43.500
state that the store starts from so
00:22:46.679
let's just do initial okay so this is
00:22:48.840
the initial state
00:22:50.100
okay and let's just create a factory
00:22:52.200
function const create store and then in
00:22:55.679
that store we just pass the initial
00:22:58.860
state to that store initial so we just
00:23:01.679
pass the initial state to that store put
00:23:04.740
it in state over here and this is the
00:23:07.140
only thing that can be mutated the state
00:23:10.020
can be replaced that is it I'll show you
00:23:12.780
another example in a minute where we can
00:23:14.940
go even further and never replace the
00:23:16.919
state and how that allows us to do
00:23:19.679
really cool things like undo and redo
00:23:21.900
and so forth okay so then we assign our
00:23:24.299
state over there and then create store
00:23:26.580
Returns the actual store itself let's
00:23:29.159
say you can pass a specific action to
00:23:31.620
the store so update okay and update this
00:23:35.640
takes a function we can even put it up
00:23:37.799
here and you can do all of this with the
00:23:39.659
class as well
00:23:41.280
um for me it's just I I enjoy I prefer
00:23:44.340
working with Factory functions
00:23:48.179
um as mentioned I find them more
00:23:49.559
idiomatic I find them nicer to work with
00:23:51.600
than classes but but this is just a
00:23:53.460
personal preference that both of them do
00:23:55.080
the same thing under the hood so you can
00:23:56.640
use either this is just what I
00:23:58.679
personally prefer one thing to to note
00:24:01.860
though is remember because classes use
00:24:05.280
prototypes
00:24:07.020
um they actually create a prototype
00:24:09.240
chain and all objects that you create
00:24:12.240
from that class fall back to that
00:24:15.179
prototype chain that you created there
00:24:17.460
are some performance benefits to that
00:24:19.320
because you're not creating a new object
00:24:22.140
every time so it uses less memory and
00:24:25.020
this is the exact reason why prototypes
00:24:27.480
were actually added to JavaScript so I
00:24:29.760
spoke quite a bit about how gross
00:24:31.860
prototypes is and how I don't like them
00:24:33.539
at all but I never actually spoke about
00:24:34.919
why they were added and when they were
00:24:37.140
added they were actually an amazing
00:24:38.640
thing because they allow us to extend
00:24:41.700
things by using very little memory and
00:24:45.059
so at the time when JavaScript was
00:24:47.340
created you know let's say 1995 this
00:24:49.679
wasn't amazing because your primary
00:24:52.140
concern at that point was memory like
00:24:54.780
the standard memory that a computer came
00:24:57.059
out with at that time was about eight
00:24:59.400
megabytes of ram let me actually see how
00:25:01.860
much RAM I have on this device over here
00:25:03.960
the the computer that I'm using right
00:25:06.360
now let's have a look I had 32 gigabytes
00:25:09.120
and that's not even a lot for modern day
00:25:11.280
computers um some go up to 64 gigabytes
00:25:14.640
there are some that go even higher eight
00:25:17.220
megabyte is about 2.4 percent of what I
00:25:20.700
have
00:25:21.659
um if you have even more than your then
00:25:23.400
you're kind of approaching the one
00:25:24.600
percentage number and it's probably
00:25:26.039
going to go bigger and bigger so this
00:25:28.080
was a time when memory was when memory
00:25:30.600
usage was a huge issue and you know like
00:25:33.240
now we have a lot more memory available
00:25:35.600
this doesn't necessarily mean that
00:25:37.740
memory is not an issue you know memory
00:25:40.679
is still an issue let me even in my task
00:25:43.140
manager let's see how much memory my
00:25:45.600
computer is using right now so if we
00:25:47.760
have a look here and we look at my
00:25:49.260
computer even with all that memory right
00:25:51.960
now I'm using about fifty percent of it
00:25:54.059
okay so memory is still an issue at the
00:25:56.700
scope that we're working at now whether
00:25:59.640
something is uses the Prototype or
00:26:03.000
creates a new object the difference in
00:26:05.820
memory is like a little blip on this
00:26:07.980
radio you if you would be able to see it
00:26:10.140
at all so there is something to be said
00:26:12.720
about memory optimization I generally
00:26:15.240
don't think whether you're using the
00:26:17.820
Prototype or creating your own objects
00:26:19.919
maybe in the top thousand of things you
00:26:23.760
need to talk about when you talk about
00:26:25.080
how to use memory more efficient in your
00:26:27.299
app the only caveat being when you have
00:26:30.059
an app that is doing a million and
00:26:33.240
million calculations per second so you
00:26:36.539
are writing maybe drivers for a database
00:26:39.020
or you are building something like figma
00:26:41.940
itself which we're using over here then
00:26:44.640
you really want to maybe squeeze out
00:26:48.000
that little bit of performance you can
00:26:49.919
it because you know even something that
00:26:52.500
is a super small blip if you perform it
00:26:55.140
a million times a second you know so
00:26:57.299
let's say you're creating a million
00:26:58.919
stores per second that's a different
00:27:00.419
story but the top of apps that we
00:27:02.820
generally build that's a non-issue and
00:27:04.860
I've actually never encountered and
00:27:06.480
encountered an instance where I'm
00:27:08.340
working on something at that scale where
00:27:10.860
I need to squeeze out that little bit of
00:27:13.200
granular memory usage if anything the
00:27:16.080
thing that slows our apps down nowadays
00:27:18.179
is computational Cycles which ironically
00:27:21.120
has more to do with the Dom and we're
00:27:23.760
going to talk about when we talk about
00:27:25.140
Frameworks we're going to talk about
00:27:26.100
this idea of a virtual Dom and the idea
00:27:28.500
of a virtual Dom actually says that the
00:27:31.380
performance problems we have today is
00:27:33.179
related to computational Cycles
00:27:35.240
therefore we're putting more stuff in
00:27:38.400
memory to save computational Cycles this
00:27:41.880
is just to actually show like how of a
00:27:44.700
non-issue this type of memory this this
00:27:47.460
little bit of memory that you save is in
00:27:50.279
the big scope of things I just wanted to
00:27:52.080
bring that up in case you ever come
00:27:53.700
across someone who's like over classes
00:27:55.440
or way faster and and this is the case
00:27:57.779
for any type of Micro optimization
00:27:59.760
whether it be like the type of of Loops
00:28:02.520
you use or whether you're using VAR and
00:28:05.039
constant all of those things and you
00:28:07.260
know this brings us also back
00:28:09.179
that can back Axiom of make it work make
00:28:13.799
it right and any only then make it fast
00:28:16.559
because a lot of times like these are
00:28:19.740
actually competing concerns and making
00:28:23.220
it fast should always be the last
00:28:25.500
concern it's a lot easier to make
00:28:29.039
something fast once it has it is
00:28:32.400
actually working and also once it is in
00:28:35.400
a readable manner like I said a lot of
00:28:37.799
people actually say make it pretty which
00:28:40.320
talks about like how the actual code is
00:28:42.360
structured so it's pretty trivial to
00:28:44.400
convert this to a class if we do decide
00:28:47.159
to do that and if it actually becomes a
00:28:48.840
problem but you might just go I actually
00:28:51.419
like classes more than this I prefer
00:28:53.220
working with classes which 100 go for it
00:28:55.980
I actually I actually prefer working
00:28:59.159
with Factory functions that's at end of
00:29:01.200
the day all right so update so what does
00:29:03.659
update future update takes an action and
00:29:06.299
that action is a function so we can
00:29:08.520
actually just check ensure that type of
00:29:11.520
action equals function so if it doesn't
00:29:15.179
then throw error action is required to
00:29:19.740
be function so let's actually create a
00:29:21.840
quick interface for our store so let's
00:29:24.059
do it up here and remember I write my
00:29:27.299
types as
00:29:29.480
Pascal case so let's do type Dev store
00:29:33.179
object
00:29:34.740
store okay and that store has a couple
00:29:38.580
of props okay so the first one at the
00:29:41.760
moment it just has update and update we
00:29:45.360
can just specify up here and that is all
00:29:47.760
it has for now so let's do callback yeah
00:29:51.240
and the Callback is update and what does
00:29:54.059
update accept it actually accepts
00:29:56.039
another callback and here you'll see
00:29:58.380
where we're using parametric
00:29:59.700
polymorphism and then parametric
00:30:01.799
polymorphism is a key part of functional
00:30:05.279
programming and you will see like as I
00:30:08.700
mentioned you know sometimes it gets a
00:30:10.440
bit hard to get a grasp on what exactly
00:30:13.679
is happening and and the reason for that
00:30:16.140
is not because functional programming is
00:30:18.840
complex functional programming is
00:30:21.299
actually I find a lot more simpler but
00:30:24.059
understanding the concepts of functional
00:30:26.520
programming is harder because they don't
00:30:28.919
reflect anything that we experience in
00:30:32.100
the real world so I spoke about those
00:30:33.840
Russian Esther dolls I spoke about the
00:30:36.480
tree with the branches you know like
00:30:38.159
those are metaphors but like they don't
00:30:41.220
actually think itself fully okay so just
00:30:44.159
be mindful that when you're like I'm not
00:30:46.320
following anymore I don't know what's
00:30:48.120
going on maybe stop go back a bit
00:30:50.279
re-watch it again
00:30:51.659
um the point being is it should be hard
00:30:53.580
to understand it but once you understand
00:30:54.960
that like it's actually going to be much
00:30:56.580
easier to understand the code once you
00:30:58.559
understand the principle okay so in here
00:31:00.960
we actually pass action right and let's
00:31:03.840
just declare action up here and that's
00:31:06.059
also a callback and action and all that
00:31:09.720
that does is it takes a param and it
00:31:13.140
returns a new state so let me put all of
00:31:15.840
this for us in vs code so we can
00:31:18.179
actually get this Auto completion and
00:31:19.860
and so forth so let me just spin up a
00:31:23.159
completely new project and just to
00:31:26.399
illustrate the principle before we start
00:31:28.140
applying it to our to do app okay so let
00:31:32.460
me just pull that in and let me just add
00:31:35.159
my
00:31:36.500
scripts.js here and let's actually just
00:31:39.240
create a store.js I usually encapsulate
00:31:43.080
it in a store file as well and then I
00:31:45.899
kind of use the built-in export and
00:31:47.880
import aspects of modules in JavaScript
00:31:50.760
to actually manage this instead of
00:31:52.380
actually having a store Creator so let's
00:31:54.720
just grab everything we have up until
00:31:57.059
now and Pull It in so here is our
00:32:00.000
initial store here is the actual
00:32:03.140
functions and the actual store itself
00:32:07.080
but you remember I'm saying that this
00:32:10.380
actually shouldn't be encapsulated with
00:32:13.500
the data so let's actually you just do
00:32:15.840
you know actions dot JS so these are
00:32:18.720
actual actions that you can pass okay
00:32:21.840
and so let's move all this Js Js dock up
00:32:25.260
here to the top and let's also just
00:32:28.200
create the shape of our store up here as
00:32:31.080
well we can go and because this is a
00:32:34.620
pretty common pattern actually create a
00:32:36.360
type definition for this and let's just
00:32:38.820
call it and for now item just has a prop
00:32:41.460
which is value and that is a number all
00:32:44.340
right so then let's just create our
00:32:46.860
state so type def object State items on
00:32:50.760
there humidity temperature and wind all
00:32:53.159
right so this takes us this state it
00:32:55.260
returns a new State uh update there we
00:32:58.380
go and this should be prop and we're
00:33:00.539
gonna need two other
00:33:02.580
um props as well and this is where I
00:33:04.620
said it's useful to actually understand
00:33:06.980
design patterns even if I said you
00:33:10.320
shouldn't Implement them directly as is
00:33:12.720
in your code because we're going to be
00:33:14.700
drawing inspiration here from a specific
00:33:16.799
design pattern which is the Observer
00:33:18.659
pattern but the key here being
00:33:20.840
inspiration so effectively what our
00:33:23.640
store is going to do is things can
00:33:26.760
listen to the store the store will let
00:33:29.460
it know when the store itself changes
00:33:31.980
and they can respond accordingly and you
00:33:35.159
can effectively think about this you
00:33:37.080
know almost like a newsletter so if you
00:33:39.419
subscribe to your newsletter so you
00:33:41.820
effectively subscribe to the store from
00:33:44.460
somewhere in your code and when the
00:33:46.620
store changes you get sent in an alert
00:33:49.260
that the store has changed and this is
00:33:51.360
the new state of the store and that is
00:33:53.519
how you handle your side effects in a
00:33:55.980
lot of JavaScript projects so most
00:33:58.320
Frameworks have something that kind of
00:34:00.960
provides this type of behavior the big
00:34:03.600
one the original one is Redux which was
00:34:07.500
created for react but you can use it in
00:34:10.020
anything we might even pull Redux in and
00:34:12.540
then there is one full view which is
00:34:15.739
and then spelled actually has a built-in
00:34:20.159
way to actually create stores and so
00:34:23.280
you'll see here it shows how you can
00:34:24.599
subscribe and so forth and it actually
00:34:26.280
uses the this counter example that we
00:34:30.119
built initially so what we then need is
00:34:33.179
we need a way to to subscribe so when
00:34:36.960
update is run we get notified and so
00:34:39.780
let's quickly create that subscribe and
00:34:42.480
this is also why this works really
00:34:44.940
nicely with functional programming is
00:34:46.918
because you actually don't mutate the
00:34:50.580
store directly so you keep a copy of the
00:34:53.520
old store so that means that you can
00:34:56.280
provide both the previous and the next
00:34:58.320
store on a subscription event so
00:35:01.380
wherever you're listening for it you can
00:35:03.300
compare the actual changes okay so let's
00:35:05.640
just quickly finish this also throw a
00:35:07.859
new error what are we missing here const
00:35:10.140
update run your error and we need to
00:35:12.240
close that okay also what we're going to
00:35:14.700
do is let's actually make our state
00:35:16.859
States and it is actually an array so
00:35:20.099
let's just while we're at it assign that
00:35:21.780
so we can go to type and array state so
00:35:25.260
it's an array of states and the first
00:35:27.240
one that gets added is initial and then
00:35:29.579
we just push on top of this every time
00:35:31.560
and let us do cons
00:35:35.000
subscribe as well let's just do that and
00:35:37.800
so what we're going to do we're going to
00:35:39.060
return update and we're going to return
00:35:41.099
subscribe okay and let's just say what
00:35:43.980
this is going to do for us we actually
00:35:46.079
don't need this I actually said we can
00:35:48.119
actually get rid of this because we are
00:35:51.660
just using the export functionality of
00:35:53.940
the module itself so we can actually
00:35:56.280
just export const update and Export
00:35:59.640
these as two different things so States
00:36:02.460
or else update so what we're going to do
00:36:05.460
is we're going to get the previous state
00:36:07.980
so there we go effectively it just looks
00:36:10.619
at the current states and it does the
00:36:13.200
length and -1 so to get the last one
00:36:15.720
that has been added what I actually
00:36:17.760
prefer to do is I'll do it the other way
00:36:19.380
around so I don't put them at the end of
00:36:23.099
the array I put the latest State
00:36:25.079
actually at the front so it pushes all
00:36:27.000
the other ones back so we check the very
00:36:29.280
first one and then we calculate the next
00:36:31.980
one and the next state effectively we
00:36:34.740
run the action on the next state and
00:36:37.560
that's going to give us the next state
00:36:38.760
and then what we do is we just take
00:36:42.180
States and we unshift in other words we
00:36:45.240
put it in the front moving everything
00:36:46.680
else next so that it puts it at the
00:36:48.839
front over there what we also want to do
00:36:51.000
it might be worth going object freeze on
00:36:54.780
both of these that just means that you
00:36:57.180
actually can't modify it prevent
00:36:59.400
accidental reassignments and so forth
00:37:01.619
and what we can also do is let's just
00:37:04.380
destructure them inside here just to
00:37:07.500
ensure that these are two completely new
00:37:10.619
arrays objects some others might be a
00:37:12.960
bit Overkill but we want to make sure
00:37:14.520
that you can't accidentally directly
00:37:16.740
mutate the store okay and then we
00:37:18.480
unshift that in so how is subscribe
00:37:21.180
going to work so in subscribe let's also
00:37:24.180
add subscribers okay so these are actual
00:37:27.359
functions that are subscribed to the
00:37:29.400
store so these functions are going to
00:37:30.960
get called let's create what this would
00:37:33.960
look like the callback for that so and
00:37:37.140
let's just say notification so this is
00:37:39.839
the notification that you get when the
00:37:42.839
actual store changes so the first param
00:37:45.780
is is next and the other one is previous
00:37:49.440
so you can get the the actual upcoming
00:37:52.320
State and you can also look at the
00:37:55.619
previous one if you want optionally
00:37:57.420
actually have any return because it is a
00:38:00.420
side effect all right so you need to
00:38:02.099
register a notification so let's
00:38:04.560
actually call this notifications it does
00:38:06.540
look a bit too closely to States so
00:38:09.720
let's just mark this up this is type
00:38:11.579
array State and this is array
00:38:16.140
notification all right and there's
00:38:18.000
currently nothing in notifications so
00:38:20.599
notification or let's call this Handler
00:38:23.460
so this handles the notification and
00:38:26.040
Handler is actually just a notification
00:38:28.380
that gets passed well it's actually the
00:38:30.720
language is actually a bit confusing
00:38:32.339
here so let's actually say no to fi to
00:38:36.000
indicate that it's a function instead
00:38:37.920
and we can just say node to buyers and
00:38:42.000
notify okay and notify there we go just
00:38:46.079
to indicate that it's a function and
00:38:48.420
what it returns way to unsubscribe if
00:38:52.680
you want to remove the subscription so
00:38:54.359
this is very similar to ad event
00:38:55.980
listeners and so subscribe Ram take
00:38:59.460
notify and notify so once again you
00:39:01.980
might be like losing track here maybe
00:39:04.800
re-watch this section A couple of times
00:39:06.599
maybe try playing around with it
00:39:08.400
yourself to get your head around it it
00:39:10.619
is quite hard to get your head around
00:39:12.720
the concept but once you understand the
00:39:14.760
concept this is actually a very
00:39:16.380
simplified way to actually do super
00:39:19.859
complex logic and this is infinitely
00:39:21.720
scalable because you can just update
00:39:23.520
your state as your app grows none of
00:39:25.500
this ever needs to change like this is
00:39:27.180
you can scale this Behavior infinitely
00:39:29.339
so notifiers so the first thing that
00:39:32.760
gets done is no dirt devise and we can
00:39:36.000
maybe push that on the end so notify
00:39:39.960
gets pushed to notifiers again and
00:39:42.960
unsubscribe function is returned this is
00:39:46.020
also very functional programming-esque
00:39:48.420
so it might be a bit hard for you to
00:39:51.540
really follow him once again because we
00:39:54.060
are actually returning a function we're
00:39:56.280
actually passing the functions around
00:39:58.079
that should do the things instead of
00:40:00.540
passing the data itself to the function
00:40:03.420
to the way that you keep your data
00:40:05.880
encapsulated and you and you prevent
00:40:07.980
data from being mutated is you actually
00:40:10.440
read the functions as the thing that
00:40:12.839
gets moved around and changed instead of
00:40:15.420
the actual data itself because at the
00:40:17.460
end of the day when we are thinking
00:40:19.859
about apps we're thinking about
00:40:21.540
interactivity so what is the core thing
00:40:23.760
in an app is actually the interactions
00:40:25.980
so it makes sense that actually the
00:40:28.500
thing that you use the most and the
00:40:30.420
actual thing that gets passed around is
00:40:32.640
actual functions and not the data if
00:40:35.339
you're doing data analysis or let's say
00:40:37.079
you have a big data set and you want to
00:40:38.640
find patterns and whatever then like it
00:40:40.619
would make sense that the thing that you
00:40:42.359
pass around is the data itself but due
00:40:44.880
to the high interactivity and all the
00:40:47.760
events that fire in most modern apps it
00:40:51.060
actually makes sense that functions are
00:40:52.740
the primary thing that you pass around
00:40:54.119
but we can explore this in the upcoming
00:40:56.040
videos in much more detail all right so