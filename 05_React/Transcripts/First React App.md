00:00:00.000
let's create our first actual virtual
00:00:02.879
Dom let's do that okay and look
00:00:06.060
and literally to write re opponents like
00:00:08.639
this for several reasons for several
00:00:10.679
reasons first and foremost because the
00:00:12.059
first version of react used classes and
00:00:14.580
secondly because it's the way that we
00:00:16.680
differentiate react components from
00:00:18.660
plain HTML so we can create a component
00:00:21.480
called div and the way we differentiate
00:00:23.580
between you know the HTML div and our
00:00:26.400
custom div component is this way so you
00:00:28.680
know I spoke about custom elements and
00:00:30.539
you know the whole thing about dashes
00:00:32.040
and so forth keep in mind like react was
00:00:34.500
created way before all of that so this
00:00:36.960
is the way they solve this problem
00:00:39.000
um it actually fit really well then
00:00:40.800
because these were actually classes and
00:00:43.020
that was the way you would write classes
00:00:44.820
nowadays it is a bit of an awkward
00:00:46.680
approach
00:00:47.760
um but it is what it is you know and in
00:00:49.680
most Frameworks also because they were
00:00:51.360
so heavily influenced by react that's
00:00:53.760
also the way you express any custom
00:00:55.320
elements obviously exception is kind of
00:00:57.420
like lit and and the other ones that are
00:00:59.340
I think angular as well the ones that
00:01:00.960
are very close to actual web components
00:01:03.120
but yeah so let's do app app is
00:01:05.640
effectively just a function and it's a
00:01:07.439
function turns some jsx so and that is
00:01:10.920
just going to create it's going to run
00:01:13.320
create element on each of these in one
00:01:16.080
thing in codepen in order to transform
00:01:18.360
jsx we just need to set this to babble
00:01:21.420
over there so we need to set our
00:01:23.280
JavaScript pre-processor to babble so
00:01:25.619
just click on that little gear here on
00:01:27.360
JavaScript and you go Babble you know
00:01:29.400
allows you to write jsx and so let's
00:01:31.920
just do hello effectively just runs
00:01:34.680
react create element on one level of
00:01:37.619
nesting and it passes to that the name
00:01:41.100
of the actual XML element any attributes
00:01:44.579
So currently there are no attributes so
00:01:46.439
let's just do ID you know one two three
00:01:48.420
then it passes that as an object and
00:01:51.060
then any children and the children is
00:01:53.280
just a regular string like that but that
00:01:55.619
can also be other react create elements
00:01:58.320
and so this is great so we have now used
00:02:01.320
react the core react library to actually
00:02:04.380
create the virtual Dom for us and we can
00:02:06.600
even create another version so we can
00:02:08.459
it's an example and let's say you know
00:02:10.639
example two example one and example two
00:02:13.980
and so we have two virtual Doms here
00:02:16.440
this one is maybe World okay so that's
00:02:18.720
great we can log them let's log them
00:02:21.060
let's see what it looks like so console
00:02:22.620
log uh example one and example two we
00:02:26.400
obviously need to call them you can
00:02:28.080
either go once again you can do create
00:02:30.360
element like that or you can just call
00:02:33.300
it with jsx like this so these are
00:02:36.000
self-closing so you can write it like
00:02:37.920
that but like in reacting actually or
00:02:40.080
XML in general you can do self-closing
00:02:43.319
just like that so you'll see both of
00:02:45.420
these do they exact same thing so they
00:02:47.519
create a virtual Dom for us so here's
00:02:50.220
some lots of stuff props whatever
00:02:51.660
whatever so this is still very similar
00:02:54.599
to what we did with the lit HTML but now
00:02:57.720
we need to also similar to the lit HTML
00:02:59.819
to something like that this is where
00:03:01.440
react render comes in so that's a
00:03:03.420
completely different Library we can use
00:03:05.580
any binding so the react Dom is for the
00:03:08.940
Dom specifically but you know we get
00:03:10.500
react native we get react VR yeah you
00:03:14.280
can use any type of binding that you
00:03:16.319
want so the core react logic this is
00:03:19.080
just the core react logic then we need
00:03:20.819
to bind it with something so what we
00:03:22.620
then do that change the API quite a bit
00:03:25.560
it's it's been it's been a while since I
00:03:28.260
actually used react Dom because as
00:03:30.360
mentioned you know like I'm mostly just
00:03:32.340
use beat and those things nowadays um
00:03:35.879
let me just see the last time I actually
00:03:38.099
had to set up my own react Dom you know
00:03:41.700
that was before you had all these
00:03:43.200
awesome build tools client reactor Dom
00:03:45.420
because you
00:03:46.440
like use react to write server side
00:03:49.500
templating as well uh uh create root yes
00:03:54.000
I think creative root is what we use
00:03:56.400
yeah and then we render on that route
00:03:58.319
the way it works is we need to first and
00:04:01.680
foremost create a route so react Dom
00:04:06.060
preheat root and
00:04:09.019
this is document body okay and then
00:04:12.360
effectively very similar to the lit HTML
00:04:15.659
stuff we do root render and what do we
00:04:18.298
want to render we want to render let's
00:04:19.738
do example one and remember you need to
00:04:21.720
call it to turn it into an actual let's
00:04:24.360
see is that sufficient I might get some
00:04:26.400
errors Roots directly oh it actually
00:04:29.520
tells you uh you shouldn't actually use
00:04:32.340
uh body it's generally considered bad
00:04:34.680
practice first thing here so let's just
00:04:37.620
do document query selector and example
00:04:41.460
is not the point oh it's example one
00:04:42.900
hello all right there we go and let's
00:04:45.240
just do a quick set timeout where after
00:04:47.040
three seconds it replaces it with we go
00:04:50.580
root render so obviously when you're
00:04:52.560
using like wheat and these things all
00:04:53.940
all of this is abstracted away from you
00:04:55.740
but it it's still good to just know it's
00:04:58.800
listening after 30 seconds what these
00:05:00.960
things actually do behind the hood like
00:05:02.639
why actually do you need react Dom and
00:05:05.220
all of that cool their changes right so
00:05:07.740
hello and then after three seconds
00:05:10.199
um okay yes sorry am I the only one who
00:05:12.419
has a frozen screen never mind it caught
00:05:13.979
up now it was stuck on one thing and
00:05:16.080
then mine were inside and off too
00:05:18.800
all right stop your torrents in the
00:05:21.479
background okay there's no 3G there's
00:05:23.100
only five I come now okay and this is
00:05:25.860
once again this is the beauty of react
00:05:28.199
and how small of an API reactors this is
00:05:31.139
now literally all our components are
00:05:33.840
literally just functions that we use jsx
00:05:36.479
to run create element to create a
00:05:39.240
specific virtual Dom object and then
00:05:41.880
these virtual Doms just get compared
00:05:43.979
against one another and that is it like
00:05:45.840
if you understand that that is react and
00:05:48.300
you can build basically anything you
00:05:49.740
want the trick comes like we don't
00:05:52.139
necessarily want to manually listen for
00:05:53.880
changes so we can add event listeners or
00:05:56.759
similar what we did with the HTML
00:05:58.800
element and so forth and this is why we
00:06:00.780
kind of did it in that way
00:06:02.520
um you might feel like yes man like why
00:06:04.680
do we go through all of that nonsense
00:06:06.780
why don't we just dive straight into
00:06:08.220
react because I think this gives you an
00:06:10.259
appreciation for what react actually
00:06:12.720
does and so we obviously don't want to
00:06:16.979
actually set up our own event listeners
00:06:19.080
and whatever and then actually call
00:06:21.720
render manually based and like kind of
00:06:23.940
recreate the virtual Dom and then
00:06:26.039
manually re-render so this is where
00:06:28.020
hooks come in so you can actually use
00:06:30.660
react without hooks completely but then
00:06:33.180
you just need to manage your own events
00:06:34.800
so what Hooks do is hooks allows a
00:06:37.080
declarative way to express interactivity
00:06:39.780
to express events that fire and how
00:06:42.300
those events change actually what gets
00:06:44.699
shown there isn't older API I will maybe
00:06:47.580
touch on it a bit later it's the one
00:06:50.100
that is covered on free code Camp I
00:06:51.900
don't know if the Scrambler content is
00:06:53.639
also gonna cover it but there is an
00:06:55.860
older version before hooks that is built
00:06:58.919
on classes so you still have your
00:07:01.259
functional components like this but if
00:07:03.300
you wanted interactivity you needed to
00:07:05.400
create a class that had something called
00:07:07.979
the set State uh hooks are much nicer to
00:07:10.919
work with so I'm not necessarily going
00:07:12.360
to visit this now but we might touch on
00:07:14.520
it later so how do hooks work I'm not
00:07:17.220
going to go into to 100 what Hooks do
00:07:21.120
underneath the scene but effectively
00:07:24.300
it looks actually pretty straightforward
00:07:26.280
much like everything else in react works
00:07:28.860
are literally just closures so you can
00:07:31.139
think about a hook let's just create our
00:07:32.699
own version of a hook here so let's say
00:07:34.380
const and let's just say use skulk hook
00:07:37.259
whatever and you can actually create
00:07:39.240
your own custom hooks in react okay so
00:07:41.940
when we call use skulk hook there's a
00:07:44.340
value in there and we set a initial
00:07:47.400
value and so whatever we set as an
00:07:49.319
initial value gets set to the value in
00:07:51.120
the closure then we also so we return
00:07:53.460
the value itself and a way to change the
00:07:56.819
value so let's say we have const or set
00:08:00.120
value again all that set value it takes
00:08:02.400
the new value and then it actually just
00:08:05.400
like it just replaces you know new value
00:08:07.860
it actually does lots of other things
00:08:09.720
where it's actually an array actually in
00:08:12.120
the proper way what it actually does is
00:08:13.919
very similar to what we did when we did
00:08:16.440
functional programming where it actually
00:08:18.120
has an array it actually pushes that
00:08:20.220
onto the array and the reason for that
00:08:22.500
is then it can actually compare previous
00:08:24.240
versions of the hook and do
00:08:26.759
optimizations in terms of rendering and
00:08:28.800
so important you can use references and
00:08:30.599
so forth but so effectively new value
00:08:33.299
and you can also then check obviously if
00:08:35.399
you do this whether the new value is
00:08:37.380
different than the current value and
00:08:38.760
only pushed in and so forth but let me
00:08:41.219
just do a very more basic implementation
00:08:43.440
we and then set value and this is the
00:08:46.020
part that
00:08:47.100
that handles by itself and it does this
00:08:49.320
you know like with curry and whatever
00:08:50.760
but let's just actually pass it as you
00:08:53.399
know yeah let's say re-render and all
00:08:55.500
that happens when you set the value
00:08:56.940
re-render just fires obviously you don't
00:08:59.459
do this with with react because react
00:09:01.140
manages the spot for you automatically
00:09:03.120
but we have effectively created our own
00:09:05.940
hook so we can just say you know let's
00:09:07.980
say sculpt value let's say count and set
00:09:10.620
count so you use the structuring and the
00:09:13.860
reason why it does it with arrays
00:09:16.140
instead of as an object because you can
00:09:19.140
call it whatever you want you know it
00:09:21.060
was an object you'd have to go you know
00:09:22.560
value and then change it to count and
00:09:24.600
save value so it's just a quality of
00:09:26.399
life thing so by exporting it as an
00:09:29.160
array of the value and a way to change
00:09:31.380
the value you can call it whatever you
00:09:33.420
want okay it's just easier then we can
00:09:35.700
just say you know use skulker and it
00:09:38.279
starts as one and obviously so react
00:09:40.620
automatically triggers the re-render but
00:09:42.899
you know let's just here's our logic buy
00:09:45.240
it or whatever and so obviously you can
00:09:47.040
and use Talent or whatever but then you
00:09:50.459
know every time you change the count and
00:09:52.680
let's change it to two or whatever then
00:09:55.080
it's going to tell like it's going to
00:09:58.140
change it in the hook so this value is
00:10:00.180
going to update and it's going to tell
00:10:01.740
everything to re-render and this is done
00:10:04.080
on a component basis then we'd use hooks
00:10:06.839
as follows so let's quickly do our
00:10:08.580
counter let me just super quickly do
00:10:10.500
const I'll share this with you guys if
00:10:13.140
you want to check it out in our app
00:10:14.700
let's just return super quickly Dev are
00:10:17.760
usually just write it like that and in
00:10:20.040
that let's do a button that is you know
00:10:22.620
minus let's just do a span that is uh
00:10:26.279
let's just say zero for now another
00:10:28.080
button that is plus uh let's see there
00:10:30.839
we go I hope you guys can see that
00:10:32.580
somewhat I'll when I actually use it
00:10:34.440
I'll use this version obviously this
00:10:36.540
isn't doing much so we can go you know
00:10:39.060
constant count you know say one okay so
00:10:42.540
in with with the jsx you don't do
00:10:46.200
interpolation like that you just do the
00:10:48.360
brackets well that's again the reason
00:10:49.860
being because believe it or not react is
00:10:52.380
so old it actually existed before uh
00:10:56.459
before string templates okay like you
00:10:59.160
didn't have the syntax when react was
00:11:00.540
created and this is also one of the
00:11:02.040
drawbacks of reactants that reacts age
00:11:04.620
sometimes starts showing a bit so they
00:11:06.899
kind of came up with their own way to do
00:11:08.700
interpolation but yeah a lot of weird
00:11:10.500
stuff interact it's just because it
00:11:11.940
didn't exist in JavaScript at the time
00:11:14.100
which is kind of one of the things that
00:11:16.500
spelled maybe for example has a benefit
00:11:19.140
in is that it's kind of a lot newer so
00:11:21.360
it can use existing stuff the problem
00:11:23.040
with react is they can't now go and say
00:11:24.899
no this is actually not how
00:11:26.160
interpolation works because then a crap
00:11:28.680
ton of react projects need to be
00:11:30.779
refactors and refactored and recreated
00:11:32.880
so they'd rather just keep it the way it
00:11:34.620
is even if it doesn't make much sense we
00:11:36.899
can have that in there and it should
00:11:38.820
show up then if you're new to react you
00:11:41.640
might be like okay cool in react you
00:11:44.399
write your events like this so on click
00:11:48.300
in the same way that in some other
00:11:50.700
Frameworks you do on I think it's
00:11:52.860
spelled you do for example on click in
00:11:55.200
lit I think you just do at click and so
00:11:58.320
forth this is just starting with on is a
00:12:01.140
way to indicate that it needs to attach
00:12:03.240
event listener here and this
00:12:05.399
this and an event list now we can and
00:12:06.839
you want you have to use the curly
00:12:08.399
brackets again otherwise it's going to
00:12:10.440
set it as a string yeah like in View and
00:12:12.899
so forth I think it is able to parse the
00:12:15.420
string but in JavaScript I can react
00:12:17.459
because this is all just functions if
00:12:19.380
you write it like that it's going to
00:12:20.399
treat it as a string so there you go so
00:12:22.620
you can even go event counter log the
00:12:24.959
event to show you that this is an actual
00:12:26.820
event listener
00:12:28.380
um and you actually sometimes use the
00:12:30.180
event object in here so let's just see
00:12:32.880
so if I now press that but you'll see it
00:12:36.060
says synthetic event so react has
00:12:38.820
something called synthetic events it
00:12:41.040
just does a bit of like a little small
00:12:44.279
abstraction on top of events to make
00:12:46.079
them a bit more performant to speed up
00:12:48.120
events it allows them to batch them so
00:12:50.639
for example if I like super quickly like
00:12:53.220
click or whatever it's able to batch
00:12:54.959
them together instead of re-rendering
00:12:56.940
all the time like three separate
00:12:59.100
re-renders so this is just it uses
00:13:01.079
something called synthetic events uh
00:13:03.000
count minus count equals minus one and
00:13:06.779
over here count equals plus one it gives
00:13:09.959
it like that so when you click those
00:13:11.399
buttons it changes the count value oops
00:13:13.740
trying to assign to a constant uh save
00:13:16.200
sorry I have a question so flag four
00:13:18.180
like you're doing it like in line like
00:13:20.339
the event listen yeah in a sense so
00:13:22.500
obviously for something small like this
00:13:24.180
where you're just gonna like increment
00:13:25.860
or decrement one you wouldn't do a full
00:13:27.660
out like you wouldn't build out your
00:13:30.180
whole logic if you had something more
00:13:31.320
complicated in that you put it somewhere
00:13:33.180
else or this is just me being lazy I
00:13:35.399
probably do you know just for
00:13:37.079
readability I'd probably do handle
00:13:38.820
increase and const handle yeah increase
00:13:41.120
no 100 100
00:13:44.040
um honestly what I would probably do is
00:13:46.560
well I'll get to that later I'll
00:13:48.360
probably just use a Constructor function
00:13:50.339
that creates decrease in my increase for
00:13:52.800
me but yeah we can get through that
00:13:54.480
later but yeah like you can 100 do I
00:13:56.760
would also recommend you do it this way
00:13:58.079
there's also performance implications
00:13:59.639
it's also a bit slightly more performant
00:14:01.740
to do it in this way I was just thinking
00:14:03.420
if like it's perfect the way you did it
00:14:05.100
if you is doing like an increment or a
00:14:07.260
single decrement but for something a
00:14:09.060
little bit more complicated if you had a
00:14:10.440
bigger 100 if you write if you write uh
00:14:14.100
a very massive yeah like I'm gonna fire
00:14:16.560
you if you give me like this function in
00:14:19.139
line yeah no like definitely like it's
00:14:22.079
it's important to to aim for
00:14:24.420
expressiveness so what I sometimes do as
00:14:27.120
well is I actually write some of my
00:14:30.240
um you know let's say you know modal or
00:14:32.459
whatever actually up here and once again
00:14:34.320
because these are just functions uh you
00:14:36.839
can you know like just assign them to
00:14:38.940
variables so it's effective is just
00:14:40.680
objects that you're passing around and
00:14:42.360
then you know in here I would have you
00:14:44.579
know if uh open then you know modal or
00:14:47.940
whatever this is a lot more expressive
00:14:49.920
than having like all this code you need
00:14:52.139
to scroll generally you want to aim for
00:14:53.760
having a chunk of jsx fit on the screen
00:14:56.399
at once so you can see kind of the
00:14:57.839
entire structure because also what
00:14:59.220
happens if you kind of start having to
00:15:00.839
scroll now you have opening tags that
00:15:03.120
aren't being closed and whatever so
00:15:04.920
generally yeah 100 you want to aim for
00:15:07.079
having your your pieces of jsx as
00:15:09.240
expressive as possible because you can
00:15:11.040
always control click in vs code to go to
00:15:13.440
that function uh or just hover on it
00:15:15.600
okay but yeah so over here now
00:15:17.399
effectively happens here is it does
00:15:19.740
actually increase it so you might think
00:15:21.540
like if we click that it doesn't
00:15:22.680
increase it and let me show you let's
00:15:24.480
create a button that actually shows the
00:15:26.399
value so let's say button all that that
00:15:28.560
does I'm just going to write this on
00:15:29.820
click inside here it's just console logs
00:15:32.639
down for us okay you've got increase and
00:15:35.220
decrease on the
00:15:37.079
um on the jsx the buttons the event
00:15:39.180
handlers are the wrong way around ah so
00:15:41.639
we saw one guy thanks for instance
00:15:44.779
the reason I was like I'm gonna show him
00:15:47.839
Mr react expert
00:15:50.339
um no thanks for that uh oh like I tend
00:15:53.339
to like I think I've mentioned in the
00:15:54.959
videos a couple of times as well like
00:15:56.160
it's it's so hard talking and coding at
00:15:58.560
the same time I can't believe like we I
00:16:01.320
can barely speak about my code still and
00:16:03.540
like you go through it and do it and
00:16:06.000
like present it at the same time like
00:16:07.800
you're on another level my man yes yeah
00:16:10.139
but but that but that comes with
00:16:11.820
experience you know like I don't know
00:16:13.320
how many of you it just comes off your
00:16:14.639
head yeah
00:16:15.800
yeah I don't know how many of you guys
00:16:18.420
have your license but I remember when I
00:16:20.820
learned to drive the first time I was
00:16:22.199
like oh man oh man oh man okay focus now
00:16:25.440
oh now I'm like yeah bro like the other
00:16:28.920
like I just like chatted the guy next to
00:16:30.839
me I'm like damn some tunes and I'm like
00:16:33.720
becomes easier yes yeah no like you just
00:16:36.420
like it almost become subconscious yeah
00:16:38.639
but yeah but like there are some parts
00:16:40.440
where it just makes your amount of
00:16:41.820
Errors like much higher reload so so
00:16:44.399
you'll see actually if I click this it
00:16:45.899
increases because if it says show it's
00:16:47.880
eight Okay Plus versus plus 14 you know
00:16:50.459
minus one so it does update the value so
00:16:52.800
it's not like that it's not updating the
00:16:54.540
value but the trick here is react never
00:16:57.300
knows that it should re-render and so
00:16:59.579
effectively when it re-renders it runs
00:17:01.740
this function again to calculate the new
00:17:03.540
jsx so we can check that by actually
00:17:06.179
putting a console log in here uh
00:17:08.760
rendered so theoretically every time it
00:17:11.220
renders or not renders it evaluates it
00:17:13.439
checks the neojis it creates it because
00:17:15.720
keep in mind react is functional so in
00:17:18.599
other words every time a quote unquote
00:17:20.520
re-render happens it runs the functions
00:17:23.040
again and like then the output of those
00:17:25.380
functions is what it Compares against
00:17:27.359
the previous output of the functions and
00:17:29.520
this is also the magic of react react is
00:17:31.440
one big function it's literally your
00:17:33.540
code is one big function that runs
00:17:35.039
against your state if something changes
00:17:36.740
it just runs that function see what it
00:17:39.360
splits out and it Compares it pumping
00:17:41.039
changes again it runs that big function
00:17:45.140
doesn't that have like performance
00:17:47.220
implications at some point yes 100 like
00:17:49.679
the bigger it gets or yeah yes 100 okay
00:17:52.740
so first
00:17:55.020
first spoke about the Dom I kind of
00:17:57.120
spoke about this a bit when I spoke
00:17:58.860
about prototypes that has big memory
00:18:01.380
implications computationally it's not
00:18:03.900
that intense actually what takes the
00:18:06.840
most resources is the reflowing of the
00:18:09.900
Dom so when something changes now the
00:18:12.960
Dom has to calculate okay it checks like
00:18:15.360
does this thing need to be reset like
00:18:18.000
where everything goes because remember
00:18:19.679
the Dom is like these Tetris blocks so
00:18:21.840
if one thing changes it has to
00:18:23.340
recalculate everything that's actually
00:18:24.900
what takes the most resources
00:18:26.059
comparatively running a function that
00:18:28.320
spits out an object is very minimal
00:18:30.840
remember all you're doing is you're just
00:18:32.580
creating objects so in the scope of that
00:18:34.919
sure yes vanilla JavaScript is always
00:18:37.380
going to be more performant the the
00:18:39.240
difference in terms of performance is
00:18:41.700
not that massive you're literally just
00:18:44.039
creating objects so yeah you'd actually
00:18:46.080
be surprised that this is the trade-off
00:18:47.520
that react does and like with that react
00:18:50.760
made early on as it said like it's much
00:18:53.880
easier to create a version of the Dom in
00:18:57.480
memory every time than to actually
00:18:59.460
update the real Dom and have all that
00:19:01.200
reflowing and whatever happens so it
00:19:03.419
actually makes a trade-off and it says
00:19:04.620
that part is really fast and actually
00:19:06.299
with V8 so what Chrome uses we really
00:19:08.820
saw those computational stuff getting
00:19:10.440
really really fast react also does a bit
00:19:12.660
of clever things you know behind the
00:19:14.700
scenes that sounds way more expensive
00:19:17.460
than it actually is literally this is
00:19:19.740
just spitting out an object it feels
00:19:21.840
very expensive because you see all this
00:19:23.820
crap in here and the other thing is as
00:19:25.559
well is yeah there are cases where that
00:19:28.440
becomes a problem if you have thousands
00:19:30.960
of things being read more often than not
00:19:33.179
that's not a big problem and in fact
00:19:35.580
actually the the the problem is people
00:19:37.980
tend to actually prematurely optimize so
00:19:40.740
there's actually a lot of material that
00:19:43.500
says don't try and prevent things from
00:19:46.440
re-evaluating there are ways in which
00:19:48.480
you can do that but react is really
00:19:51.059
really fast like the chances are that
00:19:53.280
you're gonna make it worse if you try
00:19:54.660
and find with it yourself but you can
00:19:56.760
fiddle with it if you actually want to
00:19:58.980
so let's say you have thousands and
00:20:00.480
thousands of things on the screen at
00:20:02.100
once so this is where use memo comes in
00:20:04.799
I don't know if you guys have heard
00:20:06.299
about use memo or memorization or any of
00:20:08.820
those things when you when you do use
00:20:10.860
memo you effectively tell it when should
00:20:13.500
it reach it if we have so let's say we
00:20:15.900
have app and we have you know for let's
00:20:17.640
say this example example returns level
00:20:20.520
required but obviously let's say it's
00:20:21.780
something super expensive I sometimes do
00:20:23.880
memorization with data visualization and
00:20:26.520
those type of things what you can then
00:20:28.320
do is you can wrap it in a memo I don't
00:20:30.120
know remember the exact context of the
00:20:32.100
exact API so I might be wrong here but
00:20:34.260
I'm just going to show the principle so
00:20:36.240
you do react memo and then you go the
00:20:39.360
component I'm not mistaken you just
00:20:42.480
assign it to a new component so they say
00:20:44.880
memo memo example so memo means
00:20:47.820
memorization in other words memorization
00:20:50.160
is a technique that you actually work
00:20:52.380
really well with functional programming
00:20:53.940
and that is you look at the inputs
00:20:56.400
depending on the inputs if the inputs
00:20:58.980
are the same you can just assume it has
00:21:00.900
the same output adding function and I
00:21:02.880
pass in one and one then I can just look
00:21:04.980
at what happened the last time I passed
00:21:06.900
in one and one just use that without
00:21:08.460
doing the entire calculation again so
00:21:10.260
that's memorization you spell it like
00:21:12.620
memoization I think like that I might be
00:21:15.480
embarrassing myself now and then you can
00:21:17.280
set the condition so you can just say if
00:21:19.919
so it's a predicate so in other words
00:21:22.080
you can just say you know if user is
00:21:24.600
Scott so if that is true I think it's
00:21:27.120
this way around and not the other way
00:21:28.500
around it actually says that but okay
00:21:31.020
this thing shouldn't change the output
00:21:33.120
would remain the same so if you have
00:21:34.860
things that have like like take a lot of
00:21:37.740
time to run that there's like a big list
00:21:39.539
or something you can wrap it in
00:21:41.159
memorization more often than not when
00:21:43.559
people try and do this unless you're
00:21:45.659
doing like really advanced stuff people
00:21:47.460
actually make it worse so I can't see
00:21:49.559
Dodds has a really great article on this
00:21:52.860
memo and there's another one called use
00:21:55.380
callback as well and so he actually
00:21:57.539
talks about this and he actually shows a
00:22:00.179
couple of cases where if you add memo
00:22:02.520
you actually make it worse you make your
00:22:04.260
app slower so unless you actually know
00:22:06.840
what you're doing
00:22:07.919
my classic can't pick Axiom make it work
00:22:10.919
make it right make it fast only if it
00:22:13.380
starts becoming really slow then look at
00:22:15.419
doing some memorization don't fix a
00:22:17.280
problem that you don't have yet but
00:22:19.440
you'd be surprised at how performant
00:22:22.020
react actually is once again something
00:22:23.820
like svelt blows it out of the water
00:22:25.500
what svelt does is so different it does
00:22:28.559
all of this for you in the build process
00:22:30.179
but it does have other trade-offs but
00:22:32.580
generally
00:22:33.860
comparisons JavaScript Frameworks take
00:22:37.320
some of these things that it with a
00:22:38.820
grain of salt not always comparing
00:22:40.799
apples with apples like you can have a
00:22:42.780
look but generally reactors in the is in
00:22:45.659
the fall like the faster side of things
00:22:47.340
so it's cool so then the question is uh
00:22:50.220
how do we tell it to update and this is
00:22:52.440
where hooks come in and it is as simple
00:22:54.480
as the clearing of values like this
00:22:56.640
going constant count so the actual value
00:22:59.520
itself so we restructure it and a way to
00:23:01.559
change the value the convention is to
00:23:03.360
just write it as safe thing so the thing
00:23:05.460
and safe thing that's the convention and
00:23:07.380
we go react and use State and then we
00:23:10.740
set it to what it should start as let's
00:23:12.539
start it as one and then instead of
00:23:15.000
manually setting it like this we just
00:23:17.280
use the function to update it like that
00:23:19.440
and so when we updated with this
00:23:22.200
function it actually tells react to
00:23:24.299
re-render the component I think I have
00:23:27.299
its typo somewhere obviously you you
00:23:29.700
can't actually change this thing itself
00:23:32.039
and so what I'm trying I'm doing here is
00:23:33.840
some so I need to create a new value
00:23:35.760
based over it not assigned back to it so
00:23:38.039
I missed that part where I reassign it
00:23:40.500
you know this is the way react works you
00:23:42.900
can't go like count because of its
00:23:44.880
functional Roots the only way you can
00:23:46.559
update something is through the the set
00:23:49.799
that you get from uh you state and once
00:23:53.100
again what's really nice there is
00:23:54.659
because it's the single pipe that
00:23:56.760
changes can flow through actually react
00:23:59.039
itself actually listens on that pipe and
00:24:00.960
sees when things flow through it so
00:24:02.760
they're like so things aren't mutable by
00:24:05.400
default you can't go and say count is
00:24:07.320
now a you need to actually run a
00:24:09.840
function to update it in the same way we
00:24:12.000
did with our Redux store and all of that
00:24:13.820
so it allows reactors just listen at the
00:24:17.159
single point and anything that goes
00:24:18.659
through it it triggers a re-render which
00:24:20.580
is amazing and there we go of course now
00:24:22.679
every time we actually run that it
00:24:25.200
triggers a re-render it just changes
00:24:27.659
this little number because it creates
00:24:29.100
that virtual Dom object like it checks
00:24:31.260
that the only thing that's different is
00:24:32.820
that little piece of the Dom okay so
00:24:34.799
it's really fast and like this even
00:24:36.900
still works so if you go show it
00:24:38.700
actually says seven as well because the
00:24:40.380
only difference now is we're actually
00:24:41.580
doing it in a way where cells react it
00:24:43.500
fires that rear end as a side effect I'm
00:24:45.539
quickly just going to talk about use
00:24:46.679
effect that the two big ones is use
00:24:48.659
State and use effect and like honestly
00:24:50.520
with those two you can do anything you
00:24:52.679
want
00:24:53.460
um in the next session I'll maybe chat
00:24:55.020
about creating our own custom hooks you
00:24:57.000
can actually create your own custom
00:24:58.380
hooks by composing these things once
00:25:00.659
again you know functional programming
00:25:01.980
compositional functions hooks are just
00:25:04.260
functions and you can compose them
00:25:05.760
there's actually libraries that there's
00:25:08.280
react use that is very similar to low
00:25:10.980
Dash that I covered so low Dash is kind
00:25:13.200
of like all these functional helper
00:25:15.179
functions that you can compose a react
00:25:17.520
use actually is like all these base
00:25:19.980
level hooks that you can compose to
00:25:22.320
create your own custom hooks so this is
00:25:24.419
once again this is where you know if
00:25:25.740
people say that react is more like
00:25:27.900
functional programming and something
00:25:29.820
like angular is more object orientated
00:25:32.640
um this is the part where like the
00:25:34.500
benefits of reacting so functional
00:25:36.240
really shines is that you know we can
00:25:38.520
grab like okay cool we want uh you know
00:25:41.640
use list and we want to combine that
00:25:44.400
with use local storage with a used
00:25:47.100
timeout out so you can compose these
00:25:49.020
things to create more and more complex
00:25:50.700
behavior and these are like very low
00:25:52.799
level things you know so for example
00:25:54.419
here's a here's a hook that checks when
00:25:56.640
a user is idle when their Mouse is not
00:25:58.679
moving
00:25:59.640
um here's a hook that you know tracks
00:26:01.380
when they scroll
00:26:02.640
um here's a hook that allows you to copy
00:26:05.279
something to the clipboard or you know
00:26:07.620
update the title of the page you know
00:26:09.720
here's a hook that runs when a component
00:26:12.000
mounts you know lots of cool stuff what
00:26:14.159
I also wanted to show is to indicate
00:26:16.080
that every time when a re-render gets
00:26:18.779
triggered with you state the function
00:26:20.400
runs again so if we put a console here
00:26:22.559
in our function uh you'll see it on
00:26:24.779
every re-render so every time it
00:26:27.120
effectively runs the function it outputs
00:26:29.100
the virtual Dom once again this might
00:26:31.020
seem like it's really really inefficient
00:26:33.659
but you'd be surprised it's efficient
00:26:36.059
enough it's good enough and that most
00:26:38.159
apps are built with react yeah so you
00:26:39.960
can put anything in there you can even
00:26:41.220
have accounts every time it evaluates
00:26:43.679
keep in mind this I use the term render
00:26:46.200
but it's actually not correct actually
00:26:47.880
evaluate it evaluates because obviously
00:26:50.039
if I click show or whatever that
00:26:52.200
reevaluates but nothing changes so it
00:26:55.260
doesn't touch the Dom because it just
00:26:56.940
confirms that
00:26:58.799
um actually nothing changed but yeah
00:27:00.840
you'll see here so there's literally
00:27:02.340
this function literally runs every
00:27:04.260
single time so what's also really cool
00:27:06.299
about this approach is that you can like
00:27:09.360
just log in your components if something
00:27:11.400
weird is going on just log that value in
00:27:14.220
the component every time the component
00:27:15.779
renders and you can see when that
00:27:17.640
component breaks so let's say there's a
00:27:19.559
problem where if you go like minus
00:27:21.539
something it breaks and you can see okay
00:27:23.220
what was the last what was the value of
00:27:25.740
things in that time that the actual
00:27:27.659
component Ran So this really makes a
00:27:29.700
really nice debugging but so then we can
00:27:32.039
also tell it to just listen for specific
00:27:34.200
things so at the moment it obviously
00:27:36.419
runs that every time the component
00:27:38.640
re-evaluates and we obviously don't want
00:27:40.500
that we only want it if the if the com
00:27:43.080
if the count changes so we can actually
00:27:45.480
tell us to just listen for specific
00:27:47.039
things and this is where use effect
00:27:48.539
comes in so you can say react use effect
00:27:51.240
and then we give it a callback function
00:27:53.159
and let's just say console log count is
00:27:57.960
um and we can say and then we give it an
00:28:00.900
array of things to listen to
00:28:03.179
um so we can just say count all that it
00:28:05.100
does in here it does like and this is
00:28:07.080
where I said that what it actually does
00:28:09.240
it actually keeps an array
00:28:11.640
um of like states of the hooks um
00:28:14.940
because it Compares it against the
00:28:16.740
previous one and it just checks for
00:28:18.179
referential equality so it just checks
00:28:20.460
like is this effectively you know equal
00:28:23.100
to you know the previous count and if
00:28:25.500
it's not then it runs the effect all
00:28:27.539
right so now you'll see that if I now
00:28:30.659
click show
00:28:33.000
oh it's because this itself is logging
00:28:36.500
that's actually what it does so let's
00:28:39.299
just like remove that and make that uh
00:28:41.640
so I can't actually show this right now
00:28:43.740
because we don't have anything else but
00:28:45.179
if we had something else you know like
00:28:46.740
another value or whatever you can only
00:28:48.360
listen you can listen for a specific
00:28:49.860
value uh one thing you can do as well is
00:28:52.620
that if you don't pass anything it just
00:28:54.720
runs when the component mounts so this
00:28:56.820
is useful when you want to fetch data or
00:28:58.919
whatever so for example in that Palm
00:29:01.620
Matrix example I showed um so we're not
00:29:04.320
using use effect here it's a bit more
00:29:06.840
complex but effectively you can have a
00:29:09.240
basic version of the component that
00:29:10.679
mounts and then when it mounts you run
00:29:12.480
an effect that immediately fetches the
00:29:14.159
dot on when the data comes back you've
00:29:15.900
set the state
00:29:17.340
um and so forth but we'll get into those
00:29:19.020
things a lot more in the next session I
00:29:21.120
think we have about eight more minutes
00:29:23.279
um and but this should be enough for you
00:29:25.860
guys to get started on the screen bar
00:29:27.779
stuff
00:29:28.679
um and so in the next session what I
00:29:30.779
want to do is I just want to kind of
00:29:32.940
chat about not um like some of the stuff
00:29:35.700
I mentioned now in react and what are
00:29:39.840
actual similarities in other Frameworks
00:29:42.480
and what are common things you know so
00:29:45.059
here we have you know reactive State and
00:29:47.399
then we obviously have a rendering uh by
00:29:49.559
means of jsx and circle so most
00:29:51.360
Frameworks solve these things in
00:29:53.460
different ways and just kind of planning
00:29:55.260
on that
00:29:56.520
um yeah so we have about seven minutes I
00:29:59.100
just want to check if there are any
00:30:00.840
questions before we head off
00:30:03.000
um in terms of exercises renza I don't
00:30:05.820
know how how did you guys run it
00:30:07.799
previously would you just tell them to
00:30:09.480
look on the LMS or
00:30:11.580
um yeah how would they actually get
00:30:13.020
homework
00:30:14.100
um so what we're going to do is I
00:30:16.860
believe we're going to put the
00:30:18.620
scrimmer content on the lesson plan
00:30:22.399
and that would then also be integrated
00:30:25.500
possibly into into the LMS but also
00:30:28.440
people posted about that yes as as the
00:30:32.460
details are yeah so obviously the the
00:30:35.279
thing is since you guys are the first
00:30:36.899
ones doing this we don't really know
00:30:39.480
like how fast or slow you're going to be
00:30:42.179
able to move through that scrubber
00:30:43.799
content so I don't think we're
00:30:45.960
necessarily going to enforce like okay
00:30:47.760
by next lesson you need to be at this
00:30:50.460
point or whatever
00:30:52.020
um but like what we want is we want
00:30:55.200
everyone to have worked through it by
00:30:57.960
the end
00:30:59.100
um before you actually start building
00:31:00.600
your final Capstone project
00:31:03.120
um so I guess