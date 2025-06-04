00:00:00.000
now we have data attribute and then we
00:00:02.639
can also add Target and the target is
00:00:05.160
actually the element that we got up here
00:00:07.140
right so now it is getting those for us
00:00:09.300
let's just call that inner right and so
00:00:11.940
all that we do is it is selected I think
00:00:15.839
it is selected that just needs to be set
00:00:18.420
to whatever complete it is but here's a
00:00:21.900
problem and it is that it just knows
00:00:24.660
it's a generic HTML element it doesn't
00:00:27.240
know that it's actually an input because
00:00:30.060
we're just checking if it's an actual
00:00:31.740
generic HTML element and get HTML so we
00:00:34.440
might need to do another error here that
00:00:36.540
once again we throw early and loudly if
00:00:38.520
we are if we think something is wrong
00:00:40.140
and so what we can do is we can write
00:00:42.239
the following we can say we can check is
00:00:44.520
selected in inner over here but we need
00:00:48.059
to wrap it in double because we're
00:00:49.200
checking if it's not and if it's not
00:00:51.120
throw new error expected input element
00:00:55.559
so sometimes you might need to do
00:00:57.539
something like this because we're just
00:01:00.120
checking if it's a generic HTML element
00:01:03.359
we don't know what type you can get
00:01:06.299
stricter types so you can go for example
00:01:09.680
HTML input element as a type or
00:01:12.900
something but it it's just too much
00:01:15.299
effort I'd rather just solve it in this
00:01:17.760
way case the title so inner and in a
00:01:21.900
text sorry is equal to whatever gets
00:01:25.080
passed to title in our scrubs so we
00:01:28.680
let's pull that in and let's pull in
00:01:32.000
modules.js and let's pull in create task
00:01:35.640
so create task doesn't return anything
00:01:37.920
just yet it just adds it to the Dom and
00:01:40.740
I can see it did add it but the title
00:01:45.000
wasn't added we are actually getting
00:01:48.060
this error over here and so we had that
00:01:51.240
window error catcher thing previously
00:01:53.220
but I removed it so this is also so you
00:01:56.159
might be like ah damn it like it through
00:01:57.780
an error but keep in mind like this is
00:02:00.600
much better than actually if we perceive
00:02:02.759
it now we wouldn't have known like it
00:02:05.280
would just not have shown if it's
00:02:06.659
completed we wouldn't have known that
00:02:08.758
that behavior doesn't even work so we
00:02:11.340
just need to check for checked instead
00:02:14.520
but it's not adding the title and so
00:02:17.040
let's we never update you might have
00:02:19.379
seen me do this in what I've been stop
00:02:21.000
stop stop stop what are you doing and
00:02:23.700
once again I don't know why yeah I make
00:02:26.580
these stupid mistakes Okay cool so let's
00:02:28.440
Maybe by default say just remove these
00:02:31.800
disableds for now let's add a couple of
00:02:34.319
these so let's say create task create
00:02:37.080
task um write code and the due date is
00:02:40.739
right now so this is cool
00:02:43.620
um one thing though so here's a couple
00:02:46.019
of things and and we can get them just
00:02:47.940
straight from the Dom so I can just find
00:02:50.040
this but there's some other things that
00:02:51.900
are not actually being represented in
00:02:53.580
the Dom so what if we at a later Point
00:02:55.620
want to check what is the due date for
00:02:57.360
this but it's not being represented in
00:02:58.980
the Dom so we probably need some type of
00:03:02.519
object that we can work with and this is
00:03:04.200
where oop comes in so we create that
00:03:06.300
task and let's just call this you know
00:03:08.220
task one and call this one task two and
00:03:11.760
we might even want to be able to go task
00:03:14.220
two title is no no and if we set that it
00:03:19.260
should actually update here as well
00:03:21.000
probably already realize the way we're
00:03:22.739
going to do that is with Getters and
00:03:24.239
Setters let's first just return an
00:03:27.480
actual object currently there is nothing
00:03:29.760
there let's write an interface for our
00:03:32.400
tasks have it actually in our state
00:03:35.040
already and as you can imagine with oop
00:03:38.879
you actually move all of that into worth
00:03:42.780
the actual task itself so let's move all
00:03:45.360
of that in here okay so we'll Define all
00:03:47.400
of this up here and so let's create our
00:03:49.680
actual interface according to that so
00:03:53.280
what this should return is the actual
00:03:56.340
task so then the question is where do we
00:03:59.099
store these values because for example
00:04:01.319
we're definitely going to have an action
00:04:02.819
where if you click on it it's going to
00:04:04.379
show you more details and so let's
00:04:06.780
actually create the object that contains
00:04:09.420
these in our actual closure so before we
00:04:12.599
actually modify our HTML let's just do
00:04:15.120
it straight up in here just save all the
00:04:18.540
and let's just call it State you know
00:04:21.120
because effectively this is this of the
00:04:23.460
task if we want more type security we
00:04:25.860
can actually just explicitly say add
00:04:27.780
type task so this is the current state
00:04:30.060
we can just pass the props once again we
00:04:32.820
can just spread the props in there and
00:04:35.280
we can just add the ID which doesn't
00:04:37.919
come with the props and then also
00:04:40.020
because we did this it can actually tell
00:04:42.060
us what is missing so what is missing
00:04:44.419
completed and created so completed is
00:04:47.460
just false and created is literally when
00:04:51.840
we run this so created is created we can
00:04:55.560
literally just do new okay so this is
00:04:57.600
the internal state of the task we which
00:05:00.540
is not always what gets shown so for
00:05:02.460
example you can click on it to see more
00:05:04.740
info so you should be able to update the
00:05:07.080
due date or whatever even if the due
00:05:09.060
date isn't in the Dom anywhere at the
00:05:11.160
moment or update the title even if the
00:05:13.500
task itself isn't showing right now so
00:05:16.020
it's important to keep this in mind this
00:05:17.699
is a persistent in your app whether it's
00:05:21.000
currently showing on the screen or not
00:05:23.100
let do get and Setters for all of these
00:05:26.100
yet so you can get the ID and that is
00:05:29.280
just going to return state ID but you
00:05:32.759
can't update the IDE so what you can do
00:05:34.860
is you can just return nothing but I
00:05:37.500
would actually just throw an error in
00:05:40.020
here because you shouldn't try and do
00:05:42.300
this and if you're trying to do this
00:05:44.100
there's something wrong and why are you
00:05:47.220
trying to do this so I would actually
00:05:49.199
just say cannot directly change ID so we
00:05:53.880
need to pass a actual parameter here
00:05:57.000
even if we don't use it so let's just
00:05:59.759
say new value let's do get completed and
00:06:03.479
set completed get created it's obviously
00:06:06.780
going to be the exact same with set
00:06:08.580
created you cannot directly change
00:06:11.039
created obvious reasons and get credit
00:06:14.400
just return release date re-hate it set
00:06:18.120
completed so here we can actually do
00:06:20.820
something cool and we can actually just
00:06:22.139
say if the new value equals what the
00:06:26.340
current value is so if you're trying to
00:06:28.080
set it to true and it is already true
00:06:29.940
then just don't do anything because
00:06:31.740
theoretically then it is set to true
00:06:33.720
because it was true so if it is the same
00:06:35.819
just return don't do anything just
00:06:38.400
return State completed okay otherwise
00:06:41.400
State completed equals new value this
00:06:44.819
gives you rate tight control around the
00:06:47.039
interface of your actual object let's
00:06:50.580
just pass that in there even if we don't
00:06:52.259
use it and completed created so do we
00:06:56.460
can even put validation in here if we
00:06:58.620
want we can even say that you know if
00:07:00.780
new value type of new value it's not
00:07:04.139
equal to Boolean Pro new error is not a
00:07:08.699
Boolean get title and that is just going
00:07:11.580
to return State title so when people
00:07:14.400
illustrate like Getters and Setters they
00:07:16.500
they always do stuff like you know so
00:07:18.360
you have something called first name and
00:07:20.639
last name and then you create a getter
00:07:22.440
that is like full name that just
00:07:24.599
combines the two or whatever and I find
00:07:27.599
those super contrived um it's like I
00:07:30.240
don't know like I don't like I think
00:07:32.099
initially when I was learning about
00:07:33.479
Getters and said is I didn't really see
00:07:35.280
the value in that to me this is a much
00:07:38.039
more useful
00:07:40.259
um actual use case where it allows you
00:07:42.120
to control the interface and actually
00:07:44.580
allows the way that people can inter
00:07:46.860
interface with this actual object and
00:07:49.740
what they're allowed to do all right so
00:07:51.720
let's also just do set title and we can
00:07:54.120
also put a couple of conditions in here
00:07:55.979
we can say if it isn't a new value if
00:07:58.560
there's no new value then obviously
00:08:00.120
throw an error or if type of not a
00:08:03.240
string or if new value is empty then
00:08:06.539
throw new error title is required to be
00:08:12.479
a non-empty trim which for his actual
00:08:16.620
function that we run once again like
00:08:18.300
this is thank you tsj let's just add
00:08:21.240
urgency and set urgency and we can
00:08:23.580
actually just and create a valid array
00:08:27.419
of urgency autocompletion here and we
00:08:31.740
can just say valid includes new value so
00:08:35.820
if the new value isn't one of these then
00:08:38.640
it's going to throw an error so we can
00:08:40.080
say if so by default it's also then if
00:08:42.599
it's a if it's not a string if it's
00:08:44.219
empty or whatever then obviously by
00:08:45.720
default it's not going to be any of
00:08:47.279
these so we don't need to do those extra
00:08:49.620
checks Pro new error which is valid is
00:08:55.279
required to be high low and this is
00:08:59.760
unhappy because so I'll get back to that
00:09:03.060
in a second let's just move on I think
00:09:05.100
all that's left now is due so let's say
00:09:07.800
get you and set you you can do the exact
00:09:10.800
same here where if new value instance of
00:09:14.399
date so if it's not a date in Throne
00:09:17.279
error throw new error du is required to
00:09:22.500
be a date and then you just State all
00:09:25.860
right let's add some commas here also
00:09:28.260
some commas up here
00:09:31.320
urgency so I actually just noticed you
00:09:34.140
might have been yelling at me all this
00:09:35.580
time
00:09:36.480
um I'm returning the title which is why
00:09:38.700
did it make sense I I couldn't for the
00:09:41.279
life of me figure out why is this
00:09:43.620
unhappy and so that's once again you
00:09:46.080
know that's the value of static typing
00:09:48.060
otherwise I might not have picked that
00:09:50.040
up all right let's give this a go okay
00:09:51.839
so write code watch the dog so we are
00:09:54.420
getting these Task 1 and task two back
00:09:56.640
now so task one and we set it to hello
00:10:00.740
so it's not updating so let's go in here
00:10:04.380
and let's also this is also what's
00:10:06.180
really cool about Setters and Getters is
00:10:08.399
that even in here let's we can console
00:10:10.920
log the new value so if you have any
00:10:13.019
errors or whatever say log when someone
00:10:16.440
tries to update this thing so it makes
00:10:18.779
debugging a bit easier though right so
00:10:21.720
it actually shows when we set that but
00:10:24.000
it doesn't update here and the the
00:10:26.220
reason is it updates the state but we
00:10:29.339
need to manually update the HTML and if
00:10:31.860
you're using Getters and sellers you can
00:10:33.480
actually do that as follows you can just
00:10:35.640
ensure it gets set here the HTML gets
00:10:39.180
updated as well so we can actually just
00:10:41.459
go HTML update HTML task so the areas
00:10:45.600
where it should have an influence is
00:10:47.459
when you update completed so update task
00:10:51.540
and you just we just set completed to
00:10:54.180
the new thing obviously we don't want to
00:10:56.160
de-structure props in there and
00:10:58.380
obviously you want to say new value and
00:11:01.019
then we also need to make sure so we
00:11:03.180
don't have anything like this in the
00:11:04.500
HTML just yet title so we need to make
00:11:06.839
sure as well and we actually never
00:11:09.180
updated the state here new value let's
00:11:12.060
update the title as well over here so
00:11:14.579
we're kind of having this entire object
00:11:16.680
managed like the HTML state for us and
00:11:19.380
and everything
00:11:20.760
urgency is not being shown cool it
00:11:22.920
changed it to hello and so let's
00:11:25.620
actually see that in action if we set a
00:11:28.380
timeout and only do that after like two
00:11:31.140
seconds okay watch the dog and then
00:11:33.060
three seconds there you go so you'll see
00:11:34.860
if you did it automatically you said
00:11:36.800
cubes.html and the actual object itself
00:11:40.920
in sync what we would actually end up
00:11:43.200
doing is we'll probably just put these
00:11:45.300
in an array so we'll just say we have
00:11:49.320
this array of tasks and then that's
00:11:52.079
obviously just going to be easier to
00:11:53.940
access let's just say list we need to
00:11:56.399
wrap that in rehire task all right so
00:11:59.040
you'll see probably this is very similar
00:12:00.779
to what we did with our events okay I
00:12:04.620
also just want to check something so
00:12:05.940
let's do list and let's say the second
00:12:07.680
one remember arrays or zero index so the
00:12:10.680
second one and let's set completed to
00:12:13.320
false oops I actually mean true hey
00:12:16.440
there we go check that out just add a
00:12:18.660
couple more here let's just say do
00:12:21.360
dishes learn JavaScript but so at the
00:12:24.420
moment we don't have a way to manually
00:12:28.980
add tasks so we kind of do it like this
00:12:31.140
so ideally we want to be able to
00:12:32.940
manually do that so I'm just going to
00:12:34.800
write that in here quickly Let's uh just
00:12:37.500
do quickly const uh create adding HTML
00:12:41.820
so what that is going to do it's going
00:12:44.220
to do two things for me it's going to
00:12:46.079
create a button for me that we are going
00:12:49.740
to insert here underneath app title and
00:12:53.040
let's just do an area and let's call it
00:12:54.980
data okay so that is where that is going
00:12:57.899
to go import from modules helpers so
00:13:02.040
we're going to do get HTML and let's
00:13:04.740
just get the element itself so get HTML
00:13:06.959
so we created adding what we're going to
00:13:10.200
do is in that element a pen child and
00:13:13.980
let's just put a single so so what we're
00:13:16.260
going to do is we're going to create a
00:13:17.339
fragment where we are going to add two
00:13:20.040
things to it so fragment is eventually
00:13:22.019
just a fragment is basically just a
00:13:24.380
placeholder for things that where you
00:13:27.300
can put the HTML on that would be a
00:13:29.820
document fragment okay and so the first
00:13:33.600
thing we're going to add on that
00:13:35.100
fragment is we're going to create a
00:13:36.959
button and document create element let's
00:13:40.920
just do a button and let's also add a
00:13:42.600
class I think we have class names I
00:13:45.060
think we have a button class if I'm not
00:13:47.639
mistaken I'm just going to add that on
00:13:49.200
there and the inner text is just going
00:13:52.740
to be and so let's actually add that to
00:13:56.639
our fragment quickly I actually realized
00:13:58.740
we actually don't need the fragment we
00:14:00.300
can just add it to the element directly
00:14:02.100
I don't know what I was thinking Okay
00:14:03.360
cool so there we go and let's actually
00:14:06.000
just run create adding HTML and and we
00:14:09.300
we never actually set up TS check up
00:14:12.000
here there we go let me actually show
00:14:14.279
you how you can enable it for everything
00:14:16.560
the way you would do that is be great by
00:14:19.200
creating a TS config file so tsconfig
00:14:22.519
dot Json I am going to speak much more
00:14:26.459
about this much more about typescript
00:14:28.440
you might have heard typescript now
00:14:29.940
being mentioned a couple of times but
00:14:32.519
now all you need to understand is that
00:14:34.440
vs code you might not get this in other
00:14:37.320
Ides vs code uses typescript under the
00:14:41.100
hood to do your static type checking for
00:14:43.500
you that's all you need to understand
00:14:44.880
now you don't need to know anything
00:14:46.199
about typescript so this is why this
00:14:48.660
word typescript keeps on look at it much
00:14:51.060
later when we look at something like
00:14:52.980
angular also compiler options not only
00:14:55.920
do we allow JavaScript so true but we
00:14:59.040
actually check the JavaScript that's
00:15:01.380
automatically you're just going to check
00:15:02.820
all JavaScript whether we have TS check
00:15:05.279
at the top or not and this is just
00:15:07.260
unhappy because obviously we move these
00:15:10.620
out of the state over here I can just
00:15:13.320
disable this we're not using State at
00:15:15.959
the moment we're just using tasks and
00:15:17.760
obviously so we no longer need this
00:15:19.139
because this is not actually in the task
00:15:20.579
itself yes so you also we also need to
00:15:22.980
say what version of es we're using so
00:15:27.240
you remember like when we spoke about
00:15:28.680
JavaScript we spoke about ecmascript we
00:15:31.380
also need to say a Target definitely not
00:15:34.740
ES3 it actually shows you all the ones
00:15:36.540
let's go like es2017
00:15:39.779
um it's just so it's widely supported
00:15:41.399
obviously if you go this current year
00:15:44.519
that spec hasn't even been finalized yet
00:15:47.160
so no browsers are going to support it
00:15:49.079
so obviously the further back you go the
00:15:51.240
more browsers are going to actually
00:15:52.500
support it sir so what it effectively
00:15:55.199
told us that this is also what's really
00:15:56.519
cool is it effectively told us like
00:15:59.160
because it was targeting ES3 it told us
00:16:01.800
like includes doesn't exist for it to do
00:16:04.380
proper type checking for you as well you
00:16:06.660
also need to tell it what version of
00:16:08.459
JavaScript are you actually assuming
00:16:11.279
remember this isn't going to compile
00:16:13.079
this isn't going to create that for you
00:16:14.940
it's going to depend on the browser but
00:16:16.860
what is the lowest version that you're
00:16:18.899
aiming to support and let's get rid of
00:16:21.180
that and so let's go back to here so top
00:16:24.720
string is not okay cool so I we would
00:16:27.360
have gotten that error if we had type
00:16:29.820
checking enabled by default all right
00:16:31.680
cool so add task and so what we also
00:16:35.399
want to do is we want to add a modal as
00:16:38.940
well I think I have one that we can use
00:16:43.139
in here to copy that it has all the
00:16:46.199
stuff in that we need so let's also just
00:16:48.720
create that and append it so document
00:16:51.500
create element
00:16:53.940
dialogue in HTML set it from here one
00:16:57.720
thing you'll see is that it the prettier
00:16:59.940
doesn't unfortunately do formatting for
00:17:02.699
you on this because it's technically a
00:17:04.619
string even if we do get the syntax
00:17:08.160
highlighting and then let's just say
00:17:10.140
element add append child and that would
00:17:15.000
be dialogue doing that oh because
00:17:17.880
obviously we have the dialogue inside
00:17:20.040
the dialog we need to instead dialog
00:17:23.459
class name and let's also just set it to
00:17:26.280
open open true and class layer is just
00:17:29.460
overlay okay and let's just remove these
00:17:32.100
wrapping things and now it should
00:17:33.780
actually show up and it should be open
00:17:36.179
all right so okay so let's just change
00:17:39.120
this to say add task remove the message
00:17:43.200
for now I think it's clear what you need
00:17:44.820
to do and as mentioned the design of
00:17:47.580
this isn't the prettiest but like we're
00:17:49.380
here to learn JavaScript so I just made
00:17:52.500
something basic that we can work with
00:17:55.080
what we have is we have title and you
00:17:58.020
know let's for now just leave all the
00:18:00.240
other things
00:18:01.679
um I just want to show you just do the
00:18:03.960
single thing so let's
00:18:06.360
um create this quickly let's do adding
00:18:09.780
dot JS and let's move all the stuff we
00:18:12.780
created right now into adding once again
00:18:16.020
like the goal here is to keep things
00:18:18.360
decoupled so as far as possible adding
00:18:21.299
should know as little about tasks as
00:18:24.120
possible and then what is also nice with
00:18:26.340
the Imports is like you can actually see
00:18:28.500
now it doesn't know anything about tasks
00:18:31.320
okay because we're not importing
00:18:32.940
anything about tasks all right so let's
00:18:35.520
pull in adding and let's say export cons
00:18:39.419
create adding and that is just going to
00:18:41.760
fire off this HTML for now and it tells
00:18:45.179
us once again that it's a good idea to
00:18:47.400
if we only have a single thing to do a
00:18:49.320
default pull that in here let's get rid
00:18:51.960
of all of this you can already see here
00:18:54.539
how we're starting to work with like
00:18:56.640
higher level like abstractions over here
00:19:00.000
okay cool so there are no tasks at the
00:19:02.220
moment so let's go into adding right so
00:19:04.860
we're not doing much with it just yet
00:19:06.539
but this one is a bit different because
00:19:08.580
we're not just displaying information we
00:19:11.400
actually want to react to events so
00:19:13.919
actually this shouldn't be the lead it
00:19:16.440
should actually be add task or save or
00:19:19.679
whatever so we want to also now start
00:19:22.679
using event listeners as well so what
00:19:25.559
we'll probably do is when we create the
00:19:28.080
HTML we'll also attach an event listener
00:19:30.780
so let's actually start the dialog as
00:19:33.720
closed by default it should be we don't
00:19:36.179
even need to set dialogue okay and then
00:19:38.700
obviously when we click the add task we
00:19:41.220
want it to actually show the dialog so
00:19:44.460
then after we create it let's actually
00:19:46.740
add our event listeners so we can go
00:19:49.260
let's just get the actual adding itself
00:19:52.080
after we create it and document query
00:19:55.679
select but an easier way might actually
00:19:58.080
be to just straight up export it from
00:20:00.539
here so let's actually just return their
00:20:02.940
references remember these are references
00:20:05.039
uh they because Dom elements are
00:20:07.440
theoretically objects they just retain a
00:20:10.200
reference these are not actually the
00:20:12.480
object itself it's just a reference to
00:20:15.480
where the object lives in memory okay so
00:20:17.940
that's actually it saves us this so
00:20:20.760
let's actually have a look and let's
00:20:22.380
launched and we should be able to even
00:20:24.360
destructure it straight from there so in
00:20:26.760
this case
00:20:27.720
um it was smart enough to actually know
00:20:29.640
uh that we didn't even have to mark up
00:20:32.160
the Jazz Doc it's smart enough to figure
00:20:34.260
it out itself so in those cases I won't
00:20:36.600
actually even mark it up where I will
00:20:38.580
mark it up is when like for example here
00:20:41.880
it's the main thing that I'm exporting
00:20:44.160
and I want super tight control what
00:20:46.740
people can do with it add event listener
00:20:49.260
and what that is going to do is because
00:20:51.660
we already have the reference to
00:20:53.100
dialogue we can do dialogue open is true
00:20:56.220
there we go opens it up for us and then
00:20:58.080
cancel maybe closes it for us we don't
00:21:00.600
have a reference here to that but what
00:21:02.640
we can do data cancel and data save and
00:21:06.780
then we can actually just return them
00:21:08.160
here as well so let's just do save and
00:21:11.100
cancel we can just go dialogue we select
00:21:15.000
the data save okay so this makes it a
00:21:18.059
lot more a lot easier so now we can all
00:21:20.280
just go so let's pull those out as well
00:21:23.280
so cancel and save add event listen and
00:21:26.940
it just does the exact hey check this
00:21:29.220
out another thing that you'll see is uh
00:21:31.980
there's actually this weird thing in
00:21:34.200
JavaScript where if you want the like it
00:21:36.600
to have a dark background you need to
00:21:39.059
actually show modal like that and I
00:21:41.880
can't remember what the opposite is it's
00:21:45.120
actually just close yeah now what we
00:21:47.700
want to do is when you click save what
00:21:49.500
happens so let's make save the actual
00:21:53.100
submit button so that actually means
00:21:55.559
let's put the event listener on the form
00:21:57.780
itself these aren't actually even in a
00:22:00.419
form wrap them in a form a form is just
00:22:03.480
one element and let's just do data form
00:22:06.320
instead of data save and this is just
00:22:09.539
type submit and it is for this form
00:22:13.440
needs a ID and let's just call it adding
00:22:17.580
and it is to submit adding once again
00:22:20.280
you might need to format this by hand
00:22:23.059
pretty as unfortunately not going to do
00:22:26.220
it for you and I see it already messed
00:22:28.559
up the indentation so let us continue we
00:22:31.919
want to listen for a submit event and
00:22:35.520
also save it should be form and we
00:22:38.280
should look for data form and we should
00:22:40.500
look for a submit listen for a submit
00:22:42.659
event on that so add event listener
00:22:45.000
submit and this is the event and let's
00:22:49.080
do event prevent default for now or
00:22:51.900
whenever pulling that out okay and let's
00:22:55.620
just console log that to see that it
00:22:57.960
actually fires when we submit close the
00:23:00.240
dialog when we submit I actually got it
00:23:02.880
wrong it's actually not submitted form
00:23:04.860
so now we want to do something with that
00:23:07.500
title and we want to well let me bring
00:23:11.159
in the whole package so let's actually
00:23:13.440
do
00:23:14.580
so the name of this input is title let's
00:23:18.780
bring in the other one so there is due
00:23:22.440
this is
00:23:24.600
urgency and urgency we want to transform
00:23:27.419
into a select list this is three that
00:23:30.659
you can choose from with the default
00:23:33.059
being the medium and high and low and
00:23:39.299
let's just ensure that this responds
00:23:41.880
with actual values that we have and so
00:23:44.340
do so this urgency isn't is required but
00:23:48.000
it say it is required but this is not an
00:23:50.340
issue because it's set to medium by
00:23:52.140
default title is also required and du is
00:23:55.860
not required so it won't even let us
00:23:58.020
submit without that du is the actual
00:24:01.200
type is actually date select the date
00:24:04.500
title and that and save and effectively
00:24:08.520
now it should create tasks for us all
00:24:12.480
right so then the question is is how if
00:24:16.200
we're not allowed to bring tasks in here
00:24:19.860
and assume tasks if we want to keep
00:24:22.080
these decoupled from one another and so
00:24:24.600
what we can do is we can just say that
00:24:26.940
you can set all back on this actual
00:24:29.520
object so let's say let's create our
00:24:32.400
type def so for adding itself the moment
00:24:36.380
all that it returns is Mission and that
00:24:41.100
is just a callback that will be
00:24:42.780
submission and let's create that up here
00:24:45.240
at callback submission and what a
00:24:48.840
submission do submission just turns what
00:24:52.679
actually gets submitted and so what
00:24:54.960
actually gets submitted type def listens
00:24:58.140
to data which is an object and prop so
00:25:02.340
that is the title which is has to be a
00:25:06.360
string and also prop not props a date or
00:25:10.200
null which is due and once again here I
00:25:12.780
will just duplicate it because remember
00:25:14.460
remember as if you share as little as
00:25:17.400
possible between your actual objects the
00:25:22.020
better okay so and then we can just say
00:25:25.080
urgency okay and so the submission all
00:25:27.480
that that does is takes a param data
00:25:31.140
which is the shape of that data okay
00:25:33.120
there we go if we try and submit so
00:25:36.059
obviously we need to now do state as
00:25:38.220
well and just submission again
00:25:40.740
submission starts as undefined and so
00:25:43.260
what we can just say over here if State
00:25:46.500
submission doesn't exist or even this is
00:25:50.340
a type of is not a function then we just
00:25:53.460
throw a new error that is submission
00:25:56.960
value has to be set as function so you
00:26:01.380
can't submit until that is set and let's
00:26:04.559
just do returns adding okay so obviously
00:26:07.500
it's unhappy so submission let's do our
00:26:10.260
Setters and I'll get this set submission
00:26:12.720
and get submission so so it's a return
00:26:16.200
State and set submission just takes the
00:26:19.559
new value and state the mission equals
00:26:23.159
the value okay so the reason why it's
00:26:26.760
useful to keep these decoupled is let's
00:26:28.799
say maybe we want to do something with
00:26:30.659
the actual values before then transform
00:26:33.600
it beforehand or something so create
00:26:35.820
adding so let's just have our adding
00:26:38.100
here and then on adding we go submission
00:26:41.580
and let's just say that is a function
00:26:44.480
DOTA and this is console log the data
00:26:48.480
and so we should also remember to
00:26:50.460
actually just call it we can get it from
00:26:53.279
the form by going const entries and
00:26:56.460
let's just say new form data and we pass
00:27:00.240
event Target so we get that then we
00:27:03.299
convert it into actual object from
00:27:07.440
entries take the entries send it into
00:27:10.500
response and we we need to bump this up
00:27:12.900
a little bit I don't think it's
00:27:13.860
supported in that so this goes like 2020
00:27:15.960
event Target let's also just check if if
00:27:20.640
there is no event Target throw new error
00:27:24.059
but I think it also needs we need to
00:27:26.520
check actually if it is a form so we
00:27:29.100
actually need to say if event Target not
00:27:32.400
an instance of HTML form cool because
00:27:36.000
obviously you can only pass a form to
00:27:37.679
form data the response just take what we
00:27:41.039
have and let's then run submission on it
00:27:44.220
so this is the Callback that we sent oh
00:27:47.039
State submission console add task there
00:27:50.279
we go save and what we will do is we
00:27:54.240
will just say in response every time
00:27:56.760
this form is submitted just take that
00:27:59.340
pass it to create task you can even
00:28:02.940
pause create tasks directly in us that
00:28:06.600
as the function that should be run so in
00:28:09.960
adding when we actually before we close
00:28:13.080
we should just take the actual Target
00:28:15.539
itself so event and just reset it in
00:28:18.720
other words clear everything okay and
00:28:20.880
hello all right so I hope that was
00:28:23.940
helpful in terms of I'm just going to
00:28:25.740
remove the state here because obviously
00:28:27.840
we are no longer using that so we can't
00:28:30.360
keep helpers like this um a lot of
00:28:32.460
people actually put helpers in like have
00:28:35.880
almost like a create helpers as well uh
00:28:39.480
like here
00:28:40.620
um I don't know I just pull them
00:28:42.120
directly from the module if you want to
00:28:43.740
be like super strict oop then
00:28:46.260
technically so the big problem at the
00:28:49.260
moment is that we don't get full
00:28:51.840
encapsulation so we do get encapsulation
00:28:54.179
in the abstract sense so you know like
00:28:56.460
with adding like there's only one thing
00:28:58.380
that we can do with it and you know
00:28:59.940
likewise if we were to create a task
00:29:02.279
here you know like we are working with
00:29:04.559
the interfaces here so to control and
00:29:07.440
make sense of the high level things that
00:29:09.120
are happening even if you have no idea
00:29:11.100
what's actually happening in the task
00:29:12.840
file you can just work with these
00:29:15.299
abstractions so technically speaking we
00:29:18.299
don't have full encapsulation here from
00:29:20.340
a software point of view because there's
00:29:23.399
things in other files that you can
00:29:25.080
actually do that can influence them for
00:29:27.360
example I can go back around red Here
00:29:29.580
and Now changes something that should
00:29:32.220
actually be confined only within this
00:29:34.260
object and likewise I can go document
00:29:37.140
you know query selector so I can
00:29:39.840
completely circumvent all of this and I
00:29:41.460
can go hey you know what like actually
00:29:43.380
get me the an a the H2 which is this so
00:29:48.539
get me any H2 on the page just change
00:29:51.480
the inner text to something else you
00:29:54.419
know hey and now it's actually changing
00:29:55.980
so it's very easy to to accidentally
00:29:58.320
even like Target the wrong thing or
00:30:00.840
whatever so it would be really nice if
00:30:02.760
we can encapsulate everything in a
00:30:05.580
single object and this is going to
00:30:07.320
become something that we're going to
00:30:09.299
speak a lot of Frameworks as well and
00:30:10.860
and that is like in modern like software
00:30:13.860
so there's this traditional idea to
00:30:15.659
separate your CSS and your HTML and your
00:30:18.360
JavaScript uh into kind of layers but
00:30:21.960
when you're building like web apps that
00:30:24.899
is very hard to have all those things
00:30:27.899
spread out and if you want to take a
00:30:29.940
truly oop approach like then
00:30:32.820
theoretically you want everything so in
00:30:35.039
other words if you press delete and this
00:30:37.380
button adding is gone you can't use
00:30:39.659
adding anymore everything for adding is
00:30:42.000
in this file if you create it here this
00:30:44.700
creates everything that you are allowed
00:30:46.740
to do with adding but now you have like
00:30:48.840
all this other stuff spread out like in
00:30:50.880
your Styles file and also you can
00:30:53.520
directly like Target it through the Dom
00:30:56.159
regardless of what we do in this actual
00:30:59.039
object what interface we give here
00:31:00.899
someone can just go I don't care about
00:31:02.279
this I'm just going to directly change
00:31:03.779
it and not not even maybe even
00:31:05.820
intentionally maybe accidentally so in
00:31:07.799
the next lesson we're going to look at
00:31:09.720
how web components allow us to solve
00:31:12.419
that by using inheritance and that is
00:31:16.440
where we where I finally actually show
00:31:18.360
you how to do this with classes because
00:31:20.880
the way the web components API is built
00:31:24.120
means that you need to use classes
00:31:26.460
unfortunately it doesn't work with
00:31:28.440
Factory functions
00:31:29.880
what some people do is they actually
00:31:32.100
wrap the web component classes in
00:31:34.679
factories we can even look at maybe
00:31:37.260
doing that
00:31:39.120
um if there is time but so a good
00:31:42.840
example is is this a library called
00:31:46.140
hybrids which as you'll see actually
00:31:48.899
allows you to create web components
00:31:52.080
um by just running this Define Factory
00:31:54.059
yeah you won't know what any of this is
00:31:57.419
um we are going to talk about it in the
00:32:00.059
next lesson but so the point being that
00:32:02.580
you can actually do web components and
00:32:04.860
Factory functions but natively
00:32:07.760
unfortunately the way it works you need
00:32:10.980
to use classes and that is just the API
00:32:13.559
limitation that is just what tc39
00:32:17.220
decided how it is going to work all
00:32:19.860
right so I will see you in the next
00:32:21.539
lesson