00:00:01.160
so now we have spoken about a ton of
00:00:03.959
stuff we we've spoken about like this
00:00:05.960
idea of a global State and we kind of
00:00:08.280
looked how functional programming and
00:00:10.080
kind of the Redux like pattern um can
00:00:12.759
help us manage Global state in our app
00:00:15.240
and you'll actually find that kind of
00:00:17.439
Redux pattern while there are some
00:00:20.160
stores that kind of completely go for a
00:00:22.600
different approach more in terms of gets
00:00:24.359
and sets there's also kind of a new idea
00:00:27.519
around how do you manage these type of
00:00:29.199
things that are really relateded to
00:00:30.560
something called signals which Builds on
00:00:32.920
something else called observables um so
00:00:36.000
you might come across a range of
00:00:37.719
different ways to actually manage Global
00:00:40.840
state in your app but it's impossible to
00:00:43.879
overstate how big of a role Redux and
00:00:47.360
the specific Redux approach played in
00:00:49.960
terms most of the popular tooling around
00:00:53.440
Global state that we see um once we
00:00:55.719
touch on Frameworks I'm also going to be
00:00:57.239
touching on what are some common Global
00:00:59.399
state solutions that you can use with
00:01:01.239
them I'm also going to be talking about
00:01:02.519
like when don't you need a global State
00:01:04.519
solution and there are actually cases um
00:01:07.439
but you'll see most of them are
00:01:08.880
influenced by this kind of Redux
00:01:10.680
approach because for something as big
00:01:14.080
and as important as the global state of
00:01:16.680
your app it is really helpful to have
00:01:19.520
that be handled in a very systematic way
00:01:23.280
and specifically in a way that is as
00:01:26.400
easy to debug and reason about and
00:01:29.400
update as a unidirectional Flow by means
00:01:32.799
of for example functional programming I
00:01:35.119
also spoke about custom elements web
00:01:37.680
components and and then kind of also how
00:01:40.360
these use classes in the prototypal
00:01:43.280
chain how this actually gives you the
00:01:45.600
means by means of encapsulation and
00:01:47.719
polymorphism to actually publish generic
00:01:50.799
components and not only publish your own
00:01:53.280
generic components and share them
00:01:55.000
between projects but also giving us the
00:01:58.320
means to actually pull in other people's
00:02:00.479
components so web components is kind of
00:02:02.920
the Native lowlevel version of this
00:02:05.640
there are framework specific ones which
00:02:07.479
will also touch on when we get to
00:02:09.318
Frameworks but the one I highlighted
00:02:11.879
here was kind of shoelace which is one
00:02:13.680
that I really enjoy working with and
00:02:15.640
then lastly we spoke about writing your
00:02:18.959
view in a declarative fashion so there's
00:02:22.080
a range of approaches in terms of how do
00:02:25.720
you convert state to a view and even how
00:02:30.160
do you update the state based on what
00:02:32.640
happened in the view on the one hand we
00:02:34.800
get a completely functional approach
00:02:36.800
through something like Elum which
00:02:38.239
doesn't even allow side effects it's
00:02:40.640
physically not possible to write side
00:02:42.200
effects then we get things like react
00:02:44.440
which is very much on the functional
00:02:46.400
programming side but it's not as strict
00:02:48.640
as something like Elm and then we maybe
00:02:51.120
get something like lit which also
00:02:54.040
similar to react treats your view as the
00:02:57.599
output of actual render function we see
00:03:00.519
this somewhat in other libraries like
00:03:03.280
view as well but view does allow for a
00:03:06.159
bit of two-way data binding and then
00:03:09.080
angular as well which also allows for
00:03:10.840
data binding so data binding being
00:03:13.200
instead of treating your view as actual
00:03:16.200
expression you actually decide what
00:03:20.319
parts of your state correspond with what
00:03:23.799
parts of your and then you only listen
00:03:26.519
for changes in those parts very similar
00:03:29.080
to what we did initially here with all
00:03:31.799
these if statements and so forth but in
00:03:33.760
a much more abstracted Manner and while
00:03:36.599
some of these allow you to do two-way
00:03:38.640
data binding meaning that data can flow
00:03:40.920
in both ways generally it's encouraged
00:03:43.920
that you do one-way data binding meaning
00:03:46.879
that generally it flows from the state
00:03:50.120
to The View and data doesn't directly
00:03:52.680
flow back from the view to the state you
00:03:54.959
don't directly modify the state or
00:03:57.239
mutate the state based on for example
00:04:00.120
inputting something into an input or so
00:04:01.799
forth there's usually a kind of mediated
00:04:05.079
manner in which that is done either
00:04:06.799
through like Redux actions and reduces
00:04:09.159
or so forth you don't full on go state.
00:04:12.200
tasks and you override that or change
00:04:14.720
that or mutate that this is usually
00:04:16.560
abstracted somewhat okay but we will
00:04:19.600
unpack these when we get to Frameworks I
00:04:23.000
think the key is what I'm trying to say
00:04:25.000
here is that we've covered a lot of very
00:04:27.560
broad principles in this module that are
00:04:30.840
realities of modernday development these
00:04:34.520
are considerations in modern day
00:04:37.120
software development when you are
00:04:38.639
working on some type of interface
00:04:40.720
whether that is an actual web page
00:04:43.280
whether it's a web app whether it's a
00:04:45.000
mobile app that you install from an app
00:04:47.280
store or whether it's actual software
00:04:49.160
that you install on your machine you'd
00:04:51.160
actually be surprised how many of these
00:04:52.520
are actually running JavaScript under
00:04:54.400
the hood so what I want to do is I want
00:04:56.039
to tie all those elements together now I
00:04:58.360
want to show you how we can actually use
00:05:01.960
a third party tool to treat our view as
00:05:05.919
a result of a specific function that we
00:05:08.400
run on our state and then very briefly
00:05:10.919
kind of explain what it actually does
00:05:13.639
for us how it actually is able to do
00:05:16.479
that and then lastly I've been talking
00:05:19.360
now a long time about actually saving
00:05:22.759
this to local storage so that when we
00:05:25.080
open the page again our tasks are still
00:05:28.000
there unfor UNT Ely there's a lot of
00:05:30.600
other things we had to chat about before
00:05:32.120
I could actually show you guys how to do
00:05:33.840
that so now I'm going to show you how
00:05:36.240
everything we've covered is going to
00:05:38.000
really help us do that and how that
00:05:40.240
would have been harder if we haven't
00:05:42.639
covered everything we have up until this
00:05:44.600
point and then lastly I just want to
00:05:46.280
chat about some higher order functions
00:05:48.440
what are the built-in higher order
00:05:50.000
functions in JavaScript what are higher
00:05:52.080
order functions and how they fit really
00:05:54.919
nicely in this idea of a declarative UI
00:05:58.199
or declarative View and all the
00:06:00.680
Frameworks to some degree treat how you
00:06:04.120
make changes to HTML or to what a user
00:06:07.479
sees in a declarative way the type of
00:06:10.080
software that we're building in various
00:06:12.360
places but also on the web has gotten
00:06:14.319
increasingly complex when you're
00:06:16.160
building a basic readon website that has
00:06:19.520
just information on it that's like a
00:06:21.199
digital brocher that's not that big of a
00:06:23.960
problem maybe you just want to update a
00:06:25.400
color here with JavaScript maybe you
00:06:27.000
just want to change that little thing
00:06:28.800
when we are building full on stateful
00:06:31.120
apps the general convention across the
00:06:33.680
boorder is some means of the clarity of
00:06:36.360
UI where you just indicate what the view
00:06:39.000
should be without manually doing it
00:06:41.039
yourself is the way to go in terms of
00:06:43.599
keeping your sofware maintainable right
00:06:45.840
so let me first show you the tool that I
00:06:47.880
want to introduce and it is important to
00:06:50.560
note that this is part of lit so
00:06:52.680
obviously if you search for lit you'll
00:06:54.039
get a ton of things um from slang to
00:06:57.360
rock bands to I guess long ice te um but
00:07:01.680
you can just search for live lit Dev or
00:07:04.319
lit JS or whatever and you're going to
00:07:06.759
find this one this is something that is
00:07:08.960
maintained by Google and I think it's
00:07:11.280
important to note that the specific part
00:07:14.120
of lit that I'm going to be touching on
00:07:15.840
now was actually created first and then
00:07:18.599
lit the library or the framework was
00:07:21.960
actually created around that it took
00:07:24.000
that and it actually built an entire
00:07:25.520
framework around it but the specific
00:07:27.560
thing we are interested in is lit HTML
00:07:30.560
so lit being the actual framework and
00:07:33.000
lit HTML being the tool that the
00:07:35.319
framework is built on top that actually
00:07:37.560
preceded the framework so we can go to
00:07:39.840
documentation and then here's a lot of
00:07:41.919
documentation in terms of how to use lit
00:07:44.199
the framework what we want to do is let
00:07:46.680
me just zoom in we want to go down here
00:07:49.199
and then to related libraries and look
00:07:52.520
at Standalone lit Standalone lit HTML
00:07:55.800
this is what we want to use so it does
00:07:57.440
show you how to install standalone lit
00:07:59.800
HTML with npm for the sake of Simplicity
00:08:02.680
we are not going to do that right now I
00:08:04.720
did show you guys how to use node how to
00:08:07.199
use npm but I want to do a much deeper
00:08:10.039
dive into those things before we use
00:08:12.280
them again so we can just use the CDN so
00:08:15.680
what you can search for is just type up
00:08:17.919
here type DN CDN stands for Content
00:08:21.360
delivery Network so effectively what
00:08:23.840
that means is you get a URL where you
00:08:25.599
can pull that JavaScript from and lit
00:08:28.759
Das HTML so we can just then click on
00:08:31.840
this one and you'll see it does take us
00:08:33.360
to an older version of lit so this is
00:08:35.880
lit version one as mentioned all that
00:08:39.479
the current version of lit is it's a
00:08:41.240
fullon framework that was built around
00:08:43.519
this but this is for all intents and
00:08:45.920
purposes the same um but it's if you
00:08:48.040
just want to grab this specific piece so
00:08:50.600
you can go you'll see here is an option
00:08:52.880
to grab it from the URL so you can just
00:08:56.600
go
00:08:57.640
unpkg tocom for / lit HML and module
00:09:01.800
like that so let's just head it directly
00:09:03.519
and see what we get and so you'll see it
00:09:05.800
actually gives us version two um but the
00:09:08.120
new documentation doesn't have a link to
00:09:11.040
this because I guess it assumes you know
00:09:13.880
how to do this yourself if you want to
00:09:15.480
do it this way and obviously you
00:09:16.959
actually don't want to encourage people
00:09:18.160
to do it because there are some
00:09:20.000
performance uh drawbacks but because
00:09:22.399
we're still learning effectively and I
00:09:24.200
don't want you to start using npm full
00:09:27.160
on before I cover it let's just use this
00:09:29.880
version for now but you'll see it is
00:09:32.399
2.73 so it is a pretty recent version
00:09:35.399
and even if we go go on npm you'll see
00:09:38.160
that Lit HTML itself is actually pretty
00:09:40.320
popular it's pretty commonly updated um
00:09:43.800
it was updated 7 days ago and there's
00:09:46.240
more than a million downloads every week
00:09:48.240
all right so we can just use this
00:09:49.440
unpackage link I will actually put it in
00:09:52.240
the re resources as well for you to grab
00:09:55.399
and we want to pull that into our app
00:09:58.040
let us just actually comment out our
00:10:00.640
existing scripts all of this and let's
00:10:03.720
just pull it in here let me just grab
00:10:06.279
that okay Pull It in here and let's just
00:10:09.040
quickly conso log HTML and render and
00:10:11.440
see if it actually pulled it in cool
00:10:13.519
you'll see it actually output it there
00:10:15.360
so let's do a basic example so let us
00:10:18.399
actually let's create a basic div with
00:10:20.600
data app and this is where our app is
00:10:22.959
going to go then let us render our HTML
00:10:26.880
this is an actual mapping of our h HTML
00:10:30.000
so what we do is we use this HTML tag
00:10:33.680
that we get from lit and use back Texs
00:10:36.200
and we pass the HTML in as a string so
00:10:39.920
you need to put HTML first so the
00:10:42.040
function and you pass the template
00:10:43.600
literal into the string I'm not going to
00:10:45.760
go into too much detail in terms of what
00:10:47.639
this actually does um you will actually
00:10:49.920
find this in other places as well like
00:10:52.040
styled components and so forth but let's
00:10:54.360
do Dove 1 2 3 Dove so here we actually
00:10:58.120
let's call it tree so creates an HTML
00:11:00.920
tree for us so you can think about this
00:11:03.000
let's consol log what that looks like
00:11:04.680
it's almost like objects behind the scen
00:11:06.760
so it converts the string for us into an
00:11:10.079
like an actual representation of that
00:11:12.120
HTML in programming you kind of talk
00:11:14.279
about these things as assts and meaning
00:11:16.959
an abstract syntax tree so for example
00:11:20.240
we can think you know if we for example
00:11:21.959
have this and then we have something in
00:11:23.800
there that it creates an abstract tree
00:11:26.200
for us under the hood so then it would
00:11:28.959
be for example you have div you know and
00:11:31.399
inside div there is 1 2 3 and inside
00:11:34.800
that is span and inside that is also one
00:11:38.079
two three so it creates so you can think
00:11:39.920
about these as objects you know almost
00:11:42.079
like the Dom tree itself so it creates
00:11:43.839
an as or abstract syntax tree for us
00:11:46.560
there and this is very similar to to the
00:11:48.760
actual virtual Domin react and we'll
00:11:50.440
talk about that a bit so but let's conso
00:11:52.760
log this and see what it actually looks
00:11:54.279
like so this is also what it will kind
00:11:56.560
of look like usually when you log an
00:11:58.880
acttion
00:12:00.000
react um component as well you know it's
00:12:03.200
just like a lot of internal information
00:12:05.120
you don't need to worry about what it
00:12:06.600
actually does here so what we can do
00:12:09.279
make the a so the the tree that we
00:12:12.160
derive from that a result of the output
00:12:14.959
of a function let's just say create view
00:12:19.040
okay create view takes a name okay and
00:12:22.600
let's just add some J doc string name
00:12:25.440
okay so it takes a string let's just
00:12:27.519
write it like this for readability
00:12:29.720
it Returns the as with the back deex we
00:12:33.360
just interpolate this in here so let's
00:12:34.959
just do and let's say hello your name is
00:12:39.240
okay so let's create that view okay and
00:12:41.760
we pass in sculp so you see now there's
00:12:44.760
a couple of other things it keeps track
00:12:46.360
of these are the static Parts these are
00:12:48.560
the parts of the HML that never change
00:12:51.040
and then in here it keeps track of the
00:12:52.920
skull value once again you don't need to
00:12:55.320
understand what it does internally it
00:12:57.040
does a bit of magic under the hood to be
00:12:59.440
able to actually figure out then if we
00:13:02.160
do a different one so if we do you know
00:13:04.639
example one and example two and this is
00:13:07.560
Mya and let's log both of them and you
00:13:09.880
can see actually it has some internal
00:13:11.920
things so this is the same this is the
00:13:15.160
same but then like the values it
00:13:17.920
actually keeps track of okay what has
00:13:20.480
changed so what is static what never
00:13:22.399
changes and what are the dynamic things
00:13:24.279
that change um and then you'll see it
00:13:26.720
has its own prototypes and stuff but
00:13:29.240
this is just a representation of it then
00:13:31.399
we actually still need then we still
00:13:33.880
need to turn that a into something real
00:13:37.399
and this is where render comes so render
00:13:39.360
is what performs the side effect for us
00:13:42.320
the first thing you do is you say what
00:13:44.920
as do you want to render or what tree
00:13:47.639
you know we can just call this tree one
00:13:49.480
or tree 2 Okay so let's say we want to
00:13:51.440
render that one and we want to render it
00:13:54.800
at query selector and I think we had
00:13:57.399
data app let's check if it work Works
00:13:59.639
awesome hello your name is sculp then
00:14:02.279
let's say we want to replace that so
00:14:04.440
let's do a set timeout so after 3
00:14:06.519
seconds pass it an anonymous function
00:14:08.880
and let's say after 3 seconds so 3,000
00:14:11.320
milliseconds we want to render again and
00:14:13.560
we want to render in that same place
00:14:16.199
tree2 so what it does is it actually
00:14:19.639
take these and it compares the current
00:14:22.560
one that's in there versus the new one
00:14:25.040
and it figures out what needs to change
00:14:27.800
so in that example where we had where we
00:14:29.880
recreate our entire to-do app every time
00:14:33.199
and the only thing that updates is
00:14:35.480
whether something is toggled completed
00:14:37.680
or not in this case it would scan both
00:14:40.240
those trees and it would actually figure
00:14:42.880
out what's the difference and only
00:14:44.800
update that in the HTML so this is not
00:14:48.199
100% what the virtual Dom does um but
00:14:50.920
it's very similar to what the react
00:14:52.560
virtual Dom does I think the react
00:14:54.440
virtual Dom is kind of the first way to
00:14:57.120
figure out how to do this type thing how
00:14:59.880
to give us a declarative UI that can
00:15:02.040
figure out what needs to change and and
00:15:04.680
therefore it's the most straightforward
00:15:06.160
implementation since then people have
00:15:07.959
come up with a lot more complex
00:15:10.040
implementations U but the virtual Dom is
00:15:12.360
usually sometimes people use the term
00:15:14.560
virtual Dom also
00:15:15.959
interchangeably for like what this does
00:15:18.199
this isn't 100% exactly the same as a
00:15:20.320
virtual Dom but generally sometimes
00:15:23.480
people talk about virtual Dom and they
00:15:24.720
effectively mean that you have an in me
00:15:27.320
two things in memory and and those
00:15:29.480
things are compared to figure out what
00:15:30.959
to do you're not actually replacing the
00:15:33.240
Dom itself you're almost keeping an in
00:15:35.240
memory version of the Dom so let's check
00:15:37.480
that out so after 3 seconds it should
00:15:39.680
create the new view for us and there you
00:15:41.160
see 1 2 3 there we go awesome okay and
00:15:45.120
that only changed everything else was
00:15:47.040
kept in place so lit HML is one way to
00:15:49.720
do it it's actually the most like
00:15:51.560
straightforward simplest way to do it
00:15:53.839
which is why was actually initially
00:15:55.560
published as a specific library on its
00:15:58.600
own and then the lit framework was built
00:16:00.759
out around it something similar is um by
00:16:04.160
a guy called Jason Miller not not Jason
00:16:06.560
Miller associated with Trump Jason
00:16:08.759
Miller um so if you're going to search
00:16:10.720
for Jason Miller you're going to find
00:16:12.279
the Trump guy so just search Jason
00:16:15.199
Miller JavaScript so he's a very big
00:16:17.920
name in the world of JavaScript he also
00:16:19.720
built preact and he also created
00:16:22.519
something called HDM uh which is very
00:16:24.759
similar um it's not as popular as uh lit
00:16:29.040
um but it's also it's very similar it
00:16:31.040
kind of takes the exact same approach
00:16:32.920
uses template literals and so forth so
00:16:35.560
so this is an actual virtual Dom
00:16:37.279
implementation of the same thing so it
00:16:38.839
actually allows you to use it with react
00:16:41.120
and so forth this is also very similar
00:16:43.279
to U something called hyperscript and
00:16:46.360
and so forth but we're going to go into
00:16:48.079
detail around these um at a later point
00:16:51.279
so another thing as well this is cool we
00:16:53.120
maybe don't want to pull in something
00:16:55.240
from the internet every single time so
00:16:56.959
let's actually put that in our code base
00:16:59.079
itself uh so generally the convention is
00:17:02.040
to create a folder called Libs so Li IB
00:17:04.679
so for libraries so lit HTML you might
00:17:08.079
see this in some older code bases mostly
00:17:11.240
nowadays npm packages has kind of
00:17:13.599
replaced this um you generally just npm
00:17:16.240
install it instead of doing it this way
00:17:18.359
but this is how we used to do it um so
00:17:21.079
you might see some projects like
00:17:23.559
somewhere out there in the wild that
00:17:25.559
actually have this so just know that is
00:17:27.439
what this is so let's just go directly
00:17:29.880
to that URL cool and here's the code and
00:17:32.919
let's copy all of it and put that in our
00:17:35.640
lit HML file over here one thing you
00:17:38.240
will note is that when I try and save it
00:17:40.600
it tries to format it with prettier um
00:17:43.120
it's intentionally this way um it's just
00:17:45.760
to make the file size smaller but and
00:17:48.559
obviously we are not going to make any
00:17:50.160
direct changes to it so it doesn't need
00:17:51.840
to be readable for us you can leave it
00:17:54.360
so the prettier tries to clean it up I I
00:17:56.880
don't like it when it tries to do that
00:17:59.480
so what I would just do is I just
00:18:02.159
control shift p or it would be command
00:18:04.280
shift p if you're using a Mac and then
00:18:06.679
just say save without formatting cool
00:18:10.559
then it saves the file without
00:18:11.640
formatting it for us and then we can
00:18:13.520
just do this so back back and Libs lit
00:18:16.960
HTML like that all right all right so
00:18:19.679
let us get rid of this custom component
00:18:22.480
abstraction that we created um we are
00:18:24.720
now just going to fool on use uh the so
00:18:28.120
you can get rid of this and we're just
00:18:30.000
going to use a lit HTML so let's import
00:18:34.280
from a Libs lit html. JS so we want to
00:18:38.880
import HTML and render and then we can
00:18:42.280
break those up into components if we
00:18:44.360
want to but what's really nice about
00:18:46.840
this declarative UI approach is we can
00:18:49.000
treat this effectively just as normal
00:18:51.520
functions which is effectively what
00:18:53.400
react does but there's a range this
00:18:55.559
opens up a range of options for us so
00:18:58.039
let's get rid of all of this that we had
00:19:00.120
here and let's start building out a
00:19:02.280
super basic version of our app and then
00:19:04.720
we can connect to the store and so forth
00:19:07.120
let me just get rid of this file and rid
00:19:09.840
of components let's keep our entire app
00:19:11.600
here let's so let's get rid of this as
00:19:13.240
well and let's so let us create a view
00:19:16.720
do a view file a folder let me zoom in
00:19:20.799
and effectively here we can treat our
00:19:22.760
view as actual function so let us have a
00:19:26.000
app.js and effectively this is just
00:19:28.320
going to be the function that's going to
00:19:29.880
render the entire app for us check for
00:19:32.400
updates and so forth um it is
00:19:34.559
straightforward but let's give it a try
00:19:36.760
let's see if it works and we can always
00:19:38.840
Branch it out into different things you
00:19:41.000
might at some point need to split it up
00:19:42.760
into custom web components but for now
00:19:44.919
let's keep it like this let's keep it
00:19:46.320
simple let's keep it straightforward we
00:19:48.159
can always add more complexity as we go
00:19:49.919
let's see how far we get so first thing
00:19:52.320
we need to do is this needs to return an
00:19:56.559
actual lit a so what we then do with it
00:20:01.760
is we can figure out but the View's job
00:20:04.240
itself is just to provide the view as a
00:20:07.080
result of a function so we pass the
00:20:09.320
state to that view and it gives us a
00:20:11.200
function back obviously this is very
00:20:13.080
simplified you'd probably want to do
00:20:14.840
code splitting and and loads of
00:20:16.559
different things which Frameworks
00:20:17.919
actually give us but I'm trying to show
00:20:19.440
the principles here so let's grab that
00:20:21.640
so Libs lit HTML and JS we just want
00:20:26.039
HTML we don't even want render we can
00:20:28.240
handle render in our scripts and then
00:20:30.480
let's just have a con and for now app
00:20:32.720
doesn't take anything it just returns
00:20:35.720
for us HML let's wrap all of this in the
00:20:38.919
div and let's have a header which has
00:20:41.520
inside it an H1 to do app and below that
00:20:47.080
we're going to have a form with an input
00:20:50.360
that is wrapped in a label with a span
00:20:53.640
that says new task and then just a
00:20:56.520
submit button to send it to add the new
00:20:59.280
task we can always but let's get a basic
00:21:02.120
working version for now below that we
00:21:03.919
can have the main and all that we can
00:21:05.840
put in main is the actual items
00:21:08.919
themselves so let's do main UL that is
00:21:12.880
going to have but the first thing you'll
00:21:14.640
see there's no data attributes no
00:21:16.480
nothing we're not pulling anything from
00:21:18.520
the HTML we're actually just returning
00:21:21.480
some HTML as the state of our view but
00:21:25.880
currently there's no changes here
00:21:27.279
there's nothing this is all does okay so
00:21:29.559
we export that in our scripts let's pull
00:21:32.159
that in so the first thing we want to
00:21:33.720
pull in is we want to pull in the thing
00:21:35.720
that creates our view for us and then we
00:21:39.080
want to pull in some listeners for our
00:21:41.279
store and this is where we connect our
00:21:43.320
store to our view and for now let's just
00:21:46.240
say you know get State get the state
00:21:49.000
create a view by passing state to our
00:21:52.039
app and then taking that view and using
00:21:54.679
that ASD from the view to render it
00:21:57.080
somewhere so in our case I think we
00:21:58.880
still have that data app so let's put it
00:22:00.720
in there and we need to pull that in
00:22:03.720
from lit I don't think we have it yet
00:22:06.320
and this is unhappy because oh it
00:22:08.360
doesn't take any arguments yet okay
00:22:10.279
that's fine we can do that in a second
00:22:12.840
and then we check the view and we render
00:22:15.720
it to document query selector and this
00:22:19.440
is the only place where we ever interact
00:22:21.520
with the Dom and as usual I should just
00:22:23.960
remember this hey here we go here's our
00:22:26.559
app that went really fast now I want to
00:22:28.320
show show you a great part and I hope
00:22:30.240
this is going to give you an
00:22:30.960
appreciation for how amazing the Clara
00:22:32.919
of uis are because for a very long time
00:22:35.840
remember this is not the way we used to
00:22:37.760
do it we had to manually go and update
00:22:39.760
things so being able to express
00:22:42.159
something like this F as a function that
00:22:44.760
takes stuff and splits out HTML like is
00:22:47.520
amazing let's say we want to be able to
00:22:49.400
add a task so there we go add task we
00:22:52.000
still need our event listeners and this
00:22:54.320
is where something like uh the fullon
00:22:56.559
lift framework comes in it helps us
00:22:58.159
manage that and so forth but for now
00:23:00.200
we're just going to do it manually here
00:23:01.440
in our scripts so we can just listen on
00:23:03.559
the body remember all events bubble
00:23:06.039
upwards so we can do document body and
00:23:08.440
let's just add event listeners there add
00:23:10.480
event listener and let's just listen for
00:23:12.520
a submit event okay and let's just conso
00:23:14.799
log that event for now okay let's see if
00:23:16.520
it picks it up we don't need to do this
00:23:18.440
but I just say type submit just
00:23:20.760
generally for explicitness behavior is
00:23:23.320
to reload the page so what we need to do
00:23:26.279
here is we need to say first and
00:23:27.640
foremost uh event prevent default and
00:23:30.360
also we are not actually even passing
00:23:31.960
the event through so we will need to so
00:23:35.080
it does register it so what we want to
00:23:36.600
do is let us actually grab that so if
00:23:40.120
you remember one way that we can do it
00:23:42.080
is we can go let's just say data and we
00:23:44.840
go new form data and we pass event
00:23:48.400
Target and then and it's unhappy here so
00:23:51.240
we can just say if event Target is not
00:23:55.240
instance of HML form element
00:23:58.960
so like this then throw an error throw
00:24:01.679
new error all right so now we know that
00:24:04.480
this is a form saying so it says it's
00:24:06.919
not so it's happy and let's just
00:24:09.679
destructure so we need to put a name on
00:24:12.559
that so let's just say the name is title
00:24:14.880
and then we can destructure it so if we
00:24:16.520
go object from entries data then we
00:24:19.880
should be able to grab title from that
00:24:21.720
and let's conso log title that is the
00:24:24.279
case hey check that out okay so what we
00:24:26.760
also want to do is we want to reset this
00:24:29.240
so one thing that Frameworks do is that
00:24:32.120
even allow us to add our event listeners
00:24:34.440
in a declarative manner but for now
00:24:36.520
we're just rendering our HML
00:24:38.760
declaratively without introducing too
00:24:40.880
many new Frameworks and libraries and
00:24:42.840
abstractions to our store we want to
00:24:46.240
dispatch and we want to get a specific
00:24:48.880
action that we want to dispatch I think
00:24:50.760
it was called add task all right so then
00:24:52.600
we want to dispatch add task and add
00:24:55.720
task just takes the title I think maybe
00:24:57.960
like this let me see it's like that
00:25:00.000
title and it is unhappy so what we can
00:25:03.279
do to ensure that it's a string is we
00:25:05.360
can just coers it to a string before we
00:25:07.760
pass it because at this point it's not
00:25:09.600
sure what it is it just knows it's a
00:25:11.919
entry from a fe from a form right so
00:25:15.039
console log title so then we can just do
00:25:17.640
event Target and reset and because it's
00:25:20.720
a form it knows it has reset so now we
00:25:23.399
have this event listener that's updating
00:25:25.120
that but we want to tell our view to
00:25:27.279
render when it gets added let us
00:25:29.679
actually wire this up to our actual
00:25:33.799
let's subscribe this to our actual store
00:25:36.799
so let's just get subscribed we're
00:25:39.320
probably never going to unsubscribe this
00:25:41.080
because this is the main logic that
00:25:42.880
renders our app for us so we just get
00:25:45.360
previous and next we actually don't even
00:25:47.159
need the previous one here CU we just
00:25:49.399
pass the next one to that and so what we
00:25:52.039
can even do here we can say you know Pam
00:25:55.440
we can say return any I'm not going to
00:25:57.840
type up um the actual lead stuff but
00:26:01.360
theam we can say just the state from the
00:26:05.240
store pull that in to get like Auto
00:26:07.919
completion and all that stuff so model
00:26:10.919
store and state there we go now it knows
00:26:15.039
a bit about what that is and it expects
00:26:17.360
actually State here so the first R we
00:26:20.799
can just pass the state directly like
00:26:23.000
that okay I should be happy Okay cool so
00:26:25.600
that is our first very first r
00:26:29.200
if we really want to we can even just
00:26:31.240
throw it like that directly in there and
00:26:33.600
then let's also extract this as the
00:26:35.919
actual um HTML we can reuse it this
00:26:40.000
might be a bit like too hard to read for
00:26:42.360
you so you can always go initial render
00:26:45.360
and then just pass the initial render
00:26:47.559
right so then in the subscription we're
00:26:49.720
not going to use previous uh maybe there
00:26:51.840
are some edge cases where we want to but
00:26:54.080
all that we want to do is we want to
00:26:57.240
just run that again
00:26:58.840
say new render and then just pass it to
00:27:01.399
this with the same HTML with everything
00:27:04.039
and new render and it should also take
00:27:06.440
next and not okay let's give that a try
00:27:08.919
and it is not showing at the moment
00:27:10.760
because we need to in our declarative
00:27:13.440
function we need to actually do
00:27:14.520
something with that so for now let's say
00:27:17.440
tasks and then in Brackets to really
00:27:19.760
show you guys the power of this and
00:27:21.799
without any kind of data um attributes
00:27:24.399
or whatever uh you can just go regular
00:27:27.720
interp
00:27:28.840
let's do and we can even destructure our
00:27:31.159
state up here for each render so
00:27:33.320
remember this is a function that R runs
00:27:35.720
every time a change happens so State and
00:27:39.399
then what we want to do is tasks and
00:27:41.000
let's just see the amount of tasks so we
00:27:42.960
can say tasks length right so if there's
00:27:46.039
no then just zero but one thing you
00:27:48.640
should remember is that tasks by default
00:27:51.919
is actually an object so we need to turn
00:27:54.120
it into an array first so what I usually
00:27:57.320
just do I do tasks as array and I just
00:28:00.399
do object values let's try that okay so
00:28:03.840
zero and hey check it actually every
00:28:06.360
time you add a task it increases okay
00:28:08.559
but it doesn't show those tasks yet and
00:28:10.919
we're not doing any checking we're
00:28:12.919
literally it's updating the parts that
00:28:14.760
it should update it can it goes through
00:28:16.679
all of this and it sees the only thing
00:28:18.679
that changed is this little number so
00:28:20.320
it's not rendering any of this stuff
00:28:22.600
it's just doing that little part