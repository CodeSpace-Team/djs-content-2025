00:00:00.000
what we do here is we are going to
00:00:03.240
return this unsubscribe so what does
00:00:05.640
unsubscribe do unsubscribe because
00:00:08.220
remember a function this is a reference
00:00:10.380
so it actually still has reference to
00:00:12.599
this so what we can do and here I'm
00:00:15.299
actually going to use a higher order
00:00:16.680
function you are not necessarily going
00:00:18.420
to understand 100 what it does right now
00:00:20.699
but I am going to explain it it is part
00:00:23.340
of functional programming high order
00:00:25.320
functions are a big part of functional
00:00:27.060
programming so you would think about
00:00:28.920
maybe doing this with a loop and then
00:00:30.900
looping over and removing the actual
00:00:33.120
notification itself what you can
00:00:35.280
actually do following the rules of
00:00:37.500
functional programming is create a new
00:00:40.079
notifiers where that actual notification
00:00:43.620
has been removed and this is possible
00:00:45.660
because remember this keeps references
00:00:48.000
it's not putting the actual functions in
00:00:50.039
it so we can just move the references to
00:00:52.200
a new array so how would we do this so
00:00:54.780
let's just in here say answer the result
00:00:57.059
and notifiers filter okay so we want to
00:01:01.199
create the filter creates a new let me
00:01:04.379
just switch off Copart it actually wants
00:01:05.880
to write that code for me so I can't
00:01:07.560
explain it dot filter so what we're
00:01:09.360
doing is we're running filter on this
00:01:11.220
array so you can think back to when we
00:01:13.200
spoke about arrays and mutating arrays
00:01:15.180
and splice and slice and pop and push
00:01:18.299
and all of those things and I said you
00:01:20.460
know there's a there's a lot of other
00:01:21.840
higher order functions that we're going
00:01:23.400
to talk about about like when we come
00:01:25.320
back to arrays and this is one you know
00:01:27.479
it's a filter so you pass a function to
00:01:29.580
filter so let's just say Handler and so
00:01:32.700
what Handler does it takes the current
00:01:35.060
notification and it just checks is the
00:01:39.000
current notification not the same as
00:01:42.299
notify so the one that was passed up
00:01:44.400
here originally if it is not the same
00:01:46.619
then this is true meaning that it
00:01:48.360
shouldn't filter it it's only going to
00:01:50.520
remove it from the new array if this is
00:01:54.240
not true in other words if it actually
00:01:55.619
matches so if we then pass our Handler
00:01:57.960
in there then this is going to run
00:02:00.000
button and result is just going to be
00:02:01.979
the new subscribe with the let's do
00:02:05.520
notifications notifiers and result okay
00:02:08.699
so just the new ones right so there's
00:02:10.860
our logic and you might be like okay but
00:02:13.080
why are you passing this why aren't you
00:02:14.520
creating a new function that is just
00:02:17.819
unsubscribe and and the reason for that
00:02:19.800
is because we actually have the
00:02:21.780
reference right in here so why not just
00:02:24.300
give a function back that allows a with
00:02:26.520
a reference built in and we don't need
00:02:28.260
to find the thing again from scratch
00:02:30.480
okay but so then obviously we're not
00:02:32.760
notifying at the moment so what we want
00:02:35.040
to do is in here and we're going to use
00:02:38.040
another higher order function we want to
00:02:40.260
go nodifiers
00:02:42.540
four each okay so we want to run a
00:02:45.300
function on each Notifier and once again
00:02:48.060
this is to replace a loop it's just a
00:02:50.280
much more elegant expressive way to
00:02:52.500
write that logic compared to a loop it
00:02:54.840
might not feel that way to you right now
00:02:56.640
because you're so used to Loops but once
00:02:59.519
you understand this concept and that is
00:03:01.680
sometimes a hard concept to get your
00:03:02.940
head around but once you understand this
00:03:04.980
concept like code is going to become
00:03:07.140
much more declarative what is the
00:03:09.239
Handler that we pass to that so
00:03:10.920
effectively it should just take the
00:03:13.800
actual notify in our notifiers and to
00:03:17.819
run it with previous and next like that
00:03:21.659
and then we just pass that Handler so
00:03:23.580
it's taking that function and it's
00:03:24.959
looping over every single item and then
00:03:28.500
once it's done running this it finally
00:03:31.500
if there's no error from any of the side
00:03:33.780
effects then it actually merges it into
00:03:36.120
the new state in less than 100 lines we
00:03:39.540
have created something really powerful
00:03:42.239
and you can see how powerful that is
00:03:43.980
right now and this is the beauty of
00:03:45.959
functional programming and why I like
00:03:47.519
functional programming so much if you're
00:03:49.739
really clever you can express really
00:03:52.500
powerful things in very simple manner
00:03:55.019
you know so you can think again about
00:03:56.640
like you know E equals m c Square to me
00:03:59.819
functional programming is the Pinnacle
00:04:01.620
of abstraction it's abstraction in its
00:04:03.959
greatest form okay and this is the
00:04:06.239
reason why I said to you guys up front
00:04:07.739
that I'm a big fan of functional
00:04:09.420
programming I really enjoy working a
00:04:11.280
functional programming because from here
00:04:13.620
on out I'm just going to tell you how
00:04:15.180
amazing functional programming is and if
00:04:17.519
you don't like functional programming
00:04:18.899
time to buckle up like this is going to
00:04:21.418
be a tough one for you but my hope is
00:04:23.639
that you actually also develop an
00:04:25.680
appreciation for like how expressive
00:04:29.280
functional programming can be all right
00:04:31.259
so let's use the store first of all
00:04:33.000
let's see if it actually works so let's
00:04:35.699
pull it into our scripts here the only
00:04:37.740
things that we expose from our store is
00:04:39.960
so these are all types but in terms of
00:04:42.300
actual we just have update and we have
00:04:44.040
subscribe and let's pull in our scripts
00:04:47.340
over here so refer and type module so
00:04:51.000
this is going to return unsubscribe so
00:04:52.919
let's just subscribe the following so
00:04:54.960
let's just say ref and next let's just
00:04:57.479
also say Handler so brief and next and
00:05:00.360
let's just console log refund next okay
00:05:02.940
so let's just console log that whenever
00:05:04.740
anything in the store changes and we're
00:05:07.139
not going to unsubscribe it just yet so
00:05:09.120
let's update a couple of things so let's
00:05:11.280
do update so we can pull in any of these
00:05:13.740
actions but let's write our own action
00:05:16.139
in here so update
00:05:18.240
should be bringing in GIS dock let's see
00:05:21.960
what's wrong so subscribe never marked
00:05:23.880
it up over here okay so action there we
00:05:26.820
go and we can write a bit of a
00:05:28.080
description here I'm not going to do
00:05:30.120
that right now over here all this is
00:05:32.940
this is just an empty function so we can
00:05:35.280
just create that again it's effectively
00:05:37.979
just a callback with nothing let's just
00:05:39.900
call it MP FN so it should be typed up
00:05:42.840
now sir hey there we go so update uh
00:05:46.919
let's just do custom action and let's
00:05:50.100
actually pull in the types for action
00:05:52.500
and if you remember correctly the way
00:05:55.380
you would do that is you would just give
00:05:58.380
it a empty and the fact that it is uh
00:06:02.220
written like that to me is clear that
00:06:04.199
it's an actual type so what I can then
00:06:06.660
do here is I can do and do param or type
00:06:10.560
actually action okay now it's going to
00:06:12.120
just give me some type so we need to
00:06:14.039
return something new so let's destruct a
00:06:17.880
state in our action and let's do wind
00:06:21.500
countless destruction State wind in that
00:06:24.360
as well so we're effectively recreating
00:06:27.000
the object so the reason why I'm doing
00:06:28.860
this is because obviously now if you do
00:06:30.780
this it's going to override when with
00:06:32.400
just an empty object so we de-structure
00:06:35.039
what's currently inside wind in this
00:06:37.440
object as well and then we can do value
00:06:39.840
State Value Plus let's go 19. if we
00:06:43.860
let's run this update three times and
00:06:46.919
let's see what happens in our code and
00:06:49.139
oh I needed to say store.js so every
00:06:52.380
time we update it it actually gives us
00:06:54.720
the previous store and the next door and
00:06:57.240
it is not a number why is it not a
00:06:59.220
number so value so over here so this is
00:07:01.919
also cool so we can actually follow and
00:07:03.720
see where the error happened because and
00:07:05.639
this is also why you get a lot of like
00:07:07.020
Dev tools you get like Redux Dev tools
00:07:09.900
and so for for example stores and
00:07:12.600
whatever and so it actually allows you
00:07:14.580
to actually see like what changed time
00:07:18.900
to do at this check because that would
00:07:21.720
have told me ha okay that would have
00:07:23.580
told me like this doesn't exist I need
00:07:25.440
to go wind value there we go all right
00:07:27.840
so let's check now so so you can see
00:07:31.139
what changed um so let's actually after
00:07:33.599
we do it once uh let's unsubscribe it
00:07:36.660
will actually stop sharing this to us
00:07:39.419
because then nothing is subscribed to
00:07:41.759
that
00:07:43.020
um so it'll just show once and then we
00:07:44.759
unsubscribe it cool and the others fire
00:07:46.860
without anything listening to it
00:07:49.560
um but so what we probably want to do is
00:07:51.599
let's add another subscription and what
00:07:54.900
we probably want to do is what we can do
00:07:56.580
is let's say we want to listen for when
00:08:00.360
the wind actually updates and then we
00:08:02.880
want to like change a number on the Dom
00:08:05.580
so let's create another Handler and
00:08:08.520
generally you actually and this is also
00:08:10.979
why you kind of generally create actions
00:08:13.020
and you import them instead of declare
00:08:15.120
but you can write them right in here so
00:08:17.220
let's just do another one and as with
00:08:19.020
event listeners you obviously need to
00:08:20.340
register them up front otherwise they're
00:08:23.160
not going to get triggered they're only
00:08:24.720
going to get triggered once they are
00:08:26.039
registered let's just say let's call it
00:08:27.840
HTML Handler and I can even then pull in
00:08:31.440
notify so if I do the same here uh node
00:08:35.159
to buy okay that's just going to give me
00:08:37.080
a bit of type safety and let's just say
00:08:39.179
type is notify and so what notified does
00:08:42.719
notify so actually you can see next
00:08:45.480
state and previous state oh we actually
00:08:47.040
got it the other way around actually
00:08:48.660
wondering whether we get it right in our
00:08:51.480
actual app no actually got it wrong in
00:08:53.100
our app so the reason why I do it this
00:08:54.899
way around is because sometimes you just
00:08:56.279
care about the next state you actually
00:08:57.839
don't care about the previous state but
00:08:59.760
you can do it any way you want uh so
00:09:02.279
let's just get next and so all we want
00:09:05.459
to do is we want to check is previous
00:09:07.880
wind value not the same as next wind
00:09:12.060
value in other words did a change and if
00:09:14.700
it didn't if it didn't change so
00:09:16.500
actually sorry if it is the same then
00:09:18.720
just return don't do anything otherwise
00:09:20.339
we can assume it changed and what you do
00:09:22.620
is you do document body
00:09:25.260
um let's just say append tiled and let's
00:09:28.320
just create a Dev honest and let's just
00:09:31.560
say Dev document create element div and
00:09:36.360
put that in there but what we want to do
00:09:38.519
is div in a text is just the new is next
00:09:43.200
wind value okay and this is unhappy
00:09:47.640
because now number is not okay we just
00:09:50.519
need to do through string so you don't
00:09:52.260
even have to grab the unsubscribe you
00:09:54.660
can just say I'm never going to
00:09:56.100
unsubscribe this so I'm just going to
00:09:57.660
leave that and I'm just going to pass
00:09:59.040
that I don't care about the function
00:10:01.140
that allows me to unsubscribe it and
00:10:03.300
here we go there it goes 20 39 58 and
00:10:07.680
just to show this principle let's say if
00:10:10.680
we actually listen for then it's not
00:10:13.560
going to do anything because temperature
00:10:14.880
never actually changes here we go just a
00:10:17.459
blank screen so you can listen for
00:10:19.200
specific changes in your store but
00:10:21.120
what's really cool is the way you update
00:10:23.339
your store is completely functional
00:10:25.500
there are no side effects and why this
00:10:28.260
is really helpful is it's super easy to
00:10:31.680
test and we're going to do test driven
00:10:33.839
development at a later lesson but you
00:10:35.760
can effectively if you want to check
00:10:37.260
does increase actually work correctly
00:10:39.240
you can actually just take these
00:10:41.459
functions as just functions on their own
00:10:43.440
and just pass a state and check if it
00:10:46.140
Returns the new state so check if it
00:10:48.180
adds one and so forth and stuff well
00:10:50.279
obviously these are going to work
00:10:51.420
because we actually need to go like wind
00:10:53.519
and all of that when I created these
00:10:56.100
there was only one single thing so
00:10:58.200
here's where it gets really cool so I'm
00:11:00.480
just going to create a super simple
00:11:02.279
version of art to do app to show you
00:11:04.860
what problems this uh Global store
00:11:08.339
pattern solves for us and these are
00:11:11.519
basically something called prop Drilling
00:11:14.160
and the other one is related to actually
00:11:17.519
serializing the state of your app okay
00:11:19.800
so those those sound really scary I'm
00:11:21.720
gonna unpack about what they mean and
00:11:23.700
it's also worth saying that it is very
00:11:26.160
possible to build an app without having
00:11:28.560
a global State Management solution like
00:11:30.959
a store but at some point most apps
00:11:33.959
reach enough complexity where you need
00:11:36.720
to pull something like this in and most
00:11:39.300
JavaScript Frameworks either have an
00:11:41.399
explicit store that is built into the
00:11:43.740
framework so for example xfeld Alpine
00:11:46.380
also has one and then others have
00:11:48.779
implicit stores so I mentioned in react
00:11:51.480
you get uh Redux there's also mobx
00:11:54.779
there's Zoo stand and in view there's
00:11:58.019
view X but the the kind of new favorite
00:12:00.540
is pinia and all of these have different
00:12:02.880
takes on them but so what I'm gonna do
00:12:05.459
here is I'm gonna kind of follow the
00:12:07.140
Redux approach which was one of the very
00:12:09.360
first libraries that provided us with
00:12:12.240
this so I personally don't use Redux I
00:12:15.120
use something called Zoo stand I did
00:12:17.160
cover it a bit when I talked about
00:12:18.720
markdown files and documentation
00:12:21.120
um I personally prefer it because it is
00:12:23.040
a bit lower level than Redux um it
00:12:25.500
allows you to get a bit closer to the
00:12:27.420
metal and really configure it in a way
00:12:29.519
that you want allowing you to do things
00:12:31.740
like dependency injections and so forth
00:12:33.959
we will cover this when we get to
00:12:37.440
JavaScript Frameworks it's useful to
00:12:40.079
maybe take a Redux approach right now
00:12:42.060
purely because regardless of my personal
00:12:44.339
preferences most react projects out
00:12:47.040
there actually use Redux and also what's
00:12:49.560
very nice about Redux is Redux is Redux
00:12:52.680
is a very functional programming based
00:12:55.500
approach so it's also a good intro for
00:12:58.200
us into functional programming whereas
00:13:00.420
some other Solutions like mob X and so
00:13:02.760
forth tend to mix functional programming
00:13:04.980
and other approaches a bit so I just
00:13:07.079
wanted to kind of mention that so you'll
00:13:09.360
see even on npm there is about almost 8
00:13:12.180
million installations so Redux is still
00:13:14.459
immensely popular compared to something
00:13:16.620
like Zoo stand which is getting there
00:13:18.480
you know 1.3 million but nowhere near
00:13:20.820
the scale of Redux let me open a fig Jam
00:13:23.820
file and I let me explain how Redux
00:13:26.519
works and also why Redux lean so heavily
00:13:30.360
on a functional programming Paradigm so
00:13:32.760
it's very similar to that little store
00:13:34.740
example that we created right now so I
00:13:37.440
just wanted to show you the the actual
00:13:39.839
underlying JavaScript principles before
00:13:42.540
we get bogged down in redux's specific
00:13:45.120
approach but I think Redux has a very
00:13:48.300
nice surprise approach so there's no
00:13:49.800
reason to reinvent the wheel and it is
00:13:52.200
simple enough and it's close enough to
00:13:54.180
our little store example that we built
00:13:56.100
just now that we can just rebuild it
00:13:58.260
ourselves with very little JavaScript
00:14:00.660
effectively what Redux has is reduct has
00:14:05.160
three different concepts it has the
00:14:07.500
store and it has actions and it has a
00:14:12.300
reducer and let me just copy and paste a
00:14:15.300
bit about each in here just so we can
00:14:17.339
reference it so if we go on Redux and we
00:14:20.040
go on getting started so let's go Core
00:14:22.980
Concepts so effectively we have our
00:14:25.800
store here which is very similar to what
00:14:28.740
we have done up until now so this is
00:14:30.600
just like a big object you know and it's
00:14:32.820
actually a to-do app which is helpful
00:14:34.920
and then it has actions so this is how
00:14:37.920
actions look okay so actions are
00:14:40.079
effectively an object that has a name so
00:14:43.500
this action's name is add to do this
00:14:45.720
action's name is toggle to do and then
00:14:47.940
you can send extra information with a
00:14:50.040
common convention is actually to include
00:14:52.199
the extra stuff in something called
00:14:54.060
payload and I actually do that as well
00:14:56.880
so you would go type and you would maybe
00:14:58.380
do add to do and then then you would
00:15:01.199
create a payload object what you often
00:15:03.600
do is then you put anything that you
00:15:05.639
want to send along with the action in
00:15:08.760
here so you would then go text go to
00:15:12.180
swimming pool for example so this just
00:15:15.420
makes it a bit more structured so that
00:15:17.100
you have type and payload as your two
00:15:19.740
root properties in your action and so
00:15:22.800
then what we have is we have a reducer
00:15:26.100
so what the reducer does is the reducer
00:15:29.220
effectively takes the action and the
00:15:31.680
store and combines it into a new store
00:15:33.779
so this is effectively how it works you
00:15:37.380
submit an action to a reducer then the
00:15:40.260
reducer pulls in the store it then takes
00:15:43.019
the current state and the action that
00:15:44.820
was submitted and reduces it into a new
00:15:48.180
state that gets added to the store so
00:15:50.639
this might seem over convoluted and one
00:15:53.699
of the critiques against Redux sometimes
00:15:55.920
is that it requires a lot of boilerplate
00:15:57.839
but there is also a case to be made 8
00:16:01.079
for when you are dealing with something
00:16:03.360
as critical as the the global state of
00:16:07.320
your app you maybe want it to be more
00:16:10.440
readable more clear more deliberate than
00:16:13.320
just running something called add task
00:16:16.320
or whatever and that does some magic
00:16:18.480
behind the scenes and somehow it adds a
00:16:20.519
task to the store so this is kind of the
00:16:23.779
basic approaching as the stores reduces
00:16:26.940
and actions you can read the Redux
00:16:29.699
documentation if you want so maybe a
00:16:32.579
good read as well is thinking in Redux
00:16:35.760
uh so let me just quickly highlight some
00:16:38.279
things here so effectively what they say
00:16:41.339
um is you know as apps have become
00:16:43.620
increasingly more complicated and
00:16:45.360
interactive we must manage more State
00:16:48.360
than ever and so what it effectively
00:16:50.399
says is that managing ever-changing
00:16:52.320
state is hard so this is kind of the
00:16:55.259
problem that it tries to solve and I'm
00:16:57.180
going to show you now in a second where
00:16:59.220
if we just take a purely oop approach
00:17:02.100
how eventually we're going to reach a
00:17:04.559
point where you no longer understand
00:17:05.939
what happens in your app and you've lost
00:17:08.040
control over the when why and how of its
00:17:11.040
state so a lot of those oop principles
00:17:13.439
are good in terms of keeping the
00:17:16.919
behavior manageable and structured one
00:17:20.339
of the drawbacks is at no point can we
00:17:22.980
actually see a unified picture of what
00:17:26.640
is going on in our app what is the
00:17:28.679
current state of the app right now
00:17:30.540
because that state is split between all
00:17:34.260
these entities the car are tasks that
00:17:36.900
might be shown might be in a tasks
00:17:38.760
object the actual filters that applied
00:17:41.340
might be in a filters object so there
00:17:44.100
might even be pieces of state that we're
00:17:45.720
not aware of that is fragmented all
00:17:48.120
across our app so what something like
00:17:50.220
Global store does it gives you a
00:17:52.740
centralized place where you can see the
00:17:54.539
entire state of your app at a glance and
00:17:57.120
if you do that you also have a lot of
00:17:59.039
other powerful things for example being
00:18:02.580
able to actually serialize and save that
00:18:05.160
state so we could say every time the
00:18:07.440
State updates automatically save it
00:18:10.020
locally so that the next time you open
00:18:11.880
the app it just continues from where it
00:18:14.400
left off last time and following a
00:18:16.740
traditional oop approach you might need
00:18:19.860
to actually make saving the state a
00:18:21.840
deliberate a deliberate action that the
00:18:23.940
user needs to perform so they might need
00:18:25.740
to click a button that says save and
00:18:27.840
they might need to manually load the
00:18:29.400
state again so this allows us to auto
00:18:31.500
save and auto load a serialized version
00:18:34.080
of the state and effectively what Redux
00:18:36.660
says is the reason why state is really
00:18:39.360
hard to manage in most modern apps is
00:18:42.480
because we're managing two different
00:18:44.700
ideas we're managing mutation and
00:18:47.820
asynchrony so mutation is effectively
00:18:50.640
things can actually change so one of the
00:18:54.480
principles of functional programming is
00:18:56.460
that as far as possible you avoid side
00:18:58.919
effects you avoid mutations and
00:19:01.380
asynchrony effectively is just things
00:19:03.840
can actually happen after the code has
00:19:06.179
run so event listeners you know someone
00:19:08.520
can click somewhere someone can drag
00:19:10.140
something someone can delete something
00:19:11.820
so Redux effectively says that these two
00:19:15.059
ideas when combined makes managing
00:19:17.580
modern JavaScript apps really really
00:19:19.980
hard and and it uses the example of
00:19:22.200
saying like almost like Mentos and Coke
00:19:24.000
and both of them are great in separation
00:19:26.280
but when you mix them like things get
00:19:28.559
out of hand and so seriously you know
00:19:30.600
like libraries like react and so forth
00:19:33.720
actually manage the presentational layer
00:19:37.320
of this so you know if we think about
00:19:39.539
web components web components help us
00:19:42.179
manage like the presentation of things
00:19:44.220
is a task completed is it not completed
00:19:46.980
how do we show that and this is also
00:19:49.200
what a lot of these libraries do and for
00:19:51.600
this reason usually Global state is
00:19:54.419
actually solved by a secondary Library
00:19:56.299
whether it be so stand Redux paneer and
00:19:59.640
so forth and then some Frameworks like
00:20:01.620
svelt actually build a global State
00:20:03.900
solution into itself but effectively it
00:20:06.419
sees these as two different
00:20:07.700
considerations so if we spoke about
00:20:09.900
separation of concerns and single
00:20:11.880
responsibility principle so it
00:20:14.160
effectively says you need a solution is
00:20:16.860
actually going to control how data gets
00:20:19.740
rendered and this is where we are at the
00:20:21.720
moment using web components but then you
00:20:23.940
also need a secondary solution that
00:20:25.740
manages what is the actual State what is
00:20:28.500
the data in the app at the moment and
00:20:30.900
that's completely removed from how that
00:20:35.220
data is actually presented and so what
00:20:37.559
Redux says is functional programming
00:20:39.720
actually gives us a very nice model
00:20:42.380
to think about reason and do the part
00:20:45.780
where we're actually updating the global
00:20:47.940
State and so it talks about its three
00:20:50.160
principles so the global state so it
00:20:53.100
says effectively the global States a
00:20:54.539
single source of Truth what's really
00:20:56.340
cool about this is because it is a
00:20:58.140
single source of Truth it means that if
00:21:00.900
you save it you can just load it again
00:21:02.940
and you know everything that's required
00:21:05.340
to render a specific state of the app is
00:21:08.340
actually in your store and you don't
00:21:10.380
need to manually save every little bit
00:21:12.179
which is something that you'll have to
00:21:13.919
do in a traditional oop approach and
00:21:17.039
also it's really nice it allows us to
00:21:18.600
undo and redo because if you remember
00:21:21.320
what we did previously is we actually
00:21:25.320
put our new States in an array so that
00:21:27.660
means if you want to undo you just move
00:21:30.360
back in your States if you want to redo
00:21:32.460
you just move forward in that array
00:21:34.320
again so this is really cool and you
00:21:36.419
know this is often called time traveling
00:21:38.340
so you can travel back and forwards in
00:21:40.440
time in your state you can look at that
00:21:42.720
entire array and actually see how the
00:21:45.059
state changed across the life cycle of
00:21:47.580
the current station so it's very nice
00:21:49.320
for debugging figuring out where things
00:21:51.240
are going wrong so this is the first
00:21:53.100
principle single source of Truth second
00:21:54.900
principle is a status read only so you
00:21:57.720
can't directly update the state you need
00:21:59.520
to emit an action so what's really cool
00:22:01.559
about this is you can just listen for
00:22:03.120
actions as a means to actually figure
00:22:05.880
out when what caused the actual state to
00:22:09.840
change and this is something that's very
00:22:11.640
critical in in functional programming
00:22:14.640
data is what is called unidirectional it
00:22:18.419
can only flow in One Direction in oop we
00:22:22.559
might have this object and we might have
00:22:24.720
that object and they talk to one another
00:22:27.240
through an interface okay but so data
00:22:29.940
can go both ways data can go from this
00:22:32.820
object to that object or from this
00:22:34.799
object to that object
00:22:36.840
so sometimes it's very hard to reason
00:22:39.539
about where data comes from and why
00:22:43.320
something changed and how you got to the
00:22:45.600
data and then if you have even more you
00:22:47.460
know like then you have kind of like
00:22:48.840
these dependencies so it's kind of like
00:22:50.340
a graph
00:22:51.600
so it's very hard to figure out where
00:22:54.900
the change originate from
00:22:57.240
in functional programming because data
00:23:00.120
is unidirectional in other words it only
00:23:02.100
Flows In One Direction if you want to
00:23:04.440
figure out what why something changed
00:23:07.919
why did this button turn from blue to
00:23:09.960
green why did this task get removed why
00:23:12.480
did the stars get added you just listen
00:23:15.120
somewhere along that path and everything
00:23:17.159
that happens like has to go through that
00:23:20.400
you know and then obviously it goes all
00:23:22.200
the way around again but like it goes in
00:23:24.480
generally a circular motion but in Only
00:23:26.760
One Direction so if you listen at a
00:23:29.159
specific Place everything needs to flow
00:23:31.260
through there you're not going to miss
00:23:32.460
anything so what this means is because
00:23:35.039
we can only update the store via actions
00:23:37.260
we just listen what actions are
00:23:39.000
submitted and there we can infer what
00:23:42.120
action caused the store to actually
00:23:43.799
change and then once an action arrives
00:23:46.740
at the store the way the new store is
00:23:49.799
calculated is through something called a
00:23:51.960
pure function
00:23:53.460
um so this is the first time I'm talking
00:23:54.840
about this idea of a pure function but
00:23:56.580
effectively appear a function is just a
00:23:58.559
function that doesn't have side effects
00:24:00.299
and we did this in our previous example
00:24:02.640
where we passed the action in which was
00:24:05.100
a function that just returned a new
00:24:07.020
state it didn't have any side effects so
00:24:09.240
changes are made with pure functions so
00:24:11.280
they're predictable and they're super
00:24:13.140
easy to test so these are very high
00:24:15.840
level and might be a bit hard for you to
00:24:18.419
wrap your head around it I actually
00:24:19.799
encourage you to watch a couple of
00:24:21.000
videos on Redux maybe read the
00:24:23.340
documentation a bit as I mentioned in
00:24:25.320
functional programming the concepts are
00:24:27.720
hard to understand but once you
00:24:29.940
understand the concepts the code is very
00:24:32.760
easy to reason about you know for
00:24:34.799
example here so once you understand this
00:24:37.620
this interplay it's actually very easy
00:24:39.600
to figure out what the code is doing
00:24:41.340
whereas with traditional oop it's not
00:24:44.520
that hard to understand because this
00:24:46.020
kind of models how we experience things
00:24:48.059
around us so we experience things as
00:24:50.220
separate entities that just interact
00:24:52.200
with one another so this is very easy to
00:24:54.539
understand but it's much harder to
00:24:56.820
reason about figure out why something
00:24:59.460
happened why did this thing change what
00:25:01.980
caused this to change and so forth
00:25:04.020
because there are side effects all over
00:25:05.520
the place and because there are no side
00:25:07.799
effects here in functional programming
00:25:10.080
you can't for example have this Branch
00:25:11.820
off and now actually change that thing
00:25:13.620
or have a change from here that changes
00:25:15.900
that thing everything needs to flow
00:25:18.059
through this little this little cycle
00:25:20.580
through this pipe and you can listen
00:25:22.260
anyway on this pipe and you're going to
00:25:23.880
catch everything that flows through it
00:25:25.559
so let me show what that looks like in
00:25:27.360
practice so if we just quickly look at
00:25:30.480
the API for Redux as well so the store
00:25:33.240
itself
00:25:34.200
um has get state it has dispatch which
00:25:36.659
is very similar to the update that we
00:25:39.000
created it has subscribe which is
00:25:41.460
similar to the Subscribe that we had and
00:25:44.100
it has replaced reducer and so we're not
00:25:46.020
going to do replace reducer this is a
00:25:47.760
bit more advanced but effectively let's
00:25:49.980
just create our own version of Redux
00:25:52.020
with these three methods so let us
00:25:55.080
create our model here and in in our
00:25:57.720
model we have the store itself we have
00:26:00.779
our reducers and we have our actions so
00:26:05.100
here all those three spots are split up
00:26:07.140
and you can test them individually and
00:26:08.940
separately without requiring the other
00:26:10.919
stuff so let's say we're doing an
00:26:12.500
extremely basic version of our to-do app
00:26:15.000
and another thing that's really cool
00:26:16.919
about Redux is it's very easy to
00:26:20.640
actually type these things up you can
00:26:22.980
actually ensure type correctness ensure
00:26:25.919
that you don't make any spelling
00:26:27.360
mistakes or whatever because this is not
00:26:29.940
a function that you call it's an actual
00:26:31.679
object that you send and you can
00:26:33.840
actually not only can you cancel log
00:26:36.000
that object every time for debugging
00:26:38.220
purposes or do something with that
00:26:39.840
object you can even check that object
00:26:42.240
for correctness either during run time
00:26:44.960
just doing a manual check on this or
00:26:47.820
even through static typing through jsdot
00:26:49.980
so as we did in the module we recovered
00:26:52.380
documentation and writing your
00:26:53.580
documentation first let's quickly do
00:26:55.320
that over here and it's going to really
00:26:57.000
fast because this is just a
00:26:59.220
straightforward to do app much simpler
00:27:01.559
than the one that we have created up
00:27:03.059
until now so let's just say each to do
00:27:05.159
is literally just a string so let's
00:27:07.140
create our store so we can just say our
00:27:09.240
store effectively and state actually
00:27:11.640
sorry it's a state so the state is
00:27:13.799
what's in the store a store can have
00:27:16.020
multiple States so it can have a
00:27:17.340
previous state and the next state and so
00:27:19.559
the prop on here is tasks type def
00:27:23.520
object a task is an object that has ID
00:27:27.779
there's a string as a title which is
00:27:30.600
also a string and just the created date
00:27:33.419
so we have tasks and so this is just an
00:27:36.539
object so record of strings which would
00:27:39.240
be the IDS and then the actual task
00:27:41.760
itself so like that so this is tasks
00:27:44.100
let's just do our filters and our
00:27:46.740
filters at the moment is just going to
00:27:48.240
have sorting and nothing else okay so
00:27:50.400
filters and that's just an object
00:27:51.900
sorting and it's just let's say A to Z
00:27:55.320
and z2a that's the only two options and
00:27:59.640
then lastly we just want a phase okay
00:28:02.580
and so what are the possible phases that
00:28:05.039
the app can be in so we're going to talk
00:28:06.659
a bit more about this idea of phases
00:28:08.400
when you talk about State machines but
00:28:10.080
for now this can just be idle so doing
00:28:13.320
nothing
00:28:14.460
um adding okay so what does our store
00:28:16.860
look like so type Dev and this is just
00:28:19.260
the interface that our store is going to
00:28:21.179
use it's just Object Store a couple of
00:28:23.520
callbacks so add callback get state so
00:28:27.480
we just emulate what Redux does over
00:28:30.059
here so get State and all that get state
00:28:32.279
is it's just a callback that Returns the
00:28:35.340
current state okay then there is another
00:28:37.679
one which is dispatch which is very
00:28:40.020
similar to what we had previously with
00:28:43.740
update so it takes a param and that
00:28:46.200
param is an action okay we haven't
00:28:49.679
specified actions just the extra action
00:28:52.200
and then the last one is subscribe so
00:28:56.340
callback subscribe and we also need to
00:28:59.220
make this all caps and subscribe takes
00:29:02.100
uh and I think like I confused myself a
00:29:04.980
bit last time when I mixed these up so
00:29:07.080
let's just say it starts with the
00:29:08.340
previous so stay to the previous date
00:29:10.679
and and the next one is the next state
00:29:15.120
um okay so then our store has the
00:29:18.000
following props gate state which is the
00:29:20.460
sketch state so that is a function that
00:29:22.740
you can run to get the current state if
00:29:25.020
you want to check anything subscribe and
00:29:27.659
we can do the same where we just return
00:29:29.640
the actual unsubscribe so that would
00:29:31.980
just be an empty function so callback if
00:29:34.980
n this gives us the means to oops in
00:29:38.279
this returns gives us the means to
00:29:40.140
unsubscribe right so then the last part
00:29:43.440
is dispatch so this is a very simplified
00:29:47.700
version of Redux this is just to show
00:29:49.740
the principle that Redux uses under the
00:29:52.679
hood if we were to create our own
00:29:54.360
simplified version of Redux if you look
00:29:56.520
at actual read products that is a bit
00:29:58.080
more complexity and it adds a couple of
00:30:00.960
quality of life things that makes it
00:30:02.760
easier but that does add a bit more
00:30:05.159
complexity so we are just keeping it
00:30:07.200
simple so just keep in mind this isn't a
00:30:08.940
hundred percent mapping how Redux works
00:30:11.340
this is just to show the principle now
00:30:13.380
what do we want to do is let's create
00:30:15.539
our actions and let's give each of these
00:30:18.120
actions a unique name so add task to
00:30:21.659
sort and start add cancel add now you
00:30:25.740
can see everything you can literally do
00:30:27.240
with the App State here so all of these
00:30:29.279
are objects and they all have a prop
00:30:32.100
called type which is just for each of
00:30:34.919
them a string literal and the convention
00:30:37.919
is to write it an upper snake case so a
00:30:41.460
task like that change sort start add
00:30:45.120
like that and cancel add
00:30:48.240
um and I'm not going to do that payload
00:30:50.460
pattern just yet just to keep it simple
00:30:52.679
so all that we want over here is let's
00:30:56.279
also create a task in our store and we
00:30:59.760
actually have it if you remember
00:31:01.500
correctly we can just go export con task
00:31:05.240
like that to be able to import it so
00:31:08.520
let's just pull that in from our store
00:31:10.980
and so all that this accepts is a task
00:31:14.159
and then change sort would be new sort
00:31:18.179
but let's also break sort out into its
00:31:21.419
own thing here is to type Dev sorting it
00:31:25.140
can be one of these okay and let's also
00:31:27.419
export that to export const sorting okay
00:31:30.720
so we want to pull in tasks we want to
00:31:32.640
pull in sorting okay there we go and
00:31:36.000
start adding so we don't need to send
00:31:38.460
any extra info this just starts the
00:31:40.559
adding process this just cancels the
00:31:42.480
adding process if you really want to you
00:31:44.640
can add some documentation here so you
00:31:47.100
can see how this is very self
00:31:48.980
documenting like this is one of the
00:31:51.000
benefits of something that is so
00:31:52.980
deliberate like Redux so let's just say
00:31:55.460
adds a task to the store so obviously
00:31:58.740
this isn't the greatest documentation
00:32:00.659
but but I just want to show the
00:32:02.279
principal changes the order in which
00:32:05.220
tasks are sorted starts the adding
00:32:08.940
process of a new task cancels the adding
00:32:13.200
process of a new task we can even
00:32:16.320
combine these into a single one that
00:32:18.600
says toggle adding so starts or can't or
00:32:23.460
stops the adding process of a new task
00:32:25.799
comma depending on what the current
00:32:29.460
phase is then what we will usually do is
00:32:32.520
we would do action creators so Redux
00:32:35.460
makes a very big distinction between
00:32:37.500
actions and action creators let's just
00:32:40.260
action creators and I think sometimes
00:32:42.779
people mix them up confuse them
00:32:45.539
so effectively what it says is you know
00:32:48.059
it's a pain to create the entire action
00:32:51.539
every time you want to do it so what you
00:32:53.820
might do is you might create a function
00:32:55.200
that creates that action for you like
00:32:57.600
this add to do as an action Creator but
00:33:00.960
it tells you to not confuse the action
00:33:02.940
creator for the action itself so the
00:33:05.520
action itself is always an object the
00:33:07.740
action Creator just creates that object
00:33:09.779
for you
00:33:11.100
so let's just create some action
00:33:13.019
creators here for us so let's just also
00:33:16.200
export them so add task let's just Mark
00:33:19.140
that up so that should return a task for
00:33:22.440
us like that and let's also just enable
00:33:24.840
TS check across this entire project so
00:33:27.120
we would go TS config and what we want
00:33:30.120
to do is we want to say compiler options
00:33:33.019
allow.js true check JS true and then
00:33:37.080
just what version we want to Target
00:33:39.059
let's go 2018 just let's just randomly
00:33:42.480
deciding on one so I'm not going to pull
00:33:44.340
in pretty earn all of this stuff I just
00:33:46.620
wanted to show the principles super
00:33:48.000
quickly but obviously if this was an
00:33:50.460
actual real project I would pull in
00:33:52.320
pretty uh eslint all of that stuff okay
00:33:55.200
so it's unhappy because it doesn't
00:33:56.640
return that what also what does it
00:33:59.039
accept so let's just do and the browser
00:34:02.640
is an object and the object is is called
00:34:05.100
props and inside that param just a
00:34:08.520
string for now that is the name or the
00:34:10.859
title so we have to go props props dot
00:34:14.280
title like that and so Props let's just
00:34:18.300
destructure that so Props and so then
00:34:22.560
everything else that gets Auto created
00:34:24.359
we can actually automatically create in
00:34:26.399
here like I said type would be add task
00:34:29.399
and they're created we can just do
00:34:32.040
straight up new date ID let's pull in
00:34:35.159
that other function that we created that
00:34:37.260
creates unique IDs for us and title we
00:34:39.839
can just grab from there okay and let's
00:34:42.179
just put this here in our actions there
00:34:44.879
we go it's just a Helper but we're not
00:34:46.500
using it anywhere else so let's just
00:34:47.820
keep it in our actions and we can go
00:34:50.339
create unique ID right so now this is
00:34:53.339
nailed down we have type security we
00:34:55.560
have everything we need let's do the
00:34:57.900
other the next one which would be let's
00:34:59.400
say toggle right so this one is much
00:35:01.920
more straightforward we can literally
00:35:03.480
just do it as follows but let's just
00:35:05.700
creates that action for us without
00:35:07.500
taking anything in so it just returns
00:35:10.260
toggle I think we never updated the name
00:35:13.140
toggle and this is literally what it
00:35:16.260
does so it's as simple as that and
00:35:19.200
change sort okay so our app can't do
00:35:22.800
much at the moment and intentionally
00:35:25.220
intentionally so
00:35:27.480
um because obviously I just want to show
00:35:28.980
the principle an actual Redux store
00:35:31.619
would look would have many many more
00:35:33.780
actions and actually have separate like
00:35:35.880
action files and separate reducer files
00:35:38.700
because this is functional programming
00:35:40.980
what's really nice is the scales really
00:35:43.560
well because like all of these are
00:35:45.420
effectively just pipes so we can just
00:35:48.240
connect all these pipes here if we want
00:35:51.060
to extend that
00:35:52.920
um you know or if we want to extend this
00:35:55.079
part we just like connect more pipes and
00:35:57.660
all of because all of it just flows
00:35:59.400
through you can add infinite amount and
00:36:02.520
it's not going to change the way it
00:36:03.960
works it just flows through more pipes
00:36:05.880
and so reduces and actions you know
00:36:08.220
effectively just allow you to extend
00:36:09.960
this but I know Point does it actually
00:36:12.359
Branch out does something outside and so
00:36:15.960
in the next video I'm going to unpack
00:36:17.640
this a bit more because this might be a
00:36:20.220
bit confusing at the moment but I think
00:36:22.079
I need to implement the store first so
00:36:24.839
you can actually see it in action and
00:36:26.099
then we can talk about what it actually
00:36:27.720
does so this one is just I think was a
00:36:31.020
change sort right and Export const
00:36:35.339
change sort that just takes a param and
00:36:39.000
let's say sorting I think we are
00:36:40.560
importing it yep let's just say props
00:36:43.380
and that's an object so we can so only
00:36:46.380
just pass for example you know sorting
00:36:49.020
and not make it part of an object but I
00:36:52.260
just find it's easier to extend it and
00:36:54.660
add more things if you later on so let's
00:36:57.119
say you want an option to reverse the
00:36:58.980
sorting and then you can pass more
00:37:01.020
things at a later Point okay and this
00:37:03.660
should be props dot sorting and change
00:37:06.240
sort so it's unhappy because it doesn't
00:37:08.160
actually return that action so sorting
00:37:10.560
and type and type is change sort let's
00:37:14.220
just grab sorting over here and we
00:37:16.560
actually mess this up this should be
00:37:17.940
like that I think this should be full
00:37:20.820
toes yes okay and so we haven't created
00:37:23.040
our store just yet but so the next thing
00:37:25.440
we want to do is we create our actions
00:37:26.820
we want to create our reducer and you
00:37:28.619
can have multiple reducers and as
00:37:30.300
mentioned because these are just pipes
00:37:31.740
you can just connect them and create a
00:37:33.960
longer pipe but we're just going to have
00:37:35.940
a single reducer all right so let's
00:37:38.040
create our reducer so what is our
00:37:40.140
reducer going to do effectively all a
00:37:42.599
reducer does is and you can connect
00:37:44.579
multiple reducers and all the reducer
00:37:46.619
does it takes the statement it returns a
00:37:49.079
new state get our state and I think we
00:37:52.380
need to export it as well yep can't
00:37:55.859
State okay there we go and what we also
00:37:59.220
need to do is we now can combine all our
00:38:02.280
actions into a single generic action
00:38:05.520
that can be any of these so you just go
00:38:08.579
type Def and you just say action and you
00:38:12.119
just add all your actions in here so
00:38:13.859
what's an add task and sort so this is
00:38:16.260
effectively a union saying that it can
00:38:18.660
be any of these and let's just also
00:38:21.660
export const action right so from a
00:38:25.320
store we get the state from our actions
00:38:28.140
we get an action so in our reducer the
00:38:32.880
first thing a reducer usually takes is
00:38:34.980
the state and then an action okay and we
00:38:37.800
can just Mark these up so param one and
00:38:41.400
I'm just writing this in the way that
00:38:43.140
Redux does it Redux has it as two
00:38:45.240
separate params so you have your state
00:38:47.460
and then you have a new parameter which
00:38:50.040
is action and then this should just
00:38:52.800
return a new state okay and it is
00:38:55.500
unhappy because it doesn't do any of
00:38:57.300
that stuff right now here we actually we
00:38:59.640
can use this reducer it's just always no
00:39:01.859
matter what action you pass to it it's
00:39:03.660
just going to return the same state it's
00:39:05.099
not going to change anything so let's
00:39:06.839
just work with this for now and then we
00:39:09.240
add the actual changes to our state
00:39:11.700
after we set up like the entire store
00:39:13.740
okay so let's get going here so in our
00:39:16.980
store over here let us create an array
00:39:20.099
that has our subscribers that is just an
00:39:23.579
array of subscribe okay and then let's
00:39:27.780
also just do all our states which is an
00:39:31.020
array of State you can just replace the
00:39:33.839
state each time but what's cool about
00:39:35.339
this is
00:39:37.020
um you can actually then do go back and
00:39:39.300
so forth and we might even add an
00:39:41.339
ability to go back and forwards or you
00:39:43.500
can log the entire State and if you want
00:39:45.960
to see what went wrong or debugging
00:39:47.960
that's really cool so let's just say
00:39:50.400
states which is also an array so let's
00:39:52.859
actually not create a store object let's
00:39:54.960
just once again use the JavaScript
00:39:56.820
module and Export it as functions so get
00:40:00.839
State return State okay and all that
00:40:04.200
that does is it grabs the latest State
00:40:06.720
and it returns it and remember I put the
00:40:09.240
new states in the front me meaning we
00:40:11.880
can just go States zero the very first
00:40:15.000
one there we go then dispatch
00:40:17.960
effectively does the following so
00:40:20.640
dispatch takes uh action so let's import
00:40:24.000
our actions in here then go forgot yes I
00:40:27.180
forgot to put the JS here as well and in
00:40:30.480
actions yes I didn't put it in any of
00:40:33.599
these whoops all right so then our store
00:40:36.240
so what we want is export const dispatch
00:40:40.940
dispatch just takes an action and that
00:40:43.859
is it so it can be any of those actions
00:40:45.839
that we defined so what this effectively
00:40:48.839
does is it gets the current store to get
00:40:51.900
State here it might even be worth to
00:40:54.240
return the state as a completely new
00:40:56.820
object so that you can't mutate it and
00:40:59.760
maybe even just freeze it if you're
00:41:01.920
running in strict mode it gives you an
00:41:03.720
error and if you're not running in
00:41:05.760
strict mode it actually just doesn't
00:41:07.619
change the thing and you don't even know
00:41:09.359
that it didn't do that
00:41:10.920
if you're using modules so if you're
00:41:13.980
going you know deferred type module when
00:41:16.680
you import the script it automatically
00:41:18.300
uses strict mode so you don't need to
00:41:19.800
worry about that okay so we get the
00:41:21.660
state here so it's smart enough to know
00:41:23.940
State and then we create the next one
00:41:26.160
and we do that by actually running our
00:41:28.800
reducer on that so let's import our
00:41:31.500
reducer here okay in several reducers we
00:41:34.440
only have a single reducer at the moment
00:41:36.619
that we are not exporting and so what
00:41:39.780
you do is you just pass the previous
00:41:41.579
state and you pass the action and it
00:41:43.740
gives you a new state so then just what
00:41:46.079
we do is after we get the next state we
00:41:48.540
take States and we unshift in other
00:41:50.940
words put it in front just push in the
00:41:53.220
new state okay so this patch is working
00:41:54.960
now let's quickly do subscribe and you
00:41:57.599
can see that I go quite fast on this
00:41:59.880
because I'm already very familiar with
00:42:01.619
the pattern I've used it a ton I've used
00:42:03.359
reduxitone obviously you might not be
00:42:06.359
familiar with it and you're struggling
00:42:08.339
to follow along which as mentioned you
00:42:10.800
know a functional programming it's hard
00:42:12.720
to understand the concepts so you might
00:42:15.119
need to re-watch this video you might
00:42:16.740
need to pause replay certain bits get
00:42:19.680
your head around exactly what I'm doing
00:42:22.380
maybe even follow along step for step
00:42:24.599
but the key being like once you
00:42:26.099
understand the concept it's going to be
00:42:28.200
very easy to reason about your code it's
00:42:30.420
going to be very easy to understand what
00:42:32.339
your code is doing so you're making a
00:42:34.560
trade-off in terms of the complexity of
00:42:36.960
the concepts as opposed to the code
00:42:39.420
itself being complex but the concepts
00:42:42.000
being simple now we're using more
00:42:43.920
complex Concepts which are going to make
00:42:46.020
our code simpler and more readable if
00:42:48.420
you understand the concepts in the same
00:42:50.520
way that when we started talking about
00:42:52.079
abstraction we spoke about mathematics
00:42:54.180
and so we can think about what we've
00:42:56.940
been doing up until now is that we've
00:42:58.920
been actually writing that entire
00:43:00.920
paragraph out where we say imagine you
00:43:03.420
have one thing and you have another
00:43:05.040
thing and if you combine those two
00:43:06.839
things now you have two things so that
00:43:09.540
is what we've been doing up until now
00:43:10.800
all and it doesn't require us to
00:43:12.960
understand any additional complex
00:43:16.020
Concepts but if we say you need to
00:43:19.319
understand mathematics and you need to
00:43:21.420
understand equality and also the plus
00:43:24.300
sign in mathematics and what that means
00:43:26.880
and also numbers then you can just write
00:43:29.400
it as one plus one equals two so you're
00:43:32.099
writing it in a very simple
00:43:33.599
straightforward manner but it does
00:43:35.220
require you to understand some of the
00:43:37.980
more complex ideas underlying that
00:43:40.800
actual expression and it's the same here
00:43:43.020
with functional programming and honestly
00:43:45.420
even if you hate this even if you're
00:43:47.040
like this sucks I'm never going to do
00:43:48.660
this the reality is there's a ton of
00:43:50.640
projects out there that are using Redux
00:43:52.859
or Redux like libraries I show that you
00:43:56.400
know it said you know every week almost
00:43:59.160
8 million downloads okay so at the very
00:44:01.740
least this just means it's useful to
00:44:04.380
understand how it works because there's
00:44:05.760
a possibility you are probably going to
00:44:07.560
encounter a Redux project at some point
00:44:09.720
that uses kind of this redox model okay
00:44:12.180
so subscribe so what subscribe takes is
00:44:15.119
it takes a param that is just a
00:44:18.540
subscription a subscribe should actually
00:44:20.880
be a subscription subscription not a
00:44:24.480
subscribe there's no such thing as a
00:44:27.000
subscribe you can subscribe a
00:44:29.220
subscription so it just takes that and
00:44:31.440
this is called subscription all right so
00:44:33.480
when you pass that first number was what
00:44:35.700
it does is it just goes subscribers and
00:44:39.119
we push that on there and we just return
00:44:41.579
the means to unsubscribe we just create
00:44:44.099
a unsubscribe function that just returns
00:44:47.760
and all this does it Loops over so new
00:44:51.680
subscribers so it Maps over the current
00:44:54.660
subscribers and so this is also why I
00:44:56.880
like Factory functions and just using
00:44:59.339
the built-in modules in JavaScript
00:45:01.460
nowhere here we're fiddling with this
00:45:04.140
you know and private things and so forth
00:45:07.079
yeah so this is just personally for me
00:45:09.420
to just show you why actually like doing
00:45:12.599
Factory functions why I actually like
00:45:14.400
using the built-in modules instead of
00:45:16.500
creating classes but it might not be
00:45:18.599
something that is such a pain for you
00:45:20.579
but like and the less I have to work
00:45:22.740
with this in JavaScript the better so
00:45:24.900
subscribers and we do falter and we just
00:45:27.660
get an item so it Maps over all of these
00:45:30.000
and then it just determines whether it
00:45:32.940
actually should include it so let's just
00:45:35.220
create the Handler for a filter up here
00:45:36.960
so const Handler you can write it
00:45:39.420
directly in there as well if you want I
00:45:42.180
like to actually keep it separate I find
00:45:44.040
it to be a bit more readable and all
00:45:47.220
that this does is it gets the current
00:45:49.260
item in the array and it just Compares
00:45:52.200
is that item not equal to the current
00:45:55.680
subscription and if it's not then it
00:45:57.839
keeps it so this is true so anything
00:45:59.940
that resolves to true when you call
00:46:02.880
filter it keeps
00:46:04.920
um if it's false it removes it so it
00:46:07.560
just runs this Handler on every single
00:46:09.720
item in subscribers and returns new a
00:46:12.660
new array so this is a higher order
00:46:14.400
function it's kind of at the core of
00:46:16.740
functional programming and we're really
00:46:18.660
going to unpack what are all these
00:46:20.220
higher order functions and how can you
00:46:21.720
use them
00:46:22.859
this is a lot more expressive than if I
00:46:24.900
were to do a for Loop now and not only
00:46:26.819
that I can actually reuse this logic if
00:46:29.099
I want to do another filter or I want to
00:46:30.780
do a map or something else and then all
00:46:33.780
we do is we just replace subscribers the
00:46:36.599
new subscribers and it needs to be a let
00:46:38.940
okay and now we just need to actually in
00:46:42.180
here trigger the subscriptions as well
00:46:44.940
so so what we want to do here is we want
00:46:47.400
to get all the subscribers and we just
00:46:49.260
wanna for each on them so Loop over each
00:46:51.839
one and then what handler do we want to
00:46:54.660
do use like what do we want to run on
00:46:57.119
each of them so just take the item and
00:46:59.520
run it and pass previous and next so we
00:47:04.020
can even just put it like that in there
00:47:06.599
as well and it's actually smart enough
00:47:08.400
to know that net previous is a state and
00:47:10.740
next is the state so let's even just do
00:47:13.740
it directly like that okay for a bit
00:47:15.839
more type safety in other words if we do
00:47:19.140
that it's going to tell us hey like this
00:47:21.780
actually requires two arguments okay
00:47:24.359
because it knows that this item is a
00:47:28.140
actual the subscription that we created
00:47:30.900
up here and I think that is it so let's
00:47:34.440
quickly do our reduces okay you can do
00:47:36.839
an if statement you can do whatever you
00:47:38.940
want the common approach is to do a
00:47:41.040
switch I personally don't like switches
00:47:43.500
but I would actually just do it with if
00:47:46.260
statements myself but just to kind of
00:47:48.660
keep it as close to how Redux does it as
00:47:51.119
possible let's use a switch so that if
00:47:53.520
you do see Redux code you're kind of
00:47:55.740
already familiar with the way that it
00:47:57.540
does it so it uses a switch statement so
00:47:59.700
that switch looks at the action time and
00:48:02.099
then based on the action type it
00:48:04.020
determines what to do if none of the
00:48:06.180
action types match any of the conditions
00:48:08.640
in here we just return State okay so the
00:48:11.579
default fallback is return state so at
00:48:14.760
the very least if none if you don't have
00:48:16.560
any conditions for any actions here it's
00:48:18.780
just going to return the state as is
00:48:20.760
but in most of these cases we want to
00:48:23.099
update the state based on the action
00:48:25.200
that was dispatched all right so what
00:48:27.119
you would do is you would say case and
00:48:29.099
it would actually say here are the
00:48:30.720
actual actions this is the case then do
00:48:33.060
the following
00:48:34.079
if this is the case then do the
00:48:38.220
following over here and if this is the
00:48:41.339
case toggle add then do the following
00:48:44.220
here and now if we go here case it
00:48:46.440
actually there's nothing left you know
00:48:48.060
it'll actually tell us like you know
00:48:49.980
like there is no other cases this is all
00:48:52.079
it can be and this is how you can also
00:48:53.880
split up your reduces so you can have a
00:48:55.740
reducer that specifically looks at the
00:48:58.200
task things already so that looks at
00:49:00.060
something else and effectively it just
00:49:02.220
passes it through each reducer each
00:49:03.900
reducer just checks if it matches all
00:49:06.180
right so add task
00:49:07.740
so we want to return a new state so
00:49:10.619
let's in all these cases just return the
00:49:13.440
state exactly as is and then let's just
00:49:15.420
put our modifications in there okay so
00:49:17.339
toggle ad is pretty straightforward all
00:49:19.020
that toggle ad does is we update the
00:49:20.880
phase and we look at the current state
00:49:24.000
and the current phase and we say if the
00:49:26.760
current phase is then set the new phase
00:49:29.700
to idle so we use a ternary otherwise
00:49:31.980
set it to adding okay there we go let's
00:49:33.900
change sort is pretty straightforward
00:49:35.400
filters and remember we now need to just
00:49:38.520
destructure filters back into that so
00:49:40.980
remember each of these create a new
00:49:42.720
object each time we just want to action
00:49:47.040
sorting and it's smart enough to
00:49:49.140
actually know based on this what
00:49:51.839
actually comes along with that action so
00:49:54.720
we can even control click on it and you
00:49:56.880
know it'll actually tell us and then the
00:49:58.920
last one so tasks all right and we're
00:50:02.280
just going to destructure tasks in here
00:50:05.160
so State tasks so the current ask let's
00:50:08.640
just put the new one at the top if you
00:50:10.440
do it up here it's going to be at the
00:50:12.180
Top If you do it down here it's going to
00:50:14.220
add it at the bottom so let's just say
00:50:16.560
the key should be action task ID and
00:50:21.000
then just action dot task should be the
00:50:23.760
task itself all right and there we go
00:50:25.680
here is our entire store I think we have
00:50:28.079
everything we need let's give it a test
00:50:30.240
so
00:50:31.339
scripts.js and in here let's just grab
00:50:35.700
from our model we just want to grab the
00:50:38.579
store and from the store let's just do a
00:50:42.060
subscribe and let's just do uh dispatch
00:50:45.240
and let's also pull in some actions that
00:50:47.940
we want to pass to this patch so model
00:50:50.700
also remember the JS and let's say we
00:50:55.020
want to add a task we want to change the
00:50:58.260
sort this should actually be toggle add
00:51:01.079
not toggle task toggle ad all right so
00:51:04.140
let's subscribe first so subscribe and
00:51:08.280
we can just pass a function straight
00:51:10.020
into there we can just subscribe Contour
00:51:12.660
log so let's just do our function in
00:51:14.880
there and all this function does it
00:51:16.260
cancel logs the let's just say the next
00:51:18.240
state we don't even care about the
00:51:19.800
previous state so let's go next we just
00:51:22.619
got our types wrong so let's just click
00:51:24.240
on that so actually so the Subscribe
00:51:27.240
should return an empty function not the
00:51:29.099
subscription itself okay there we go all
00:51:31.440
right so we do that so let us go so
00:51:34.260
toggle ad so let's do toggle ad so it
00:51:37.619
should then switch it to adding let's
00:51:40.380
toggle that again let's just switch it
00:51:41.880
back to idle let's switch toggle adding
00:51:44.640
again and also maybe what we want to do
00:51:47.400
is in our reducer when we also want to
00:51:50.460
check if the current the add task we
00:51:54.420
also just want to set the phase to idle
00:51:56.640
so when you add a task it automatically
00:51:58.980
sets the app back to the idle State list
00:52:02.339
to add ask okay and what does it require
00:52:05.099
from us just a title they say hello
00:52:07.680
let's add another one world let's uh
00:52:11.460
change the sort and why do we want to
00:52:13.140
change it to sorting what do we want to
00:52:15.660
change it to let's say Z to A and let's
00:52:18.240
just toggle add again let's check this
00:52:20.579
out so let me just bring in some HTML
00:52:23.099
and there we go and let's not put
00:52:26.220
anything in the body let's just pull in
00:52:28.500
that script Source
00:52:31.460
scripts.js deferred type equals module
00:52:35.400
okay so the other thing is we obviously
00:52:38.579
create the actions here but we need to
00:52:40.260
dispatch them to the store to actually
00:52:42.359
do anything otherwise we just have like
00:52:44.520
all these objects here that we're not
00:52:46.380
doing anything with so the action
00:52:48.240
Creator this creates the action for us
00:52:51.180
but we still need to send it to the
00:52:52.980
store there we go and let's have a look
00:52:55.079
hey look at this all right so we can see
00:52:57.359
here phase adding okay it's that's how
00:52:59.819
it starts then it switches to idle one
00:53:02.940
thing here is we actually don't have an
00:53:04.920
initial state it should have an empty
00:53:07.619
the tasks so let's quickly add that in
00:53:09.960
our store so we should actually have a
00:53:12.780
starting State and we can just do it
00:53:14.520
directly in here filters okay sorting so
00:53:18.359
the Sorting is a to z and phase it
00:53:21.720
starts as Idle and tasks is just an
00:53:25.440
empty object so this is the starting
00:53:27.780
State we actually didn't put a starting
00:53:29.339
State all right let's have a look now of
00:53:31.200
course a phase adding tasks no tasks so
00:53:34.440
it goes to adding then it goes back to
00:53:36.240
idle then it goes back to adding then it
00:53:38.819
goes back to idle but it goes to idle
00:53:40.920
because we added a task and here's the
00:53:43.559
unique ID when it was created the ID in
00:53:45.720
the title then we create another one and
00:53:48.359
which should be hello so you can see
00:53:49.800
there's two in there now so up here it's
00:53:52.079
changing the Sorting from A to Z so and
00:53:54.900
so let's say we don't want to do that we
00:53:56.339
instead just want to get the actual
00:53:57.900
state after we do all of this manually
00:54:00.359
so you can even do that as well so get
00:54:03.059
state so after we do all of this let's
00:54:05.040
just cancel log the current state God
00:54:07.079
there's only one that shows the final
00:54:09.180
State over here so that is basically the
00:54:13.380
store pattern specifically a very
00:54:15.059
functional approach to the store pattern
00:54:17.040
even more specifically like through the
00:54:19.319
lens of what Redux does so we covered a
00:54:22.740
lot of stuff this was a really dense
00:54:24.420
video you are probably gonna have to
00:54:26.400
re-watch it a couple of times I
00:54:28.200
encourage that you actually play around
00:54:29.400
with Redux a bit