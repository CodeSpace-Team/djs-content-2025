These concepts collectively contribute to a comprehensive understanding of building and managing applications with React and similar frameworks, highlighting the importance of state management, component-based architecture, and the declarative approach to UI development.


### Major Concepts

- **React and Frameworks**: Understanding React's approach to UI development, including its functional programming underpinnings and the declarative nature of creating user interfaces.
- **State Management**: Exploring how state is managed within React components, emphasizing the distinction between state and props, and the concept of lifting state for shared state management across components.
- **Components**: The fundamental building blocks of React applications, including the differentiation between functional and class components.
- **Hooks**: Focusing on the useState hook for state management within functional components and its role in React's functional approach.
- **Props**: Passing data to components, allowing for customizable and reusable components.
- **Declarative UI**: The approach of defining UIs in a declarative manner with React, as opposed to imperatively manipulating the DOM.
- **Event Handling**: Managing user interactions and events in React, including custom event handling.
- **Controlled vs. Uncontrolled Components**: The difference between controlled components, where React manages the state, and uncontrolled components, which manage their own state.

### Minor Concepts

- **Rendering and Re-rendering**: The process of displaying the UI based on the current state and updating it in response to state changes.
- **Component Nesting and Composition**: Building complex UIs through the composition of smaller components, including nested routing and nested components.
- **State Lifting**: Sharing state across multiple components by moving the state to their common ancestor.
- **Custom Events**: Creating and handling custom events for component communication.
- **Accessibility**: Ensuring components are accessible, including using appropriate attributes and roles.
- **Styling**: Applying styles to components, including the use of CSS-in-JS approaches and external styling libraries.
- **Utility Functions**: Using utility functions for common tasks, such as date formatting and string manipulation.







00:00:00.000
so one thing that you can do is you can
00:00:02.220
lift the state so if I go back to that
00:00:04.860
react visualized and once again this is
00:00:08.039
looking through it through the lens of
00:00:10.320
react but you can probably already see a
00:00:12.780
couple of things here that we have
00:00:14.639
spoken about because you find these
00:00:17.160
exact same Concepts in react the way it
00:00:19.859
maybe just does it the way I add
00:00:21.660
abstracts it is maybe a bit different so
00:00:23.820
we spoke about rendering we spoke about
00:00:25.640
re-rendering and then I also kind of
00:00:27.900
spoke about this idea of you know react
00:00:31.260
is effectively just composed functions
00:00:35.219
all the way down so you have your state
00:00:36.660
and then you have all these composed
00:00:38.340
functions that run that turn that state
00:00:40.860
into a UI so in react you wouldn't
00:00:43.680
necessarily do this type of thing where
00:00:45.780
we have a method and then you know like
00:00:48.780
we call that method and we directly you
00:00:50.640
can't for example do this in react you
00:00:52.379
can't just manually go and change the
00:00:55.739
state update the state manually Target
00:00:58.020
Something and update it but and
00:01:00.000
sometimes gives react a bit of a higher
00:01:02.280
learning curve but we will get to that
00:01:04.860
when we touch on Frameworks and then
00:01:06.960
also just this idea of components and so
00:01:09.720
State and so the way reactors that so
00:01:12.900
the way react does this thing you know
00:01:15.119
like keeping state in components is
00:01:17.939
through hooks so one of them being used
00:01:20.280
State and we'll talk about that and
00:01:22.680
props so you should know what props are
00:01:25.020
by now
00:01:26.220
um and it's effectively these things so
00:01:29.280
those are things that can be passed down
00:01:31.500
to components from outside
00:01:34.140
um although in lit every all of these
00:01:37.320
things are properties and some of them
00:01:39.240
are just state or just properties that
00:01:42.420
are State
00:01:43.560
um in react it usually makes a
00:01:45.060
difference between things that are State
00:01:47.040
and things that are property it treats
00:01:48.780
these as differently instead of just
00:01:51.659
bundling all of them together in one
00:01:53.700
thing so you would specify your state
00:01:56.040
things differently than properties let's
00:01:58.259
say instead of tracking that state into
00:01:59.939
internally and we rather want to have it
00:02:01.860
passed through then we just do that that
00:02:04.259
means like whether it's open or not
00:02:06.119
comes from its parent we scroll down so
00:02:09.060
once again just to recap uh you very
00:02:12.120
clearly saw the pain of doing it in this
00:02:14.400
way you very clearly saw what is the
00:02:16.860
benefit of writing your HTML
00:02:18.720
declaratively and then you know one of
00:02:20.819
the first tabs added MVC resulted in a
00:02:24.300
lot of boilerplate code AS mentioned you
00:02:26.220
know if they thought Redux was a lot of
00:02:28.080
like code just to get it to work uh MVC
00:02:31.739
generally results in a lot of code and
00:02:34.200
then there's this idea that was
00:02:35.700
pioneered by angularjs so the very first
00:02:38.160
version of angular also keep in mind I
00:02:41.160
mentioned that angular 234 onwards is a
00:02:45.420
completely different framework from
00:02:47.239
angularjs the first one those just have
00:02:50.400
the same name but for all intents and
00:02:52.019
purposes they are not the same thing in
00:02:54.060
classic Google fashion so this is
00:02:56.040
two-way data binding you can still do it
00:02:59.400
in the new angulars you can do it in
00:03:02.220
view as well so what two-day data biting
00:03:05.400
just means like if it updates here it
00:03:07.379
keeps the view in sync but if it updates
00:03:09.360
in the view it keeps the model in sync
00:03:11.459
as well and then we just spoke about
00:03:13.200
this idea of view as a function of your
00:03:16.680
state which to a certain degree all the
00:03:19.620
Frameworks do when it comes to
00:03:21.780
declarative UI so in this case you know
00:03:24.900
this is this is just a function although
00:03:27.540
what react does
00:03:29.400
um is react everything this like even
00:03:32.159
this is a function not just the actual
00:03:35.040
HTML that you express all your event
00:03:36.780
listeners everything is part of a
00:03:38.340
function you would literally create your
00:03:40.379
components by going like adding as a
00:03:42.659
function and there you go you know and
00:03:44.640
you pass like and the props is actually
00:03:46.620
just like like a regular function all
00:03:48.900
Frameworks do you a certain degree do
00:03:51.120
this a react just does it all the way
00:03:53.159
from the top to the bottom and so you
00:03:55.200
know effectively when the state changes
00:03:57.299
the functions run and it calculates the
00:03:59.099
new state so scroll down a bit once
00:04:01.980
again like most Frameworks share a lot
00:04:04.799
of these things because reactors are so
00:04:08.159
popular at the moment a lot of the
00:04:10.379
material is react specific but these are
00:04:13.260
generally applicable to most Frameworks
00:04:15.180
so we in depth looked at you know this
00:04:18.000
idea of components of you know not
00:04:20.279
splitting out your HTML CSS and
00:04:22.199
JavaScript and instead breaking it up in
00:04:25.800
terms of responsibilities instead of
00:04:27.780
just Technologies and so effectively
00:04:30.000
here is how you would write this with
00:04:33.600
jsx which is very similar to what we're
00:04:36.419
now doing with HTML with that HTML
00:04:39.479
function in lit although this isn't a
00:04:42.660
string okay but that's just react so you
00:04:45.660
should understand so effectively you can
00:04:47.759
think about props as attributes with web
00:04:50.160
components so we can pause attributes
00:04:52.560
all the way down into nested components
00:04:54.960
so through components down to their
00:04:57.360
children so for example here's an
00:04:58.919
example and so what we sometimes want to
00:05:01.620
do is we need to figure out where the
00:05:04.500
state of something specific lives in our
00:05:06.419
app so in this case whether the model is
00:05:08.580
open or closed that can be in several
00:05:10.620
places it can be all the way in the top
00:05:12.800
at in the store itself which is maybe
00:05:15.720
not a bad idea
00:05:17.300
or it can be in the modal itself or it
00:05:21.180
can be one level above the modal which
00:05:23.759
is the actual TV adding component that
00:05:26.820
wraps all that functionality so we need
00:05:28.860
to figure out where that state is going
00:05:30.479
to live and so the problem is now is we
00:05:33.300
have exactly this problem so there's two
00:05:35.880
components that need to know a single
00:05:39.419
piece of state so we have a button so
00:05:42.479
button needs to know if it's open or
00:05:44.400
closed and the modal itself but the
00:05:47.880
problem is both of them keep their own
00:05:50.520
version of the state so what we need to
00:05:52.380
do is we need to lift the state so it
00:05:54.479
can be shared by both of them so
00:05:56.220
effectively if you have a look here you
00:05:58.259
lift it up and then you pass it through
00:06:00.000
as props so it's only in one place okay
00:06:02.699
and that is what we're going to do now
00:06:04.500
so effectively the the SL dialog itself
00:06:08.160
keeps track of if it's open or not and
00:06:11.460
then we have this open here in the
00:06:14.160
parents so inside SL dialog itself as
00:06:16.860
well and in the parent itself so the
00:06:19.979
first thing we need to do is we need to
00:06:22.199
stop this from controlling its own state
00:06:24.960
so it does accept this at the moment but
00:06:27.900
it's both internally controlling its own
00:06:30.060
State and getting state from outside so
00:06:33.600
in other words if we go add task and we
00:06:35.819
close it internally it resets its own
00:06:38.880
state to closed but it never tells the
00:06:41.699
stuff above it it never tells its parent
00:06:43.919
that it's closed so according to the
00:06:46.199
parent so according to the adding
00:06:48.360
component it still thinks it's it's open
00:06:51.539
which is why if we click it again then
00:06:53.460
it sets it to closed and then we have to
00:06:55.740
click again to set it back to open so
00:06:57.780
let's look at the shoelace documentation
00:06:59.520
and how we would actually prevent it
00:07:01.919
from actually closing itself and have
00:07:04.680
the closing and have the parent actually
00:07:07.259
take control of it in react there's also
00:07:09.419
this idea of control of controlled and
00:07:11.819
uncontrolled components and you can read
00:07:14.400
up a bit more about this generally find
00:07:16.560
this type of thing in most Frameworks as
00:07:19.500
well but yeah most of the writing about
00:07:22.319
it is on react for obvious reasons so
00:07:25.979
let's go dialogue and let's see I
00:07:29.340
actually don't know how to do this maybe
00:07:30.599
there's a property that we thought I
00:07:32.639
actually don't know how to do this maybe
00:07:34.560
there is a property that we passed where
00:07:36.900
we tell it like listen don't control it
00:07:39.000
own state or we intercept the event
00:07:41.280
listener or something let's see and you
00:07:43.620
can think almost about this in the same
00:07:45.780
way that you know we need to stop a form
00:07:49.080
in HML from following its own internal
00:07:52.259
logic where it refreshes the page
00:07:54.539
because we're actually doing something
00:07:56.639
outside of it that it doesn't know about
00:07:59.280
so you need to tell it like don't do the
00:08:01.380
thing you usually do don't control your
00:08:03.000
own State and we are going to actually
00:08:04.860
tell you what to do so we are going to
00:08:06.780
tell you when you need to be open we are
00:08:08.280
going to tell you when you need to be
00:08:09.360
closed okay so this emits when it opens
00:08:11.759
this emits when it closes a SL request
00:08:15.900
closed Okay so there's two ways to
00:08:18.539
approach this the one would be to just
00:08:21.300
let the parent know that it closed and
00:08:24.900
the other one might be to intercept it
00:08:27.120
and prevent it from closing and only
00:08:28.979
give the parent permission to close it
00:08:31.379
and open it and then like like stop it
00:08:33.958
from closing itself and tell the parent
00:08:35.640
to close it I would have actually gone
00:08:38.039
for this one but because the
00:08:40.020
documentation says avoid use this let's
00:08:43.620
actually just go with the other option
00:08:45.180
where it tells the parent that it closed
00:08:47.399
so emitted when the dialogue closes so
00:08:50.820
we need to listen for SL hide and we can
00:08:53.940
actually listen for custom events Inlet
00:08:56.580
itself so we can go at SL hide like that
00:09:01.560
and then tell it to toggle open so this
00:09:04.800
should fix the issue so it should say
00:09:06.660
when this component internally the state
00:09:09.120
changes to hiding also let the parent
00:09:11.459
know so the parent state is also in sync
00:09:14.220
okay this should solve the problem let's
00:09:16.200
try again to add ask close add task cool
00:09:19.860
so it works now so it actually just
00:09:22.080
changes this and once again like this
00:09:24.300
type of thing is a bit easier in some
00:09:27.540
Frameworks in react this is very hard
00:09:30.300
react usually isn't a big fan if you try
00:09:33.000
and keep the state of two components in
00:09:35.100
sync uh purely just because of kind of
00:09:38.700
its functional programming underpinnings
00:09:40.500
within react we'll need to figure out
00:09:42.660
another way to do this but in lit you
00:09:45.240
can actually just ensure that they are
00:09:46.800
kept in sync so now we want to handle
00:09:49.320
the submit as well so this is pretty
00:09:51.540
easy we can just go here at subnet and
00:09:54.899
let's just create a function that is
00:09:56.640
this handle subnet and so let's do
00:09:59.399
handle submit okay and we take the event
00:10:02.120
and so we do const so we can grab all
00:10:06.240
that logic we previously did here and I
00:10:08.760
think it's in our script still commented
00:10:10.500
out yes let's just grab that sure
00:10:13.160
dispatch we don't necessarily maybe so
00:10:16.080
here here we decide whether we were on a
00:10:18.779
talk directly to the store or maybe just
00:10:21.600
let the parent know and I think maybe we
00:10:23.880
just bubble this up to the parent and
00:10:25.740
the parent can decide whether it wants
00:10:27.300
to send it to the store or not let's
00:10:29.459
actually this batch a custom event from
00:10:32.100
this component and let's actually start
00:10:33.660
marking this component up so because
00:10:35.940
this is true State like you actually
00:10:38.519
won't know if it is open or closed so
00:10:41.820
let's just write a bit of documentation
00:10:43.800
let's say no so the element is PD adding
00:10:47.700
and what is this element what does this
00:10:49.560
component do so effectively managers
00:10:52.760
provides users with the means to add new
00:10:58.200
tasks we'll only show an add task button
00:11:03.360
however once button is clicked will open
00:11:08.360
an overlay with a form inside that
00:11:13.860
provides the means to add a task so the
00:11:18.600
only thing that we're going to have in
00:11:20.760
here is actual event that fires so what
00:11:24.540
you didn't do is you say fires and you
00:11:27.600
actually say the the name of it so let's
00:11:29.940
say a save and then you specify what
00:11:33.180
goes in details and so if you remember
00:11:35.579
correctly when we spoke about custom
00:11:37.320
events in custom events you can actually
00:11:39.180
pass details so let's just create this
00:11:41.579
up here so add type Def and let's just
00:11:44.579
call it response okay and it's an object
00:11:47.220
and it has the following props on it
00:11:49.320
let's have a look and see so title view
00:11:52.040
du and and
00:11:54.779
urgency and I think urgency was low
00:11:57.660
normal and high and this is null or a
00:12:01.680
date and title is just a string and it's
00:12:04.140
obviously required this isn't standard J
00:12:06.480
stock I actually don't know if we're
00:12:08.100
going to get Auto completion on this but
00:12:10.320
this is still pretty great just in terms
00:12:12.660
of documentation if someone looks at
00:12:14.279
this component then they can at the
00:12:15.899
really see and let's also just put a
00:12:17.880
note here that is weather open or closed
00:12:21.480
internally with own State all right so
00:12:24.660
what's also cool here is because we now
00:12:27.660
have that type definition we can go
00:12:30.120
response and we can set it here to say
00:12:32.820
this needs to be type response and then
00:12:35.160
it's actually going to ensure that it
00:12:37.320
you know this contract that we set that
00:12:39.720
it actually matches this probably need
00:12:41.519
to just convert that to a string like we
00:12:43.380
did last time so do and we need we can
00:12:46.560
pull that from these let me just check
00:12:49.260
what the names of the inputs are so we
00:12:51.899
have do you we don't have something on
00:12:54.660
here so let's just say the name is
00:12:57.000
urgency and so do we could say if D if
00:13:01.019
there's not du then null otherwise new
00:13:04.620
date just passed due because I think
00:13:07.560
this is a string yeah everything we get
00:13:10.440
back from the submission is an actual
00:13:13.680
string which is why we need to actually
00:13:15.839
use a ternary to say if there's no du
00:13:18.540
make it null otherwise coerce it into a
00:13:21.300
date and the only thing it's unhappy
00:13:23.100
about is urgency and it's probably going
00:13:25.260
to complain because it's going to say
00:13:26.700
urgency conscious via string we need to
00:13:28.980
know whether it is low and high and and
00:13:31.980
so forth so let's just put a condition
00:13:34.079
in here let's say if
00:13:36.000
urgency is not low or it is not normal
00:13:40.380
or it is not high then Pro new error
00:13:44.880
invalid
00:13:46.860
urgency value and so what is and not or
00:13:49.740
so if all three of these conditions are
00:13:52.079
made then is not valid so is it smart
00:13:54.420
enough to know then what urgency is yes
00:13:57.420
and it no longer gives us a error so
00:14:00.360
then we know for a fact that response
00:14:02.519
corresponds with that shape and let's
00:14:04.920
look how we dispatch custom events in
00:14:07.320
lit dispatch events so dispatching
00:14:10.740
events so all the stuff up here is about
00:14:12.540
listening for events so we want to look
00:14:14.579
at dispatching events we can just go new
00:14:17.279
event bubbles true compose but we need
00:14:20.100
to use a custom event if we want to add
00:14:22.680
details let's see how the dispatch oh so
00:14:25.320
let's go this new custom event all right
00:14:27.899
that seems reasonable so then what we do
00:14:30.839
is we just reset the form so what we
00:14:33.600
then do is we close the form we can just
00:14:35.399
go this toggle open on this function
00:14:38.399
itself that should just update the state
00:14:40.800
reset the form dispatch event new custom
00:14:45.480
event let's just call it save I think is
00:14:49.500
what we said settings so bubbles yes it
00:14:53.160
does bubble composed yes and the detail
00:14:58.019
is just response so let's now try and
00:15:01.920
capture it in the parent component so in
00:15:05.100
here let's do at save let's just cancel
00:15:08.880
log it for now cool so it actually
00:15:10.860
caught it and we can have a look at
00:15:12.660
detail and here is all the stuff so
00:15:15.180
what's really cool is now we've created
00:15:17.399
this little piece of encapsulated
00:15:19.199
behavior which is just behind this
00:15:21.720
component and that component just does
00:15:23.639
one thing and I just like we can just
00:15:26.100
say add a listener to actually check if
00:15:29.639
something if it's if it's saved and
00:15:32.100
it'll let us know when save happens but
00:15:34.260
otherwise it's just going to handle its
00:15:36.180
own thing it's just going to do its own
00:15:37.500
thing we don't need to know about like
00:15:39.000
yeah what it does so it's handling all
00:15:40.860
of this for us and so forth closing
00:15:43.320
adding tasks and so forth until we save
00:15:46.680
and only then does it actually do
00:15:49.079
something and you'll see there's a
00:15:51.120
moment where it kind of
00:15:53.699
um jumps a bit and and the reason is
00:15:55.680
because we need to actually be able to
00:15:58.680
not only toggle from the current but
00:16:01.680
let's also say that you can actually set
00:16:05.279
the value so we can just say this open
00:16:08.519
is value if value is undefined then just
00:16:12.660
do the opposite of what it currently is
00:16:14.339
otherwise set it to value and then we
00:16:16.860
can also just mark this up and go
00:16:19.019
Boolean and that's optional and so what
00:16:22.560
that allows us to tell it allows us to
00:16:24.540
just toggle from what it currently is
00:16:26.040
set it to something specific so this is
00:16:28.380
going to be a bit more helpful because
00:16:30.000
it's kind of like a bit of a janky
00:16:32.660
animation because it's trying to figure
00:16:35.399
out what it should be but we know that
00:16:38.519
it should be closed so let's just say
00:16:41.399
false and likewise over here and if we
00:16:44.699
want to force it we can actually wrap it
00:16:46.980
in another function in here so we can go
00:16:49.380
like that and say we can't do this
00:16:52.920
because remember now this is actually
00:16:54.720
going to evaluate so let's actually
00:16:57.240
write it as a function that we pass into
00:16:59.579
click we can do the same for our cancel
00:17:03.000
over here and just say false and let's
00:17:06.599
do the same in here to check that out
00:17:09.179
that's working nicely now but what's
00:17:11.699
going on with save and I think it's we
00:17:15.359
are trying to submit it yes so we're
00:17:17.699
trying to submit it even if it's not so
00:17:20.699
we obviously want to tell it like okay
00:17:22.140
only do this if these things are correct
00:17:24.959
although I stop don't continue the
00:17:27.059
submission process so it is actually
00:17:28.740
gonna submit it so let's go to adding
00:17:31.679
and in this logic over here let us
00:17:34.860
actually check whether we should
00:17:37.080
continue so we can just say there's only
00:17:39.240
one condition that's going to stop it
00:17:41.580
and that is
00:17:44.039
um if there's no title or if response
00:17:47.700
title trim equals an empty string it's
00:17:51.120
just empty spaces then just return like
00:17:53.820
don't continue with this stuff don't do
00:17:55.740
this stuff so let's see so only if that
00:17:58.080
passes does it continue and dispatches
00:18:00.600
it and all of that all right so now
00:18:03.179
let's actually do the tasks and so let's
00:18:05.460
just create a single TD task JS and
00:18:09.360
let's just super quickly go class task
00:18:13.160
extends let's pull in that Lit HTML lit
00:18:18.299
element and let's just do a Constructor
00:18:20.700
up here so super okay and let's do our
00:18:24.480
static property so this one is going to
00:18:27.179
be a bit more reliant on properties I
00:18:29.460
don't actually think it's going to have
00:18:30.539
any state of its own so title is type
00:18:33.980
string completed which is type Boolean
00:18:37.980
let's just have urgency in here and that
00:18:40.620
is this right so this should
00:18:42.900
automatically populate it for us based
00:18:45.240
on the attributes of the same names so
00:18:47.820
let's just quickly do a render okay and
00:18:50.340
remember so I'm not going to type this
00:18:52.500
up exactly right now let's just set the
00:18:54.900
returns to any for now okay and we need
00:18:57.120
to remember to Define it and this is
00:19:00.900
just TD task and we just do task and we
00:19:04.559
obviously need to import it so in our
00:19:06.780
scripts let's pull it in here it
00:19:08.760
actually doesn't matter what order you
00:19:10.980
actually import them in then in our app
00:19:13.260
let's uh you know Li and TD task let's
00:19:18.299
see okay so one two three
00:19:20.700
um and I'm also now going to show you
00:19:22.140
how would you actually do custom styling
00:19:24.120
in here so in the class itself you would
00:19:26.880
go static dial so I think we need to
00:19:30.059
pull CSS from there and then Styles and
00:19:34.020
CSS and let's just do Li all Li elements
00:19:39.720
have list style none margin of zero and
00:19:43.200
padding of zero and so remember this is
00:19:45.720
the shadow root so it's only going to
00:19:48.179
apply to that if we put a unordered list
00:19:51.419
in here it's obviously not gonna see
00:19:54.179
there it actually works so it only
00:19:56.280
applies to the shadow Dom of the actual
00:19:59.100
element that you are working with them
00:20:01.500
and let's also just add a ul and I think
00:20:05.340
we also need to do margin zero to
00:20:07.380
override that or I think it's padding
00:20:09.240
let's just do both all right there we go
00:20:11.400
so let's quickly just build out a basic
00:20:14.400
task here let's go to shoelace and let's
00:20:16.740
just check the check box and we also
00:20:18.660
just check elevation while we're at it
00:20:20.640
so uh yeah let's say we actually want
00:20:22.679
the SL Shadow large so let's quickly
00:20:24.539
just do that while we're here we need to
00:20:26.820
import CSS as well here and we go a
00:20:30.720
static Styles equals CSS so this
00:20:33.660
actually does some clever stuff with
00:20:35.280
constructable style sheets and so forth
00:20:37.400
behind the scenes so which is why you
00:20:40.740
actually want to do it this way and not
00:20:42.000
put it in your render itself so this is
00:20:44.160
closer to what you would do with a
00:20:46.020
template whereas this is dynamically
00:20:47.580
generated each time shadow of War oh we
00:20:49.980
need to obviously assign it to something
00:20:51.360
so let's do hey okay there we go okay so
00:20:54.840
let's actually put our spacing element
00:20:56.280
inside it as well so TD spacing and
00:21:00.120
let's do top medium bottom medium lift
00:21:04.200
medium and right medium it also just
00:21:07.260
creates a bit of spacing for us around
00:21:08.880
that uh let's also just in here give
00:21:11.400
this a slight white background a gray
00:21:14.039
background background and let's just do
00:21:16.440
RGB I think what was it let's have a
00:21:19.860
look at the variables for colors and
00:21:22.740
neutral SL color 50 let's go with that
00:21:26.880
SL color neutral 200 yeah let's go to
00:21:31.919
100 that's maybe subtle enough and then
00:21:34.919
obviously in the comp in the task itself
00:21:37.559
so let's go TD task uh title hello and
00:21:43.380
let's say completed remember we can only
00:21:45.720
pass strings down so it probably need to
00:21:48.179
do is so we have two options here so
00:21:50.640
either we passed U as an actual string
00:21:54.059
so you know we go for example like the
00:21:57.000
date and then we and we convert it to a
00:21:59.340
string before we pass it down and then
00:22:01.020
we convert it back to a date in the
00:22:03.240
component itself
00:22:04.740
um or we can just pass it as an actual
00:22:06.780
prop uh because so we start the dot so
00:22:10.020
because of properties you can pass
00:22:11.520
anything so dot and then we can go you
00:22:14.820
know do or whatever but let's just leave
00:22:17.700
do you for now in other words it's null
00:22:19.559
so let's see if we have access to this
00:22:22.440
so so in here let's see if we can do
00:22:25.460
this Dot title cool and there we go so
00:22:29.700
let's uh bring in a checkbox element
00:22:31.740
from shoelace so let's first bring in
00:22:34.679
the check box okay and we want a large
00:22:37.799
one and we don't want a label with it so
00:22:41.100
just like okay let's put it on the side
00:22:43.200
and close it and we want the title to so
00:22:47.760
you should be able to click the title to
00:22:49.679
open more info about the task so for now
00:22:53.880
let's actually just put it in a button
00:22:55.679
and we can look at The Styling in a
00:22:58.140
second so text only button so variant
00:23:01.679
text so that would be SL button and the
00:23:05.280
variant would be text okay so we can
00:23:08.580
click on that as well we can toggle this
00:23:10.580
and then if it has been clicked we can
00:23:14.400
delete it we want an icon button at the
00:23:17.220
end so we can put SL icon in it let's
00:23:20.159
just get the medium one all right so
00:23:22.320
that looks good and but we don't want
00:23:24.419
gear we want let's see what are all the
00:23:27.539
icons at our disposal uh let's trash or
00:23:31.679
delete here let's go this one and let's
00:23:34.200
just make the label the lead so this is
00:23:36.000
what it'll show if we hover over it and
00:23:38.159
so this will just be what gets shown
00:23:41.280
um for accessibility and so forth so
00:23:43.380
let's also say delete task so here we
00:23:45.600
might need to do a bit of classes so
00:23:47.640
let's say class outside and class inside
00:23:50.940
and so outside the Shadow and whatever
00:23:54.559
inside is just where we actually do
00:23:58.380
display flicks and justify content space
00:24:02.640
between and align items we can also put
00:24:05.880
some padding let's put some padding in
00:24:07.919
our app itself as well or we can just do
00:24:10.500
TD spacing once again let's just do lift
00:24:14.460
medium right medium let's just do a top
00:24:18.480
large and bottom extra large okay and
00:24:22.080
let's close that down here and let's
00:24:24.419
also do a bit of Border radius on the
00:24:26.940
outside of that border radius and if I'm
00:24:30.299
not mistaken SL I think there's radius
00:24:34.200
let's go with medium so let's just fill
00:24:36.780
this up with some more tasks and once
00:24:38.700
again what's really cool is now this is
00:24:40.320
completely encapsulated away and even
00:24:43.380
better let's actually create some mock
00:24:46.260
tasks up here so let's just say tasks
00:24:49.080
add all in the shape of the tasks from
00:24:52.080
our store so model uh store and I think
00:24:57.240
it's just task let's just create testing
00:25:00.960
which is just a let's say an array of
00:25:03.480
tasks type array task and we added ID
00:25:08.159
title let's grab those ones we created
00:25:10.440
in fig Jam actually there are some stuff
00:25:12.960
missing here yes so we need to also add
00:25:17.700
urgency which can be low normal or high
00:25:22.500
and then also so we have created we want
00:25:25.559
due as well which is date or null and
00:25:29.039
complete it as well
00:25:31.080
um in any other circumstance I would
00:25:32.700
actually write some documentation here
00:25:34.380
but yeah we want to get this working and
00:25:36.480
I think we should now get an error on
00:25:38.460
our action as well because it doesn't
00:25:40.679
Supply us with everything we need from
00:25:44.039
here we also know so there's needs
00:25:46.620
completed so completed always starts as
00:25:48.600
false du is dependent on what gets
00:25:52.679
passed and urgency as well just pick
00:25:55.380
what we need so we can go pick task so
00:25:58.020
we need the title we need you and we
00:26:01.020
need completed oops urgency not
00:26:03.299
completed there we go the task all right
00:26:05.940
what what does urgency yeah it's times
00:26:09.539
like this where like it kind of feels to
00:26:11.700
me like sure I really like that we have
00:26:14.220
went through the effort of getting the
00:26:15.960
static type checking going and so let's
00:26:18.000
uh just grab our tasks example that we
00:26:21.480
created in fig Jam it's actually just
00:26:23.820
put it in here and it actually complains
00:26:26.700
because uh there's some stuff here so
00:26:29.220
completed all of these are falselets
00:26:32.279
toggled in false and groove Falls and
00:26:34.140
crew just so we can see the visual
00:26:35.880
effect let's make this one true and then
00:26:38.159
what else created an mutate all of them
00:26:41.340
are created right now so then let's map
00:26:44.279
over testing we can do it up here or
00:26:46.620
straight in my HDM I prefer to just keep
00:26:49.080
it separate it makes it more readable so
00:26:52.020
let's just say list is map and so we can
00:26:55.440
just de-structure directly from there
00:26:57.360
and we return HTML and so that is Li
00:27:02.100
with the closing Li and then just a TD
00:27:05.640
task inside okay and then we can just
00:27:07.860
specify this is where it goes so list
00:27:10.080
let's see what we can de-structure from
00:27:12.120
here completed created do IDE title and
00:27:16.559
urgency so obviously all of the titles
00:27:18.480
at the moment are hello let's just pass
00:27:20.820
the actual title cool there we go watch
00:27:23.279
the dog so forth
00:27:25.520
completed and so we can if we're working
00:27:28.440
with a Boolean we can just do this and
00:27:30.840
you saw sometimes I forgo this it
00:27:33.480
doesn't matter if you put the quotes
00:27:34.620
around it or not we can actually just
00:27:36.480
write it like that as well and we can
00:27:38.520
say completed and that's because in the
00:27:40.919
component itself we need to actually
00:27:43.500
state that to be the condition I think
00:27:46.440
it's checked let's see so let's just
00:27:48.779
pass it as a prop so checked and this
00:27:52.440
completed so why don't we have access to
00:27:54.960
this completed this title we I think we
00:27:57.960
maybe need to write it like that yes
00:27:59.640
okay I was actually wrong you don't
00:28:01.559
write it like this you actually pass the
00:28:03.840
class for that type itself in all that
00:28:06.539
we do is we just tell it there is
00:28:08.880
something completed so we can just put
00:28:10.559
it up here we don't assign anything to
00:28:12.600
it we just tell it there is a thing
00:28:14.100
called completed and this seems strange
00:28:16.200
but you know that's JavaScript classes
00:28:18.120
for you now so similar to that task we
00:28:22.020
also want uh tasks themselves to handle
00:28:25.200
them total that shows up so we can
00:28:27.360
actually just copy some stuff from here
00:28:29.760
so just SL dialog put it over here it's
00:28:33.299
hidden and so let's just put it below
00:28:35.039
that and let's just set it to open for
00:28:38.279
now just so we can see what it looks
00:28:39.720
like and SL hide and so forth and the
00:28:43.919
label is just a task let's just use an
00:28:46.980
unordered list for now if we show it
00:28:48.720
this is not the prettiest but you know
00:28:51.179
like I just want to show you guys the
00:28:52.500
JavaScript so we can just put the title
00:28:55.200
here as well and we can also have
00:28:57.919
whether it is completed or not so we can
00:29:01.320
say this completed so if it is completed
00:29:04.440
just show completed otherwise show the
00:29:07.140
text and not completed okay there we go
00:29:09.960
clean room not completed this dot
00:29:13.140
urgency okay and we are actually not
00:29:15.240
passing urgency to that so let's add
00:29:18.419
some extra things here so I've created
00:29:21.059
is type date
00:29:23.720
do is okay so at the moment I don't know
00:29:28.799
so we can just not give it a type and
00:29:31.500
then it's not going to try and convert
00:29:33.720
it if it's an attribute which is okay
00:29:35.700
because we actually don't want to pause
00:29:37.620
these as attributes we want to pass them
00:29:39.360
as props let's just get rid of that up
00:29:41.580
there
00:29:42.299
so now so this urgency so remember what
00:29:46.559
we can do is we can do urgency created
00:29:49.700
uh du okay and what's a title so now it
00:29:54.120
should know all of those exist
00:29:56.399
urgency should show there and we're not
00:29:59.220
passing anything in Via urgency so
00:30:03.059
urgency okay like that and do and that
00:30:08.220
needs to be passed as a prop because it
00:30:09.960
can actually be a date everything else
00:30:11.880
can be passed at as strings obvious
00:30:14.520
except for completed which can be true
00:30:16.260
or false created also gets passed as a
00:30:20.640
prop because it's a date not a string
00:30:23.279
well and you'll see low but we maybe
00:30:25.380
want to map those to something nicer so
00:30:28.620
what we can do is we can say you know
00:30:32.520
urgency display map and low would be
00:30:37.080
this low urgency okay so we map the
00:30:39.779
actual values to how they would be
00:30:42.320
displayed and so this is nicer than you
00:30:44.940
know just a chain of if statements and
00:30:47.460
then we just use the value over here as
00:30:50.760
the actual key okay so that just shows
00:30:52.980
it a bit nicer and then freelance
00:30:56.039
actually has some cool stuff that allow
00:30:57.600
us to format dates nicely so there's
00:31:00.539
some utility stuff here uh format date
00:31:03.120
there's also another one called relative
00:31:05.820
time that allows us to say how long
00:31:08.940
until that so SL and then we just pass
00:31:11.640
it so let's do Li and let's over here
00:31:15.179
just convert it to a string so create a
00:31:18.960
function that's going to calculate that
00:31:20.520
for us so let's just say let's just call
00:31:23.159
it const calc due and so we just accept
00:31:26.760
you and do is null or a date If U does
00:31:32.460
not exist then just return the following
00:31:35.640
HTML span no due date we can actually
00:31:39.779
check if you has passed already so if
00:31:42.360
let's just say cons so technically here
00:31:45.000
it should assume that the U does exist
00:31:47.159
has passed so let's get the current date
00:31:50.100
okay and get time let's also convert you
00:31:53.279
to time get time so the epoch numbers
00:31:56.100
and all we do is we check if the current
00:31:59.700
time is larger or equal to U so if it
00:32:03.779
has passed then maybe just strong due
00:32:07.080
date asked and we passed that as I'll
00:32:10.740
remember we're passing in AST meaning
00:32:13.260
it's actually passing an object
00:32:14.820
technically we can just say return any
00:32:17.700
and then lastly if none of these
00:32:20.220
conditions are met there's a relative
00:32:22.140
time and we also just convert to you to
00:32:25.980
a string so let's just say display and
00:32:29.340
this is just due dot to string throw
00:32:32.820
that in there and also this needs to be
00:32:35.700
wrapped in an HTML so that's a nice
00:32:38.279
function so calc do is just going to
00:32:41.039
return some an a AST for us so you can
00:32:44.340
even you know evaluate a function in
00:32:46.260
here and then we just pass this view
00:32:49.320
okay obviously it opens now for every
00:32:51.840
single one SL relative time what's going
00:32:54.659
on here oh no due date two years seven
00:32:58.620
years again then you can also just have
00:33:01.260
I think there's also a shoelace for
00:33:04.860
um just showing like regular dates a
00:33:07.020
utility so there are some cool utilities
00:33:09.120
here that you can use the format date
00:33:11.279
yeah let's just say we want it like that
00:33:13.440
it's just start this with new and let's
00:33:16.740
start this with create it and then we
00:33:19.019
just throw that in there because there
00:33:20.519
needs to be a created I think I think it
00:33:22.860
takes the current time if we don't pass
00:33:24.899
anything and we can just do this created
00:33:28.320
to to string created and and let's
00:33:32.760
actually make the title the label okay
00:33:35.940
and so then down here let's add some
00:33:38.220
buttons uh maybe in the way that we had
00:33:41.279
it previously so so we can just use
00:33:43.320
adding and let's just grab those put
00:33:46.140
them down here and to cancel save so we
00:33:49.980
can just have close so the primary one
00:33:52.740
can just be closed but then we also have
00:33:54.539
a edit so you can edit it in here as
00:33:57.059
well and let's just remove the event
00:33:59.519
listeners for now and this is not a
00:34:01.500
submit that's close so let's just handle
00:34:03.899
the close for now but you'll probably
00:34:06.899
start seeing like sure there's a lot of
00:34:08.820
different states that this thing can be
00:34:10.440
in and this is where I want to introduce
00:34:12.418
State machines all right so let's have a
00:34:14.699
look at what is a statement and how can
00:34:17.159
this help us manage all the different
00:34:19.139
states that one of these tasks can be in