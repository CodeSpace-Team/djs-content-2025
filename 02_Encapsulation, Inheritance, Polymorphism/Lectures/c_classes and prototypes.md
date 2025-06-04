Please write clear and comprehensive lecture notes and lesson content for this lecture:

00:00:00.000
all right so we have actually done a ton
00:00:02.639
and I hope that you have a bit of a
00:00:04.200
better understanding now of um not only
00:00:06.720
oop but encapsulation and how
00:00:09.059
encapsulation can help us keep our code
00:00:11.040
maintainable what I want to cover now is
00:00:14.460
let me just create a trusty old
00:00:17.660
example.js file again we spoke about the
00:00:21.060
tally app previously and how we could
00:00:24.480
actually use a factory function
00:00:26.820
to create a completely encapsulated
00:00:29.880
version of it and then I also showed how
00:00:32.579
we can create encapsulation in our code
00:00:35.700
base wrapping our data and our Behavior
00:00:39.860
underneath this kind of simplified
00:00:41.760
interface that you can just use so let's
00:00:44.940
say I know absolutely nothing about this
00:00:48.120
code base but I know kind of it's a
00:00:51.000
to-do app and so forth so I'm like okay
00:00:52.620
cool how would I create a task uh
00:00:55.079
probably with create tasks so let's say
00:00:56.879
you know like I'm gonna create a task
00:00:58.980
that is called example and all right so
00:01:02.219
what do I need so let's click on that
00:01:04.920
and let's control space Oh okay I said
00:01:07.140
the title so the task is do homework
00:01:10.740
what else do I need yeah I need you
00:01:13.260
again but what is due so do is a user
00:01:16.680
specified date for when the task should
00:01:18.240
be completed okay so this should be by
00:01:20.460
so let's say there's no due date and
00:01:24.180
urgency what is urgency okay urgency is
00:01:26.580
you use a specified indication of how
00:01:28.500
important the task is okay so let's just
00:01:31.200
say oh okay cool so high low medium
00:01:33.600
let's say hi okay cool there we go let's
00:01:36.299
see it in action so let me open it up
00:01:38.220
here on the side oh cool okay there it
00:01:40.259
is and I what can I do oh I can toggle
00:01:42.119
it on and off so let's look at the task
00:01:44.100
let's see what we can do so example oh I
00:01:46.920
can actually get these things and set
00:01:49.020
them so let's try and set the ID to
00:01:52.200
something and as you know it's actually
00:01:54.240
throwing an error cannot directly change
00:01:56.399
ID oh okay sure it doesn't quickly add
00:01:59.040
the window add event listener let's just
00:02:02.759
say error just to catch the errors and
00:02:04.799
and so critical errors let's just say
00:02:07.619
document something went very wrong all
00:02:11.038
right okay cool uh all right so let's
00:02:13.560
maybe try changing the title hey we can
00:02:15.840
do that let's see if we can actually get
00:02:18.599
even though it's not being displayed
00:02:20.280
right now let's see if we can get when
00:02:21.780
it was created let's have a look in the
00:02:23.640
console oh okay cool so you can see over
00:02:26.520
here here how abstracting things and
00:02:30.000
encapsulating them through means of
00:02:32.580
interfaces really helps keep your code
00:02:34.860
maintainable and really helps making it
00:02:37.980
easy to work with your code base even
00:02:39.900
for yourself so what I want to do now so
00:02:43.019
the next thing I want to talk about is
00:02:45.739
inheritance and specifically how we use
00:02:50.420
class-based inheritance to create web
00:02:53.280
components but before I do that I just
00:02:56.280
want to introduce classes I've been
00:02:58.019
speaking about it a ton now and you're
00:03:00.000
finally going to get to see it so let me
00:03:02.220
just do a super basic example of the
00:03:04.379
tally example so it's very similar to a
00:03:09.360
factory function here's the actual
00:03:11.159
secret it is actually a factory function
00:03:13.620
in JavaScript there isn't a thing like a
00:03:16.800
class it is what is called syntactic
00:03:19.319
sugar so syntactic sugar it's a computer
00:03:22.140
science principle which is a syntax
00:03:24.540
within a language that is designed to
00:03:27.180
make things easier to easier to read or
00:03:29.159
Express
00:03:30.180
it makes the language sweeter for human
00:03:33.180
use things can be expressed more clearly
00:03:36.060
or in an alternative style that some may
00:03:39.239
prefer it is usually shorthand for a
00:03:42.000
common operation that can also be
00:03:43.739
expressed in an alternate more verbose
00:03:46.319
form let me show you an example an
00:03:49.080
example of syntactic sugar is
00:03:51.980
destructuring in other words it doesn't
00:03:54.599
add anything new to the language it just
00:03:57.540
gives you extra some tactical
00:03:59.599
alternatives to expressing things
00:04:01.860
obviously if we have an object here and
00:04:04.440
we have the object name is skulk and
00:04:07.080
surname is Fender and we want to
00:04:09.900
destructure that this didn't exist in
00:04:12.659
JavaScript a decade ago the way you used
00:04:15.420
to do this would have been like this so
00:04:17.699
you would have had to do it this way so
00:04:19.858
this is just synthetic sugar it still
00:04:22.800
does this under the hood it's just an
00:04:25.199
easier nicer way to write it so before I
00:04:28.320
actually show you the underlying
00:04:29.699
mechanism
00:04:31.020
um let's actually just get into classes
00:04:33.060
so how would we do that tally app as a
00:04:36.180
class so classes you do by starting with
00:04:39.240
the word class then you write the name
00:04:41.340
of the class so let's just say counter
00:04:43.440
the convention is usually classes are
00:04:45.900
written as Pascal case like this so you
00:04:48.419
won't write it like that it's just a
00:04:50.280
convention you can do this it's not the
00:04:52.740
end of the world inside our class we can
00:04:56.040
actually set the value directory so we
00:04:58.860
can say the value is one we can add
00:05:01.560
methods in here that let's do increase
00:05:04.040
decrease let's just do it exactly the
00:05:06.960
way we did it before so here's the first
00:05:09.300
difference between a class and object
00:05:13.380
literal is in an object literal we had
00:05:16.560
this we could reference the object and
00:05:19.500
go for example you know increase counter
00:05:21.960
so we could reference itself in here so
00:05:25.560
whether that's a good or a bad thing is
00:05:27.360
Up For Debate but you could do this
00:05:29.880
because this is an actual thing and also
00:05:32.400
you also note that the way you'd clay
00:05:34.680
actual values in a class is a bit
00:05:36.840
different you can't do this here because
00:05:40.500
as mentioned counters are actually
00:05:43.080
syntactic sugar on top of factory
00:05:44.940
functions so the counter itself so the
00:05:48.180
class itself is actually not the thing
00:05:49.620
you have to create the thing in this
00:05:51.720
manner like we did previously there's a
00:05:54.180
catch classes you have to start with the
00:05:57.539
word Neo this is not going to create the
00:06:00.000
class so effectively there we have the
00:06:02.340
thing so we can't so inside a class you
00:06:04.740
have to use this there's no way around
00:06:07.020
it if you're creating classes you're
00:06:08.880
gonna use this all over the place which
00:06:12.060
is also one of the reasons why I don't
00:06:13.440
actually like classes that much
00:06:15.720
so you can have to go this value and we
00:06:19.199
actually need to say amount and let us
00:06:21.960
also just add display and all that
00:06:24.539
display does it console logs this dot
00:06:28.199
value okay
00:06:29.699
so we create our instance here and then
00:06:33.360
as you can see it's exactly the same
00:06:35.940
decrease display increase we can do that
00:06:38.759
and then we can go example display uh
00:06:42.720
the only caveat being that similar to
00:06:46.440
objects
00:06:48.000
um unfortunately there is no way to hide
00:06:51.180
this if something is accessible from
00:06:53.699
inside the class it is also accessible
00:06:55.979
from outside so the has been a recent
00:06:59.580
ly that if you dash before it like that
00:07:03.000
and this actually creates a private
00:07:06.600
property or a private method okay so
00:07:10.139
this has been added very very recently
00:07:12.660
to JavaScript it might not be supported
00:07:15.300
in all browsers uh but yeah so recently
00:07:19.620
JavaScript actually got the ability to
00:07:21.240
create private properties and so forth
00:07:23.639
but this is only in very new browsers
00:07:26.220
okay but so at this point still this
00:07:29.520
kind of exactly the same as olfactory
00:07:31.740
functions and so if we want to do the
00:07:33.720
temperature example again we can also do
00:07:36.180
the same so you can actually create
00:07:38.699
something called a Constructor so a
00:07:41.340
Constructor effectively just runs it's a
00:07:44.520
method that automatically runs when the
00:07:47.280
class gets created and so what we can do
00:07:49.680
is we can say in there the label and
00:07:52.440
then we can say this label equals label
00:07:55.380
in other words you need to pass in a
00:07:58.139
label and when you pass in that label
00:08:00.900
it's going to set it in here and you can
00:08:03.900
actually get it from inside the class
00:08:06.419
itself so then we can go this is similar
00:08:09.539
to the fahrenheit and things we did this
00:08:12.479
label and so obviously it doesn't give
00:08:15.000
us an error yet so what we can do is
00:08:18.060
let's just create an interface for this
00:08:21.599
so already we have a problem where my
00:08:25.680
convention that I previously did where I
00:08:27.660
made my types Pascal case no longer work
00:08:30.060
so what a lot of people do is they
00:08:32.580
prefix it with I to indicate that it's
00:08:34.919
an interface and this is actually
00:08:36.539
something that comes from other
00:08:38.039
languages and let's do a prop and we
00:08:42.120
also want this to be hidden so we're not
00:08:44.459
going to include this and in here we are
00:08:47.940
just going to have two callbacks so it
00:08:50.640
doesn't take anything doesn't return
00:08:52.140
anything and that is just display all
00:08:54.180
right so can we go returns I counter so
00:08:57.779
this doesn't work unfortunately the way
00:09:00.480
classes work in JavaScript I mean it's
00:09:03.060
actually very hard to wholly separate
00:09:05.600
your interfaces from your actual classes
00:09:08.700
themselves like this so if you want to
00:09:11.279
do that you would need to assign it here
00:09:14.880
you actually set everything in the class
00:09:18.000
itself so you would you know you would
00:09:20.580
write your documentation like this
00:09:22.920
inside the class itself instead of in a
00:09:25.860
separate type definition and so that
00:09:28.920
might be a good thing or a bad thing uh
00:09:31.140
depending about how you feel about that
00:09:34.440
but
00:09:36.120
um I actually prefer completely
00:09:37.860
separating my interface
00:09:40.019
um sometimes even in a completely
00:09:41.399
different file
00:09:43.140
um from the actual implementation of
00:09:45.660
that interface and the reason being that
00:09:48.120
when you're talking about classes
00:09:50.000
interfaces aren't necessarily something
00:09:52.560
that is separate from the actual code
00:09:55.080
that gets run within like very
00:09:57.500
class-based oope the class itself is the
00:10:01.019
interface I'm not going to go too much
00:10:03.000
into the theoretical reasons and that
00:10:05.399
critical underpinnings but just know
00:10:06.839
when you are working with classes this
00:10:09.480
is probably the way you want to do it
00:10:10.800
instead of doing a typedef completely
00:10:13.019
separately I prefer to keep my
00:10:15.000
definition separate but yeah it depends
00:10:17.220
on what you if this might actually be a
00:10:19.680
plus point for you with classes which is
00:10:22.080
why what I sometimes do when I am forced
00:10:25.620
to use classes and and I actually want
00:10:27.959
to do this is that I actually wrap the
00:10:30.180
class in a further Factory function so I
00:10:33.060
would go you know create counter and
00:10:35.700
then in there I would create the class
00:10:38.459
and then just return an instance props
00:10:41.880
that I pass through here I would just
00:10:43.980
pass directly into that because if I do
00:10:47.700
this I can go returns I counter okay and
00:10:52.440
in here because I now have this
00:10:53.820
namespace a lot of times I just call
00:10:56.519
this or whatever which means that I can
00:10:59.220
do this again so now I can just do okay
00:11:02.339
so this is just me personally but um
00:11:05.640
yeah let's put I just wanted to show
00:11:07.019
that so
00:11:08.579
um let's just also show this behavior of
00:11:11.399
where we use the Constructor so let me
00:11:13.980
just pop that out of there and let's
00:11:15.779
just get rid of all of this okay so then
00:11:18.360
you would set the parameters on here and
00:11:21.600
obviously now it's unhappy and let's
00:11:23.880
just say the label is Celsius
00:11:26.880
when we do example display one Celsius
00:11:29.760
okay so that's how you would do that the
00:11:32.160
other thing then is that you will see
00:11:35.220
now example the label is now actually
00:11:38.700
this is also where I like working
00:11:41.040
directly with Factory functions where
00:11:42.959
you have tighter control you can't
00:11:44.339
accidentally expose something like this
00:11:46.440
so we will need to do this but the thing
00:11:50.100
is you can't do a private function like
00:11:52.980
this you need to prepare it first create
00:11:56.579
it first up here before you assign into
00:11:59.940
it in the Constructor so obviously but
00:12:02.459
it is going to have to be undefined
00:12:04.800
until the Constructor is called right so
00:12:07.380
now it is gone so another thing that I
00:12:10.920
also want to note about losses is so for
00:12:14.760
example obviously there are a couple of
00:12:16.800
things in JavaScript that you can only
00:12:18.959
access by means of a Class A lot of
00:12:21.300
times your hand is kind of forced
00:12:22.800
whether you want to use a class or not
00:12:24.420
you know if we want to do today
00:12:26.820
and new date and this is where the new
00:12:29.399
comes from you might have been wondering
00:12:30.839
about that because date is actually a
00:12:33.720
class and the same for math you very
00:12:36.420
rarely use math to create an instance so
00:12:40.860
you actually see you can't actually math
00:12:43.320
doesn't even have a Constructor and what
00:12:45.839
with math you use what's called like
00:12:47.940
static properties on it so in other
00:12:49.680
words you know if you do random that is
00:12:51.839
a static property so in other words you
00:12:53.700
can use it without instantiating it so
00:12:56.339
math has both static methods and also
00:12:59.279
static values so for example pi and so
00:13:02.519
we can create static methods or static
00:13:05.040
values by just using the word static and
00:13:08.399
the convention is usually to put them at
00:13:10.200
the top so static values can be used
00:13:12.540
without instantiating a clause so I can
00:13:14.820
go static first name it's also just do
00:13:17.279
static surname and let's do a static
00:13:20.519
method as well static read and that just
00:13:24.060
returns yo-yo so then we can run run
00:13:27.300
those so we can go for example console
00:13:29.399
log counter DOT first name counter dot
00:13:32.940
surname and let's also just do counter
00:13:35.519
dot greet and let's run that because
00:13:38.279
it's a method skull painter yoyo all
00:13:40.560
right and so then the other thing is as
00:13:42.420
well is you can also do Setters and
00:13:44.940
Getters so if we want to do expose this
00:13:49.440
we will have we can also go set value
00:13:54.000
new value this value is new value okay
00:13:58.800
and get value is just return this dot
00:14:03.720
value so you can already see you're just
00:14:05.279
writing this all over the place so many
00:14:07.440
this is but effectively what we've done
00:14:09.959
now is we've just replicated the normal
00:14:13.079
functionality of value keep in mind that
00:14:16.740
in classes you can't have Setters and
00:14:19.680
Getters for something that already
00:14:21.200
exists so uh even if you want this to be
00:14:25.380
public the set time geta needs to be a
00:14:28.800
different name so let's just say diff
00:14:30.899
value so even if this is public example
00:14:33.899
value and example the value will give us
00:14:37.200
the same stuff right and also this is
00:14:40.380
also one of the things that I don't like
00:14:42.180
that much about classes is as you can
00:14:44.339
see it's much harder to split out your
00:14:48.060
functionality
00:14:49.399
and a lot of times you end up with this
00:14:52.019
massive long class you can do this you
00:14:55.800
can for example do functions up here
00:14:58.399
increase and so forth and then you know
00:15:01.860
just return it in here generally in my
00:15:05.160
experience class get a bit more unwieldy
00:15:07.139
a lot quicker let me just remove all of
00:15:09.600
this let's get back to our counter
00:15:12.720
example so now what I'm going to do is
00:15:15.060
I'm going to show you what inheritance
00:15:18.600
means has to be stated that a lot of
00:15:21.899
people consider inheritance as something
00:15:24.180
that's at the core of oop but it's worth
00:15:27.420
noting that like probably the biggest
00:15:29.639
book in the world of op called design
00:15:31.440
patterns elements of reusable object
00:15:34.380
orientated software even in this book it
00:15:37.800
actually says favor composition over
00:15:41.120
inheritance so what does this mean so
00:15:44.100
we've looked at composition before
00:15:45.480
composition is effectively where we take
00:15:48.180
things and combine them into a bigger
00:15:50.940
whole so I'm going to show you how to do
00:15:53.760
this how to do the same thing with
00:15:55.500
composition and how to do the same thing
00:15:57.180
with inheritance and these aren't p
00:16:00.779
class principles they're not even purely
00:16:04.199
oop principles but inheritance becomes
00:16:07.980
very easy with classes and there's also
00:16:10.680
a popular notion that inheritance is
00:16:13.079
somehow the preferred way to do things
00:16:15.060
in oop so it is important to talk about
00:16:18.180
this there are instances where you need
00:16:20.760
to do inheritance one of them being web
00:16:23.220
components inheritance always within
00:16:27.060
JavaScript
00:16:28.220
needs to be your last option there are
00:16:32.399
way better ways to achieve higher levels
00:16:35.279
of abstraction without inheritance but
00:16:38.040
it's very easy with classes which you've
00:16:40.980
guessed it is another reason I don't
00:16:42.420
like classes
00:16:43.680
so let me show you how inheritance Works
00:16:47.699
let's say we have a class and that class
00:16:51.060
is animal and we know that all animals
00:16:54.540
can I can either be alive or dead Okay
00:16:57.959
so let's say alive which is true so it's
00:17:01.800
a Boolean let's just create an instance
00:17:04.439
and let's say new animal and on that
00:17:07.380
instance live and let's just console log
00:17:10.740
alive and it's smart enough to know it's
00:17:13.319
a Boolean if we wanted to say only be
00:17:16.319
alive uh we needed to add a bit more
00:17:18.660
typing information so we need to say
00:17:20.459
like a true literal now they can just be
00:17:23.280
alive but a Boolean is fine then there
00:17:26.819
are specific types of animals they are
00:17:29.100
mammals so let's say mammal mammals
00:17:32.220
extend animals so it inherits from
00:17:35.340
animals in other words in other words
00:17:37.380
these values from CES lint actually like
00:17:41.760
doesn't even want us there doesn't even
00:17:45.179
allow us to have more than one class in
00:17:46.919
a file so let me just use lint disable
00:17:50.280
it just so he can focus what do we know
00:17:53.100
about mammals mammals have legs but
00:17:56.100
mammals have different amount of legs we
00:17:58.500
generally don't know how many but we
00:18:00.840
know they have legs
00:18:02.640
so what type of mammals do we get so
00:18:04.500
let's say we have a dog okay and we have
00:18:08.100
a cat both of these should be alive
00:18:11.640
um and we can actually set their legs
00:18:13.380
now we know that both of them have four
00:18:16.020
legs they both extend mammal but let's
00:18:19.140
create a specific dog and let's say spot
00:18:21.900
the dog which is extended from dogs
00:18:26.600
unfortunately spot wasn't a very tragic
00:18:28.980
accident and he lost one of his legs
00:18:31.500
okay so spot only has three legs so
00:18:34.080
let's create some things here so let's
00:18:36.299
say hey we want to create a cat so let's
00:18:40.260
say new cat
00:18:41.880
um we just want to create a general
00:18:43.140
mammal and we want to create let's say
00:18:46.440
spot the dog okay and all these we just
00:18:49.380
want to check how many legs they have
00:18:51.000
example one all of them should be alive
00:18:53.520
cool four undefined and three so
00:18:56.700
effectively you can think about
00:18:59.240
inheritance as you're almost kind of
00:19:02.100
going over over it and you can add more
00:19:05.880
specific information every time you
00:19:08.280
extend it further this is something that
00:19:10.679
sounds great in principle and it can
00:19:12.960
actually make your code look really nice
00:19:14.940
I mean like looking at this you're like
00:19:16.799
sure this is pretty neat you know like
00:19:19.020
we have a very nice structure here but
00:19:21.780
in practice results in a lot of hidden
00:19:25.620
things that are very hard to debug for
00:19:28.140
example let's say we're working on spot
00:19:29.580
the dog we're like okay example three
00:19:32.160
this oh I never set this thing alive
00:19:35.160
where does Alive come from all right
00:19:37.140
let's go so animal okay but how does
00:19:41.160
spot the dog get this from animal okay
00:19:44.460
let's go to spot the dog so this and it
00:19:47.340
takes it okay there it's declared and
00:19:49.260
let's go to spot the dog it doesn't
00:19:51.000
extend animal it extends dog okay but so
00:19:54.059
let's go deeper into dog so like you
00:19:56.460
have this chain and you need to dig and
00:19:58.860
find things and it it it really it's it
00:20:02.280
come couples your code very tightly
00:20:04.919
because another thing now is let's say
00:20:08.460
someone is working on spot the dog and
00:20:11.220
they have you know they add a method run
00:20:13.860
that is you know Zoom because even with
00:20:18.000
three legs this guy is fast okay but
00:20:21.059
let's say further up someone else
00:20:23.940
creates run here the intent here is they
00:20:27.419
want to actually they should start
00:20:29.100
executing something you know so so let's
00:20:31.980
say you know animals start as dead and
00:20:34.320
then you have to execute the run method
00:20:37.140
on them to actually set them to True
00:20:41.160
again this guy's gonna be like cool okay
00:20:42.840
so everything had inherits now from
00:20:44.400
animals
00:20:45.720
um actually will need to do this we can
00:20:48.480
go you know the cat so example one and
00:20:51.660
run and there we go and now if we log
00:20:54.780
example one and let's check if the cat
00:20:57.840
is alive after we run that cool true all
00:21:01.380
right okay so obviously because spot is
00:21:03.960
a mammal
00:21:05.100
um and he's an animal we should be able
00:21:07.679
to do the same on example three okay
00:21:10.020
let's have a look wait why is Scott
00:21:12.240
still dead we did what we were supposed
00:21:14.520
to do because it's an animal we executed
00:21:17.400
run to actually create him but he's
00:21:20.160
still dead not only is he dead but he's
00:21:22.020
what is this so I guess you have a
00:21:24.480
zombie duck running at full speed down
00:21:27.840
the road
00:21:29.159
um so yeah you can see like the problem
00:21:31.200
with extension is it hides too many
00:21:34.020
things which is why composition should
00:21:36.780
always be referred and so how you would
00:21:39.480
do that is instead of saying what
00:21:42.840
something is you would just Express the
00:21:45.900
behavior and the data itself compose
00:21:49.140
those together to create things very
00:21:51.360
similar to what we have done up until
00:21:53.220
now so an example let's say a duck all
00:21:55.559
right so let's say instead of
00:21:57.000
categorizing things into the type of
00:22:00.360
things that they are we just we just
00:22:02.039
create more loose threats of behavior
00:22:04.860
and values and so forth so let's say
00:22:07.380
classic objects what we would do is and
00:22:11.280
this approach is actually called mixins
00:22:13.320
so you can actually read up about that
00:22:15.480
so make is a concept in computer science
00:22:19.679
so effectively you can think about it as
00:22:22.440
you know you're cons you're creating an
00:22:23.940
ice cream and you kind of say I want
00:22:26.580
chocolate I want sprinkles I want a
00:22:28.380
flake so you have these specific things
00:22:30.360
so you don't say I want uh this specific
00:22:33.659
ice cream you effectively take all the
00:22:35.820
ingredients and you can combine them
00:22:37.559
into any ice cream that you want so but
00:22:40.440
let's just do it with the example of
00:22:42.720
once again for animals or whatever so
00:22:44.520
let's say uh flyable and things that are
00:22:48.299
flyable obviously has a value is flying
00:22:51.539
and they usually start as false and lift
00:22:55.080
off which just sets this is flying to
00:22:59.580
true and then land this is flying to
00:23:04.140
false okay let's just wrap those in
00:23:06.960
curly brackets and let's just say metal
00:23:10.200
so something can be metal material is
00:23:13.799
just metal if you tap it it goes clang
00:23:18.840
clang and then you also have something
00:23:21.419
that can be they're those like a duck
00:23:24.000
it's just so material is hard material
00:23:27.299
is soft when you tap it I don't know
00:23:30.539
what sound it makes if you tap feathers
00:23:33.539
I guess just like
00:23:35.400
so now we can actually create two things
00:23:39.780
here purely just from composition alone
00:23:42.179
actually before we proceed I actually
00:23:44.100
just picked up something here it
00:23:45.780
obviously it doesn't affect the actual
00:23:47.640
point or the example itself but just in
00:23:49.620
case anyone actually tries to run this
00:23:51.600
uh this actually won't work because
00:23:54.600
um over here it's fine we don't need
00:23:56.340
like this lexical scope because we're
00:23:58.020
just console logging but if you remember
00:23:59.940
correctly if you use an arrow function
00:24:01.500
it actually doesn't create lexical scope
00:24:03.440
meaning this is not going to work so we
00:24:06.240
actually need to write it like that for
00:24:09.840
it to work so just a heads up but it's
00:24:12.059
not related to the actual point I'm
00:24:13.860
trying to illustrate so but anyway let's
00:24:16.080
continue so we can actually say hey we
00:24:19.440
want an airplane an airplane is flyable
00:24:22.280
and it is metal we want a duck and a
00:24:26.400
duck is flyable and it has feathers now
00:24:29.760
we can go airplane liftoff airplane
00:24:32.280
let's tap it while it's lifted off and
00:24:35.220
it's should be able to go clang clang
00:24:37.380
clang we have a duck and duck lifts off
00:24:40.140
it's flying duck lands it's a duck lifts
00:24:43.380
off again lands again tap the duck and
00:24:46.500
it goes let's change this to poke poke
00:24:48.840
that makes a lot more sense if you
00:24:51.299
because if you if you tap or not so yeah
00:24:55.020
this is composition this is a lot easier
00:24:57.539
so you can actually just go if you want
00:25:00.360
to know where something comes from so
00:25:02.520
you're like hey what like why why can a
00:25:04.980
duck lift off so let's look at a duck
00:25:07.440
let's hover over this oh okay it comes
00:25:10.080
from Fly ball oh this is where this
00:25:12.000
comes from okay and you know so if you
00:25:14.640
do this correctly you can compose
00:25:17.280
basically anything you want whereas with
00:25:20.220
inheritance you're just gonna have to
00:25:22.200
keep on like creating these these
00:25:25.200
different levels of inheritance
00:25:27.539
um until you have like a million classes
00:25:29.720
there's this image and this is 100 my
00:25:33.299
experience as well don't mind oop part
00:25:36.480
here you know I think this is more about
00:25:38.220
inheritance than it is actually about oh
00:25:40.200
and once again it's because like a lot
00:25:41.640
of people think oop is about inheritance
00:25:43.919
and you know so here is what you know
00:25:46.440
like kind of a basic example like we did
00:25:48.360
here you know so you have an animal and
00:25:50.820
that can be a human or a pet and a pet
00:25:53.700
can be a cat or a dog here is what tends
00:25:56.640
to happen in actual practice when you
00:26:00.840
actually build software with this this
00:26:03.059
has definitely been my experience it's
00:26:04.860
something that's very seems very easy
00:26:07.080
and like a cool idea and practice and
00:26:09.900
then when you try and build something in
00:26:11.580
it the requirements become clearer and
00:26:13.740
you want to add stuff you want to extend
00:26:15.360
stuff sure it just turns into this
00:26:17.460
coupled mess which is why one of the
00:26:20.700
core books about oop says always always
00:26:23.700
always prefer composition over inherited
00:26:27.059
I also appreciate this when someone says
00:26:29.400
this isn't accurate you're saying every
00:26:31.799
class would also have an interface and a
00:26:33.900
test implementation so there's not
00:26:36.000
enough stuff here oh man some of these
00:26:37.919
jokes are amazing
00:26:39.539
okay
00:26:40.440
but there are cases where you can't
00:26:43.559
avoid inheritance sometimes this is for
00:26:47.820
legacy reasons uh sometimes this is
00:26:50.460
because someone created a framework and
00:26:52.200
this is their preferred way of actually
00:26:55.220
extending things even if you find
00:26:58.380
something like this and you have to
00:27:00.600
change the code or fix a bug or whatever
00:27:02.279
I would just continue the approach even
00:27:05.159
like if there are a million classes
00:27:07.620
because the moment you start combining
00:27:09.659
this and composition like then things
00:27:12.659
are just getting wild I'm not saying
00:27:14.580
avoid this I'm just saying when when you
00:27:17.100
have a choice prefer composition but
00:27:19.380
sometimes like it makes sense to rather
00:27:21.480
just continue with this one of those
00:27:23.340
instances are web components because
00:27:26.039
what web component we're going to touch
00:27:27.600
on web components now in a second the
00:27:29.880
only way to create web components is to
00:27:32.880
extend existing HTML elements and I'm
00:27:35.880
going to show you now why this is what
00:27:38.880
the dc39 decided and it's because of a
00:27:42.240
lot of Legacy stuff it's because of the
00:27:44.400
way the Dom works and the Dom is a very
00:27:47.880
frustrating thing to work with Douglas
00:27:50.159
crockford who wrote the book JavaScript
00:27:52.679
the good parts he actually said that for
00:27:55.140
him to write a book called JavaScript
00:27:57.480
the good parts he needs to pretend that
00:27:59.760
the Dom doesn't exist Because he
00:28:01.799
believes there are no good parts to the
00:28:03.600
Dom I agree with that the Dom is a mess
00:28:05.640
but it is what it is and it is what we
00:28:08.039
have and we have to work with it and we
00:28:09.960
can't change it because of those reasons
00:28:11.880
about backwards compatibility that I
00:28:13.860
mentioned and because of a lot of that
00:28:16.020
web components are dependent on classes
00:28:18.779
or not necessarily even classes but what
00:28:20.760
classes abstract so I did mention a
00:28:23.640
couple of times under the hood that
00:28:25.140
classes and functions are actually a lot
00:28:27.659
closer than you think and so I just want
00:28:30.480
to kind of actually show what is this
00:28:32.520
underlying logic that class is actually
00:28:35.820
abstract and as mentioned you know like
00:28:38.100
this is purely syntactical sugar it's
00:28:40.500
still does this for you actually beneath
00:28:43.440
under the hood before we start talking
00:28:45.720
about this it's important to talk about
00:28:48.500
prototypes in JavaScript so what exactly
00:28:52.020
are prototypes I did mention that a lot
00:28:54.960
of the confusion that especially other
00:28:57.779
developers coming from class based oop
00:29:00.960
languages actually experience is that
00:29:03.720
they assume JavaScript classes are
00:29:07.260
actually similar to classes in other
00:29:09.840
languages and I think I made it clear by
00:29:12.600
now that the big problem is that they
00:29:14.520
are actually not classes in JavaScript
00:29:17.340
are actually based on something called
00:29:19.260
prototypes in order to show you what
00:29:21.960
exactly prototypes are let me just open
00:29:24.779
the browser console and let us just get
00:29:28.020
a random element on this page at Google
00:29:31.200
at the Google page let us just find the
00:29:34.500
very first button on this page I don't
00:29:36.360
even know what it is so let's go
00:29:38.220
document query selector and let's just
00:29:41.640
find right I don't even know what this
00:29:44.159
is
00:29:45.360
um but let's also console der so if you
00:29:49.679
remember duh actually shows it to us as
00:29:52.559
an object because remember all Dom
00:29:55.020
elements even though they get displayed
00:29:57.960
like HTML in the console that is just
00:30:00.720
for help with debugging similar to what
00:30:03.299
it does with the shadow Dom they are
00:30:06.600
actually objects not only that
00:30:08.880
everything in JavaScript is an object
00:30:10.799
and I'll speak about that in a second so
00:30:13.740
if we open this up we can see all of
00:30:16.679
these properties and if we scroll all
00:30:20.039
the way down you will see this prototype
00:30:23.220
in two brackets written here and it
00:30:25.679
actually even tells you where this
00:30:27.539
prototype comes from so let's open that
00:30:29.460
up here is lots of properties so we can
00:30:32.220
just keep on scrolling scrolling
00:30:33.539
scrolling and then the next prototype
00:30:36.059
which is HTML element so let's see what
00:30:38.820
comes from the HTML element and if
00:30:41.640
you're scrolling and you get this this
00:30:43.080
means that there's more and you can just
00:30:44.700
click on that to show more then further
00:30:46.980
we get stuff from element and then if we
00:30:49.140
go further down we get stuff from node
00:30:50.940
and then if we go further down event
00:30:53.220
Target and finally we reach object and
00:30:57.179
after object there is no more prototypes
00:30:59.640
a everything in JavaScript is based on
00:31:03.539
this object prototype so how do we
00:31:06.419
create that thing thinking back to that
00:31:08.760
example that we have about you know
00:31:11.100
animal and we have like mammal and all
00:31:14.220
of that we can think about everything in
00:31:17.640
JavaScript is actually based on object
00:31:20.580
it just extends it so we have event
00:31:23.820
Target which which extends object and
00:31:27.659
then if we go further up node extends
00:31:30.960
event Target and so forth and so forth
00:31:33.720
and so forth until we get all the way to
00:31:35.940
HTML element so this is called the
00:31:39.360
prototypal chain and if you go and have
00:31:42.240
a look on mdn so you can actually see
00:31:45.000
the prototypal chain here HTML button
00:31:47.520
element HTML element element
00:31:49.700
node event Target so you can follow it
00:31:53.100
all the way down so this is very similar
00:31:55.740
to that inheritance example that we
00:31:58.260
showed but there's an important mistake
00:31:59.940
function between prototypes at actual
00:32:02.760
true to form classes I obviously can't
00:32:05.820
illustrate real actual classes here
00:32:09.059
because we don't have real actual
00:32:11.760
classes in the true sense in JavaScript
00:32:13.980
so for example languages like Java
00:32:17.039
python C shops and these are class-based
00:32:19.919
oop languages obvious example where this
00:32:23.220
differs from traditional classes is
00:32:25.559
traditional class-based oop languages
00:32:27.960
you can actually extend several things
00:32:29.880
so this would have actually made our
00:32:32.279
composition example a bit easier so if
00:32:34.799
we remember that example that we had we
00:32:36.960
in if this was a true class-based
00:32:39.179
language we would have been able to go
00:32:41.779
extends flying and Feathers likewise
00:32:46.559
plane extends flying and metal so one of
00:32:52.679
the key things about prototypes and
00:32:54.779
prototypal inheritance is you can only
00:32:57.600
extend a single thing at a time you
00:33:00.960
can't actually compose different things
00:33:04.080
together and likewise in through
00:33:07.980
class-based systems you you can also not
00:33:10.740
only extend but you can also Implement
00:33:12.600
so I can actually then create something
00:33:16.200
and say class Johnny the duck implements
00:33:20.519
and so obviously it gives me a warning
00:33:22.740
because it says can only be used in
00:33:24.899
typescript files it's not supported in
00:33:26.580
JavaScript and then it ensures that I
00:33:29.519
have actually everything that a duck
00:33:32.399
needs so a lot of classic oop languages
00:33:35.399
allow mechanisms to ensure that
00:33:38.100
something is the shape of a specific
00:33:40.380
thing in JavaScript there's no way to do
00:33:43.140
that so that also means in actual
00:33:46.500
class-based languages that you can
00:33:49.019
actually create something purely as a
00:33:52.140
what would be called an abstract class
00:33:54.200
purely as almost like an interface like
00:33:57.600
we had so you can I can create you know
00:34:00.299
human first name and last name and then
00:34:04.679
I can go plus skulk implements human and
00:34:09.659
then it's gonna give me an error if I
00:34:12.418
don't put first name and that stuff in
00:34:15.119
it I'm going to show you
00:34:17.099
um just what a class actually does under
00:34:19.020
the hood and then I'm going to talk a
00:34:20.219
bit more about prototypes even before
00:34:22.619
the days of the actual class syntax and
00:34:24.719
so forth so if I were to do class
00:34:27.000
example one and that is just Constructor
00:34:31.440
and we just pass it let's just say label
00:34:35.040
and all that that does is it sets this
00:34:37.918
in a test and test starts out as
00:34:40.679
undefined it just actually sets this
00:34:43.679
test to whatever you pass in label then
00:34:46.918
we would call that and we would just say
00:34:48.719
you know instance one is new example one
00:34:53.339
so like that what does this actually do
00:34:55.260
under the hood this is just syntactic
00:34:57.480
sugar on top of the following function
00:34:59.400
function two okay there we go and we
00:35:02.520
pass in label there and remember
00:35:04.440
everything in JavaScript is an object
00:35:07.140
including functions so what we can
00:35:09.599
actually do this is a very clever actual
00:35:12.119
approach is that this will refer to the
00:35:15.240
function itself which is also why you
00:35:17.700
need to use it in this way you can't do
00:35:19.920
it with a an arrow function because an
00:35:22.079
arrow function doesn't have lexical
00:35:23.339
scope so the function itself test equals
00:35:27.540
label so then we can also do new example
00:35:30.720
two so let's console log sorry instance
00:35:33.780
one and instance two and you will see
00:35:36.060
that they are the exact and also we need
00:35:38.940
to pass actually something to it let's
00:35:42.119
just pass one to both of them and let's
00:35:44.220
have a look and see go you'll see that
00:35:46.920
they do exactly the same you can even
00:35:50.160
check if it's an instance of so I can
00:35:52.680
check console log is instance 2 instance
00:35:56.760
of example two and let's just do the
00:35:59.820
same without class as well let's run
00:36:02.160
this to show you that it treats both of
00:36:04.320
these as if they are the same thing
00:36:06.060
there you go both are true okay so it
00:36:08.339
treats both of these as if they kind of
00:36:10.859
have the exact same functionality this
00:36:12.900
is just written in this manner which is
00:36:14.640
the syntactic sugar on top of this and
00:36:17.400
we can even have a look at the
00:36:18.780
prototypal inheritance so you'll see it
00:36:21.180
just inherits how does prototypal
00:36:23.280
inheritance work effectively it works as
00:36:26.040
follows so I'm just gonna so in that
00:36:28.260
example that we had where we had where
00:36:30.660
we had animal and then we had mammal and
00:36:34.140
then we had dog and then we had spot the
00:36:36.660
dog effectively if we go spot the dog
00:36:40.320
effectively if we have you know const
00:36:43.500
let's say we create an instance of you
00:36:46.500
know new spot the dog yeah obviously
00:36:49.380
it's going to give an error because that
00:36:50.460
doesn't exist and on that instance we go
00:36:54.780
bark a chicks does spot the dog have
00:36:59.099
something called bark if it does it runs
00:37:01.920
it it doesn't find it checks the next
00:37:04.140
one it checks dog and dog maybe has bark
00:37:06.599
and then it runs that the big difference
00:37:09.359
as well is with prototypes the actual
00:37:12.060
values themselves don't even come along
00:37:14.579
for the ride the actual when you call it
00:37:17.820
it checks the current thing and if it
00:37:20.339
doesn't find it goes on to the next
00:37:21.839
thing into the next and so it kind of
00:37:23.700
keeps on falling back until it
00:37:25.800
eventually reaches something which as
00:37:27.960
you can imagine once again can result in
00:37:31.140
a lot of really subtle bugs that are
00:37:34.440
hard to pick up as with the example
00:37:36.300
where we had you know run on animal
00:37:38.760
which created we created the animal but
00:37:41.099
then we also had run on spot spot the
00:37:43.440
dog so if we did run then immediately it
00:37:46.380
would get the one on here on the other
00:37:48.839
so if we just did run on cat you know
00:37:52.020
which also inherited from mammal it
00:37:55.800
doesn't have run so it goes to the next
00:37:57.660
one it doesn't have run and then finally
00:37:59.460
it reaches this and you might even have
00:38:01.440
other things above that which is like
00:38:03.420
organism and so forth so generally you
00:38:06.839
want to kind of stay away from
00:38:08.160
inheritance it kind of results in a lot
00:38:10.500
of these type of things if we just go in
00:38:12.660
here and let's just grab the first H1
00:38:15.260
document query selector H1 and but let's
00:38:19.800
also do console der to just show it as a
00:38:23.280
Dom node all right so you can click on
00:38:25.140
that and then you can see this specific
00:38:26.940
H1 we go down what is the Proto what's
00:38:30.720
the next prototype in the line HTML
00:38:33.240
heading element all right so we can go
00:38:35.400
down so we can follow this entire
00:38:37.320
prototype chain so for example something
00:38:39.900
like click click is something that is a
00:38:43.440
actual method on all HTML elements so
00:38:47.160
anything that inherits and also the term
00:38:50.640
inherent is actually a bit misleading
00:38:53.579
here because it doesn't actually inherit
00:38:55.260
it doesn't come along it just sets that
00:38:58.440
as the target fallback so in other words
00:39:01.079
if I do click on this H1 it's going to
00:39:04.859
see is there something called click on
00:39:06.540
it there isn't so it's going to go to
00:39:08.579
the next item in the Prototype chain
00:39:10.320
HTML heading element does that have
00:39:12.660
click no it doesn't and then it finally
00:39:15.480
runs this over here but here's where it
00:39:18.540
gets even Wilder we can directly add and
00:39:22.859
remove things from prototypes and this
00:39:25.200
is where it gets wild which is why I
00:39:28.200
really think the JavaScript
00:39:30.420
implementation of classes is very
00:39:31.980
problematic granted most people are
00:39:34.440
never going to run into these type of
00:39:36.420
cases but even just the fact that it
00:39:38.460
exists excuse me you can actually
00:39:41.640
directly modify prototypes after they
00:39:44.700
have been created so this is also what
00:39:47.040
the difference is with traditional
00:39:48.480
classes so if I go class bird okay and
00:39:53.460
bird has a color which is starts as
00:39:57.300
undefined and let's say it is a certain
00:40:00.240
now I know if I look at this thing this
00:40:03.420
is this is the shape of a bird this is
00:40:05.940
what all birds are going to be if I see
00:40:08.220
a bird this definition is actually what
00:40:11.460
actual birds look like and not only that
00:40:14.820
some languages are just like this is
00:40:16.920
crazy you can set your class and that is
00:40:19.200
it and you can't change it again for you
00:40:21.359
know obvious reasons like you know if
00:40:23.640
you want to look at this you want to
00:40:24.660
know this is what a bird looks like
00:40:26.640
um you don't want to know okay you can
00:40:28.440
further modify it down here which you
00:40:30.900
know some languages allow you to do that
00:40:32.700
I think it's a bad idea but some do that
00:40:35.520
and so you can also go uh Wings you know
00:40:38.460
let's just say all birds have two wings
00:40:40.920
okay so but this isn't that great but at
00:40:43.920
the very least still there is uh actual
00:40:47.520
set of rules that when you create a bird
00:40:51.000
um let's just say you know Dove and we
00:40:53.280
say new bird that when we create them
00:40:55.619
here all of them are going to be created
00:40:57.660
with the same rules you know like once
00:40:59.579
that's created uh whatever these rules
00:41:01.800
are that's going to be the shape of the
00:41:03.060
bird what makes JavaScript absolutely
00:41:06.000
crazy in terms of its prototypal
00:41:08.640
inheritance is I can actually go after
00:41:12.300
this and update bird and it's
00:41:14.579
automatically going to update all the
00:41:16.920
birds that have been created already
00:41:18.420
that is insane that sounds super
00:41:20.700
powerful and it is but it's very very
00:41:24.119
scary because someone can just go bird
00:41:27.560
prototype legs nine and now all birds
00:41:31.740
that have ever been created up until
00:41:33.540
this point is automatically gonna get
00:41:35.760
nine legs added to them retroactively
00:41:38.280
which is crazy and this is also why I
00:41:41.220
prefer Factory functions because you
00:41:42.720
can't do this this type of crazy stuff
00:41:44.520
with Factory functions when a factory
00:41:46.200
function runs the thing that gets
00:41:48.300
created is based on the conditions of
00:41:50.640
that factory when it was created with
00:41:52.560
prototypes because remember prototypes
00:41:55.260
fall back they don't actually get
00:41:57.300
inherited they don't actually get
00:41:58.920
extended that me means that you have
00:42:01.800
Dove and it checks does dove have legs
00:42:04.440
and no it doesn't and it falls back to
00:42:06.780
the next thing so at any point when you
00:42:08.520
call it you can set the fallback
00:42:10.200
condition so you can change the
00:42:11.460
Prototype even after the thing has been
00:42:13.140
created and because it falls back it's
00:42:15.000
going to pick it up that might have even
00:42:16.800
confused you even more so I'm going to
00:42:18.300
show you a practical example and in the
00:42:20.160
early days of JavaScript people thought
00:42:21.720
like this is amazing and they went nuts
00:42:24.060
with it I'm going to show you an example
00:42:26.099
of like how you can actually would have
00:42:27.720
done something useful with this but
00:42:29.460
there are very very big problems uh if
00:42:32.579
we go on mdn Prototype they actually
00:42:35.880
have this big red warning over here
00:42:38.700
telling you not to do it so if we look
00:42:40.859
at for example object which is what
00:42:42.960
everything is built on every single
00:42:45.420
actual built-in prototype in JavaScript
00:42:47.640
to have this warning that says do not
00:42:50.280
modify the Prototype you are asking for
00:42:52.680
trouble it says modifying the Prototype
00:42:54.780
property of any built-in Constructor is
00:42:57.180
considered bad practice and risks
00:42:59.520
forward compatibility on mdn they
00:43:02.099
actually tell you to avoid directly
00:43:04.380
using the Prototype itself so and so
00:43:06.660
what does this actually mean so let's
00:43:08.220
let's go to the MTN home page so let's
00:43:10.920
go to latest news let's get the very
00:43:13.380
first H2 and just ignore that error up
00:43:16.619
there it's mdn specific all right there
00:43:18.780
we go and so let's get it as a dur so as
00:43:21.359
the actual Dom object okay and you can
00:43:24.480
see it has all these prototypes that
00:43:26.880
will fall back to when you try and
00:43:29.220
access something so you can imagine even
00:43:32.280
after this thing has been created if you
00:43:35.220
update one of the prototypes that it was
00:43:37.380
created from it's actually gonna be able
00:43:41.160
to fall back to that updated version of
00:43:43.319
the Prototype because it doesn't contain
00:43:45.599
everything inside it so it's dependent
00:43:48.240
on things that are completely outside of
00:43:50.400
it that can become that can actually be
00:43:52.560
updated and and without even knowing
00:43:55.380
that there's something that depends on
00:43:56.819
it at the very least it was traditional
00:43:58.700
class-based languages you don't get this
00:44:01.319
so let's say hey everything that is
00:44:04.560
actually based on this HTML element
00:44:07.500
let's add something to it so effectively
00:44:10.260
every single HTML element on this page
00:44:12.780
the Dom node of it the Dom object is
00:44:15.720
going to get something new HTML element
00:44:17.839
prototype let's add something called
00:44:20.099
greet and let's just make that a
00:44:22.440
function all right uh let's just say
00:44:24.000
that says console logged all right so
00:44:25.920
that has been added so let's find that
00:44:28.500
document query selector so let's get a
00:44:30.420
heading and on that heading let's try
00:44:32.760
and run greet wow check that hello so
00:44:36.839
how on Earth did this happen we never
00:44:39.000
added anything to H2S but the reason is
00:44:42.720
because like the Prototype keeps on
00:44:44.520
falling back falling back falling back
00:44:46.200
any object that is in that actual chain
00:44:49.260
it's actually going to be able to treat
00:44:51.720
it as if that is a property on the thing
00:44:53.579
itself so that effectively means if we
00:44:56.880
add anything to the object prototype
00:44:59.460
it's going to be available on everything
00:45:02.339
not only that we can actually override
00:45:05.520
how something like two string works on
00:45:09.060
the object prototype and because
00:45:10.200
everything inherits from the object
00:45:11.819
prototype it's completely actually going
00:45:13.680
to override how to string Works in
00:45:15.599
JavaScript itself so as you can imagine
00:45:17.760
when this was discovered people went
00:45:20.099
absolutely insane so they started doing
00:45:23.460
things like um taking the array
00:45:26.220
prototype and adding something like sum
00:45:29.280
which all the values so let's say this
00:45:32.760
and I'm just going to use a higher order
00:45:34.260
function here just to calculate the sum
00:45:36.240
I'm not going to you don't need to know
00:45:37.680
what I'm doing right now so let's just
00:45:38.940
do reduce this value and results don't
00:45:44.040
worry too much about what I'm doing
00:45:45.480
right now I'm just adding the ability to
00:45:48.359
calculate the sum of values so of L plus
00:45:51.060
result we just added that to an array
00:45:53.520
that means now if we do this run sum on
00:45:56.339
it you can actually just add your own
00:45:59.339
methods and properties to JavaScript as
00:46:01.680
you can imagine that is a really really
00:46:03.780
big problem it just takes me doing this
00:46:06.480
and now literally I'm changing every
00:46:10.380
single possible line of JavaScript in a
00:46:13.319
code base even code that I've never seen
00:46:16.020
before I'm influencing how it's going to
00:46:18.300
work now so some of the really very
00:46:21.180
early
00:46:22.440
um JavaScript libraries actually added
00:46:24.480
the the the actual extended behavior in
00:46:28.319
this manner you had these like prototype
00:46:30.480
and so forth so if we look at the
00:46:32.640
documentation for Prototype if you
00:46:34.200
install prototype now all of a sudden
00:46:36.300
you've got all these extra things so you
00:46:38.160
know element layout you know now you've
00:46:41.099
got this thing called layout
00:46:43.380
um On All or to CSS or whatever and
00:46:47.160
people thought this was amazing and like
00:46:49.560
people just pulled this in left right
00:46:51.839
and Center until we started realizing
00:46:54.060
hey being able to just like update make
00:46:56.819
these massive changes to how things work
00:46:58.859
in our code base with something as
00:47:01.020
simple as this is maybe not a good idea
00:47:03.480
especially when you're several people
00:47:05.099
working on the same code base and so so
00:47:08.160
we saw dramatic change in approach with
00:47:11.880
libraries from there on out I'm going to
00:47:14.220
speak a bit about libraries a bit later
00:47:15.660
but so the the main one that came after
00:47:18.300
that was one called jQuery and you'll
00:47:20.700
actually see that what jQuery does if we
00:47:23.520
look at the jQuery documentation all the
00:47:26.040
jQuery stuff is actually just in a
00:47:28.079
jQuery object that you install so for
00:47:31.319
example if we go to the documentation
00:47:33.839
and yeah you can see from from the
00:47:35.700
website jQuery is is a bit old school
00:47:38.040
you shouldn't really be using jQuery
00:47:40.200
anymore nowadays
00:47:41.940
um so it actually create an object in
00:47:44.579
the dollar sign that you could use
00:47:47.280
because you can't technically actually
00:47:49.140
use the dollar sign as a string you know
00:47:51.960
it would do something like this so ad or
00:47:54.960
whatever and it had all its behavior in
00:47:57.119
here so it kind of moved away completely
00:48:01.079
from this ideal prototypes and so forth
00:48:04.260
um in fact you could actually even
00:48:05.700
create plugins for jQuery that used
00:48:09.599
actually a factory function so if you
00:48:13.079
wanted to add something to jQuery you
00:48:16.020
could go.fn and just say what you want
00:48:19.140
to call your thing so you know yo yo yo
00:48:21.560
and that kind of prevented you from even
00:48:23.940
overriding some of the bolt in jQuery
00:48:26.220
stuff prototypes have a Troublesome
00:48:28.440
history in JavaScript classes are based
00:48:31.740
on prototypes at the very least classes
00:48:34.260
don't expose a way to do this directly
00:48:38.640
in the class itself so it tries to Model
00:48:41.900
class-like Behavior on top of JavaScript
00:48:45.260
it's not a hundred percent the same as
00:48:48.240
classes in other languages as mentioned
00:48:50.160
you don't have implements you can't
00:48:51.960
extend from more than one plus or
00:48:55.440
abstraction and it actually doesn't even
00:48:58.020
extend it actually just sets something
00:49:00.300
as a fallback Target it does it in such
00:49:02.880
a way where at the very least it it
00:49:05.280
hides the dangerous stuff from you but
00:49:08.520
kind of just to prove that it's still
00:49:10.920
there if we go for example class bird
00:49:13.079
and you create an instance so let's just
00:49:16.020
actually say you know Wings two and I
00:49:19.020
create an instance of that bird so I say
00:49:21.780
new bird if I then even after the
00:49:24.300
instance has been created and I extend
00:49:27.300
that from animal and let's just add
00:49:30.180
class animal up here and extends with an
00:49:33.480
S okay and it's just unhappy and it's
00:49:36.000
just unhappy because it's not a big fan
00:49:37.859
if I do two classes in the same file so
00:49:42.180
what I can still do is I can still go
00:49:45.000
animal prototype legs nine and then if I
00:49:49.740
want to check this instance of this bird
00:49:51.960
that I created how many legs does it
00:49:53.760
have nine despite the fact that by the
00:49:57.839
time the bird was created there was like
00:50:01.079
there's nothing in the actual things
00:50:03.599
that it was created from it was added
00:50:06.420
afterwards even after this instance was
00:50:08.460
created so you can real time update
00:50:10.940
existing instances which is very very
00:50:13.859
scary at the very least two classes
00:50:16.260
created classes actually doesn't allow
00:50:18.420
you to do this it is still there so you
00:50:21.420
need to know how to do it to actually be
00:50:23.940
able to do do it any documentation you
00:50:26.160
read anywhere whether it be mdn or
00:50:28.200
whatever it's going to tell you do not
00:50:29.520
do this please do not do this that's two
00:50:31.740
classes as credit but be mindful that
00:50:34.800
this is actually what classes are built
00:50:36.540
on and that it's actually not through
00:50:39.180
classes in the sense that you would have
00:50:41.160
a class in an object-orientated language
00:50:43.619
which you know isn't an issue at the
00:50:46.440
very least it gives us the exact same
00:50:47.940
behavior that we get from a factory
00:50:49.859
function the good news is that at the
00:50:52.200
end of the day it just comes down to
00:50:54.059
what is your personal preference a lot
00:50:56.160
of people would say classes are
00:50:57.599
inherently bad I wouldn't go that far I
00:51:00.000
would just say personally I actually
00:51:01.319
don't like working with classes if it's
00:51:03.300
not an interface that I enjoy it's also
00:51:06.420
I find it reads a bit too differently
00:51:08.579
from the way that you write your other
00:51:10.319
JavaScript it works a bit too
00:51:12.300
differently and it requires you to rely
00:51:16.500
on this quite heavily um and pretty
00:51:19.440
clear that I'm not a fan of this but
00:51:21.420
yeah like subjectively I just I'm not a
00:51:23.460
big fan of classes but if you like
00:51:25.980
classes if you like working with classes
00:51:28.740
I would encourage you go ahead use
00:51:30.900
classes but in the case of something
00:51:34.140
like web components because web
00:51:36.359
components extend the Dom and because
00:51:38.520
all these Dom elements are prototypal
00:51:40.920
and have these prototype chains they do
00:51:44.099
require us to use classes there's no
00:51:47.040
other way so so in the next section I'm
00:51:49.680
going to chat about this but effectively
00:51:51.839
you would create a web component as you
00:51:53.880
would extend an HTML element so I would
00:51:55.920
go for example skulk custom and I would
00:51:59.220
need to extend the HTML element and it
00:52:02.339
would and it would set up the prototypal
00:52:04.140
chain in terms of you know HTML element
00:52:06.780
and then element and then further down
00:52:09.180
element node and so forth and so forth
00:52:12.180
and so forth all right so in the next
00:52:14.040
session I'm going to introduce web
00:52:15.839
components and I'm going to show you why
00:52:18.119
web components are useful