00:00:00.080
all right so if we go all the way back
00:00:02.360
here to some of the higher order
00:00:04.759
functions so just to recap so we spoke
00:00:07.520
about all of this we spoke about you
00:00:09.320
know length versus item index versus key
00:00:12.759
how to check items in an array so we
00:00:14.799
looked at some methods check um we
00:00:17.560
looked at some methods to add or remove
00:00:19.359
things from arrays how to change the
00:00:21.359
structure of arrays and we spoke a bit
00:00:23.680
about mutating and new arrays and so
00:00:26.800
forth and so forth translating between
00:00:29.480
objects and arrays and then higher order
00:00:33.280
functions and you'll see I actually
00:00:35.399
marked up here talk later and now is
00:00:38.200
talk later and so let us start talking
00:00:40.640
about these high order functions that
00:00:42.760
come with arrays and also now with the
00:00:46.199
new knowledge that you have you should
00:00:47.520
also understand what that dot prototype
00:00:50.440
means in mdn that effectively means that
00:00:53.879
this comes along on the array prototypes
00:00:57.239
if you do 1 2 3 Dot you're going to have
00:01:01.120
this as part of the Prototype that comes
00:01:03.399
along and you're going to be able to do
00:01:05.438
any of this on any array because
00:01:08.200
remember it's going to look for that
00:01:10.119
method and fall back all the way to the
00:01:12.360
Prototype okay so let us start working
00:01:15.640
our way through this with the example of
00:01:19.040
actual tasks so let's create some tasks
00:01:22.320
here in an array and then I will show
00:01:24.360
you how we can use higher order
00:01:25.720
functions to transform that data uh
00:01:28.840
let's just say task and that is an array
00:01:32.200
of actual tasks and we let's just put a
00:01:35.000
uyu ID here title is you know wash the
00:01:38.840
dog urgency let's say hi dog is really
00:01:42.960
smelly then we have another one let's
00:01:45.360
say celebrate New Year's and the due
00:01:48.880
date first of yet January
00:01:51.960
0101 urgency is low and let's just add
00:01:56.439
one more learn JavaScript well let's say
00:01:59.640
that date is at the very least before
00:02:03.520
2025 and that is for title and let's
00:02:08.119
just say clean room and it has no due
00:02:11.120
date and urgency say the urgency is low
00:02:15.239
first and foremost find so this returns
00:02:17.840
a value of the first element that
00:02:20.480
matches the specific function that we
00:02:22.879
passed to it is let's say we want to
00:02:25.599
find the first thing that is urgency low
00:02:28.840
const result
00:02:30.400
equals tasks find and then we just pass
00:02:33.840
a function into that so the item so it
00:02:36.480
Maps over each item it Loops over each
00:02:38.840
item and then whenever the function
00:02:41.360
returns true uh we call this a predicate
00:02:45.400
uh in programming function that runs and
00:02:48.280
that can resolve to true or false you
00:02:51.120
actually get a lot of higher order
00:02:52.360
functions that use a predicate to
00:02:54.040
determine when it should stop looping or
00:02:56.239
when it should do something or so forth
00:02:58.080
all that we want to say is we can say
00:02:59.959
item do urgency is low and so then that
00:03:04.120
is going to return this one so it's
00:03:06.720
going to stop once it finds it it's not
00:03:08.560
going to continue to the other one but
00:03:10.560
let's say we want to make the we want to
00:03:12.599
specify the condition so let's just say
00:03:14.959
so we can say return item urgency is low
00:03:18.280
and there is no due date so then it's
00:03:20.959
going to skip this one because it has a
00:03:23.120
due date so it's going to check is this
00:03:24.840
true no is this true no is this true no
00:03:28.280
is this true yes okay so it's going to
00:03:31.159
return that object for us and so
00:03:33.879
obviously if we pass true then obviously
00:03:36.920
the very first one is going to result in
00:03:39.920
true uh if you pass false um it's not
00:03:43.000
going to find any um because it's just
00:03:45.400
going to the predicate is just going to
00:03:46.879
return to false on each Loop then so
00:03:49.519
four each uh we already spoke about so
00:03:53.239
these are mostly if you want to do side
00:03:55.400
effects because they don't return
00:03:57.159
anything so if we you know for example
00:03:59.439
do for each on this uh results is going
00:04:02.319
to be nothing it's not going to return
00:04:03.920
anything uh so this is usually for side
00:04:06.360
effects so let's say for example you
00:04:08.000
want to conso log the ID each time okay
00:04:11.560
and so you can even write it like this
00:04:13.519
you know you can pass it directly like
00:04:15.680
that and then it's just going to so this
00:04:17.918
is once again this is the beauty of uh
00:04:20.440
functional programming is you can
00:04:21.959
express it like tasks so it actually
00:04:24.919
reads like natural language so tasks for
00:04:29.160
each conso log so each task conso log if
00:04:32.479
we were to do this with a for Loop uh it
00:04:34.880
would be as follows you know we'd have
00:04:36.240
to go for and we do cons uh single task
00:04:40.479
of tasks and then we have to say console
00:04:43.560
log single task so this reads a lot more
00:04:46.919
naturally as well so the next one is map
00:04:51.000
and so map is effectively the same as
00:04:54.039
for each but the big difference is it
00:04:58.400
expect something in response let's say
00:05:01.520
we want to add onto each array so bring
00:05:05.000
this back where we do this more
00:05:07.479
explicitly so map goes over each item
00:05:10.199
performs a function on it and returns a
00:05:12.479
new array with the result of the
00:05:14.800
function so we would do const result
00:05:18.000
equals 4 each so instead of four each we
00:05:21.120
would do tasks map okay and we can get
00:05:24.039
each item let's say we want to return
00:05:26.880
the item itself or let's say we want to
00:05:29.440
return turn we want to add something
00:05:31.240
onto it let's say we want to add two
00:05:33.240
more properties on it so we can
00:05:34.440
destructure the current one and let's
00:05:37.120
actually add is Task and that is going
00:05:40.319
to be true on all of these CU all of
00:05:42.600
them are tasks and let's maybe also add
00:05:45.520
you know has Dash and so what we can do
00:05:48.840
is we can actually just go the current
00:05:51.120
item Does it include a dash okay so
00:05:54.639
it'll create a new object so for example
00:05:57.120
this one it has a dash and this one had
00:05:59.400
does doesn't in the new like array it
00:06:02.479
will effectively be you know his task is
00:06:04.319
going to be true and has Dash is going
00:06:07.960
to be false and here it's going to be
00:06:11.479
true and map is the one you actually use
00:06:14.759
the most uh spe especially with HTML and
00:06:18.560
so forth and let me quickly show you why
00:06:21.199
so let's just do basic HTML um we're not
00:06:24.360
even talking about um you know lit or
00:06:27.319
whatever so let's just say we have
00:06:29.840
document body uh inner HTML this is just
00:06:33.680
plain HTML like no lit no nothing and we
00:06:36.720
have an unordered list and we want to
00:06:39.000
put something inside that unordered list
00:06:41.520
so all that we can do is up here let's
00:06:43.919
just create the list we can just
00:06:46.400
interpolate it in there and so let's
00:06:48.400
base that off our tasks so let's say
00:06:50.560
tasks and what do we return we just
00:06:53.000
return template literal that has Li and
00:06:57.039
item. title and
00:07:00.080
and let's maybe just put urgency in
00:07:02.520
there so then this is going to create
00:07:04.520
this for us and the only thing we need
00:07:06.039
to do is here because this is an array
00:07:08.960
uh we need to just join it to be a
00:07:11.720
string but in lit and so forth you don't
00:07:14.720
need to it actually accepts arrays as
00:07:17.360
actual expressions of HTML so this is
00:07:20.479
quite common and you can even if you
00:07:22.440
want you can destructure it up here and
00:07:25.199
go you know title urgency and then just
00:07:28.440
do this and so so another thing as well
00:07:30.720
is all of these almost all of these the
00:07:34.199
first argument is the item and the
00:07:36.840
second argument is the index we can
00:07:39.120
maybe even so it passes the index as
00:07:41.240
well so this would be 0 2 and three and
00:07:43.919
let's say either this let's do an F
00:07:46.800
statement here let's say if index is
00:07:49.800
bigger than one return remember this is
00:07:53.360
a predicate so we just say false or true
00:07:56.319
um so that means it's going to be 0er
00:07:58.560
one and then this one is going to get
00:08:00.319
returned before it can even get to this
00:08:02.360
one so all of these are the same here
00:08:04.599
you know we can even add index and let's
00:08:07.000
say we even just want to add the actual
00:08:08.840
index onto the thing itself and so there
00:08:11.919
we go this is the Shand assignment so
00:08:14.960
effectively what sum does sum so this is
00:08:17.520
very similar to includes over here you
00:08:20.120
know so we check does the string have
00:08:23.000
that um so let's say we want to check
00:08:26.000
you know has urgent whether there is a
00:08:29.800
task that like whether a list of tasks
00:08:32.000
has a task that is urgent so you can't
00:08:34.679
do tasks include because include only
00:08:39.000
looks at the values it can only look at
00:08:41.519
primitive values so unless we actually
00:08:44.000
have a reference to this one so the only
00:08:46.839
case where we can actually do something
00:08:48.360
like this is you know U if we have you
00:08:50.279
know example and then we put example and
00:08:53.839
then we put example in the array and
00:08:55.959
then we just want to check does the
00:08:57.320
array include example cuz remember this
00:08:59.200
is a reference uh we can't go you know
00:09:02.120
does it have like does it look like this
00:09:05.200
it needs to be a reference so we can't
00:09:06.959
go like that so but the way you do that
00:09:09.800
is by means of a high order function so
00:09:13.160
we can go item and it's also a predicate
00:09:15.720
all that we do is we do if item and also
00:09:19.240
this does not include sum so if sum in
00:09:22.200
other words at least one item meets this
00:09:24.959
condition urgency equals Pi so if
00:09:28.079
there's at least one that meets this
00:09:30.440
condition and we actually don't need to
00:09:31.640
say if we can actually just write it
00:09:33.399
directly like that and if we want to go
00:09:35.560
really like expressive we can go uh we
00:09:38.680
can use actually curring and partial
00:09:40.880
application to say you know has urgency
00:09:44.680
and we pass a value and then we actually
00:09:48.240
just create a new function that takes
00:09:50.360
the item and checks if that item urgency
00:09:54.279
equals the value that we passed so check
00:09:56.320
this this is really cool so we can
00:09:58.720
actually you know consel log let's
00:10:01.079
create a object that we just conso log
00:10:03.560
and let's just say you know has high has
00:10:07.600
normal has low then we go tasks sum and
00:10:12.079
then we use partial application or
00:10:14.519
crying in this case to actually create
00:10:17.680
the predicate in there so then we go you
00:10:20.360
know has urgency once again if we did
00:10:23.079
this with the loop it would have been
00:10:25.120
much less expressive and this is also
00:10:27.279
reusable so if we add another urgency we
00:10:30.920
can probably even abstract this if you
00:10:32.480
want and just pass in has urgency you
00:10:35.120
know go like uh check items or let's
00:10:38.399
just say uh operation arrays and then we
00:10:41.560
can just map over the arrays and then we
00:10:44.000
just pass the operation directly to that
00:10:45.959
we can even write it actually as this oh
00:10:48.160
no sorry I should actually do it the
00:10:49.560
other way around so the operation so we
00:10:51.560
map over the operation and that gives us
00:10:53.920
a function and then we run that function
00:10:56.720
with the single array so like that so
00:10:59.880
console log items the tasks and then we
00:11:03.320
just pass an array of operations okay
00:11:06.399
and we can do it like that there's lots
00:11:08.800
of different ways in which you can
00:11:10.360
actually compose things U and you'll see
00:11:12.800
this starts looking a bit like that
00:11:14.839
example that we had where we had
00:11:17.000
employees and we had the government
00:11:18.959
inspectors and you know we had that code
00:11:21.040
space um inspection events and so forth
00:11:24.120
and we pass a employee into an event and
00:11:27.040
so forth so once again you know we're
00:11:29.639
we're looking at encapsulation and
00:11:31.760
polymorphism here but since we're not
00:11:34.600
doing oop and in oop you're passing
00:11:37.040
objects around so you're passing objects
00:11:39.000
into objects so you know we're passing
00:11:42.160
employees into events here we're passing
00:11:46.200
functions into other functions so we're
00:11:48.399
passing has urgency into some and then
00:11:51.120
we're passing that custom operation into
00:11:53.839
check items and that gives us the result
00:11:55.959
so you compose all these functions
00:11:58.440
together we're not assigning a variable
00:12:00.440
any place and it just splits out the
00:12:02.800
result for you so you know like it's
00:12:04.760
also by this means by which something
00:12:06.600
like react works so react has your state
00:12:10.000
and you literally just you know have
00:12:12.079
your logic and UI uh you compose
00:12:15.560
components um and you know so if you
00:12:18.279
treat your components as functions then
00:12:22.079
effectively this is just one big
00:12:24.120
function that runs on your state each
00:12:26.480
time and every time the State updates it
00:12:28.360
just creates a new UI so there's just
00:12:31.240
one object here so this is why react you
00:12:34.399
would say react follows a functional
00:12:37.160
programming uh Paradigm because
00:12:39.040
effectively everything you write is just
00:12:41.440
one big function and in react that
00:12:43.680
function is usually just called app okay
00:12:46.320
and at some other functions that get
00:12:48.360
composed into it and so forth so your
00:12:50.839
app itself is like like this you know
00:12:52.600
it's just all these composed components
00:12:54.720
all the way up and down so there's also
00:12:56.320
different ways of thinking about
00:12:57.680
components so in angular you think about
00:12:59.800
components as classes um in react a
00:13:02.519
component is a function angular tends to
00:13:05.199
be a bit more o op and react tends to be
00:13:08.920
a bit more functional programming but as
00:13:11.199
I mentioned you know um be careful like
00:13:14.120
none of these are too dogmatic um
00:13:16.720
angular has a bit of functional
00:13:18.160
programming react has a bit of oop you
00:13:21.199
can never really write JavaScript by
00:13:22.760
neglecting one completely so let's look
00:13:25.360
at some more so sort so every so every
00:13:28.880
is exactly the same as Su uh the only
00:13:31.480
difference is that instead of checking
00:13:33.920
if sum if a a single one has an urgency
00:13:38.360
of high at least it checks does all of
00:13:41.040
them have an urgency of high so this is
00:13:43.720
going to be false but what we can maybe
00:13:45.480
do is we can maybe check is Task and
00:13:48.040
this is going to be true because all of
00:13:49.639
them if we map over them so that example
00:13:52.120
we had in that example all of them has
00:13:55.279
task so let's Al change this to every
00:13:57.480
okay uh what falter does is we have I
00:14:00.759
think we have used filter before uh you
00:14:03.079
can do tasks and you know filter and
00:14:06.399
item and let's filter out all the tasks
00:14:09.880
that don't have dates so effectively
00:14:12.399
just item. do we can just say the
00:14:15.600
opposite so in other words it Maps over
00:14:17.800
each item this condition needs to be
00:14:20.279
true for it to keep the item in the
00:14:22.759
results so in other words it shouldn't
00:14:25.639
have a due so we're looking with dates
00:14:27.880
that don't we're looking at tasks that
00:14:29.720
don't have a due date so it'll create a
00:14:31.959
new array for us where it just
00:14:34.800
removes this one and that one and just
00:14:37.880
has the two that don't have dates
00:14:40.000
likewise if we do the opposite so the
00:14:42.040
predicate if it's yes it keeps it if the
00:14:44.720
predicate is false then it actually
00:14:47.120
removes it and so sort is a bit trickier
00:14:50.120
and also as mentioned keep in mind that
00:14:53.519
I did mention that sort uh by default is
00:14:57.759
like does mutate so in AR C what we want
00:15:00.440
to do is to sort which is the new one
00:15:03.240
that was added this just reorders things
00:15:06.040
for you in the array it's not a true
00:15:08.399
predicate in the sense that it doesn't
00:15:10.040
take true or false it actually takes 0 1
00:15:13.680
or minus one so let us look at the
00:15:17.560
actual documentation for sort on mdn so
00:15:21.120
for sort and both reduce um I will just
00:15:24.959
like look at the documentation here
00:15:27.199
because um both of these are a bit
00:15:29.440
harder to explain so yeah let's dive
00:15:32.000
into them just a bit deeper so
00:15:34.160
effectively sort sorts elements in place
00:15:38.120
so this effectively means what I
00:15:40.920
mentioned about mutating and so forth so
00:15:42.959
it actually changes the elements in the
00:15:45.759
actual array itself um I mentioned that
00:15:48.319
two sorted um has been added as a actual
00:15:52.480
pure way to do that so a way that
00:15:54.880
returns a new array instead of actually
00:15:57.560
updating the current one that you run it
00:16:00.000
on uh which is what you should avoid so
00:16:03.160
here is an example so I did mention sort
00:16:06.079
works with Zer minus one and one so it's
00:16:09.759
not a true predicate in so far that it
00:16:12.600
returns true or false uh so here is an
00:16:16.279
example and and just keep in mind as
00:16:18.639
mentioned here it performs it on the
00:16:20.199
array itself but we will probably be
00:16:22.959
using to sort it to return a new array
00:16:27.319
well that's what I prefer to do
00:16:29.519
so over here when you arrange this March
00:16:33.519
Jan Feb and December it arranges it
00:16:36.720
alphabetically so if you run sort on it
00:16:38.959
so obviously DJ M and so here's the
00:16:42.480
important thing it arranges numbers also
00:16:46.199
based on the characters so this is
00:16:48.680
something to keep in mind so if you just
00:16:50.880
run sort without any passing anything
00:16:53.920
into it it's going to treat these as
00:16:56.480
characters this number comes before this
00:16:59.680
because it starts with the one character
00:17:02.600
uh in the same way that it looks at the
00:17:04.400
characters the starting characters of of
00:17:06.880
the words over here but it's very rare
00:17:09.640
that you just run sort like this unless
00:17:12.119
you just want something to be
00:17:13.760
alphabetical uh more often than not you
00:17:16.039
pass a compare function into it which is
00:17:19.199
you know makes it a higher order
00:17:20.799
function and that function defines the
00:17:23.359
sort order sort is a bit different than
00:17:26.480
some of the other higher order functions
00:17:28.160
in so far that it gives you two
00:17:31.760
arguments and those arguments are of the
00:17:34.240
actual items in the array doesn't need
00:17:37.160
to be one or minus one it actually needs
00:17:41.000
to be any value above zero or any value
00:17:44.440
below Z but for obvious reasons almost
00:17:47.080
everyone just uses minus one and one and
00:17:49.520
zero effectively you take these two
00:17:51.880
things if you return zero then it keeps
00:17:55.679
the order that they are in if you return
00:17:58.320
less than Z puts the first one before
00:18:01.760
the second one if you return more than
00:18:04.440
zero it Returns the second one before
00:18:06.799
the first one so this is usually what
00:18:08.960
you would write it as the reason why it
00:18:11.799
uses this kind of weird way instead of
00:18:14.400
true or false or something is because
00:18:17.640
that allows you a means to actually do
00:18:21.280
to actually do numbers let's just start
00:18:23.559
with a basic example first so let me
00:18:26.520
just do John skull
00:18:29.360
Alice Alice and C4 and George and so
00:18:34.760
let's do two sorted okay so if we just
00:18:39.000
run that as is without passing anything
00:18:41.440
it will sort them in alphabetical order
00:18:44.000
okay but so as mentioned uh the problem
00:18:46.559
is if we just run sort on you know 1 2 3
00:18:51.559
100 uh 2,000 let's do four here and
00:18:55.360
let's do 20 there the problem is we'll
00:18:58.280
treat these as strings so by default it
00:19:01.960
will actually you know look at the
00:19:03.640
actual characters so if we actually want
00:19:07.080
to sort it based on the actual amount
00:19:09.760
this is why it's useful to have that
00:19:12.480
negative or positive number thing
00:19:14.960
because effectively then we pass a
00:19:16.640
function in and we can just do a and b
00:19:19.760
so in other words it just Loops through
00:19:22.480
the items and then it Compares each one
00:19:25.159
of them all that we do is we do a minus
00:19:27.400
B and B minus a for the other way around
00:19:31.760
you can always just go to reversed as
00:19:35.320
well you want to as well so what happens
00:19:38.679
here so effectively it takes one and it
00:19:43.080
minuses four from it that means that
00:19:47.360
it's a negative number it's minus 3 so
00:19:49.480
it's less than zero so that means it
00:19:52.080
puts a in front of B so it kind of keeps
00:19:54.400
the order that it is then it go it takes
00:19:57.960
four and it minuses 20 from it and that
00:20:00.919
also gives a negative number so it keeps
00:20:03.120
it the way it is it takes 20 and it
00:20:05.600
minuses three so that will give a
00:20:08.799
positive number it will give 17 which
00:20:11.559
means that it actually swaps it around
00:20:13.520
so then it puts B in front of a
00:20:16.840
essentially we can say that if it's Zer
00:20:19.880
or lower than zero so let's say you know
00:20:23.880
Z or lower than zero then it keeps it in
00:20:27.200
place if it is more than zero then it
00:20:30.559
swaps it around we can use so you can do
00:20:33.919
this but then like for numbers but you
00:20:36.120
can also manually set this so we can say
00:20:39.559
that you know let's say we have a true
00:20:43.640
false true true false false and let's
00:20:48.400
say we want to order these so two sorted
00:20:52.320
and we can effectively just say and just
00:20:55.200
have the following condition so we can
00:20:57.240
say that if so let's assume by default
00:21:01.840
we want all the TRS and then we want all
00:21:04.120
the falses so we can say if a is false
00:21:09.720
and B is true then return one otherwise
00:21:15.200
just return zero in other words keep it
00:21:16.960
in place oops and we need to say minus
00:21:19.679
one not there we go so all right and
00:21:24.240
then obviously we can just swap it
00:21:25.760
around if we want um a the other way
00:21:29.080
around okay so you can do lots of
00:21:31.400
different things um as long as you can
00:21:33.880
just say if it returns zero don't do
00:21:36.600
anything um more often than not uh I
00:21:39.480
don't ever really return zero you either
00:21:41.720
just return a number that's bigger than
00:21:44.000
zero or less than zero and yeah and you
00:21:46.880
can create your own conditions in terms
00:21:48.640
of how it should sort if you have for
00:21:50.679
example objects uh you can even do the
00:21:54.159
following so let me just open fig Jam so
00:21:56.880
let's say we have our tasks here and we
00:21:58.799
want to sort our tasks then we can go
00:22:01.520
obviously result and tasks do to sorted
00:22:06.200
and we just take A and B so let's
00:22:08.400
actually start with the dates first so
00:22:10.840
what we can say is effectively let's say
00:22:14.159
a date and B date and let's first say a
00:22:18.640
do du and if it doesn't exist just make
00:22:21.720
it zero and we also want to turn it into
00:22:24.240
a number so get time and get time so
00:22:27.039
into a Epoch number so so in other words
00:22:29.360
the amount of milliseconds that has
00:22:30.880
passed in 1970 it is as simple as a date
00:22:35.080
minus B date and that'll arrange it for
00:22:38.200
you in order with all the the ones that
00:22:42.279
don't have dates at the end if you want
00:22:44.520
all the ones that don't have dates to be
00:22:46.120
at the front you can just say if a do
00:22:50.559
and B do not exist then turn one and it
00:22:54.840
should put it at the front otherwise do
00:22:57.279
a comparison and then check and so then
00:23:00.679
lastly the other thing is let's say you
00:23:03.360
want to sort based on urgency so you
00:23:05.640
might want to go a urgency and B urgency
00:23:09.480
but how do you now actually sort this
00:23:12.799
alphabetically because you can't go a
00:23:15.720
minus B urgency because effectively
00:23:18.400
obviously these are um strings and you
00:23:21.279
can't minus strings so what you can do
00:23:24.480
is you can turn the string into its
00:23:27.520
actual unic code value and then it
00:23:30.440
compares the Unicode values as if it's
00:23:32.840
numbers and so you can actually compare
00:23:35.360
the two Unicode uh numbers so you just
00:23:38.240
use something called local compare B and
00:23:42.360
that should just return zero or one so
00:23:45.279
that should be sufficient actually like
00:23:48.480
order it alphabetically based on a
00:23:50.600
nested value oh obviously sorry we need
00:23:52.520
to do a du not do urgency and B urgency
00:23:58.000
and so let's actually check that out so
00:23:59.760
if we put it down here and let's run
00:24:01.840
that in the browser and we actually made
00:24:04.320
a typ of this should be tasks multiple
00:24:07.360
and we obviously need to log result okay
00:24:10.480
so high low low and normal so it
00:24:14.840
obviously arranges it alphabetical so
00:24:17.000
obviously High H is before L and before
00:24:21.159
n but this obviously doesn't make sense
00:24:23.559
in terms of what the things actually
00:24:25.159
mean so one thing that we can do is we
00:24:28.880
can create an array that specifies like
00:24:31.840
the order so we can go you know like
00:24:34.240
let's just say order low normal high
00:24:38.120
normal and low so we don't want it to be
00:24:41.080
alphabetical instead what we wanted to
00:24:43.159
do is base it on the position in here so
00:24:46.399
then what we can do is we can say the
00:24:48.840
order so in order get the index of a
00:24:53.640
urgency and just minus the index of B
00:24:58.000
urgy so we just actually um uses the
00:25:01.919
indexes to determine and so now it just
00:25:04.880
puts all the high ones first then the
00:25:07.320
normal ones then the low ones and so
00:25:10.080
forth so yeah like you can do loads of
00:25:13.120
things here it's up to you to figure out
00:25:15.360
how you want to order it purely just by
00:25:18.320
either it returning 1 0 or minus one or
00:25:22.760
or any value below you know zero or so
00:25:26.000
forth okay so that's basically sorting
00:25:27.880
it's actually really powerful and you
00:25:29.399
can imagine like it allows us to build
00:25:31.679
like a lot of filtering and sorting and
00:25:34.039
things into our apps and for example aut
00:25:36.440
to do app so now I'm going to get to the
00:25:38.440
really scary one which is reduce so
00:25:41.559
let's look at the mdn documentation
00:25:43.480
first so it effectively says reduce
00:25:46.399
executes a user supplied reducer
00:25:49.080
callback function on each element of the
00:25:51.559
array passing in the return value from
00:25:54.159
the calculation on the preceding element
00:25:56.799
okay so I'll show I'll kind of
00:25:59.000
illustrate in a second what this means
00:26:01.120
but effectively a reducer takes an array
00:26:05.240
and it can turn it into anything by
00:26:08.000
mapping over it whereas a map takes a
00:26:10.960
array and turns it into a new array it
00:26:13.600
has so it takes a function and it passes
00:26:16.720
four things to that function so the
00:26:20.039
first one is the accumulator so this is
00:26:22.919
effectively the result of the reduce up
00:26:26.080
until that point on that iteration
00:26:28.880
and so the first time that this gets
00:26:30.679
called you can specify the initial value
00:26:33.520
um otherwise it just starts with the
00:26:35.840
first value in the array then it takes
00:26:38.279
the current value of where it is M
00:26:41.080
looping at the moment then current index
00:26:44.520
and the array itself and you can also
00:26:47.320
specify initial value where it should
00:26:50.279
start from um I encourage you to maybe
00:26:52.840
watch some videos on YouTube on reduce
00:26:55.640
um most of those videos would be able to
00:26:57.960
expl explain it better than I would um
00:27:00.399
but I'm just going to give it a go and
00:27:01.960
also I'm don't necessarily have the time
00:27:04.080
that uh half an hour video or a 20
00:27:06.799
minute video can take to actually just
00:27:09.399
dive into reduce but I'm going to see
00:27:11.399
maybe I can explain it simply enough so
00:27:15.039
effectively let's say we have an array
00:27:17.159
so we have you know 1 2 3 4 5 6 7 let's
00:27:21.799
just write our reduce Handler separately
00:27:24.320
from reduce itself okay and let's just
00:27:26.840
put that in result and let us conso log
00:27:30.279
result conso log result all right so
00:27:34.279
effectively what does our handler do so
00:27:36.760
our Handler takes four things when we
00:27:39.600
put it in reduce four things get passed
00:27:41.840
to it the accumulator the current value
00:27:45.679
the index and the array itself more
00:27:50.039
often than not I just use the first two
00:27:52.519
in some cases I use this never I I
00:27:56.000
actually use the array itself so you
00:27:57.760
don't need to use all of these and
00:27:59.840
another thing is as well you can give it
00:28:02.399
something to start with so let's say we
00:28:04.760
pass it it starts with a 100 actually
00:28:07.279
put it here it's the second thing in
00:28:09.200
reduce so even if that is the case um
00:28:13.399
and I have like an array then I usually
00:28:15.360
just go like array zero or whatever if I
00:28:18.159
actually want that I would rather
00:28:19.840
explicitly give it something to start
00:28:22.000
with okay but let's start with 100 here
00:28:24.200
now so what happens so it goes so let's
00:28:27.399
write our hand let's leave index for now
00:28:30.679
so let's just say the accumulator and
00:28:32.440
current okay so let's keep it super
00:28:34.559
simple so what does it return just the
00:28:36.960
accumulator plus the current that's it
00:28:39.640
okay so we passed that to it so what
00:28:42.279
happens so it starts with 100 it
00:28:44.360
iterates over the first item in our
00:28:46.120
array which is you know one and so it
00:28:49.799
passes it to the Handler so the
00:28:52.120
accumulator and the current what and we
00:28:54.679
specify what it should do and
00:28:56.679
effectively we just add it so it gives
00:28:58.519
us 101 okay then it goes to the next one
00:29:02.200
and so this creates the next accumulator
00:29:05.320
so whatever you return gets passed on to
00:29:07.279
the next one so now we have 101 and then
00:29:10.600
we plus two so that's 103 okay and
00:29:13.840
because this gets returned it actually
00:29:16.360
gets passed on to the next one and so
00:29:18.880
forth and so forth and so forth so what
00:29:21.799
we can do then if this is a zero then
00:29:24.640
what this effectively does is going to
00:29:26.399
calculate the the sum of all of these
00:29:28.799
combined so one sum all of them together
00:29:32.399
and that gives us like an actual value
00:29:34.919
because it Loops over them and it kind
00:29:36.760
of every time adds it to a final value
00:29:40.600
let's look at some examples okay so
00:29:43.600
maybe what we can do is we can say hey
00:29:46.159
we want to know how many times the word
00:29:48.799
c comes up in titles all right so let's
00:29:52.480
do the following so let's just write our
00:29:55.000
reducer right in here and obviously we
00:29:57.519
start with zero we start with there's no
00:30:01.000
C yet in any title and then what we do
00:30:04.519
so we get the accumulator so obviously
00:30:06.480
that starts at zero and then we get the
00:30:08.600
value that's getting looped over we can
00:30:10.840
even destructure straight in here so
00:30:13.440
let's just grab the title from that
00:30:16.720
let's just take the title and let's say
00:30:19.320
title as array so let's turn it into an
00:30:22.279
array of letters so we can do title
00:30:25.120
split let's falter out everything that
00:30:27.559
is in C okay so let's say total C so
00:30:32.039
title as array and filter and let's just
00:30:35.679
say Char for character and we just check
00:30:39.640
is the Char if the Char is equal to C
00:30:44.519
and this can be lowercase or uppercase
00:30:46.760
so let's force it to be lowercase to
00:30:49.200
lowercase I'm not sure I think maybe you
00:30:52.080
write it like that we'll see in a second
00:30:54.200
so we force it to be lowercase and then
00:30:56.399
we check if it's lowercase is it a c
00:30:59.440
then we just check the length so we just
00:31:03.240
return the accumulator plus the total C
00:31:07.760
all the previous counts we add it to all
00:31:10.639
the previous counts so every time we go
00:31:12.399
over each item um and then results
00:31:15.240
should just be the amount of C's in
00:31:17.279
titles and once again I should just make
00:31:19.639
this tasks plural and two lowercase and
00:31:23.320
I think I got it wrong I think it is
00:31:25.919
actually like that total C total C's
00:31:29.880
plural as well yeah I'm really getting
00:31:32.240
tripped up here without my static type
00:31:34.320
checking three okay so there's a total
00:31:37.240
of three C's let's check something else
00:31:39.760
let's say a how many A's are there seven
00:31:42.919
um so you can do really cool stuff like
00:31:44.880
this um you can even have if statements
00:31:47.120
in there so let's say it should only
00:31:50.519
check for C's so only if there is no
00:31:55.159
date so let's also just pull out uh due
00:31:58.960
and so we say only if there is no due
00:32:01.720
date so if there is a due date we just
00:32:05.679
return the accumulator as is without
00:32:08.200
doing anything with it otherwise we
00:32:10.600
calculate a new accumulator right so I
00:32:13.279
think it should be two now well let's
00:32:15.600
see here's a c and there's no date here
00:32:18.840
is a c but there is a due date and there
00:32:22.159
it should actually just be one cuz
00:32:24.039
there's no C here let's see one all
00:32:26.639
right and then obviously other way
00:32:28.320
around it's going to be two all right so
00:32:31.279
this was a very very very brief summary
00:32:34.600
of reduce um there's a lot of really
00:32:37.760
great material out there including the
00:32:39.880
mdn article itself um I don't want to
00:32:43.039
get too deeply into reduce in this
00:32:45.200
lesson um it is already quite long um
00:32:48.519
and then the goal is just to talk about
00:32:50.000
higher order functions of which reduce
00:32:52.200
is one but I encourage you to watch some
00:32:54.519
other videos I encourage you to actually
00:32:56.480
read up on it a bit I use reduce all
00:32:59.799
over the place it it is super powerful
00:33:02.440
it's probably reduce and map are the two
00:33:05.919
map I would say is probably the most
00:33:07.639
powerful reduce probably the second most
00:33:10.240
powerful um so I would definitely
00:33:12.519
encourage you to kind of learn how to
00:33:14.240
use reduce um it's going to feel like a
00:33:16.760
superpower like you would be able to
00:33:18.760
express something like this something as
00:33:21.000
complex as how many tasks that don't
00:33:24.159
have due dates how many times does a
00:33:26.519
letter C come up in them you know like
00:33:28.679
this is such a very specific thing and
00:33:31.200
you can express it in such an elegant
00:33:33.639
like an expressive manner um by using a
00:33:36.159
reduce all right so I will see you guys
00:33:38.639
in the next lesson the final lesson
00:33:40.600
where we're going to touch on state
00:33:42.799
machines and we're also going to finish
00:33:45.600
up our app and then once we have a kind
00:33:48.039
of a final version of our app we're
00:33:49.760
going to go into JavaScript Frameworks
00:33:52.000
cuz then we know all the big Concepts
00:33:55.559
that Frameworks try and solve for us and
00:33:58.080
we can then actually compare Frameworks
00:34:00.000
and discuss Frameworks in the context of
00:34:02.960
talking about encapsulation polymorphism
00:34:06.080
declarative uis higher order functions
00:34:09.119
all these things how these Frameworks
00:34:11.440
actually use these principles to
00:34:14.560
abstract away all the lowlevel stuff and
00:34:16.879
give you a really really nice
00:34:19.440
abstraction that you can actually use to
00:34:21.960
create your app logic I will see you in
00:34:24.399
the next video