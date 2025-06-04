00:00:00.000
what I want to do is let's just say vdom
00:00:03.419
I want to show you a very basic
00:00:05.759
abstraction that a lot of Frameworks use
00:00:08.039
the reason for that abstraction is
00:00:11.099
because we realized there's a lot of
00:00:13.799
value in expressing our user interfaces
00:00:17.340
in a functional manner so that would
00:00:19.440
mean you know if we think about
00:00:20.580
immutability if we think about purity
00:00:23.220
and all those things that our data is
00:00:25.560
unidirectional so let's say here's our
00:00:27.720
data there's some type of transformation
00:00:29.460
that happens then you know that is a
00:00:32.520
specific HTML and so where a framework
00:00:35.399
like react was very revolutionary it
00:00:38.040
said that whenever anything changes this
00:00:41.280
just keeps on running and that results
00:00:43.200
in the new UI State okay so all you do
00:00:46.140
is you just change the data so the data
00:00:48.780
just goes from one state to another
00:00:50.280
state and that just forces a re-render
00:00:52.980
and it changes what gets shown this is
00:00:55.559
much more useful than what's called
00:00:57.480
two-way data binding and other some
00:00:59.520
Frameworks do do two-way data binding
00:01:02.219
but they have some type of functional
00:01:04.920
expression of your HTML to make up for
00:01:07.680
that so what two-day data two-way data
00:01:10.439
binding would be you know it can go both
00:01:12.600
ways it's like something in the HTML
00:01:14.280
changes and you need to sync it with
00:01:15.900
your data something in the data changes
00:01:17.820
you need to sync it so you have to keep
00:01:19.200
these two states in sync all the time
00:01:21.900
what unidirectional data flow means in
00:01:24.420
terms of functional programming in other
00:01:26.220
words you can't mutate things you can't
00:01:27.720
go back and change things means that
00:01:29.880
this is your source of Truth so if you
00:01:31.500
think about Redux you know your single
00:01:33.060
source of Truth and that is very easy to
00:01:35.159
debug because if something's happening
00:01:36.780
you can just listen in here and check
00:01:38.759
what's happening whereas over here you
00:01:40.979
don't know what direction it's flowing
00:01:42.540
you don't know if this is going up the
00:01:43.920
chain and then something else comes down
00:01:45.420
the chain again and you don't know what
00:01:47.640
actually corresponds with what because
00:01:49.020
it flows in both directions it's just
00:01:51.360
like a single pipe and every time it
00:01:53.220
just updates
00:01:54.420
so the HTML itself is a side effect it
00:01:57.420
doesn't actually have any state within
00:01:59.820
itself you only have state here and what
00:02:02.759
gets rendered in your view is just a
00:02:05.399
side effect of changes in your data
00:02:07.200
instead of having a state here and a
00:02:09.598
state here maintaining two different
00:02:11.038
states and keeping them in sync so you
00:02:13.500
might also be asking okay why don't we
00:02:15.599
just do it this way around why I keep
00:02:18.000
all our state in HTML and just
00:02:19.980
completely forego having our state like
00:02:22.980
in an object somewhere so the the big
00:02:25.260
problem comes that at some point in
00:02:28.379
order to do something with your app
00:02:30.840
state do something with your data you're
00:02:33.120
going to have to have that in an actual
00:02:35.580
data structure you can't save an entire
00:02:38.640
HTML Tree in local storage you can or if
00:02:42.780
you can't send an entire HTML tree to
00:02:45.420
the server at some point you need to be
00:02:47.519
able to send something like an array of
00:02:49.739
tasks okay so I just briefly that's what
00:02:51.959
I know I'm going to go into it in a
00:02:53.280
modern a lot more depth in in in the
00:02:55.140
next part but I just want to show you
00:02:56.940
like a very basic abstraction and how we
00:02:59.400
would do something similar ourselves the
00:03:01.319
big problem at the moment as you
00:03:03.360
probably saw over here is that we can't
00:03:05.940
express actual state in a declarative
00:03:08.940
manner We call we need to manually sync
00:03:11.940
up our HTML and make HTML changes by
00:03:15.780
manually looking at the two-store states
00:03:19.019
we can't there's no declarative way to
00:03:21.599
do it so we need to do all these
00:03:23.099
mutations so already this goes against
00:03:25.680
functional programming in functional
00:03:27.599
programming the goal would be to just
00:03:29.940
treat HTML changes as the result of a
00:03:33.360
function and that function is usually
00:03:34.739
called render okay so you pass something
00:03:37.080
to render and that returns you know a
00:03:39.959
new HTML for you and every time you run
00:03:42.360
this it just updates HTML and given the
00:03:44.940
same input it always gives you the same
00:03:47.040
response so before we get into this I
00:03:49.560
just want to show you this principle um
00:03:51.840
this isn't react specific but just
00:03:54.000
because we're Act is so flip and popular
00:03:55.860
there is a lot of related to this that
00:03:58.560
is react specific so let me show you so
00:04:01.140
this is a really great um I'm going to
00:04:03.540
touch on it super lightly we're going to
00:04:05.040
get into it in more depth uh once we get
00:04:07.680
to react specifically
00:04:09.599
um I will include it as a link if you
00:04:11.220
want to check it out but keep in mind
00:04:12.780
the principles that I want to pull out
00:04:14.340
here is related to this Frameworks in
00:04:17.699
general and how we can actually do our
00:04:20.940
HTML in a more functional programming
00:04:23.520
way than a strict oop way so it kind of
00:04:27.000
speaks a bit about the history of
00:04:29.040
Frameworks as well and this is also once
00:04:31.259
again something we're going to go into
00:04:32.160
into much more depth so it talks about
00:04:34.259
jQuery talks about backbone it talks
00:04:36.060
about angularjs which all of this came
00:04:39.120
before a lot of the current generation
00:04:40.800
offering so effectively it says this is
00:04:43.320
how we used to do it so this is what
00:04:45.120
we've been doing up until now we
00:04:47.040
actually kept our state separate from
00:04:49.800
our UI but then we had to manually
00:04:52.860
resolve the changes so you you can
00:04:54.720
actually see here it shows how you kind
00:04:56.820
of go through the Dom you find the
00:04:58.800
things and you ensure that your Dom
00:05:00.479
reflects what is going on in your state
00:05:03.240
you'll see how it kind of traverses the
00:05:04.860
Dom and you know and then it puts a
00:05:06.419
thing over there and then you make
00:05:07.680
another change and it goes through the
00:05:09.300
Dom again and then we manually put it in
00:05:11.400
there so this is what we have done up
00:05:13.380
until now but then people like started
00:05:15.240
realizing sure this is a lot of work
00:05:16.680
that for example looping over all the
00:05:18.960
tasks checking what has been added what
00:05:21.360
hasn't been added and then manually
00:05:22.979
updating the Dom and HTML sure this is a
00:05:25.620
lot of work so then people started
00:05:27.300
looking at are there actual ways in
00:05:28.979
which you can abstract that away and
00:05:31.199
actually get a library to actually
00:05:34.139
figure out how or idea of a store or a
00:05:38.340
state as a purely abstract thing
00:05:40.320
translates into HTML this is where we
00:05:43.440
got backbone I would probably say that
00:05:45.419
backbone is the first actual JavaScript
00:05:47.759
framework that we got some people might
00:05:49.919
disagree some people might say something
00:05:51.360
like dojo and so forth um I would say
00:05:53.580
backbone was the first first one I've
00:05:55.139
actually worked with backbone a bit in
00:05:57.120
retrospect now given the Frameworks you
00:05:59.639
have now backbone is a pain to work with
00:06:01.620
but at that time it was magical so what
00:06:04.680
backbone did it looked at how a lot of
00:06:06.780
back end languages solved some of these
00:06:09.180
problems and so we spoke about the model
00:06:11.400
and we spoke about the view so
00:06:12.660
effectively the model is our Redux store
00:06:15.060
it's the state of our app the view is
00:06:17.699
kind of what gets shown to a user and
00:06:20.220
then it kind of borrowed this idea of a
00:06:21.960
controller from a lot of back-end
00:06:24.419
languages it actually even says here
00:06:26.460
backbone invented the model view
00:06:28.020
controller pattern that's a joke that is
00:06:30.360
a joke like this comes from the world of
00:06:31.800
back-end development so languages like
00:06:34.259
Python and so forth but it was the first
00:06:36.900
popular JavaScript framework that
00:06:38.880
embraced the traditional software design
00:06:40.560
pattern and bought it to the web so
00:06:43.080
let's see what that actually does so
00:06:45.060
here we can look at an example so
00:06:47.160
effectively these are our models so you
00:06:49.440
can think about these as actual Redux
00:06:51.240
stores and then you bind it up so you
00:06:54.120
don't need to care about what happens
00:06:55.620
here you just update your store and then
00:06:58.319
it ensures that your view does what is
00:07:01.020
supposed to do based on if you add a new
00:07:03.419
task or whatever you know and if you add
00:07:05.280
something here it updates it for you so
00:07:07.740
the key is you don't need to every time
00:07:09.539
you add something new go through the Dom
00:07:11.819
like this and you know do every little
00:07:14.520
thing manually check everything update
00:07:16.259
every little thing manually okay but
00:07:18.479
this was a lot of work if you thought
00:07:20.520
Redux was a lot of boilerplate and a lot
00:07:22.740
of extra code you know the joke here is
00:07:24.720
in Just 2 000 lines of code backbone
00:07:26.819
allowed you to decouple your application
00:07:28.440
state from the Dom so we got this but it
00:07:30.780
was a pain so instead of living in the
00:07:33.120
Dom Backbone State lived inside models
00:07:35.940
so whenever a model changed all views
00:07:38.759
that cared about that model would
00:07:40.620
re-render and we can do something
00:07:42.599
similar in our app but there are some
00:07:44.699
trade-offs I'm going to show you that in
00:07:46.259
a second then we got angular J is an
00:07:49.139
angular Sid this is just too much work
00:07:51.720
it's over complicated and so forth and
00:07:53.880
it effectively said instead of having
00:07:55.680
your UI be a side effect of your data
00:07:58.259
let's keep let's treat these as two
00:08:00.539
states and use angularjs to keep those
00:08:04.740
two in sync the two-way data binding so
00:08:07.380
what angularjs said and keep in mind
00:08:09.599
this is angularjs is different from
00:08:12.419
angular today a lot of people fall into
00:08:14.580
that trap so effectively you've got
00:08:16.560
angular 2 you know three four five
00:08:19.379
whatever and this is kind of the modern
00:08:21.419
versions of angular there's a joke that
00:08:23.580
Google effectively created a completely
00:08:25.919
new framework but they just kept the
00:08:27.419
angular name so the general consensus
00:08:29.940
angularjs which is effectively known as
00:08:32.640
you know angular one is a completely
00:08:34.559
different framework from angular 2.
00:08:36.419
these are not the same so keep that in
00:08:37.979
mind and you know that's classic Google
00:08:40.080
for you but so effectively it said you
00:08:42.240
know okay so if you change something in
00:08:43.440
your model it automatically updates here
00:08:45.360
if you change something in your view
00:08:46.980
then it doesn't the updates in your
00:08:48.720
model so try to keep both of these in
00:08:50.640
sync So in theory this was nice because
00:08:53.160
you didn't have to worry about doing
00:08:54.600
manual Dom manipulation in practice this
00:08:58.260
led to code that was very hard to follow
00:09:00.600
very hard to debug so effectively this
00:09:04.560
resulted in a worse abstraction in the
00:09:06.779
long run which is also why Google
00:09:08.820
actually abandoned it I think they're
00:09:10.500
officially no longer supporting
00:09:11.760
angularjs and it led to a ton of
00:09:15.120
performance issues because you needed to
00:09:17.220
keep both States updated at the same
00:09:19.320
time and so this is where react comes
00:09:21.360
into the picture and it would be
00:09:22.980
impossible to overstate the effect that
00:09:25.740
this react approach had on the way we
00:09:28.920
think about JavaScript Frameworks and
00:09:30.420
this isn't necessarily
00:09:31.800
saying react is amazing react is the
00:09:34.200
best I react is the most popular at this
00:09:36.600
point like let's be clear about that
00:09:38.399
react has the biggest amount of market
00:09:41.040
share but react has a lot of flaws and I
00:09:43.860
think we also need to be cognizant of
00:09:45.540
those flaws one of it being that react
00:09:47.459
is actually really old by this point the
00:09:49.740
react team is kind of struggling to keep
00:09:51.720
kind of up with new developments while
00:09:54.300
still sticking to the core architecture
00:09:57.660
of react itself so react is in an
00:09:59.339
interesting position I'm unsure about
00:10:01.320
the future of react but for now it is
00:10:03.240
the by far the most popular framework
00:10:06.600
um and this is also one of the reasons
00:10:07.860
why it's important to understand the
00:10:09.300
underlying Frameworks because if you
00:10:11.040
just learn the react abstraction and
00:10:13.320
something else replaces react or
00:10:14.820
something else becomes widely more
00:10:16.320
popular you've learned react and you and
00:10:18.660
that's the end of your career you don't
00:10:20.100
know how to switch to a new framework
00:10:21.720
here's the magic of react we can say all
00:10:23.940
of this and we can still appreciate just
00:10:26.100
how phenomenal Rex take on this is so
00:10:29.160
what react does it actually said the
00:10:31.740
think about your UI as the result of a
00:10:35.940
function so it said your view and here
00:10:38.580
you can see now we're getting into
00:10:39.899
functional programming this starts
00:10:41.459
looking a lot like mathematics so your
00:10:44.399
view is the result of writing a function
00:10:47.100
on your state let me show you that okay
00:10:49.079
so your view is a result of running a
00:10:51.839
function on your state what you do is
00:10:55.019
you write this function this is the
00:10:57.480
react code that you write you write the
00:10:59.760
function that gets run on your state to
00:11:02.640
create your actual view so what this
00:11:05.100
means is that once again your view is
00:11:07.980
just a result of the actual file so this
00:11:10.380
is a purely functional approach we have
00:11:12.899
a function that we run give them the
00:11:14.820
same inputs it's always going to give
00:11:16.740
the same outputs and this is also where
00:11:19.079
it talks about kind of a component
00:11:20.700
approach but we've spoken about this now
00:11:22.380
a bit already like we are Beyond this
00:11:25.140
point already so we spoke about you know
00:11:27.980
traditionally you would separate your
00:11:29.880
HTML your CSS in your JavaScript when
00:11:32.279
you think about components instead of
00:11:34.320
separating it between these different
00:11:35.760
Technologies you separate it based on
00:11:38.519
responsibility and you kind of bundle
00:11:40.320
them all together in a single thing I
00:11:42.300
like this weird here makes a pizza and a
00:11:44.700
taco okay and so here it actually starts
00:11:46.680
talking about about react I'm not going
00:11:48.120
to go into that just right now here's
00:11:50.700
also a really good example of how react
00:11:53.160
does polymorphism so it just shows that
00:11:55.740
you know so your component can take
00:11:57.660
another component as a value and we're
00:12:00.120
gonna We be talking about a lot of these
00:12:02.100
things as we get to react a lot of this
00:12:04.079
is maybe a bit too advanced for now but
00:12:06.300
I think this article by illustrating how
00:12:09.000
react Works actually explains a lot of
00:12:11.220
the underlying principles that most
00:12:12.720
Frameworks use once again reactors being
00:12:15.060
the most popular at the moment so
00:12:16.800
obviously a lot of the materials kind of
00:12:18.839
talk about react specifically I don't
00:12:21.000
know what's going on here like the spike
00:12:23.339
here I don't know I think something went
00:12:25.320
wrong with npm Trends I don't know why
00:12:27.920
Vue jumped to 500
00:12:31.380
000 yeah like there's something going on
00:12:32.880
here but if we look at the rest of it
00:12:35.279
you can see react is steadily steadily
00:12:37.500
arising and so we're kind of at this
00:12:39.360
point now where react is hands down way
00:12:42.959
in the lead over all the other
00:12:44.399
Frameworks 2018 it maybe wasn't such a
00:12:47.940
clear case but yeah there's a massive so
00:12:50.040
for now react is you know if we even
00:12:52.079
look at the stars you know here
00:12:54.300
um react is immensely popular if we want
00:12:57.720
to treat of view as the result result of
00:13:01.260
a function so let's just call that
00:13:02.760
function that function is usually called
00:13:04.980
render okay so render text props and it
00:13:08.339
returns a view
00:13:10.740
so then if we call render multiple times
00:13:13.860
how do we then make the changes without
00:13:16.860
replacing the entire Dom because we're
00:13:19.260
effectively creating a new Dom every
00:13:21.300
time so the easiest way is obviously to
00:13:24.420
just wipe the Dom completely and replace
00:13:26.880
it with a new Dom so every time we run
00:13:29.459
the render we get new HTML we get rid of
00:13:32.459
all the HTML and we put in the new HTML
00:13:34.680
that would be a very nice way to solve
00:13:36.959
this in a functional manner we get a new
00:13:39.120
result we throw away the old result put
00:13:41.040
the new result in so you never mutate
00:13:43.019
anything you're just like full on get
00:13:45.000
rid of the current HTML and put in the
00:13:47.519
new HTML in the same way that the only
00:13:50.339
thing we had in our state that was
00:13:51.959
mutable was maybe the state so we ended
00:13:53.940
up actually doing it in an array manner
00:13:56.459
where we just push to the state but
00:13:58.440
another approach would have been just
00:13:59.700
the new state just replace the do the
00:14:01.980
changes get a completely new state and
00:14:03.839
replace the state do the changes get a
00:14:05.880
completely new state replace the alt
00:14:08.160
state so this would be a much more
00:14:10.139
functional way way than going for
00:14:12.180
example State
00:14:13.800
um number like tasks number two the
00:14:17.579
value is now four and state task number
00:14:22.339
five uh the completed is now the
00:14:26.279
opposite of what it currently is so in
00:14:29.700
this case we have data flowing in both
00:14:31.680
directions whereas in this one we have
00:14:34.500
data just flowing in One Direction and
00:14:36.660
then when it's done we just check what
00:14:39.240
the new thing that's created and we just
00:14:41.040
replace entirely the existing one with
00:14:43.260
the new one instead of going back and
00:14:46.019
you know changing the existing one yeah
00:14:48.720
we just have the existing and it just
00:14:50.760
flat out changes to the to the new one
00:14:52.920
so this is a a lot easier to maintain
00:14:56.220
because you just check in the same way
00:14:57.899
that in our Redux store you can see all
00:14:59.820
right you can see how the store changed
00:15:01.500
from one to the other one to the other
00:15:03.060
every time you can just it's a full on
00:15:05.339
transition and it's much easier to debug
00:15:07.620
now you might have been like okay skull
00:15:09.360
like I actually knew this you could have
00:15:10.680
done it this way I don't know why you
00:15:12.120
did it in the super tricky weird way
00:15:14.579
um you could have actually just gone
00:15:16.440
ul and then every time you just replace
00:15:18.660
the inner HTML of UL how we would
00:15:21.060
actually do it in a completely
00:15:22.260
functional Manner and you'll see this is
00:15:24.120
actually a lot easier to read and reason
00:15:25.980
about than what we did down here but I'm
00:15:28.199
going to do this now and I'm going to
00:15:29.220
explain to you why we actually did it in
00:15:31.740
this weird gross way because there is a
00:15:34.260
problem with just doing this so if you
00:15:36.120
take a purely functional programming
00:15:38.399
approach you would say that there's a
00:15:40.380
render function and that render function
00:15:42.000
just takes some props and that creates
00:15:44.040
an HTML for us okay and that also means
00:15:46.920
we don't need
00:15:48.180
either because like we're just we're
00:15:49.680
just creating the HTML every time render
00:15:52.320
happens okay so let's just say this
00:15:54.600
returns this for us okay so what our
00:15:58.560
render function does it just returns a
00:16:00.899
string for us so let's I don't know what
00:16:03.240
the props is right now so let's just put
00:16:04.800
that in there but it just returns a
00:16:06.720
string for us which will be our HTML who
00:16:09.240
he hates new HTML based on state there
00:16:13.800
we go label input so forth so forth UL
00:16:17.399
all right we don't actually even now
00:16:19.920
need to listen to this because this is
00:16:21.839
just a result let's make our entire
00:16:23.940
State uh prop so then we can just pass
00:16:26.459
the state exactly as is so we get the
00:16:29.760
state and then based off the state we
00:16:31.680
just so all that we need for now is
00:16:33.720
tasks tasks HTML as an array so let's
00:16:37.380
say this is an array of strings and so
00:16:40.320
what we're doing is we're getting tasks
00:16:42.000
this is an object so let's do object
00:16:44.100
value to create to turn it into array
00:16:47.519
and so we just pass tasks in there okay
00:16:50.639
and then we map over it so what map does
00:16:52.860
map is very similar to like four each
00:16:55.019
but the only difference is you have to
00:16:56.940
return something and what you return is
00:16:58.680
going to be that new item so for example
00:17:01.019
I'm going to talk about this in the next
00:17:02.699
video when you talk about higher order
00:17:03.959
function so I'm going to go you know
00:17:05.939
let's say you have an array that is that
00:17:07.740
and you have a you pass a Handler to map
00:17:11.819
and the Handler is just going to take
00:17:13.679
the current item and multiply it by
00:17:16.319
three okay so then what's going to
00:17:17.880
happen is when you run map with Handler
00:17:19.859
over that so in other words if you go
00:17:21.480
that map dot you know Handler then what
00:17:24.119
you're going to get obviously it's
00:17:25.679
giving a lot of Errors because I'm
00:17:26.880
writing it in the middle of nowhere but
00:17:28.679
what you're going to get is then you're
00:17:29.880
going to get three a new array that's
00:17:32.220
three six nine okay so effectively we
00:17:36.000
pass in a function that transforms each
00:17:38.340
of these tasks and it's going to
00:17:39.660
transform it to us into HTML so we can
00:17:42.120
just destructure right in here let's
00:17:43.740
write a function right in here and
00:17:45.660
return and we obviously need to return a
00:17:47.520
string and what can we destructure we
00:17:49.500
can destructure created ID and title all
00:17:52.620
right and then let's just return the
00:17:54.000
HTML right here let's also just get some
00:17:57.299
syntax highlighting over here so Li in
00:18:00.660
that Li we're going to have a button
00:18:02.280
that is just going to have the title for
00:18:04.140
now okay and let's just put the ID let's
00:18:06.780
say data ID equals the actual ID and we
00:18:10.320
don't need to put the data created in
00:18:11.940
there so here's that and then let's just
00:18:14.100
so what we want to do is take that array
00:18:16.080
put it in here and just join it the join
00:18:18.780
is just going to convert it into a
00:18:20.340
string using whatever so if you and
00:18:22.559
separates the items whatever you pass in
00:18:24.539
there we don't want to separate so this
00:18:26.820
should render that for us and so we
00:18:29.460
don't need this template so let's get
00:18:31.500
rid of this Pawn connection grab the
00:18:34.679
current state of the store so let's just
00:18:36.960
say HTML it's a render just past the
00:18:40.020
store and then all we do is we just grab
00:18:42.780
this we just get HTML and let's just in
00:18:45.600
our template maybe just create a wrapper
00:18:47.460
for it so let's say a Dev let's just say
00:18:49.740
data wrapper because this is just where
00:18:52.020
we're going to put everything inside get
00:18:53.880
HTML so let's just say constant wrapper
00:18:56.100
hit HTML and we just look for wrapper
00:18:59.100
and then all we do is wrap a inner HTML
00:19:02.160
is the HTML that we just created this is
00:19:04.679
a lot more straightforward than manually
00:19:06.840
moving things around manually deleting
00:19:09.000
things manually creating nodes and so
00:19:10.679
forth we just create HTML and then every
00:19:14.100
time our store changes we recreate the
00:19:16.500
HTML so I'm not going to show this right
00:19:19.320
now because I otherwise this video is
00:19:21.299
going to get very long so I just want to
00:19:23.580
show you this principle and but now I
00:19:25.500
want to explain the problem to you so
00:19:27.660
this seems very elegant so we so we have
00:19:30.120
a render function and so we have our
00:19:32.760
state and then we actually have body in
00:19:35.400
our HTML and so ideally what would be
00:19:37.740
really cool is every time you listen to
00:19:40.080
this and every time the state changes
00:19:42.539
you run render past the new state into
00:19:45.179
render it spits out HTML and you just
00:19:47.760
put that new HTML in between here and in
00:19:51.299
short this is what a lot of Frameworks
00:19:52.799
actually do but so what I'm going to
00:19:54.480
show now is why you need a framework why
00:19:56.400
you can't just do this wholesale and
00:19:58.320
let's just say you know the state
00:20:00.120
changes all of this runs again and it
00:20:03.059
replaces you know what's inside there so
00:20:05.280
now we have created like a very
00:20:07.440
functional approach to building apps
00:20:09.840
because effectively now the HTML just
00:20:12.419
gets recreated every time the state
00:20:14.880
changes as opposed to what we've done up
00:20:17.340
until now we have a logic here which
00:20:20.580
isn't as simple as what we have here
00:20:22.620
which is effectively just you know HTML
00:20:25.100
equals render this is a pure function it
00:20:29.820
returns new HTML for us this is not what
00:20:32.160
we had previously is not a pure function
00:20:33.840
because we just had you know logic and
00:20:36.539
you pass the state in but you know it
00:20:39.059
does stuff it doesn't it does loads of
00:20:41.100
side effects and whatever it doesn't
00:20:42.419
actually return anything so we don't
00:20:45.059
actually just pass the response in here
00:20:46.919
you know it does lots of side effects
00:20:49.140
you know checking all their new ones
00:20:51.059
checking if there are old ones that are
00:20:52.799
no longer present so you have you know
00:20:54.600
all these side effects happening there's
00:20:56.700
not a single all this logic that happens
00:20:58.980
outside of this it reaches directly into
00:21:01.620
the HTML and makes these changes whereas
00:21:04.320
here it just spits out HTML and that
00:21:06.059
HTML just gets thrown in here so this is
00:21:08.280
feasible if you're building something
00:21:09.840
basic so let me show you an example so
00:21:12.120
let's say we have a very basic version
00:21:14.940
of our to-do app which is we have our
00:21:18.120
input up here and this is where you
00:21:20.400
enter new so here's you know new task
00:21:22.740
and then here's a save button make it
00:21:25.320
like that says button and then you know
00:21:27.600
the tasks are shown down here and you
00:21:30.000
enter in here
00:21:31.880
and you save it adds it to the state all
00:21:36.600
right so
00:21:38.120
and it goes to the new state this
00:21:40.140
triggers a render knows that okay what
00:21:42.480
should happen the new HTML this is the
00:21:45.120
new HTML that should be created so okay
00:21:47.520
so this should be clean in the new HML
00:21:50.340
and whatever is there should now be down
00:21:53.580
here as actual task oh that was pretty
00:21:56.159
cool okay let's do it again so you do it
00:21:59.039
again and it recreates and it just
00:22:01.140
replaces the current HTML and so forth
00:22:03.419
and so forth here's the problem the
00:22:05.940
problem is because the HTML first and
00:22:09.840
foremost gets recreated from scratch all
00:22:12.840
the time this is going to be a massive
00:22:15.059
problem in terms of performance let's
00:22:17.280
say you are doing something as simple as
00:22:19.559
clicking a check box okay so something
00:22:22.140
gets toggled from completed to or not
00:22:26.100
completed to completed you have to now
00:22:28.679
rebuild all of this throw away all of
00:22:32.039
this rebuild all of this with just that
00:22:34.440
little change so this is completely it
00:22:37.020
doesn't just go and change that so with
00:22:39.179
our current approach of the side effects
00:22:40.919
while it's not great and it requires a
00:22:43.380
lot of work for us at the very least
00:22:45.299
what these side effects do is they okay
00:22:48.179
they're able to just actually Target the
00:22:50.220
thing that needs to change at the very
00:22:51.900
least our logic is able to see and just
00:22:54.539
actually Target that specific thing and
00:22:57.059
change this it it never throws away this
00:23:00.480
is the same HTML that just gets mutated
00:23:03.000
you know so it changes that it changes
00:23:05.039
that so it just mutates it from a
00:23:06.840
functional world this is a bad thing you
00:23:10.200
know so mutations bad because it makes
00:23:12.780
it very hard to reason about why the
00:23:16.020
HTML is now in the state that it is
00:23:17.940
because you can't see a clear
00:23:19.820
unidirectional flow from your state to
00:23:22.440
the new UI from the state to the new UI
00:23:25.080
from the new state to the UI so you
00:23:27.480
can't ever be really sure why something
00:23:29.520
changed unless you actually detangle all
00:23:32.580
these side effects and with enough time
00:23:33.900
you know this is going to turn into the
00:23:35.280
spaghetti mess of side effects and
00:23:37.320
you're going to forget to check this
00:23:38.820
thing you're going to forget to check
00:23:39.900
that thing this is going to become
00:23:40.919
unmanageable and this is the problem
00:23:43.200
space where Frameworks enter so we spoke
00:23:45.659
about like why this is maybe more
00:23:47.460
perform but you might be like okay like
00:23:50.220
I'm willing to suck that up you know my
00:23:52.080
apps are going to suck they're going to
00:23:53.400
be really slow but that's just that I
00:23:55.679
want to do it in this way like even if
00:23:57.780
my apps are slow even if someone needs
00:23:59.940
to wait 10 minutes after they toggle
00:24:02.580
completed to be able to continue this is
00:24:05.220
going to be like a massive loading
00:24:06.659
spinner every time anything changes but
00:24:08.880
the other problem is every time this
00:24:11.940
gets created this is no longer the same
00:24:14.280
HTML so every time the save button gets
00:24:17.760
created it's a completely new HTML
00:24:21.179
element so what that means is a couple
00:24:24.600
of things if you have attached event
00:24:26.940
listeners to this thing you need to
00:24:29.039
remove them and re-add them every single
00:24:31.679
time because according to the Dom this
00:24:33.960
is a completely new HTML thing it has
00:24:36.000
the same text inside it but it's not the
00:24:37.860
same button because you're recreating
00:24:39.240
all the HTML if a user is focused on
00:24:42.960
this and a re-render happens they're
00:24:45.360
going to lose focus because this is a
00:24:47.820
completely new thing the thing that they
00:24:49.620
were focused on previously is deleted
00:24:51.780
it's typing something in here and the
00:24:54.240
re-render happens even if you put this
00:24:56.340
back in in the re-render a user is going
00:24:59.280
to lose focus where the the first thing
00:25:01.860
that people start running into with this
00:25:03.720
approach and let me show you this in
00:25:06.000
practice let me just do this in codepen
00:25:08.039
so let's say const render and all that
00:25:10.679
that does it returns uh let's just say
00:25:13.500
what we have is we have a form that has
00:25:16.320
an input and outside of that is an H2
00:25:19.799
and it just shows whatever you put in
00:25:22.860
the input over there we start off by
00:25:25.260
going document body in a HTML and we
00:25:28.679
just render and it should this accepts a
00:25:31.620
value say value and value is what's
00:25:34.020
going to be passed in here and value is
00:25:36.840
what's going to show yeah and we just
00:25:39.179
started off by saying like placeholder
00:25:42.240
or whatever and it is unhappy because
00:25:44.279
this needs to be a string all right so
00:25:47.039
this is cool so our HTML is the result
00:25:49.140
of a function that we run and so
00:25:51.299
obviously now if you want to change this
00:25:52.799
we want to listen and re-render every
00:25:55.260
time this gets changed so all that we
00:25:57.900
can do is let's just honestly on our
00:26:00.179
document body add event listener and we
00:26:02.700
just want to listen for input so input
00:26:04.140
is whenever uh the like anything changes
00:26:07.380
in an input and then we want to grab the
00:26:09.539
event and from the event we want to just
00:26:12.659
get the value so we can destructure that
00:26:15.000
of value from the event Target and let's
00:26:17.700
just console log that for now so we're
00:26:19.980
just going to cancel log any time we
00:26:22.140
actually change what's in there we're
00:26:23.700
just going to counter log it quickly and
00:26:25.200
let me just add cool you'll see hello
00:26:28.500
and every time we change it fires all
00:26:31.200
right so let's say we want to do one of
00:26:33.360
the most basic things that you do in a
00:26:35.039
framework so we want to update our store
00:26:37.620
and that should actually replace this so
00:26:41.340
this is pretty simple all we do we just
00:26:43.679
re-render with the value okay let's try
00:26:46.919
that out okay place all that's fine a
00:26:49.500
okay so check that out this is cool but
00:26:52.260
here's the thing you'll see what happens
00:26:53.700
every time you enter something it loses
00:26:55.559
Focus so let's say I want to enter my
00:26:58.320
name so s it uses Focus I need to
00:27:00.900
refocus again okay click on again C
00:27:02.820
loses Focus hey it loses Focus so I
00:27:06.240
can't every time I update the Dom or
00:27:09.840
enter a character it creates a
00:27:11.520
completely new input it takes the value
00:27:13.860
it still puts it in the input but
00:27:15.360
according to the Dom this is a
00:27:16.980
completely new thing so obviously it
00:27:19.620
can't it loses Focus because it's not
00:27:21.840
the same thing it's as if I put another
00:27:23.700
input below it with just the same value
00:27:26.340
and this is the first place where people
00:27:28.080
start running into issues when they do
00:27:30.419
this and the way we solve this and this
00:27:33.360
is what Frameworks do for us and
00:27:35.100
specifically something with the virtual
00:27:36.179
Dom is you do it in this way but then
00:27:40.440
you give the framework the current HTML
00:27:43.320
and the next HTML and you let the
00:27:46.679
framework figure out what has changed
00:27:49.679
and it'll see okay this is what you're
00:27:51.900
an it will handle that for you so you
00:27:54.840
can write your HTML changes as a result
00:27:58.500
of a render function but then the
00:28:01.559
framework checks what are the
00:28:03.299
differences and it manually does the
00:28:05.100
changes for you and it abstracts that
00:28:07.380
away from you so you can just think
00:28:09.659
about your changes as the result of a
00:28:12.299
function so this allows us to actually
00:28:14.820
write our HTML in a functional
00:28:17.400
programming manner with no side effects
00:28:20.100
immutable data in other words the date
00:28:22.440
we create new data each time this is
00:28:24.900
going to keep it really easy to debug
00:28:27.179
it's going to actually make it very easy
00:28:29.100
to reason about like why is that why is
00:28:32.039
HTML now in the state that it is now as
00:28:34.500
opposed to like this kind of mess and
00:28:37.080
this is where Frameworks come in and so
00:28:39.000
you get Frameworks like react that is
00:28:40.679
like full on functional programming
00:28:42.480
there are some that are even a more
00:28:44.640
functional programming than react so a
00:28:47.340
good example is Elm so Elm is one that's
00:28:50.820
like just full-on functional programming
00:28:52.799
there are no side effects no impure
00:28:55.260
functions and so forth
00:28:56.840
react is one of the ones that tend to be
00:28:59.940
a bit more functional programming
00:29:01.740
specific but it's not as hardcore as
00:29:04.919
something like Elm but but most of them
00:29:07.380
work on this principle that your what
00:29:11.820
you see you express your HTML as a
00:29:15.960
result of a render function and then
00:29:18.059
it's a Frameworks job to figure out how
00:29:20.820
to ensure that what has changed between
00:29:23.820
these two renders actually gets applied
00:29:25.860
to the Dom so it completely abstracts
00:29:28.080
the Dom away for us we don't even think
00:29:30.480
about the Dom so when you're using a
00:29:32.820
framework this is all you care about you
00:29:35.760
only care about this what do you pass to
00:29:39.240
your render function what happens here
00:29:41.460
is completely abstracted away from you
00:29:43.620
but as mentioned you still need to
00:29:46.080
understand what happens here because
00:29:48.000
sometimes weird things will happen here
00:29:50.039
and if you don't understand what goes on
00:29:53.159
over here you're going to get stuck and
00:29:55.140
you're not going to be able to actually
00:29:56.940
fix the problem or likewise certain
00:29:59.220
Frameworks might do different things
00:30:01.380
here behind the abstraction and if you
00:30:03.419
don't understand what they actually
00:30:04.679
abstract away it's going be a very hard
00:30:06.779
choice for you to decide between what is
00:30:09.240
a good framework for your solution or
00:30:11.520
what is the best thing to pass to render
00:30:14.159
to make this as fast as it as it can
00:30:17.220
possibly be and so forth in the next
00:30:19.740
lesson we're going to start talking
00:30:21.240
about higher order functions and as you
00:30:23.220
can imagine if we take this approach
00:30:25.440
higher order functions are a really good
00:30:28.559
fit for data transformation so you use
00:30:31.559
them a lot actually in react when you
00:30:34.679
actually want to create a list of
00:30:35.760
something let me show you quickly you
00:30:37.620
actually use a higher order function so
00:30:39.600
in react or kind of the way it does kind
00:30:41.940
of Dom diffing through something called
00:30:43.980
the virtual Dom you actually Express
00:30:46.020
through something called jsx so you
00:30:48.899
would effectively have a function that
00:30:50.580
is you know let's say you know View and
00:30:53.520
in our view currently is just we just
00:30:56.580
take tasks and then we return some jsx
00:31:00.000
so we just return an unordered list and
00:31:02.580
inside that we want to return let's say
00:31:04.980
task is just just a string is a array of
00:31:08.520
strings so tasks and so if we were to
00:31:10.679
mark that up in JS Dock you would just
00:31:12.840
do param array of strings tasks so
00:31:16.500
effectively what you can just do is you
00:31:18.960
would just Express a piece of JavaScript
00:31:20.880
logic in this way in jsx so you say
00:31:22.860
there's going to be some JavaScript here
00:31:24.360
you can think about this in the same way
00:31:26.340
as interpolation so resolve this
00:31:28.919
evaluate this first before you continue
00:31:31.020
and some some Frameworks actually use
00:31:33.440
interpolation and template literals let
00:31:36.299
for example does it we're gonna we're
00:31:37.860
gonna talk a bit about let HTML in the
00:31:39.659
next section but effectively if you
00:31:41.640
react you can go tasks map and let's
00:31:44.340
grab the name and you return new jsx so
00:31:48.659
Li and name and there we go this is your
00:31:51.899
render passing tasks you return jsx
00:31:54.720
inside that you map over all the tasks
00:31:57.659
and you create a new array that is just
00:32:00.840
an Li with the names in it and this is
00:32:03.659
and so whatever you pass to tasks is
00:32:05.820
just going to render something different
00:32:07.380
so I can go you know A and B and let's
00:32:10.740
say something happens you know there's
00:32:12.120
an update and it changes from view a or
00:32:15.419
whatever or view a b we don't have to
00:32:19.799
worry about the Dom we don't have to
00:32:21.120
worry about updating the Dom query
00:32:23.279
selectors none of that you never write
00:32:25.320
any query select unless it's something
00:32:26.940
very specific that you need to do you
00:32:28.740
never actually touch the Dom you just
00:32:31.320
work with a function that renders the
00:32:34.140
new HTML for you and that's the
00:32:35.640
framework's job to figure out how to
00:32:38.520
take this piece of new HTML and update
00:32:41.460
your current HTML in the performant
00:32:43.380
manner that actually just changes what
00:32:46.260
has changed and doesn't completely throw
00:32:48.659
everything away and add something new in
00:32:50.940
so in the next module we're going to
00:32:52.620
talk about this we're going to talk
00:32:53.460
about virtual Doms we're going to talk
00:32:54.960
about the ways that some of these
00:32:56.880
Frameworks do it and kind of this
00:32:58.860
process and specifically we're going to
00:33:01.679
talk about how we can actually use
00:33:03.360
higher order functions as a very one way
00:33:06.840
to actually express our logic because
00:33:09.720
you can theoretically do this you know
00:33:12.000
you can theoretically go can't result
00:33:14.519
and then you know that's an array and
00:33:17.279
for single task of tasks and and then we
00:33:23.100
go result and you push you know this to
00:33:26.340
result and then you put result in there
00:33:28.980
so you can do this
00:33:30.960
um and because you're more familiar with
00:33:33.120
for Loops this might actually seem more
00:33:35.640
straightforward to you obviously this is
00:33:37.679
a very simple app like your app's going
00:33:39.299
to get much more complicated so you can
00:33:41.760
imagine having something as expressive
00:33:44.399
and declarative as this where once again
00:33:46.980
data just Flows In One Direction there
00:33:49.860
is no like creating something up here
00:33:52.080
then a for Loop then setting it back
00:33:54.360
changing it after it's been created
00:33:56.279
following going up and down in the
00:33:58.320
component trying to figure out where
00:33:59.940
things come from data just follows in
00:34:01.919
One Direction you always just keep
00:34:03.419
reading down so here you go here you go
00:34:05.760
this happens this happens and that gives
00:34:08.280
you an indication of what does this
00:34:10.440
render actually do how does it take the
00:34:12.359
state and turn it into HTML that was a
00:34:14.639
lot my things are getting intense now
00:34:17.639
um it might seem overwhelming just be
00:34:20.099
patient just maybe watch it again try
00:34:23.219
and get a sense of the key takeaways
00:34:25.500
here and when we touch on Frameworks
00:34:28.199
maybe come back to this again to
00:34:30.540
understand okay what is the point that
00:34:34.020
I'm trying to make here now that you
00:34:36.119
have a bit of an understanding in terms
00:34:37.560
of how you actually use Frameworks
00:34:39.060
because I think if anything the point
00:34:41.879
that I'm trying to make in this lesson
00:34:44.159
is one of the most critical points when
00:34:47.580
working with JavaScript and if you
00:34:49.800
understand this it's going to be such a
00:34:53.219
superpower in your career because a lot
00:34:55.859
of people come into JavaScript and they
00:34:58.380
just learn this part they just learn how
00:35:01.440
to use react to give you something they
00:35:04.500
don't understand why that happens or why
00:35:07.560
do you even do that and then when this
00:35:09.660
breaks or when this doesn't give them
00:35:11.700
what they want or when this becomes
00:35:13.619
really slow they don't understand the
00:35:15.960
underlying logic and they're unable to
00:35:18.060
even search for answers online or chat
00:35:20.820
with their colleagues about what they
00:35:23.040
think is actually happening I will see
00:35:25.200
you in the next video