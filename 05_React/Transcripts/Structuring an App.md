00:00:00.000
what I want to do now is I want to build
00:00:02.639
a super basic to do app in react it's
00:00:05.819
super exciting for me showing you guys
00:00:08.340
how these ideas translate to how you
00:00:11.519
approach your code a lot of it is like
00:00:13.320
you just have to trust me that you know
00:00:15.360
understanding encapsulation
00:00:16.560
understanding these things are important
00:00:18.480
and then I get to show you guys actually
00:00:20.400
how you make meaningful decisions based
00:00:23.400
on like all of these computer science
00:00:25.380
principles if you played around with any
00:00:28.019
of these Frameworks yet once you reach a
00:00:30.779
certain size you kind of realize that
00:00:32.940
parts that you struggle with isn't
00:00:34.680
necessarily how do I change the CSS
00:00:37.200
styling here how do I trigger an on
00:00:39.540
click here and you actually start
00:00:41.700
struggling less with the actual API of
00:00:44.280
the framework itself especially you know
00:00:46.320
if you've kind of worked with the
00:00:48.059
framework for a while like you learn
00:00:49.860
those things and then you kind of
00:00:51.000
understand the framework then the hard
00:00:52.920
part is actually how do you architect
00:00:54.780
projects with that framework how do you
00:00:57.059
where do you decide what should be a
00:00:58.739
component should these things be being
00:01:00.360
the same component should they be split
00:01:02.460
into three different components should
00:01:03.960
this be connected to the store should I
00:01:06.299
pull in a global store at all so these
00:01:08.580
are the type of decisions that I'm
00:01:10.080
hoping to empower you guys to be able to
00:01:12.000
make meaningfully all the other stuff
00:01:13.799
you can just go out to YouTube video
00:01:15.240
learn react in two hours three hours
00:01:17.700
four hours so I I'm gonna pull in Veep
00:01:20.400
now I think I'm gonna get diminishing
00:01:22.439
returns if I show you guys how to do
00:01:24.659
this in codepen because obviously
00:01:26.580
codepen doesn't allow you to break up
00:01:28.500
into different files and those type of
00:01:30.420
things so you don't need to understand V
00:01:33.900
just yet if you want to play around with
00:01:36.240
it you are welcome to follow along to
00:01:39.900
what I am actually doing I'm mindful
00:01:42.540
that if you lose me at any point or you
00:01:45.000
don't know why I'm doing something
00:01:46.799
specific it's not the end of the world
00:01:48.360
don't stress about it too much we're
00:01:50.820
going to do a lot of things and then I'm
00:01:52.140
going to try and explain them the best I
00:01:54.240
can while I'm doing it but we might also
00:01:56.820
need to cover some of it in the next
00:01:58.320
session sorry skog I'm went through some
00:02:01.259
of the beat stuff yesterday and one
00:02:03.299
thing during installation it said like
00:02:05.520
you know you can do typescript or
00:02:07.079
JavaScript but then it has a secondary
00:02:09.479
option for both of them that was either
00:02:11.720
JavaScript or typescript plus swc and I
00:02:15.120
had a hard time finding out what swc
00:02:17.220
means and I still don't know
00:02:19.280
swc of respectively it's it's a
00:02:22.739
rust-based compiler wheat is obviously
00:02:26.120
written in node the swc is like it uses
00:02:31.920
it's written in a different language
00:02:33.599
it's written in Rust lower level
00:02:35.700
language and this is more so you get
00:02:38.099
your languages like python JavaScript
00:02:40.440
PHP these are not compiler level
00:02:44.160
languages so they do a lot of the kind
00:02:46.920
of much higher level they do a lot of
00:02:48.480
stuff like
00:02:49.620
um automatic garbage collection like
00:02:51.720
managing memory for you and so forth
00:02:53.580
there you get your lower level languages
00:02:55.379
like C and so forth okay those are kind
00:02:59.160
of lower level languages you need to do
00:03:01.080
a lot more things like manually set
00:03:03.360
memory what piece of memory do you want
00:03:05.459
to use like that's kind of what the
00:03:07.200
hardcore programmers use so rust is also
00:03:10.140
one of those languages although rust is
00:03:11.640
kind of a very nice introduction to kind
00:03:13.560
of lower level languages I really enjoy
00:03:15.480
rust there's some debacles recently
00:03:17.640
about rust like trade box and stuff
00:03:19.560
which is just like ego gross but in
00:03:22.379
short we Rewritten from JavaScript in
00:03:25.319
Rust it's a lot faster because you work
00:03:27.659
at a lower level but it is still
00:03:29.459
experimental I wouldn't use it unless
00:03:32.580
like your compilation is really really
00:03:34.680
slow and my guess is if you actually
00:03:38.760
like get to the level where like you're
00:03:41.580
working on an app that is getting builds
00:03:44.340
really slowly there's probably some
00:03:46.080
senior lead engineer or whoever who's
00:03:48.239
making these decisions for you so for
00:03:50.940
you guys just stick with the normal one
00:03:52.680
for now what swc is effectively it's
00:03:55.580
experimental version of V that's much
00:03:59.220
faster but obviously because it's it's
00:04:01.560
kind of written in Rust it's not as
00:04:04.019
stable as the the core one at the moment
00:04:05.879
right it's set up super quickly so npm
00:04:08.940
create beat at latest so you should have
00:04:12.239
node installed by this point when we
00:04:14.879
showed the Airbnb style guide and those
00:04:17.100
type of things I I did Cover node so you
00:04:19.620
should have it installed by now if you
00:04:21.720
don't go revisit code style and so forth
00:04:24.300
they actually show you how to set up
00:04:26.340
node so yeah I just wanted to find out
00:04:28.139
yesterday I had a bit of a challenge
00:04:30.419
um I was trying to install the component
00:04:32.400
onto one of my react apps npm didn't
00:04:34.620
want to know its business so I tried
00:04:36.300
yarn so I don't know which one your GTA
00:04:38.699
is better yarn or npm there's three big
00:04:41.160
players at the moment there's bass npm
00:04:43.800
that you just get with node then there's
00:04:45.840
yarn and then there's another one called
00:04:47.940
pnpm I like PMP npm is really fast for
00:04:51.660
these type of things I just actually
00:04:53.880
just use straight up npm when it comes
00:04:55.979
to yarn and npm maybe three years ago
00:04:59.699
four years ago I actually made yawn a
00:05:04.500
non-negotiable dependency of all my
00:05:06.419
products or projects if we wanted to
00:05:08.580
work on the same project that I'm
00:05:09.840
working on you're gonna have to install
00:05:11.520
yarn it's part of the installation
00:05:13.139
process you don't work straight with npm
00:05:15.780
so what is yarn npm is obviously a
00:05:18.780
package manager so there's npm him the
00:05:21.180
repository so npm the the big thing with
00:05:24.539
all the JavaScript packages but then
00:05:26.160
like in order how do you get those
00:05:27.780
packages on your machine there's npm the
00:05:30.000
command line tool as well okay so don't
00:05:32.220
confuse those two so what yarn is yarn
00:05:34.440
is an alternative to the npm command
00:05:37.320
line tool and it's maintained by
00:05:39.120
Facebook and so instead of running npm
00:05:41.580
install you run yarn install or whatever
00:05:43.860
why was yawn created very very very long
00:05:47.220
ago there was this company Microsoft and
00:05:50.759
Microsoft hasn't purchased purchased
00:05:53.160
GitHub yet they haven't purchased npm
00:05:55.560
yet some of you might not even know that
00:05:57.060
that Microsoft owns GitHub and they
00:05:58.740
actually own npm so there was a very
00:06:00.960
long time ago when npm was actually a
00:06:04.199
company on its own GitHub was also a
00:06:06.000
company on its own I don't have a lot of
00:06:07.680
nice things to say about in the npm
00:06:09.900
company before the Microsoft takeover I
00:06:12.000
think a lot of people were like
00:06:13.740
lamenting the fact that they got
00:06:15.360
purchased by Microsoft and like ooh
00:06:17.220
scary Bill Gates I actually think that
00:06:18.960
was a massive upgrade the end PM team
00:06:21.539
was not a nice team there's a lot of
00:06:24.120
reports about super toxic Behavior also
00:06:26.880
they kind of stifled the development of
00:06:29.580
es modules so you know the whole common
00:06:32.160
JS like require es modules import syntax
00:06:35.639
a lot of that's the mess that we're in
00:06:37.500
right now a lot of that is actually the
00:06:39.419
npm team is to blame for that but
00:06:41.340
effectively at some point Facebook was
00:06:43.620
like Hey there are lots of ways in which
00:06:45.720
the npm command line tool can be
00:06:47.759
improved hey npm team here's some
00:06:49.860
suggestions we'll help you with it and
00:06:52.139
the npm team was just like nah thanks
00:06:54.000
bro but nah Facebook was effectively
00:06:55.919
just like okay we're just gonna then
00:06:57.120
build our own we're going to fork npm
00:06:58.740
and build our own tool and so they built
00:07:00.900
one that was much more stable much more
00:07:02.699
better after the purchase by Microsoft
00:07:04.680
npm has gotten substantially better both
00:07:07.080
GitHub and npm have gotten substantially
00:07:09.180
better I would say that npm is now about
00:07:12.300
the same feature parity as yarn yarn
00:07:14.819
gives you a bit more description when
00:07:16.380
you install it gives the emojis come on
00:07:18.240
let's be real what's the real reason why
00:07:20.340
anyone wants to use yawn yarn used to do
00:07:23.039
a lot of cool things like caching so in
00:07:24.840
other words if you install a package
00:07:27.060
install it again it doesn't download it
00:07:29.039
again it uses a local cached version of
00:07:31.199
it lots of stuff like that yarn used to
00:07:33.180
be a lot faster as well you're used to
00:07:35.340
you could do workspaces in PR and you
00:07:37.680
couldn't do it for npm nowadays I would
00:07:39.720
say you're on an npm are pretty much
00:07:41.759
equal that reason alone I wouldn't use
00:07:43.740
yarn just because it's an extra
00:07:45.479
dependency the base one that you can put
00:07:47.940
in papers more or less the same there
00:07:50.220
might be reasons maybe you're like hey I
00:07:51.660
really want the Emojis maybe you just
00:07:54.120
don't like typing npm run with yarn you
00:07:57.599
can just type yarn Dev or whatever
00:07:59.479
nowadays it would come down to like
00:08:01.380
small little things like that I don't
00:08:03.180
think the yarn feature-wise has much
00:08:05.520
more going for it than you get with
00:08:07.259
playing npm the only other one is that I
00:08:10.080
would consider is pnpm I wouldn't
00:08:12.599
consider yawn nowadays if this is a lot
00:08:14.819
of this is confusing you and you're like
00:08:16.259
oh man too many things to think about
00:08:18.900
stick to the npm npm fire nowadays we're
00:08:21.539
luckily at a point where I don't need to
00:08:23.400
tell you to install something extra as
00:08:25.139
well npm is mostly good nowadays but if
00:08:28.080
you find this interesting if you you're
00:08:29.699
interested in looking at other tools
00:08:31.199
pnpm is great it does a lot of like
00:08:33.779
really clever things to really speed up
00:08:35.820
installation and and so forth of modules
00:08:38.700
so Veep npm create createvit at latest
00:08:42.839
then it asks us what do we want to call
00:08:44.760
a project let's just say to do example
00:08:46.680
and what do we want to use we want to
00:08:49.200
use react okay so we just take that
00:08:51.480
space and here is the swc thing that
00:08:54.839
Justin spoke about and we can just go
00:08:56.580
typescript or JavaScript just leave the
00:08:58.800
swc thing for now the type of things you
00:09:01.320
guys are going to be building it's not
00:09:02.820
going to be like it's not going to be
00:09:04.200
worth it so I'm just going to go with
00:09:05.640
playing JavaScript now and we are going
00:09:07.440
to do the the typescript version a bit
00:09:09.839
later and I'll show you guys okay
00:09:11.160
example of Beats those of you that might
00:09:13.440
not know you can actually go code dot in
00:09:15.899
the folder that you are in and it opens
00:09:17.519
vs code in that folder in your terminal
00:09:19.440
and I'm in the wrong folder I need to go
00:09:21.300
into to do example so it comes with like
00:09:24.240
all the eslint stuff set up and whatever
00:09:26.519
I would also pull in the Airbnb stuff
00:09:30.360
but for now just in the interest of time
00:09:32.399
let me just keep it simple you open up
00:09:34.740
your terminal so you go view terminal
00:09:37.500
there or you can press control backpack
00:09:39.899
or command backpack to toggle it like
00:09:42.000
this or if you're one of those weirdos
00:09:44.160
that actually want to run your terminal
00:09:45.779
as a separate thing you can do that as
00:09:47.459
well I just like actually having it in
00:09:49.620
here do I why are you laughing you're
00:09:51.180
one of those weirdos I know it you know
00:09:53.040
what my computer needs more tabs and
00:09:55.860
windows like there isn't enough of them
00:09:58.019
when I all tab like it's too easy to get
00:10:00.540
where I want to go I want to add even
00:10:02.220
more stuff that I need to I'll tab
00:10:03.899
through so we need to still do npm
00:10:06.000
install so we just set everything up for
00:10:08.399
us we still need to install the
00:10:09.899
dependency depending on how fast your
00:10:12.000
connection is that might go pretty fast
00:10:14.940
it might take a long time quickly so npm
00:10:17.519
run Dev you can just control or command
00:10:19.740
click on that to open that in the
00:10:21.779
browser and there we go we aren't using
00:10:24.300
this go live that we did here previously
00:10:26.459
for several reasons because the code
00:10:28.620
needs to be compiled so all the stuff
00:10:31.019
you can Source if you actually build
00:10:33.000
your code so npm run build you'll see it
00:10:36.180
actually compiles all of that for us I
00:10:38.519
think there's a distribution folder it's
00:10:40.500
a dist so here it actually creates all
00:10:42.779
of that for us but obviously it's it's a
00:10:45.420
pain to actually compile it every time
00:10:47.399
and view it in the browser so that's
00:10:49.320
where you run what's called hot module
00:10:51.480
reloading so npm run Dev stuff like Veet
00:10:54.300
give us what's hot module reloading so
00:10:56.459
it spins up a like a server for us
00:10:59.279
there's some clever stuff with like web
00:11:01.079
sockets and whatever to not actually
00:11:02.820
refresh the page so when you update
00:11:04.800
something it just swaps out that little
00:11:06.360
part and so it's really fast so you
00:11:08.519
might hear about like um hot module
00:11:10.680
reloading and that's effectively what it
00:11:12.779
is oh hot module replacement sorry my
00:11:14.940
bad but it does some clever stuff um
00:11:17.040
webpack was the one that originally did
00:11:18.899
it it doesn't clever stuff you just
00:11:20.459
actually swap out the little piece of
00:11:21.839
code you'll also see if you for example
00:11:24.300
kill the server so controller command C
00:11:27.300
to just stop it or you can click that
00:11:28.980
little Trash Can up there then you'll
00:11:31.320
get some errors here it's polling and
00:11:33.959
you'll you'll see I kind of get that
00:11:35.640
error because it uses websockets so at
00:11:37.860
web talk it's all they keep a connection
00:11:39.660
open so for example something like figma
00:11:42.000
uses websockets or Google Google Docs if
00:11:45.720
someone edits with you you see their
00:11:47.279
Mouse moving around or whatever that's
00:11:48.660
websockets so it doesn't send an HTTP
00:11:50.940
request it keeps the connection open and
00:11:53.040
it just streams information up and up
00:11:55.680
and down the server connection what
00:11:57.660
module replacement also uses websockets
00:11:59.700
which is why now it's giving some errors
00:12:01.260
because it's saying the the websocket
00:12:02.940
connection has actually closed I can't I
00:12:05.160
can't access it anymore if you see those
00:12:07.079
type of Errors let us just do npm run
00:12:10.620
Dev one of the first things I do is
00:12:13.680
actually just remove a lot of the
00:12:15.420
boilerplate stuff that comes with it so
00:12:17.160
I just remove this app CSS index CSS
00:12:21.300
even this app.js so I keep this main so
00:12:25.079
this main file what this does is this is
00:12:27.420
just the entry point so you'll see so
00:12:29.160
that stuff we did was react Dom create
00:12:31.440
root all of that stuff it actually just
00:12:34.260
does all of that for us in here we can
00:12:36.360
even destructure strict mode directly
00:12:38.700
like that from react and just use it as
00:12:41.100
that as a component the strict mode just
00:12:43.440
gives us some extra errors and stuff and
00:12:45.480
it's giving an error here because we
00:12:47.279
deleted app.jsx and we deleted index.csx
00:12:50.820
so we're trying to import it and it no
00:12:53.160
longer exists so there we go remove that
00:12:55.500
what I usually do is I create data
00:12:57.540
components folder and then in that
00:12:59.160
components folder have my components as
00:13:01.440
separate you know like as an actual
00:13:03.000
folder in itself then we also just get
00:13:04.440
rid of this assets over here so let's
00:13:06.899
start by creating an app folder well let
00:13:09.600
me keep it simple for now actually let's
00:13:11.399
just put our app jsx in there like that
00:13:14.220
and let's just add another component
00:13:15.839
quickly let's just call it like
00:13:17.300
button.jsx okay so we have two
00:13:19.260
components I usually do it as named
00:13:22.139
exports so I do it that way you can do
00:13:25.380
it as a default export and remember what
00:13:27.959
I said that a react opponent is just a
00:13:30.300
function so let's just do so export
00:13:32.459
const app there we go uh let's just do
00:13:35.160
return div one two three so it's
00:13:38.160
actually components you can even remove
00:13:40.139
the public folder directly what I
00:13:42.300
usually have I just have a source folder
00:13:44.160
I have the main that sets up the react
00:13:47.100
project and then I just have my
00:13:48.660
components that I import into Main and
00:13:50.760
so forth includes a lot of stuff to show
00:13:52.800
you how you can use react there's two
00:13:55.139
schools of thought so there's a lot of
00:13:56.399
people that would say a you need to
00:13:58.440
start with a uml chart and map out
00:14:01.260
everything first I don't know like I
00:14:03.779
guess there's value in that I actually
00:14:05.579
find a lot of value prototyping and
00:14:08.220
thinking through my code by means of
00:14:10.380
prototyping just getting in the code
00:14:12.540
writing a couple of stuff moving it
00:14:14.880
around I actually find trying to plan
00:14:17.639
everything out forehand to have
00:14:19.560
diminishing returns some people might
00:14:21.480
get angry if I say that because you know
00:14:23.880
there's this idea that you need to spend
00:14:25.740
a lot of time thinking and thinking
00:14:27.300
about things before you do it I actually
00:14:29.279
prefer to think in terms of code but I
00:14:32.519
think the key distinction here is I try
00:14:34.500
and figure out how I'm going to
00:14:36.120
structure something by coding but then I
00:14:38.639
get to a point where I'm okay cool I
00:14:40.139
have it figured out now now I'm going to
00:14:41.639
do the real thing I think what a lot of
00:14:43.139
people do is they create this mess they
00:14:45.000
prototype stuff and then they're like
00:14:46.260
all right done it's working okay so
00:14:47.940
there's a key distinction here that I
00:14:49.500
definitely have a phase where I try and
00:14:50.880
figure out how I'm going to structure it
00:14:52.440
but I do find diminishing returns and
00:14:54.480
doing it in this way I would just dive
00:14:56.339
directly in here if we're doing like a
00:14:58.680
get flow of branches or whatever you
00:15:00.720
could start making a mess and you're
00:15:01.980
like okay I just made it worse you just
00:15:03.660
wipe that branch and you start again
00:15:05.339
personally for me I I find a lot of
00:15:07.380
value in Thinking by coding this is also
00:15:09.839
another thing you might find a lot of
00:15:11.339
articles that are like how to structure
00:15:14.339
a react project and a lot of you might
00:15:16.800
have Googled something like this you
00:15:18.360
might find something like this and
00:15:19.680
you're like oh cool awesome okay I'm
00:15:21.300
just going to follow this this is how to
00:15:23.160
structure your app don't pay mind to any
00:15:25.500
of this stuff anyone who has experience
00:15:29.279
or who's usually react for a long time
00:15:31.260
will tell you that point of react and
00:15:34.199
water react is so popular is it doesn't
00:15:36.380
enforce the actual structure this is
00:15:38.820
where stuff like meta Frameworks and
00:15:40.740
whatever come in anyone who tells you
00:15:43.079
how to structure react app they don't
00:15:46.079
know what they're talking you know it's
00:15:47.220
similar to kind of BuzzFeed articles
00:15:48.899
that you know 10 tips to get that job
00:15:51.480
interview or whatever it's like I don't
00:15:53.399
know treat it with some suspicion to
00:15:55.320
kind of hone this point even further Dan
00:15:57.660
abramov also one of the I think the
00:16:00.300
smartest software developers at this
00:16:02.279
point in time very big core react
00:16:04.440
Project Lead people ask them how do you
00:16:07.199
structure react project this is his
00:16:09.660
answer start by putting everything in
00:16:11.639
one file when it feels like it's
00:16:13.079
annoying start splitting it up that gets
00:16:15.360
annoying add some folders someone asked
00:16:17.040
him last year do you still stand by this
00:16:18.600
and he said sure why not I like how
00:16:20.579
someone framed it as annoyance driven
00:16:22.620
development effectively that's it move
00:16:24.839
stuff around until it feels right there
00:16:27.000
is your your advice for how to structure
00:16:29.399
a react project this is also where all
00:16:31.560
those things about encapsulation all
00:16:33.120
those concept that we learn is going to
00:16:35.339
help you figure this out this is the
00:16:37.620
work of writing JavaScript this is where
00:16:39.660
the workout the work doesn't happen by
00:16:41.339
figuring out how to use you state how to
00:16:43.680
use effect installing style components
00:16:45.600
all that stuff that's trivial this is
00:16:48.060
where the Crux of development happens
00:16:49.820
figuring out where to put things
00:16:52.139
figuring out how to encapsulate things
00:16:54.060
what needs to go in its own file and so
00:16:56.040
forth I start with one big app opponent
00:16:59.279
and I throw everything in there until it
00:17:01.860
gets unwieldy and then I kind of split
00:17:04.140
it out because I allow kind of like
00:17:06.299
these structures and stuff to start
00:17:07.859
emerging organically and then I'm like
00:17:09.839
okay cool all right this seems yeah I
00:17:11.939
can see something starting to form or
00:17:13.500
whatever and the same for like Global
00:17:15.119
stores all of that stuff a lot of people
00:17:17.040
would create a project that immediately
00:17:18.900
pull in Redux or whatever I would just
00:17:21.240
like actually use regular State use
00:17:23.459
State until I'm like okay this is
00:17:25.559
getting a bit unwieldy this is getting a
00:17:27.359
bit out of control then I'd solve that
00:17:29.220
problem be careful of premature
00:17:31.020
optimizations don't solve problems you
00:17:34.380
don't have yet the reason being here's a
00:17:36.660
trick about complexity complexity just
00:17:38.520
goes in One Direction things don't get
00:17:40.440
less complex the longer you work on them
00:17:42.360
the more you work on something the more
00:17:44.880
complex it tends to get an app that's 10
00:17:46.860
years old is going to be way more
00:17:48.120
complex than the app that's one year old
00:17:49.740
do not add complexity for the sake of
00:17:52.860
adding complexity be very careful when
00:17:55.500
you add complexity that you're actually
00:17:57.179
solving a problem that you're having
00:17:58.559
because you can get to a point where
00:18:00.660
you've added all this stuff to solve
00:18:02.340
problems that you never actually had and
00:18:03.780
it added all this complexity cost and
00:18:06.120
let's just say tasks okay this is
00:18:08.400
definitely something that we're going to
00:18:09.900
need in our to-do app up until now we've
00:18:12.000
kind of used Imports to you know go dot
00:18:15.360
or whatever and you still do that in
00:18:17.700
react and jsx in things like Veet and so
00:18:20.580
forth you actually when you don't prefix
00:18:23.039
it with a DOT or a forward slash or
00:18:25.080
whatever it assumes you're trying to
00:18:27.179
pull something in from your node modules
00:18:29.760
so node modules effectively are the
00:18:32.640
modules that have been installed so you
00:18:34.380
can have a look in your package.json
00:18:35.880
file here so we have two we have react
00:18:37.980
Dom so you'll see in in here it actually
00:18:40.320
pulls in you know react Dom and react
00:18:42.660
here when you're actually pulling in an
00:18:44.520
actual file in your project you start
00:18:46.140
with DOT forward slash and Dot forward
00:18:48.179
slash just means where you currently are
00:18:50.160
where I currently am go to components
00:18:52.740
and pull in app but when we want to pull
00:18:54.600
in something from react itself we just
00:18:56.220
write it like that press Ctrl space it
00:18:58.260
actually gives us a lot of
00:18:59.160
autocompletion in terms of stuff that we
00:19:00.900
can't pull and pull in use State you can
00:19:03.360
also do the following you can also pull
00:19:05.340
in the entire react Library something
00:19:07.500
like V does code splitting the
00:19:09.480
performance implications aren't really
00:19:11.220
issue here I just personally like
00:19:13.380
restructuring things that I use directly
00:19:15.660
if only purely for the fact that I'm
00:19:17.340
lazy and I don't want to type out react
00:19:19.140
each time so if you remember what we
00:19:20.820
said about hooks the use State hook
00:19:23.160
which is the one you're using the most
00:19:24.660
is the one that travels things to
00:19:27.059
re-render so when we spoke about
00:19:28.679
reactivity components listen to this
00:19:31.320
when this changes when tasks change and
00:19:34.200
then it tells it to re-rent or
00:19:35.820
re-evaluate so we pass a start thing to
00:19:38.760
use state so when it starts out we don't
00:19:41.640
have anything in here so it's an MP
00:19:44.100
array and then we can use set tasks over
00:19:46.980
here to update it so let's do something
00:19:49.380
simple here so let's test and it's an
00:19:51.660
array with ID let's just add some pretty
00:19:54.120
tasks and just give them unique IDs just
00:19:57.600
a array of objects let's make that the
00:20:00.600
starting ones if you remember correctly
00:20:02.820
jsx effectively is just a way to write
00:20:04.980
functions so that means similar to LIT
00:20:08.039
you actually can pass an array of jsx so
00:20:11.400
it's going to treat that as children so
00:20:13.679
we can actually do a UL like that's a
00:20:16.500
return this from our app and then in
00:20:18.960
there we can just do a map so remember
00:20:21.179
also that you don't in react don't do
00:20:24.240
the dollar sign I sometimes do it by
00:20:26.460
accident and then there's a random
00:20:27.840
dollar sign in my unordered list it
00:20:30.000
would just output it as actual HTML and
00:20:32.400
then in here we can actually write our
00:20:34.559
map so tasks so this is an array and
00:20:37.020
then we can destructure directly from
00:20:38.940
there remember a map takes a function so
00:20:41.700
it's a higher order function you can
00:20:43.140
just grab ID and title vs code is smart
00:20:45.720
enough to actually know what are the
00:20:47.400
things in this object and then we return
00:20:49.320
Then Li for now with the title in it so
00:20:52.380
like because I didn't remove it
00:20:53.760
sometimes I do this by accident and then
00:20:56.100
there's a random dollar sign in my UI
00:20:58.200
this is unhappy why is it unhappy it's
00:21:00.299
unhappy because we never use set tasks
00:21:03.120
so it's like hey why do you even pull
00:21:04.620
this thing out if you're not using it
00:21:06.120
then also we're not using ID then
00:21:08.340
there's another thing here which is
00:21:10.140
missing key prop for element in react
00:21:13.500
when you're mapping over you need to
00:21:15.720
give it a unique key and so here I'll
00:21:18.299
just use ID I'm going to talk about that
00:21:20.160
in a second now what is this key thing
00:21:22.260
and why do we need to do it there's
00:21:23.880
actually a example that actually shows
00:21:26.940
this a lot better let me actually see if
00:21:28.559
I can find that speed because spelled
00:21:30.419
also uses the same principle and
00:21:32.220
actually they actually do a good job of
00:21:34.080
explaining why you need to add keys and
00:21:36.720
and this is also the thing I mean you
00:21:38.520
know a lot of these Frameworks are very
00:21:39.960
similar they do a lot of the same things
00:21:41.880
I would actually encourage you to play
00:21:43.500
around with different Frameworks because
00:21:45.000
it here's a good example of where svelp
00:21:47.400
actually does a better job of explaining
00:21:49.320
why you need to do this than the react
00:21:52.020
documentation does so at the very least
00:21:54.000
if you play around with other Frameworks
00:21:55.620
you might get a better idea of why react
00:21:57.659
does certain things because in svelt it
00:21:59.880
doesn't use mapping it uses something
00:22:01.620
called directives so you just say each
00:22:04.260
thing as things so this create multiple
00:22:06.780
versions of something so a list or
00:22:08.760
whatever so here it creates the emoji
00:22:11.039
for Apple it takes this array and then
00:22:12.900
it Maps over it to create this when you
00:22:15.900
modify the value of an each block it
00:22:18.240
will add and remove items at the end of
00:22:20.640
the block and update any values that
00:22:22.380
have changed this might not be what you
00:22:24.179
want so here just shows the behavior the
00:22:26.460
problem is the way that a jsx Works
00:22:30.299
remember it just Compares One virtual
00:22:33.659
Dom to another one let's say in our
00:22:36.000
virtual Dom we have these three things
00:22:37.740
okay A B C in it this one has one two
00:22:41.280
three in it and this one has hello in it
00:22:43.620
so then we give it a new virtual Dom
00:22:46.080
we've just removed this one two three
00:22:47.820
one it Compares these okay it goes over
00:22:50.820
this and it's like cool there are no
00:22:52.140
changes here it's like oh okay this one
00:22:54.659
there are changes so make this change
00:22:56.580
and oh there are changes here make this
00:22:58.980
change remove it so it Compares those
00:23:01.140
elements but it Compares these it goes
00:23:04.559
over this and it's like cool there are
00:23:05.820
no changes here it's like this one there
00:23:08.340
are changes so make this change there
00:23:10.320
are changes here make this change remove
00:23:12.120
it but you
00:23:13.799
a lot of performance benefits by
00:23:15.539
actually knowing that something is the
00:23:17.520
same thing between two virtual Dom
00:23:19.320
instances if you give these unique Keys
00:23:22.320
it's actually able to tell that instead
00:23:25.140
of just treating them as distinct nodes
00:23:28.440
that it just Compares again one and the
00:23:30.240
other one if you give these Keys it is
00:23:32.640
able to see let's say these are the keys
00:23:34.740
as well it's a like ABC or whatever it
00:23:37.559
knows between the re-renders that this
00:23:39.840
is the same thing and this is the same
00:23:41.820
thing so it's able to tell that oh the
00:23:44.460
only difference is this thing is gone so
00:23:46.559
all that it does it just like Pops that
00:23:48.539
out of the knob it just removes it
00:23:50.039
instead of treating this as two separate
00:23:53.039
updates as mentioned you know I think
00:23:55.140
spelled does a good job of explaining
00:23:57.840
this very well if it encourage you to
00:24:00.059
check out this felt documentation
00:24:01.500
because it's felt it's the exact same
00:24:03.480
thing because you know when you want to
00:24:05.520
write declarative code and want to use
00:24:08.340
rendering on declarative UI then like
00:24:11.880
this is something that's going to come
00:24:12.960
up at some point and there is value in
00:24:15.840
knowing when something gets removed
00:24:17.460
instead of just treating everything as
00:24:19.260
an update if you don't understand any of
00:24:21.120
this don't worry give me a very long
00:24:23.039
time to actually understand this I've
00:24:24.659
been using react for a very very long
00:24:26.220
time before this actually clicked for me
00:24:27.780
it's also just fine if you don't
00:24:29.400
understand this and you just know that
00:24:30.960
when you are mapping over things you
00:24:33.419
need to for every item that you map over
00:24:35.820
you need to give it a unique key
00:24:38.400
property and that needs to be unique
00:24:40.260
like if there are duplicates it's going
00:24:42.000
to shout at you first and foremost and a
00:24:44.460
lot of weird stuff is going to happen
00:24:45.960
two children with the same key so a lot
00:24:48.480
of weird stuff can happen you can add
00:24:50.280
things and it gets added twice and
00:24:51.960
whatever if you remember correctly with
00:24:53.940
map one thing that you get is you map
00:24:55.799
over the values but you can also get the
00:24:57.960
index can use the index as the ID so I
00:25:01.740
can't go okay so this ID is zero this ID
00:25:04.679
generally that's not recommended and the
00:25:07.860
reason being is that you actually lose
00:25:10.200
the benefit of this because then it
00:25:12.780
actually just does this again because
00:25:14.520
the IDS then change between renders so
00:25:16.980
this ID is then one or zero actually and
00:25:19.799
this one is two but you actually lose
00:25:22.200
the benefit because then it actually
00:25:23.520
does exactly that because it then treats
00:25:25.380
these the same thing these are the same
00:25:27.419
thing and this it kind of Compares that
00:25:29.460
instead of being able to do this not the
00:25:31.380
end of the world sometimes the only
00:25:33.059
thing you have available is the index
00:25:35.460
just keep in mind that if you're using
00:25:37.860
the index then it bases it off the
00:25:40.140
position that something is in and not
00:25:42.360
something inherently about it okay best
00:25:45.179
case scenario you want to have a
00:25:47.159
completely unique ID that's maybe
00:25:48.900
associated with it in the data itself
00:25:51.240
index is better than nothing you can not
00:25:54.120
use a key or apple still work but it'll
00:25:56.640
complain because you know it can't do a
00:25:58.679
lot of performance boosts if you
00:26:00.720
actually do it this way we want now a
00:26:02.580
way to add to that above here let's just
00:26:04.620
wrap all of this in a div it's a form
00:26:07.080
that has an input and a button and we
00:26:10.440
also need a just a label in there one
00:26:12.659
thing though in HTML you can do this you
00:26:15.659
can just write it like that without a
00:26:17.400
closing tag in react you need to either
00:26:20.039
have a closing element or you need to
00:26:22.860
have it be self-closing like that the
00:26:25.140
reason being that remember jsx is
00:26:28.380
actually based on XML it's actually not
00:26:31.140
the same as HTML in XML you always need
00:26:35.039
to close something so you need to close
00:26:37.320
it like that or have it be self-closing
00:26:39.659
for example in HTML you can have you
00:26:42.120
know IMG or whatever without a closing
00:26:44.580
tag but in react everything needs to be
00:26:47.460
closed and that is just because it's
00:26:49.380
based on XML and I think this is also
00:26:52.020
where react you'll find oftentimes that
00:26:54.779
react prioritizes correctness quote
00:26:58.200
unquote correctness over developer
00:27:00.120
experience something like view would
00:27:02.640
allow you to just do this and it'd be
00:27:04.440
like ah make it similar to HTML because
00:27:06.600
it's a better developer experience even
00:27:08.820
though it's technically not correct
00:27:10.440
whereas react would always opt for
00:27:12.600
correctness but opting for correctness
00:27:15.000
it actually makes the abstraction a lot
00:27:17.279
thinner because now you don't need to
00:27:19.799
learn the react specific way of doing
00:27:21.900
things you can just learn like okay it's
00:27:23.760
XML but for functions that's it you can
00:27:26.400
just learn XML and if you know XML you
00:27:28.020
know jsx and react is also a lot closer
00:27:30.960
to the Dom and this is also where is
00:27:33.179
valuable thinking about jsx as actual
00:27:35.940
functions we have you know Dev and we
00:27:38.340
have ID 3 and inside that hello what
00:27:41.520
this effectively does document create
00:27:43.620
element div and then it assigns like
00:27:46.260
attributes to it so it would go live ID
00:27:48.360
equals you know three and then also the
00:27:50.820
pen child or whatever if you you
00:27:52.799
understand this a lot of things in react
00:27:55.740
is also going to be less confusing to
00:27:57.360
you for example one of the things that
00:27:59.340
trip people up is in react you actually
00:28:01.500
write class name instead of class so I
00:28:04.140
would go class name like red button so
00:28:06.539
the reason is because if we have
00:28:08.279
document create element we actually
00:28:10.740
change that with class name that is what
00:28:13.919
it's called in the div there isn't
00:28:15.779
something called class because Clauses
00:28:17.940
is a reserved word in JavaScript class
00:28:19.980
means something else in the Dom when we
00:28:22.500
want to update the class name the class
00:28:24.659
of something we use class name and
00:28:26.580
because this is effectively just a
00:28:28.200
function we need to use what it is on
00:28:30.419
the Dom everything in react is camel
00:28:32.820
case because it it actually mirrors what
00:28:35.220
it is on the actual Dom attribute you
00:28:37.740
know example you don't write it like
00:28:39.480
this in jsx you write it like that
00:28:42.179
because chances are that's probably how
00:28:44.340
it's expressed on the actual Dom keep in
00:28:46.679
mind like this is an object you're just
00:28:48.600
using XML to write it in a more
00:28:50.880
declarative manner whereas something
00:28:52.919
like view or whatever this is actually a
00:28:55.320
string you might be like okay but why
00:28:57.059
doesn't react just do this okay one of
00:28:59.880
the drawbacks is because you are not
00:29:02.159
using like a straight up templating
00:29:04.020
language you're kind of just using a
00:29:06.179
different way to write functions it can
00:29:08.520
get a bit confusing sometimes if you
00:29:10.080
don't understand that distinction by
00:29:12.539
using an actual templating string that
00:29:14.820
is like a few specific templating
00:29:16.620
strings get a lot of benefits because
00:29:18.419
you can control it make it a bit nicer
00:29:21.240
so you just write for example class
00:29:22.620
without class name and so forth the
00:29:24.419
problem is because you're like you're
00:29:26.159
working with strings and working with
00:29:27.779
templating then instead of jsx if you're
00:29:30.059
using jsx and vs code understands that
00:29:33.720
jsx is just a way of writing function
00:29:36.240
like you actually get a ton of stuff for
00:29:39.059
free you it actually treats it as
00:29:40.980
functions so you know you get Auto
00:29:42.600
completion errors like it tells you like
00:29:44.520
listen you know this is a this thing
00:29:46.320
doesn't exist or whatever for free just
00:29:48.659
because it knows what it is whereas if
00:29:51.299
you're using view or whatever you need
00:29:53.100
to actually install specific plugins I
00:29:55.679
think volar this is a view one so you
00:29:58.200
need to install these plugins the same
00:29:59.760
with spell you need to install plugins
00:30:01.559
to get like syntax highlighting and
00:30:03.480
whatever and this is also the magic
00:30:05.520
about like react you might not realize
00:30:08.100
this you know there is no react plug-in
00:30:10.559
you can just write react react it's just
00:30:12.659
plain JavaScript and so the only stuff
00:30:14.520
that here is like Snippets and whatever
00:30:16.020
you know like so if you want like quick
00:30:17.580
Snippets over this isn't actually by the
00:30:19.740
react team these are just like random
00:30:21.299
stuff that people create as we dive into
00:30:23.520
the other Frameworks I think the other
00:30:25.200
one that's made thinner than react is
00:30:27.960
let just in terms of it's closer to the
00:30:30.179
Dom and so forth but in terms of an
00:30:31.980
actual abstraction on top of JavaScript
00:30:33.779
like react is so tiny and that's what
00:30:36.600
makes reactor powerful at the end of the
00:30:38.760
day you're just writing JavaScript this
00:30:40.559
map all this stuff this is just plain
00:30:42.480
JavaScript whereas in spelled or
00:30:44.460
whatever they spelled specific
00:30:45.840
directives that you need to use what's
00:30:47.880
really great about react is the better
00:30:49.500
you get it react the better you get a
00:30:50.880
JavaScript and likewise because react
00:30:53.100
apis are small most of it is just plain
00:30:55.080
JavaScript so here we have this let's
00:30:57.120
bring this in here the new task so and
00:31:00.419
let's just do a submit button the button
00:31:02.700
uh let's just do type submitting a
00:31:04.559
couple of things you'll see that if we
00:31:06.720
type this it actually reloads the page
00:31:09.179
you'll see it so this is still just
00:31:10.799
plain like HTML the planes JavaScript
00:31:12.779
Behavior react doesn't abstract this
00:31:15.000
away for us we need to actually do the
00:31:16.740
prevent default here some Frameworks
00:31:19.559
actually do this on your behalf they
00:31:22.200
actually stop a form from submitting in
00:31:24.840
react you need to manually do it so
00:31:26.399
let's pass an event handler so if you
00:31:28.260
remember I said on click on submit on
00:31:30.419
change that is how you do event
00:31:32.820
listeners in react on submit so we put
00:31:35.279
that on the form itself and say unsubmit
00:31:37.380
and we do let's just do handles a handle
00:31:40.080
submit takes the event from the form so
00:31:43.440
the event get the target of the event
00:31:46.020
you structure the target which should be
00:31:48.179
the form itself from that we can just
00:31:50.279
create form data so we say new form data
00:31:53.580
so what this does it takes what's
00:31:55.200
currently in the form for us this is all
00:31:57.179
just plain JavaScript playing HTML this
00:31:59.279
isn't react specific you can copy this
00:32:01.260
and put this in a regular event handler
00:32:03.360
in HTML or JavaScript pause the Target
00:32:05.880
in there so it creates form data from it
00:32:08.460
then we want to turn that form data
00:32:10.320
because form data is what's called zip
00:32:13.200
so in other words it would express it as
00:32:15.240
name skulk surname so it structures it
00:32:18.960
like this for legacy reasons so we need
00:32:21.899
to turn that into an object object from
00:32:24.720
entries data we need to give it a name
00:32:27.419
otherwise say the name is this is called
00:32:29.880
a title then this is the structure title
00:32:32.340
and let's console log it for now title
00:32:34.620
there we go okay but we still need to do
00:32:36.720
the event prevent default because by
00:32:39.059
default it is going to try and reload
00:32:42.360
the page when you submit a form we
00:32:45.059
obviously want to clear that and go
00:32:46.679
Target reset and that just clears
00:32:49.320
everything in the form itself all that
00:32:51.419
we want to do is we want to to take that
00:32:52.860
title and just add it to tasks so you
00:32:55.080
might be tempted to go tasks you know
00:32:58.140
push you know title let's try that it's
00:33:00.539
going to scream at us it's actually not
00:33:03.000
even doing anything it actually updates
00:33:04.799
it but it doesn't re-render is we need
00:33:07.080
to you know set tasks so we grab the
00:33:10.380
method from you state to change that
00:33:12.600
until it will re-render we need to do
00:33:14.880
that in a completely functional manner
00:33:16.679
it's a treated immutable so what you do
00:33:19.019
is we create a new array spread the
00:33:22.140
current tasks in that array and then we
00:33:25.080
add this title either in front or at the
00:33:28.080
back of the array it actually needs to
00:33:30.120
be an object if you guys remember so
00:33:32.279
let's just say new task and so that
00:33:34.380
needs to be an object ID let me actually
00:33:36.960
show you guys so what I would do is
00:33:39.240
there isn't since we're using npm and
00:33:41.519
node now there is a uuid package so npm
00:33:45.539
install
00:33:46.760
uuid this will create if you guys
00:33:49.559
remember this uuid stuff that I showed
00:33:52.019
uh so this will create a completely
00:33:54.299
unique uuid every time we run this
00:33:56.760
function and that's just across across
00:33:58.559
the board that I use to create unique
00:34:00.539
IDs and so there are different versions
00:34:03.480
of uuid so we want to use the latest one
00:34:06.059
so we pull in that package so these
00:34:08.280
versions are just different calculations
00:34:10.320
to create a unique ID so what I just do
00:34:13.260
is I use version four that's one I
00:34:15.300
usually use and let's just say as create
00:34:17.159
ID so I import version 4 of the uuid and
00:34:21.239
then I just rename it as create ID and
00:34:24.000
then I can just use it in here to create
00:34:25.679
a completely unique ID and let's also
00:34:28.020
just create these as unique IDs all
00:34:30.719
right so new task and title is just
00:34:33.119
title so we just use the shorthand and
00:34:35.219
then we just Chuck in new task there
00:34:37.500
let's check our processes let's say we
00:34:39.780
want to save this in local storage
00:34:42.000
because if we reload it resets so let's
00:34:44.940
just get rid of this test stuff and just
00:34:47.580
give it an empty array so what I would
00:34:49.980
do is that I would maybe now I would
00:34:53.219
maybe start breaking this out into a
00:34:55.199
custom hook but if you want to create a
00:34:57.359
custom hook you just preface at what you
00:35:00.000
use you'll see all Hooks and react start
00:35:03.359
with the use and in the next session
00:35:04.859
we're going to talk about about like
00:35:06.060
what are all the different hooks so
00:35:07.920
there's use callback use context use
00:35:10.740
debug use deferred use effect use ID the
00:35:14.520
main ones that we are using at the
00:35:16.380
moment is use State and use effect but
00:35:19.380
you can create your own custom ones that
00:35:22.800
wrap some of these remember this
00:35:24.480
functional programming principle of
00:35:26.220
composing functions you can compose
00:35:28.500
hooks in react and this is what makes it
00:35:30.900
so amazing for me so let's just call it
00:35:32.579
use tasks inside use task we actually
00:35:35.400
have this use State then what do we
00:35:37.920
return so I generally just return it in
00:35:40.260
the same way that you State this meaning
00:35:42.839
it's an array and the first one is the
00:35:46.079
tasks itself and then secondly is maybe
00:35:48.000
an object of things that we can do to
00:35:50.520
action so I usually split this out but
00:35:52.859
you can do you can expose it in any way
00:35:54.720
you want this is just a factory function
00:35:56.820
because hooks affect effectively or just
00:35:59.220
closures that's just a factory function
00:36:01.440
that creates this behavior for us tasks
00:36:04.560
so let's add remove update at this so
00:36:08.400
let's say you know the consulate say add
00:36:10.380
let's just say title for now remove what
00:36:13.020
remove does is remove protects the ID
00:36:16.560
let's have each of these create new
00:36:18.900
tasks inside new tasks and then it just
00:36:21.540
sets tasks to new tasks what we're going
00:36:23.880
to do is we're going to map over the
00:36:25.260
existing tasks filter okay so what's the
00:36:27.839
logic so we say If an item id does not
00:36:31.440
match the ID that we pass keep it so
00:36:34.320
it's a predicate meaning if this is true
00:36:36.480
it doesn't remove the thing if it's
00:36:38.640
false it removes something so it's going
00:36:40.560
to be false if the ID that we're
00:36:42.599
currently mapping the item we're
00:36:43.920
currently mapping over doesn't match the
00:36:45.960
ID that we pass so what it's going to
00:36:47.880
effectively do it's going to map over
00:36:49.140
the array using filter to create a new
00:36:51.480
array for us where the the ID that the
00:36:54.060
past is not in the array saved tasks and
00:36:57.240
new tasks and this is a very good
00:36:59.400
example where you might be like oh okay
00:37:01.619
why all this nonsense why can't we just
00:37:03.780
tasks you know and delete you know
00:37:06.839
delete task whatever whatever just like
00:37:09.180
that um and this is one of the key key
00:37:11.160
things where you know something like
00:37:12.540
one-way data binding creates a bit more
00:37:14.820
work for you but it keeps your code very
00:37:17.940
predictable you're recreating the tasks
00:37:20.640
each time so it's kind of functional
00:37:22.320
program I mean you're not reaching to
00:37:24.060
something and directly mutating it
00:37:25.740
you're creating a new thing and passing
00:37:27.599
the new thing so data only flows in a
00:37:29.820
single Direction you don't go back up
00:37:31.500
and change things it's just to ID create
00:37:33.780
ID and title and let's just leave update
00:37:37.020
for now okay so we have add and remove
00:37:38.579
so use tasks now we can pull that in you
00:37:42.060
need to prefix custom hooks of use you
00:37:44.820
can't do that um it's actually going to
00:37:46.560
complain and it's going to say use state
00:37:48.720
is called in a function that is neither
00:37:50.880
a function or a hook it's actually
00:37:52.859
pretty nice so there is a eslint plugin
00:37:55.560
called react hooks that warn you when
00:37:58.140
you're actually breaking the rules of
00:38:00.420
hooks beat actually includes it by
00:38:02.460
default which is nice but you need to
00:38:04.200
start all hooks need to start because
00:38:06.180
this towels react check for a re-render
00:38:08.880
if it's just a regular function it's not
00:38:10.800
going to influence whether it should
00:38:12.240
check for a rearender so this tells it
00:38:14.820
you know in terms of reactivity this is
00:38:17.640
bound to specific things so you need to
00:38:19.980
check it and check if you should update
00:38:21.540
then this is where you start making
00:38:23.099
decisions around abstraction and so
00:38:25.020
forth whether you should include this
00:38:27.359
form submit in here and like there is no
00:38:30.420
right or wrong answer it depends on kind
00:38:33.119
of once again single responsibility and
00:38:35.400
and so forth what is how are you
00:38:38.520
architecting your code like how are you
00:38:40.320
splitting your code up but for now I'm
00:38:42.240
just going to put it in here if only to
00:38:44.099
show you
00:38:45.119
um how creating custom hooks actually
00:38:47.700
make your code much much more readable
00:38:49.920
so let's just say form submit task okay
00:38:52.320
so we can get rid of this and then we
00:38:53.880
can actually just have in here add and
00:38:56.400
we just pass title so this is so what's
00:38:58.619
cool about like Factory functions is
00:39:00.240
like this function that you create here
00:39:01.800
you can just call it directly in here in
00:39:04.200
this closure you don't need to go and
00:39:05.880
Fiddle with this and all of that
00:39:07.859
nonsense right so let's pull in so let's
00:39:10.560
do const and let's pull in what was it
00:39:12.839
the use tasks and use tasks the tasks
00:39:16.140
itself and then just the structure from
00:39:18.599
there it's easier actually for it
00:39:20.400
without typescript to do it in this way
00:39:22.079
so let's just do it in this way so if we
00:39:24.000
just destructure it from an object yeah
00:39:26.099
so full typescript it's actually so
00:39:28.020
let's do form submit let's just pull
00:39:29.760
that out and let's pull out tasks okay
00:39:32.040
so all of this is now behind this use
00:39:34.140
tasks logic then we just pass form
00:39:36.599
submit so now we actually keep our app
00:39:38.579
just for actually rendering that jsx and
00:39:42.000
we put our logic inside the actual hook
00:39:44.760
hey okay so that works so let's actually
00:39:47.160
make a way to delete it so in the LI you
00:39:50.640
know there's a span say button which is
00:39:52.859
just you know an x on click on that
00:39:55.260
button so here I will just do an inline
00:39:57.720
function and I would just say remove
00:40:00.119
once again like the way in which whether
00:40:02.820
you decide to do an inline function or
00:40:04.859
not or a Handler those are the decisions
00:40:07.740
that you need to make and that's going
00:40:09.839
to depend on what it is that you're
00:40:11.460
building like this is what I'm hoping to
00:40:13.500
equip you guys for to be able to make
00:40:15.720
those decisions meaningfully in terms of
00:40:17.820
abstraction and so forth if we then go
00:40:19.859
remove and we can just pass the ID there
00:40:22.680
so we actually for every one of these
00:40:24.420
we're creating a custom event listener
00:40:26.460
that just tells it when this button gets
00:40:28.619
clicked via that okay and if I click one
00:40:30.839
of them it should oops it removed all of
00:40:32.760
them that wasn't good so this is also
00:40:35.099
where this one-way data binding is is
00:40:37.440
really cool because what we can now do
00:40:38.940
is okay something weird is going on here
00:40:40.619
so let's log here let's follow the flow
00:40:43.800
of the data so Mr removed let's see what
00:40:46.800
is the ID that gets passed to that all
00:40:49.200
right let's inspect let's see okay okay
00:40:51.720
so that fires with and what we can also
00:40:54.420
do is let's log the ID and let's log
00:40:56.880
what are all the tasks at that point I
00:40:59.460
think also like once we start looking at
00:41:01.859
some of the other Frameworks and you
00:41:03.180
stop playing around with them you're
00:41:04.619
also going to have an appreciation for
00:41:06.240
how much easier this treating the the
00:41:09.060
direction that your data can flow in as
00:41:11.640
a single Direction how easy it makes it
00:41:13.740
for debugging because once again we can
00:41:15.480
just check at this specific render what
00:41:17.400
are the values I always never do that
00:41:19.440
kind of break point uh debugging where
00:41:21.780
you kind of Step through things because
00:41:23.339
react makes it so easy to just log a
00:41:25.560
specific State at a specific time okay
00:41:27.300
so let's see there we go so something
00:41:29.220
weird happens yes sir three b six four
00:41:32.760
so this one is right why does the others
00:41:35.460
get removed as well ah I found it yo man
00:41:38.160
I feel like a naked man without static
00:41:40.680
type checking I often say that I think
00:41:42.660
static type checking has made me lazy
00:41:45.000
because I no longer look at my code AS
00:41:47.880
critically because I just assume I was
00:41:50.040
going to give a red squiggly line if
00:41:51.420
it's if it's wrong I never return this
00:41:54.119
it's always going to be false because
00:41:56.520
nothing gets returned so I I either need
00:41:58.920
to write it like this or I need to do
00:42:01.800
that if this was typescript it would
00:42:03.900
complain and it would say listen this
00:42:05.339
needs to be true or false it's undefined
00:42:07.200
at the moment but because of falsiness
00:42:09.180
and all of that it treats undefined as
00:42:11.220
yeah you probably made false you
00:42:12.780
probably meant it wasn't a match okay
00:42:14.640
there we go it is as simple as that this
00:42:17.099
should now fix it hey look at that so
00:42:19.800
the last thing we want is obviously now
00:42:21.359
if we reload we want it to stick around
00:42:23.160
so what I would do is I would actually
00:42:25.020
create a factory function that creates a
00:42:27.300
bit of a local storage abstraction for
00:42:28.859
me uh let's just call it create local it
00:42:31.619
just takes an ID take the uuid and
00:42:34.680
assign that to a specific piece of local
00:42:38.220
storage for example if we have a look at
00:42:41.339
Biometrics or whatever you'll and we
00:42:43.260
look at local storage you'll see that
00:42:45.359
there's a couple of uuids in local
00:42:47.099
storage first of all there's something
00:42:48.839
to be said for security through
00:42:50.400
obscurity if I'm a hacker or whatever
00:42:52.560
I'm looking at this I don't know what
00:42:54.240
this is if I call this user password or
00:42:57.240
whatever you should security through
00:42:58.680
obscurity which is actually that's not a
00:43:00.599
clever term I made up people talk about
00:43:02.280
superiority through obscurity in other
00:43:04.140
words things are a bit more obscure it's
00:43:06.540
harder to kind of hack and whatever I
00:43:08.940
just do that and also what's really cool
00:43:11.220
about this is if I wanna in the next
00:43:14.160
version break that cache I just generate
00:43:16.800
a new uu ID and then it's gonna like
00:43:19.440
actually treat it as a completely new
00:43:21.359
saved version otherwise if I call this
00:43:23.760
you know save tasks or whatever now if I
00:43:26.579
want to bust that cache in other words
00:43:28.200
if I want to have it now actually be
00:43:30.480
like oh we should get rid of all the
00:43:32.160
same things now and create a new saved
00:43:34.140
version then I have to go like version
00:43:35.579
one or two or three or whatever doing a
00:43:38.400
uuid is just easy just create a new uuid
00:43:40.859
and then it's almost a new version so I
00:43:42.960
just pass the IDE and that is what's
00:43:44.640
used for the local storage so I then do
00:43:48.060
because it's a factory function I just
00:43:50.040
do get them set you can do these as
00:43:52.380
legit Getters and Setters I do them
00:43:55.260
actually as functions because I prefer
00:43:57.300
just functions instead of mutating
00:43:59.700
things directly get S A get is just a
00:44:03.180
function inside this closure that I'll
00:44:05.400
talk a bit more about local storage in
00:44:07.500
the next session there isn't much time
00:44:09.720
left so I'm speed running through this
00:44:11.640
but if you don't know what local storage
00:44:13.740
is I'll talk about that in the next
00:44:15.660
session so we can do you know response
00:44:18.599
window local storage get item and
00:44:22.140
whatever ID we pass why do we also do it
00:44:24.839
like this because then if we want
00:44:26.220
another value we can reuse this for
00:44:28.560
whatever local values we want to say so
00:44:30.720
it will return a string if there is
00:44:33.240
something otherwise it will return null
00:44:34.980
we can say if nothing is returned then
00:44:38.160
just return an empty array if something
00:44:40.920
is returned then turn that into that
00:44:44.520
string into an actual Json in actual
00:44:47.220
JavaScript object it's a response for
00:44:49.800
set we need to turn it into a spring
00:44:51.780
because it can only save a string in
00:44:54.480
local storage if you want to save an
00:44:56.040
actual object if you try and save an
00:44:57.540
object that's going to save it as object
00:44:59.760
object like that because because
00:45:01.500
remember objects are references when I
00:45:04.920
am working with this the actual object
00:45:07.500
itself isn't stored in response it's a
00:45:09.900
reference to the object if you remember
00:45:11.880
all the way back when we spoke about
00:45:13.680
primitive values and references and
00:45:15.420
composite types and so forth so what
00:45:17.460
you're doing here is you're saving the
00:45:18.780
reference which isn't useful at all
00:45:20.640
because when you reload the app then
00:45:23.099
that reference no longer exists the
00:45:25.260
thing that it points to no longer exists
00:45:26.760
what we do is we take that object we
00:45:28.440
turn it into a string and we save that
00:45:30.180
string and then when we load the app we
00:45:32.099
kind of take that string back and we
00:45:33.540
turn it back into an object okay so what
00:45:36.180
we want to do here is then let's just
00:45:38.280
say value let's just say string and we
00:45:40.619
do Json stringify so Json allows us to
00:45:43.319
do string of file parse parse Texas
00:45:45.359
string turns it into a JavaScript object
00:45:47.400
Springer file takes the object turns it
00:45:49.440
into a string yeah let me say value and
00:45:52.020
then we just set so window dot local
00:45:54.780
storage set item the ID and just the
00:45:58.560
spring there we go that is so there's
00:46:00.660
our attraction create local let's just
00:46:03.180
say save and so then in here in our
00:46:06.060
custom hook we can actually just use
00:46:07.980
effect so we tell it listen for tasks
00:46:10.380
when tasks change do the following pause
00:46:13.500
an array of things to listen to I'm
00:46:15.960
going very fast through this in the next
00:46:17.940
lesson or maybe come back to this
00:46:19.740
example and step through it slowly again
00:46:21.720
and cover what we've done okay so when
00:46:23.819
it updates saved set to tasks okay so we
00:46:27.720
just tell it whenever tasks update just
00:46:29.700
take tasks on this abstraction that we
00:46:32.040
created just actually set tasks then
00:46:35.520
what we also want to do in here save we
00:46:38.160
want to check if there are any saved
00:46:40.380
tasks and use that as the starting one
00:46:42.480
if they are not then it's obviously
00:46:44.640
gonna return an array is it getting an
00:46:46.980
error it needs to be get item once again
00:46:49.020
typescript has made me lazy I don't
00:46:51.060
re-read my code I just assume I write it
00:46:53.280
and if it doesn't give me a red squiggly
00:46:54.960
then it's fine okay and let's close this
00:46:56.940
window completely open it again and whoo
00:46:59.880
there are tasks if we remove one and we
00:47:03.060
reload all still there so we can
00:47:04.980
actually go an application we can look
00:47:06.420
in local stories here is what's stored
00:47:08.579
in local storage at the moment so here
00:47:10.859
you have an app that can actually save
00:47:13.319
in local storage and it is actually the
00:47:15.839
code is actually very expressive so let
00:47:18.359
me quickly go through it just to show
00:47:20.400
how expressive react allows us to write
00:47:22.500
our code if you try to do something like
00:47:24.420
this with plain JavaScript you know that
00:47:26.700
it starts getting messy really really
00:47:28.859
quickly so we have our create local
00:47:30.839
abstraction here I would probably use
00:47:32.819
put some jstock annotations here for
00:47:35.460
readability but so effectively this
00:47:37.380
creates a local thing for us that we can
00:47:40.440
get and set we assign it a unique ID in
00:47:43.619
our custom hook we create a piece of
00:47:46.020
State we call it tasks we can get it
00:47:48.420
look at it or we can set it to get the
00:47:50.819
starting tasks when the page opens up we
00:47:53.700
use the abstraction we created to get
00:47:55.619
any saved ones if there are if there are
00:47:57.900
no side ones it's just an empty array so
00:48:00.119
that's the starting State we also
00:48:01.920
register a use effect hook that every
00:48:04.260
time tasks update in memory also update
00:48:07.500
this use this abstraction to update our
00:48:09.660
local storage and then we have a
00:48:11.400
function function that adds a task for
00:48:13.619
us to this we have one that removes the
00:48:16.500
tasks from here and we expose both those
00:48:18.900
functions through the hook as a factory
00:48:21.300
function form submit as well I might
00:48:24.420
actually put form submit in here
00:48:26.099
directly I would say the hook probably
00:48:28.440
shouldn't know about the form probably
00:48:30.720
do it in this manner I would say adding
00:48:33.119
or removing a task whether it's from a
00:48:35.520
form or not is not a concern that this
00:48:37.920
hook should actually know about probably
00:48:39.780
just put it in the component because
00:48:41.160
this to me is closer to the actual
00:48:43.260
presentation of the component itself
00:48:45.300
yeah and then we just have our jsx here
00:48:47.220
and then we get all this Behavior I got
00:48:49.800
a bit of a question but uh definitely
00:48:51.540
not so the same way you were doing a
00:48:54.000
markup in that like in previous videos
00:48:55.740
and that you can also do it in react the
00:48:57.480
same way like for JS doc yeah yeah 100
00:48:59.940
so I can comments yeah yeah and this is
00:49:03.180
what's so great about react is it's not
00:49:05.760
a custom templating language it is
00:49:07.740
actually just JavaScript functions so I
00:49:10.200
can go yeah I can go use Style tasks
00:49:12.240
returns and let me just do a quick type
00:49:14.819
Dev up here and let's just say object
00:49:16.859
and let's just say you know a tasks hook
00:49:19.920
or whatever property prop I don't know
00:49:22.859
something string I think it's called and
00:49:26.400
this is the description obviously it's
00:49:28.440
going to be super unhappy now because
00:49:30.480
that's not actually what it returns but
00:49:33.119
theoretically if I then hover over this
00:49:34.980
it should think that it returns that I
00:49:37.319
can hover over that thing and like this
00:49:39.420
but it's not going to be happy but
00:49:41.220
obviously it's unhappy because that's
00:49:42.839
not actually what it returns um but yeah
00:49:45.000
100 show you even in touch screen use JS
00:49:48.060
dot extensively isn't it like Overkill
00:49:51.000
though no in terms of actually marking
00:49:53.940
up the the types yes but there's a lot
00:49:57.480
of information so we're supposed to get
00:49:59.460
type doc as well yeah we can get to that
00:50:02.280
that's a separate discussion but yeah
00:50:04.619
like look at this I I type it up quite
00:50:06.960
extensively because like someone might
00:50:09.359
look at this and they might not know
00:50:10.800
okay what what does reload do okay and
00:50:14.040
now if I hover over it it actually tells
00:50:15.839
me you know find this will cause the
00:50:17.220
browser to do a hard refresh and that it
00:50:19.319
will also remove all data currently
00:50:20.819
stored in the indexeddb cache should
00:50:23.099
yeah only be called when a critical
00:50:24.720
error has occurred and so forth and so
00:50:26.460
forth no I still do a lot of Trash Talk
00:50:28.740
definitely project you have no idea it's
00:50:32.040
not even the worst I like I have a
00:50:33.720
couple of things that I'm working on
00:50:34.800
that is like yeah it just takes 10
00:50:36.900
minutes to open up the project just
00:50:38.460
because of all the files the code gets
00:50:40.440
big guys it goes really big