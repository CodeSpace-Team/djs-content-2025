00:00:00.359
okay so we have done a lot of really
00:00:02.879
great things um so let's get really into
00:00:06.040
the meat of this and really flashh this
00:00:08.039
out bring in the shoeless stuff as well
00:00:10.200
and let's just build some basic
00:00:12.000
semblance of a to-do app and then we can
00:00:14.440
start talking about high order functions
00:00:16.560
and you'll be able to see how high order
00:00:19.000
functions fit very nicely into this
00:00:21.359
approach all right so let us go to
00:00:24.439
shoelace and pull that in so we're just
00:00:27.279
going to use the CDN um as mentioned you
00:00:30.039
know there are some performance
00:00:31.640
implications to using the CDN which is
00:00:34.360
why generally you want to install it via
00:00:36.239
node so you'll see down here as
00:00:38.680
mentioned let's just keep with the CDN
00:00:40.559
now up until we kind of really unpack
00:00:42.719
node and npm and and dive into the
00:00:45.079
details so I'm just going to use a
00:00:46.920
traditional loader so let's just copy
00:00:49.160
that and let us just pull it in here in
00:00:52.120
our HTML as last time you can just defer
00:00:55.440
the um JavaScript the only reason why
00:00:58.480
it's not deferred by default is cuz it
00:01:00.760
isn't sure whether you are deferring
00:01:02.800
yours and the problem is if you are not
00:01:05.159
deferring yours and this is deferred
00:01:07.680
this is only going to run after your
00:01:09.479
code runs um so it's just trying to be
00:01:12.040
safe but obviously since we are
00:01:14.479
deferring both they should actually load
00:01:16.400
in the correct order to do app uh let's
00:01:19.280
just start with a button and so this
00:01:21.360
form itself um I want to put this in a
00:01:24.479
dialogue but for now let's just add a
00:01:26.520
button that's going to trigger that
00:01:28.119
dialogue up here that would be SL button
00:01:31.920
so variant primary and that would just
00:01:35.040
be add task and that would open the
00:01:37.640
model so let's spin this up and there is
00:01:40.799
our add task let's also just add some
00:01:43.439
basic um styling to this from shoelace
00:01:47.240
so styles. CSS we can if we do decide to
00:01:51.840
create some web components which I I
00:01:53.880
think we are going to then we can
00:01:55.479
actually split up the styling but let's
00:01:57.640
start simple and then we can always make
00:02:00.119
it more complex break out some
00:02:01.719
components as we go think shoelace
00:02:04.240
already includes this but let us just
00:02:06.479
include it just to be double sure um
00:02:08.878
just and also maybe just out of habit I
00:02:10.959
tend to do this at the start of any CSS
00:02:13.239
file and then let's do our body and also
00:02:15.599
I think shoeless does this for us as
00:02:17.560
well but you can never be too sure so
00:02:19.720
let's say font family and this will be
00:02:21.800
VAR and let's put in SL font s there and
00:02:26.519
we need to pull in the Styles file so
00:02:29.200
let's pull that and after shoelace
00:02:31.840
because remember like the variables are
00:02:33.480
declared in shoelace so we need to pull
00:02:35.840
in shoelace first and then our own
00:02:37.879
custom style there we go right that's
00:02:39.879
looking really nice and what we now want
00:02:42.000
to do is let's put this new task behind
00:02:43.879
a model so you need to click that to
00:02:45.519
open the task SL dialogue okay so let's
00:02:49.480
do SL dialogue and SL uh dialogue and we
00:02:54.360
can even move this out of the header and
00:02:56.840
let's put it at the top of the site up
00:02:59.680
here yeah I need to close that that's
00:03:02.080
why it's unhappy and you'll also see a
00:03:04.840
really cool thing and we didn't get this
00:03:07.280
previously and I forgot to mention it so
00:03:09.159
up until now we've mostly been working
00:03:11.200
with strings so we would go do for
00:03:14.599
example you know example and then H like
00:03:17.440
a template Lal like that so Dove you
00:03:19.680
know 1 2 3 Dove and we would use this
00:03:24.680
extension that we have to actually add
00:03:26.680
syntax highlighting but we wouldn't it
00:03:29.319
wouldn't treat this as HTML so you know
00:03:31.840
we would do and prio wouldn't work on it
00:03:34.400
so we would also get no Auto completion
00:03:36.760
so if we do control space um you know it
00:03:39.680
doesn't give us it's just a string so
00:03:41.680
even if I save it doesn't format it
00:03:43.840
correctly whereas here we do so you'll
00:03:45.879
see even if I make it like that and I
00:03:47.519
save it actually formats it as if it's
00:03:49.720
HTML so there's a specific plugin that I
00:03:52.840
use called just simply called L HTML and
00:03:55.959
you'll see it has like three 300,000
00:03:58.560
downloads um and what this effectively
00:04:01.680
does it actually treats what you put
00:04:06.000
inside this HTML HTML with a backtick it
00:04:10.360
treats that as if it is actual HTML so
00:04:13.799
as if you are inside an HTML file so
00:04:16.120
that is amazing so you once again you
00:04:18.639
know you get order so if I do control
00:04:20.079
space it actually gives me like the same
00:04:22.280
Auto completion I would get in actual
00:04:24.360
HTML if I do style it actually gives me
00:04:28.320
CSS autoc completion
00:04:30.240
which we didn't get before so you know I
00:04:32.039
can go background you know I can go body
00:04:34.639
and you know background and whatever
00:04:36.479
okay so this is really cool it treats it
00:04:38.320
as if it is HML which helps a ton and
00:04:40.880
I'm going to show you how this also is
00:04:42.560
really cool in terms of giving us Auto
00:04:44.479
completion on our own components so we
00:04:46.840
put this in here and it's currently
00:04:48.320
closed so if we do open then it should
00:04:51.080
show um so let's just keep it open for
00:04:53.080
now so we can work on it um one thing
00:04:56.240
that we need to have a look at is in it
00:05:00.320
it it talks about uh form controls and
00:05:04.000
there's just a couple of things we need
00:05:05.520
to be mindful of when we're working with
00:05:07.360
forms and that is because every shoelace
00:05:09.960
component uses the shadow Dom one of the
00:05:12.680
problems with this is keep in mind
00:05:14.680
remember that the shadow Dom is almost a
00:05:16.520
domum in itself and it's completely
00:05:18.520
hidden from the actual real Dom this
00:05:21.800
means that if there's a form outside it
00:05:25.039
or next to it it actually doesn't have
00:05:27.520
access to the input element inside it so
00:05:30.520
you need to use a special shoelace
00:05:33.080
specific method to actually get that so
00:05:36.400
the way it does this uh is by using the
00:05:38.800
form data event so what the shoeless
00:05:41.400
components do is they automatically
00:05:44.319
append their values to the form data
00:05:47.479
object when the form is actually
00:05:49.960
submitted this doesn't change anything
00:05:52.360
because we have been doing it in this
00:05:54.479
way so it actually just provides the
00:05:57.080
means for that to still work but it is
00:05:59.720
important to keep in mind it has some
00:06:02.240
built-in ways to actually give you this
00:06:04.520
by default um if you create your own web
00:06:07.160
components you need to also allow for
00:06:09.800
this cuz by default it's not going to be
00:06:11.639
able to do it but yeah so here it
00:06:13.520
actually shows you know exactly how
00:06:15.599
we've done it so you take the actual
00:06:17.680
element the form element itself and you
00:06:19.440
put it in form data form and we're
00:06:21.720
already listening for form submissions
00:06:24.280
so let's add some shoeless things in
00:06:26.759
here so let's say SL button and variant
00:06:31.400
primary and let's close that and let's
00:06:33.919
say save let's add another button that
00:06:36.280
is cancel that is not primary okay so
00:06:39.440
there's our two buttons it is going nuts
00:06:42.319
because we're not closing this properly
00:06:43.919
there we go let's add a SL I think it's
00:06:47.759
input over here let's have a look at the
00:06:50.160
documentation say copy that and we can
00:06:52.720
actually say Okay so let's just say the
00:06:54.960
name is title and let's just make the
00:06:58.120
label task name and we can set it to
00:07:00.800
required remember that web components
00:07:04.080
need to be closed manually you can't
00:07:06.520
just like in regular HTML just keep it
00:07:09.240
open like that okay so there we go task
00:07:11.360
name so let's just see what else we can
00:07:13.280
do with the inputs so let's do s input
00:07:16.919
and so I actually like this fold version
00:07:20.000
as well like that so let's actually add
00:07:21.919
fold as well just to give it a bit more
00:07:24.240
depth like that uh let's also just add
00:07:26.599
some spacing here so let's I would
00:07:29.160
actually create my own web component to
00:07:31.360
help with spacing like these type of
00:07:33.360
things so let's actually go components
00:07:36.800
and let's just create TD spacing so TD
00:07:41.120
being to-do app and so this can be a
00:07:43.240
very simple one let's go class spacing
00:07:46.360
extends HTML element and I sometimes do
00:07:50.080
these in Frameworks as well I create
00:07:51.919
these type of things and effectively
00:07:54.080
this is just a Constructor and we run
00:07:56.039
super on it let's create a template up
00:07:58.520
here just for performance reasons
00:08:00.879
document create element template and all
00:08:06.080
that we have in there template in a HTML
00:08:09.520
it literally just wraps what we have in
00:08:11.759
a Dev and so let's put slot there and
00:08:14.240
let's also put some styling here so and
00:08:17.000
I'm just I'm not even going to use the
00:08:18.440
render from lit HML I'm just going to do
00:08:20.840
this myself it is simple enough and
00:08:22.840
let's just add a couple of styles and we
00:08:25.039
can map these to actual spacing from
00:08:28.440
shoelace so it goes from 3x to XX small
00:08:33.320
medium large x okay okay so let's grab
00:08:37.000
them and map them out and what I'm also
00:08:38.599
want to show you now is I want to show
00:08:40.120
you how we can actually get autoc
00:08:42.039
completion on our own components so let
00:08:44.839
me first do a type dep up here so as
00:08:48.200
said these are a bit intense so let's
00:08:49.800
just go XS s m l and XL all right so
00:08:57.279
then what we can say is we can say you
00:08:59.079
no so this is an element this is where
00:09:01.519
that H lit HML really becomes cool so we
00:09:04.279
can say element and the element is just
00:09:06.680
DD spacing and we can actually Define
00:09:08.959
attributes on it so we can go like that
00:09:11.360
and measurement and you won't get uh
00:09:15.720
like the actual highlighting that you
00:09:17.240
usually get of J's docks because this is
00:09:19.399
not an official J's do thing this is an
00:09:22.000
extra that um let HTML adds on top and
00:09:26.120
top bottom so we can set spacing on any
00:09:28.760
of these Left Right top bottom just
00:09:33.040
comment that out for now and let's just
00:09:34.640
register this and Export con spacing
00:09:38.360
export default spacing and let's export
00:09:40.959
spacing itself as well all right and
00:09:43.480
then obviously just before that we
00:09:45.839
register it so custom elements Define
00:09:49.240
and we do TD spacing and spacing pull
00:09:53.160
that in to our scripts meaning that we
00:09:55.880
have it available everywhere so let just
00:09:58.040
keep our things SE so here's all our
00:10:00.399
store stuff here's all our rendering
00:10:02.240
stuff let's do it in this order so store
00:10:05.959
stuff rendering stuff and then just
00:10:08.120
components at the top import components
00:10:11.800
uh TD spacing JS okay so check this out
00:10:15.640
now so if I go here now and I go TD
00:10:20.200
spacing one thing that's really cool
00:10:22.440
that you'll see now is that if we go on
00:10:25.040
that and we do control space it'll
00:10:27.480
actually give us some Auto completion
00:10:29.040
it'll say you know bottom left right top
00:10:31.320
so these are the actual attributes that
00:10:32.920
we can Define but one thing is that
00:10:35.680
you'll see if you do this it doesn't
00:10:37.639
actually tell you what are the actual
00:10:40.320
selections so let me show you how you
00:10:42.560
would do that so one thing that I forgot
00:10:44.880
about is that unfortunately you need to
00:10:47.680
manually put it in here um that is just
00:10:50.079
the way lit HTML works but otherwise it
00:10:53.040
kind of works in a similar fashion let
00:10:54.680
me just keep this up there uh just for
00:10:56.839
reference if I want um but we need to go
00:11:00.360
like this and see now it'll actually
00:11:02.600
warn us so the TS check itself is saying
00:11:05.560
that we're trying to actually pass
00:11:07.440
something that isn't valid um so this is
00:11:10.519
great so then you'll see I actually have
00:11:12.839
another plugin here that actually gives
00:11:15.959
me warnings if I'm trying to pass
00:11:18.560
something that's not correct and I'll
00:11:19.959
I'll say what plugin this is is in I
00:11:22.519
will mention what plugin this is in a
00:11:24.880
second but you can also do control space
00:11:26.800
and you will actually get Auto
00:11:27.959
completion and then it goes away and
00:11:29.519
then if you try and do that so this is
00:11:31.320
really cool just in terms of type safety
00:11:33.240
in our actual HTML itself um but let me
00:11:35.880
just show you the plugin that I use to
00:11:37.519
give me that so that is uh so you can
00:11:39.959
just search I think it's just called lit
00:11:41.519
plugin yes so this one um it has a bit
00:11:44.600
less um uh downloads and and all it does
00:11:47.560
it actually gives you like type checking
00:11:50.240
um on your HTML so on your lit HTML
00:11:52.480
which is amazing um so yeah um install
00:11:56.160
that one if if this is something you
00:11:57.720
like as well but uh the only caveat
00:11:59.839
being that the just the way it works you
00:12:02.760
just need to declare it directly in here
00:12:06.560
um instead of a type Def and then
00:12:08.360
reusing it so now obviously we need to
00:12:11.040
do something with that so let's actually
00:12:13.639
just create the styles for this as you
00:12:16.000
remember um the actual variables
00:12:18.920
actually Pierce The Shadow Dom so this
00:12:20.880
means that all of these are actually
00:12:23.360
going to be available in our CSS so let
00:12:26.440
me just just do HTML remember we're not
00:12:28.839
using us um lit HML here I'm just doing
00:12:31.600
it straight up as a string with like
00:12:33.560
plain web components meaning this
00:12:35.079
project can also be used like this
00:12:37.160
component itself can actually be used in
00:12:39.519
any uh JavaScript framework I might even
00:12:41.800
share this with you guys um this
00:12:43.600
Javascript file in the resources if you
00:12:45.560
just want to pull it into yours so one
00:12:48.120
thing that's really cool that we can do
00:12:50.560
here is we can actually map the Styles
00:12:53.600
based on what is set on the parent
00:12:56.440
component so in other words what is
00:12:58.279
actually set here so that's actually
00:13:01.079
really neat so let me show you how to do
00:13:02.800
that so you do that by making use of
00:13:05.639
host so you can just search for host
00:13:08.839
CSS um so over here so you'll see this
00:13:11.920
is only for the shadow Dom it has no
00:13:13.600
effect outside of actual Shadow Doms and
00:13:16.360
what you can say is if the host has the
00:13:18.360
following then apply the following style
00:13:20.600
so what we can actually do is we can say
00:13:22.680
if the host has a left equals XS then
00:13:28.320
apply the following to the dev inside
00:13:30.760
what we can actually do is we can create
00:13:32.680
this D so we can type all of these out
00:13:34.360
by hand or we can create it dynamically
00:13:36.639
and this is a good opportunity for me to
00:13:38.720
show you actually uh higher order
00:13:41.120
functions so let's just say template
00:13:43.519
string and so what we want to do is we
00:13:46.800
want to create an array of all
00:13:49.320
measurements and let's put it here at
00:13:52.000
the top of our file and let's just say
00:13:54.279
it is type measurement and array of
00:13:58.480
measurements okay and I'm writing it
00:14:00.199
like this effectively indicating that
00:14:02.199
it's kind of a configuration it's not an
00:14:04.120
actual value that's getting passed so
00:14:05.800
it's instructions for the code itself
00:14:08.800
not part of the code and so then we
00:14:10.959
should also get Auto completion so let's
00:14:13.320
do XS s m
00:14:16.759
LX and I missed a comma over there and I
00:14:20.279
think that's all of them so then what we
00:14:22.399
want to do is and let's do template
00:14:24.639
string we map over these and we create
00:14:28.320
four new arrays so we duplicate four
00:14:31.160
times creating four new arrays so let's
00:14:34.759
also just create the direction so we can
00:14:37.800
put this in this type def up here as
00:14:39.759
well so let's just say Direction so Left
00:14:44.040
Right top and bottom okay there we go so
00:14:47.759
Direction so let's also create type
00:14:50.920
Direction and I broke my own rule where
00:14:53.759
I usually write these in uppercase like
00:14:56.639
that all right so const directions Left
00:15:00.440
Right top bottom okay so now what we can
00:15:04.240
do is say template string so we start
00:15:09.320
with directions okay then we say map
00:15:12.880
over directions get the actual Direction
00:15:17.680
abbreviation and return a new array and
00:15:22.040
that array should be return the actual
00:15:25.800
measure measurements array and let's
00:15:27.560
just close that function all right so
00:15:29.519
now we're using a higher order function
00:15:31.279
we're mapping over it and let me
00:15:33.600
actually just do this in the browser so
00:15:35.600
you can see the result of it each of
00:15:38.880
these have xss m l XL and what I also
00:15:43.839
realized is we actually don't want the
00:15:45.560
abbreviations we want the full name
00:15:47.279
because that's actually how we're
00:15:49.000
writing the attribute so there should be
00:15:51.360
left right top and bottom and it's
00:15:54.240
obviously unhappy because these don't
00:15:56.079
correspond to any of that so left right
00:15:59.839
top and bottom so let's give it a try
00:16:02.600
again so what we want to do is we want
00:16:04.639
to map over measurements again before we
00:16:07.759
return it and so that would be a single
00:16:11.399
measurement let's call the single
00:16:13.560
Direction so we map over this again if
00:16:16.360
it's easy for you to reason about you
00:16:18.000
can write it like this result and then
00:16:19.880
it has a function in it and then what we
00:16:22.120
want to do is each time we map over that
00:16:25.120
inner array we just want to return the
00:16:28.160
single Direction C with the single
00:16:31.120
measurement inside okay so this should
00:16:33.160
give us the attributes and then just
00:16:34.800
return the result so there's two higher
00:16:37.360
order functions inside one another left
00:16:40.079
XL left s left M left L left XL so but
00:16:44.959
this is nested arrays so what we can do
00:16:48.000
if we want to actually make it a single
00:16:50.399
level so just not have it an like a set
00:16:53.360
of arrays inside arrays we can do
00:16:55.759
another thing on it so after we do that
00:16:58.079
we can actually just do flat okay let's
00:17:00.519
check now so now it's a big array with
00:17:02.360
all this stuff um this is just escaped
00:17:05.319
don't worry about this it's not actually
00:17:07.640
going to be in the thing itself so it
00:17:10.000
just escapes that you'll see here it
00:17:12.319
doesn't have the Escape but we can
00:17:13.959
actually combine these we can combine
00:17:15.919
them into something called flat map
00:17:17.799
which is actually something that's a
00:17:19.439
very big a functional programming
00:17:21.720
principle so mapping over something and
00:17:23.679
then make and flattening it afterwards
00:17:26.359
so if we want to go more full on
00:17:28.919
functional programming we can also make
00:17:31.160
this more what is called Point free
00:17:33.400
which means like we don't actually at
00:17:35.960
any time save anything in the variable
00:17:38.120
so we can full on do this but if you're
00:17:40.600
not used to this this might get a bit
00:17:42.240
hard to read but I'm just going to do it
00:17:44.160
in that style to kind of show you how
00:17:45.760
expressive um functional programming can
00:17:48.280
be okay there we go exact same result we
00:17:51.280
another thing we can do is we can break
00:17:53.240
this out into what's called a cured
00:17:56.799
function so in other words a function
00:17:59.240
that takes one parameter and returns a
00:18:02.000
new function so let's just say inner
00:18:05.240
Handler an inner Handler takes single
00:18:08.159
Direction and it just returns it does
00:18:11.400
The Following on it so then you can even
00:18:13.360
pass it like that um but let's keep it
00:18:15.799
like this for now and just to make it a
00:18:17.440
bit more readable to you um if you're
00:18:19.679
not used to this style of programming
00:18:22.159
let's just return like if you're used to
00:18:24.600
this this is very expressive you know
00:18:26.320
it's almost like once again that
00:18:27.760
mathematical 1 + 1 is 2 so if you
00:18:30.559
understand uh addition if you understand
00:18:33.039
equation and if you understand
00:18:34.880
mathematics then this is really very
00:18:38.039
expressive but if you don't if you have
00:18:40.120
no idea what these me things mean it's
00:18:42.159
very confusing um and it's the case here
00:18:44.720
if you're used to this type of style
00:18:46.520
then it's actually very expressive and
00:18:48.360
so what we want to do then is we want to
00:18:50.720
map over it again and I'm just going to
00:18:53.400
get rid of the flat map because once
00:18:55.400
again if you're not used to this this
00:18:57.159
might be a bit hard for you to follow
00:18:58.840
I'm just going to do these as two
00:19:00.640
separate steps and then run flat
00:19:02.760
afterwards and then once we flatten it
00:19:05.080
so let me just bring flat in there and
00:19:06.840
then the next thing we want to do on it
00:19:08.440
is we want to map over it again at that
00:19:10.919
point we can just say it is an attribute
00:19:12.880
so you can even use your um naming of
00:19:16.400
your arguments in functional programming
00:19:18.799
to indicate also a bit of like what is
00:19:21.760
the thing at that point what are you
00:19:23.080
expecting and so forth and so then we
00:19:25.120
want to maybe turn it into a selector so
00:19:28.000
that would mean we would go host and
00:19:31.080
just put the attribute in there and let
00:19:33.760
me maybe break this up so what I
00:19:36.240
sometimes do if I have files that
00:19:38.080
support other files is I actually go for
00:19:40.720
example like this and then I do dot for
00:19:43.320
example helpers okay then let clear the
00:19:46.000
relationship so let's break all of this
00:19:48.480
out into a complete separate thing and
00:19:50.960
we can just export the template string
00:19:53.520
so that means that from here we can just
00:19:56.280
import it from helpers and just apply it
00:19:59.600
directly we can just Chuck it in there
00:20:01.480
like this and let's just grab this for
00:20:03.000
reference if we want to really lean into
00:20:05.760
functional programming let's actually
00:20:07.760
write this as an actual function that we
00:20:11.520
can reuse if we want to do something
00:20:13.600
like this again so let's go merge arrays
00:20:17.960
and then we can just write our
00:20:18.960
description up here and so effectively
00:20:21.880
what this does is we can just say you
00:20:23.799
know array one and array two let's say
00:20:27.400
both of them need to be an array of
00:20:30.200
strings and let's also accept a call
00:20:32.640
back that we can just call join that
00:20:36.679
determines how they should be combined
00:20:39.039
and let's just call it join and so all
00:20:41.039
that that does bam it just takes string
00:20:45.120
and let's say value One String value two
00:20:48.520
and that just determines how they get
00:20:50.159
merged together we can even make this
00:20:52.360
optional and say that if you don't
00:20:54.520
specify anything then it actually just
00:20:57.120
merges them directly as is and so this
00:20:59.919
we can say array string and array string
00:21:03.000
like that and let's just do join as
00:21:06.679
always let's maybe even write this as
00:21:08.280
props I that's needs to beam and it's as
00:21:11.200
easy as going props props okay and then
00:21:14.559
we can just destructure here our actual
00:21:17.080
custom function that we create we're
00:21:18.799
actually creating our own custom higher
00:21:20.400
order function which is effectively it
00:21:23.120
takes a function itself so you can see
00:21:24.919
how we can now start actually combining
00:21:26.880
these functions almost as Lego block to
00:21:29.159
create more and more advanced uh
00:21:31.360
behavior and let's just do props over
00:21:34.000
here array one and array two and then
00:21:37.200
also join oh we need to say props join
00:21:40.559
let's just add a note here um if no call
00:21:44.360
back is provided then we'll simply
00:21:48.640
combine as is let's just Che this logic
00:21:51.840
so let's just say const result so result
00:21:55.520
it takes array one and it flat Maps over
00:21:58.279
array aray one let's just say array one
00:22:01.400
value inside that closure what it does
00:22:04.279
it let's just do inner and we say array
00:22:07.240
two and we map over that let's just say
00:22:10.679
array two value and it simply returns
00:22:15.360
join so what we want to do is Let's do
00:22:17.480
an interpolation see if join exists if
00:22:20.120
join exists then we simply pass value
00:22:24.520
array value one and array two value
00:22:28.200
otherwise
00:22:29.039
we just combine them as is cool so this
00:22:31.520
is very expressive as well there's no
00:22:33.559
four Loops or whatever you can follow
00:22:35.279
the logic all the way step one step two
00:22:38.039
step three step four and so forth you
00:22:40.480
don't need to go back up again down up
00:22:43.000
back follow like the logic all the time
00:22:45.279
and so now we actually created our own
00:22:47.279
reusable functional higher order
00:22:49.640
function and so we can actually then do
00:22:52.559
template string and we do merge arrays
00:22:55.320
and then obviously we need to return
00:22:57.720
Okay so let's do template string over
00:23:01.120
here and we do merge arrays I also need
00:23:04.200
to return that so obviously it's unhappy
00:23:07.400
because it expects the following so
00:23:10.080
array one uh directions and array two is
00:23:14.720
measurements and then we have our join
00:23:17.080
function which you can just declare
00:23:18.760
straight in here and let's say Direction
00:23:22.720
and measurement um here I let go my
00:23:26.640
general rule because it's very clear to
00:23:28.720
me that these are different things and
00:23:32.120
Direction measurement all right so let's
00:23:36.200
also add the host stuff over here as
00:23:39.080
well okay cool um and then we can also
00:23:41.760
maybe even split out join here and we
00:23:44.000
can say handle join and just pass that
00:23:47.480
and so what we want is we want padding
00:23:50.880
and the direction and let's also just
00:23:52.960
write it like this so it looks a bit
00:23:55.120
more like cssh is and now we just want
00:23:58.000
to map M the measurement to one of the
00:24:01.799
actual values is let's actually create
00:24:04.799
an object and let's just say
00:24:07.559
measurements map so as you can see here
00:24:10.840
so this is very similar to the actual
00:24:12.760
method map so map means you actually
00:24:14.880
connect two things to one another the
00:24:17.760
one is just like by means of a method
00:24:20.000
the other one like so I just write map
00:24:22.400
but the idea of map is you have this
00:24:24.120
connection like there's one thing that
00:24:26.120
connects to another thing and let me
00:24:28.000
just get get those from shoelace quickly
00:24:31.080
spacing all right here they are and
00:24:33.559
let's just map them and we can map them
00:24:35.039
in whatever way we want and this is also
00:24:37.320
why um it's useful to kind of have this
00:24:39.440
type of thing because it allows you to
00:24:42.080
actually configure how the code should
00:24:44.840
actually run without actually changing
00:24:46.520
the logic itself so we can just say
00:24:49.000
record and a measurement that maps to a
00:24:53.399
string value that string value will just
00:24:56.039
be the name of the array and because we
00:24:57.880
did that we can just auto complete so
00:25:01.279
these don't even need to perfectly line
00:25:03.279
up with what we are using we can do it
00:25:05.640
whatever way we want so we can say large
00:25:08.080
ears let's just organize them in a
00:25:11.039
reasonable increasing fashion so all
00:25:13.919
right so let's see so medium let's keep
00:25:16.919
that at 16 that's what I make my own
00:25:19.320
medium usually as well uh small let's go
00:25:22.679
the extra small R XS like that and
00:25:27.600
usually let's go with extra large for
00:25:31.440
their large we don't necessarily want
00:25:34.000
and then 3XL and we can always toggle
00:25:36.200
these let's just go with that and this
00:25:38.399
is unhappy because oops I actually wrote
00:25:40.960
it as typescript we are going to touch
00:25:42.520
on typescript at some point don't worry
00:25:44.320
you you might have been like SC what are
00:25:45.679
you doing okay so there we go so now we
00:25:49.720
can just use that as a reference and
00:25:52.520
let's also move this all the way to the
00:25:54.559
top let's just say bar let's say
00:25:59.080
measurements map and then we just pass
00:26:02.880
measurement so obviously this is still
00:26:04.840
an array and at the end we need to
00:26:08.159
actually join all of them and how do we
00:26:11.720
want to join them we just want to join
00:26:13.600
them as as and let's actually put like
00:26:16.159
empty space below them so just a single
00:26:18.760
empty space like this and let's run it
00:26:21.039
in our browser so control a control C
00:26:24.279
and here we go so this is what it
00:26:25.760
produces for us yes okay okay and then
00:26:28.880
we just so what we then lastly want to
00:26:31.039
do is we obviously so we can just do CSS
00:26:34.279
and then the actual temperature that we
00:26:36.840
export is as follows and we can even put
00:26:40.840
this on there for syntax highlighting so
00:26:42.799
that would be you know style and then we
00:26:45.320
just put CSS in there and just a div
00:26:48.320
with a slot one thing that I did miss
00:26:52.440
here we actually need something to apply
00:26:55.039
to and that is just the div so remember
00:26:57.360
if you have a space it's like okay that
00:26:59.600
is a child of that so the div the only
00:27:02.200
div in the component that is a child of
00:27:04.520
this and we can even if we want do this
00:27:07.120
to get CSS highlighting which actually
00:27:09.840
shows me error so I'm actually glad we
00:27:11.919
did this cuz it actually showed me a
00:27:13.720
typo that I made and while we're at it
00:27:16.399
obviously dollar sign there as well
00:27:18.559
right so let's cheuck this in the
00:27:19.720
browser and we just need to get rid of
00:27:21.960
export CU it obviously doesn't like
00:27:24.080
export all right so all right so let's
00:27:27.279
give it a try let's C so we can just
00:27:29.880
import that and any other handlers we
00:27:32.200
can put in here as well this should be
00:27:34.760
good and so before we do this we also
00:27:38.320
just need to actually attach the
00:27:40.000
template so um we can create a private
00:27:44.799
here again so we can go inner and this
00:27:48.440
attach Shadow and mode is closed and all
00:27:52.360
that we do is we grab that so we go
00:27:55.880
template CL content clone node true and
00:28:01.039
then we just go this in a Ben child cool
00:28:05.159
so let me go to the browser let's see
00:28:07.440
and let me also just remove these let's
00:28:09.360
see so let's just add three of these
00:28:12.480
underneath one another and actually see
00:28:13.960
if it add some spacing and check that
00:28:16.120
out it actually adds some spacing uh
00:28:18.039
let's add some spacing on the one side
00:28:20.080
of it so let's go left let's also just
00:28:22.640
go XL cool check it out okay so now we
00:28:24.960
have a pretty cool utility that we can
00:28:26.880
actually just use like that
00:28:29.000
um to move things around so let's create
00:28:31.799
our utils folder again and let's
00:28:34.640
actually put this as a generic utility
00:28:38.240
in there that we can use any place and
00:28:40.919
let's just call it um arrays so this is
00:28:43.720
maybe all my utilities that have to do
00:28:46.240
with arrays actually I shouldn't pull
00:28:48.240
handle join in here merge arrays just
00:28:51.760
pull it in here okay so let's just say
00:28:54.519
import so it's useful to start um
00:28:57.279
building out kind
00:28:58.760
utilities folder with kind of common
00:29:01.159
utilities that you use throughout your
00:29:03.760
project and these are kind of not
00:29:05.159
necessarily the code itself but these
00:29:06.720
are actual functions and things that you
00:29:08.720
actually use on your code itself they
00:29:10.559
are maybe tools so they're not related
00:29:13.039
to the code base itself uh so this is
00:29:16.559
you know like Hammers and SS and so
00:29:18.519
forth It's not the actual material
00:29:20.799
itself specifically if it's something
00:29:23.080
that you kind of might possibly do on a
00:29:25.840
regular basis that's generic enough like
00:29:27.760
this let's also I think we can actually
00:29:30.000
let's make this arrays and just pass it
00:29:32.720
in like that is a bit nicer so we can
00:29:36.080
just say it's an array of array of
00:29:39.039
strings and then we can just go first
00:29:42.720
second and so here's where things get
00:29:45.200
crazy and I I want to show you you know
00:29:47.360
like this is the this is what's so great
00:29:50.080
about composition let's say we want to
00:29:52.760
merge three um so let me just copy that
00:29:55.159
and let's actually just do it right in
00:29:57.000
our console window and once again now
00:29:58.919
we're getting back into like
00:30:00.159
polymorphism and specifically where I
00:30:02.480
mentioned you know this idea of passing
00:30:04.320
abstractions into abstractions into
00:30:06.080
abstractions into abstractions so let's
00:30:08.080
bring in the code that actually uses
00:30:10.159
that so this is in our spacing Helper
00:30:13.000
and this is maybe actually now short
00:30:15.679
enough that we can even we no longer
00:30:18.600
need to put it in here and we can
00:30:20.080
actually maybe just put it straight in
00:30:21.840
here because we extracted the generic
00:30:24.720
part of it into actual utility so if I
00:30:28.480
just grab this the handle join and the
00:30:31.919
merge so just to kind of illustrate this
00:30:34.880
so let's say we uh just have two arrays
00:30:38.440
and I'm just going to do them straight
00:30:39.919
up in here so let's say we have a b c d
00:30:44.080
e f okay so those are our two arrays uh
00:30:47.559
let's just write something directly in
00:30:49.159
here we don't need something as fancy as
00:30:51.120
this uh let's just say Val one and Val 2
00:30:54.840
and what we do with them is just
00:30:57.279
separate them with the dash so Val one
00:31:00.159
dash Val 2 okay there we go this should
00:31:03.240
work and let's just also result instead
00:31:06.399
of CSS and console log result oh
00:31:10.000
obviously it's not happy doesn't like
00:31:12.399
export just get rid of this joint so we
00:31:15.120
can actually see it as an emerged array
00:31:17.960
and not as a big string okay ad cool so
00:31:21.440
let's say we want to add another thing
00:31:23.039
into the mix you can actually call this
00:31:26.760
itself in the joint join so you can pass
00:31:29.279
the function into itself or pass the
00:31:31.480
abstraction into itself with its own
00:31:33.519
join so let's just say in a result and
00:31:36.519
let's do inner result and let's add
00:31:39.240
another array so let's do merge arrays
00:31:42.960
and let's also not give this one a join
00:31:45.039
so it can just do the default behavior
00:31:47.320
in fact let's have it do the default
00:31:49.240
Behavior here but we just manually do it
00:31:51.559
g h i and a single array just with the
00:31:56.279
new string return that
00:31:58.360
in a result and I just need to go array
00:32:02.399
close that one okay forgot about that
00:32:04.559
one and we need another extra one out
00:32:07.360
here we don't necessarily want to turn
00:32:08.880
it into a string but let's flatten uh
00:32:11.440
the results at the end flat not flat now
00:32:15.240
we've kind of extended this um to
00:32:18.559
actually do another loop and if we
00:32:20.799
really want to we can do even yet
00:32:22.360
another one and another one and another
00:32:24.039
one so you can pass merge array into
00:32:26.679
merge array itself and and this is
00:32:28.320
what's amazing about thinking about
00:32:31.240
functional composition