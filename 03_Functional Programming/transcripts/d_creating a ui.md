00:00:00.000
all right so now that we have this um
00:00:03.000
Thor set up here to model all our data
00:00:06.359
we probably want to start looking at
00:00:08.340
what we're actually going to be showing
00:00:09.900
on the screen and so I'm going to be
00:00:11.580
doing it a bit the other way around now
00:00:13.380
I'm going to be building the example
00:00:15.540
first and then I'm retroactively going
00:00:17.520
to explain what I did in the example
00:00:19.859
specifically with the focus on how
00:00:22.800
immutability and Purity from a
00:00:26.039
functional programming perspective
00:00:27.300
actually helped keep our code more
00:00:29.279
manageable and also how we can't get rid
00:00:33.180
of oop a hundred percent there are still
00:00:36.239
some things in our app that are handled
00:00:39.239
with an oop approach the primary one
00:00:42.059
being components you might have seen in
00:00:44.760
the previous videos that our components
00:00:46.620
started getting very unwieldy they
00:00:48.899
started getting very big a lot of code
00:00:51.120
and also a lot of repetition we wrote
00:00:54.000
the same things over and over again so
00:00:56.460
they're doing the elements attaching the
00:00:58.320
shadow Dom all of those things
00:01:00.420
so what I want to do now is I actually
00:01:02.760
want to show you how I would create an
00:01:05.099
abstraction around my components to
00:01:08.280
actually as we learned reduce some of
00:01:10.920
that noise you know hide some of that
00:01:12.720
stuff around the shadow Dom around
00:01:14.760
actually attaching event listeners all
00:01:16.920
of that stuff and bring forward the
00:01:19.860
essence so let me just create a utils
00:01:22.740
folder here and this is where I would
00:01:24.659
just put utilities so these are things
00:01:26.580
that aren't specific to a piece of the
00:01:29.520
app but there are just tools you can
00:01:31.860
think almost like a hammer or a saw and
00:01:34.619
so forth that actually help us write our
00:01:36.960
code or build our app as we go and I'm
00:01:39.600
just going to say components so this is
00:01:41.759
just where I'm going to put all my
00:01:43.079
component specific utilities and let's
00:01:46.380
create a specific Factory function and
00:01:48.659
let's call it create component there are
00:01:51.119
two approaches to this you might have
00:01:52.740
probably guessed it the other one is to
00:01:54.540
create a class and call it component and
00:01:57.479
then just extend that and then further
00:01:59.759
extend that so this is what some
00:02:02.759
libraries like actually let do let me
00:02:05.700
show you lit element so when we start
00:02:07.920
talking about JavaScript Frameworks so
00:02:10.020
the lit one which we're going to talk
00:02:12.120
about actually has something called lit
00:02:14.520
element that is actually built on top of
00:02:16.500
web components that give its own kind of
00:02:19.620
level of abstraction on top of it and
00:02:21.660
then you further extend it
00:02:23.459
I am just going to do a factory function
00:02:25.920
for now because as you know that is just
00:02:27.900
how I prefer to do it but at this point
00:02:30.840
it's mostly just an issue of personal
00:02:32.879
preference so I would just say class
00:02:35.160
component and we need to remember to
00:02:37.980
extend the HTML element and extend with
00:02:42.420
an S okay so we create our component in
00:02:44.700
the scope let us write up the interface
00:02:47.099
for this utility obviously it's going to
00:02:49.680
accept some props and let's say we want
00:02:52.739
to pass the following props to it I
00:02:55.140
think first and foremost the name so the
00:02:56.879
element itself and let's add this as
00:03:00.000
we're writing the documentation actually
00:03:01.700
pulling in some of the logic so param
00:03:04.800
Props and this needs to be object right
00:03:08.239
so and type Dev instead right so we're
00:03:12.599
pulling this in prompts element so while
00:03:16.140
we're at it let's actually check if the
00:03:18.120
element has a dash in it remember custom
00:03:21.840
components need a Dash or a hyphen in it
00:03:24.900
and we can just say if it doesn't throw
00:03:27.420
new error and let me enable copilot
00:03:29.700
again it sometimes helps me write errors
00:03:32.040
a bit quicker because it can look at the
00:03:33.959
code and then actually make a
00:03:35.340
recommendation in terms of what the
00:03:36.659
error message should be yeah element
00:03:38.280
name is include a hyphen there you go
00:03:39.900
all right so by this point we're going
00:03:41.459
to assume it has a hyphen and so we
00:03:43.500
create the class what we do is we custom
00:03:46.760
elements Define element the name and the
00:03:51.420
component and then let's just return the
00:03:53.459
component uh if you want to use the
00:03:56.280
class to kind of check whether it's an
00:03:58.379
instance of this component or so forth
00:04:00.659
so in here it's actually smart enough to
00:04:03.840
start writing this for us so obviously
00:04:06.000
we have a Constructor with a super in it
00:04:07.799
as I mentioned all that super does it
00:04:09.720
calls the Constructor on the thing we're
00:04:12.180
extending we can even pass things to it
00:04:14.519
if it accepts things so we can pause it
00:04:16.320
like that it doesn't accept anything
00:04:18.858
mode it's just closed and not open so
00:04:22.440
the other thing is just I put prefer to
00:04:24.120
put my actual Shadow Dom inner component
00:04:26.639
here so let's just do it that way and
00:04:29.639
then inner and a pen child node let's
00:04:35.280
say the next thing that this accepts is
00:04:37.320
the actual template it's a string and so
00:04:40.080
let's create it up here before we
00:04:41.520
actually declare our components a
00:04:43.020
template document create element
00:04:44.460
template templates in a HTML props
00:04:48.720
template and let me just call this
00:04:51.360
template string and then over here when
00:04:55.020
we destructure it we just rename it to
00:04:57.479
template string all right so we assign
00:04:59.759
that and then over here we just create
00:05:02.400
the node template content clone node yes
00:05:05.820
this is correct all right but so now we
00:05:07.860
probably want to pass some other things
00:05:09.060
as well and let's say we probably want
00:05:12.000
to pass events so what events do we want
00:05:15.600
to listen for and let's say this is a
00:05:17.580
record of string which would be the
00:05:19.440
names of the events so these will attach
00:05:21.720
event listeners for us let's just create
00:05:24.360
something called the Handler and that
00:05:26.699
would be a callback and let's create it
00:05:28.919
up here so callback and Handler and all
00:05:32.940
that that does it just has a param event
00:05:35.580
so it can be an event or a custom event
00:05:38.100
one of these two we won't know which it
00:05:40.979
is and then the last thing we want to do
00:05:43.199
is maybe actually do something called
00:05:46.620
connect and so I'm just using the Redux
00:05:49.320
terminology here so you can look for
00:05:51.720
Redux connect a way to connect
00:05:55.620
components to your store so that is just
00:05:57.780
the word they use I'm just going to
00:05:59.100
stick with that and what connect does it
00:06:02.160
effectively is just creates a subscriber
00:06:05.639
for a store and attaches it to the
00:06:08.280
component so let us pull that in so if
00:06:11.280
we go model store JS we're going to pull
00:06:14.940
And subscribe all right so but what we
00:06:18.360
also want is State because connect is a
00:06:22.080
callback and it just has two params
00:06:25.680
previous and next and both of these are
00:06:28.440
just instances of the of the state
00:06:31.340
state and so connect and I think that is
00:06:35.639
it we might need to add some other
00:06:37.560
things but I think for now this is good
00:06:39.360
enough abstraction to get working
00:06:40.680
effectively it's also worth noting that
00:06:42.960
what we're doing here is we are actually
00:06:44.940
creating our own JavaScript framework
00:06:46.979
now from the ground up what we are doing
00:06:49.319
here is we're actually we're actually
00:06:51.720
hiding the noise of the low low level
00:06:53.940
noise associated with updating the UI
00:06:57.000
keeping the UI in sync with our state
00:06:59.039
and so forth and we're elevating the
00:07:01.440
essence and you know so the essence is
00:07:03.780
you know what is the template what how
00:07:06.060
should the stand in relation to the
00:07:07.680
store and then we're getting rid of all
00:07:09.360
this you know attached to
00:07:11.600
cloning the node all of that stuff and
00:07:14.400
so forth so we are effectively creating
00:07:16.620
our own JavaScript framework here I
00:07:18.780
would actually encourage you guys to try
00:07:21.000
and create your own libraries your own
00:07:22.620
Frameworks let's see up front no one's
00:07:24.780
going to use it I mean like if you look
00:07:26.400
at react and like all those big
00:07:28.440
Frameworks have really smart people
00:07:30.240
behind them they have the entire
00:07:31.560
Facebook team behind them
00:07:33.780
um angular has the entire Google team
00:07:35.699
behind it and what reactors now like I
00:07:38.580
think older than 10 years already so you
00:07:41.699
know you obviously won't be able to
00:07:42.840
compete with that life cycle in terms of
00:07:46.259
maturity that that framework has and
00:07:48.479
also just like I don't really care how
00:07:50.220
smart you are you are not as smart as
00:07:52.020
the entire Facebook in engineering team
00:07:54.120
combined and the reality is whatever
00:07:55.740
you're going to come up with is going to
00:07:57.240
be worse than any of the existing
00:07:58.740
Frameworks I would always just like use
00:08:01.259
those Frameworks they're much more
00:08:02.580
stable there is a lot of value in
00:08:04.680
creating your own framework and playing
00:08:06.240
around with it yourself
00:08:08.580
um just as an experiment I think it
00:08:11.220
helps you understand kind of what these
00:08:13.620
Frameworks do much better and how to
00:08:15.720
make sense of Frameworks and also it's
00:08:17.699
it's just a phenomenal exercise in terms
00:08:19.919
of practicing JavaScript getting better
00:08:22.199
at JavaScript and also abstraction it's
00:08:24.419
a phenomenal exercise in terms of
00:08:26.520
getting better at creating abstractions
00:08:28.680
because a JavaScript framework is like
00:08:31.020
one of the Cornerstone abstractions
00:08:33.240
because at the end of the day you are
00:08:35.279
rendering things on the screen and
00:08:37.620
you're changing what gets shown on the
00:08:39.539
screen based on certain things that is
00:08:42.299
like the most important abstraction that
00:08:44.459
any app can have which is also one of
00:08:46.800
the reasons why people have so many
00:08:48.899
fights around Frameworks and this
00:08:50.399
framework is the best that framework's
00:08:51.899
the best you should use frame actually
00:08:53.519
shouldn't have used Frameworks because
00:08:55.019
that is such an important thing but for
00:08:56.880
now let's just continue with our own
00:08:58.260
little framework here and it actually
00:09:00.000
does very little but like it kind of
00:09:02.580
first and foremost it's going to make
00:09:04.440
our life just a bit easier not having to
00:09:06.779
do all of this stuff
00:09:08.519
um only being able to kind of set the
00:09:11.040
important stuff and it's also just a
00:09:12.959
really good exercise in terms of as a
00:09:15.360
stepping stone towards Frameworks
00:09:18.180
um and we're going to start talking
00:09:19.200
about Frameworks pretty soon all right
00:09:21.420
so let's continue with this so there's
00:09:23.519
two things that can be passed here
00:09:24.899
events and connect so effectively what
00:09:29.880
we want to do whoa where did all this
00:09:32.580
stuff come from okay sometimes you need
00:09:34.800
to sometimes you need to watch out for
00:09:37.080
co-pilot it sometimes stuff like that
00:09:39.600
and you're like wait wait this code come
00:09:41.339
from sometimes it tries to be a bit too
00:09:43.560
helpful
00:09:44.519
it's not actually what you want it's
00:09:46.620
actually adding code that doesn't make
00:09:48.300
sense so I'll keep it on now for a while
00:09:50.820
and let's see if it gets annoying I'll
00:09:53.459
turn it off obviously co-pilot is also
00:09:55.800
much better if it's a big project that
00:09:58.200
has a lot of code in it because it can
00:09:59.640
look at all the code in the project and
00:10:02.100
based on all the other code in the
00:10:03.660
project get a sense for how you
00:10:06.060
structure things and there isn't really
00:10:07.860
much in here so it just takes these wild
00:10:10.140
guesses at the moment so if it gets
00:10:12.360
annoying I I will turn it off in here
00:10:14.760
what we want to do is and it's also
00:10:17.100
saying that let's say both of these are
00:10:20.519
optional you don't need to listen for
00:10:22.440
events and you don't need to connect to
00:10:24.420
the store but what we can say is that if
00:10:27.060
you have events what we're going to do
00:10:29.339
is let's see here's actually pretty
00:10:31.380
smart so object so we create entries
00:10:34.560
from those events we map over each of
00:10:37.500
those so this is a higher order function
00:10:39.600
I'm gonna unpack these and list all the
00:10:43.019
different types of higher order
00:10:44.040
functions
00:10:45.360
um in the next lesson you grab the key
00:10:47.519
we grab the Handler and this add event
00:10:49.680
yeah the power is actually pretty smart
00:10:51.480
here in terms of figuring out what we
00:10:53.820
want to do then we want to say but we
00:10:56.160
just need to create
00:10:57.980
unsubscribe like that and then we just
00:11:01.279
unsubscribe in there when we're done
00:11:03.660
connect okay and so we subscribe and see
00:11:07.680
this is actually not right which is
00:11:10.320
pause connect straight into it and
00:11:12.300
that's if connect exists so here's the
00:11:14.459
other thing so one thing we haven't
00:11:16.440
talked about as of yet is with web
00:11:19.980
components or any event listeners you
00:11:23.160
should remove all the listeners whether
00:11:25.680
it's listening to a subscription for a
00:11:27.420
store or it's actually listening to user
00:11:30.899
events because that's how you create
00:11:33.540
memory leaks if you remove the component
00:11:36.060
that listener is still going to be there
00:11:37.920
and it's going to keep on listening for
00:11:40.019
something that doesn't exist anymore so
00:11:42.540
that means like if you add a couple of
00:11:44.399
components remove them add some more
00:11:47.220
after a while you can have all these
00:11:49.079
listeners happening in the background
00:11:50.339
that are actually listening for things
00:11:52.019
that don't even exist anymore and
00:11:53.640
that'll give you a pretty big
00:11:55.620
performance hit with web components
00:11:57.839
there are specific cases where you don't
00:11:59.880
need to remove event listeners where
00:12:01.800
it's smart enough to know that it should
00:12:04.260
remove it
00:12:05.220
um this is mostly for ones that you put
00:12:08.399
directly on the component
00:12:10.620
uh but there are cases with like the
00:12:13.260
shadow Dom and so forth where you need
00:12:14.940
to manually do it the implications of
00:12:17.399
actually removing something that doesn't
00:12:20.100
need to be removed
00:12:21.720
um is pretty trivial it's just more code
00:12:24.420
if it would have done it automatically
00:12:26.459
uh the implications of not removing
00:12:29.579
something that actually isn't going to
00:12:31.320
get removed automatically is not that
00:12:33.660
great so I just as a lot of thumb just
00:12:35.880
remove everything even if it is overkill
00:12:38.220
but it's pretty easy to actually do so
00:12:40.920
what we can just say if there are events
00:12:42.600
so exactly the same code again we do the
00:12:45.180
exact same thing but it's smart enough
00:12:47.220
to actually know that remove event
00:12:49.260
listeners instead of adding the event
00:12:50.880
listeners and here it actually checks if
00:12:53.579
there is an unsubscribe and if it is
00:12:55.380
unsubscribe then just run unsubscribe as
00:12:58.740
well so we're as connected callback runs
00:13:02.100
when the component gets mounted in the
00:13:04.620
Dom so when you create an instance of it
00:13:07.100
disconnected callback runs when it gets
00:13:09.420
removed from the Dom that might be
00:13:11.760
because you're going to a different page
00:13:13.320
that might be because for some reason
00:13:15.120
you're actually removing it with
00:13:16.500
JavaScript so you're deleting a task or
00:13:18.899
whatever it's also important to note
00:13:21.360
that this is also something that's kind
00:13:23.760
of a common Redux pattern is Redux makes
00:13:27.060
a distinction between containers and
00:13:29.940
components containers are effectively
00:13:32.820
just components that connect to the
00:13:36.839
store regular components don't connect
00:13:39.660
to the store regular components just
00:13:41.279
take attributes or Properties or
00:13:43.079
whatever in that Addie Osmani book that
00:13:45.959
I mentioned he actually talks about it
00:13:47.579
he actually lists uh
00:13:49.680
um so I mentioned you know like kind of
00:13:51.360
he mentioned some of the traditional
00:13:53.639
patterns like a Singleton and so forth
00:13:55.980
and observer which we kind of now looked
00:13:58.620
at for the store that we built keep in
00:14:00.600
mind once again you know the the key
00:14:02.940
here is we look at them for inspiration
00:14:04.920
we don't just Implement them blindly but
00:14:08.639
he actually includes this as one of the
00:14:10.200
patterns yeah and effectively so what
00:14:12.899
this effectively just says is that you
00:14:15.240
effectively you have your containers
00:14:17.040
that are components that have data that
00:14:19.800
connect to the store and the components
00:14:22.100
these are actually just the ones that
00:14:24.600
actually render so the containers are
00:14:26.519
what connect your components to your
00:14:28.860
actual model so let's just do and I'm
00:14:31.380
just going to do TD for to do JS let's
00:14:34.139
just create a component that's going to
00:14:36.420
wrap the entire app for now and we can
00:14:39.000
just then break it up as it gets bigger
00:14:41.699
so let's pull in our create
00:14:44.779
component so utils components JS let's
00:14:50.100
bring that in create component and let's
00:14:53.040
try something really basic to just start
00:14:55.560
off with so let's do create component
00:14:58.579
props so element TD app template okay so
00:15:03.120
let's try let's just do Dev world and
00:15:06.899
let's just add this here for some syntax
00:15:09.240
highlighting and and let's not add any
00:15:12.120
events any anything let's see if it
00:15:14.399
actually renders so if we then pull it
00:15:16.440
in here pull our actual container
00:15:18.920
components in here and let's get rid of
00:15:21.300
all of this we don't need this so that
00:15:23.820
is the actual container and there is and
00:15:26.579
let's give it a go let's see and we also
00:15:29.220
need to remember to just so let's do TD
00:15:32.399
app over here and let's see maybe I'm
00:15:34.800
surprised maybe it just works hey and
00:15:37.139
there we go huh I'm actually impressed
00:15:39.480
with myself that I was able to create
00:15:40.800
that entire abstraction without any
00:15:43.220
typos or any bugs or so forth so let's
00:15:46.860
give this a test with
00:15:48.959
um some buttons or something so let's go
00:15:51.779
no button and let's say Tata key one
00:15:58.139
okay and two okay and so we have that in
00:16:01.800
our template so then let's put some
00:16:05.040
event listeners up here so let's listen
00:16:07.019
for click let's just cancel log the
00:16:10.139
event Target data set so it's gonna just
00:16:14.100
register it for all Clicks in this
00:16:16.139
component so you know if we click there
00:16:17.760
if we click there if I click there and
00:16:19.380
if we click there let's just create a
00:16:21.540
form we just get a very basic one where
00:16:23.940
I show you how the store works and also
00:16:27.060
show you how we would actually just so I
00:16:29.579
can super quickly show you how we can
00:16:32.279
actually store and retrieve our store
00:16:34.980
and our data for our app from local
00:16:37.560
memory from the local machine even if we
00:16:40.860
res turn off our computer turn it back
00:16:43.139
on close the browser to persist it and
00:16:46.320
then we just have a submit button and on
00:16:48.839
this form data key let's just call it
00:16:52.259
form or ADD and then let's just down
00:16:54.720
here have an unordered list which you
00:16:57.120
can call data key list and I'm already
00:16:59.639
seeing something else here so what we
00:17:02.160
might maybe put in not abstraction as
00:17:03.899
well is to check all the data keys and
00:17:06.419
compile elements for us automatically so
00:17:09.720
what we can actually do in our actual
00:17:12.780
event let's wrap it in another function
00:17:16.140
that passes something along as well Ram
00:17:19.380
event and let's pause a second thing
00:17:22.319
that is a function that just gets us a
00:17:26.040
specific so this needs to be a callback
00:17:28.319
as well so let's just say let's call
00:17:30.720
this callback and let's say get elements
00:17:33.540
and a param that is just a string and
00:17:37.380
that is a key and it returns a array of
00:17:42.660
HTML elements so it depends on how many
00:17:45.480
there are let's say a second param HTML
00:17:49.380
element and the second param is just and
00:17:54.360
let's just make an optional Boolean is
00:17:57.059
let's just call it strict by default
00:17:59.940
strict mode is true the that means that
00:18:04.559
if strict mode is true let's make it
00:18:07.799
something shorter let's say just get
00:18:09.660
HTML yeah let's let's keep it that like
00:18:12.720
we had it previously at HTML and so
00:18:15.600
let's just add a quick note here that
00:18:17.280
the others are pretty self-explanatory
00:18:19.200
uh if true throws an error if not a
00:18:24.480
single match is found okay and here we
00:18:27.480
can just say the data key attribute
00:18:29.700
value okay let's just also say here is
00:18:33.660
through by default so you need to
00:18:35.940
explicitly set it to false all right and
00:18:38.400
so we want to make this available
00:18:41.640
um both our events callback and our
00:18:44.640
connect callback let's maybe pass it as
00:18:47.460
the third one so let's maybe pass the
00:18:50.100
get HTML and here maybe after the event
00:18:52.919
cool so that's if we want to do anything
00:18:55.559
with anything here so how would we pass
00:18:58.500
this through to any of these so it's
00:19:01.980
actually not that hard it's the issue
00:19:04.860
comes in when we want to unregister it
00:19:07.860
because we need to have access to it in
00:19:10.140
here so unsubscribe is actually easy
00:19:11.940
because we can actually just create a
00:19:15.179
wrapper for that so in here let's just
00:19:17.760
say wrapper and that is previous next
00:19:22.260
yes this is just the current behavior so
00:19:25.740
if we were to do it in that way then we
00:19:28.080
want to pass another thing automatically
00:19:31.220
to connect that will be get HTML so
00:19:36.480
let's create get HTML and let's just
00:19:39.600
create it in our connected callback
00:19:41.340
actually because we're registering both
00:19:43.740
of them here okay so key strict okay so
00:19:47.940
we can say that let's say const results
00:19:51.480
is document this in a query selector and
00:19:55.799
just looking for the data key that was
00:19:58.140
specified so the only conditions when
00:20:01.380
strict shouldn't run is if it is false
00:20:05.220
so we effectively say if it's not false
00:20:07.440
then do the following we want to say a
00:20:09.720
result well let's say smaller or equal
00:20:11.520
to zero it is strict mode and this
00:20:15.660
condition is made in throw error and
00:20:18.000
that is throw a new era no elements
00:20:20.160
found work okay and let's close that off
00:20:22.620
so that means that we can ask it in here
00:20:26.400
and it is unhappy because expect two
00:20:29.039
arguments connect and we need to update
00:20:32.460
connect here and say param is get HTML
00:20:36.419
and handlers so we already have it there
00:20:38.940
so here we are passing it and it's
00:20:41.160
unhappy because oh we never actually
00:20:43.320
return results so let us just create a
00:20:47.100
quick helper function to coerce that
00:20:49.260
into HTML elements up here what we can
00:20:52.200
just do is let's just say const node
00:20:54.960
list to array okay so node list array
00:20:58.860
from node list but we want to say that
00:21:01.200
it should take Ram any return an array
00:21:06.780
of HTML elements once the result is all
00:21:11.760
right and then we return the result into
00:21:13.980
that where is R so here we go so let's
00:21:18.480
just return cool so now it should return
00:21:21.000
an HTML element all right this is Happy
00:21:24.000
the only thing that is still missing is
00:21:26.940
our event listeners
00:21:29.159
we might need to do this in another way
00:21:31.380
so we might need to just say you know
00:21:33.659
listeners and then instead create the
00:21:37.620
wrapper here and then instead do it this
00:21:41.280
way so a Handler event yeah and then
00:21:44.580
unfortunately a sign listeners so push
00:21:49.400
the key and the and the wrapper and then
00:21:53.280
we'll need to use this then instead to
00:21:56.220
remove it instead so we won't be able to
00:21:58.620
Loop over the actual object itself we'll
00:22:00.840
need to Loop over this because there's a
00:22:04.080
functional one level up so it's not the
00:22:07.080
actual Handler itself that we're
00:22:08.940
registering we're wrapping the handling
00:22:10.679
another function and that function is
00:22:12.900
actually the one that we should remove
00:22:14.460
okay all right and that is all what are
00:22:18.000
we missing okay cool here we go and so
00:22:22.020
you you might have lost me somewhere
00:22:24.120
here that is okay like don't worry too
00:22:27.120
much about it if you were able to
00:22:29.520
understand most of this congratulations
00:22:32.039
like you actually know enough to be able
00:22:35.039
to create your own JavaScript framework
00:22:37.080
which is not something a lot of even
00:22:39.000
Junior developers can say if you
00:22:41.039
understood everything even better but my
00:22:44.039
guess is you probably understood some of
00:22:45.600
it it's not the end of the world I just
00:22:47.039
want to show you kind of broadly how we
00:22:49.320
would actually go about abstracting a
00:22:51.360
lot of this low-level stuff so that we
00:22:53.340
don't need to all the time rewrite all
00:22:56.039
of this and we can Elevate the essence
00:22:58.080
of what it means to create a component
00:23:00.299
with without all of this low-level noise
00:23:02.840
of assigning things making things
00:23:05.340
private Setters Getters all of that
00:23:08.280
stuff so here is effectively our
00:23:10.860
JavaScript framework that we created and
00:23:13.440
obviously pretty soon we're going to be
00:23:14.700
looking at actual real JavaScript
00:23:16.500
Frameworks that you would probably use
00:23:18.480
in production in your work day in day
00:23:20.520
out as a JavaScript developer all right
00:23:22.679
so let's just see at the very least of
00:23:24.419
these things do not break reload okay
00:23:27.840
awesome so what we want to do is we so
00:23:31.860
we have this form we want to listen for
00:23:34.860
submit event instead so what we want to
00:23:37.860
do is we want to go event first and
00:23:40.500
foremost we want to do event prevent
00:23:42.240
default okay so to prevent the default
00:23:44.880
submission Behavior here just to make
00:23:47.460
our lives easier we are going to tell he
00:23:50.100
is check that hey let us take control
00:23:51.780
here we know what we're doing so what I
00:23:53.460
would usually do is I would go event as
00:23:56.100
any and then just pass event and I will
00:23:59.400
just set the type to any so any
00:24:01.440
effectively says leave this alone this
00:24:03.780
can be anything we are going to handle
00:24:05.640
this what I then would do is I would try
00:24:07.980
and grab the key event has any Target
00:24:10.860
and I would go data set and key so if at
00:24:15.059
any of these so we use a chain of
00:24:17.940
optional dot notations like this so if
00:24:21.179
any of these are not true this is going
00:24:22.860
to be undefined so here we can bring the
00:24:25.020
typing back in and tell it like okay
00:24:26.520
cool you can take control here again so
00:24:28.200
we can say type string or undefined so
00:24:31.080
effective fatality hey give us control
00:24:32.940
then we write this and we say it like
00:24:35.220
cool okay here you can continue again
00:24:36.840
and then we can do our logic here so
00:24:38.820
let's just say E equals add so if
00:24:42.780
there's an ad let's just console log for
00:24:45.059
now one two three so this should
00:24:47.340
theoretically trigger so hey one two
00:24:49.620
three and if we click anywhere else or
00:24:51.480
whatever here we want to check what's in
00:24:53.700
the form convert it into Data so we can
00:24:56.580
do let's just say response so new form
00:25:01.520
data and we just do event Target and we
00:25:05.280
should just check that event Target is
00:25:08.220
an instance of HTML form element so you
00:25:12.900
might be feeling that sure this is a lot
00:25:15.059
of work like marking these things up and
00:25:17.820
that is the reality of static typing and
00:25:20.159
then this is something you need to
00:25:21.720
figure out whether it is worth it for
00:25:23.400
you
00:25:24.059
um do you want the guarantees that you
00:25:26.460
get and like the you know if I were to
00:25:28.799
do that like those little things
00:25:31.919
um are you willing to do a bit of extra
00:25:33.419
typing to get those warnings for me I do
00:25:36.600
so I'm happy with it but you might be
00:25:38.640
like listen I don't want to use TS check
00:25:40.559
but my guess is you'll probably actually
00:25:42.120
spend more time fixing errors but it is
00:25:44.159
for you for you to actually decide to be
00:25:46.799
a form because vs code can only tell you
00:25:49.559
if something is wrong if it is able to
00:25:51.419
figure out what it is so you might need
00:25:53.400
to help it figure out and so data then
00:25:56.640
just is we just have a name there oh
00:25:59.820
crap so we can do object from entries
00:26:03.380
and response is it from entries well I
00:26:07.860
think we're also maybe just using a
00:26:09.419
version that is too old let's go up to
00:26:11.940
19 yes okay what we also need to do
00:26:15.360
after we do that event Target reset we
00:26:20.760
might even create an abstraction for us
00:26:22.919
to handle form submissions that is
00:26:25.380
probably what I will do for now let's
00:26:27.419
check this out
00:26:29.720
hey check this out all right so what we
00:26:33.360
want to do now is we want to push these
00:26:35.340
up into our store let's also just while
00:26:38.340
we're at it and let's actually just
00:26:40.440
every time after we do a submission
00:26:42.539
let's actually just cancel log the state
00:26:44.340
of the store the store so it does
00:26:46.260
doesn't obviously added to the task so
00:26:48.480
up to the store let's add some logic so
00:26:52.200
let's bring in the action that would do
00:26:54.720
that so from a store we need to get
00:26:57.240
dispatch and we also need to get actions
00:27:01.620
so one thing that you will see is you'll
00:27:04.200
see as your code gets more structured as
00:27:07.380
it gets more complex you are going to
00:27:09.539
have to do more typing and that is just
00:27:12.299
the reality in the same way that if you
00:27:14.640
are building a skyscraper you are going
00:27:17.279
to have to do a lot of extra things
00:27:19.320
compared to if you are just building a
00:27:21.900
Wendy house at the back of your house
00:27:23.940
and you're gonna have to take a much
00:27:26.760
more structured approach you're going to
00:27:28.140
have a lot more things in place one of
00:27:30.419
them you can go very fast the other one
00:27:32.580
you actually go slowly and a little bit
00:27:34.740
and deliberately because you understand
00:27:37.559
the complexity is going to grow why do
00:27:40.320
we want so from we don't want our store
00:27:43.260
we want actions and uh task action
00:27:47.279
Creator all right so all that we do over
00:27:50.880
here is then dispatch and why do we
00:27:54.720
dispatch we dispatch we create an action
00:27:57.960
here and we use the what was it create
00:28:00.059
task let's just rename that to title
00:28:03.299
here all right and that is a string and
00:28:05.880
it's not happy because file is not
00:28:08.220
assigned let's call that title instead
00:28:10.380
of name we might also need to turn it
00:28:12.600
into a string just to make this check
00:28:15.120
happy let's just say to string just to
00:28:17.760
ensure it's a string because at this
00:28:19.380
point it doesn't know what it is it
00:28:21.000
doesn't know where it comes from cool
00:28:22.740
and there are three tasks so now we
00:28:25.980
obviously want to listen to our store
00:28:27.840
and actually when a new task gets added
00:28:31.500
put it in our unordered list here so
00:28:33.900
this is where the get HTML is going to
00:28:35.820
be helpful so let's say
00:28:37.679
UL let's say get HTML and what we want
00:28:41.340
is we want list and it is strict and we
00:28:44.520
can assume that there's going to be be
00:28:46.620
at least one so we can de-structure and
00:28:49.140
then that should be an HTML element
00:28:51.059
otherwise it's going to give us an error
00:28:52.799
then child to that and we obviously need
00:28:56.460
to create so let's say Li and create
00:28:59.960
document create element so Li and then
00:29:04.679
we want to assign in a text again so
00:29:07.620
before all of this we need to compare
00:29:10.400
the previous and the current state all
00:29:13.860
right but before we do any of this we
00:29:15.480
need to figure out when we need to add
00:29:17.159
something we want to create two arrays
00:29:19.200
we want to create a array of all the
00:29:22.020
let's say next tasks so object value so
00:29:25.620
we get all the values of next task and
00:29:28.260
we turn that into an array we want all
00:29:30.419
the keys of the previous task the
00:29:32.820
previous task IDs and so instead we do
00:29:35.760
object keys so what we then want to do
00:29:38.580
is we want to Loop over the next tasks
00:29:40.620
the for each item and then in that we
00:29:44.340
want to say const is new so we want to
00:29:47.640
take all the previous task IDs and check
00:29:50.340
if the one that we're currently mapping
00:29:52.500
over is in that so if it's not in it we
00:29:56.340
can say it's new let's just say if is
00:29:59.159
new then we want to attach it so this
00:30:01.740
would be item title UL a bin child l i
00:30:06.600
so theoretically this should work let's
00:30:09.120
have a look hey check this out and let
00:30:11.039
me also just have the condition for
00:30:13.320
should delete const should delete so
00:30:17.520
let's just move this in here and so
00:30:21.240
we're gonna also map over it but the
00:30:23.760
other way around we're gonna map over
00:30:26.100
the previous ones and see if there are
00:30:29.100
any of the previous ones that are not in
00:30:31.799
the new one so let's also just create a
00:30:34.440
const next tasks desktos ID object Keys
00:30:39.299
Next tasks okay so we're mapping over
00:30:42.600
all the previous keys and what we want
00:30:45.059
to check is we want to check if a key
00:30:48.779
that was previously in the store is now
00:30:51.779
no longer in the store so we want to say
00:30:53.940
if next task IDs does not include the ID
00:30:58.980
that we're mapping over so if it does
00:31:01.380
then just return don't do anything and
00:31:04.020
actually let's do the same here let's
00:31:06.059
just because now we can get rid of the
00:31:08.159
level of nesting just to keep our code
00:31:10.200
from getting like heavily nested and the
00:31:12.480
same here so if it does that's fine
00:31:14.700
don't do anything so let's also add the
00:31:17.940
ID when we add it l i data set ID we can
00:31:23.520
just get item.id and that way we'll be
00:31:26.760
able to find it in here as well let's
00:31:29.460
actually just grab ul and we would then
00:31:32.220
let's just get the node so UL query
00:31:35.520
selector data ID equals and then we can
00:31:40.740
just check if node instance of HTML
00:31:44.039
elements if it's not then new error
00:31:47.179
required to be HTML element what we can
00:31:51.299
then do is just node remove as simple as
00:31:54.299
that right so now we map over it we
00:31:56.399
check what has been added we map over it
00:31:58.320
we check what has been removed and this
00:32:00.720
should still work okay so we are
00:32:02.880
listening for things that if anything
00:32:04.799
gets removed but currently with the
00:32:06.779
store there is no way to remove
00:32:08.340
something so what I want to show you now
00:32:10.860
is why do we go through all of this you
00:32:15.360
might look at what we've done up until
00:32:16.919
now and and you might actually start
00:32:18.720
questioning what I'm doing and why I'm
00:32:21.000
doing it and I think that's why I
00:32:22.919
started this video by saying that I'm
00:32:25.799
going to do the example first and then
00:32:27.720
I'm going to explain it and the reason
00:32:30.120
for that is from here on out we're going
00:32:33.179
to start using third-party abstractions
00:32:35.460
so whether these are libraries there are
00:32:39.059
Frameworks and so forth we need to
00:32:41.820
understand what problem these libraries
00:32:44.399
solve for us before we start using them
00:32:47.220
I very strongly believe that because if
00:32:49.919
you just learn the library or the
00:32:51.720
framework for its own sake and you never
00:32:54.419
understand what it actually does you
00:32:57.120
just learn it because people told you
00:32:58.980
you need to learn Redux you need to
00:33:01.080
learn react you need to learn view first
00:33:03.419
and foremost you're not going to have
00:33:05.039
the insight to actually make a decision
00:33:07.559
in terms of what framework is best for
00:33:10.200
what type of project because I do
00:33:11.940
believe certain Frameworks are better
00:33:13.620
suited for certain projects and we'll
00:33:15.840
talk about that a bit more when we start
00:33:17.640
introducing these Frameworks and the
00:33:19.679
other thing is if you don't know what
00:33:21.240
these Frameworks extract you're going to
00:33:23.220
have a very hard time actually debugging
00:33:26.279
it when they start falling apart so
00:33:28.679
let's take first example a car so you
00:33:30.960
don't need to understand how a Car Works
00:33:33.299
in order to drive the car you just need
00:33:35.760
to know you can turn the steering wheel
00:33:37.500
you can press the gas pedal and change
00:33:40.019
the gears that's all you need to know
00:33:42.059
and generally that is the sign of a good
00:33:44.399
abstraction any good abstraction should
00:33:46.980
hide all the low-level things that are
00:33:49.140
not important and knowing how combustion
00:33:51.779
Works knowing how the tires are attached
00:33:54.419
to the car knowing what a spark plug
00:33:56.640
does or a compressor or a fuel injector
00:33:59.700
knowing what those things do is
00:34:01.200
irrelevant in terms of using the
00:34:03.360
abstraction but here is the trick and
00:34:06.419
there's a very famous article by someone
00:34:08.820
called Joel spielenski and this is an
00:34:11.879
old article it was written in 2002 but
00:34:15.000
it still has a very big impact on the
00:34:18.060
software industry and how we think about
00:34:20.219
abstractions and you might in your
00:34:22.139
career hear this article referenced a
00:34:24.300
lot and I'm just going to highlight some
00:34:26.040
key things from it and it's called The
00:34:28.020
Law of leaking abstractions and what
00:34:30.659
this effectively says is that there is
00:34:33.060
no such thing as an abstraction that
00:34:35.040
doesn't leak at some point and what we
00:34:37.859
mean when we say an abstraction leaks is
00:34:40.260
that sometimes it can hide all the
00:34:43.139
underlying stuff from you in some
00:34:45.000
circumstances some abstractions do that
00:34:47.520
better than others but at some point
00:34:49.918
some of that is going to leak you can't
00:34:52.379
always under all circumstances hide the
00:34:55.379
thing that is getting abstracted purely
00:34:57.780
just through your interface so he uses
00:35:00.420
the example of TCP we're not going to
00:35:02.520
touch on TCP specifically I'm just going
00:35:05.220
to talk to talk about the general idea
00:35:07.020
TCP is a very Advanced concept so let's
00:35:11.280
look at his example instead of getting
00:35:13.380
down into the the weeds around like what
00:35:16.140
exactly TCP is so he uses the example
00:35:18.900
and he says imagine action allows you to
00:35:21.300
send actors from one place to another
00:35:24.660
and it involves putting them in cars and
00:35:27.000
driving them across the country some of
00:35:29.040
the cars crash killing the poor actors
00:35:32.339
so you know that some of them don't
00:35:34.500
reach the destination that like you lose
00:35:36.780
them some get drunk on the way go
00:35:39.060
authorells and you know they can no
00:35:42.000
longer work as an actor he also says
00:35:43.980
sometimes actors you know come in a
00:35:46.500
different order than you actually sent
00:35:48.660
them so let's say you send one person
00:35:50.220
but someone else arrives before them and
00:35:52.920
so what he effectively just did here is
00:35:54.780
he described PCP for us okay so you
00:35:58.079
might think this is a very weird example
00:35:59.520
but he's just describing the realities
00:36:01.140
of TCP and so he says like imagine
00:36:03.000
there's a new service called Hollywood
00:36:04.740
Express he's much more reliable and it
00:36:08.040
guarantees that they first and foremost
00:36:09.839
they arrive in the order that you sent
00:36:11.880
them and they arrive in perfect
00:36:13.859
condition so they don't get caught up in
00:36:16.500
a car crash they don't get lost along
00:36:18.300
the way you don't lose them and they
00:36:21.060
don't come out at the side completely
00:36:23.520
erect I don't know why he chose this
00:36:26.160
example but it is what it is so let's
00:36:28.800
just run with it so he says the magic
00:36:30.599
part about Hollywood Express is that it
00:36:33.420
actually abstracts the first super messy
00:36:37.079
version that we spoke about it checks
00:36:39.660
that the actors arrive in good condition
00:36:42.240
and if they don't arrive in good
00:36:44.460
condition it fixes it for you so it
00:36:47.099
effectively says hey let's get someone
00:36:49.079
who looks like this actor and let's send
00:36:51.300
them instead so you don't know what's
00:36:53.160
happening behind the scenes it solves
00:36:54.660
that problem for you all you know is you
00:36:56.160
you put an actor in a car and they
00:36:57.900
arrive in the same order at the new
00:36:59.520
place you don't know how that happened
00:37:00.780
so
00:37:02.099
his example gets a bit weird in some
00:37:04.619
places but he says you know let's say
00:37:06.060
something weird happens and they don't
00:37:08.099
arrive in the order that you sent them
00:37:10.500
underneath the hood what Hollywood
00:37:12.420
Express does is it actually waits for
00:37:14.940
all of them to arrive and then it
00:37:16.380
rearranges them it takes longer than it
00:37:18.599
would have been but they do arrive in
00:37:20.520
the order that you sent them it just
00:37:22.320
from your side using the abstraction it
00:37:25.380
just looks like the actors are arriving
00:37:26.820
more slowly than usual and so he said
00:37:28.980
you know that is approximately the magic
00:37:30.900
of tcpe it is what computers call an
00:37:33.900
abstraction in other words a
00:37:35.520
simplification of something much more
00:37:37.320
complicated that is going on under the
00:37:39.599
covers this is what we've been doing up
00:37:42.180
until now with our own abstractions this
00:37:44.339
is what Frameworks do this is what
00:37:45.960
libraries do this is even what
00:37:47.880
JavaScript itself does if you remember
00:37:49.859
JavaScript there's actually several
00:37:51.960
lower levels below JavaScript that
00:37:54.540
JavaScript actually abstracts he said
00:37:56.940
you know like so in his example he says
00:37:59.099
that his example abstracts away the
00:38:01.560
lower level logic and in most cases it
00:38:04.200
does but there are age cases where it
00:38:06.420
doesn't there are edge cases where you
00:38:07.800
actually need to understand what is
00:38:09.060
happening under the hood to fix problems
00:38:11.339
you said you know in his example he said
00:38:13.500
that TCP guarantees your messages will
00:38:16.079
arrive and if you want to be technically
00:38:18.300
correct that's not the case things can
00:38:20.220
happen you know your cable might break
00:38:23.099
you might be at a workplace where they
00:38:25.320
actually block specific type of traffic
00:38:26.940
and so he effectively says you know this
00:38:29.339
is what's called a leaky abstraction and
00:38:31.320
in these cases the abstraction can't
00:38:33.900
hide all of that from us and this is
00:38:36.300
where he coins the law of leaky
00:38:38.339
abstractions he says all non-trivial
00:38:40.320
abstractions are non-trivial being
00:38:41.940
important abstractions all important
00:38:44.700
abstractions to some degree early so he
00:38:47.400
says abstractions fail sometimes a
00:38:49.619
little sometimes a lot things go wrong
00:38:51.480
it happens all over the place when you
00:38:53.160
have abstraction so he lists a couple of
00:38:55.440
like really complex things um the
00:38:58.140
closest one to what we are doing is so
00:39:00.119
he talks about learning asp b.net which
00:39:03.599
is a kind of a different language but
00:39:05.040
it's also a way to build websites and
00:39:07.020
stuff so he says it would be nice if you
00:39:09.060
could just teach them to double click on
00:39:11.160
things and then write code that runs on
00:39:13.140
the server when the user clicks on those
00:39:14.820
things and honestly this is what a lot
00:39:16.859
of tutorials do this is a lot what a lot
00:39:18.960
of coding schools do so you might come
00:39:21.119
across as coding schools where they they
00:39:23.160
are going to teach you JavaScript in two
00:39:25.500
weeks and I'll maybe even link a video
00:39:27.480
where someone kind of talks about this
00:39:29.220
concept but the thing is what they do is
00:39:30.960
they teach you the abstraction okay
00:39:32.880
that's cool you know like so you just
00:39:34.740
follow along step by step you use the
00:39:36.300
abstraction in the same way that someone
00:39:38.160
teaches you about cars they just show
00:39:40.140
you how to turn the steering wheel they
00:39:41.760
just show you how to press the gas pedal
00:39:44.220
and how to actually use the gears and
00:39:47.760
they might tell you I've taught you how
00:39:49.500
to use a car go ahead use a car and your
00:39:51.900
friend might also be at a place where
00:39:53.700
they're teaching them about cars before
00:39:55.859
they get to that part they teach them
00:39:57.480
about like Wheels what are wheels how
00:39:59.220
are the wheels attached to the car what
00:40:00.839
do you do if you get a flat tire player
00:40:02.579
when you turn the steering wheel what is
00:40:04.619
actually happening what is moving in the
00:40:06.660
car when you press the gas pedal what is
00:40:09.599
actually happening why do you need
00:40:11.099
petrol in your car why is the gas pedal
00:40:13.740
not working if you don't have petrol and
00:40:15.780
so forth that teach the underlying
00:40:18.180
Concepts that are getting abstracted
00:40:19.980
away and you might tell that person
00:40:21.420
listen you're getting ripped off I went
00:40:23.220
to this amazing place they taught me how
00:40:24.839
to use a car in two weeks and I am
00:40:26.940
driving and living my best life I'm
00:40:28.619
driving all over the world and he might
00:40:30.480
take four months to reach that same
00:40:32.099
place but here's where the problem comes
00:40:34.500
and I'm going to continue with the
00:40:35.640
article to show this he uses the example
00:40:38.220
what asp.net does it extracts away the
00:40:41.940
HTML so you don't need to know the
00:40:44.760
difference between hyperlinks and a tag
00:40:47.640
and a button tag because it actually
00:40:49.560
says you know it's going to abstract
00:40:50.880
that away you just want something that
00:40:52.920
performs an action you don't want to
00:40:54.599
know what are all the ways that that
00:40:55.920
action can be performed why the
00:40:58.260
abstraction does it in this way instead
00:41:00.180
of that way what even isn't a tag or a
00:41:03.060
button and as you should probably know
00:41:04.619
by now from the examples we've shown he
00:41:06.540
says the problem is what is getting
00:41:09.060
abstracted away is the fact that only a
00:41:12.300
button can submit a form a link an ATAC
00:41:15.540
can't actually submit a form so what
00:41:17.700
they then do in asp.net is they actually
00:41:21.240
abstract that away and they do a bit of
00:41:23.520
magic to make sure that whether it's a a
00:41:27.119
tag or a button it can still submit the
00:41:29.220
form it doesn't matter so keep in mind
00:41:31.140
this is 2002 this is quite some time ago
00:41:34.560
this is 21 years ago so obviously the
00:41:37.200
examples that he's using is a bit data
00:41:39.540
people don't do these things with
00:41:41.280
asp.net anymore.net is used in a
00:41:44.280
completely different way nowadays you
00:41:45.660
mostly just still find asp.net on like
00:41:47.760
Old Government websites and so forth and
00:41:50.040
he also talks about you know
00:41:51.780
um they'd say someone's JavaScript is
00:41:53.460
not working properly which was a much
00:41:55.200
bigger problem 20 years ago than
00:41:57.420
nowadays but the point being let's say
00:42:00.119
someone visits a website and the
00:42:01.920
JavaScript doesn't run and if you don't
00:42:04.140
understand that the way in which asp.net
00:42:08.400
make sure that you can use either an a
00:42:11.460
tag or a button is by means of
00:42:13.680
JavaScript and what how it actually does
00:42:16.200
that when you use the abstraction and
00:42:19.020
something goes wrong with the JavaScript
00:42:20.700
let's say you add a bug in the
00:42:22.320
JavaScript and it fails also well then
00:42:24.960
the forms are not going to work and
00:42:26.579
you're not gonna know why the forms
00:42:28.260
don't work because you don't understand
00:42:29.460
in the abstraction somewhere it actually
00:42:32.400
does that but magic with JavaScript so
00:42:34.920
you might try and solve the issue of the
00:42:36.599
forms first before you get to the
00:42:38.520
JavaScript because you're not being able
00:42:40.440
to submit a form is maybe much more
00:42:42.780
important than like some JavaScript
00:42:44.339
animation not working or whatever but
00:42:46.260
because you don't understand that
00:42:47.820
there's a part of the JavaScript under
00:42:49.619
the abstraction you might be banging
00:42:51.900
your head against the wall not able to
00:42:54.359
solve this you don't know why it's not
00:42:56.400
working anymore in the same way you know
00:42:58.680
if you've just been taught that you
00:43:01.440
press the pedal to drive the car you
00:43:03.540
turn the steering wheel and you change
00:43:05.640
the gears you might not understand why
00:43:08.280
if the petrol Runs Out you press the
00:43:10.260
pedal the thing that you've always done
00:43:11.940
and it the car doesn't want to drive you
00:43:14.099
don't know it's been abstracted away
00:43:15.540
from you you're just like this usually
00:43:17.099
works I don't know why it's not working
00:43:18.180
now or you might get a flat tire and you
00:43:20.460
might struggle to turn the steering
00:43:21.839
wheel and you don't know why is the
00:43:24.060
stroke usually this is fine what's going
00:43:26.280
on now whereas the person that actually
00:43:28.440
learned those underlying abstractions
00:43:30.599
learned what those actual tools abstract
00:43:32.940
way is able to actually just efficiently
00:43:36.240
use the pedal use the steering wheel use
00:43:39.720
the gears as someone who only knows the
00:43:42.420
abstraction knowing what goes on under
00:43:44.640
the abstraction isn't going to make it
00:43:46.560
harder to use abstraction you're going
00:43:48.119
to still use it in the same way but when
00:43:50.400
things go wrong you know enough about
00:43:52.319
what's under the abstraction to actually
00:43:54.619
talk about it even if you can't fix it
00:43:57.660
yourself at the very least you know you
00:44:00.359
can talk about it somewhat so even if
00:44:02.700
you like you would know then the car
00:44:05.099
needs to go to a mechanic or at the very
00:44:07.020
least you need to know you need to go to
00:44:08.880
a petrol station to get some more petrol
00:44:11.099
where someone who just learns
00:44:12.420
abstraction they have no idea all they
00:44:14.760
can say is this usually works I don't
00:44:16.500
know why it's not working now and I've
00:44:18.000
seen a lot of developers specifically
00:44:20.040
Junior developers get themselves in a
00:44:22.260
lot of trouble that way because they
00:44:24.119
just learned abstraction so they just
00:44:26.160
know how to use abstractions they just
00:44:28.200
know how to create a component and react
00:44:30.000
they know how to submit a form in react
00:44:31.740
they know how to call data binary act
00:44:33.720
but when something goes wrong and
00:44:37.140
something in the abstraction doesn't 100
00:44:39.119
line up then they have no idea where to
00:44:42.420
even start talking with their team about
00:44:45.180
what's going on all they can say is I
00:44:47.099
usually do this and now for some reason
00:44:49.140
it's not working and that's not helpful
00:44:50.760
to anyone and it's definitely not going
00:44:52.560
to be useful for you in terms of your
00:44:54.960
career and also you are not gonna be
00:44:57.420
able to have meaning discussions over
00:44:59.160
why you use this framework instead of
00:45:01.380
that framework because you don't even
00:45:03.000
know what these Frameworks do under the
00:45:04.980
hood so I might have a discussion
00:45:06.780
whether I'm buying like a small fuel
00:45:08.760
efficient car so in the same way if
00:45:10.800
you're shopping for cars you might look
00:45:12.660
at like a massive four by four Hummer or
00:45:15.960
like a small let's say like Polo or
00:45:18.240
something and if you don't know anything
00:45:19.740
about cars or how engines work very bare
00:45:23.339
minimum level you might buy the the
00:45:25.619
massive like four by four and then a
00:45:27.900
couple of months later you might realize
00:45:29.160
why am I spending so much money on
00:45:31.440
petrol my previous car all cost me like
00:45:34.380
a thousand Rands two thousand three
00:45:36.240
thousand rounds of petrol every month
00:45:37.980
this one is costing me like twenty
00:45:40.319
thousand what is going on and it's
00:45:41.579
because you don't understand the
00:45:43.500
Dynamics of why certain cars consume
00:45:46.260
more petrol and why and you might leave
00:45:49.079
that experience going okay next time I'm
00:45:51.780
just gonna buy like a small little Polo
00:45:53.640
or whatever I'm I'm never gonna buy a
00:45:56.220
car that I'm gonna pay so much on petrol
00:45:58.380
again and so you do that but then for
00:46:00.720
some holiday trip you join friends and
00:46:02.700
you kind of go to some rural place out
00:46:05.579
in South Africa somewhere and all of a
00:46:07.380
sudden your little Polo is getting stuck
00:46:09.000
in the mud it's struggling with the dirt
00:46:11.220
roads and maybe even breaks down
00:46:13.560
somewhere and now you kind of flip to
00:46:15.420
the other side again you're like I'm
00:46:16.680
never buying a car again that can't
00:46:18.839
handle like rough terrain and so forth
00:46:21.000
and you can see how if you don't
00:46:23.040
understand the things that get
00:46:24.540
abstracted again you're just gonna keep
00:46:26.940
on ending in these positions over and
00:46:29.460
over and over again where you're making
00:46:31.560
bad decisions and you don't have enough
00:46:33.960
information to even learn from those
00:46:36.240
decisions you don't even understand why
00:46:38.760
the framework you used wasn't a good fit
00:46:40.680
and then you end up in that position
00:46:42.119
again for another reason so what I'm
00:46:45.000
trying to do in this entire section
00:46:47.460
where we're talking about things like
00:46:49.619
encapsulation polymorphism even like
00:46:52.560
functional programming oop is these are
00:46:55.260
the parts that Frameworks are made of
00:46:57.240
and by understanding these parts you can
00:46:59.520
make a much more informed decision in
00:47:02.160
terms of what framework is a good fit
00:47:04.440
for what project and not only that but
00:47:07.140
you are also cognizant of what are the
00:47:09.480
trade-offs so you need to be aware of
00:47:12.240
those so let's say I do buy a polo then
00:47:14.760
I'm going to be like I don't think I
00:47:17.460
this holiday trip is a good idea my car
00:47:19.680
is going to struggle or let's say you
00:47:21.660
buy a 4x4 massive 4x4 that's just like
00:47:24.359
chugs petrol you might be like what I
00:47:26.700
know about this car and like a bit about
00:47:29.640
what happens underneath the abstraction
00:47:32.220
of the steering wheel and the pedal and
00:47:34.440
so forth I know that I probably
00:47:36.060
shouldn't use this car for daily commute
00:47:38.520
in and out of the office every day why
00:47:41.099
am I saying all of this and the reason
00:47:42.839
is that this video and maybe this little
00:47:46.079
bit that's come gonna come after this as
00:47:48.060
well is going to be really frustrating
00:47:50.099
but that frustration is important
00:47:52.980
because it shows you what problem
00:47:54.960
Frameworks are solving for us and being
00:47:57.359
able to have a bit of an understanding
00:47:59.160
of what goes on below the abstraction of
00:48:01.500
Frameworks is also going to help you
00:48:03.720
really make good decisions in terms of
00:48:05.760
Frameworks and also understand what are
00:48:09.119
good ways to use a specific framework
00:48:11.040
what type of things should you not try
00:48:12.900
and do with a framework even if you are
00:48:15.240
forced to use a specific framework so
00:48:16.859
let's say you join a team that is using
00:48:19.200
angular and you might not even like
00:48:20.940
angular at the very least you know a bit
00:48:23.160
about what goes on under the abstraction
00:48:25.260
to understand what are the type of
00:48:27.180
things that are idiomatic to this
00:48:29.520
framework what are the type of things
00:48:30.839
that you should avoid and is this going
00:48:32.640
to actually make it perform worse make
00:48:35.940
it less maintainable and so forth and so
00:48:38.040
forth so just to end this article let me
00:48:40.440
just highlight the following so what he
00:48:42.240
effectively says the law of leaky
00:48:43.920
abstractions means that whenever
00:48:45.540
somebody comes up with a new code
00:48:47.460
generation tool that is supposed to make
00:48:49.680
all of us more efficient you hear a lot
00:48:51.599
of people saying the following learn how
00:48:53.940
to do it manually first then use the new
00:48:56.640
tool to save you time and he says the
00:48:58.800
reason is like all abstractions these
00:49:01.740
tools lead and the only way to deal with
00:49:04.500
these leaks is to learn about how the
00:49:07.140
abstractions work and what they are
00:49:09.540
abstract the abstractions save us time
00:49:11.099
working but they don't save us time
00:49:13.079
learning and he says that irony being
00:49:16.200
because our abstractions are getting
00:49:17.819
better becoming a proficient programming
00:49:20.400
is actually getting harder and harder
00:49:22.500
and I definitely find this to be the
00:49:24.180
case because it is so easy to just jump
00:49:26.880
in with react and start using react and
00:49:29.220
not understand anything about what
00:49:30.960
reactors under the hood it's actually
00:49:32.700
becoming harder to become a good
00:49:34.319
programmer because you're running into
00:49:36.000
so many problems that are so far
00:49:38.400
abstracted from what you've learned that
00:49:40.560
you have no way of even knowing where to
00:49:42.780
start understanding those problems
00:49:44.520
interestingly enough he said to a
00:49:46.680
certain degree the law of leaky
00:49:48.300
abstractions is dragging us down and
00:49:50.339
this was like 21 years ago and I would
00:49:52.680
definitely say this is not only still
00:49:54.180
the case today but it is even more the
00:49:56.760
case now and this is why it is so hard
00:50:00.000
becoming a software developer because on
00:50:03.240
the surface it seems easy and the
00:50:05.460
surface it seems like you only need to
00:50:07.200
learn the abstraction you can watch a
00:50:09.119
five minute video that shows you how to
00:50:11.880
create a to-do list in react and you
00:50:14.760
might be all right I know react let's go
00:50:17.099
I'm gonna apply for a job and that's
00:50:18.720
because you just learned the abstraction
00:50:20.300
the problem is when you want to extend
00:50:24.060
that a bit further or you want to debug
00:50:26.940
a problem that came up now there's this
00:50:29.460
massive amount of knowledge that is so
00:50:31.740
far removed from this little basic
00:50:34.140
abstraction that you learned don't even
00:50:36.180
know how to tackle and this is also why
00:50:37.980
the industry at the moment is so Junior
00:50:40.200
heavy I always tell people your main job
00:50:43.020
as a junior entering the industry is to
00:50:45.359
get out of the junior pool as quickly as
00:50:47.700
possible there's a big demand for
00:50:49.319
intermediate developers there's a
00:50:51.059
massive mod for senior developers the
00:50:53.099
reason why the junior pool is so heavy
00:50:54.900
and why there are so many Juniors that
00:50:56.880
really struggle to get into that
00:50:58.559
intermediate level it's because they
00:51:00.300
just learned abstractions and the jump
00:51:02.640
from actually following instructions and
00:51:05.160
building something without understanding
00:51:06.780
what you're doing to a jump where you
00:51:08.880
understand what goes on below those
00:51:10.619
abstractions is a massive jump and they
00:51:12.900
don't understand why this next step in
00:51:15.300
their journey is so hard compared to how
00:51:17.819
easy the first step was and what you
00:51:19.859
actually find is a lot of people
00:51:20.880
actually drop out of the industry and
00:51:22.740
they're like there's something wrong
00:51:24.059
with me like I could get a job very
00:51:26.280
easily I could start as a junior very
00:51:28.020
easily but 10 years has passed and I'm
00:51:30.300
still a junior what is going on I'm not
00:51:32.040
growing in my career so it's very
00:51:34.319
important that we have these discussions
00:51:36.180
and it's very important that you are
00:51:38.160
patient when we talk through these
00:51:40.319
complex topics even though you might
00:51:42.420
have a friend that's like hey check how
00:51:44.400
easy it is to use react see how easy it
00:51:46.980
is to use view or you might see a
00:51:48.540
YouTube video where it is like hey
00:51:50.819
here's how to learn react in five
00:51:52.500
minutes here's how to create an app in
00:51:54.839
view in an hour it might very well be
00:51:57.119
that you don't believe me at this point
00:51:58.800
I was first and foremost say look for
00:52:01.319
similar opinion against there's a lot of
00:52:03.059
people out there saying the same thing
00:52:04.559
including Joel 21 years ago and then
00:52:07.380
eventually you're going to find this out
00:52:09.000
yourself the hard way if you just learn
00:52:11.040
the abstractions and at the very least
00:52:13.079
then you might think back about this
00:52:14.819
discussion you might be like okay I at
00:52:16.859
the very least know now what to do even
00:52:19.079
though it took me very long to realize
00:52:21.300
there's a lot of developers out there
00:52:22.800
that don't realize this and I think they
00:52:24.540
are the problem they think they're just
00:52:26.280
not smart enough or they can't just
00:52:28.079
progress in their career quickly enough
00:52:29.640
what I'm gonna do is I'm gonna just
00:52:32.040
query how the last bit of abstraction
00:52:33.900
something that allows us to
00:52:35.640
declaratively update our Dom and all
00:52:38.400
JavaScript Frameworks are based on this
00:52:40.440
principle of declaratively updating the
00:52:42.420
Dom which is a very functional
00:52:43.920
programming Principle as well so I'm
00:52:45.540
going to show you how we would build
00:52:46.619
that ourselves I'm going to tell you why
00:52:49.380
that is useful why that relates to
00:52:51.540
functional programming and why it's a
00:52:53.040
much more reasonable approach than not
00:52:55.619
doing it and then I'm going to actually
00:52:57.240
pull in a third-party tool that makes
00:52:59.160
that a lot easier for us my hope is that
00:53:01.500
at that point you had know everything
00:53:03.540
you need to understand what all these
00:53:06.839
Frameworks abstract away for us and we
00:53:09.300
can start gradually moving into the
00:53:11.940
space where we pull in the Frameworks to
00:53:14.160
show you how it saves us a lot of work
00:53:16.559
out saves us a lot of typing and code
00:53:19.020
but still understanding what it's doing
00:53:21.300
under the hood so that if it breaks we
00:53:23.819
know enough about what it abstracts to
00:53:26.099
attempt to solve the problem and get it
00:53:27.900
working again