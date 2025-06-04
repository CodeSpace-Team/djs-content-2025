00:00:00.000
but obviously this isn't great so you
00:00:01.740
don't want it in this format so let's
00:00:03.480
just say values I'm running out of names
00:00:06.060
for things is it saying like you know
00:00:07.919
like the the two hardest things in
00:00:09.599
programming is caching validation and
00:00:11.160
naming things and then there's another
00:00:12.840
joke that's the two hardest things in in
00:00:15.360
programming is caching validation aiming
00:00:17.340
things in off by one errors the joke
00:00:19.380
being there's actually three and you
00:00:20.939
said there's going to be two programming
00:00:22.560
is fun let's just say that is value and
00:00:24.660
that is DD and I think it's margin let's
00:00:27.480
say margin zero and we probably want
00:00:29.939
these to be next to one another as well
00:00:31.920
so we can line the display Flex so you
00:00:36.300
can't put devs in your definition list
00:00:38.700
like that and we want a space there so
00:00:40.739
what I would just do is n bsp
00:00:43.340
non-breaking space what some people do
00:00:46.260
is they do this I I'm not a fan and I
00:00:49.260
don't like how it looks I just actually
00:00:50.579
write it out as a non-nb SP so
00:00:52.980
non-breaking space you tell it put a
00:00:55.020
non-breaking space character in there so
00:00:57.120
release so that is a release here and we
00:00:59.940
actually don't want release Here We want
00:01:01.860
actors also another thing we maybe want
00:01:04.860
to make this a button base so that when
00:01:07.439
you click it it has a little animation
00:01:09.060
button base uh if we put the button base
00:01:12.360
in here so this ripple effect but then
00:01:15.240
we need to put our padding in the button
00:01:16.920
base instead instead of the card make
00:01:19.740
this thing the button base so let's keep
00:01:21.720
this card and then let's just say const
00:01:24.840
style button base padding and the
00:01:27.479
display Flex we're going to keep the
00:01:28.979
margin on the card and this should be
00:01:31.140
the paper so that's a nice effect okay
00:01:33.479
so if we click at it it's a bit of a
00:01:35.460
ripple effect python base because
00:01:37.140
buttons by default we need to tell it to
00:01:39.360
text align left buttons might be for
00:01:42.119
Center text align all right so we're
00:01:43.799
getting somewhere here the last part is
00:01:45.780
bring in that icon that just shows you
00:01:47.759
can click on it add material icons and
00:01:51.619
arrow I think we need to check the iOS
00:01:54.479
one over here and we let's actually make
00:01:57.659
our info try and fill up all the space
00:01:59.880
so it would so the button itself needs
00:02:02.399
to be 100 the button itself which also
00:02:04.619
explains like when we clicked here it
00:02:06.060
didn't file and the button itself so let
00:02:08.580
me just show you if I make the button
00:02:09.959
itself red you'll see the button itself
00:02:11.760
doesn't extend all the way everywhere
00:02:13.680
100 this is maybe a bit too intense so
00:02:17.580
let's just icons give it a bit of an
00:02:19.860
opacity opacity let's go like 0.4 so
00:02:24.180
let's go four but let's make it a bit
00:02:26.220
smaller so we can do height uh one rim
00:02:29.160
with one Rim obviously not the greatest
00:02:31.500
design but it works maybe just a little
00:02:33.840
bit of a hover effect and then we are
00:02:35.940
mostly done background
00:02:38.220
um rgba let's just grab the material UI
00:02:41.459
regular color just this blue color I'd
00:02:43.860
encourage you to use a bit of a
00:02:45.420
different color scheme
00:02:47.400
um than what they're using your site
00:02:49.080
doesn't just look like a stock standard
00:02:50.819
like base mui side and let's give it
00:02:53.459
like 10. we actually let's put this on
00:02:55.739
the button instead probably now we have
00:02:58.200
a clear idea of something that can be
00:02:59.580
split up into a component so this thing
00:03:01.860
is probably we can probably make this a
00:03:03.599
component and so let's just call it
00:03:05.220
preview let's create a preview stories
00:03:07.739
TSX preview TSX and just index what I
00:03:12.900
generally do is I just pull everything
00:03:14.220
in here and instead of figuring out what
00:03:16.379
to move I pull everything in and then I
00:03:18.780
just delete the stuff so I just copy it
00:03:21.060
and I delete the stuff that I don't need
00:03:23.159
the props and what I usually do is and
00:03:26.159
I'll show you guys in a second what I
00:03:27.599
usually do is I name my my props type
00:03:30.540
the exact same as my as my actual
00:03:33.599
component we don't actually need the ID
00:03:36.000
though the title we need the actors we
00:03:38.400
need the release we need let's say the
00:03:40.319
release already needs to be a date by
00:03:42.120
the time we pass it in here an image
00:03:43.799
needs to be a string so by the time we
00:03:46.620
get it over here it already needs to be
00:03:48.959
a date so Props factors image release
00:03:52.019
and title here and then we don't need
00:03:56.220
the IDE then it should also okay so this
00:03:59.099
we can delete Within need the list mock
00:04:01.500
previews we can delete active we can
00:04:03.840
delete CSS Baseline we can delete all of
00:04:07.080
this we can delete so it shows us the
00:04:08.760
stuff that we're not using so then in
00:04:12.120
here let me just copy and paste this and
00:04:14.159
this will be preview let me get it from
00:04:17.040
preview and components preview preview
00:04:19.440
basic and it's unhappy because we need
00:04:21.540
to pass some stuff to it so this is now
00:04:24.479
where it starts getting cool we are
00:04:26.639
going to use something called storybook
00:04:28.020
controls right how do we add them all
00:04:30.300
right I'm going to have to try and
00:04:31.800
remember Port from so this would be
00:04:34.680
storybook react which is what we're
00:04:36.840
using and we want to pull in story
00:04:38.940
object just for type safety so we need
00:04:41.820
to pull in meta as well and then just
00:04:43.800
the types okay so we pull in meta as
00:04:46.560
well meta and Ebu all right and then the
00:04:51.000
remainder we do basic okay so we need to
00:04:54.479
say the component so the component that
00:04:57.060
this is used for is preview this is now
00:04:59.699
our object so we need to go story object
00:05:03.900
and we've passed the preview prompts to
00:05:07.259
it okay cool and so the default
00:05:09.180
arguments that it starts with we can
00:05:11.040
just make these the fake the values this
00:05:13.919
is what it starts with by default so
00:05:16.500
let's just grab that from here I need to
00:05:19.259
import Faker in here and we are no
00:05:21.960
longer doing the preview we're just
00:05:23.820
doing that I think we should be able to
00:05:26.039
do this I think it's just ID that we
00:05:28.680
don't need release oh and release now
00:05:30.720
needs to be an actual date cool so now
00:05:33.180
this preview as well and we go here and
00:05:34.979
check this out so now we can actually
00:05:37.259
toggle it so we can increase decrease
00:05:39.419
the amount of actors the image we can
00:05:41.820
change but it's probably going to break
00:05:43.199
if we give it like another Image Grab A
00:05:45.419
random image all right I don't even know
00:05:47.880
guys all right welcome to the internet I
00:05:50.520
guess all right so then we can put that
00:05:52.080
in there there's a beautiful movie so
00:05:54.479
and we can also change the date but this
00:05:56.639
is going to break because that is not a
00:05:58.740
valid date so you can see if you change
00:06:00.539
the title it updates real time and so
00:06:02.460
forth try to estimate what these things
00:06:04.080
are but you can give it a bit more
00:06:05.960
clarity if you want by directly going
00:06:08.520
here and saying oh
00:06:10.320
types and then saying that as a release
00:06:14.240
control
00:06:15.979
so you can give it a bit more guidance
00:06:18.539
and so let's see if we then update it to
00:06:21.300
instead of 2013 we do so we can check
00:06:24.720
Cloud now it was completely isolated
00:06:26.699
this so we can test that component
00:06:28.560
completely on its own so the LI is the
00:06:31.620
card so let's just list style none on
00:06:34.560
here do so we have that thing we have it
00:06:36.419
tested and you know we can see okay what
00:06:38.880
happens if there's minus one actors or
00:06:42.060
you know whatever or this many actors or
00:06:44.160
what happens if the title is this long
00:06:46.080
so let's actually then say that after X
00:06:48.600
amount of lines let's say after three
00:06:50.520
lines it should actually just truncate
00:06:52.800
line clamps it says line clamp I'm just
00:06:55.560
going to copy the code and so what we
00:06:58.020
can do is on our title we can do line
00:07:00.479
clamp and yeah let's say three lines so
00:07:02.400
so now it actually does three dots if it
00:07:04.860
goes below that we actually just want to
00:07:07.319
set a width on our image not a height so
00:07:10.259
can actually you know like scale
00:07:12.539
accordingly it's swap out all of these
00:07:15.120
over here so we can actually now we're
00:07:17.520
going to get rid of a lot of code here
00:07:19.440
so let's just import let's import the
00:07:21.599
preview over here so let's get rid of
00:07:23.759
that if we can replace all of this now
00:07:26.099
with return just the preview we just we
00:07:30.539
can actually just pass all of these
00:07:32.400
except the ID or let's just say I just
00:07:35.160
call it inner props usually as not to
00:07:38.400
conflict with if we have props up there
00:07:40.560
but you can call it anything and then we
00:07:43.020
just pass in a prop so we can
00:07:45.240
destructure it directly on the component
00:07:47.520
and it is going to complain because it
00:07:49.680
wants release so let's just actually say
00:07:51.900
here release release string then that
00:07:54.240
part we just need to manually pass in
00:07:56.099
because we change it into a date before
00:07:58.080
we pass it in we just need the key for
00:08:00.419
the mapping and we don't pass the ID
00:08:02.520
through generally you put the the
00:08:05.340
structuring first okay so we no longer
00:08:07.919
need any of this all of this is now
00:08:09.660
contained in in our card okay so we
00:08:11.819
don't need this icon we don't need paper
00:08:13.500
we don't need typography we don't need
00:08:15.599
any of this so over here we need to
00:08:17.819
actually just tell it to actually just
00:08:19.379
export everything from preview some
00:08:22.020
people would write the actual component
00:08:23.759
in the index file the reason why I don't
00:08:26.580
do it is it's easier for me to actually
00:08:29.879
do my git diffing if it says for example
00:08:33.000
preview and I know what I'm looking at
00:08:35.159
otherwise you should have all these
00:08:36.659
index files and you need to look at okay
00:08:38.580
with the folder where does it come from
00:08:40.260
I just find it easier and for searching
00:08:42.958
and so forth so I don't put my code I
00:08:45.060
just re-export with the index the code
00:08:47.519
itself I put in a file with the name of
00:08:49.560
the component and so let's do our
00:08:51.540
filtering now okay so we need to now
00:08:53.519
actually go a level up let's pass all
00:08:55.800
this fake info now through storybook
00:08:58.200
instead let's create our types of the
00:09:01.019
app itself it props the app accepts is
00:09:04.620
let's just say list and list is a list
00:09:08.160
of previous weapon IDs so we can say
00:09:11.399
preview and let's just say you know ID
00:09:13.980
with the string as well props and let's
00:09:16.560
just destructure our list here same here
00:09:19.140
just app list and we need to say it's
00:09:22.140
obviously a array of this okay and
00:09:25.019
styles Global oh I think we accidentally
00:09:27.180
deleted this
00:09:28.620
um let me just undo undo undo until I
00:09:30.779
get it back again so yeah I need to pull
00:09:33.600
this in and where do we actually declare
00:09:35.399
that to export type app and app is list
00:09:39.180
and list is preview with IDE that is a
00:09:43.620
string I might even show you guys a bit
00:09:45.240
later how to do nominal typing which is
00:09:47.339
what I would actually do over here but
00:09:49.740
I'm scared it's going to confuse you if
00:09:51.839
I show it to you now and then list props
00:09:55.200
map over that list spell button we don't
00:09:57.899
need this we don't need this part we
00:10:00.000
need we've accidentally removed it last
00:10:01.740
time this we don't need image list we do
00:10:05.100
need card title info value line none of
00:10:08.399
this we need yeah I see now like the
00:10:09.899
actual app itself is below 40 Lines Just
00:10:13.440
because we've extracted all of this
00:10:15.120
Behavior into a preview component and we
00:10:17.760
can get rid of Faker and all of this and
00:10:19.680
all of this and yeah and obviously you
00:10:21.360
want your actual mock info in storybook
00:10:24.000
here instead of in your actual app
00:10:26.220
itself don't actually want to put mock
00:10:28.920
info in your app itself because it's
00:10:30.899
very easy to accidentally push code
00:10:32.700
online that uses fake information I've
00:10:34.680
typically done it in my life wouldn't
00:10:36.480
recommend it but like obviously if
00:10:38.220
you're just starting and you're just
00:10:39.420
building out the thing like and you're
00:10:40.920
sloppy and lazy like me just put it
00:10:43.260
straight in the file and work from there
00:10:44.760
until you're ready to pull it out just
00:10:46.860
be careful to not actually push it live
00:10:48.779
with the fake information so that users
00:10:51.420
see lorem ipsum and whatever pass some
00:10:53.820
stuff to that and that stuff is just
00:10:56.640
going to be this fake infinite that we
00:10:58.440
create um what I actually sometimes even
00:11:00.180
do is I actually do the following I do
00:11:02.760
preview and I do a mocking or mocks put
00:11:06.779
all my mocking stuff for that component
00:11:09.240
there and I'll show show you why in a
00:11:11.399
second from there I just export mocs or
00:11:14.519
I have like basic call and preview just
00:11:17.220
for the typing preview and then I say
00:11:19.740
okay I'm just make these functions so
00:11:22.140
you call a mocking function so preview
00:11:24.420
and this just creates this for you and
00:11:27.240
this needs to be a const fakely I need
00:11:29.640
to pull in Faker as well I think that is
00:11:31.860
it so and then I just actually export it
00:11:34.320
here as well the from mocks I just
00:11:36.540
export this mocking info as well why
00:11:39.300
that's useful is obviously now I can
00:11:41.100
just pull that in here and then I just
00:11:43.079
mock this here so this allows me to
00:11:45.420
create a basic mock of a preview
00:11:48.480
anywhere in my code so let's do list in
00:11:51.360
typescript I think I did show you guys
00:11:52.920
this you can go aft and then you can
00:11:55.019
select a specific thing on the on the
00:11:57.839
actual object but you need to do it in
00:11:59.940
this way in typescript you can't go dot
00:12:01.980
list like that there are several reasons
00:12:04.380
for it I'm not basically going to go
00:12:06.180
into it but so we just want that type of
00:12:08.279
new array once again let's do 40 this
00:12:11.640
time full undefined then map in that map
00:12:14.880
it's just going to run mocks basic you
00:12:18.180
can even I think you should even be able
00:12:20.040
to just pass it like that then just
00:12:22.620
creates 40 marks for us but I do think
00:12:25.200
one thing we need to add on top of that
00:12:27.360
that isn't part of this mocking actual
00:12:29.700
ID so we map over it again we just take
00:12:32.640
what's already there item and we just
00:12:35.100
add the ID onto it as well item so we
00:12:38.459
just destructure that in there and the
00:12:40.740
ID and we can base it off the index
00:12:43.800
again let's just do index plus one so
00:12:46.139
you're kind of working you're building
00:12:47.579
your app out you start it's just a blob
00:12:50.279
of code and then you kind of build it
00:12:51.660
out build it out build it out and every
00:12:53.279
step you're mindful of okay how do I
00:12:55.139
abstract it what all kind of what things
00:12:57.600
are encapsulated from one another yeah
00:12:59.639
it needs to be a number not a string so
00:13:01.860
let's add a big filtering button up
00:13:03.959
there and once again instead of like
00:13:05.399
breaking out the filtering already into
00:13:07.740
its own component I just extend my app
00:13:10.440
component until it starts getting about
00:13:12.060
bit obnoxious and then I'm like okay
00:13:14.100
cool I think I shared at some point with
00:13:16.200
you guys the wrong abstraction by Sandy
00:13:19.500
Metz yes the point being that it's
00:13:22.920
easier to actually create abstraction
00:13:26.700
than to remove abstraction the start of
00:13:29.639
duplication also the point of
00:13:31.860
abstraction is not remove duplication I
00:13:34.620
think this is a big thing that a lot of
00:13:36.839
people actually fall a trap they fall
00:13:38.940
into they think the point of abstraction
00:13:40.380
is to reduce duplication it's not the
00:13:43.200
point of abstraction is to make it
00:13:44.940
easier to reason and maintain your code
00:13:46.860
there's a really great article on or
00:13:48.959
video on this um kurdist epic he has
00:13:51.600
some great videos
00:13:53.040
um although like he doesn't do
00:13:54.779
JavaScript it's C I think so but he
00:13:57.360
explains the concept pretty well as long
00:13:59.160
as you're like mindful that this isn't
00:14:00.779
JavaScript so he shows where okay
00:14:03.300
there's this there's this piece of code
00:14:05.160
that you know comes up three times in
00:14:07.380
three different things that this piece
00:14:09.120
of code and you abstract it so you can
00:14:10.740
only put it in a single function but the
00:14:13.139
point being is this creates coupling
00:14:15.720
that shouldn't be there it actually
00:14:17.820
makes the code worse so don't look at
00:14:19.980
code and be like okay I want to keep
00:14:22.380
this as nice looking as possible think
00:14:24.839
about like like actual abstraction as
00:14:28.019
something that you do in order to make
00:14:29.760
your code maintainable and easier to
00:14:31.500
reason about don't fall into oh this is
00:14:34.079
a lot of code I need to move it
00:14:35.459
somewhere rather start adding
00:14:37.560
duplication and then abstract from there
00:14:40.139
instead of doing the wrong abstraction
00:14:42.000
and then having to go back and fix it so
00:14:44.519
what I'm going to do is I'm just going
00:14:45.480
to put the filters in here directly as
00:14:47.459
well until I see okay it should probably
00:14:49.980
be abstracted away and I can write my
00:14:52.440
own tests and stuff for it or let's say
00:14:54.300
filter or filter list doesn't really
00:14:56.579
matter what we call it alter list and so
00:14:58.440
there's a filter list button up there
00:15:00.000
give it a bit more styling so the
00:15:01.740
variant is contained let's move it to
00:15:04.860
the right hand side so let's create a
00:15:06.779
row thing row Style
00:15:09.779
a black justify content space between so
00:15:13.440
align item Center all right so let's
00:15:15.540
also just put a little logo here and
00:15:17.399
let's just call it typography movies app
00:15:20.339
and we need to pull in typography so
00:15:22.500
movies out put a strong in there not the
00:15:24.779
nicest logo but it is what it is we can
00:15:27.300
just grab dialogue from Material UI and
00:15:31.380
and I would be open just so we can work
00:15:34.139
on it okay so let's put a title in there
00:15:36.779
so H2 no let's make it an H1 okay so H1
00:15:40.620
photos all right and then in there let's
00:15:44.399
create a font in material UI you have
00:15:47.040
your text Fields uh also in our dialog
00:15:49.920
dialog content this is the dialog itself
00:15:52.740
the dialogue content it's just a regular
00:15:55.199
div actually let's make it the form
00:15:58.199
itself that's maybe not a bad idea okay
00:16:00.300
so let's make this the actual form
00:16:02.160
itself the dialogue content is the
00:16:04.740
actual form and let's also do this text
00:16:06.959
field variant bold and so the label on
00:16:11.040
this is just search something in there
00:16:13.620
and then you can submit it let's just
00:16:16.800
add a button here and let's just say
00:16:19.320
apply apply the filters and and make
00:16:23.040
this variant obtained material UI
00:16:26.040
actually ships with titles that you can
00:16:27.959
use for your dialogues action uh here's
00:16:30.959
all this done content uh okay I like
00:16:33.899
title dialogue action dialog content is
00:16:37.079
the other one yeah so you can do this
00:16:38.699
yourself or you can just use what they
00:16:40.440
give you that looks better yeah apply
00:16:42.480
and we maybe want cancel as well
00:16:44.579
outlined we need to tell this one it
00:16:47.160
should submit the form and I think we
00:16:49.259
can tell dialogue content let's just do
00:16:51.540
it this way let's do form I think you
00:16:53.880
need to give the form an ID D and let's
00:16:56.820
just filters and then what you can do is
00:16:59.639
apply you do supplement type supplement
00:17:02.040
so it's a submit form and so I think and
00:17:04.859
you have to say form what form to attach
00:17:07.380
it to yes okay but obviously it
00:17:09.240
refreshes is the page so now we're kind
00:17:12.059
of starting to get into like okay
00:17:13.500
there's too much actual logic that's
00:17:15.540
overlapping and interweaving let's maybe
00:17:18.059
now actually break it up into its own
00:17:20.699
component like I usually just take this
00:17:23.160
copy it in there and rename it this
00:17:25.319
filters we don't have Marks here and we
00:17:28.020
need to rename Alters Alters Alters I'm
00:17:33.059
gonna use Faker here and we also need to
00:17:35.340
say components filter filters filters
00:17:37.679
and it's unhappy because faulters
00:17:39.240
doesn't exist yet and the arguments we
00:17:42.299
can just say for now it's just an empty
00:17:44.580
object const filters and my classic
00:17:47.539
dev123 and let's drag this over to there
00:17:52.200
and we need to pull all of that in here
00:17:54.240
now as well so let's wrap the stuff from
00:17:57.120
here that we're no longer using put it
00:17:59.160
in filters and this typography we're not
00:18:02.520
using any of these uh is there anything
00:18:04.740
in here that we no longer need so this
00:18:06.900
looks good no so what filters is going
00:18:09.360
to do is when you submit it so all that
00:18:12.840
filters has is uh on submit type and
00:18:16.380
submit so we just pass that up here
00:18:19.260
let's do type and response and so for
00:18:22.740
now it's just search which is a string
00:18:25.020
so response it doesn't need to return
00:18:27.660
anything oops not value off or is it on
00:18:30.419
submit and we need to return this the
00:18:33.120
form itself so unsubmit what we let's do
00:18:36.240
handle submit because we want to do a
00:18:37.919
couple of things we figure this
00:18:40.140
um so in the actual component itself so
00:18:42.120
Handle Sub mode and that obviously takes
00:18:44.160
the event is I think from react you need
00:18:47.280
to because remember react uses synthetic
00:18:49.380
events and this would be a form event
00:18:52.320
and I always find that like super
00:18:54.360
interesting that you need to tell it it
00:18:56.100
actually comes from an HTML form as if a
00:18:59.039
form of in can come from somewhere else
00:19:00.660
the first thing you want to do is event
00:19:02.100
prevent default uh this may be a good
00:19:04.380
opportunity to introduce Zod you might
00:19:06.600
have heard about Zod like it's really
00:19:09.120
cool not even a year old like you'll see
00:19:11.760
it's almost like 23 000 Stars it's
00:19:14.820
really amazing I really like it it helps
00:19:17.400
you to do your type validation and your
00:19:20.520
writing of your schema at the same time
00:19:22.860
so once again you don't need to do this
00:19:25.380
but you can if you want I really like it
00:19:27.539
I would probably use it so npm install
00:19:30.900
Zod so Z from Zod instead of doing this
00:19:34.620
I would do const a response equals z
00:19:39.240
object so we're expecting an object the
00:19:42.299
object has a search a z and then what
00:19:46.080
you can just do is response but we're
00:19:48.179
gonna have some other things here later
00:19:49.799
I guess that have some value validation
00:19:51.900
I think you do Z infer yes and then you
00:19:55.200
do type of res when you pass the object
00:19:57.960
and then it's able to actually figure
00:19:59.460
out what the shape of this is so you
00:20:01.679
write your validation for your forms and
00:20:03.660
stuff in here and then it automatically
00:20:05.220
gives you the types as well fine so in
00:20:08.460
here what we need to do is eventually
00:20:09.600
prevent default we need to turn this
00:20:12.360
into entries so we go data we do new
00:20:16.620
form data and we pass event Target to
00:20:20.820
that so there are several ways to do
00:20:22.740
this this is the way I prefer to do it
00:20:24.480
you might actually build it so that you
00:20:27.059
have this up here and as people type it
00:20:28.919
automatically filters the list
00:20:31.440
um I actually prefer to just keep
00:20:33.600
through the kind of idiomatic way of
00:20:36.360
using forms I find that it makes it
00:20:40.260
easier to reason about your code easier
00:20:42.360
to reason about your state that your
00:20:43.980
code is in unless there's a ux demand or
00:20:47.520
a good use case for having this here and
00:20:50.100
having it be real time and as you type
00:20:52.500
it actually like filters yeah so I don't
00:20:55.380
preemptively build too much
00:20:57.360
interactivity in because it can be very
00:20:59.400
hard if you have too much of that it
00:21:01.380
becomes a bit of a mess and your code
00:21:02.820
gets very complex and so forth so I
00:21:05.160
rather generally just do it this way
00:21:06.660
until I realize that hey there's a very
00:21:08.820
big use case I had to do it the other
00:21:10.679
way so upscript you are insane okay I'm
00:21:13.860
just going to say as any
00:21:15.500
response we just take data and object
00:21:19.080
from entries uh entries data and then we
00:21:24.120
feed that into Zod for validation uh
00:21:27.660
response let's call this submission or
00:21:30.120
naming conventions are getting a bit
00:21:31.799
weird here transformed entries
00:21:34.020
transformed and then finally this is
00:21:36.480
turned into data and you can response
00:21:38.520
safe bars okay so we don't want it to
00:21:41.039
throw an error we just want it to
00:21:42.900
validate if you do regular Parts it's
00:21:44.880
going to throw a JavaScript error if if
00:21:46.919
this doesn't match
00:21:48.960
um so we're going to do save parse and
00:21:51.000
then you want to save pause transformed
00:21:52.799
and then you know that if it passes if
00:21:56.159
data doesn't have success though on our
00:22:00.419
list is console log invalid order
00:22:02.100
theoretically this should be valid
00:22:04.260
always now and so we can then assume so
00:22:06.659
then if you do that you should know the
00:22:09.179
data is how you want it let me just
00:22:11.460
let's just console log the data then
00:22:13.260
because we want to theoretically then
00:22:14.580
pass it to on submit and so oh you need
00:22:17.940
to put a name on it so I need to text
00:22:20.340
field name so the name here I need to be
00:22:22.919
searched success Okay cool so then we
00:22:25.919
can destructure data from it validation
00:22:28.380
yeah I'm running out of names for things
00:22:30.720
now and then on subnet this is maybe a
00:22:32.940
contrived example but let's actually say
00:22:35.039
search can be nothing but if you want
00:22:39.240
something it needs to be a minimum of at
00:22:41.520
least three you can't search for like
00:22:43.620
you need at least three things so it
00:22:45.780
needs to be nothing or three things so
00:22:47.580
let's do a minimum of three unless I
00:22:49.679
have message search needs to be empty or
00:22:54.240
at least three characters let us in here
00:22:58.080
add our actual alert let's grab an alert
00:23:02.580
from over here alert let's just do
00:23:05.640
styled alert to give it a bit of heading
00:23:07.799
above styled and we pass alert in and we
00:23:10.559
just say give it a bit of margin at the
00:23:12.480
top one rim and we also need to pull in
00:23:15.000
styled if you do a lot of like complex
00:23:17.520
forms and stuff you can even pull in
00:23:19.380
some actual form specific libraries so
00:23:21.840
you know something like formic like you
00:23:24.000
use this in addition with something like
00:23:26.580
uh Zod this just handles like form
00:23:28.799
submissions and stuff for you this is
00:23:31.140
simple enough that we don't need a
00:23:32.640
separate entire form library but I work
00:23:35.280
on projects where we pull in libraries
00:23:37.260
that help us manage forms styled alerts
00:23:39.780
so here we go and we obviously don't
00:23:41.460
want it to be a success we want it to be
00:23:43.799
severity and we wanted to just be a
00:23:47.159
warning all right how do we get the
00:23:48.900
error then success is false then we need
00:23:51.659
to get the error itself let's do
00:23:54.120
validation dot error okay let's try
00:23:56.820
again all right and go to small message
00:24:00.360
okay so we can get the first error that
00:24:03.900
I always usually just show the first
00:24:05.700
error
00:24:07.140
um do know is that at this point we
00:24:10.799
should be able grab error from
00:24:13.440
validation and it should be a Zod error
00:24:16.380
so error turn error issues it looks okay
00:24:20.580
issues let's see I think we can go
00:24:22.740
message okay it works now so here we
00:24:25.440
have to decide do we want to lift the
00:24:27.480
state like who is going to be
00:24:29.280
responsible for handling the errors here
00:24:31.980
is it going to be the app is the app
00:24:34.140
gonna know that there's an error in the
00:24:36.120
filters or is the filter modal just
00:24:38.640
gonna actually handle its own errors and
00:24:41.700
the rest of the app doesn't even need to
00:24:43.140
know there's an error here and there is
00:24:45.240
no right answer here but what I like to
00:24:47.580
do is I I prefer to handle it in here
00:24:50.100
and on submit we just assume that like
00:24:53.460
it worked and there were no errors so on
00:24:55.740
submit doesn't fire unless there are if
00:24:58.980
there are any errors okay but like this
00:25:00.720
is an architectural thing like and it's
00:25:02.340
up to you to figure out how you want to
00:25:04.020
do this but so I would actually just do
00:25:06.360
the error handling in here so I would go
00:25:09.299
and that would just be error and save
00:25:12.539
error and it starts as null but now the
00:25:15.539
problem is it's just going to think it
00:25:17.340
should always just be null so I need to
00:25:19.080
tell it so I use it generic here and I
00:25:21.120
tell it it can be a string or null these
00:25:23.940
angular brackets tell it like set a
00:25:26.100
generic on it so now it knows it can be
00:25:28.559
string or null but it starts as null I
00:25:31.860
actually go then you know if there is an
00:25:34.500
error and and show that by default it's
00:25:37.320
not going to show that unless there is
00:25:39.000
an error here if this is the case then
00:25:41.400
we just return set error we don't
00:25:44.039
continue with any of this we just set
00:25:46.080
the error to whatever like Zod returns
00:25:48.419
and what's really cool about this like
00:25:49.679
this was now a bit of a roundabout way
00:25:51.299
of doing it but now whatever we add here
00:25:53.640
we'll just automatically turn in errors
00:25:55.740
so now we just configure our validation
00:25:57.779
up here we've set up the actual
00:25:59.580
infrastructure that takes whatever Zod
00:26:01.860
spits out and shows it on the screen
00:26:03.659
this is maybe a bit sudden maybe you
00:26:06.299
wanted to animate in and this is maybe
00:26:08.100
where we can pull in react spring
00:26:09.840
generally it's a good idea to animate
00:26:13.140
errors just to draw a bit of attention
00:26:15.000
to it so that someone aims it I've
00:26:17.279
typically been on sites where I
00:26:19.260
submitted and it wasn't clear that the
00:26:21.120
error appeared it appeared like a little
00:26:22.860
corner or something and I didn't see an
00:26:24.240
animation or whatever and I'm like why
00:26:25.559
does it not want to submit let's just
00:26:26.940
quickly install react spring what we
00:26:29.400
want to do is we want to pull in react
00:26:31.260
spring react spring forward slash web we
00:26:34.380
use spring use Springs from and two and
00:26:37.860
let's just do opacity one and remember
00:26:40.080
this is declarative from 0 to 1 animated
00:26:43.980
so we always show it but it's hidden
00:26:47.220
let's wrap it in an animated div
00:26:50.159
animated but the opacity is zero if
00:26:52.679
there are no errors and so this would be
00:26:55.260
Styles I think and we can just pass in
00:26:57.120
Styles like that style name it the same
00:27:00.600
thing up here this actually create a
00:27:02.220
quick hook so let's say use filters if
00:27:04.799
it gets big enough I sometimes even swap
00:27:07.200
it out into its own file take all of of
00:27:09.779
this and put it in a hook to turn
00:27:12.299
whether there's an error or and the
00:27:15.120
style or the use spring and handle
00:27:18.000
submit now we're actually nicely
00:27:19.620
encapsulating all of this pass props in
00:27:22.380
there and the prop is just boltons to
00:27:25.260
use filters and then we have a nice
00:27:27.059
component here and with this we just
00:27:29.100
pass props indirectly error and also
00:27:31.919
that install so our actual rendering is
00:27:34.679
now completely separated from the
00:27:36.840
filters and what is going on here cannot
00:27:40.140
find name style and that should fix it
00:27:42.960
up for us all right okay so there's
00:27:44.640
where it will show that wasn't great the
00:27:47.700
text field we can say I think full width
00:27:50.580
yes just to have it like span all the
00:27:52.559
space what we also want is if this
00:27:54.960
succeeds then we want to get rid of the
00:27:57.360
error if validation succeeds set error
00:28:00.360
to null so what we want to do is if
00:28:02.940
there is an error the opacity should go
00:28:06.600
from 0 to 1. let's also just make this a
00:28:10.860
bit wider sort of styled I'm just going
00:28:13.440
to call it styled content Max it out at
00:28:15.720
like 20 Rams just so we don't have that
00:28:17.880
jumping effect yeah I think we need to
00:28:19.799
do it this way let's just do content
00:28:21.539
like this we need to wrap all of that
00:28:23.640
stuff in this oops and it needs to be
00:28:25.679
just a regular div okay so let's just
00:28:27.600
force it for now to be a width of 20 RAM
00:28:31.980
and also we maybe want the space to just
00:28:35.159
expand a little bit so we're gonna have
00:28:36.840
to use dull components to do that
00:28:38.900
installed a look height let's go 0.5 Rim
00:28:43.919
by default and then we can just do here
00:28:47.059
error and error is just a spring or it's
00:28:50.279
null so we also pass a generic once
00:28:52.440
again telling it what can be passed to
00:28:54.360
style alert to interpolation in here we
00:28:56.460
do props and props dot error and if
00:29:00.659
there is an error to Ram otherwise it's
00:29:03.900
0.5 obviously it's going to complain
00:29:06.360
because we need to pass that directly to
00:29:08.220
it so error we handled that with the
00:29:10.919
style component Auto let's actually do
00:29:13.620
this like really small yeah I don't know
00:29:15.720
why my typescript is so slow uh let's do
00:29:18.059
one uh cool and okay so here's another
00:29:20.880
thing so you'll see that when it does
00:29:23.399
mount it starts as that it actually then
00:29:26.700
goes to the opacity so we might need to
00:29:29.279
use a reference here so you might have
00:29:32.279
encountered react ref and this allows us
00:29:34.740
to keep track of values that don't
00:29:36.659
affect rendering use ref is starting is
00:29:40.679
starting as true if it is starting or
00:29:44.760
it's an error then it should be zero
00:29:48.740
unused effect so when the component just
00:29:52.020
mounts we just change is starting
00:29:54.480
current pulse so this is a pretty
00:29:56.880
Advanced react so I'm hoping like you
00:29:59.279
understand enough of react at this point
00:30:01.620
to understand what I'm doing here with
00:30:03.720
the ref and so forth if you've been
00:30:06.120
wondering what do you even use ref4
00:30:08.399
here's a example of where it might be
00:30:10.559
useful so we want to keep track of this
00:30:12.960
value and we want to update this value
00:30:14.340
but we don't want it to re-render when
00:30:16.440
we update this value because we also
00:30:18.179
needed to tell it that it can actually
00:30:20.039
be zero as well let's say uh men of 0 or
00:30:26.399
3 Min and Max or Zod Mt is valid uh
00:30:32.720
non-empty automaker field optional
00:30:36.200
refine using emails you could do or okay
00:30:40.260
there you go so we do all of this so we
00:30:42.419
say optional or electoral empty string
00:30:45.299
with a placeholder in here that says any
00:30:48.480
and just shows any now that on submit
00:30:51.120
should also fire so what we can do is
00:30:53.820
let's quickly set up our stories filters
00:30:58.080
okay so filters just has unsubmit at the
00:31:01.320
moment in storybook by default anything
00:31:05.220
that has I think a prop that starts with
00:31:07.919
on automatically fires uh you don't need
00:31:11.340
to mock that yes anything that starts
00:31:14.159
with on automatically gets logged here
00:31:16.860
when you fire it so this is what's
00:31:18.539
really neat about storybook so anything
00:31:20.460
that you post a component that starts
00:31:22.200
with on that it shows if it fires and so
00:31:25.140
if we go there it doesn't fire okay so
00:31:27.240
we can click apply as many times as we
00:31:29.159
want it doesn't fire but then if we fill
00:31:31.799
that fires again so this is working 100
00:31:33.720
as expected