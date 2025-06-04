00:00:00.000
so now that we've got a lot of that
00:00:01.680
marketing stuff out of the way let us
00:00:03.540
quickly dig into the actual
00:00:05.580
documentation itself and if you've
00:00:07.620
already worked through the documentation
00:00:09.120
there might be some subtle things that
00:00:10.740
you might have missed um I would still
00:00:12.719
actually advise that you kind of pay
00:00:14.460
attention because you might have
00:00:16.079
misunderstood something or there's maybe
00:00:17.640
something subtle that you misunderstood
00:00:19.800
and so forth but yeah the react
00:00:21.960
documentation is really great I advise
00:00:23.699
you guys to work through it so here it
00:00:25.680
just mentions you know apps are made out
00:00:27.300
of components components usually
00:00:30.180
correspond to a piece of the user
00:00:31.980
interface so it usually corresponds to
00:00:34.320
something that gets shown on the screen
00:00:37.040
not like I'd say 99 of the time there
00:00:40.980
are edge cases but generally when you
00:00:43.500
see a react component you can assume
00:00:45.300
it's bound to something that gets shown
00:00:47.160
on the screen if something gets shown on
00:00:49.860
the screen 100 there's a component
00:00:51.660
that's actually rendering it so you can
00:00:54.120
actually install you know react Dev
00:00:56.100
tools to actually it allows you I
00:00:59.280
actually don't use it that much but it
00:01:01.020
does allow you to kind of like see what
00:01:03.120
is the component that renders this thing
00:01:04.860
and whatever so you can install it in
00:01:06.479
your browser and you can see what are
00:01:08.400
the props that get passed through it
00:01:09.840
what Hooks are associated with it and so
00:01:12.180
forth I find it easy enough to just
00:01:14.040
console log stuff in react but you can
00:01:16.860
use the dev tools uh if you want a lot
00:01:19.080
of people do that okay components of
00:01:21.600
this JavaScript functions yep sure yeah
00:01:23.700
in here just says you know like this is
00:01:25.200
a custom component starts with the
00:01:27.119
capital letter the regular HTML must be
00:01:29.640
lowercase if you're not familiar with
00:01:31.439
JavaScript check out mdn or JavaScript
00:01:33.240
info it's optional yeah so jsx is
00:01:36.900
optional although you can't
00:01:38.579
theoretically write without it I don't
00:01:40.140
think anyone is actually because like it
00:01:43.079
just makes it so much easier no one's
00:01:45.000
actually going unless it's for learning
00:01:47.159
purposes but I don't think anyone is
00:01:48.780
actually going recreate element and then
00:01:51.360
you know passing Dev and a class name
00:01:55.680
red and whatever okay but you can do
00:01:59.040
that and this is the point here but I I
00:02:01.500
don't see anyone's doing it because it's
00:02:03.119
just so much easier this but I I did
00:02:06.119
talk about this a bit it's also like jsx
00:02:08.459
because it's based on XML it is a lot
00:02:10.800
stricter than HTML so everything needs
00:02:13.920
to be closed so in JavaScript there are
00:02:15.959
a couple of tags you know for example
00:02:17.580
like input or image it doesn't need to
00:02:20.400
be closed in react you need to go like
00:02:23.580
even something like a br you can also go
00:02:26.099
like you can also close it like this if
00:02:27.840
you really want to but it's easy enough
00:02:29.700
to just make itself closing okay there
00:02:31.860
you go adding Styles okay so class name
00:02:34.020
we spoke about class name the reason why
00:02:36.420
we why the user's class name is because
00:02:38.580
these are properties they're not
00:02:40.319
attributes so this once again react
00:02:42.800
adheres to actually accuracy above
00:02:46.319
developer experience whereas something
00:02:48.480
like view would prioritize developer
00:02:50.700
experience so they might be like okay
00:02:51.900
people are going to get confused if they
00:02:53.459
have the right class name let's just
00:02:55.019
make it closer it looks like HTML the
00:02:57.120
same with like the self-closing and so
00:02:58.860
forth something like view myself say ah
00:03:00.599
you know let's I can make it look as
00:03:01.980
much as HTML as possible with react
00:03:05.099
they're like no this is a property so
00:03:07.319
we're going to give it the property name
00:03:08.760
and also because it's it's actually just
00:03:10.980
functions that run create element
00:03:14.340
um you would actually use it in the same
00:03:15.720
way so you know let's say we have a Dev
00:03:17.760
and we do document uh create element if
00:03:21.360
you actually want to set a class on that
00:03:23.280
you would actually in plain JavaScript
00:03:25.379
go class name is you know red or
00:03:28.319
whatever there is no property called
00:03:30.120
class like that thing doesn't exist it's
00:03:32.700
there's only a class attribute so when
00:03:34.680
you write it like this
00:03:36.420
um and you guys should now honestly
00:03:38.280
already understand the difference
00:03:39.239
between attributes and properties so in
00:03:41.640
react you always write it with a
00:03:43.620
property name yeah so be mindful of that
00:03:45.959
so sometimes out of habit you might
00:03:47.760
write things as actual attributes
00:03:50.099
because you're so used to writing HTML
00:03:52.379
but you actually need to use the
00:03:54.840
property name um I think also if you
00:03:57.239
have a label you can't go for I think
00:03:59.760
you need to go label I think it's HTML
00:04:02.519
or for HTML or something once again you
00:04:05.459
know just because this is the property
00:04:07.080
not the attribute if you're unsure what
00:04:09.180
the difference is between attributes
00:04:12.180
versus properties when I introduce the
00:04:15.120
Dom for the very first time I really go
00:04:17.579
into this in a lot of depth maybe
00:04:19.680
revisit this that will explain why you
00:04:22.320
write it like that then you write your
00:04:23.880
CSS the same exactly when you actually
00:04:26.280
update your CSS you go you know the
00:04:30.139
documents queries no man create element
00:04:33.660
and then if you want to go you can go
00:04:35.880
like Dove style I think it's style
00:04:38.160
background and you set it to red and div
00:04:41.699
style border with 10 pixels again once
00:04:44.940
again this is just plenty JavaScript
00:04:46.380
this is the Dom and for that reason as
00:04:48.780
well in regular HTML you go div and I
00:04:52.080
think you can go style go you know like
00:04:53.940
background red you would actually write
00:04:56.460
it like that okay this is not HTML once
00:04:59.100
again this is not attributes these are
00:05:01.440
prompts meaning that you use an object
00:05:03.540
that corresponds to this because this is
00:05:06.240
in JavaScript give me a moment to write
00:05:08.160
one of the like things that really
00:05:10.380
translate up against the wall is when
00:05:11.820
people say react is gross because you
00:05:14.220
write HTML in your JavaScript you
00:05:16.259
actually don't write HTML in your
00:05:18.180
JavaScript when you're doing view or
00:05:20.040
you're doing spell you are actually
00:05:21.240
writing HTML in your JavaScript in react
00:05:23.639
you don't you're interfacing with the
00:05:25.500
Dom through jsx okay you don't write
00:05:28.560
HTML because if you were to write HTML
00:05:31.259
you would do it like this okay but
00:05:33.060
you're instead doing this but you're
00:05:35.160
writing it this is where the jsx
00:05:37.139
JavaScript syntax extension comes in it
00:05:39.840
extends the JavaScript syntax it just
00:05:41.820
adds extra stuff to JavaScript so you
00:05:44.340
can actually Express functions as XML so
00:05:47.460
that would mean this exact same thing
00:05:49.020
you would go style and that would be an
00:05:51.960
object so you can declare the object you
00:05:54.060
know like out here so let's just say
00:05:55.740
example and in that you would go
00:05:58.740
background red there needs to be a
00:06:01.320
string a lot of times I forget to do
00:06:03.060
this and Border once again it's the Dom
00:06:05.280
so you don't do this you do border with
00:06:07.380
this is what it's called on the Dom and
00:06:10.500
a string and then you pass it to Styles
00:06:14.520
over here so example like that you can
00:06:16.740
do it in line there as well remember the
00:06:19.380
the curly brackets is interpolation so
00:06:22.080
it's the same as you would have here
00:06:24.000
with a string so if you want to do an
00:06:26.160
object in one you need to do two curly
00:06:28.740
brackets one for the interpolation and
00:06:30.600
then for the actual object and then you
00:06:32.580
can do in some templating languages
00:06:34.620
double curly brackets have special
00:06:36.780
meaning and react they don't like it's
00:06:39.240
just one bracket for one curly bracket
00:06:41.880
for the interpolation and another one
00:06:44.160
for the actual object in the
00:06:45.660
interpolation so you can write your CSS
00:06:48.360
as explain CSS files what you might also
00:06:51.180
see a lot is you might see well let's
00:06:53.400
say we have our you know app here return
00:06:56.660
dev123 and then you can import your CSS
00:06:59.580
is so import you know let's just say
00:07:02.699
like app dot CSS or whatever what does
00:07:05.580
this do actually this doesn't do
00:07:07.440
anything with this file unless you you
00:07:10.139
can't do it like this but I'm not
00:07:12.180
necessarily going to cover that but if
00:07:14.039
you just import it like this all you're
00:07:15.840
telling it all you're telling react is
00:07:18.060
that also pull this in there's nothing
00:07:20.220
happening in this file effectively it's
00:07:22.560
just pulling it into when it creates the
00:07:24.960
spits out the CSS so you're just
00:07:27.780
attaching a dependency and the reason
00:07:29.819
why I do this is because if you actually
00:07:32.759
put in your CSS in the HTML so you go
00:07:35.699
for example you know link CSS whatever
00:07:38.039
and you pull in a specific what am I
00:07:40.560
doing I think it's real style sheet okay
00:07:43.139
if you do it in this way you might
00:07:45.180
delete this app component but it's CSS
00:07:47.639
is still there so the only reason I do
00:07:50.039
it this way is that when you delete this
00:07:51.720
file it no longer pulls in the CSS as
00:07:54.240
well so this is just like this isn't
00:07:56.639
even a react specific thing this is a v
00:07:58.860
thing or a neck thing or whatever it's
00:08:01.259
just a way for the bundler for you to
00:08:03.599
express that okay this this is
00:08:05.520
dependency of this component and so if I
00:08:07.979
delete this don't pull that in anymore
00:08:09.900
so that's the only reason why we do this
00:08:12.479
uh theoretically you can pull in
00:08:14.460
anything it doesn't even have to
00:08:16.380
correspond to the component you can even
00:08:18.180
literally just have a file that pulls
00:08:20.280
that in so just be mindful of that it
00:08:22.500
doesn't prescribe how to add your CSS
00:08:24.780
files your headsets you can actually
00:08:26.460
pull it in with a regular link if you
00:08:28.620
use a bold tool or framework consult its
00:08:31.199
documentation so yeah once again this is
00:08:33.899
what most Frameworks actually do some of
00:08:37.080
them actually allow you to use CSS
00:08:40.080
modules and stuff as well it's just
00:08:42.000
important to understand that that is not
00:08:43.799
part of react itself that comes with
00:08:45.779
something like read or next or so forth
00:08:48.060
react has no opinion on how to handle
00:08:50.640
CSS displaying data you guys should know
00:08:53.220
this now already talks about Escape back
00:08:55.560
into JavaScript so interpolate you can
00:08:58.500
escape into JavaScript from jsx so
00:09:00.959
obviously you can do the same with
00:09:02.820
attributes as well so you can put actual
00:09:05.160
things in your inside your component
00:09:07.560
itself but you can also set specific
00:09:09.240
attributes for example class name more
00:09:12.360
complex Expressions so you can put more
00:09:14.519
complex Expressions inside jsx curly
00:09:16.740
brackets to a string concatenation okay
00:09:19.019
so this is an example like cut off here
00:09:21.600
but I think yeah it just goes you know
00:09:23.339
for example you know div and something
00:09:27.060
like you know let's say math random plus
00:09:30.000
100 plus hello or whatever so you can
00:09:32.640
actually run calculations you can do
00:09:34.500
more complex stuff in here and it
00:09:36.720
evaluates this first if you know me I
00:09:39.540
would probably do it this way because I
00:09:42.120
don't like the fact that we're mixing
00:09:44.279
different types here and we're using
00:09:45.480
type coercion so there you go so a lot
00:09:47.760
of times we actually want to calculate
00:09:49.260
something you would do the curly
00:09:51.240
brackets and then you do the back decks
00:09:53.100
and do the interpolation in there
00:09:54.660
because in the back decks this is just
00:09:56.339
plain JavaScript okay this isn't react
00:09:58.680
specific you even put a function in this
00:10:00.899
we can do a function that is calculating
00:10:03.060
and that's just a function that runs and
00:10:04.800
it you know spit something back you
00:10:06.899
can't do this because obviously you
00:10:09.000
can't pause a function to an ID you
00:10:11.820
can't set but it needs to be a string
00:10:13.680
but you can run it in there so it
00:10:15.420
evaluates and then outputs the string
00:10:17.459
there yeah so he had spoke about style
00:10:19.680
and it said it's not a spatial syntax
00:10:21.480
it's effectively you just do the
00:10:22.860
interpolation and then you just put an
00:10:24.300
object in it additional rendering yeah
00:10:26.459
so you can have if statements once again
00:10:28.620
over here it does it in a like very
00:10:31.019
imperative manner this is very hard to
00:10:33.240
read but it's just because it's like
00:10:35.220
introductory obviously it would be much
00:10:37.260
easier if you go content and just use a
00:10:39.600
ternary so logged in admin panel so you
00:10:42.720
can actually use this for actual
00:10:44.700
components use a ternary to figure out
00:10:46.980
what should actually render there and
00:10:48.959
here they actually do it although I'm
00:10:50.760
not a fan of splitting up turneries
00:10:52.380
across multiple lines but like at this
00:10:54.420
point it's just actually differences in
00:10:56.100
JavaScript and how we write JavaScript
00:10:58.500
and not necessary clearly even like a
00:11:01.140
react specific thing you can also use I
00:11:03.899
use this actually quite a bit you can
00:11:05.700
use logical and operators because
00:11:08.160
anything that's falsy would be
00:11:10.440
effectively the same as null so if I do
00:11:12.720
div and I put anything in there that is
00:11:15.240
falsy so it's obviously false empty
00:11:17.820
array or whatever like that would not
00:11:19.920
render anything it would be the like as
00:11:22.019
if there's nothing there so what you can
00:11:23.880
do is you can actually do the following
00:11:26.279
you can go you know like value and one
00:11:28.560
and then you can say you know like if
00:11:30.480
there is a value then rendered with the
00:11:33.360
value in it or whatever very common use
00:11:35.820
cases you have like a image you know and
00:11:38.579
whatever the URL for the images and then
00:11:41.160
you check if the as a URL do image
00:11:44.120
source URL otherwise just leave it don't
00:11:47.399
don't do anything there so this is
00:11:49.500
really cool because the problem is if
00:11:51.720
you just do that and this is null or
00:11:54.240
whatever it's going to rain in an image
00:11:55.740
with the invalid URL so you actually do
00:11:57.959
this a ton or even turn over to say user
00:12:01.140
you know if user null so then you have
00:12:03.240
for example button in there you actually
00:12:05.339
resolve the ternary so you say you know
00:12:07.740
if there's a user then the button should
00:12:09.779
be you know sign out otherwise it would
00:12:12.660
be you know login so you do this type of
00:12:14.640
thing a ton uh in react and that this is
00:12:17.399
just plain JavaScript so here just says
00:12:19.260
you know if you're unfamiliar with these
00:12:20.760
luckily we've done a lot of JavaScript
00:12:22.320
up until now so you should be familiar
00:12:24.300
with these you can do if else this reads
00:12:27.240
very not great compared to something
00:12:30.300
like this rendering lists Okay cool so
00:12:32.760
here I think we spoke about this last
00:12:34.440
time as well you can have an array that
00:12:36.959
you map over to turn into jsx so a good
00:12:40.140
example here would be you know so they
00:12:41.760
have list items which is an Li and
00:12:43.920
you'll see here they have the key that
00:12:45.720
we spoke about and so they kind of use a
00:12:48.180
map and they create a new array with map
00:12:50.399
so they take products and they you know
00:12:52.740
convert it into a new array of jsx and
00:12:56.760
then they just pass that jsx in here you
00:13:00.120
know here talks about the key attribute
00:13:01.800
Keys Can Only Be Strings or numbers
00:13:04.079
technically only strings but it does
00:13:06.600
coerce it pass for example if you pass a
00:13:09.720
hundred it just occurs as a draw you
00:13:12.120
into a string automatically it can be uh
00:13:15.959
strings or numbers and this is used to
00:13:18.600
uniquely identify something
00:13:21.120
um I spoke to the reason why you need
00:13:23.399
keys in the last video that we did you
00:13:25.740
can recap there if you if you don't
00:13:28.019
understand why you need to add Keys when
00:13:31.380
you're mapping over things or even if
00:13:33.720
you still don't understand just remember
00:13:35.339
that whenever you use map whenever
00:13:37.800
you're dynamically creating a list of
00:13:39.839
jsx you need to assign keys for react to
00:13:43.440
be able to figure out what changed is
00:13:46.260
this the same thing that moved up is
00:13:48.120
this the same thing and it doesn't
00:13:49.200
recreate it each time from scratch and
00:13:52.320
this here just shows like functions and
00:13:53.940
you can pass functions to event
00:13:57.060
listeners so these all correspond to
00:13:58.980
actually listeners so if you were would
00:14:01.740
to go you know document create element
00:14:04.920
uh Dev and you say add event listener
00:14:08.279
whatever you would put there as a string
00:14:11.040
you would just say on if you have like
00:14:13.200
you know click uh or whatever so you
00:14:15.300
have you know on click uh on change on
00:14:18.839
scroll on focus on blur anything that is
00:14:23.880
an event listener you can just prefix it
00:14:26.100
on all JavaScript event listeners touch
00:14:29.639
move touch end scroll blur click copy
00:14:33.240
cut all of these you would do like on
00:14:35.880
focus on key up on Mouse leave on
00:14:39.120
pointer up and so forth that is how you
00:14:41.399
do event listeners and you just prefix
00:14:43.440
it with on and obviously it's camel case
00:14:45.660
you just prefix it with on to indicate
00:14:48.180
that it is an event listener if you
00:14:50.519
don't if you for example go button click
00:14:53.339
then it's just going to pass that
00:14:55.380
function as a prop that's how you do
00:14:58.139
event listeners and it talks about event
00:15:00.420
handlers you should be familiar now with
00:15:02.519
this term of Handler functions okay we
00:15:04.980
covered this at the very beginning and
00:15:07.139
also common common mistake this is
00:15:10.199
who does which I think it shouldn't do I
00:15:12.420
think this is I don't know maybe it's
00:15:14.160
just like the purest in me that's like
00:15:16.019
this is bad you shouldn't do this but if
00:15:18.720
you like decided that enough people do
00:15:21.300
this by accident with it and
00:15:22.740
accidentally call the function in there
00:15:24.899
instead of just passing the function if
00:15:27.660
you're doing this it's gonna actually
00:15:29.459
pretend like you actually just passed it
00:15:31.800
I I don't like this but uh react it's
00:15:35.459
going to be like hey you said you wanted
00:15:37.139
to call it you didn't say you passed it
00:15:39.180
so we're going to call it then it's
00:15:41.040
going to assume that whatever handle
00:15:43.740
click returns it's going to put in there
00:15:45.779
because you're actually calling it so
00:15:47.699
just be mindful of this you know be
00:15:49.320
mindful of accidentally calling it
00:15:50.880
actually just passing you can also do
00:15:53.760
Anonymous functions in here when you are
00:15:56.760
for example mapping over something or
00:15:58.560
whatever so or you do an event listener
00:16:01.139
so you do you know document ad event
00:16:04.260
listener so when you are just creating
00:16:06.360
the function in there you call it an
00:16:08.880
anonymous function because as it doesn't
00:16:10.800
have a name theoretically you can look
00:16:12.839
at the name of a function so you can go
00:16:14.639
for example you know tests to say
00:16:16.860
console log or whatever obviously
00:16:18.420
there's no reason why you would want to
00:16:19.800
do this but you can actually go test
00:16:21.420
name and that is going to be test it's
00:16:23.760
going to be the name of the of the
00:16:25.620
function that you assigned Anonymous
00:16:27.600
functions obviously don't have names
00:16:29.100
because you don't assign them to a
00:16:31.019
variable you actually declare them
00:16:32.579
directly where you pass them you can do
00:16:35.579
Anonymous functions as well and this is
00:16:38.279
a JavaScript principle this isn't a
00:16:40.380
react principle so you can go button
00:16:43.139
click create the function in the console
00:16:45.660
log for very basic stuff you tend to
00:16:48.300
actually just do this it's created in
00:16:50.459
there instead of creating it up here and
00:16:52.199
then passing it you know you can even do
00:16:54.720
like partial application example because
00:16:57.060
this is all just plain JavaScript create
00:16:59.160
click open or whatever and this is a
00:17:02.639
function that returns a function so you
00:17:04.319
pass the ID which is a string part it
00:17:07.679
creates a new callback function it's
00:17:09.839
just stay safe open so let's just say we
00:17:13.199
have open and then we have set open this
00:17:16.199
is just a use State and nothing is safe
00:17:19.079
as open at the moment in here so you're
00:17:21.359
wrapping this in two levels of functions
00:17:23.939
and now we're getting into carrying and
00:17:25.559
all of that stuff so this is where these
00:17:27.599
type of things get really useful then
00:17:29.880
you can just do this that is really cool
00:17:32.400
in terms of you don't need to clear it
00:17:33.900
create all these Anonymous functions so
00:17:36.000
let's say you have a list of one two
00:17:38.220
three four five six seven and so you're
00:17:40.860
mapping over that you know from that you
00:17:43.260
just extract the ID turn some jsx so Li
00:17:47.179
with the button inside it click me or
00:17:50.520
whatever so what you would generally do
00:17:52.919
and I a lot of times do this just
00:17:54.539
because I'm lazy is you can do on click
00:17:57.480
and then just create an anonymous
00:17:59.160
function in there that is you know set
00:18:01.440
open and the ID itself but you can
00:18:04.500
actually use coloring to make that a bit
00:18:06.840
more expressive so you can go because we
00:18:09.360
have this function that Returns the
00:18:11.400
Handler for us and we can just say on
00:18:13.200
click you know create click open and
00:18:15.299
just pass pass it in there so we call a
00:18:17.580
function that returns a function and
00:18:19.440
that function that gets returned then
00:18:21.480
actually gets passed to the on click and
00:18:23.640
also like what's really cool is now if
00:18:25.140
you decide hey we want to add a side
00:18:26.580
effect we can just do console log you
00:18:28.679
know in here and so forth so you can
00:18:30.480
create a factory that creates your
00:18:31.980
Handler for you which is really cool and
00:18:33.720
what's also cool about this is now you
00:18:35.160
actually just have less logic happening
00:18:36.960
in your rendering this is also very nice
00:18:39.120
I'm not going to go into it now I'm not
00:18:40.919
going to show use callback and that
00:18:42.480
stuff but if you want to optimize this
00:18:43.919
for performance as well you can actually
00:18:45.780
just go you know use callback to
00:18:48.960
actually memorize it and so forth but
00:18:50.760
I'm not going to go into that but just
00:18:52.200
know like this is also really cool for
00:18:53.760
performance optimizations so here just
00:18:55.740
talks about State and state is
00:18:57.240
effectively what tells it to re-render
00:18:59.580
so you have your value from your state
00:19:01.740
and then a way to change the value so it
00:19:04.200
says you get two things from you state
00:19:06.299
you get the actual count itself and then
00:19:08.760
a way to update account okay so it just
00:19:12.299
gives an array of two items the first
00:19:14.400
one being the value the second one being
00:19:15.840
a way to change that value and when you
00:19:17.880
call set something it causes the
00:19:19.679
component to re-render like it just
00:19:21.660
causes the component that it's in to
00:19:23.280
re-render so if I for example have div
00:19:26.520
and in my div I have button one two
00:19:29.760
three and I have other thing or whatever
00:19:32.340
let's say other and inside button I have
00:19:36.240
a use state that let's just say button
00:19:38.760
values set value thoughts as you state
00:19:41.280
starts you know click me turns you know
00:19:44.400
this button with the value inside what
00:19:47.280
I'm going to do now is I'm just going to
00:19:48.960
say on click it's just an anonymous
00:19:51.179
function and that returns set value to I
00:19:55.919
was click so when you click then on this
00:19:58.620
it's going to update this component so
00:20:01.080
this is where hooks are really cool
00:20:02.580
react is smart enough to know because of
00:20:05.280
one way data binding because data can
00:20:08.039
only flow in One Direction only the a
00:20:10.440
hook inside this button actually
00:20:12.480
triggered it's not able to actually
00:20:15.360
influence anything outside it so it
00:20:18.120
actually just reevaluates this and
00:20:20.700
leaves everything intact so this is
00:20:22.500
really great in terms of performance
00:20:24.000
which is why you you always have this
00:20:26.580
tension between localizing data and
00:20:30.000
global data that you so you don't want
00:20:32.340
to necessarily put all your data at the
00:20:34.320
top of the app because then if anything
00:20:35.880
changes a waterfall of everything needs
00:20:39.299
to re-render you localize it it's smart
00:20:41.640
enough to know that only the scope that
00:20:43.799
you put that hook in needs to reevaluate
00:20:46.980
and so yeah here just shows an example
00:20:48.600
of how you can do a handle click and
00:20:51.000
then you know set count call the
00:20:52.679
component function so it'll change the
00:20:54.840
count to one and then when you call it
00:20:56.340
again it'll change it to two and so
00:20:58.080
forth if you render the same component
00:21:00.480
multiple times each will have its own
00:21:02.520
State okay so here it shows an example
00:21:05.100
of where you actually use this component
00:21:07.140
multiple times and because it only has
00:21:09.419
that actual state in there when this one
00:21:12.419
changes so if you click this this is
00:21:13.980
going to change to one it's going to
00:21:15.240
change to two it's going to change to
00:21:16.980
three and this the hook is only it only
00:21:19.020
fires the hook in that little
00:21:20.640
encapsulated place this thing is never
00:21:23.160
gonna like it's never gonna check
00:21:24.780
whether this should update so
00:21:26.340
performance wise it only updates the
00:21:28.860
scope where the the hook is it actually
00:21:31.620
or not upload to the revalue it's only
00:21:33.419
that scope so this is really cool so you
00:21:35.460
might be wondering okay why don't we
00:21:36.780
just use like Redux for everything or
00:21:39.720
does this stand for everything and the
00:21:41.640
reason is because if you have everything
00:21:43.740
in global State everything is going to
00:21:45.780
re-render all the time or it's going to
00:21:47.640
revalue it because it doesn't know how
00:21:49.620
things are scoped because it is globally
00:21:51.720
available but because you're doing it
00:21:54.000
your your use state in the component
00:21:55.980
itself it knows that okay it can only
00:21:58.380
influence this component so it only
00:22:00.179
checks us okay a functions starting with
00:22:02.940
the use okay so hooks hooks always need
00:22:05.460
to start a fuse so this includes the
00:22:07.679
bolt-in hooks that you get with react so
00:22:09.720
the ball and hooks or any hooks that you
00:22:12.419
create yourself always needs to start
00:22:14.460
with use this is how you tell react Hey
00:22:17.280
listen to what this thing returns okay
00:22:19.320
so they just have a link here to the API
00:22:21.120
we can look at all the hooks you can
00:22:22.980
also write your own hooks which I showed
00:22:24.780
last time hooks are more restrictive
00:22:26.880
than functions so there's a couple of
00:22:28.559
rules around hooks by default wheat
00:22:31.380
installs the react hooks eslint plugin
00:22:34.679
that gives tells you when you're
00:22:36.539
breaking the rules around hooks if
00:22:38.760
you're not using Veet or you don't get
00:22:41.580
that by default ensure that you have the
00:22:43.740
hooks react hooks eslint plugin yeah
00:22:46.679
otherwise you're going to cause yourself
00:22:47.820
a lot of pain if you accidentally Break
00:22:50.220
The Rules around Hooks and you don't
00:22:52.020
even realize it so you can only call
00:22:54.120
hooks at the top of your component one
00:22:56.580
very important thing about hooks is you
00:22:58.440
can't do hooks can't be conditional so I
00:23:00.840
can't go cons button have if statements
00:23:03.659
uh above it so I can't go you know like
00:23:05.940
if math but random is bigger than it
00:23:09.059
says 0.5 I've turned Bev one one one one
00:23:12.600
one otherwise return Dev and then have a
00:23:17.700
hook you know so const you know value
00:23:19.980
and set value down here hooks need to
00:23:23.400
run every single time books need to
00:23:26.400
evaluate every single time the component
00:23:28.860
renders or evaluates you can't have
00:23:32.280
conditional logic where the hook
00:23:34.200
sometimes doesn't evaluate so hooks
00:23:36.720
generally always almost always go at the
00:23:39.600
top of your component it's going to give
00:23:41.340
you an error if you have any actual
00:23:43.260
logic that can cause the hook to not run
00:23:46.620
when a component updates the only thing
00:23:48.960
I use sometimes but usually put above
00:23:51.480
works is if I'm just destructuring my
00:23:53.400
props everything else comes after hooks
00:23:56.280
as far as possible hooks should always
00:23:58.679
run when creating a new virtual Dom okay
00:24:01.980
this is just one of the rules around
00:24:03.419
Hooks and so here we get to lifting the
00:24:05.940
state so we spoke a bit about lifting
00:24:07.740
the state effectively what we have here
00:24:10.020
is we have our click in here and we have
00:24:13.020
in two different versions of State here
00:24:15.120
we want to access both of them at the
00:24:17.700
same time
00:24:18.720
um and so here it says you know we click
00:24:20.280
one but this one's still a zero because
00:24:22.380
it's these are two separate pieces of
00:24:24.120
state but let's say we want any click to
00:24:26.880
update the count across the board so
00:24:28.980
then we need to lift the state up here
00:24:31.200
and pass it down to the components
00:24:33.960
usually you lift the state when you
00:24:36.059
share data between components components
00:24:38.820
can't talk to one another components
00:24:41.220
also can't go through that once again
00:24:44.580
you know unidirectional data flow data
00:24:47.280
can only flow down the data can't flow
00:24:49.740
up like this it can't flow sideways it
00:24:52.140
can only flow down to children so this
00:24:54.600
is why you lift the state okay this
00:24:56.520
lifting the state thing is very
00:24:58.260
important it is key react principle if
00:25:01.200
you don't understand this concept of
00:25:02.940
lifting the state then like watch a
00:25:05.280
couple of YouTube videos try and get
00:25:07.200
your head around it it's very very very
00:25:09.419
important and so here's an example where
00:25:11.460
they lifted the state so the state lives
00:25:13.500
here and then it just gets passed down
00:25:15.960
um how do you then trigger events from
00:25:19.200
children that should happen in a lifted
00:25:21.840
State because obviously the state is no
00:25:23.520
longer in the count itself so how do you
00:25:25.799
trigger it if the state is then the
00:25:27.600
parent hint remember functions remember
00:25:30.480
the difference between composite types
00:25:32.760
and actual primitive types which means
00:25:35.340
that the function still lives in here
00:25:38.400
you're not actually like but you're
00:25:40.500
passing a reference to that function
00:25:43.200
down to the children you're not passing
00:25:45.539
the function itself down so it's not
00:25:47.580
like you're passing the function and you
00:25:49.140
call the function here and then it like
00:25:51.419
does something above it the function
00:25:53.159
never moves the function always stays in
00:25:55.679
the lifted State all you're doing is
00:25:57.539
you're passing a reference down to that
00:26:00.000
function and you're passing a reference
00:26:01.620
down you're not passing the same
00:26:03.120
function to two different places you're
00:26:05.279
just passing a reference to that
00:26:07.080
function around and it's the same it's
00:26:08.940
the same principle by which like the
00:26:10.559
global store and those type of things
00:26:12.360
work and then you can call that
00:26:14.460
reference here and it fires the function
00:26:16.799
where it lives up here this is generally
00:26:19.380
the first stumbling block for people and
00:26:21.480
we actually get their heads around this
00:26:23.100
is kind of a bit of a mind Bender but
00:26:25.020
like give it time except that they're
00:26:27.059
trying to understand it this is such an
00:26:29.159
elegant approach like and I think it
00:26:31.140
speaks to just how good of an API react
00:26:33.659
is so the state that was so we had these
00:26:36.360
use States in here then it tells us like
00:26:38.640
okay put the use State put our state in
00:26:40.860
the in the top one so here it just shows
00:26:42.720
us how to do that pause information to
00:26:44.820
my button using jsx and so forth and so
00:26:47.700
here we actually two our buttons or
00:26:49.740
buttons don't have any state in them
00:26:51.720
anymore we pass the value down as props
00:26:55.080
into the buttons and then we also pass a
00:26:59.039
reference I'm going to actually indicate
00:27:00.840
this looks like a dotted line we're not
00:27:03.120
passing the function down we're passing
00:27:04.799
a reference in the same way that
00:27:07.020
remember you know like if you have an
00:27:08.640
object so test and we have hello and
00:27:12.299
World in there like we can do console
00:27:14.880
log test equals hello world we covered
00:27:18.900
this in some of the very early
00:27:20.460
fundamental videos composite types are
00:27:23.760
references this is going to be false
00:27:26.520
because they have the same shape they
00:27:29.220
have the same properties and values but
00:27:30.720
they're not the same thing this is a
00:27:33.000
reference to test and in the same way
00:27:35.520
that if we go const yo yo repos test in
00:27:39.480
there and then we go const ah where and
00:27:42.900
we passed yo-yo in there then if we go
00:27:45.059
away away hello equals five and we
00:27:49.200
cancel log test what is this going to be
00:27:51.480
this is going to be hello five but we
00:27:54.360
never ever update a test and so this is
00:27:56.880
It's because we're passing references
00:27:58.799
around and for that reason test is going
00:28:01.200
to be equal to yoyo as well because they
00:28:03.840
refer to the same thing if you don't
00:28:06.299
understand this please please please
00:28:09.059
please please go back to that video back
00:28:11.820
to that lesson where I talk about
00:28:13.320
Primitives and Composites if you don't
00:28:15.600
understand this
00:28:17.400
can this
00:28:18.779
destroy you and
00:28:20.940
it's such a pain it is gonna be such a
00:28:23.400
frustrating experience
00:28:24.960
um I just have one question so the state
00:28:26.940
is passed around in the parent
00:28:28.380
components here from the parent
00:28:30.000
component and in the child component is
00:28:32.279
just a reference basically the the child
00:28:34.740
component accepts a property okay and a
00:28:37.020
property can be anything it can be one
00:28:38.460
it can be five it can be null true but
00:28:41.940
what you're passing is you're passing a
00:28:43.500
reference to a function in other words
00:28:45.659
you know it's effectively you can think
00:28:48.179
about it as a road sign that just says
00:28:49.980
you know oh this this value points to
00:28:52.200
this thing over here and then when you
00:28:54.299
call that reference it's like okay cool
00:28:55.799
I know it then follows that reference
00:28:57.900
and it calls it from The Source uh which
00:29:00.360
would be the parent component so the
00:29:01.799
function itself never moves down it
00:29:03.900
makes sense now like it's it's as if the
00:29:06.299
child components is basically just a
00:29:08.400
property the parent component
00:29:09.900
understands it yeah okay yeah yes so let
00:29:12.480
me let me quickly like just like really
00:29:15.059
cement this let me just super quickly do
00:29:16.980
you know let's say example in example
00:29:19.260
const and let's just say once again you
00:29:21.899
know value well let's just say skull you
00:29:23.880
know I I prefer to call it wacky things
00:29:26.039
so you guys don't get fixated on change
00:29:29.159
sculpt or whatever you can call these
00:29:30.899
things whatever you want okay don't get
00:29:33.299
fixated on value or use value or set
00:29:35.520
value or whatever so then you say use
00:29:37.740
State and skulk starts as hello then we
00:29:41.039
have another component and I'll just
00:29:43.260
declare it up here inner and you know it
00:29:45.840
takes a couple of props it takes color
00:29:47.640
it takes a name you don't even need to
00:29:50.580
call this on oh let's just say do things
00:29:52.620
so so it returns let's actually say Dev
00:29:57.000
and in that let's just say if there is a
00:29:59.399
color and and do an H1 with the name of
00:30:02.279
the color let's show you know name down
00:30:05.159
here and then there's a button that and
00:30:07.260
we can also say if do thing if a
00:30:09.419
reference is paused do thing render the
00:30:11.940
button only if if it has a do thing and
00:30:14.220
we can also like say you know if do
00:30:16.740
thing is post and then just say I can
00:30:19.679
change in the actual title itself so you
00:30:22.020
can also like do other derive other
00:30:24.360
things from like this property that you
00:30:26.700
pass so inner and this inner only has a
00:30:29.940
name ah this one has a name and a color
00:30:32.820
we can even further modify that so let's
00:30:35.279
say when you do on click we do do things
00:30:38.520
and we actually pass the the color back
00:30:41.399
you know whatever we pass in on click
00:30:43.620
and so you can pause different things
00:30:45.000
and you know this is where we get to the
00:30:47.279
scary word polymorphism it's really so
00:30:50.340
simple you can follow this documentation
00:30:51.960
and be like cool cool but when you
00:30:54.120
really get into it when you really get
00:30:55.620
into what you can actually do like when
00:30:58.740
you get into the complexity of what this
00:31:00.899
allows you to do it's only then when you
00:31:03.240
realize how powerful react is and when
00:31:05.700
you realize wow this is why react is so
00:31:08.100
popular it's not just a randomly like oh
00:31:10.620
people just like react more than view or
00:31:13.140
whatever like react allows you to do
00:31:15.299
super powerful things because it's built
00:31:17.279
on these principles of things like
00:31:18.720
encapsulation polymorphism and so forth
00:31:20.580
so by the definition of polymorphism we
00:31:22.860
just declare a shape for this thing and
00:31:24.539
we effectively says it needs to be a
00:31:25.799
function it can be any function so if we
00:31:28.020
pass you know name here and do things
00:31:30.720
and over here we can just pass a
00:31:32.279
function and we can just say result so
00:31:34.919
whatever this thing returns just console
00:31:37.080
log that this is completely removed from
00:31:39.179
from this like it doesn't even it
00:31:41.039
doesn't even know it just knows do thing
00:31:43.380
as a function and it needs to call do
00:31:45.240
thing when you click the button it
00:31:46.679
doesn't even know what two thing is
00:31:48.059
we're just creating a contract fact that
00:31:50.100
we're saying this is the interface and
00:31:52.320
this just accepts a function but
00:31:54.059
essentially that is an interface here
00:31:55.679
yeah 100 and this is the thing about
00:31:57.360
functions and this is why I I kind of
00:31:59.760
covered this idea of fact
00:32:01.440
because components in react are wait for
00:32:04.140
it Factory functions and this is also
00:32:06.179
why you probably realize like hey this
00:32:09.000
is why a guy that likes Factory function
00:32:11.220
so much actually likes react so much is
00:32:13.260
because this it's factory functions
00:32:14.700
that's what it is you can even do jazz
00:32:16.500
dot let's do type diff uh object and
00:32:19.380
let's just say inner okay let's write it
00:32:21.720
out so let's go string color but it's
00:32:24.360
also so not required it's optional prop
00:32:27.659
name which is also a string but it is
00:32:30.240
required and then prop callback up here
00:32:33.240
so pull back and do things param Ram is
00:32:39.140
string and it's color and it doesn't
00:32:42.600
return anything pause do thing Ram uh
00:32:47.600
cool and now we have type safety on our
00:32:50.100
components but it's also really cool is
00:32:52.320
that you get tools that are able to
00:32:54.600
extract this and create documentation
00:32:57.659
for you automatically based on this
00:32:59.279
check this out so let's do storybook
00:33:02.419
odds table so in storybook this is kind
00:33:05.880
of what it looks like so it
00:33:07.140
automatically creates document we're
00:33:08.760
going to touch storybook when we get to
00:33:10.679
test driven development storybook
00:33:12.840
animatically creates documentation for
00:33:15.240
you in terms of your JS doc or your
00:33:18.059
typescript because again and then it
00:33:19.860
says you know like when you look at the
00:33:21.299
component this is what you can pass
00:33:22.980
through the component this is what like
00:33:24.840
the values and so forth and it arrives
00:33:26.700
so you get automatic documentation
00:33:28.620
creation and not only that if you have
00:33:30.659
static type checking then it's going to
00:33:32.220
give you a warning if you try and do
00:33:34.740
inner and for example you try and pass
00:33:37.380
to do thing one then you can say hey you
00:33:40.440
said this needs to be a function this is
00:33:42.299
incorrect and in the same way then you
00:33:44.279
can hover over it and it's going to give
00:33:46.019
you a description oh man like I can't
00:33:47.940
tell you guys how cool this is and this
00:33:49.980
is why there's no specific react plug-in
00:33:53.100
for vs code because this is all just
00:33:55.200
JavaScript so you get all the stuff from
00:33:57.360
JavaScript for free if you hover over
00:33:59.399
this it's effective it's just a function
00:34:00.840
with the property right we can create
00:34:02.760
interfaces for your components because
00:34:05.220
you know they're just encapsulated
00:34:06.899
things the encapsulated functions with
00:34:09.780
an interface and then you just pass a
00:34:12.060
reference of a function you can pass it
00:34:13.980
down into that encapsulated thing and it
00:34:16.139
just calls it it doesn't know what it's
00:34:17.639
doing you just tell it call this thing
00:34:19.500
that was passed into it when you click
00:34:21.000
or whatever so you can actually swap out
00:34:23.099
Behavior as well which once again now we
00:34:25.320
get to polymorphism where you actually
00:34:27.599
don't know what this thing is going to
00:34:29.460
accept you can pass anything into it so
00:34:31.139
on the Fly you can swap things out you
00:34:33.000
can even have conditional things where
00:34:34.918
if a user is signed in then call this
00:34:37.800
function if a user isn't signed in then
00:34:40.139
call this function okay so you can do
00:34:41.940
super powerful stuff like that and you
00:34:44.040
might notice that this corresponds to
00:34:46.560
prop in jstock so this props isn't a
00:34:49.560
made-up reactor it's effectively just
00:34:51.839
properties it's literally a function and
00:34:53.879
you're passing down properties this is
00:34:55.560
this idea of a property is as all the
00:34:57.839
JavaScript itself once again there's a
00:35:00.000
ton of material on the it is a bit of a
00:35:02.700
hard thing to understand so if you still
00:35:04.260
don't understand what what lifting the
00:35:06.180
state up means just Google it you're
00:35:07.980
going to find a ton of stuff have a look
00:35:09.720
on YouTube on videos where it explains
00:35:11.460
you know what is lifting the state up so
00:35:13.079
effectively just move the state up and
00:35:14.760
you pass the references to the functions
00:35:17.579
and stuff downwards so here it just
00:35:19.800
shows an example