00:00:00.000
so there are a couple of Animation
00:00:02.159
libraries for react react spring is the
00:00:04.860
one that I kind of like the most and
00:00:06.899
I'll get into it in a second why but so
00:00:09.599
some other Frameworks for example you
00:00:12.240
have libraries like Alpine you have
00:00:14.160
libraries like svelp and so forth that
00:00:16.260
have their built-in animation apis so
00:00:19.680
for example if you if you look at Alpine
00:00:21.660
I think there are apis that you can use
00:00:24.900
for animation spelled for example has
00:00:27.900
built in ways to do animation yeah
00:00:31.080
transition transition animations yeah so
00:00:33.480
you can do Fade you can do blur and so
00:00:35.460
forth if I'm not mistaken I think Vue
00:00:38.399
has animation built in as well yes
00:00:42.480
angular also has animations because
00:00:45.000
angular has everything built in so if
00:00:47.100
your question is ever does angular have
00:00:48.840
X thing built in the answer is always
00:00:50.460
yes okay angular is like comes with
00:00:52.920
everything included which is why some
00:00:54.840
people like it which is why I don't like
00:00:56.579
that but some people like that some
00:00:58.860
people like getting a all-in-one tool
00:01:01.559
chain everything set up they have
00:01:03.600
everything they need but the drawback of
00:01:05.580
that is you then need to use that thing
00:01:07.920
you can't use something else react as
00:01:10.920
you would expect does not have a way
00:01:14.100
natively to do animation so either you
00:01:17.100
need to use CSS animation or you need to
00:01:20.100
actually use a third-party Library so
00:01:22.979
CSS animation works really well when you
00:01:25.020
have things that transition between
00:01:26.460
different states okay so when you have a
00:01:28.680
button and on Hover the series is
00:01:30.479
changes it becomes a bit more
00:01:33.119
problematic when you want things to be
00:01:35.640
animated when they leave the Dom or when
00:01:38.520
they enter the Dom you can't use CSS to
00:01:41.700
tell something when you remove the thing
00:01:44.040
animated out because you can't
00:01:45.900
theoretically animate something that
00:01:47.640
gets removed because it's no longer
00:01:49.259
there so because we act as a rendering
00:01:52.259
for you you can hook into that rendering
00:01:54.420
pipeline you can use third-party
00:01:56.640
libraries to tell it like hey before if
00:01:59.280
there's a difference in the virtual Dom
00:02:00.960
between two things hold on for a second
00:02:03.240
before the thing gets removed just so we
00:02:05.520
have a second that we can do an
00:02:07.079
animation or just hold on a second
00:02:09.060
before the thing gets added so these
00:02:11.340
libraries allow you to hook into the
00:02:13.500
render Pipeline and do that I've been
00:02:15.840
using react spring for so long I don't
00:02:17.879
even remember what the others were or
00:02:19.500
even are nowadays there were a couple
00:02:21.780
that I've used in the past so it's also
00:02:24.000
really nice about spring is first and
00:02:25.980
foremost it's modeled on physics so it's
00:02:28.560
not linear so in other words it has a
00:02:30.660
bit of a like con tangible feel to it so
00:02:33.060
the animations you know they
00:02:34.680
a bit as if the actual objects that get
00:02:37.379
like moved around in physical space of
00:02:39.660
gravity and so forth and the other thing
00:02:41.760
is as well the animations happen without
00:02:44.840
triggering a rearender it takes the
00:02:47.580
animated elements completely out of the
00:02:49.560
react Dom and it animates it irrelevant
00:02:52.080
so it doesn't Trigger or re-render every
00:02:54.360
time something updates which is really
00:02:56.040
cool it treats the animation as a
00:02:58.319
completely different concern than
00:03:00.239
actually figuring out what to show
00:03:02.040
because those are two different concerns
00:03:03.720
figuring out what to show on the screen
00:03:05.819
and animating moving something around on
00:03:07.980
the screen are two different concerns
00:03:09.780
quickly look at the documentation and
00:03:11.879
the point here and the reason why I
00:03:13.800
cover lots of other Frameworks is not so
00:03:16.379
that you learn like all these different
00:03:18.300
Frameworks and you know all these
00:03:19.620
Frameworks I think we don't have even
00:03:21.360
enough time to do that even if we wanted
00:03:23.280
to what I want to do is I want to teach
00:03:26.159
you guys how to approach documentation
00:03:28.080
if you want to learn this framework how
00:03:30.000
do I approach the documentation if I
00:03:31.560
want to learn react spring how do I
00:03:33.300
approach the documentation because I I
00:03:35.040
mentioned last time you know it's a
00:03:36.239
thing about like give a man a fish or
00:03:37.739
teach a man to fish you know if I show
00:03:39.840
you guys how to approach documentation
00:03:41.340
you can effectively learn any tool if I
00:03:44.459
just learn you the tools you're just
00:03:46.440
going to struggle learning anything new
00:03:47.940
that's not helpful to anyone most
00:03:49.920
documentation has a great started page
00:03:51.720
and then it just here tells us how to
00:03:53.459
install it so react spring is a library
00:03:55.920
for building interactive data driven and
00:03:58.140
animated UI components it can animate
00:04:00.299
HTML so for so forth so what's actually
00:04:02.879
cool about react spring it can animate
00:04:05.760
you know HTML SVG but it can also
00:04:09.360
because here's another thing you can't
00:04:10.860
animate svgu with CSS or you can but
00:04:13.379
very limited so it's actually very
00:04:15.239
tricky but you can also animate native
00:04:17.760
if you have a native app you can use
00:04:19.620
react spring with react native to
00:04:22.620
animate things in your native app you
00:04:24.780
can also animate 3js things you might be
00:04:27.419
asking what is 3js let me show you
00:04:30.020
prepare to have your mind blown the DJs
00:04:33.419
is a way to two 3D rendering and 3D
00:04:36.540
modeling in the browser it uses webgl so
00:04:40.080
this is Canon so you'll see it's
00:04:41.280
actually used by a lot of companies yeah
00:04:43.380
so this is 3D rendered in the actual
00:04:46.020
browser itself so if I scroll it moves
00:04:48.240
two this is really impressive now so
00:04:50.280
3djs allows you to do 3D rendering in
00:04:53.100
the browser itself through memes of like
00:04:55.500
webgl so webgl is so those of you that
00:04:58.620
know kind of opengl and those things you
00:05:01.320
can actually there is an API natively in
00:05:03.660
the browsers called webgl that allows
00:05:05.759
you to actually use the opengl standard
00:05:08.759
in the browser and do like 3D rendering
00:05:11.160
of things and so forth it's it's really
00:05:13.080
cool I can actually move it around by
00:05:15.660
dragging so
00:05:17.360
and this is the value of something like
00:05:19.800
react so react sometimes has a bit of a
00:05:23.160
higher learning curve and it's sometimes
00:05:24.479
a bit harder to get your head around
00:05:25.860
because it doesn't assume a Dom it
00:05:29.580
doesn't assume a specific use case but
00:05:32.100
the cool thing about that is you can and
00:05:34.919
use it on mobile apps you can use it to
00:05:37.680
do like VR things and so forth because
00:05:40.080
it's just a way to express what gets
00:05:42.840
shown on the screen in a declarative
00:05:44.820
manner that is all that react is then
00:05:47.639
you use react Dom or whatever to
00:05:49.320
actually bind it to something else so
00:05:51.419
the core of reacting why the react
00:05:53.280
abstraction is so small is all it gives
00:05:55.680
you in terms of single responsibility is
00:05:57.900
it gives you a way to express something
00:06:00.060
that gets shown in a declarative Manner
00:06:01.979
and because of this something like react
00:06:04.320
spring you can actually use it on
00:06:06.240
anything but obviously we're going to
00:06:07.440
use it on the web so we're going to
00:06:08.820
install react spring forward slash web
00:06:11.520
and if you remember correctly the last
00:06:13.560
time I said you know when you see this
00:06:15.120
at something forward slash it means that
00:06:17.880
it's a it's a package it's an npm
00:06:19.680
package but it's made up of several
00:06:22.080
different packages and so this means
00:06:24.479
that this is one of the packages related
00:06:27.660
to react spring and you can install it
00:06:29.759
separately okay so it's almost like
00:06:31.319
packages of packages and this is just a
00:06:33.900
convention it's not enforced or whatever
00:06:37.039
there's no technical reason for this
00:06:39.660
it's just everyone agreed that if you
00:06:41.759
have related packages on npm you
00:06:45.300
actually just have the actual main
00:06:47.880
umbrella package name like this in
00:06:49.800
forward slash the actual related one
00:06:51.660
that you're installing I think with
00:06:53.280
angular whatever like there's a ton
00:06:55.199
you'll have like at angular and then on
00:06:57.900
slash whatever and so forth we saw this
00:06:59.940
with material design as well you'll see
00:07:01.979
it uses yarn here and so we had a
00:07:03.900
discussion like a couple of videos ago
00:07:05.759
about yarn about npm about pmpm you
00:07:09.780
should be like oh crap how do I install
00:07:11.400
this I don't have yarn effectively just
00:07:13.800
like this you just say npm install
00:07:15.419
instead of yarn add so let's scroll
00:07:17.580
further down a bit I did mention that
00:07:19.800
what react spring does is it actually
00:07:22.220
handles the component outside of the
00:07:25.380
react rendering so it pulls it out and
00:07:27.780
it handles the animation separately and
00:07:29.699
it uses a lot of clever things in terms
00:07:31.740
of using your GPU if you have a a
00:07:34.800
graphics card and whatever so because of
00:07:37.020
that it's custom built elements that you
00:07:39.360
need to pull in you can't just use a
00:07:41.400
standard Dev or a standard span or
00:07:43.740
whatever it has specialized versions of
00:07:47.280
those things that can be animated in
00:07:49.199
performant manners that you need to pull
00:07:51.300
in and you do that in the same way that
00:07:53.340
you would do a styled components we
00:07:55.259
would just go in here animated and then
00:07:57.720
instead of styled with
00:07:59.300
animated.div even and this is once again
00:08:01.860
you know where the reacts functional
00:08:04.919
roots not only reacts functional Roots
00:08:06.720
but this idea of function composition
00:08:08.759
and composition gets really wild because
00:08:11.520
you can even go const and you can do
00:08:14.039
style turf or whatever and you can even
00:08:16.380
wrap that in that you can even style the
00:08:19.919
custom element here so we can say
00:08:21.720
background red that is really really
00:08:23.759
cool and this is like what's so great
00:08:25.560
like these are two completely different
00:08:27.479
libraries they're not maintained by the
00:08:29.160
same team but because of once again you
00:08:31.199
know polymorphism so this idea that
00:08:33.839
takes any thing like it's kind of like a
00:08:36.179
generic almost and it can handle any
00:08:38.219
type of data you don't make assumptions
00:08:40.440
about what you're going to pass in and
00:08:42.419
because you know solid and encapsulation
00:08:44.520
and all of that it means that the way
00:08:46.140
these libraries are built you can just
00:08:48.420
compose them with anything they didn't
00:08:50.100
even know that you're going to use this
00:08:52.320
with style components but the way it's
00:08:54.899
just built it can take anything and
00:08:56.580
apply styling to it I cannot express to
00:08:59.220
you guys how amazing this is let's have
00:09:00.959
a look and let's do a super basic
00:09:02.580
example first so let's pull in that
00:09:04.080
animated component there's a use spring
00:09:06.480
hook so let me show you guys how this
00:09:08.399
works and let's use that style div let's
00:09:10.680
just put it at the far top and this is
00:09:13.320
another thing so let me quickly talk
00:09:14.880
about this you might have encountered
00:09:16.740
this already a react component needs to
00:09:20.100
have only a single chart you can't have
00:09:22.320
two elements at the root of a component
00:09:25.140
like that it's going to give you an
00:09:26.700
error so you need to if you do something
00:09:28.500
like this you need to wrap it in
00:09:30.540
something there always needs to be a
00:09:32.160
single root element why is that that is
00:09:35.040
just the XML thing so in XML you always
00:09:38.220
if you look at any XML even if you look
00:09:40.920
at HTML which is kind of tangentially
00:09:43.019
related to XML you need to have an HTML
00:09:46.380
tag that wraps everything oh there's a
00:09:48.959
tree-like structure and a tree needs to
00:09:51.240
have a trunk you can't have a tree with
00:09:53.640
two trunks that's two separate trees
00:09:56.100
quote unquote you can't say oh this tree
00:09:57.839
has two trunks then it's two different
00:09:59.519
trees you always need to have a root XML
00:10:02.880
element and this is a case where once
00:10:04.920
again the react team said instead of
00:10:07.200
saying like oh this is a pain abstract
00:10:09.540
over this make it easier for people to
00:10:11.580
use manually do something in the
00:10:13.380
background they said like no we're going
00:10:14.700
to opt for technical greatness value of
00:10:17.040
that is you keep the API really small
00:10:18.720
you just learn jsx you just learn XML
00:10:21.180
you're not like oh this is a react
00:10:22.740
specific flavor of this thing you are
00:10:25.500
able to actually set empty fragments if
00:10:28.980
you go like this if you define like a
00:10:31.680
element with nothing in it so
00:10:33.720
effectively Mr opening angular bracket
00:10:36.240
and a closing one that's a kind of a
00:10:37.860
fragment it's the actual name for it is
00:10:40.140
fragment so you can actually pull it
00:10:42.360
from react so you can say react and you
00:10:45.000
can pull fragment and use that it's
00:10:47.040
exactly the same like a actual XML node
00:10:49.860
that doesn't get rendered this is just
00:10:52.079
to adhere to XML it doesn't actually
00:10:54.600
split anything out on the Dom this is
00:10:56.399
just so still technically correct XML
00:10:59.279
this is not correct XML but you can also
00:11:02.820
just write it like that as well as
00:11:04.980
shorthand and react is automatically
00:11:06.839
going to assume anything that doesn't
00:11:09.300
have a tag name is a fragment sorry yes
00:11:11.640
no I was actually going to ask if
00:11:13.140
there's like a major difference between
00:11:15.120
using a fragment or you know a trade-off
00:11:17.519
even if it is a performance one a bit I
00:11:19.620
guess not yeah it's it's literally
00:11:21.600
syntactic sugar but you might be asking
00:11:24.120
like why do you even have this fragment
00:11:26.220
thing at all why not just have this be
00:11:28.620
the only way you can do it and the
00:11:30.240
reason is because there are times when
00:11:32.040
you actually want to specifically
00:11:33.600
reference on something so here's a good
00:11:35.579
example we have a wrapper there it's
00:11:37.980
actually declared okay so we have our
00:11:39.540
wrapper component for whatever reason is
00:11:41.760
button then we want that to be a button
00:11:44.519
because once again remember this is just
00:11:47.220
a function it's a function that you know
00:11:49.740
create element you know it takes
00:11:51.480
something so for example a div you can
00:11:53.519
use a string and you can just say you
00:11:55.440
know Dev because the only thing is this
00:11:57.420
is just the name of the thing you're
00:11:59.399
going to use so you can also
00:12:00.839
conditionally determine what you
00:12:02.880
actually want to pass so you can go you
00:12:06.300
know here's button then it is a button
00:12:08.760
you can use a ternary or you can say you
00:12:10.740
know it's a span otherwise when it
00:12:12.779
renders it determines what it should be
00:12:14.279
let's say you don't want anything then
00:12:16.079
you can actually just say fragment
00:12:17.519
because you can actually either you can
00:12:19.260
use strings for built-in HTML stuff or
00:12:22.140
you can go for example like style div
00:12:23.820
like custom components as well so there
00:12:26.100
is value in being able to actually
00:12:28.260
reference the actual fragment itself
00:12:30.660
because if you do it this way then it
00:12:32.399
actually calls it so it's not component
00:12:34.800
you're actually calling the fragment
00:12:36.300
because when you do this in jsx you're
00:12:38.640
actually calling the thing you're
00:12:39.899
calling the function being able to just
00:12:41.700
pass the target of that actual function
00:12:44.579
call is helpful let me just undo undo
00:12:47.040
undo so in this case we probably need to
00:12:49.139
just wrap it with a fragment you can
00:12:51.720
just do it this way then we don't have
00:12:53.279
to import fragment from react you can
00:12:55.440
actually set the component that also
00:12:57.540
means that you should be able to go you
00:12:59.040
know component fragment but that
00:13:00.839
wouldn't make sense in this case this is
00:13:03.660
something that needs to be output to the
00:13:05.519
Dom so you can do that but then it's not
00:13:08.100
going to render anything like why even
00:13:09.899
have a material UI component if you're
00:13:13.079
going to say treat it as a fake element
00:13:14.940
that's not going to be spit out to the
00:13:16.680
Dom okay so you never pass fragment but
00:13:19.260
there are certain cases where you would
00:13:20.940
as I showed previously well so there is
00:13:23.579
the red animated div that we added and
00:13:26.519
it just acts like a normal div because
00:13:28.380
we're not doing anything with it at the
00:13:30.360
moment so let's animate it and it is as
00:13:33.060
simple as go doing so you get a specific
00:13:36.000
hook animated so use spring is the most
00:13:39.120
basic one and this allows you to express
00:13:41.660
how things should animate in a
00:13:44.220
declarative manner usually you derive
00:13:46.139
the value in use spring from another
00:13:48.120
hook usually so you you base what the
00:13:51.180
actual spring values are based on you
00:13:53.339
know other things that change but it's a
00:13:55.440
way to do it in a declarative manner so
00:13:57.480
let me show you so we have our Hooks and
00:13:59.220
stuff up here but let me just do const I
00:14:02.220
think you just call it Styles usually
00:14:04.019
let's say use spring and use spring from
00:14:07.079
so it animates from from opacity zero to
00:14:10.440
opacity one okay and then what you do is
00:14:13.200
it gives you back an object if you hover
00:14:15.360
over that it gives you an object and you
00:14:17.459
just pre-structure that object or you
00:14:19.920
pass that object as the styles to this
00:14:23.040
custom animated thing because remember
00:14:24.899
this is just an object this is the style
00:14:26.880
element on the Dom so we can background
00:14:29.240
green and whatever I spoke about this
00:14:32.279
quite a bit in one of the videos I think
00:14:34.500
the previous video so if you're not sure
00:14:36.720
what the style thing is on react
00:14:38.880
elements then maybe just revisit that
00:14:41.279
video check it out again this
00:14:42.779
dynamically calculates like what that
00:14:45.300
should be so if you want to add other
00:14:46.680
things you can be structure it as well
00:14:48.779
you know and then you can add like
00:14:50.220
background red or whatever let's just
00:14:52.920
dynamically calculates a value for us
00:14:55.620
wherever that is at that point you know
00:14:58.019
in the in the animation so it animates
00:15:00.240
from zero to one and wherever it just
00:15:02.579
dynamically so we can even if we really
00:15:04.440
wanted to we can even just go you know
00:15:06.420
opacity opacity equals style dot opacity
00:15:10.139
like that you can just force it to be
00:15:12.120
like two or whatever just dynamically
00:15:14.639
updates that for us to keep it short and
00:15:17.279
concise I'm just passing that directly
00:15:19.139
as is but if you want to add other
00:15:21.480
things along with it you can
00:15:22.740
de-structure it it's literally just
00:15:24.300
values and so you can set the time as
00:15:26.519
well I think you do that in the hook
00:15:28.320
itself yeah duration let's make it like
00:15:31.019
10 seconds just to really show the
00:15:33.540
effect and if I reload you go like
00:15:35.880
really slowly okay so this allows you to
00:15:39.720
actually write animations into
00:15:42.240
declarative Manner and you might be like
00:15:43.980
okay this is cool but I can do this with
00:15:45.420
CSS sculpt like why are you wasting my
00:15:47.339
time so work it's really cool is you can
00:15:50.339
derive these values from an existing
00:15:52.980
value so let's actually just put a
00:15:54.660
button in here below this and let's just
00:15:57.180
say toggle and we have another value
00:16:00.839
here that is just above it you state
00:16:05.100
let's say const yeah let's just say show
00:16:08.880
and set show this is also maybe an
00:16:11.459
opportunity to show how we can use
00:16:13.079
another cool Library so I spoke about
00:16:16.440
low Dash then I said you know you also
00:16:18.300
because of reacts functional
00:16:19.860
underpinnings you also get things that
00:16:21.959
are kind of similar to low dash one of
00:16:24.360
them is react use which are like these
00:16:26.880
low level react hooks because hooks are
00:16:29.220
just like functions and you can compose
00:16:30.899
them so these low level hooks that you
00:16:33.660
can come compose you can read over it
00:16:36.720
even if you click on it they have
00:16:38.040
examples so let's find an example so
00:16:42.259
what's a cool one that's maybe we can
00:16:44.880
demo use copy to clipboard okay so here
00:16:47.579
it kind of explains how it works and so
00:16:49.019
forth and they usually have I think they
00:16:51.300
have demos as well if I'm not mistaken
00:16:54.420
yes over here you can see them in action
00:16:57.120
as well you'll see it's actually built
00:16:58.440
in storybook but you don't know what
00:16:59.699
Storybook is just yet
00:17:01.620
um we'll talk about it a bit later but
00:17:03.000
EA you can actually see them in action
00:17:04.919
and the documentation and so forth so
00:17:07.679
but what we want to grab is we want to
00:17:10.380
you grab the use toggle so these are
00:17:12.660
just like small
00:17:14.520
um quality of life things uh as
00:17:17.339
mentioned they like really low level and
00:17:19.980
so all this one does is instead of
00:17:22.140
deliberately setting it so setting it to
00:17:24.179
true or false it's a Boolean you just
00:17:26.160
call the function to switch it to the
00:17:27.780
opposite of what it currently is so once
00:17:29.880
again it's a very low level and you
00:17:31.679
might be like ask I can just write this
00:17:33.299
myself I don't you need a react use and
00:17:36.059
that's the same with low Dash you know
00:17:37.380
like with like low Dash most of that
00:17:39.299
stuff you can write yourself
00:17:41.160
um so it's for you to decide you know do
00:17:43.140
you want to pull in a third party
00:17:44.220
Library it just gives you a lot of the
00:17:45.780
stuff out of the box or do you want to
00:17:47.039
be like no screw this I'm going to write
00:17:48.480
this myself I don't need no Library okay
00:17:50.940
but um there's a lot of other stuff with
00:17:53.400
react use that is super useful and so
00:17:55.740
forth
00:17:56.820
um for example another one is use uh I
00:18:00.660
think there's a used Mount which also
00:18:02.520
fires when a component mounts once again
00:18:05.580
you know like it's super easy to do
00:18:07.020
yourself but like enough if you with
00:18:09.600
enough time like it just saves you time
00:18:11.340
being able to just write these like not
00:18:14.220
have to write all these little things
00:18:15.539
yourself and what's also really cool is
00:18:17.700
it's already documented so you don't
00:18:19.679
need to go and document and say what
00:18:21.480
does this hook do okay you just tell
00:18:23.520
someone go read the react use
00:18:25.020
documentation the same with low Dash as
00:18:26.880
well all right so let's quickly install
00:18:29.280
it
00:18:30.419
um so npm install react use okay and it
00:18:34.500
should install pretty quickly it's a
00:18:35.820
very small library and let me just
00:18:37.860
actually Pull It in here already so from
00:18:40.919
and react use and I want to grab use
00:18:44.700
toggle okay and we can even use it
00:18:47.580
generally you would use it in your own
00:18:49.200
custom hooks because once again you know
00:18:51.059
as I mentioned this idea of composing
00:18:52.620
Hooks and so forth but in our case I'm
00:18:55.200
just going to pull it here directly in
00:18:57.179
here so up here we have use toggle so
00:18:59.940
let's just say you know show and toggle
00:19:02.400
show ah no man okay so show and toggle
00:19:07.260
show so it's effectively just use state
00:19:09.179
that is a Boolean that you can just use
00:19:12.419
toggle show to toggle it from its
00:19:14.100
current state instead of actually
00:19:15.360
setting a specific state so then what we
00:19:18.120
can say is
00:19:20.340
if show is true then this then it
00:19:24.120
animates from zero to one okay the other
00:19:28.440
way around if show is false then it
00:19:31.200
animates from one to zero okay yes
00:19:34.919
exactly so this allows you to express
00:19:37.500
animations in a very declarative manner
00:19:40.500
so let's try that out so on click all
00:19:44.340
right let's see so where is that button
00:19:47.280
I might need to oh I need to restart my
00:19:50.039
server so npm Run start oh Dev sorry run
00:19:54.419
div that's the beat one okay all right
00:19:56.760
so check that out cool all right and you
00:19:59.160
can do loads of other things we can
00:20:00.539
maybe do
00:20:01.740
um what's also really cool about
00:20:04.559
um about uh react use is that by default
00:20:09.179
um it like you need to maybe you need to
00:20:12.179
understand about how reflows in the Dom
00:20:14.220
and so work if you want to do crazy
00:20:16.200
things like uh mutating like like
00:20:19.080
animating things around like to the side
00:20:21.240
or whatever so that it does doesn't
00:20:22.860
Force actual re-render so if you do for
00:20:25.799
use padding to do that good luck your
00:20:27.900
site's going to get destroyed
00:20:29.400
performance wise so what's also really
00:20:31.980
cool about
00:20:33.539
um you uh you use hook there's a oh I
00:20:36.780
brought this up into a separate file
00:20:38.640
um is that it actually just has
00:20:42.240
something called X or Y that actually
00:20:44.760
just abstracts that away for you so you
00:20:47.160
can just say you know the X and the Y
00:20:48.660
position
00:20:49.980
um let me just get rid of the opacity
00:20:52.140
um and it does it for you in a
00:20:53.640
performant manner you don't need to know
00:20:55.380
what is the best way to move things
00:20:57.240
around you just use X and Y and it's
00:20:59.880
like cool I'll figure out what's the
00:21:01.679
best way to do it you don't need to
00:21:03.000
worry you just say what you want okay so
00:21:05.220
now it should move it around if I'm not
00:21:07.740
mistaken yeah check that out you have
00:21:09.900
two x's yeah but I swap them around
00:21:12.960
um as I did last like so I'm
00:21:15.539
declaratively saying X so from X if so
00:21:18.900
then from 0x to 100 but if show is false
00:21:23.820
then from 100 to zero so I just reverse
00:21:26.580
them yeah so
00:21:28.220
[Music]
00:21:30.020
okay so that's all cool but here's where
00:21:33.299
it gets really neat um I'm not gonna go
00:21:35.640
over all the apis because you can do a
00:21:38.700
lot of uh advanced stuff with react uh
00:21:41.520
spring uh just to show you guys a couple
00:21:43.440
of examples if you want to check what
00:21:44.760
you can actually do
00:21:46.559
um you can check on the examples here
00:21:48.179
let's get to some of the advanced ones
00:21:50.100
so
00:21:51.179
um yeah check this out and you can
00:21:52.620
actually check the code here
00:21:54.419
um so it's loading it's like that this
00:21:56.580
is react spring but it uses webgl so
00:21:58.919
this is a toggle it's like a toggle but
00:22:01.140
it's completely all 3D and whatever
00:22:03.440
that's also a cool one yeah so you can
00:22:06.059
even do like stuff like this check this
00:22:07.799
out like it looks like it's underwater
00:22:09.720
or whatever you'll see I said loads yeah
00:22:12.059
so you can do like chicken stuff there's
00:22:13.799
a lot of really amazing stuff in here
00:22:16.620
um like even like crazy stuff like this
00:22:18.900
okay stuff you wouldn't imagine like as
00:22:21.059
you imagine this is like a video or
00:22:22.740
something or a gif or whatever this is
00:22:24.900
all just like JavaScript all right so um
00:22:28.140
I'm not going to cover all of it so you
00:22:29.880
can have a look and you can see you know
00:22:31.799
if you want to play around with it
00:22:33.480
there's a lot of like hooks there's like
00:22:35.520
new spring use transition use chain use
00:22:38.280
Trail Parallax and whatever and some
00:22:40.559
Advanced like API stuff you can do the
00:22:43.200
other one I want to show is use
00:22:44.640
transition so use transition
00:22:47.400
um is very cool in so far that
00:22:50.220
um instead of you supplying like a
00:22:53.640
actual value that it uses to
00:22:55.740
declaratively uh
00:22:57.720
um calculate the weather where like the
00:23:00.600
values
00:23:01.799
um it just automatically has two states
00:23:04.200
so the one is the thing is entering the
00:23:06.900
screen the thing is exiting the screen
00:23:08.820
so it's getting added or it gets removed
00:23:11.760
um so it uses the same API but use
00:23:14.580
transition and so the only so it has
00:23:17.039
from the from is always just where
00:23:19.260
things start from so when it when it
00:23:21.840
actually so let's say when it so the
00:23:25.559
opacity is zero when it gets added so
00:23:28.380
this is the immediate State when it gets
00:23:30.360
added where does it animate two Wards
00:23:33.120
when it gets added to enter to enter is
00:23:36.000
so it when it gets added it goes from
00:23:38.039
from to enter and then obviously it
00:23:40.559
stays on enter as long as it's in the
00:23:42.480
screen and then when it leaves it goes
00:23:44.580
from enter to I think it's exit no leave
00:23:48.299
I think it's leave if I'm not mistaken
00:23:50.520
yes so leave okay so enter is kind of
00:23:53.460
the resting state so it goes from from
00:23:55.140
to enter and it stays and enter as long
00:23:57.059
as it's in the screen and then when it
00:23:59.340
it's deleted it goes from enter to lease
00:24:01.260
and once again you can set the how long
00:24:04.200
it should take I'm just going to keep
00:24:05.340
the default I think the default is one
00:24:06.900
second okay so let me also just remove
00:24:08.940
that so this one works a bit different
00:24:11.039
it's not a style that you just actually
00:24:13.200
actually apply to something it's
00:24:15.840
actually let me just quickly see if my
00:24:19.280
to-do list actually still works if I
00:24:22.440
reload did I break it let's have a look
00:24:24.840
at the errors what's going on here style
00:24:27.659
Dev okay we might need to just comment
00:24:30.659
that out I think it's unhappy if there
00:24:32.460
are actually errors in our code let's
00:24:34.500
just also comment that out all right so
00:24:36.840
I guess if this still works not the
00:24:38.940
prettiest but it works okay so now what
00:24:42.659
we do is so you can probably imagine we
00:24:44.880
need to now wrap our components in this
00:24:47.220
animated thing because react use has
00:24:49.559
special components
00:24:51.780
um most of the time you just wrap it you
00:24:54.120
can keep it as is and you just wrap it
00:24:56.159
in an animated divs okay there we go oh
00:24:58.620
and we need to pull in animated okay
00:25:00.780
okay so everything's still the same it
00:25:02.580
is unhappy because it requires a key so
00:25:05.280
we can put the key on that animated like
00:25:07.919
that all right but so here's the thing
00:25:10.860
we need to pause because if you remember
00:25:13.260
like it does it actually intercepts the
00:25:15.659
rendering so it's not only animating it
00:25:18.120
tells it wait a couple of seconds or
00:25:20.820
wait a second before you remove it so
00:25:23.039
when the virtual Dom detects it needs to
00:25:25.620
be removed wait a second it just needs
00:25:28.080
to animate and then you can remove it
00:25:29.760
and the same for when you add it wait a
00:25:32.100
second before you add it so like because
00:25:34.440
of that we this
00:25:37.080
um where is it now this doesn't return a
00:25:39.419
style what we do is we pass our array to
00:25:42.960
it and it adds that onto the jsx so we
00:25:46.740
pass tasks through it so the first thing
00:25:49.260
that passes tasks but this is probably
00:25:51.720
about too advanced for you guys but what
00:25:54.059
you can do is by default so the hook
00:25:56.640
gave us back Styles object here it gives
00:25:59.279
us back like that array that we can use
00:26:01.740
if you want a bit more fine game get
00:26:04.440
around control you can't destructure it
00:26:06.600
like this to get the second thing as an
00:26:09.059
API so if if you the same with your
00:26:11.279
spring and you can do lots of advanced
00:26:13.559
stuff with that API object that it gives
00:26:15.779
you but we're not gonna we're not going
00:26:17.820
to cover that that's way too advanced
00:26:19.559
but you can check it out if you want
00:26:21.059
first thing it gives us back is what we
00:26:24.179
would have gotten back if this was just
00:26:26.100
a regular use string so the style thing
00:26:29.039
that we got back so this contains like
00:26:31.380
all the animation Logic for that thing
00:26:34.380
the second one is just the item itself
00:26:37.380
this is what we would have gotten if we
00:26:39.900
didn't pass it through this so this is
00:26:42.779
if we just mapped over tasks itself the
00:26:45.120
second thing is what we would have
00:26:46.140
gotten as mentioned you know keep in
00:26:48.179
mind higher order functions you would
00:26:49.620
might be like what on Earth is going on
00:26:52.200
now that's the thing like higher order
00:26:54.000
functions or sometimes it's hard to get
00:26:55.980
your head around it and figure out you
00:26:57.840
need to go and sit and then it like
00:26:59.279
clicks so it's hard to understand but
00:27:01.919
once you understand it it makes the code
00:27:03.900
so simple so you're treating one type of
00:27:06.299
complexity for another type of
00:27:07.799
complexity or treating complexity into
00:27:09.659
of learning and understanding so that
00:27:12.360
has a bit of a higher what would be a
00:27:14.220
little bit with learning curve but once
00:27:17.100
you get over that learning curve and you
00:27:18.659
understand what you're looking at
00:27:20.039
everything is so simple from there on
00:27:21.900
out otherwise the code itself is simple
00:27:23.940
it's simple to understand but it's very
00:27:25.860
hard to understand exactly what it does
00:27:27.900
you hear it's the opposite once you
00:27:29.400
understand that abstraction is actually
00:27:30.480
very easy to understand what it does
00:27:31.860
instead of the other way around just in
00:27:33.480
case you're like skull why like what am
00:27:35.640
I missing here why is this so hard for
00:27:36.960
me to understand and it seems like it's
00:27:38.940
so easy for you you're just like oh yeah
00:27:40.740
and it takes this thing in this thing
00:27:42.240
and that's just because I'm used to I
00:27:44.039
can understand this I'm kind of used to
00:27:46.260
functional code but effectively here
00:27:48.360
what this does it just it's a higher
00:27:50.220
order function it wraps your array and
00:27:52.500
it adds another thing on top of your
00:27:54.059
array if you don't understand words this
00:27:56.940
is simple enough that you can just
00:27:58.140
follow along if you want some super
00:27:59.940
basic animations to your to-do app just
00:28:02.520
do what I'm doing maybe spend some time
00:28:04.980
at a later Point digging into this
00:28:06.659
trying to understand because if you
00:28:08.100
understand it you're going to be able to
00:28:09.179
do some really cool animations let's
00:28:11.520
just Chuck that in there I'll just go
00:28:13.860
directly in there before it gives it to
00:28:16.500
you okay and then this should just be if
00:28:19.440
you don't map over it you call it itself
00:28:21.840
and you pass a function to it so I
00:28:24.659
actually call list and then I pass a
00:28:27.720
function into list and it splits back
00:28:29.820
the jsx to me I don't manually map over
00:28:33.779
it and let's just destruct a key and
00:28:35.940
let's just destruct height from there so
00:28:38.220
let's add a new task and let's see what
00:28:39.840
happens but and you'll see there's like
00:28:41.460
a little short animation of like the
00:28:44.279
opacity but let's actually do something
00:28:45.539
with the X let's actually have it slide
00:28:47.520
in and slide out when we delete it we
00:28:49.799
can do from a list of X and let's do
00:28:52.260
minus 200 and then obviously it should
00:28:55.260
rest at zero when it leaves it should
00:28:57.779
just go 200. hey look how it slides in
00:29:00.779
that's really cool and when you delete
00:29:02.400
it it should slide out but it's not
00:29:04.500
deleting at the moment and it's not
00:29:06.000
deleting because we're also this needs
00:29:08.940
to be ID I think check this out so okay
00:29:11.159
now when we delete it goes out awesome
00:29:13.559
check how cool that is and now when we
00:29:15.480
add it to the Cross slides in that's
00:29:17.279
pretty cool but yeah so that's that's
00:29:19.080
pretty cool you can do some pretty neat
00:29:20.460
stuff with with that type so just
00:29:22.919
knowing a little bit of super basic
00:29:24.539
react spring like is really helpful so I
00:29:27.179
thought I'd just show that to you guys