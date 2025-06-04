00:00:00.000
that I just found the way that we had to
00:00:02.820
map over arrays and stuff just a little
00:00:04.440
bit different yesterday but it's it's
00:00:06.180
more just me needing to get used to
00:00:08.340
doing it that way that's the only issue
00:00:10.679
that I kind of had with it yesterday but
00:00:12.360
that's that's not I wouldn't call it a
00:00:13.980
massive issue it's just something to get
00:00:15.480
used to so when you say a bit different
00:00:17.880
what do you mean by that just out of
00:00:19.500
curiosity as opposed to no just the
00:00:22.020
syntactical differences between it um
00:00:24.300
and the way that they use their function
00:00:26.519
to create their awareness I still keep
00:00:28.980
thinking and the imperative way of
00:00:31.679
JavaScript I think that's probably what
00:00:35.100
is what made it motivated for me a
00:00:37.620
little bit difficult to uh to grasp
00:00:39.660
yesterday so that's why I said it's more
00:00:40.980
of a thing for me to just this is the
00:00:42.420
way it needs to be done I must just get
00:00:43.800
used to it being done in this way yeah
00:00:45.960
it is and you know and we haven't even
00:00:48.420
like started getting into like reduce
00:00:50.100
and all of those things and I I did
00:00:52.920
mention this in all the content leading
00:00:55.199
up to this is that this is the the
00:00:57.360
Paradox is that you know functional
00:01:00.199
programming is it takes a bit of time to
00:01:03.000
get your head around but once you get
00:01:05.280
your head around it it's so expressive
00:01:07.619
like you are just going to be like why
00:01:10.080
didn't I just use map and reduce
00:01:11.520
everything up until now but it is it is
00:01:14.880
a bit of a learning curve and you don't
00:01:16.740
have to do it that way but it's just
00:01:18.479
like it's almost for your own good so no
00:01:20.640
like definitely it is a bit of a mind
00:01:22.680
switch but um it's just going to make or
00:01:25.080
code so much more readable and so much
00:01:26.880
easier to reason about you know so if we
00:01:28.860
talk about kind of my general approach
00:01:31.320
to how I want to teach you guys there's
00:01:33.180
this kind of Axiom of you guys everyone
00:01:35.159
knows that you know like the whole thing
00:01:36.840
about teacher man to fish
00:01:38.460
um or give a manifest you know teach
00:01:40.439
them into JavaScript or give a man a
00:01:42.180
JavaScript but so the point being is
00:01:44.640
what I actually want to teach you guys I
00:01:46.680
don't want to teach you guys react I
00:01:48.360
want you getting good at react to be a
00:01:50.520
side effect of what I teach you guys but
00:01:52.920
what I want to teach you guys is how to
00:01:54.960
read documentation because if you are
00:01:57.899
able to do that you are able to teach
00:01:59.880
yourself basically anything and this is
00:02:02.100
why we did all these high level Concepts
00:02:04.320
because you'll see a lot of it come
00:02:06.000
through in the react documentation but
00:02:08.520
being able to just go and sit with
00:02:11.099
documentation and read it and understand
00:02:13.800
what the documentation says is a
00:02:16.080
superpower because now you can teach
00:02:17.760
yourself anything view Redux felt
00:02:20.760
opinion or whatever you don't need to
00:02:22.500
buy a udemy course for someone to
00:02:24.540
manually show you everything you can
00:02:26.459
actually just read any documentation and
00:02:28.319
not only can you read the documentation
00:02:29.879
you understand the general language that
00:02:32.640
is used to talk about the things so you
00:02:34.260
can also talk about it so if you're in a
00:02:36.720
team you're not going to be like my
00:02:38.459
component doesn't work and someone's
00:02:40.319
like okay what's going on why is it not
00:02:42.420
working no it just doesn't want to work
00:02:43.920
you know like that that's not useful to
00:02:45.840
anyone and like to me that wouldn't be a
00:02:47.640
good impression from it from a teammate
00:02:50.099
if they're not even able to talk about
00:02:51.660
their code so what I want to do going
00:02:53.640
forward is I spent a lot of time kind of
00:02:56.340
explaining react explaining how some of
00:02:58.440
these higher Concepts actually tie in
00:03:00.780
with reactai in with Frameworks what I
00:03:03.120
want to do now is gradually work through
00:03:05.760
the react documentation and then I also
00:03:08.220
want to introduce some additional
00:03:09.300
Concepts so whether that is another
00:03:10.800
framework on the side but we can quickly
00:03:13.260
look at or some extra things so for
00:03:15.239
example in this one I want to introduce
00:03:17.280
kind of material UI which is kind of the
00:03:21.060
most popular react component library and
00:03:23.819
so forth I have gone and I've just
00:03:26.159
actually taken some screenshots of the
00:03:28.620
actual documentation it's like put it
00:03:30.480
here in fig Jam so I can just write over
00:03:32.459
it add some code examples on the side
00:03:34.200
and so forth and explain it let's get
00:03:36.420
started on just the home page of the
00:03:38.280
react documentation it's a library for
00:03:40.319
web and Native user interfaces so this
00:03:43.260
effectively means that you can either
00:03:45.659
build something that runs in a browser
00:03:47.700
or you can build actual native signs and
00:03:49.799
so native doesn't only mean mobile apps
00:03:52.860
or app stores and so forth it kind of
00:03:54.780
means also stuff that you can store on
00:03:56.580
your desktop it's something that you can
00:03:58.080
install I don't know like on like a VR
00:04:00.900
device or whatever okay where it's often
00:04:04.019
used as for web interfaces so you know
00:04:07.140
software as a service so things like
00:04:08.819
Trello Netflix you know you guys haven't
00:04:11.580
heard the list
00:04:12.900
um but you can actually use it to build
00:04:15.480
like native software as well which is
00:04:18.000
one of the things that makes reactor
00:04:20.459
popular uh some of the other Frameworks
00:04:22.919
doesn't have this level of flexibility
00:04:24.419
and that's because it separates the core
00:04:27.000
react logic from what you bind it to
00:04:29.100
which is where we need that react Dom
00:04:31.020
Library
00:04:32.220
um because we actually we pull in the
00:04:34.320
logic and then we actually say we want
00:04:36.479
to apply this logic to the Dom
00:04:39.120
um but you can pull in react native and
00:04:41.100
all of that and I will maybe show you
00:04:42.960
guys super quickly some react native
00:04:44.460
stuff in the lessons effectively at the
00:04:47.400
core of react is this idea of components
00:04:50.759
no surprises here you by now should very
00:04:53.880
clearly know what a component is if you
00:04:56.820
came onto this documentation and you
00:04:58.979
didn't know anything about components
00:05:00.660
the knowledge that you have right now is
00:05:02.400
already empowering you a lot more to
00:05:03.960
actually understand what the
00:05:05.220
documentation says so it effectively
00:05:07.199
says you bowl your user interfaces out
00:05:09.660
of individual pieces called components
00:05:12.120
and you know and you kind of compose
00:05:13.800
these components so you combine them
00:05:15.720
into bigger and bigger structures into
00:05:17.460
screens pages and then eventually apps
00:05:19.560
okay so you have this little Lego
00:05:21.180
building block that you compose compose
00:05:23.039
compose compose and then all of a sudden
00:05:24.840
you have Netflix okay and here's an
00:05:27.660
example of a component just being a
00:05:29.580
function and I think also this is why
00:05:32.280
it's important to understand
00:05:34.940
JavaScript really well before you dive
00:05:37.020
into react because react relies so
00:05:40.500
heavily on JavaScript it's such a thin
00:05:42.060
abstraction that for example over here
00:05:44.220
you probably seen that I actually write
00:05:46.680
my components like this purely just a
00:05:50.039
stylistic you know uh so I this is I
00:05:53.340
just prefer Arrow functions so if you
00:05:55.320
didn't understand like the different
00:05:57.120
types of functions in JavaScript you
00:05:58.919
might be like okay why why is he writing
00:06:01.620
his code like this but in the example
00:06:03.300
it's like this and so forth if you don't
00:06:05.699
understand JavaScript like pretty well
00:06:07.500
and you don't actually understand the
00:06:09.000
JavaScript part and you think all of
00:06:10.860
this is just react specific you know
00:06:12.780
this is oh react syntax you're going to
00:06:15.000
get confused because you can see a lot
00:06:16.500
of different ways of doing the same
00:06:18.060
thing and if you aren't able to separate
00:06:20.460
the part that's react and the part from
00:06:22.080
the part that's JavaScript like things
00:06:23.759
are going to get really confusing
00:06:24.840
because you might work on a project that
00:06:26.520
does it this way you might work on a
00:06:28.139
project that does it this way like
00:06:30.120
because these are just functions you can
00:06:31.860
effectively do anything with it you can
00:06:33.419
even like go you know for example const
00:06:36.419
components and put them actually in an
00:06:39.539
object and go you know like video and
00:06:41.880
then you have your component there and
00:06:44.220
something else you know text and have
00:06:46.380
you so these are literally just
00:06:47.940
functions that you can move around and
00:06:49.440
so forth and if you don't understand
00:06:51.120
this things are going to get very
00:06:52.800
complicated and like you're going to
00:06:54.479
like look at different projects you're
00:06:56.039
not going to know okay why why is it so
00:06:59.280
different okay so here's a basic example
00:07:01.560
of this and what they also mention is
00:07:03.960
that you know custom components are
00:07:05.699
indicated by Pascal case so in other
00:07:07.919
words Pascal case meaning that it starts
00:07:09.780
with the uppercase letter regular Dom
00:07:12.060
elements are just indicated with
00:07:13.979
lowercase yes to end uh sorry Scott just
00:07:16.560
on that where you had const components
00:07:19.259
um you know when you import something
00:07:21.180
and it's in curly braces is it the same
00:07:23.639
idea uh you mean like for example if I
00:07:26.759
go import or react from react versus
00:07:30.500
import and use state from reacting this
00:07:33.960
so effectively this is a named export so
00:07:37.740
react effectively has a entry file so
00:07:40.500
when you install it via like npm let me
00:07:43.139
show you there should be a react folder
00:07:45.180
here there we go and in that is a
00:07:47.720
index.js file this is literally what it
00:07:49.979
explains okay so you can go a bit deeper
00:07:52.020
into this and so forth and so forth and
00:07:54.240
that just depends on how it gets
00:07:56.220
exported if you let's say we have our
00:07:58.440
actual file up here let's also just say
00:08:00.419
you know this is file a file hello so by
00:08:03.840
default anything that you prefix of
00:08:05.880
export is going to be exported so you
00:08:08.520
know there needs to be like a use state
00:08:10.020
or whatever theoretically if you want
00:08:13.080
all the named exports together just so
00:08:15.960
you know text or whatever is you know
00:08:18.060
one two three if you want all the named
00:08:20.039
exports together uh you would actually
00:08:22.620
you know start with asterisks and like
00:08:25.979
that and then it grabs all of these and
00:08:28.199
put them for you in an object but
00:08:30.419
generally most libraries actually have a
00:08:33.599
default export that where they export
00:08:35.640
all the named exports as as an actual
00:08:38.760
object so they would go you know default
00:08:40.620
and then they would just actually put
00:08:42.779
all the things in there but this isn't a
00:08:44.760
given so effectively like whether it
00:08:47.160
follows close the structure where the
00:08:49.500
default export is an object of all the
00:08:52.140
named exports is you know whoever
00:08:54.240
created the file or the package or
00:08:56.220
whatever for their own discretion you
00:08:58.440
know you can very well just go and say
00:09:00.360
the default export is test or the
00:09:02.459
default export is you know something
00:09:03.899
that isn't any of these things okay this
00:09:07.140
is a general convention uh that like
00:09:10.019
developers follow is that then the
00:09:11.940
assumption would be that you can do
00:09:13.740
react to use State okay but it's not a
00:09:15.899
given it's not enforced here's just a
00:09:17.880
basic example you guys know
00:09:19.500
destructuring so yes it's destructuring
00:09:21.720
the props whether you work on your own
00:09:23.519
or thousands of developers okay call
00:09:25.620
some marketing stuff so yeah effectively
00:09:28.140
react components are just functions I
00:09:30.180
want to show some content conditionally
00:09:32.040
use an if statement so you can
00:09:33.899
effectively do the following let's say
00:09:35.820
we have button uh so the props for that
00:09:38.279
button and you'll also see that one
00:09:40.080
thing that I do is I don't destructure
00:09:42.480
directly in here like they do so you'll
00:09:45.420
see there they just destructure their
00:09:47.100
property directly the reason why I don't
00:09:49.260
do this is because this can start
00:09:51.300
getting very unwieldy and then you
00:09:53.519
actually specifically if you're using
00:09:55.080
something like protea then it kind of
00:09:57.120
starts like doing this and I'm not a big
00:09:59.760
fan of like having the actual closing
00:10:03.779
part of the function or the the
00:10:06.360
parameters part of the function so far
00:10:08.760
away from like I prefer to have both of
00:10:11.820
these brackets on the same line so
00:10:14.100
that's why I usually just do this and
00:10:16.380
then rather if it gets long I do it like
00:10:19.019
that in here because then at the very
00:10:20.399
least I can still at a glance see this
00:10:22.080
is a function I'm not a big fan of this
00:10:24.240
type of thing where it kind of goes
00:10:25.920
across several lines let's say there's
00:10:28.440
something like disabled or whatever and
00:10:31.019
you can actually have if statements in
00:10:32.820
your function because once again it's
00:10:34.440
like in your component because it's just
00:10:35.700
a function so you can go you know if
00:10:37.800
disabled then just return Dove you know
00:10:40.920
one two three or whatever by definition
00:10:42.660
the next slide because if it reaches
00:10:45.240
this line you can assume that it's not
00:10:46.860
disabled old because this would have run
00:10:48.660
and it would have returned then you can
00:10:50.640
like just return you know let's say of
00:10:52.620
can even return null okay so most
00:10:55.380
functions return jsx or null so you can
00:10:59.220
actually return null as well which means
00:11:01.019
it's not going to render anything then
00:11:02.640
you know if you have for example div and
00:11:04.800
you have button you know it is disabled
00:11:06.959
then it's effectively as if there's
00:11:08.880
nothing there so you can return null as
00:11:11.820
well yeah so effective it says yeah and
00:11:13.680
you know like you can use array map so
00:11:15.600
as just mentioned this is you know
00:11:17.279
something that's maybe a bit hard to get
00:11:18.959
your head around if you tend to think in
00:11:20.940
terms of Loops but if you understand it
00:11:23.760
and if you get good at it it's much more
00:11:25.320
readable than Loops so down here they
00:11:27.540
have another example and I think what's
00:11:29.279
what's cool here is they kind of show
00:11:30.779
they do all the logic up here and then
00:11:33.540
after they've calculated everything then
00:11:35.579
they spit out the the kind of the jsx so
00:11:38.940
you can obviously have regular
00:11:40.320
JavaScript logic in here as well you
00:11:42.660
know because a function is just
00:11:43.800
something that resolves and spits
00:11:45.779
something out I wouldn't recommend this
00:11:47.519
uh because what you generally want is
00:11:49.320
you generally want your functions to be
00:11:51.180
as pure as possible in other words given
00:11:54.240
the same props it always returns the
00:11:56.100
same thing but you can even do something
00:11:57.959
like random you know and then math
00:11:59.459
random and then you know just spit that
00:12:02.399
out anyone want to take a guess at why
00:12:05.279
this is extremely problematic doing this
00:12:07.800
bonus points come on because it's always
00:12:10.260
going to return a completely different
00:12:12.120
virtual Dom so it's always going to
00:12:14.220
re-render because every time it runs
00:12:16.680
because we have like a side effect in
00:12:18.660
here it's it's just going to keep on
00:12:20.399
re-rendering every time so obviously you
00:12:22.680
want your functions to be as pure as
00:12:24.300
possible so that when you pass the same
00:12:26.399
stuff it always returns the same stuff
00:12:28.140
meaning that no Dom updates happen but
00:12:30.660
you can do any logic in here you know
00:12:32.640
you can you know save to local storage
00:12:34.380
you can get from local storage
00:12:36.899
um yeah this is just plain JavaScript
00:12:38.519
effectively if you return null then
00:12:40.800
there's actually no jsx there's no react
00:12:42.839
to anything in here this is just a
00:12:44.279
function that does some stuff okay so
00:12:46.500
like it's important to to keep your kind
00:12:49.139
of eyes on this idea of components are
00:12:51.660
just functions they're functions that
00:12:53.040
run that spit out a piece of virtual Dom
00:12:56.040
and that is just compared about what
00:12:57.779
what it spit out previously and it just
00:13:00.060
does a comparison to check okay is it
00:13:01.680
different this time you can actually and
00:13:03.959
because of this you can't theoretically
00:13:05.639
write this code as follows you can go
00:13:07.920
you know cons let's say video list if
00:13:10.680
you really want to you can say you know
00:13:12.839
can't videos whatever and let's just
00:13:15.720
destructure let's just say list you can
00:13:18.600
do something like this you know for and
00:13:21.120
then you can go for const uh single of
00:13:25.620
videos push it into the list and you
00:13:28.920
know like then create create your jsx
00:13:31.320
there and because jsx is just once again
00:13:34.260
it's a function that when you create it
00:13:36.899
it creates an element it creates an
00:13:38.700
object you can do this and then just you
00:13:41.279
know render the list but I think it's
00:13:43.740
important to rather rely that the
00:13:46.320
general best practice in react is to
00:13:48.420
rather rely on mapping because mapping
00:13:52.019
is a lot more declarative because if
00:13:54.000
you're reading this you're like okay
00:13:55.019
cool there's an array and okay cool oh
00:13:57.240
something happens here oh it pushes that
00:13:59.279
back up there
00:14:00.779
um oh okay cool cool cool cool and then
00:14:03.180
down here oh okay so you're you're
00:14:04.860
jumping around all the time whereas if
00:14:07.320
you just do this so you can't even
00:14:09.420
resolve it up here if you're fine if you
00:14:11.700
find that easier to read so you do
00:14:13.500
videos map and let's just do single and
00:14:16.620
uh let's do it like that you don't even
00:14:19.079
need these brackets you can just go like
00:14:20.700
that this is a lot more declarative she
00:14:23.160
and Lee would probably actually do this
00:14:25.019
there you go I might even just bump it
00:14:27.000
down to the next line so this is a lot
00:14:29.160
more declarative it might seem like oh
00:14:31.260
my eyes are just like going cross-eyed
00:14:33.540
like I can I can't read what's going on
00:14:35.100
here and that's just because you're not
00:14:36.540
used to it it's just it's just a matter
00:14:38.519
of what you're used to you're maybe not
00:14:41.339
used to actually reading stuff in such a
00:14:44.040
declarative manner but you can imagine
00:14:45.779
if you are then this is a lot more
00:14:48.120
information to process as opposed to
00:14:50.040
this so that's why things like map and
00:14:52.199
so forth are generally preferred yeah so
00:14:54.480
just talks here about jsx it's a syntax
00:14:57.600
extension so we also spoke about that a
00:15:00.420
bit it's not it's not a template uh so a
00:15:03.720
syntax extension so I think it's
00:15:05.820
actually JavaScript syntax extension I
00:15:08.459
think that's actually what J is X extend
00:15:11.880
oh I can't spell extension I think
00:15:14.880
that's actually what jsx actually stands
00:15:17.100
for if I'm not mistaken so it's an
00:15:19.680
extension of JavaScript syntax and why
00:15:22.440
is it important that note that jsx is
00:15:24.959
not a templating language because in
00:15:27.060
templating languages things are treated
00:15:29.339
as a string so in other words in a
00:15:31.920
templating language if this was a
00:15:33.480
templating language first of all you'd
00:15:35.639
probably have to return this as a string
00:15:37.320
okay so something like that and
00:15:39.600
generally you would have something
00:15:41.579
you'll see this in like things like
00:15:43.680
svelp in things like view you'd probably
00:15:45.839
have something like Loop over videos and
00:15:49.860
then you know in bloop or whatever and
00:15:53.040
then you know you have whatever in there
00:15:56.040
so it's a string that has instructions
00:15:58.620
so you can't move things around there's
00:16:01.199
value in terms of that there's only one
00:16:03.000
way to do something but like there's a
00:16:05.519
lot of flexibility in treating it as
00:16:07.380
this plain JavaScript and not some
00:16:09.000
special reacting because now you can use
00:16:11.699
both in JavaScript things like mapping
00:16:13.800
for Loops filter reduce all that stuff
00:16:16.079
to actually modify what gets spit out
00:16:18.779
instead of actually describing it with
00:16:20.940
the templating language so temporary
00:16:22.500
language is much more limited but it is
00:16:24.779
important to understand that it's not a
00:16:26.279
templating language a templating
00:16:27.480
language is let me show you an example
00:16:29.639
so a pretty well known temporary
00:16:31.740
language is something like handlebars
00:16:33.720
which some of these Frameworks once
00:16:35.579
again like view or whatever based on uh
00:16:38.880
svelt's ball so you do like each to Loop
00:16:42.000
but that means like you need to use the
00:16:44.160
templating language itself to do these
00:16:46.139
things in react you can do it and react
00:16:48.660
itself and then pass it to jsx okay this
00:16:51.720
sounds like a very pedantic distinction
00:16:54.480
and if you don't see the value in
00:16:56.759
understanding these differences at the
00:16:58.620
moment that's fine like at some point
00:17:00.480
it's going to click and you're going to
00:17:01.560
be like wow this is why jsx is so
00:17:03.959
powerful it's so actual powerful because
00:17:06.119
once again you know if you do this like
00:17:08.400
it's going to be very hard to build like
00:17:10.079
native apps and stuff because you
00:17:12.240
actually this is built with a specific
00:17:14.579
use case in mind whereas if you kind of
00:17:17.220
just use plain JavaScript to arrange the
00:17:19.679
things that get spit out now you can
00:17:21.419
apply to anything you can apply to
00:17:22.799
Native apps VR whatever and it doesn't
00:17:24.959
even have to be something visual you can
00:17:26.699
build like people do weird things where
00:17:28.260
they like actually create music with
00:17:30.059
react and whatever and they just because
00:17:31.620
these are just functions that run okay
00:17:33.799
components just receive data and they
00:17:36.840
return what should be on the screen as
00:17:38.640
simple as that you can pass them new
00:17:40.679
data in response to interaction
00:17:43.140
um and then react will update a screen
00:17:45.000
okay and so yeah they use the use state
00:17:47.280
so you use State we covered this last
00:17:49.799
time this actually just tells the
00:17:51.840
interface to actually compare the new
00:17:54.240
version of the the virtual Dom to the
00:17:56.220
old version okay yeah and here they're
00:17:58.679
just actually show an example I am going
00:18:01.380
to talk a little bit about next and
00:18:03.900
remix there's another one there's a
00:18:05.760
couple of these there's like Gatsby as
00:18:08.280
well there's uh one I think called Blitz
00:18:10.919
there's Redwood a lot of some other ones
00:18:13.559
so let's just look at some of these
00:18:16.320
um so the big one is next year is
00:18:18.120
chances are if you're going to work on a
00:18:20.400
react project you are actually going to
00:18:23.880
be using the xjs but there are a couple
00:18:26.220
of other ones so Gatsby not not Gatsby
00:18:30.179
sandwich SP JavaScript framework these
00:18:33.960
are and and so you might have heard
00:18:35.820
people say react as a library not a
00:18:38.220
framework I've just resigned to calling
00:18:40.500
it a framework because I'm just tired of
00:18:42.419
having that discussion there's value in
00:18:44.400
just saying okay these things are
00:18:46.020
somewhat kind of alike but react is
00:18:49.320
unique and so far that react doesn't
00:18:51.660
actually make assumptions about where it
00:18:53.640
gets run it it doesn't even know that
00:18:55.860
you're going to use it with the Dom it
00:18:57.059
doesn't even know that there is
00:18:58.200
something like a URL you need to pull in
00:19:00.539
react Dom so because of that the
00:19:03.360
trade-off of this com this this
00:19:05.220
flexibility that react gives us we
00:19:08.460
actually one of the drawbacks is that
00:19:11.280
doesn't have things like a router and so
00:19:13.679
forth you know it doesn't have an easy
00:19:15.660
way to map pages to like actual pieces
00:19:19.080
of data so there are a couple of
00:19:21.780
third-party ones the big one is react
00:19:23.520
router and another one that is one
00:19:25.919
called uh is it react location by
00:19:28.500
Lindsay Tanner who does a lot of really
00:19:30.660
cool like react stuff yeah so react
00:19:32.760
location these are all third party they
00:19:35.280
have no affiliation to the react team
00:19:37.620
itself then I spoke about you know like
00:19:39.600
Redux and Zoo stand and then there are
00:19:42.299
things like server side rendering
00:19:44.120
optimizations of images and stuff so
00:19:47.100
what do is meta frame actually for
00:19:49.200
example next they're all kind of thing
00:19:51.120
on their own they're third party they're
00:19:52.799
not specific they're not maintained by
00:19:54.539
the react team they take react and then
00:19:57.360
they build out all these kind of broad
00:20:00.419
level things so it's another abstraction
00:20:02.940
on top of react and these are usually
00:20:04.860
called meta Frameworks you know so it
00:20:07.020
allows you to do like routing middleware
00:20:09.419
you know fetch your data and and all of
00:20:12.240
that but because of the scope of what
00:20:15.360
we're covering we're not going to go
00:20:16.740
into next unfortunately there is a time
00:20:18.900
to go into like a lot of these things
00:20:21.360
because it requires us to understand a
00:20:23.340
bit like our databases and stuff work as
00:20:25.320
well this shouldn't be that much of an
00:20:28.620
issue because once again what I'm
00:20:30.000
teaching you guys is I'm teaching you
00:20:31.500
how to read documentation you know so
00:20:33.600
you should be able to just read this and
00:20:35.280
kind of get an understanding of cool
00:20:37.320
installation okay project structure and
00:20:40.380
so forth and so forth they talk about
00:20:42.240
this a bit here you know as as mentioned
00:20:44.640
you know like make it known that her act
00:20:46.559
as a library and put your components
00:20:48.600
together but it doesn't prescribe how to
00:20:50.400
do routing and data fetching okay a lot
00:20:53.400
of people don't like this this is kind
00:20:55.919
of the flexibility that makes react so
00:20:58.200
popular because it doesn't prescribe
00:21:00.539
these things but it makes it harder to
00:21:02.700
use react because now you need to figure
00:21:04.320
all of that out so next is like a hybrid
00:21:07.020
of reactor node basically in a way not
00:21:10.500
necessarily you can do a couple of
00:21:12.299
things it allows you to run react on a
00:21:15.299
server let me think of an example that
00:21:17.340
actually I think I'm pretty sure Airbnb
00:21:19.500
does it so when I'm actually going to
00:21:22.440
Airbnb I'm actually hitting a server and
00:21:25.200
some stuff happens on the server and
00:21:26.700
then it returns something back for me so
00:21:28.919
some of the stuff that it's shown here
00:21:31.080
gets created in react it gets computated
00:21:33.780
on the server and sent back to me which
00:21:36.120
means that things load incrementally
00:21:38.880
um I don't look at a white page well the
00:21:41.159
JavaScript loads and then you know the
00:21:43.080
JavaScript comes in I think like this is
00:21:45.240
a bit way too advanced for you guys uh
00:21:48.299
if you end up actually using some
00:21:50.100
something like next you're probably
00:21:51.960
going to be using so in next there is
00:21:54.600
it's static data I think get static
00:21:57.419
props can build a lot of the stuff
00:21:59.520
statically as well so next also spits up
00:22:02.100
like HTML and whatever for you it does
00:22:04.559
allow you to actually run react on a
00:22:06.780
server but if you actually want to
00:22:08.700
compile all your react files beforehand
00:22:10.679
it also gives you some useful tools
00:22:12.600
something like Gatsby only does like
00:22:15.419
compilation before time so you can't
00:22:17.820
actually run Gatsby on a server so it's
00:22:19.860
a meta framework that actually just
00:22:21.539
allows you to build a lot of these
00:22:23.520
things beforehand and it spits out HTML
00:22:25.440
CSS and JavaScript and you can push it
00:22:27.299
up to like netlify or whatever it was
00:22:29.460
actually purchased by netlifier a while
00:22:31.559
ago but yeah I'm not going to go too
00:22:33.120
much into these meta Frameworks but
00:22:35.280
chances are that you if you join a team
00:22:38.039
chances are you you're probably going to
00:22:39.840
work with them but you're not gonna have
00:22:41.640
to set up like the databases and stuff
00:22:43.679
because there's probably some lead
00:22:45.059
engineer who did that already but just
00:22:47.280
under stand that a lot of these use
00:22:50.220
react so you might advertise yourself as
00:22:52.559
a react developer and you might get
00:22:53.760
hired and it's like oh we use Redwood
00:22:55.860
and you're like no no I I use react I I
00:22:58.260
don't I don't know how to use remix or
00:23:00.179
whatever but it's just it's a meta
00:23:01.559
framework that just extends in the same
00:23:04.260
way that react extends JavaScript these
00:23:07.080
just take react and build out a lot of
00:23:09.059
extra things so it abstracts even more
00:23:11.580
stuff for you so he had to actually use
00:23:13.380
an example where you know you pull in a
00:23:15.299
database you get information from a
00:23:17.220
database and so forth
00:23:19.500
um so yeah to asynchronously load stuff
00:23:21.900
okay it's actually interesting I think
00:23:25.740
pretty Advanced it's interesting I think
00:23:28.320
they just put it on the home page as to
00:23:31.020
show you hey like this is how deep you
00:23:33.179
can go if react but like I actually
00:23:35.460
don't think you guys are going to be
00:23:37.320
doing this type of thing anytime soon
00:23:38.940
well unless you kind of do a bit of
00:23:40.620
extra reading and research yourself it's
00:23:43.380
a bit deceiving that it's so high up
00:23:45.480
because if you go through the
00:23:47.039
documentation it's a very long time
00:23:48.539
before you get to stuff like that it
00:23:50.580
says you know react is also an
00:23:52.260
architecture Frameworks that implemented
00:23:54.299
like you fetch data have components that
00:23:56.820
run on the server or during bold and so
00:23:59.400
forth and so forth you know so get
00:24:01.320
started with the framework so this is if
00:24:03.299
you want to use a framework I think at
00:24:05.460
this point where you guys are something
00:24:07.020
like Vita spine so yeah just also
00:24:09.539
mentions that you can build a web and
00:24:10.919
Native app apps again here's just like
00:24:13.140
how many people are using react and
00:24:15.179
whatever whatever