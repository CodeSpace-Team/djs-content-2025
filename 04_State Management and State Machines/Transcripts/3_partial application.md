00:00:01.079
so for the remainder of this um lesson
00:00:04.600
what I want to do is I want to look at
00:00:06.359
three things so first and foremost um I
00:00:09.440
want to kind of talk about this idea of
00:00:11.240
having a utils folder and generally you
00:00:15.040
have a utilties folder where you have
00:00:17.359
all these composable functions that you
00:00:19.480
can combine into bigger things so I'm
00:00:21.840
going to just show like how higher order
00:00:24.439
functions are a really great fit for
00:00:27.119
this idea of composing functions
00:00:30.320
together then I just want to quickly
00:00:32.960
show um how you can take this idea of
00:00:36.399
composable functions even further which
00:00:39.600
might be a bit too far for you and I'm
00:00:42.200
not going to do that um in the code that
00:00:45.320
I write but I want to show it to you and
00:00:47.640
it's up to you to decide whether there
00:00:49.199
something you want to explore with
00:00:50.840
yourself so I specifically also want to
00:00:53.600
look at third party libraries that give
00:00:55.760
us utility functions um that we can also
00:00:58.559
compose so things like load
00:01:01.000
then I quickly just want to refer to mdn
00:01:03.039
to go over the bolt in higher order
00:01:05.400
functions specifically the ones that are
00:01:08.680
associated with um arrays and so forth
00:01:12.080
but I think before we go deep into this
00:01:14.240
let's maybe just have a look at
00:01:15.600
Wikipedia let's actually look at what
00:01:18.240
does Wikipedia say a higher order
00:01:20.600
function is and let's work our way
00:01:23.439
backwards from there it effectively says
00:01:26.320
also we shouldn't confuse higher order
00:01:28.520
functions for funk tors um I will speak
00:01:32.360
a bit about functors the most obvious
00:01:34.960
functor in JavaScript would be an array
00:01:37.759
that has like map on it and so forth but
00:01:40.640
this is very theoretical you don't need
00:01:42.479
to worry about this but just be mindful
00:01:44.880
that when you see the term functor um
00:01:47.520
and higher order function or even just
00:01:49.439
function these are three different
00:01:50.960
things so higher order functions
00:01:53.200
actually come from the world of
00:01:54.799
mathematics so as a lot of things in
00:01:57.920
functional programming so a high
00:02:00.079
function is a function that does at
00:02:02.200
least one of the following it can do all
00:02:04.399
of them but it does at least one of them
00:02:07.200
it actually takes a function as an
00:02:10.119
argument so this is where I spoke about
00:02:12.040
that thing about abstractions inside
00:02:13.640
abstractions inside abstractions so it
00:02:16.040
effectively says you know a procedural
00:02:18.239
parameter so which is a parameter of a
00:02:21.599
procedure that is itself a procedure
00:02:24.080
okay so this is that kind of NeverEnding
00:02:26.480
nested thing that I spoke about and also
00:02:29.160
you know so parameter this is also where
00:02:31.720
we get parametric so parametric
00:02:34.599
polymorphism or it's a function that
00:02:37.640
returns another function as the actual
00:02:40.360
return so it can be both or it can be
00:02:42.599
either of these and so here you can
00:02:44.720
actually see a mathematical function
00:02:47.159
which obviously programming functions
00:02:48.840
are based on so you can actually see
00:02:50.680
this looks a lot like The Arrow function
00:02:52.599
in JavaScript and so here are some
00:02:55.360
things that are generally higher order
00:02:58.080
functions and not only in programming
00:03:00.680
but in mathematics as well so map um
00:03:03.680
which we spoke about quite extensively
00:03:05.400
now I'm going to dive into map show you
00:03:07.640
in a bit more detail actually what
00:03:10.239
exactly map does um sorting uh which we
00:03:13.680
can also talk about one of the problems
00:03:16.280
with sorting in JavaScript though is
00:03:18.120
that sorting is actually not a pure
00:03:21.040
function in the specification there is a
00:03:24.200
new way of sorting so while the
00:03:27.000
comparator that we actually pass to the
00:03:29.920
function itself so the function we pass
00:03:32.239
to the higher order function needs to be
00:03:34.959
pure sort itself is not pure so this is
00:03:38.040
where two sorted comes in so two sorted
00:03:41.400
is actually a pure version in other
00:03:43.040
words it doesn't modify the actual array
00:03:46.000
itself that gets passed to it it returns
00:03:48.879
a new array and you'll remember I
00:03:51.040
mentioned with spliced and reversed when
00:03:53.519
we were talking about arrays and things
00:03:55.439
that you can do on arrays um those two
00:03:58.720
mutate the thing that gets passed to it
00:04:01.319
which means you can accidentally change
00:04:03.640
the actual parameter that gets passed
00:04:06.159
you know retroactively outside of the
00:04:08.959
function so there are new methods so two
00:04:13.680
sorted two reversed and two spliced are
00:04:17.079
actually pure versions of this and just
00:04:19.440
be mindful that it's not yet supported
00:04:21.600
in all browsers so you'll see it's not
00:04:23.280
supported in Firefox um but in some of
00:04:26.360
the other ones like Chrome it's recently
00:04:28.600
been added but you can see this is
00:04:30.759
literally February 2023 so very very new
00:04:35.360
so you'll have to do two sort if you
00:04:37.039
want a pure version I'm going to use
00:04:38.759
that version but just be mindful that
00:04:41.000
depending on how much browsers you need
00:04:42.520
to support that might be something to
00:04:44.880
consider falter which JavaScript also
00:04:47.639
has so then we have fold so fold
00:04:51.800
effectively and this is effectively flat
00:04:54.160
map so you'll see up here it it refers
00:04:57.560
to a higher order function that analyz
00:04:59.800
is a recursive data structure apply we
00:05:03.199
can do this in JavaScript but the way
00:05:05.320
that JavaScript works we actually don't
00:05:07.320
need to and because we actually want to
00:05:09.039
stay away from this I don't really use
00:05:12.000
apply there is apply in JavaScript what
00:05:14.440
the function composition is we'll speak
00:05:16.960
about that in a second and then there's
00:05:19.000
some other things here the only other
00:05:21.039
one that you should also know is call
00:05:23.240
back so call back is effectively so
00:05:26.639
there's two reasons why you might want
00:05:28.400
to pass a function into another function
00:05:30.639
the one is as a means to resolve
00:05:33.479
something so there's some calculation or
00:05:35.919
something that happens in the function
00:05:37.880
itself and you provide it with logic
00:05:41.080
that it used to resolve that calculation
00:05:43.800
or as a callback so call back is
00:05:45.880
something that's meant to be called at a
00:05:48.919
time in the future callbox callbacks are
00:05:51.639
very related to a synchronous
00:05:54.199
programming and as we get into things
00:05:56.759
like promises and so forth we'll speak
00:05:58.639
about them much more
00:06:00.199
but for now we've mostly been using call
00:06:02.720
backs in the context of event listeners
00:06:06.000
because effectively event listeners are
00:06:07.960
asynchronous they're a way of asynchrony
00:06:10.960
that's built into JavaScript from the
00:06:13.080
beginning in other words you don't know
00:06:14.919
when it's going to run so you give it a
00:06:16.639
function that it should run that can
00:06:18.880
have side effects whenever the
00:06:21.440
conditions are met so the next thing I
00:06:23.800
want to look at is function composition
00:06:27.520
that's similar to the array that we just
00:06:29.680
create it instead of taking strings and
00:06:32.960
combining them in some way let's say you
00:06:35.360
pass two two numbers to something and
00:06:38.360
then you want to perform something on
00:06:40.039
those numbers so one way to write this
00:06:42.639
would be let's just call it calculate
00:06:45.800
and it takes it takes num one and num
00:06:49.039
two okay and then it takes an operation
00:06:53.160
and let's say if operation equals plus
00:06:58.599
then return num 1+ num 2 if operation is
00:07:04.960
minus then return num1 minus num 2 and
00:07:09.879
then if operation is multiply return num
00:07:15.000
one multiplied by num two so obviously
00:07:18.360
this is a very contrived example and the
00:07:21.199
reason why I started with that spacing
00:07:24.520
component first is because I wanted to
00:07:26.599
show you an actual real example where
00:07:28.800
you would use this because usually when
00:07:31.080
I start with like a contrived example
00:07:33.080
like this like the general response
00:07:34.960
would be like okay I guess this is nice
00:07:37.039
but I I don't really see why you would
00:07:38.960
want to do this so I started with the
00:07:40.479
why and now I'm just doing a much more
00:07:42.160
basic example to show you actually the
00:07:45.159
actual Concepts underpinning that so
00:07:48.560
operation equals divide so this is a
00:07:52.240
very very very basic function and then
00:07:55.800
you know at the end we can just if it
00:07:57.759
reaches this point we can throw a new
00:07:59.520
error that is just invalid operation
00:08:02.720
passed so we can assume at this point
00:08:05.400
that something was passed that's not one
00:08:07.479
of these things so let's do calculate at
00:08:10.319
10 20 and let's say plus so that should
00:08:13.560
be 30 there we go okay let's do the same
00:08:16.560
for multiply and then obviously if we do
00:08:20.639
something like that throws an error but
00:08:23.720
this doesn't really give us much room to
00:08:26.479
do anything else unless it's
00:08:28.599
specifically built n so let's say you
00:08:30.840
want to do modulus so if you remember
00:08:33.080
modulus is this so it's if you do the
00:08:36.440
percentage and it shows how much is left
00:08:39.200
over after the calculation so if we do
00:08:42.519
you know modulus and let's do five and
00:08:45.360
we divide it by two so one should be
00:08:47.360
left okay and so forth and so forth and
00:08:50.000
so forth and you might look at this and
00:08:52.040
through the lens of single
00:08:53.399
responsibility principle you might be
00:08:55.160
like yeah this has a single
00:08:56.320
responsibility it's just it just takes
00:08:58.360
two numbers and it performs a
00:09:00.079
calculation on them that's a single
00:09:02.000
responsibility but you can actually take
00:09:04.240
a step back and actually see that
00:09:05.920
there's two responsibilities here
00:09:07.800
there's the responsibility of actually
00:09:10.320
doing something on two numbers and then
00:09:12.920
a second responsibility is figuring out
00:09:16.160
what should actually be done on those
00:09:18.160
numbers so if we use a high order
00:09:20.399
function we actually split those up into
00:09:22.519
two different responsibilities which
00:09:24.880
actually provide us much more
00:09:26.680
flexibility and reuse in other words
00:09:29.160
like it's a much resilient and solid
00:09:32.440
abstraction so how would we do this
00:09:35.120
using higher order functions so we would
00:09:37.360
do calculat are very similar and num one
00:09:40.360
and num two but operation would actually
00:09:43.680
be a higher order function that we pass
00:09:45.600
through we can literally just do it as
00:09:47.800
follows check if operation is actually a
00:09:50.040
function so we can say type of operation
00:09:53.519
is not a function then throw an error
00:09:55.880
throw new error uh so otherwise we can
00:09:59.800
assume it's a function and what we can
00:10:01.240
do is we can return running operation on
00:10:04.640
num one and num two so that just means
00:10:07.760
we pass this as a function and so num
00:10:09.839
one num two and what do we do with that
00:10:12.880
let's say we multiply it give us a a bit
00:10:16.880
of flexibility in terms of if we maybe
00:10:19.160
want to do num one plus num one and then
00:10:22.480
multiply it so these are two different
00:10:24.959
concerns and not only that it maybe
00:10:27.760
allows us we can even even split this up
00:10:30.200
into two functions so we can create a
00:10:33.120
Handler up here so let's just create the
00:10:35.760
process of adding as a actual function
00:10:38.720
in itself let's just make this an actual
00:10:40.839
function and you know let's further
00:10:42.959
extend it so here's another concept from
00:10:45.800
functional programming and that is and
00:10:47.839
that's currying or partial application
00:10:50.440
so sometimes people get confused with
00:10:52.120
currying and partial application partial
00:10:54.560
application is the general term or the
00:10:57.160
concept currying effectively is a
00:10:59.519
specific implementation of partial
00:11:01.800
application that effectively is just
00:11:04.399
means you only pass a single parameter
00:11:08.079
argument at a time whereas with partial
00:11:10.120
application you can do however many you
00:11:12.480
want so it's just a very specific
00:11:13.880
implementation of it uh people sometimes
00:11:16.360
use them interchangeably but so what
00:11:18.160
that means is we can wrap this we can
00:11:20.800
use this to actually create specific
00:11:24.120
calculation functions for us so let's
00:11:26.639
just say create Cal and it just takes
00:11:29.040
the operation and it returns a new
00:11:31.560
function that takes numbers and let's
00:11:34.000
actually say it takes an array of
00:11:36.399
numbers okay so let's do numbers so we
00:11:39.120
can still keep this over here what we
00:11:41.160
can also check for is if numbers length
00:11:45.399
is less than two throw new error numbers
00:11:49.360
needs so what this now actually does for
00:11:52.240
us is it actually partially creates the
00:11:56.800
function for us so it's effectively say
00:11:59.240
so this let me write it like this so
00:12:01.160
it's may be easier to read if you're not
00:12:02.760
used to this so you have a return in
00:12:05.480
there that when you run this function
00:12:07.800
returns another function we can even
00:12:10.000
let's just call it like you know inner
00:12:11.560
function so that we create it in the
00:12:13.519
closure and then we return it obviously
00:12:16.199
it's just way easier to write it like
00:12:18.120
this each step you partially applying
00:12:20.760
something so this is this is effectively
00:12:23.440
currying cuz we're applying one argument
00:12:26.399
at a time so what this allows us to do
00:12:29.480
so let's first so operation and this is
00:12:32.440
where reduce also comes in so what we're
00:12:35.199
going to do is let's just do result here
00:12:39.079
and let me just do reduce uh reduce is
00:12:41.639
kind of like the multi-tool of higher
00:12:44.199
order functions you can do anything of
00:12:46.160
reduce and after this example I'm going
00:12:48.480
to talk about the different high order
00:12:49.959
functions and also reduce and reduce is
00:12:52.320
usually the one that people struggle
00:12:53.959
with the most because it is the most
00:12:56.120
powerful um and so it gives you a lot of
00:12:58.279
flexibility but because of that people
00:12:59.839
really struggle with it so what we do is
00:13:02.480
we do numbers and reduce so the
00:13:05.920
accumulator okay but this reduce is
00:13:07.920
going to seem really scary um and we're
00:13:10.600
going to tackle it at the end so I can
00:13:12.279
explain it but also be a bit patient
00:13:14.320
with yourself it might take a while to
00:13:16.600
understand exactly what a reduce does
00:13:19.199
but I use reducers all the time all over
00:13:22.079
the place in the same way that I spoke
00:13:24.160
about you know 1 + 1 equals 2 if you
00:13:27.120
understand what reduced does it has so
00:13:29.560
expressive it allows you to do such
00:13:32.279
complex behavior in a single line okay
00:13:35.519
but it takes a while to figure out
00:13:37.440
exactly how reduce works and kind of get
00:13:40.120
in that frame of mind in terms of when
00:13:42.199
you see a reduce being able to read it
00:13:44.639
and actually understand what it does so
00:13:46.920
we have the accumulator and then we have
00:13:49.560
the current and basically what we do is
00:13:54.040
we perform the current operation on the
00:13:56.959
accumulator and the current which means
00:13:59.160
means you might have noticed that this
00:14:01.440
means we can actually just pass that
00:14:03.279
directly as is so we run that we reduce
00:14:07.079
we take the numbers we reduce it and we
00:14:09.000
reduce it with the operation return
00:14:11.480
result so what this means is let us
00:14:15.079
create some calculations so let's say
00:14:18.399
add okay so create C and let's pass our
00:14:23.240
operation num one and num two num 1+ num
00:14:27.519
two then we create edit this function
00:14:30.360
that just accepts array an array of
00:14:32.360
numbers and it add and it performs this
00:14:34.480
on all of them let's go 3 4 5 and also
00:14:37.720
this should be numbers once again the
00:14:40.040
fact that we don't have static typing
00:14:41.560
here is letting me down 21 so would that
00:14:44.480
actually be so 3 6 10 yeah 21 and let's
00:14:49.320
change this to just that so not only
00:14:51.480
were we able to express like really
00:14:53.399
complex logic and what is this 1 2 3 4 5
00:14:57.279
6 7 8 9 10 10 11 lines we can actually
00:15:01.519
use that to create like functions that
00:15:05.079
have a lot of like bolt end complex
00:15:07.240
Behavior themselves as well let's create
00:15:09.440
another one and let's say divide so
00:15:11.920
create Kel and num one and num two num
00:15:15.519
one and num two and let's run divide
00:15:19.000
instead of add and let's just make this
00:15:20.800
100 instead and also that should be
00:15:22.880
divide not comma all right so it divides
00:15:24.720
it by half and then it divides so 50 by
00:15:27.639
3 but this is where it get really great
00:15:29.680
and now we're getting to composition you
00:15:31.880
can even combine those two into
00:15:34.560
themselves add and divide and so that
00:15:37.959
creates a new calculation for us that
00:15:40.240
takes effectively num one it adds them
00:15:43.319
first so let's just say in a result to
00:15:46.279
add num one num two and then it turns
00:15:50.480
divide in a result num one and num two
00:15:54.160
it adds them and then it divides by both
00:15:56.399
of them and we return that and so I
00:15:59.360
think let me have a check add and divide
00:16:02.959
plus 50 30 20 and 2 let's just make this
00:16:08.800
just for readability let's make this
00:16:10.720
const result uh let's return result hey
00:16:14.920
okay so obviously like this is extremely
00:16:17.000
contrived I have no idea why you would
00:16:19.000
want to do this ever but this is just to
00:16:20.880
show the principle you know then you can
00:16:22.759
build further on this and further on
00:16:24.480
this so this is what higher order
00:16:26.240
functions really allow us to do there is
00:16:29.000
a library called Low Dash just open low
00:16:31.560
Dash and then go documentation it has an
00:16:33.839
absolute ton of actual like these little
00:16:37.319
composable functions that you can use
00:16:40.000
you so chunk so what does chunk do so
00:16:42.319
chunk creates an array of elements
00:16:45.240
splits it into groups the length of size
00:16:48.399
okay so here it shows an example so you
00:16:51.319
pass this and then it splits it into
00:16:53.000
groups of two and so forth and so forth
00:16:55.680
uh compact so compact removes everything
00:16:59.000
that isn't true or truthy so this looks
00:17:02.759
at you know what is different between
00:17:05.439
these two so obviously one A Difference
00:17:07.760
by uses higher order functions to
00:17:10.520
actually allow you to do much more
00:17:12.679
complicated things so exactly what we
00:17:15.160
did in our previous version so it
00:17:16.559
actually passes math flaw so the built
00:17:19.039
in function in JavaScript to actually
00:17:22.319
calculate the difference and you can go
00:17:24.799
down here and you know so there are a
00:17:27.039
couple of things that are actually built
00:17:29.679
into JavaScript uh so don't pull in low
00:17:33.360
dash for those things so for example
00:17:35.880
flatten um which does what flat gives us
00:17:38.559
by default and the reason for this is
00:17:40.880
obviously low Dash is already at version
00:17:42.880
four so it's been along around for a
00:17:45.160
very long time um low Dash was obviously
00:17:47.760
created before before flat itself in
00:17:51.120
JavaScript existed so this was added to
00:17:54.080
low Dash before that but obviously it
00:17:55.919
needs to keep it in here because it
00:17:57.440
can't just go like okay this is
00:17:58.960
JavaScript now uh so we should remove it
00:18:01.520
cuz then obviously existing projects are
00:18:03.200
going to break so some of these you can
00:18:05.600
actually now do with JavaScript itself
00:18:07.440
but there's a ton that you can't so for
00:18:09.200
example intersection so what
00:18:11.039
intersection does is you know you pass
00:18:13.559
two arrays and then it actually gives
00:18:16.360
you then it returns a new array that is
00:18:19.640
what is actually in both these so these
00:18:22.400
are all that take arrays collection
00:18:24.880
takes arrays or objects date uh
00:18:29.400
yeah I I don't know like this I don't
00:18:31.120
really use date there's only one um
00:18:34.240
functions this allows you to do things
00:18:36.000
like here's one for currying um
00:18:38.640
memorization so these some of these are
00:18:40.840
very Advanced and then these are like
00:18:43.559
just general Expressions so equal
00:18:46.320
there's a ton of sof there's specific
00:18:47.919
math stuff once again add so as we as we
00:18:50.760
had here okay so why like this seems
00:18:53.080
excessive like why do you have that so
00:18:55.200
also keep in mind the way that low Dash
00:18:57.400
gives it to us is that it's very easy to
00:18:59.720
use as higher order in higher order
00:19:02.039
functions so while in JavaScript
00:19:04.799
obviously it's very easy to do ad you
00:19:06.559
don't need low dash for that because you
00:19:08.640
can just do 10 + 2 who needs low Dash
00:19:11.720
but let's say you want to do a high
00:19:13.159
order function so as mentioned that
00:19:15.280
reduce so let's say we have all these
00:19:17.960
things 2 3 4 whatever and we want to add
00:19:21.440
all of them together having add as an
00:19:23.960
actual function is really cool CU you
00:19:25.799
can just pass it to that and it's going
00:19:27.760
to add all of them for for you together
00:19:29.960
exactly in the way that we did so this
00:19:32.000
is very expressive but like in this case
00:19:34.080
I wouldn't pull in low Dash I would just
00:19:36.679
go create my own one because this is
00:19:38.400
simple enough you know I can just do num
00:19:40.159
one num two num one plus num two and
00:19:44.240
just do that and it's just unhappy
00:19:46.840
because we're not doing anything with it
00:19:48.480
so let's actually just run that so this
00:19:49.840
is what low Dash would give us and this
00:19:51.720
is just to explain like why it's
00:19:53.559
sometimes useful to have like things
00:19:55.640
like this as actual functions that you
00:19:58.280
can pass around even if you do have the
00:20:00.600
ability to go you know 10 + 2 in
00:20:04.360
JavaScript some but in most cases where
00:20:06.799
it's just something as simple as this I
00:20:08.480
would just create this myself I wouldn't
00:20:09.880
pull in low Dash but there are more
00:20:11.760
complex things like intersection and so
00:20:14.240
forth that's a bit harder to do in
00:20:15.880
JavaScript so let's just console log
00:20:17.840
that there we go so it added all of
00:20:19.600
these together um then there's some
00:20:21.320
other things some stuff you can do with
00:20:23.120
numbers you can check if it's in the
00:20:25.240
range of specific numbers uh stuff you
00:20:27.840
can do specifically with objects um and
00:20:30.679
then down here some really cool stuff
00:20:32.240
you can do with strings and I actually
00:20:33.400
use these a ton so you can convert
00:20:35.440
something to camel case convert it to
00:20:37.799
Kebab case turn the first thing to
00:20:40.360
lowercase uh pad start and so forth this
00:20:44.280
was before JavaScript had um pad start
00:20:47.520
in it uh but even though now it's
00:20:50.679
actually maybe useful to just have this
00:20:53.000
as an actual function that you can pass
00:20:55.679
instead of a method that you can perform
00:20:57.679
on a string okay so there's a ton of
00:20:59.799
stuff here you can check it out um there
00:21:01.919
is also I just I'm not going to show it
00:21:04.679
um because I think then we're getting
00:21:06.080
too deep into the world of actual
00:21:08.280
functional programming um you can
00:21:10.320
definitely check these things out
00:21:11.919
yourself if you want um I do a ton of
00:21:14.320
them I do a lot of functional
00:21:15.720
programming but I don't think it's
00:21:18.240
necessary to learn some of these things
00:21:20.480
if they don't really interest you or if
00:21:22.760
it's not the type of style programming
00:21:24.559
style that you want to develop for
00:21:26.000
yourself there is specific methods that
00:21:28.320
you can use that really help with
00:21:30.440
functional programming allows you to
00:21:32.799
actually compose things so let's search
00:21:34.400
for flow so these you'll see they're
00:21:36.279
also utilities themselves so they just
00:21:38.919
allow you to combine functions so you
00:21:41.320
can combine add and square so that part
00:21:44.799
in the end where we actually went and we
00:21:46.919
combined add and divide to create and
00:21:49.440
and divide uh so it just allows you to
00:21:51.919
do it like in this manner I don't know
00:21:54.400
like unless I'm using like a full on
00:21:56.600
functional programming I often find that
00:21:58.880
in JavaScript this maybe confuses people
00:22:01.760
more than if I just do it in the way I
00:22:03.600
did it previously there's a really great
00:22:06.200
book um that I recommend you guys maybe
00:22:09.039
check out um if you're interested in
00:22:11.440
some of these functional programming
00:22:13.120
principles by Jamon Clair so he does a
00:22:16.200
lot of really great writing he has a
00:22:18.600
book called um functional a skeptic's
00:22:21.279
guide to functional programming um and
00:22:23.919
it's a really great book um I like the
00:22:26.440
subtitle that says how to level up your
00:22:28.279
Cod without alienating your team so you
00:22:31.279
know like there is a balance here
00:22:32.919
there's a balance between the deeper you
00:22:35.120
go into functional programming you're
00:22:36.679
going to learn a lot of these
00:22:37.919
superpowers that allow you to write a
00:22:39.760
really concise really dense and
00:22:42.240
expressive code but obviously as someone
00:22:45.600
if someone doesn't understand some of
00:22:47.200
the underlying principles it's going to
00:22:49.080
be even more confusing so that's always
00:22:50.919
a balance to strike if you write your
00:22:53.039
code in that manner but the rest of your
00:22:55.200
team doesn't understand that way of
00:22:57.480
writing code it's actually going to make
00:22:59.120
your code worse that's something just to
00:23:01.559
be mindful of I really enjoy functional
00:23:04.080
programming I really enjoy like going
00:23:06.840
deep into functional programming in the
00:23:08.919
realm where you start doing these type
00:23:10.480
of things but if you don't have
00:23:12.720
experience in it it can actually make
00:23:14.480
the code harder to read so a bit of
00:23:16.799
functional programming here and there is
00:23:19.159
really great I would always strive to
00:23:21.720
keep code AS functional as possible as
00:23:24.559
little side effects as little mutations
00:23:26.840
so pure functions and so forth
00:23:29.120
but once you get into kind of the world
00:23:30.919
of academic functional programming in
00:23:33.480
other words where you're treating your
00:23:34.799
code like
00:23:35.919
mathematics I think you need to be
00:23:37.760
mindful like how readable is the code
00:23:40.440
still okay so that's just like something
00:23:42.720
to be mindful of but similar to object
00:23:45.039
orientated programming I find that
00:23:47.279
bringing a bit of it in is really
00:23:49.400
helpful the same with functional
00:23:50.760
programming bringing a bit of it into
00:23:52.679
your code is really helpful and I'm
00:23:54.919
going to talk in the next lesson about
00:23:56.679
State machines and I find it to be the
00:23:58.480
exact same thing bringing a bit of State
00:24:00.960
machine logic into your code is really
00:24:02.760
helpful but I think if you pursue any
00:24:05.760
three of these in full and just try and
00:24:09.279
write everything as a state machine try
00:24:11.720
and write everything as functional code
00:24:14.240
try and write everything as o op unless
00:24:18.120
you have a team that also subscribes to
00:24:21.120
that almost dogmatic approach it's
00:24:23.960
really going to alienate people and it's
00:24:25.559
going to make your code very hard to
00:24:28.120
read spe for the general person unless
00:24:30.399
they are in that world of like extreme o
00:24:33.840
or extreme functional programming or
00:24:35.919
extreme State machines themselves so
00:24:38.520
let's go back to that fig Jam that I did
00:24:41.279
way back when we spoke about arrays and
00:24:43.799
let's return to the actual higher order
00:24:47.480
functions there and now we can start
00:24:48.880
talking about them