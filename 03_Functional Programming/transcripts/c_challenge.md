00:00:00.000
hey everyone skulk here so I thought it
00:00:03.120
might be a good idea to record a very
00:00:05.400
brief introductory video
00:00:07.980
um to set the stage for kind of this
00:00:09.540
upcoming challenge because we are moving
00:00:12.480
a bit deeper into conceptual territory
00:00:14.519
now
00:00:15.719
um our focus is shifting a bit from
00:00:18.240
comprehending ideas to actually applying
00:00:21.300
those ideas so that means the goal is
00:00:24.000
not only to grasp but also to
00:00:26.340
demonstrate your understanding and kind
00:00:28.619
of how you can adapt to applying
00:00:30.779
Concepts to actual real circumstances so
00:00:34.860
specifically for this example obviously
00:00:37.500
it's important that you have actually
00:00:39.780
watched both videos and both of those
00:00:42.600
videos contain all the information you
00:00:44.760
need to actually build out this little
00:00:47.940
very small basic exercise that you need
00:00:50.100
to do so if you're remember correctly
00:00:52.440
the videos were first and foremost about
00:00:55.020
the global store State and then also
00:00:57.660
kind of like how something like Redux
00:00:59.820
takes this idea of a global store and
00:01:02.760
applies a very strong functional
00:01:04.619
programming approach to it so we're
00:01:07.020
going to be drawing inspiration from
00:01:09.119
that and you should then Implement your
00:01:12.119
own kind of version of this create your
00:01:14.520
own Global store
00:01:16.619
um how much of that approaches and
00:01:19.200
Concepts that I showed you add to that
00:01:21.600
and use in that is up to you but the key
00:01:25.200
here being that it's important that
00:01:28.080
first and foremost your store has a way
00:01:30.000
to subscribe so listen for specific
00:01:33.000
actions that happen in that store and a
00:01:35.759
way to dispatch or notify the store of
00:01:38.520
actions and how exactly you do this is
00:01:41.939
you know for you to decide and then this
00:01:44.400
is where we get more into the conceptual
00:01:46.500
space where not only do you need to show
00:01:48.900
that you understand theoretically a
00:01:50.939
concept but also that you understand
00:01:53.220
enough that you can actually apply to
00:01:55.500
practical instances and practical
00:01:57.840
examples so obviously this module is
00:02:01.680
about functional programming so I would
00:02:04.259
advise you to kind of draw some of that
00:02:06.960
functional programming
00:02:08.639
um aspects that you find in something
00:02:10.440
like Redux in here as well to kind of
00:02:13.920
build out your example to show kind of
00:02:15.959
some competency and not only
00:02:18.060
understanding functional programming but
00:02:19.739
actually applying it and applying it in
00:02:22.200
such a way that it adds value but to
00:02:25.500
keep things straightforward we'll just
00:02:27.420
focus on two things so first and
00:02:29.459
foremost we're going to be reverting to
00:02:31.260
a very very basic example and that is
00:02:34.319
the very very first tally app that you
00:02:36.900
built where you could only add a number
00:02:38.580
you could subtract a number or you could
00:02:41.099
reset the number so it's very basic in
00:02:43.560
terms of functionality and then secondly
00:02:46.440
we're not going to be outputting any
00:02:47.940
HTML or rendering anything on the screen
00:02:50.280
so no CSS no real HTML we're just going
00:02:54.360
to want to console log things to the dev
00:02:56.700
tools just to confirm that your store is
00:02:59.340
working as it should so you don't need
00:03:01.379
to actually build out an actual app
00:03:04.440
um I just want to see that you're able
00:03:06.180
to kind of apply these principles to a
00:03:09.000
very small scale example and in a
00:03:11.700
different context as opposed to just
00:03:13.739
copy and pasting what I did with the
00:03:16.200
to-do app so asset means to express what
00:03:18.900
exactly you have to do for this exercise
00:03:20.780
we are going to be using a syntax called
00:03:24.120
gherkin and it comes from the world of
00:03:26.400
behavior driven development and test
00:03:28.319
driven development and so forth and it
00:03:30.239
is a very nice way to express specific
00:03:32.640
behavior and functionality associated
00:03:34.860
with software either through means of
00:03:37.500
specification in terms of hey you need
00:03:39.720
to build this thing this is what it
00:03:41.159
needs to do or by means of writing tests
00:03:43.860
in order to actually confirm that hey
00:03:46.260
this piece of software actually does
00:03:47.940
what it needs to do
00:03:49.560
um in this case we are going to be using
00:03:51.239
these as tests and definitions of done
00:03:53.760
so effectively if all four of these
00:03:57.000
statements are true then you have
00:03:59.580
actually passed the challenge and these
00:04:02.159
instructions are deceptively simple and
00:04:04.440
so far that you might even wonder
00:04:05.940
whether you understood them correctly so
00:04:08.580
you don't need to Output any HTML no CSS
00:04:11.480
effectively you just need to log to the
00:04:14.340
devtools console and the reason for this
00:04:16.680
is because you just want to indicate
00:04:18.899
your conceptual understanding of the
00:04:21.298
things that were covered in the videos
00:04:22.800
you don't want to get bogged down in
00:04:25.080
lots of other things around styling and
00:04:26.880
so forth so now that we've established
00:04:29.280
kind of what you should aim for let's
00:04:30.840
kind of look at what the expectations
00:04:33.120
are in terms of the structure so broadly
00:04:36.900
speaking you're going to have some type
00:04:38.400
of store
00:04:39.840
and this store is going to need a way
00:04:42.120
for the app to send messages to it and a
00:04:45.120
way to listen for messages and the key
00:04:47.639
here is the store is global so you
00:04:49.860
should be able to pull the store in at
00:04:52.440
any place and send a message to it
00:04:54.240
likewise you need to be able to pull in
00:04:56.699
the store anywhere and listen for
00:04:58.860
specific messages on it so effectively
00:05:01.979
you should be able to take the store
00:05:04.199
that you created as part of the
00:05:06.240
challenge and Pull It in some way and
00:05:09.300
then run an update or a dispatch
00:05:11.460
function on it and you send instructions
00:05:14.100
to this update or dispatch and then you
00:05:16.680
should also be able to add a subscribe
00:05:19.199
method to it and the Subscribe method
00:05:21.240
generally takes like a Handler or
00:05:23.160
something and does something when the
00:05:25.560
store updates generally it is a good
00:05:27.720
idea to return both the previous state
00:05:30.479
of the store so the way it was before
00:05:33.060
the change happened and the state after
00:05:35.699
the change happened and this allows us
00:05:37.740
to compare specific values and only list
00:05:40.500
reason for changes in specific values
00:05:43.259
otherwise you don't do anything and the
00:05:45.960
reason being that you don't necessarily
00:05:47.940
want your store to trigger updates all
00:05:51.240
across your app regardless of what was
00:05:53.280
updated but you can also build a simpler
00:05:56.520
implementation that purely just passes
00:05:58.560
the new state to the Handler in the case
00:06:01.620
of this specific scenario that you need
00:06:04.259
to complete there's about two that
00:06:07.139
generally would relate to sending
00:06:08.880
updates and then there is a couple that
00:06:11.699
actually relate to the subscription and
00:06:14.220
passing that subscription to the
00:06:16.080
devtools console log don't get too hung
00:06:18.720
up on what exactly should be shown in
00:06:21.300
the console the the key just is that you
00:06:23.880
should be able to see this new state in
00:06:27.060
some manner after the updates have been
00:06:29.639
passed and it should also automatically
00:06:31.979
show this when that specific thing
00:06:34.620
updates if you want additional resources
00:06:38.100
on this a good place might be to have a
00:06:40.680
look at the refactor guru example that I
00:06:45.000
looked at it it does cover the
00:06:47.819
underlying pattern that is used here
00:06:50.460
which is the Observer pattern so it has
00:06:52.740
a couple of examples where it kind of
00:06:54.419
shows shows this pattern and how it gets
00:06:56.880
implemented and the ways to use it and
00:06:59.039
just be mindful that most of these are
00:07:01.500
in other languages but I do think
00:07:03.840
there's value in just broadly
00:07:06.060
understanding the pattern and then
00:07:07.740
lastly what I would also encourage is
00:07:09.720
that you may be head chat gbt ask it to
00:07:12.539
explain the Observer pattern to you and
00:07:15.180
so when I did it it showed it to me
00:07:17.100
using a class syntax so if you want to
00:07:19.380
do it with Factory functions instead ask
00:07:21.360
it hey explain this principle to me only
00:07:24.060
using Factory functions and that should
00:07:26.280
also give it to you in a factory
00:07:27.720
function way that is about it I hope
00:07:30.960
this was helpful to you guys
00:07:33.479
um and I just want to make a point to
00:07:35.699
prioritize once again what we are
00:07:37.860
testing for here is understanding don't
00:07:41.400
get too hung up on the actual
00:07:43.560
expectations and whether you're doing it
00:07:46.500
quote unquote great ensure that whatever
00:07:50.099
you're doing or sure that you're
00:07:52.199
indicating that you're understanding and
00:07:54.180
your show during that understanding of
00:07:56.460
the material that was covered in the
00:07:58.199
videos everything else is secondary the
00:08:00.900
exercise itself is just a way to confirm
00:08:03.900
whether you understood it correctly so
00:08:06.240
don't get too hung up on the
00:08:07.740
technicalities of the exercises
00:08:09.360
themselves if you have any other
00:08:11.039
questions please hit up your coach they
00:08:13.199
should be able to give you more context
00:08:15.180
if you get stuck on any of these
00:08:17.460
exercises going forward or this specific
00:08:19.680
one