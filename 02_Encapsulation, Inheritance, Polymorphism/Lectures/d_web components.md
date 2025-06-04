Please write clear and comprehensive lecture notes and lesson content for this lecture:

00:00:00.000
but now for all intents and purposes you
00:00:03.300
shouldn't know how to actually use a
00:00:07.500
class instead of a factory function both
00:00:09.660
of them achieve the exact same thing it
00:00:12.120
is just a matter of personal preference
00:00:13.860
for me personally I prefer Factory
00:00:16.199
functions
00:00:17.580
um I also find them a bit more idiomatic
00:00:20.100
in terms of the way I write JavaScript
00:00:23.520
in the end classes actually are just
00:00:26.519
syntactic sugar on top of actual
00:00:28.260
functions and so let's just quickly go
00:00:30.660
to tasks and let's just look at how we
00:00:33.239
would replace our tasks by using a class
00:00:37.260
and I'm just gonna copy this just so I
00:00:41.340
have a backup or reference so we would
00:00:44.399
just say task instead of create task
00:00:46.440
once again create is used to indicate a
00:00:49.379
factory function then over here we will
00:00:52.860
just export class task and with the
00:00:56.879
syntax we can just immediately create
00:00:58.920
the ID and that like this I wouldn't use
00:01:01.920
State like this I would just put all of
00:01:03.960
this stuff directly in it and so all of
00:01:06.840
this would just be in the Constructor so
00:01:09.299
as mentioned you can still keep this
00:01:11.040
outside of the class and over here we
00:01:13.979
just need to say this IDE same here this
00:01:16.799
ID here we can just go completed is this
00:01:21.060
completed and these are actually going
00:01:24.780
to be so we're going to put this on the
00:01:27.000
Constructor itself okay and it's
00:01:29.939
actually just destructure that right and
00:01:33.540
so instead of making this an object that
00:01:36.900
gets returned this would actually just
00:01:38.340
be on it itself and instead of getting
00:01:41.460
this from the state and also we need to
00:01:44.040
remove the commas in classes you write
00:01:46.799
it like this without the commas because
00:01:49.079
we want to use Getters and Setters and
00:01:51.479
as mentioned in classes you can't have a
00:01:53.880
get and Setter with the name as that is
00:01:57.780
the same as an actual property in the
00:02:00.540
class so we let's set these to private
00:02:03.540
and then the Getters and Setters just
00:02:05.820
mediate how we use these and return
00:02:08.580
these and so yeah so I'm just working my
00:02:11.099
way through these now and just replacing
00:02:14.280
everywhere where I need to we also need
00:02:18.599
to add title and it's going to be
00:02:21.120
undefined and also
00:02:24.000
urgency so if we want to create private
00:02:27.000
properties we need to create them first
00:02:31.020
and then in here we can assign them so
00:02:34.200
we just extract the ones that we need to
00:02:36.599
get from The Constructor and just
00:02:39.120
placing them directly in there okay cool
00:02:41.940
and then we can also once again like you
00:02:44.700
don't necessarily create an interface in
00:02:46.739
this manner so what you instead do do is
00:02:49.860
you mostly set that on in the class
00:02:52.620
itself
00:02:54.060
um generally you don't make a separation
00:02:56.599
between
00:02:58.220
your interface and the classes
00:03:01.560
themselves the class almost is the
00:03:03.780
interface so as mentioned you might
00:03:06.300
actually prefer this right so this is
00:03:10.260
all good so this would also just be this
00:03:13.140
and let's continue working our way down
00:03:15.659
here just swapping out all of these we
00:03:18.300
never actually picked this up in our
00:03:19.560
previous example but seems like we never
00:03:21.300
actually set the urgency view okay and I
00:03:25.860
think that is that there's our class so
00:03:29.940
generally Airbnb es learned actually
00:03:33.540
says that
00:03:35.900
do this in here it's probably an error
00:03:39.560
but in most cases it would be but in
00:03:43.019
this case we we actually know that that
00:03:45.959
is actually the behavior that we want so
00:03:47.879
we can just go eslant uh eslint disable
00:03:51.599
next line class method use this so it's
00:03:56.940
gonna emit that it so it just assumes
00:04:00.299
whenever you create a method you
00:04:02.459
actually need to do use this in it at
00:04:06.299
some point unless you specify otherwise
00:04:08.720
right so what we can do now we actually
00:04:11.819
made the change in the backup so let me
00:04:14.280
just make this the actual real one and
00:04:16.620
it's actually call a task as well like
00:04:20.100
this from here let us just import task
00:04:23.120
and import the actual class and then
00:04:26.280
what we would do is we just say new task
00:04:30.660
like that and then over here we need to
00:04:33.660
do data and new task and just pass data
00:04:37.860
into it and so let's have a look and for
00:04:40.800
all intents and purposes our Behavior
00:04:42.840
should still be exactly the same we are
00:04:46.500
just literally using a different way of
00:04:49.199
creating the same thing so let's give it
00:04:51.960
a go right save there we go exactly the
00:04:56.280
same behavior we're just using a class
00:04:58.080
instead of a factory function and and
00:05:00.720
these are actually closer under the hood
00:05:03.360
than you think I'm going to keep these
00:05:05.460
as just functions up here you can even
00:05:07.440
make them classes yourself if you want
00:05:09.419
to so what classes allow us to do and
00:05:12.780
and that is because the Dom itself is
00:05:14.759
built on this prototype model that
00:05:18.000
actually is underneath classes as well
00:05:20.360
we can go plus and let's just say
00:05:24.560
example extends and we go HTML element
00:05:29.520
okay so we can actually extend an actual
00:05:32.699
Dom node there's only one thing that is
00:05:35.400
needed in this and that is connected
00:05:37.680
callback and connected callback you
00:05:39.900
effectively just tell this HTML element
00:05:42.479
what that you just created now what it
00:05:45.419
needs to do when it actually gets added
00:05:47.400
to the Dom and we can just say this in a
00:05:51.240
text hello clones uh base HTML element
00:05:55.740
with no semantic meaning so something
00:05:57.960
like a div or a span but even higher
00:06:00.360
level than that literally just a vanilla
00:06:02.340
like plain HTML element with nothing and
00:06:05.580
we just say when we add this to the Dom
00:06:09.120
just put the word hello inside it
00:06:11.639
automatically now we need to register it
00:06:14.220
so let's do custom elements Define for
00:06:18.000
you'll be provided with a name and so
00:06:20.280
with custom elements you always need to
00:06:23.460
have a dash in them so I can't go
00:06:25.139
example I need to go you know for
00:06:27.300
example skulk or whatever I'm going to
00:06:31.139
speak about that in a second why that's
00:06:33.060
the case and let's just pause this in
00:06:35.460
here so let's just grab that let's put
00:06:38.639
it in our scripts file so it actually
00:06:40.380
runs now we can actually do something
00:06:42.600
amazing let me show you we can actually
00:06:44.759
go in here and we can actually use
00:06:47.520
example skulk as if it's an actual HTML
00:06:50.940
element let's do three of them hello
00:06:53.100
hello hello hello this is really cool so
00:06:56.160
you can probably imagine what we can do
00:06:58.560
here now is we can actually create this
00:07:01.860
as a single task like that and actually
00:07:04.740
pass values to it as if it's an HTML
00:07:07.800
element and that is how we actually get
00:07:10.440
full on encapsulation and we get that by
00:07:13.139
means of something called The Shadow Dom
00:07:15.000
I'm instead of explaining to you what
00:07:17.280
the shadow Dom is let me show you what
00:07:19.979
it is so there's already this thing in
00:07:22.919
HTML called The Shadow Dom so as an
00:07:26.039
example it's up here let's say we're
00:07:28.380
embedding a video component and that has
00:07:31.020
controls okay and let's have a look at
00:07:33.300
that so we we didn't include anything
00:07:35.039
but you'll see here is all of this stuff
00:07:37.919
okay
00:07:39.000
but if we inspect it it's completely
00:07:41.639
encapsulated we we can see there are
00:07:44.160
some things you know there's like a play
00:07:45.960
button there's like all of this stuff
00:07:48.240
there's some buttons only exposed to us
00:07:51.300
as a video this is we can't go deeper
00:07:53.759
into it so this is behind something
00:07:56.099
called The Shadow Dom in other words it
00:07:58.680
has its own little Dom almost like this
00:08:01.560
page has but we can't access it but we
00:08:04.919
can interface with it so you know if we
00:08:06.960
remove controls it's no longer going to
00:08:08.880
show the controls if we put it back you
00:08:11.460
know it's showing the controls we can
00:08:13.740
say you know things like autoplay and
00:08:16.919
and things like that so we can pass it
00:08:18.780
so this is pretty much like an interface
00:08:20.819
you know as we had previously but it's
00:08:23.400
all the HTML the CSS The Styling for
00:08:25.620
this is all like in a little bundle so
00:08:28.020
how do we create something like this
00:08:29.759
this is just fully encapsulated that we
00:08:31.860
can just Chuck in in this manner so
00:08:34.799
let's do single cost okay
00:08:37.440
so what I usually do is I separate just
00:08:40.559
regular modules from actual components
00:08:42.839
or components are things that have HTML
00:08:44.760
and CSS and all of that in it so
00:08:47.220
components and I usually just name the
00:08:50.820
component how I would actually call it
00:08:52.860
in HTML so single task JS so let us just
00:08:58.140
start out doing the basic HTML so we can
00:09:02.640
create it in our class in in the way
00:09:05.880
that we do over here the problem is that
00:09:10.380
um it's not the end of the world it's
00:09:12.839
fine but we can get a lot of performance
00:09:14.880
benefits by actually creating a template
00:09:17.940
putting it in the Dom and then just
00:09:20.100
cloning that template instead of every
00:09:22.740
time taking a string and turning that
00:09:25.320
string into an actual Dom element let's
00:09:28.080
grab all of this and then in here so
00:09:30.839
before anything else if we pull in this
00:09:33.060
component let's create a template so
00:09:35.279
const and let's just call it template so
00:09:37.800
and a template is actually a HTML
00:09:40.560
element you can actually create your
00:09:43.260
template like this as well in your HTML
00:09:45.600
just like this and some of the
00:09:47.640
Frameworks like View and so forth
00:09:49.140
actually do this so you can do it like
00:09:51.300
that as well I prefer having everything
00:09:54.000
in my in my component file so I create
00:09:56.580
my template in a HTML and I just put all
00:10:00.360
of this in there okay and obviously now
00:10:02.279
we need to express this as HTML as well
00:10:04.920
so let's just get rid of this for now so
00:10:08.220
we are just gonna have an Li okay and on
00:10:12.180
that we're gonna have task let's just
00:10:14.399
get the plain HTML without the data
00:10:17.279
attributes or any of that info we can
00:10:19.320
just do this as well okay and once again
00:10:22.560
um let me just set my spaces to 2 over
00:10:25.440
here uh prettier is going to have a hard
00:10:28.800
time actually formatting this for us so
00:10:31.200
we might need to do a bit of formatting
00:10:33.899
ourselves we also want to put our CSS in
00:10:37.080
here and you might be like but ours
00:10:39.600
actually taught that we shouldn't do
00:10:41.040
inline Styles and yes under normal
00:10:43.800
circumstances but when you're using
00:10:46.200
templates and and this type of thing the
00:10:48.180
browser actually gets really good at
00:10:51.420
actually caching this so the only caveat
00:10:54.300
being that as long as you don't put
00:10:56.519
anything dynamic in here as long as this
00:10:59.640
template is just just a string and you
00:11:02.459
don't have any interpolation or anything
00:11:04.019
in here it's going to be lightning fast
00:11:06.839
so we can actually move all the task
00:11:09.360
specific stuff out of here and now we
00:11:11.519
also don't even need to use Bim because
00:11:13.740
this is only if we use the shadow Dom
00:11:16.200
this is only referencing this thing
00:11:19.680
itself so we can actually get rid of the
00:11:23.100
name spacing that only gets applied to
00:11:25.260
what is in the template it can't style
00:11:27.060
anything outside of the template just
00:11:29.579
one thing we will need to just manually
00:11:32.940
add box sizing border box because for
00:11:36.660
all intents and purposes this is a
00:11:39.420
completely new Dom it's a shadow Dom but
00:11:41.519
it's a it's a new Dom so inside this
00:11:44.940
component and so we also need to tell it
00:11:47.160
how to do the Box sizing Behavior okay
00:11:49.680
but so here we go okay so we have our
00:11:52.260
template there so let us then create our
00:11:54.959
class and let's just call our class a
00:11:57.839
single task and I mentioned that I will
00:12:01.500
I would talk about why the dash so the
00:12:04.680
reason for the dash is you can imagine
00:12:07.380
that the problem is let's say I create
00:12:10.860
something called single task and this is
00:12:13.920
fine and all and have this custom
00:12:15.240
component and in three years
00:12:17.300
w3c decides hey we actually want to add
00:12:21.720
something new to HTML we want to add
00:12:23.640
this thing called single task
00:12:25.380
now we have a big problem and that
00:12:27.600
problem is that now my custom thing that
00:12:29.700
I created actually conflicts with
00:12:31.860
something that is actually now native in
00:12:34.560
the Dom in HTML so the way that this is
00:12:38.040
solved is at the moment there are no
00:12:41.100
HTML elements that have dashes in them
00:12:43.800
so you can think about Dove you know you
00:12:45.540
can think about Li you can think about
00:12:47.700
IMG at this moment in time there's not a
00:12:51.720
single native HTML element that has a
00:12:53.639
dash in it so what the w3c decided is I
00:12:57.180
said that they are going to commit never
00:13:00.480
adding anything that has a dash in it
00:13:03.240
that means that any words that have a
00:13:06.420
dash in it is now completely reserved
00:13:08.579
for just custom elements so we can
00:13:11.279
create custom elements knowing that
00:13:13.320
there's never going to be anything with
00:13:15.779
a dash that is possibly going to
00:13:17.519
conflict so because of that
00:13:20.579
um customer elements do require to have
00:13:23.100
a dash in them so we can't go uh custom
00:13:25.740
elements Define because tomorrow they
00:13:29.519
might add something called tasks so
00:13:30.899
let's just call it single task what a
00:13:33.000
lot of people do is they actually prefix
00:13:34.500
it with the name of the project so so
00:13:37.019
for example if this is Twitter they
00:13:38.579
would go t w t preview or whatever and
00:13:42.839
then they had something else that is you
00:13:44.579
know we might even go to do
00:13:47.279
um preview and then you know to do list
00:13:51.120
um but let's just for now call it single
00:13:52.860
task we also need to add a class to it
00:13:55.320
and that is just the single task class
00:13:57.660
here all we do is we do connected
00:13:59.940
callback so connected callback buyers
00:14:02.700
when it gets added to the Dom and all
00:14:05.760
that we want to do is we want to do a
00:14:07.920
couple of things so we want to create a
00:14:09.600
shadow Dom so I spoke about the shadow
00:14:11.339
Dom so the shadow Dom is effectively
00:14:13.560
kind of an encapsulated Dom with its own
00:14:15.839
HTML and CSS that you can't access from
00:14:19.139
outside so it's fully encapsulated so I
00:14:21.899
usually just assign it to a property and
00:14:24.420
I just usually call it in there and then
00:14:26.760
I go this attach Shadow and then you
00:14:31.200
just need to give it a mode I'm not
00:14:33.060
going to go into this too much but we
00:14:35.040
want to have the mode be closed meaning
00:14:37.860
you can't access it from outside and
00:14:40.500
also we need to extend HTML elements so
00:14:43.680
remember that that's this is why we got
00:14:45.720
that error because there is no attached
00:14:47.639
Shadow unless we actually because this
00:14:50.220
comes along with HTML element so instead
00:14:53.339
of actually assigning this to the inner
00:14:55.620
HTML now of the actual component itself
00:14:59.220
we have to assign it to Inner to its
00:15:01.980
actual Shadow Dom but we are no longer
00:15:03.959
going to just pass a string into the
00:15:06.720
inner HTML in fact we're just going to
00:15:09.120
take this template and just clone it
00:15:11.579
into the component meaning that it
00:15:13.260
doesn't need to parse it and render it
00:15:15.180
as Dom elements we have those Dom
00:15:17.579
elements already and it is just going to
00:15:20.459
actually clone it and pop it in here so
00:15:23.459
if you remember correctly the this
00:15:25.920
should maintain a reference to this
00:15:28.139
template element so we don't need to
00:15:29.880
query for it again we can just straight
00:15:32.699
up pop it in here what we are doing here
00:15:35.339
is we're saying this inner okay which is
00:15:37.740
the shadow Dom that we created and we
00:15:39.839
are pending something to that's a pen
00:15:42.060
child and this is just template dot
00:15:44.820
content this is going to take the
00:15:46.320
content from this template and it is
00:15:48.959
just going to pop it in there what we
00:15:50.699
need to do now is we obviously need to
00:15:54.000
let's get rid of this we obviously just
00:15:56.399
need to import that component now so
00:15:58.800
we're just importing the registration
00:16:00.360
and all of that so we're actually just
00:16:02.339
importing the code and so the code needs
00:16:05.699
to run we're actually not using any
00:16:07.199
variables or anything from it so we just
00:16:09.120
do it like that so it just runs the
00:16:11.220
registration and everything so that
00:16:13.620
means we should theoretically now be
00:16:16.199
able to go
00:16:18.000
so let me also just disable all the
00:16:20.339
other other code that we have in here
00:16:22.320
and and just before we actually never
00:16:24.600
updated this class so let's just let's
00:16:27.360
update this to wrapper all right let's
00:16:29.100
have a look now and here we go all right
00:16:31.320
so now we need to do the exact same
00:16:33.779
thing where we actually bind this to the
00:16:37.740
actual values in the class so we have
00:16:39.839
the title we have all of that but how do
00:16:42.180
we also pass that from outside so
00:16:44.279
theoretically we want to go title hello
00:16:47.759
with booleans you actually don't
00:16:50.820
actually in HTML say so you can think
00:16:53.820
about something like disabled you don't
00:16:55.380
say disabled you know true or false you
00:16:59.279
just say disabled so in the same way we
00:17:01.680
just say completed it's just it is there
00:17:03.779
or it isn't and then the same with you
00:17:06.059
if there's no du we can just so let's
00:17:08.880
just say there's a title it's hello and
00:17:11.640
it is completed and let's just add
00:17:14.579
another one below that and let's
00:17:16.199
actually just say wash clothes make bed
00:17:19.199
thing actually you'll see that it only
00:17:21.780
has one and I'll I actually missed
00:17:24.780
something and I'll I will explain to you
00:17:27.419
why now so what is actually happening
00:17:30.480
here is we're actually just moving the
00:17:33.419
same template around every time because
00:17:36.240
as you remember this is a reference to
00:17:38.760
it we're not re every time we do this
00:17:42.120
every time I append it we're not copying
00:17:44.700
it we're just moving the same one around
00:17:46.559
because it's the same reference so what
00:17:48.600
we actually need to do is we actually
00:17:50.100
need to clone it duplicate and so we do
00:17:53.340
template content flow node so like that
00:17:56.640
and then we pass the duplicate and this
00:17:59.280
is actually
00:18:00.299
nothing not
00:18:02.039
own it but this is also something we
00:18:03.900
actually already need to do in the
00:18:05.280
Constructor as well Constructor and here
00:18:08.520
and we need to call something called
00:18:09.840
super I will explain in a minute what
00:18:12.299
super is so let's just de-structure
00:18:15.000
content from the template and then this
00:18:18.419
inner the pen child content and clone
00:18:22.799
node true so now if we remove this there
00:18:26.640
you go now so now we have three so we
00:18:28.380
need to actually clone it otherwise
00:18:30.299
we're just moving the same one around
00:18:32.160
every time and another thing that people
00:18:34.740
actually do because what happens a lot
00:18:37.080
of times is you create all your stuff up
00:18:39.539
here and you create your class all of
00:18:41.580
that and then you forget specifically
00:18:43.559
when this gets very long and this gets
00:18:45.480
pushed all the way down you forget to
00:18:47.820
actually set this over here so what I've
00:18:50.220
seen a lot of people do which I actually
00:18:52.380
prefer myself just because it makes it
00:18:55.380
harder to accidentally forget to update
00:18:58.200
this is you actually wrap the class so
00:19:01.500
you don't give it a name and you just
00:19:03.539
wrap it directly like this inside the
00:19:06.900
Define comma separated you can even put
00:19:09.179
a spacer that just ensures that you
00:19:11.580
remember to update this especially if
00:19:14.100
you just copy and paste to create a new
00:19:15.840
one but it doesn't matter which way you
00:19:18.179
do it I've just seen people do this I
00:19:21.240
actually prefer that a bit so what we
00:19:23.160
want to do now so then we want to grab
00:19:26.400
the attributes and put them actually on
00:19:30.299
here classes don't allow you to have as
00:19:34.380
fine tuned control over your interface
00:19:38.400
as something like a factory function
00:19:40.140
does I just start everything as private
00:19:42.900
until manually actually say hey this is
00:19:46.320
actually not private anymore and even
00:19:47.940
then I'll probably just handle it and
00:19:49.980
manage it through Getters and Setters so
00:19:52.020
we have title and then we have completed
00:19:54.840
we can actually in here already
00:19:57.980
grab the attribute that gets passed okay
00:20:01.799
so we can actually set it in here so we
00:20:04.260
can say this get attribute title and
00:20:07.679
this get attribute completed and let's
00:20:09.900
actually just log them here just to show
00:20:13.260
that it actually grabs it from the HTML
00:20:16.080
right so as you can see wash clothes
00:20:18.419
make bed do homework so actually already
00:20:20.460
grab it from the HTML in here and we
00:20:23.280
just put it directly in there so one
00:20:26.700
thing though to keep in mind that
00:20:29.340
everything in HTML is a string so even
00:20:32.580
if you go value that is a string you
00:20:35.520
need to parse it in the component itself
00:20:37.799
and so theoretically also when you do
00:20:39.900
this it is completed equals empty string
00:20:43.080
what that means is when we're passing
00:20:44.880
things like this we actually just need
00:20:46.860
to check is it anything except null
00:20:49.799
because by default if you don't include
00:20:52.140
it it is actually null so that means if
00:20:55.020
it's any if it's not null then it's
00:20:57.360
actually true so these it's actually
00:20:59.580
null okay over here it's not null it's
00:21:03.120
an empty string so so now that we have
00:21:06.539
this when it gets rendered we actually
00:21:08.700
want to set what's inside these things
00:21:10.679
based on this okay so we have our
00:21:13.380
Constructors here and so now we do
00:21:15.960
connected callback so connected callback
00:21:18.000
once again runs them when this is now in
00:21:20.640
the Dom so we want to set the shadow Dom
00:21:23.580
based on so so what I actually do to
00:21:27.780
make my life a bit easier is I actually
00:21:30.539
also have an elements yeah which is just
00:21:34.500
an object so I don't need to have to
00:21:36.960
document query this stuff all the time
00:21:39.360
so let's just use data check it's not
00:21:43.080
make the same mistake here again let's
00:21:44.700
do data title data delete
00:21:47.520
so remove the leads actually
00:21:49.940
delete is actually a reserved word in
00:21:53.280
JavaScript so actually want to try and
00:21:54.720
stay away from it so it said data remove
00:21:57.120
instead add my elements so by this time
00:22:00.360
they are not going to exist yet but I am
00:22:02.460
going to create them so let's do checks
00:22:05.100
so by this time all of them are
00:22:06.900
undefined we haven't actually found them
00:22:09.179
yet because they haven't been added yet
00:22:11.100
and then over here we add them so this
00:22:13.919
elements and we set them so this will
00:22:16.679
just be this inner and we also want to
00:22:19.500
make in a I didn't even think about this
00:22:21.539
but obviously in there needs to be a
00:22:23.159
private thing otherwise anyone can just
00:22:25.440
grab the shadow root and do anything
00:22:27.480
with it so in all these cases we want to
00:22:30.000
query the shadow Dom and we can even
00:22:32.700
bring or get HTML element in here so
00:22:35.460
let's actually do that for that extra
00:22:37.500
level of security in terms of guarantees
00:22:41.960
outputs and so we want to say get HTML
00:22:46.140
and this will be title so the data
00:22:50.580
attribute will just be title and the
00:22:53.340
target will just be this inner all right
00:22:56.520
so let's just copy this to all of them
00:22:58.740
and also an interesting thing here is
00:23:01.980
that it actually gives us a warning
00:23:05.460
um and it says that it's not a Sim
00:23:08.280
element but it's actually shadow root so
00:23:10.919
for all intents and purposes these
00:23:12.720
should work the same so all that we can
00:23:14.580
do is we can say it can be an HTM
00:23:17.039
element or a shadow root so we can just
00:23:19.320
pass any of these two it should work for
00:23:21.780
either of them so now that we have our
00:23:23.640
elements this is going to be a bit
00:23:24.840
easier so all that we can do is we can
00:23:27.600
say this elements title equals this
00:23:32.220
title so whatever was set to title and
00:23:35.159
then this elements check equals this
00:23:39.360
completed and so let me just add my Js
00:23:43.080
up here and the reason is we need to say
00:23:46.080
in a HTML and also it didn't warn us
00:23:49.440
about this even though we have TS check
00:23:52.260
like automatically being applied to
00:23:54.000
everything because we never we need to
00:23:58.020
add our types here so let's just
00:23:59.460
actually do that so this can be a string
00:24:02.400
and only a string is a string and can
00:24:04.860
only be a string this is a pool and it
00:24:08.880
can only be a Bool elements so this can
00:24:12.840
be undefined or
00:24:15.659
um an HTML element and that is the case
00:24:18.539
for all of these so now it gives us a
00:24:21.120
because obviously we can't assign this
00:24:22.740
to an HTML element so if we did that
00:24:25.559
properly from the start as I told you
00:24:28.260
guys you should and I I didn't follow my
00:24:30.480
own advice Shadow root who would have
00:24:33.179
gotten this warning so let's say in a
00:24:34.919
text answer this would also be checked
00:24:38.280
and so in this case we have the same
00:24:40.320
problem again we can check over here if
00:24:44.520
this element's check is not instance of
00:24:47.640
input HTML input element then throw an
00:24:52.080
error throw a new error required to be
00:24:56.220
input element all right so now we get
00:24:59.340
that because checked should be on all
00:25:03.000
inputs so we know that for a fact and we
00:25:05.760
know this is an input but why is it not
00:25:08.340
setting that so let's console log and
00:25:10.679
see what this completed is let's have a
00:25:12.659
look in our console are required to be
00:25:15.240
input elements so why does this not go
00:25:18.000
all the way up here well technically
00:25:19.740
because it's not part of the Dom it's
00:25:21.600
its own Dom so unfortunately all events
00:25:25.620
or errors everything it's almost like as
00:25:27.659
if it's its own little web page in here
00:25:30.360
so obviously it never gets picked up by
00:25:32.580
this because this is only for the main
00:25:34.799
Dom it's not for the shadow Dom in here
00:25:37.200
if I'm these are the type of mistakes
00:25:40.080
that I make if I'm talking while I'm
00:25:41.580
coding because it's very hard to do both
00:25:44.059
hey all right okay what's also cool is
00:25:48.419
we can do this but we can also
00:25:50.640
programmatically create these things so
00:25:52.919
we can even go const task and we can say
00:25:56.880
you know document create element and we
00:26:00.120
can create single task because
00:26:02.400
theoretically it's now an actual HTML
00:26:04.500
element that we can use in the same way
00:26:06.120
that we can create a div or whatever
00:26:07.679
let's just log that to actually confirm
00:26:10.440
that that is the case hey and check here
00:26:12.600
single task another thing is if we go on
00:26:15.960
here you will see that if I open the
00:26:20.820
browser Chrome kind of has a bit of a
00:26:24.179
hack that allows me to actually look
00:26:26.640
inside the shadow Dom and it's usually
00:26:29.460
Shadow Dom's usually indicated by this
00:26:31.980
and you'll see actually it says here
00:26:33.779
Shadow root so in theory the JavaScript
00:26:37.919
doesn't have access to the inside of
00:26:39.840
this but just for debugging purposes and
00:26:42.299
so forth Chrome actually allows me to go
00:26:44.279
actually and look in it and I can go you
00:26:47.100
know just for debugging purposes but to
00:26:50.159
indicate this you know if I try and find
00:26:52.440
class wrapper so let's just do console
00:26:55.919
log document query selector analysis dot
00:27:00.419
wrapper so look for class wrapper let me
00:27:02.940
console log that null it doesn't exist
00:27:05.279
because it doesn't it can't go into the
00:27:07.860
shadow Dom but this is just to help with
00:27:10.020
debugging and so forth it kind of gives
00:27:11.820
us a bit of a cheat code to go in there
00:27:13.919
all right so let us create our component
00:27:16.500
for adding so copy and paste from single
00:27:20.580
task just so we can reuse this again so
00:27:23.400
let us go in adding over here let's get
00:27:25.919
the HTML so so dialogue and the class
00:27:30.600
would just be overlay and we just need
00:27:33.840
to close with overlay as well oh
00:27:36.779
dialogue not overlay sorry dialogue grab
00:27:39.960
this put it in our web component instead
00:27:42.480
of the LI let's put that in there and
00:27:45.659
let me just bump it in a little bit okay
00:27:49.860
there we go dialogue
00:27:51.900
let me also grab the CSS for the overlay
00:27:56.760
specifically oops I actually just
00:27:58.559
realized we're editing the wrong file
00:28:00.299
we're editing single tasked up we're
00:28:02.340
editing single task up here that's
00:28:04.200
probably not something you wanted to let
00:28:07.140
me just take it back to the way it was
00:28:08.760
and make sure we're actually editing in
00:28:11.159
task adding let's grab the CSS related
00:28:14.580
to that okay so overlay so task adding
00:28:18.059
let's just replace this remember to keep
00:28:20.220
this up here okay so now we have all our
00:28:22.620
template information or HTML task adding
00:28:26.700
and so for now let's just keep it as is
00:28:31.620
we can I think especially in the next
00:28:35.100
lesson where we're going to start
00:28:36.360
creating more custom things like
00:28:38.159
reusable things like building out the
00:28:40.140
rest of the app and we can start at like
00:28:42.539
breaking out things like generic modal
00:28:46.140
elements and so forth a generic form
00:28:49.260
elements and and so forth but let's for
00:28:52.320
now to keep everything in this specific
00:28:54.419
task adding so we are not actually
00:28:57.600
passing anything because this is once
00:29:00.240
off component that we're only going to
00:29:01.860
use once so we're not going to configure
00:29:04.620
it everything is hard coded inside it
00:29:07.200
which in the next lesson we're probably
00:29:09.179
going to start breaking up more modular
00:29:10.740
more reusable things in terms of
00:29:13.260
elements or whatever you so the we need
00:29:16.860
the form and is that it and the cancel
00:29:20.279
those are the only two things I think we
00:29:23.760
need yes right so we just need to grab
00:29:26.580
data form and we need to crab data
00:29:29.820
cancel all right so let's just do that
00:29:31.919
in our elements here so we don't have
00:29:34.440
access to it yet because it only gets
00:29:36.360
read and rendered on connected callback
00:29:38.760
and we create the shadow root and we
00:29:41.159
clone the template and in elements we
00:29:45.000
grab the form and we grab cancel right
00:29:48.740
and so this should be form and this
00:29:51.659
should should be cancel and this is
00:29:53.940
unhappy because we actually mocked it up
00:29:58.020
as this so this needs to be form and we
00:30:01.440
can actually say this is form and cancel
00:30:05.340
all right so then obviously we're not
00:30:07.980
passing title we're not doing any of
00:30:10.140
this stuff we actually the only thing
00:30:12.480
that we do in here is the connected
00:30:15.000
callback so actually there is one
00:30:17.940
property that we can pause and that is
00:30:19.679
whether task adding is open or not so
00:30:23.220
let's create this in here and let's say
00:30:26.279
open it starts as not open unlike our
00:30:30.059
previous example we're not including the
00:30:31.919
button that opens it as well we're going
00:30:34.200
to keep that separate but you should be
00:30:36.480
able to set this open or closed let's do
00:30:39.779
our settings down here and let's say set
00:30:42.539
open new value get open but what we can
00:30:46.799
do is we can just return this so the
00:30:50.700
private The Hidden open and over here we
00:30:54.120
just set this to the new value but then
00:30:57.360
we also want to run that go modal and
00:31:01.140
close modal that we have yeah while
00:31:03.600
we're at it let's actually just make the
00:31:07.080
classes a bit more reasonable we don't
00:31:09.779
need to use the Bim name spacing anymore
00:31:11.760
so we can actually just do overlay we
00:31:13.620
can do title we can do field you can
00:31:16.080
even just Target the HTML straight up
00:31:18.299
and I still keep the classes though but
00:31:21.059
I just make them much more generic like
00:31:23.100
this I don't need to worry about
00:31:24.779
namespace Collision I see that it has
00:31:28.679
button in here let me just add a note
00:31:31.559
here let's create that file because
00:31:33.539
let's say in the next lesson we're
00:31:35.279
probably gonna create user action which
00:31:38.640
would be a button or a link or anything
00:31:41.220
like that but for now let's just put the
00:31:43.980
styling for button in there as well
00:31:46.500
duplicate that so up here because as you
00:31:50.159
might have guessed you can actually put
00:31:51.659
web components inside web components so
00:31:54.600
we can actually put a custom component
00:31:56.640
in here which is what makes web
00:31:58.140
components so cool so task adding to
00:32:01.140
open false and so let's also in our
00:32:04.500
elements grab the actual dialog itself
00:32:08.179
undefined HTML elements and that starts
00:32:13.320
out as the actual overlay itself
00:32:16.820
undefined and then we just actually grab
00:32:19.380
it when it gets connected and so when
00:32:22.440
you set the value likewise as we did
00:32:25.740
previously with the completed we can
00:32:28.740
check if the new value is the same as
00:32:31.799
what is currently the set value then
00:32:34.080
just return don't do anything don't
00:32:35.640
update anything don't save that
00:32:37.740
processing power save those kind of
00:32:40.500
re-rendering if not then set it to the
00:32:43.679
new value and we also want to say if the
00:32:47.159
new value is true so if new value then
00:32:51.120
this elements overlay show model and
00:32:54.960
it's going to tell us show modal doesn't
00:32:56.399
exist and that is because let's in here
00:32:58.799
first of all check we know that this
00:33:01.980
elements overlay is an instance of HTML
00:33:06.120
dialog element but we say if it's not
00:33:09.500
then throw this error oh new error
00:33:12.840
dialog element required okay so now it
00:33:17.940
knows that it's a dialog element and
00:33:19.500
it's going to give us the dialogue
00:33:21.120
elements related things and so obviously
00:33:23.880
if the new value is false then this
00:33:26.100
private elements close all right so as
00:33:29.340
we said it is automatically also just
00:33:31.140
going to update it and let's add this
00:33:33.360
event listener in our connected callback
00:33:35.820
so this elements cancel add event
00:33:40.080
listener and when that is clicked all
00:33:42.600
that you need to do is set this and
00:33:46.019
remember we shouldn't directly set the
00:33:48.120
private one here because the actual
00:33:51.000
public one has side effects it handles
00:33:54.059
this HML stuff for us so we need to
00:33:55.980
actually set open to false if we set it
00:33:59.820
directly to the value then it's not
00:34:02.760
going to actually trigger all of the
00:34:04.559
center stuff because we're then
00:34:06.360
circumventing the setter then also this
00:34:10.139
elements form let's add event listener
00:34:13.560
submit okay and let's for now just
00:34:17.639
console log the values so let's get all
00:34:20.399
of this from over here and so let's just
00:34:22.918
grab the event from there we can do this
00:34:26.099
but there is a better way than actually
00:34:28.820
just passing a function to the element
00:34:32.699
we can actually Leverage The Dom's event
00:34:35.760
bubbling system and we can have this as
00:34:38.339
an actual new element that we created
00:34:40.260
actually by an event that bubbles up
00:34:42.540
that we can catch at any point so we can
00:34:44.639
catch a submit event so we're going to
00:34:46.980
just comment this out and response and
00:34:50.699
then we also can discuss this open and
00:34:53.339
we can set it to false and event Target
00:34:56.399
reset okay so we need to do let's just
00:34:58.619
console log that response for now here
00:35:00.839
is our task adding and let's just pull
00:35:03.720
that in here so similar to this let's
00:35:06.480
just pull in task adding and it would
00:35:09.060
register it as a custom component that
00:35:11.820
would mean that we can just add it to
00:35:14.640
our HTML over here as an actual element
00:35:17.820
that is called task adding and by
00:35:20.640
default open is set to false so we don't
00:35:23.579
need to but if we do that it would
00:35:25.260
actually be open okay so over there it's
00:35:28.980
not doing anything but if we set it to
00:35:30.839
open it should actually be open and so
00:35:34.619
why is it not we didn't we don't
00:35:37.079
actually get this from the attribute
00:35:39.240
when it gets created so over here so we
00:35:42.660
can go over here and we can get the
00:35:44.520
attribute directly and feed it into that
00:35:46.500
but what we actually want to do because
00:35:49.500
we once again we want to trigger like
00:35:52.320
all the side effects is let's get the
00:35:54.720
attribute in the Constructor and we
00:35:56.520
would set it on the public value so we
00:35:59.099
would just do that when the element gets
00:36:01.980
constructed so this get attribute open
00:36:05.520
and remember we need to check if it is
00:36:08.700
not null because if we don't pass it it
00:36:10.980
will be null right so that will set this
00:36:13.440
for us when the component gets mounted
00:36:15.900
because we're setting it to the public
00:36:17.880
one it triggers all the side effects as
00:36:20.820
well that we get from the setter so we
00:36:23.280
are getting this error that says it's
00:36:25.440
not a dialogue element so if I look
00:36:27.839
elements overlay
00:36:29.780
undefined but in the connected callback
00:36:33.060
we set this elements and so what is
00:36:37.440
actually happening here is that because
00:36:40.980
we are only setting this on the
00:36:43.440
connected callback but we're already
00:36:45.540
firing this in the actual Constructor we
00:36:49.740
need to move this to the connected
00:36:51.060
callback we can only open it once the
00:36:53.760
HTML has loaded so over here we're
00:36:55.740
trying to do it but it doesn't exist yet
00:36:58.980
so if we move it over here it is it
00:37:02.099
should work theoretically let's have a
00:37:03.839
look cool and there we go so obviously
00:37:06.000
then if we set it in our HTML over here
00:37:09.480
to remove the open then it's not going
00:37:12.119
to be open okay so that's pretty cool so
00:37:14.040
we've kind of created this custom
00:37:15.300
element close is not this element's
00:37:18.300
close I actually think it's called
00:37:20.040
cancel and not close yes so that is
00:37:23.000
interestingly enough it should have
00:37:25.140
given us an error not 100 sure why it
00:37:28.859
didn't so we actually need to close the
00:37:31.800
overlay right so so this should work now
00:37:35.700
let's have a look hey all right but then
00:37:38.579
how do we open it and so let us add a
00:37:41.820
button here like we had previously but
00:37:44.820
it's no longer part of task adding so
00:37:48.060
let's just do a button uh let's just say
00:37:50.520
add task and the class is button and
00:37:55.140
let's just get rid of this open here
00:37:57.540
uh let's add an event listener to this
00:38:00.660
button let's just call it data add
00:38:02.760
button so we can search for this
00:38:04.859
directly
00:38:06.359
um and because we like it's an actual
00:38:08.579
thing and it's not just HTML this is a
00:38:11.460
bit better than just actually searching
00:38:13.859
for an HTML element but regardless if
00:38:16.500
you want you can still use data
00:38:17.880
attributes on it I'm just going to
00:38:19.800
search for it directly then in our
00:38:21.900
script so obviously at this almost high
00:38:23.760
level of abstraction what we can do is
00:38:25.680
we can say const and let's say add
00:38:27.720
button that's just document query
00:38:30.300
selector and then the actual task adding
00:38:34.260
we can actually query as if it's an HTML
00:38:37.079
element so we can actually just task
00:38:39.119
adding because it is because it's one
00:38:41.040
that we just created right now and so we
00:38:43.079
can do add button add event listener and
00:38:45.720
so effectively what happens is when
00:38:47.579
someone clicks the add button task
00:38:49.680
adding open is just set to an add button
00:38:53.339
so we just need to also do so in our
00:38:55.980
modules or slash
00:38:58.640
helpers.js let's grab get HTML and we
00:39:02.940
can actually just do that and for that
00:39:04.920
purpose we
00:39:05.760
just we might want to add data a data
00:39:07.500
attribute here because it uses data
00:39:09.060
attributes so let's just say data adding
00:39:11.099
and so that actually means we can get
00:39:12.900
rid of all of this add button and adding
00:39:17.040
and we also data attribute and so add
00:39:21.119
button is assume and add event listener
00:39:24.240
for what for click task adding open so
00:39:28.619
what you can actually even do is you can
00:39:30.420
export the class from task adding so
00:39:33.599
we're not exporting anything but what we
00:39:35.820
can do is we can and this is maybe where
00:39:39.300
this approach isn't that great so we
00:39:41.940
want to be able to still export the task
00:39:44.220
and in the same way that we have HTML
00:39:46.500
element and all of that stuff let's just
00:39:49.260
call this task adding and we export that
00:39:53.040
and because we need a default export
00:39:55.140
export default task adding let's put
00:39:58.440
this before the default export and now
00:40:01.800
we can actually pull that in here so we
00:40:04.020
can go task adding from and then we can
00:40:07.140
actually check is it an instance of up
00:40:09.060
here we can actually also just say if
00:40:11.339
task adding is not an instance of task
00:40:14.339
adding the revenue error
00:40:17.040
um invalid task adding adding in HTML or
00:40:21.300
whatever obviously the errors I'm adding
00:40:23.460
right now isn't that great but it is
00:40:25.920
what it is and so now we know that it
00:40:28.680
has opened so this is also pretty cool
00:40:30.240
because we do that now and we can also
00:40:32.940
get documentation if we want so we can
00:40:35.700
even go on here and say you know whether
00:40:39.359
the overlay model is shown or not so now
00:40:44.760
check that out so we for all intents and
00:40:47.520
purposes create our own HTML elements
00:40:49.800
and then cancel so the last thing we
00:40:51.960
want to do is we want to attach a event
00:40:54.780
listener to task adding itself we can
00:40:57.960
say something like submit or whatever
00:41:00.540
but let's create our own event listener
00:41:03.180
here like we would create a custom event
00:41:05.040
that we listen to for and let's just
00:41:06.839
come up with something custom that isn't
00:41:08.700
used in HTML already let's just say
00:41:11.160
added and when added fires we get an
00:41:14.160
event now let's go in here and let's set
00:41:17.400
up what's going to fire that event in
00:41:19.980
our own custom task adding so let's in
00:41:23.940
our connected callback actually register
00:41:26.579
that so we have it in here so let's
00:41:29.940
create in here a custom event so let's
00:41:32.040
do const and let's just say event and
00:41:35.520
let's say new custom event so you can
00:41:38.220
fire an existing event but let's create
00:41:40.079
our own cast moving because custom
00:41:41.460
events allows to send extra information
00:41:43.320
along with it what is it going to be
00:41:45.540
called and it's going to be called added
00:41:47.460
and what we can't pause so we need to
00:41:50.820
set bubbles to true so that it actually
00:41:53.880
bubbles upwards because by default
00:41:56.339
custom events don't bubble so that is
00:41:58.260
something we need to enable
00:41:59.880
and we can also add detail and detail is
00:42:03.119
anything extra that we want to add and
00:42:05.460
so let's just add response to detail and
00:42:09.839
then what we need to do is we need to
00:42:11.280
say this so in other words the web
00:42:12.960
component dispatch event and we just
00:42:16.380
pass the event so that gets dispatched
00:42:18.359
and this is unhappy let's just call it
00:42:20.280
added there we go all right so now it
00:42:22.140
dispatches that for us you will see that
00:42:25.380
if we now put a console log in here to
00:42:28.140
listen for that event it is actually
00:42:30.780
going to pick it up so let's bring this
00:42:33.060
in here and if we click our task and
00:42:35.820
there save hey it actually our event
00:42:38.400
listen actually picked it up and you'll
00:42:39.900
see actually detail comes along in our
00:42:42.599
event listener here it doesn't know it's
00:42:44.280
a custom event we can just also do a
00:42:46.619
tech event instance of custom event so
00:42:50.760
if it's not a custom event throw new
00:42:53.220
error because it needs to be a custom
00:42:54.900
event required to be custom event and so
00:42:59.819
now because we know it's a custom event
00:43:02.579
if this Arrow doesn't get thrown we can
00:43:05.339
go event detail and so let's just cancel
00:43:08.160
log that and so if we do add task
00:43:11.839
hey it adds the details so then in the
00:43:14.700
next lesson I'm going to show you how we
00:43:18.240
would then actually from that create a
00:43:20.700
task and like we would also transform
00:43:23.520
everything we have into custom elements
00:43:26.520
so our entire app is just like all these
00:43:28.319
customer elements that are talking to
00:43:29.819
one another these units of encapsulation
00:43:31.800
and then actually how we can use the
00:43:34.500
principle of polymorphism to actually
00:43:37.140
have a create a list component that can
00:43:40.500
take any type of thing whether it's a
00:43:42.720
task or a reminder a sub task or
00:43:46.319
whatever and so forth and the last thing
00:43:48.780
I want to do is I also want to show you
00:43:50.760
how we can actually create a module
00:43:53.160
where we actually save this in local
00:43:54.839
storage meaning that if you close your
00:43:57.599
browser and you open it again your tasks
00:43:59.819
are still going to be there so I'm going
00:44:02.220
to do that in the next lesson
00:44:04.560
um good luck with the exercise and I
00:44:06.300
will see you guys over there