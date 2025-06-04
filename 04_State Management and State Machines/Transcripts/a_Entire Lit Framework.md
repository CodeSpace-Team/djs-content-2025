Based on the provided lecture transcripts, here's a distilled list of the major and minor concepts discussed:

### Major Concepts

1. **Framework Usage in Application Development**
   - Introduction to utilizing frameworks for enhancing application development, focusing on declarative UI rendering and state management.

2. **Reactive Properties and State Management**
   - Detailed exploration of managing component state and reactive properties within Lit for dynamic UI updates.

3. **Component Abstraction and Composition**
   - Emphasis on abstracting complex UI parts into manageable components, leveraging Lit for easier composition and readability.

4. **Event Handling in Lit**
   - Techniques for attaching event listeners directly within Lit templates for interactive components.

5. **Declarative UI Rendering**
   - The shift towards declarative UI definitions using Lit, highlighting the simplicity and efficiency of describing UI layouts and behaviors declaratively.

### Minor Concepts

1. **Properties vs. Attributes**
   - Differentiation between properties and attributes in the context of web development, especially within the scope of Lit and web components.

2. **Using Lit with TypeScript**
   - Brief mention of utilizing TypeScript with Lit for type safety and advanced JavaScript features, like decorators.

3. **Hot Module Reloading**
   - The benefits of hot module reloading for immediate feedback during development, illustrated through Lit's development server capabilities.

4. **Performance Considerations**
   - Discussion on the implications of unnecessary re-renders and the importance of optimizing property changes to prevent performance degradation.

5. **Lit Element Inheritance**
   - Introduction to creating custom elements by extending the `LitElement` base class for creating encapsulated and reusable web components.

6. **Local vs. Global State Management**
   - Insights into deciding between local state management within components versus global state management for application-wide state.

7. **HTML Native Inputs and Custom Inputs**
   - Examples of using native HTML input types (e.g., `date`) and custom inputs within Lit for form handling and data collection.

This structured list categorizes the core topics and auxiliary points covered in the lecture, offering a clear overview of the subject matter discussed.







00:00:00.000
but let's continue with our app all
00:00:02.520
right so so in here let's just put some
00:00:05.279
spacing there at some point I think I'm
00:00:07.379
gonna have to break this up into a web
00:00:09.540
component but let's keep it at this for
00:00:11.639
now let's just around our input do TD
00:00:15.059
spacing and just give it some bottom
00:00:18.060
spacing so bottom and let's go with
00:00:20.340
large for now okay so this already looks
00:00:22.740
much better I think we can even bring it
00:00:24.600
down to cool and you also see what's
00:00:26.279
really cool about the hot module
00:00:27.840
reloading it updates immediately so you
00:00:30.180
can actually just tweak the values here
00:00:31.980
and it updates we need to specify lot
00:00:38.719
and let's have a look at the slots ah
00:00:42.059
footer so this is just for semantic
00:00:44.100
reasons uh we don't need to care too
00:00:46.320
much about this so you can actually
00:00:49.260
pause label as a string or actually use
00:00:52.079
a label slot why oh because I put it on
00:00:54.840
the form I should put it on the dialog
00:00:58.140
or let's say new task let's also make
00:01:01.500
that this name and just because of the
00:01:05.040
way this is laid out we might want to
00:01:06.720
let's do XL bottom spacing just add more
00:01:09.000
spacing at the bottom okay that looks a
00:01:10.920
bit better
00:01:11.820
and so let's add the other ones as well
00:01:14.400
so we had let's add three more okay and
00:01:18.420
so they are maybe a bit tied together so
00:01:20.939
inside it we can also just use our
00:01:23.220
spacing let's just and do small spacing
00:01:26.280
below let's wrap these in our spacing uh
00:01:30.720
utility component and obviously these
00:01:32.880
won't be named so this will be let's
00:01:35.520
just say title and this will be due date
00:01:38.939
this is called a due and this will be
00:01:42.180
urgency and name is just urgency okay so
00:01:45.840
these are fine but let's maybe update
00:01:47.880
them so so let's do select okay and it
00:01:52.020
also has a fold version and so instead
00:01:54.360
of input this should be select and the
00:01:57.299
options are I can't even remember I
00:01:59.520
think it's it was high normal and low
00:02:02.460
but we can always change that and by
00:02:05.100
default the value is normal and it's not
00:02:08.280
clearable you do need to select one but
00:02:11.760
but normal being the default alright and
00:02:14.459
we can also just say this is fold and I
00:02:17.280
think we also need to provide a label
00:02:19.920
urgency do you take let's see if there
00:02:22.500
is a date selector shoelace not seeing
00:02:26.220
anything here otherwise we can just use
00:02:27.959
the browser one I think we can just go
00:02:30.780
type date that's the bolt in HTML
00:02:33.959
because remember this extends HTML so
00:02:36.360
you should still get the default HML
00:02:39.480
ones and there we go we need to set that
00:02:42.900
to actually be a submit button type
00:02:45.420
submit and let's also just indicate that
00:02:48.180
the other one is just a regular type
00:02:50.760
button cool so it actually adds the
00:02:53.220
tasks but we obviously need to close
00:02:55.379
this now so in our store and if you
00:02:58.860
remember correctly we said that open
00:03:02.220
should actually be dependent on whether
00:03:05.940
the state is adding so here is where it
00:03:10.440
gets interesting because because is
00:03:12.120
remember you just say open if you say
00:03:14.220
open false that's still treated as
00:03:16.560
actual open so ironically you know it's
00:03:19.200
considered open the only way to have it
00:03:21.239
not be open is to not pause open so one
00:03:25.080
way would be to use a ternary so you can
00:03:27.360
go phase equals adding and then you know
00:03:31.379
open if it is adding otherwise just an
00:03:33.480
empty string okay so we can do that and
00:03:36.480
you'll see it as unhappy because it's
00:03:38.940
hard for and this is also what's cool
00:03:40.680
about that Lit plugin that I showed it
00:03:43.260
effectively says like listen this this
00:03:44.879
is very hard for lit to actually do in
00:03:47.459
an optimized manner like you're you're
00:03:49.440
really this is going to become really
00:03:51.060
gross so what lit actually provides us
00:03:54.420
it provides us a way to set props
00:03:57.620
directly in the same way we set
00:04:00.120
attributes so we can effectively go as
00:04:04.379
if we actually grab this object and set
00:04:07.140
something on it whether that is you know
00:04:09.239
the class name or whatever in the domain
00:04:11.640
itself so just search for lit HTML
00:04:14.760
syntax okay and here is the syntax
00:04:17.880
reference so go here just explains how
00:04:21.120
we can control attributes and so it
00:04:23.460
effectively says we can't do this we
00:04:25.740
can't do that which is what we try to do
00:04:27.900
right now so in order for it to actually
00:04:30.840
work in a performant and useful way it
00:04:34.440
needs to set some rules in terms of what
00:04:36.300
we can do and what we can't do you'll
00:04:38.280
find this to be the case in a lot of
00:04:39.780
Frameworks specifically like for example
00:04:41.699
react hooks so react hooks also you know
00:04:45.300
has specific rules and you can actually
00:04:47.040
get it yes plugin that actually warns
00:04:50.220
you when you break those rules so the
00:04:53.040
way we do it is to set a Boolean
00:04:56.280
attribute we start with a question mark
00:04:58.560
okay but we can also so this would
00:05:01.500
probably be what we want to do here but
00:05:03.720
we can also set properties directly by
00:05:06.780
just doing a DOT you can even attach
00:05:09.840
event listeners here to elements for now
00:05:13.560
I'm keeping all my event listeners
00:05:15.180
outside of this but you can actually
00:05:17.040
write your event listeners like this as
00:05:19.320
well and we might I might show you how
00:05:21.060
to do that a bit later all that we want
00:05:23.520
to do is we want to say dot okay and
00:05:26.160
then what that is going to do it's going
00:05:28.020
to set it as a property with JavaScript
00:05:30.120
instead of as an attribute in the HTML
00:05:32.400
so we can just say phase is adding okay
00:05:35.940
it's automatically going to set that
00:05:38.820
property not the attribute directly so
00:05:41.639
you should remember the difference
00:05:42.720
between attributes and properties when
00:05:45.120
we touched on the Dom the very first
00:05:47.160
time all right so now that we've
00:05:49.979
actually set this to be bound to whether
00:05:53.280
it's adding or not at the moment it's
00:05:55.440
not adding so it's not going to be open
00:05:57.600
but if but if we for example say if it's
00:06:00.240
idle cool then it's open all right
00:06:02.699
so then how do we toggle these states so
00:06:05.639
there's all really a lot of
00:06:07.320
functionality that's happening here and
00:06:09.600
so what I'm going to do now is I'm going
00:06:12.419
to pull in a lit HTML the actual
00:06:15.600
framework to show how we can continue
00:06:17.460
with this
00:06:19.320
um we are going to touch on it later
00:06:21.479
again but we're going to look at how we
00:06:23.280
can actually use it along with
00:06:25.500
typescript and something like mob X and
00:06:28.380
so forth but for now I'm going to pull
00:06:30.300
in the framework so I'm gradually
00:06:32.639
showing you how we're kind of pulling in
00:06:35.160
frame parts of Frameworks to solve
00:06:37.380
specific problems for us what I've shown
00:06:39.780
is I've shown how we how we pull in that
00:06:41.699
Lit HTML to give us a way to
00:06:44.060
declaratively write our view or HTML so
00:06:48.300
like this so we don't have to go and
00:06:51.300
attach event handlers and all of that
00:06:53.100
stuff and data attributes and you know
00:06:55.620
manually update values so this is a lot
00:06:58.500
easier to reason about looking at this
00:07:00.600
seeing what happens then that example
00:07:02.639
example we had where we where we
00:07:05.160
manually added a pain child remove
00:07:07.500
element updated actual the check boxes
00:07:11.100
themselves and so forth so this is also
00:07:13.080
just if you're a new developer on this
00:07:15.300
project this is a lot easier just to
00:07:17.160
read at a glance and see what happens
00:07:19.340
and see this as a declarative statement
00:07:22.259
in other words what gets shown here is
00:07:25.740
the task as array length which is much
00:07:28.199
easier to read than if you were to go
00:07:30.720
document query find this thing get the
00:07:33.840
value updated and then figure out what
00:07:35.759
are all the cases that it can update in
00:07:38.160
here because data can only flow in One
00:07:40.080
Direction and it only this function only
00:07:42.539
runs on a re-render you know like in
00:07:45.360
what cases is this gonna update and what
00:07:47.880
is going to cause it to update and also
00:07:50.160
what will the value be when it updates
00:07:51.840
so it's very declarative it's very easy
00:07:53.639
to reason about it's very easy to read
00:07:55.500
and this is one of the primary problems
00:07:57.660
that Frameworks solve for us but then
00:08:00.419
I'm going to pull in the rest of the lit
00:08:02.039
framework you show you some of the other
00:08:03.720
ones and one of them is actually
00:08:05.340
managing interactivity in other words
00:08:07.860
not having to worry about event
00:08:09.360
listeners registering event listeners
00:08:11.479
unsubscribing event listeners finding
00:08:14.160
the thing that the event should be
00:08:16.080
attached to figuring out where it
00:08:18.419
actually came from the right thing all
00:08:20.099
of that so this all actually fits with
00:08:22.860
in this description of hiding the noise
00:08:25.440
so all that noise so the actual
00:08:27.780
traversing the Dom seeing where events
00:08:30.180
came from all that stuff and elevating
00:08:32.099
the essence and what is the essence of
00:08:33.779
what we're trying to do the essence is
00:08:35.880
effectively we just want to say then
00:08:38.520
when something happens on this thing
00:08:40.260
perform this action as simple as that we
00:08:42.419
don't wanna we don't want to worry about
00:08:43.860
the Dom we don't want to worry about
00:08:45.540
event bubbling we want all of that to be
00:08:47.580
hidden and just focus on the essence of
00:08:50.040
what we're trying to express and
00:08:52.019
Frameworks help us do that so we can
00:08:54.060
also pull in lit via CDN once again this
00:08:57.180
is not recommended and and when we start
00:08:59.640
talking about Frameworks I'm going to
00:09:01.200
show you how we would actually bootstrap
00:09:03.480
it with npm and then also with type
00:09:05.880
script but for now we're just using the
00:09:07.620
CDN because there's a lot of other
00:09:09.120
things we need to cover before we can
00:09:11.220
actually look at that so let's just look
00:09:13.260
for lit CDN and so if we go on let's go
00:09:17.339
to the latest documentation keep in mind
00:09:19.560
this is for the actual framework itself
00:09:21.600
that we're going to be pulling in when
00:09:23.399
we use the framework we actually don't
00:09:25.560
need to handle the renders ourselves
00:09:27.660
there's only two abstractions that we
00:09:29.640
use in that is the HTML so creating the
00:09:31.620
AST and then the lit element and the lit
00:09:34.500
element handles for us the actual
00:09:37.440
rendering the event listeners all of
00:09:39.480
that so we just work with the lit
00:09:41.339
element abstraction and we actually use
00:09:43.019
inheritance to extend it it's
00:09:45.300
effectively the lit element so we can
00:09:47.760
actually have a look and see at the
00:09:49.980
inheritance of the slit element and as
00:09:52.140
ranges are generally prefer composition
00:09:54.480
over inheritance but because lit works
00:09:57.000
so close to the actual Dom it almost
00:09:59.760
really doesn't have a choice when
00:10:01.560
something like react really abstracts
00:10:03.899
the Dom far away
00:10:05.940
um let's specifically works very close
00:10:08.220
to the Dom so by that itself it needs to
00:10:11.459
use inheritance so you can actually have
00:10:12.839
a look this doesn't mean you you can't
00:10:15.480
use composition in lit it's just the way
00:10:18.720
it creates its own abstraction is
00:10:20.880
through inheritance but that has no
00:10:23.160
bearing on how you actually write your
00:10:24.839
code you'll see that actually have an
00:10:26.640
entire chapter here just on composition
00:10:29.459
and actually how you can create your
00:10:32.279
components with composition but if we go
00:10:35.040
on the API here and we go to LIT element
00:10:36.660
we can actually look at the source code
00:10:38.399
it actually extends something called
00:10:40.200
reactive element and then if we go to
00:10:42.240
reactive element you'll see that it
00:10:44.579
further extends HTML element you
00:10:48.300
things here and if you remember
00:10:50.100
correctly what I said is that JavaScript
00:10:53.459
classes don't have implements and they
00:10:57.120
don't allow you to create abstract
00:10:58.620
classes but here we see abstract and we
00:11:01.440
see implements so what is going on here
00:11:03.720
and so the thing is effectively you'll
00:11:05.640
see also this file is dot TS so this
00:11:08.760
isn't actually a Javascript file this is
00:11:10.680
actually typescript which we are going
00:11:12.899
to cover when we get to Frameworks but
00:11:15.000
for all intents and purposes be mindful
00:11:17.220
now the typescript is by definition a
00:11:19.800
different language than JavaScript it it
00:11:22.260
even has its own extension okay so this
00:11:25.560
is typescript but the extension part is
00:11:29.040
the same so this is the same thing that
00:11:31.500
gets extended so this is the HTML
00:11:33.300
element that we have worked with and you
00:11:36.060
also see they they have a lot of change
00:11:37.860
Doc in their documentation itself and so
00:11:40.620
if you're curious you know definitely
00:11:42.540
have a look in the actual documentation
00:11:44.459
in the source code itself given a read
00:11:47.399
like see if you can kind of understand
00:11:49.079
and some of the principles it is
00:11:51.000
obviously very high level if you
00:11:52.320
understood everything then you're way
00:11:54.959
overqualified for this course like you
00:11:56.880
can actually go and work with the lit
00:11:58.920
team and bold let but there might be
00:12:02.519
some things that you kind of understand
00:12:04.380
here and there so here's some J stock a
00:12:07.260
function that indicates if a property
00:12:08.940
should be considered changed when it is
00:12:11.040
set the function should take new value
00:12:13.140
and old value and return true if an
00:12:15.839
update should be requested cool has
00:12:18.000
changed Value Old value and Boolean and
00:12:21.240
this type here this is just typescript
00:12:23.579
and we'll get to that later so let every
00:12:26.700
pool inlet and then I will show you how
00:12:30.839
we can actually start using it if we go
00:12:32.820
getting started and we can just use this
00:12:35.160
straight up or we can do what what I've
00:12:37.560
done and which I actually prefer is just
00:12:39.420
put it in our project itself and so it
00:12:41.760
does say here lit is available as single
00:12:44.040
file bundles and this is if you would
00:12:46.320
prefer to use this rather than npm and
00:12:49.079
build tools it does say that they are of
00:12:52.260
type module but it does have a big
00:12:54.420
warning here that says if you're using
00:12:55.920
npm you should use the lit package not
00:12:58.620
these bundles so it says this can cause
00:13:01.800
your page to download more code than it
00:13:04.079
needs so in other words there are some
00:13:07.019
performance implications but for now
00:13:08.760
we're still learning so it's okay and so
00:13:11.040
let's also grab the one that has all so
00:13:13.860
let's get that and you'll see this is
00:13:15.480
much bigger it has a couple of other
00:13:17.160
things Beyond just
00:13:19.380
um the HTML and the render so control a
00:13:22.019
control C to copy it and let's just
00:13:24.540
replace what is currently in here and
00:13:27.000
once again I don't want prettier to try
00:13:29.700
and clean this up we can leave the
00:13:30.899
copyright info here we can leave it
00:13:32.399
exactly as is Ctrl shift p or command
00:13:35.279
shift B and save without formatting okay
00:13:37.740
so we have updated that maybe means that
00:13:41.040
our app is going to break because that
00:13:44.579
specific version of it I don't think
00:13:46.760
abstracts render because now it requires
00:13:50.820
the lit elements to actually handle the
00:13:54.000
rendering so that probably means our app
00:13:56.100
is no longer going to work create over
00:13:58.320
here Ed and just the app itself so to do
00:14:01.620
app all right so let's import Libs lit
00:14:05.540
htmljs and let's see what it exports all
00:14:08.760
right so there's a ton of stuff what we
00:14:11.339
want is we want lit element and HTML we
00:14:15.959
say class and let's just call this app
00:14:18.620
extends lit element so the extension
00:14:22.320
comes with a method called render and
00:14:24.839
that just needs to return and HTML and
00:14:27.480
AST so every component needs a render
00:14:30.300
method that returns an ASD and it
00:14:33.000
actually and this is a case so for now
00:14:35.160
all that we can do is let's just set the
00:14:38.040
type on this to be any for now let's
00:14:39.959
just override this to say it returns in
00:14:43.019
here okay for now we can get to this
00:14:45.240
part later so then custom elements
00:14:48.360
Define and let's do TD app and app and
00:14:53.699
let's import it let's just comment this
00:14:55.980
out because we're now going to handle
00:14:57.360
this in or app component but let's keep
00:15:00.120
on importing our 3D spacing so you can
00:15:03.240
use that actually alongside HTML so
00:15:06.540
where you so as I mentioned you know web
00:15:08.220
components you can use plain web
00:15:09.779
components with any framework so that
00:15:11.940
just means in our HTML we just need to
00:15:14.279
call this TD app call one two three
00:15:16.440
there we go so let's grab all of this
00:15:19.199
and put it in our app now okay and let's
00:15:22.500
just remove this one now and set this to
00:15:25.980
open so here is our app okay but none of
00:15:29.220
this works yet the way that Lit works is
00:15:32.699
we can actually specify State inside our
00:15:35.820
components themselves so let's just
00:15:38.040
quickly go over the lit documentation
00:15:41.639
you just quickly get a sense of what can
00:15:44.220
we do with the actual lit HTML component
00:15:47.699
I'm just going to give it a quick glance
00:15:49.260
I recommend you give it a more intense
00:15:52.019
read so let's click overview so it just
00:15:54.240
talks about how do you define an element
00:15:56.339
a rendering reactive properties Styles
00:15:59.940
and life cycle so let's quickly start
00:16:02.699
with reactive properties so reactive
00:16:05.160
properties actually allow us to set
00:16:08.940
State inside our actual components
00:16:11.579
themselves so this is very similar to
00:16:14.820
like the whole private properties all of
00:16:17.579
that stuff we did but we don't need to
00:16:19.079
fiddle around with Setters and Getters
00:16:20.880
it does all of this for us under the
00:16:22.560
hood so it abstracts away that low level
00:16:24.660
logic
00:16:25.800
um in Getters and Setters so when you
00:16:28.620
see this at don't worry about this this
00:16:31.440
is just using decorators uh decorators
00:16:34.440
are is still experimental in JavaScript
00:16:38.459
so um you'll see here using decorators
00:16:41.579
decorators or proposed feature you'll
00:16:44.100
need to use a compiler like Babel or
00:16:45.660
typescript so we're just going to ignore
00:16:48.300
this phone also when you see like ad
00:16:49.860
property or whatever just ignore it for
00:16:51.899
now
00:16:52.620
um I'm not comfortable using decorators
00:16:54.600
in JavaScript just yet
00:16:56.820
um it can still change quite a bit and
00:16:58.680
so forth so yeah just ignore it for now
00:17:00.839
it actually gives us a warning here that
00:17:02.459
says like unless you're using Babel or
00:17:05.099
typescript maybe ignore decorators for
00:17:07.919
now so then we actually set our
00:17:10.500
properties like this and this will
00:17:12.480
actually expose it on the HTML element
00:17:14.819
itself it actually tells us here to
00:17:16.859
avoid setting properties through rather
00:17:18.839
use the static properties instead of
00:17:21.359
setting properties directly on the class
00:17:23.640
itself it says here that JavaScript
00:17:26.160
classes and have a problematic
00:17:28.740
interaction with reactive properties and
00:17:31.620
a big reason for this is because as
00:17:33.720
mentioned you know JavaScript classes
00:17:35.700
aren't actual classes they're actually
00:17:37.919
prototypes which is why these type of
00:17:39.840
things pop up all the time so this is
00:17:42.120
one way to get around it and this is
00:17:43.860
also one of the reasons why I don't
00:17:45.539
necessarily work with classes that much
00:17:47.340
but because lit tries to be as close to
00:17:50.820
the Dom as possible in terms of
00:17:53.100
Frameworks it's probably the one that's
00:17:54.419
the closest to the Dom it does have to
00:17:57.660
work with properties which is also why I
00:18:00.120
start with lit because I think lit is a
00:18:02.340
is a nice stepping stone into the world
00:18:04.380
of Frameworks because it is the closest
00:18:07.320
to the actual Dom it has it's the
00:18:09.720
smallest abstraction so it makes sense
00:18:11.940
to incrementally build on that and get
00:18:14.100
into deeper and deeper abstractions and
00:18:16.380
so it says here you know according to
00:18:17.820
the rules of JavaScript instance
00:18:19.620
property tax precedence over and hides
00:18:22.140
prototype property yeah here is that
00:18:24.660
scary word prototype you don't need to
00:18:26.880
understand what this means just
00:18:29.280
understand that I did mention prototypes
00:18:31.620
are icky and gross and this is one of
00:18:35.100
the reasons and you don't need to know
00:18:36.840
why this is sticky or gross just follow
00:18:39.299
their advice and use this to create
00:18:41.880
properties on your web components Inlet
00:18:44.220
don't set it directly on the class
00:18:46.559
itself so when we specify properties
00:18:49.620
these are the things that we can set so
00:18:51.840
we can say whether that property is
00:18:53.760
associated with an attribute on the HTML
00:18:56.340
thing itself if it's false then it
00:18:59.039
doesn't if we set converter then it
00:19:01.919
actually which specify how the attribute
00:19:04.679
should be converted into a property once
00:19:07.260
again remember the difference between
00:19:08.760
properties and attributes reflect means
00:19:11.760
that it keeps the attributes and
00:19:13.260
properties in sync because by definition
00:19:15.419
usually if a property updates the HTML
00:19:18.360
attribute doesn't update as well so
00:19:20.820
reflect does that but only use reflect
00:19:23.400
if you need to because it has
00:19:25.320
performance implication patients keeping
00:19:27.059
those two things in sync and then
00:19:28.620
there's also type but it does say here
00:19:30.840
if attribute is false then all these
00:19:33.720
others are con are ignored so they are a
00:19:36.240
bit further down so as mentioned you can
00:19:38.340
also pass a converter which tells it how
00:19:40.440
to convert an attribute to a prop has
00:19:43.200
changed you can provide it a callback
00:19:45.299
that it can use to determine whether the
00:19:48.000
property changed or not so we did
00:19:50.280
something almost similar when we used
00:19:52.860
Getters and Setters so there were
00:19:54.480
instances where we checked if this value
00:19:56.880
didn't change just return immediately
00:19:59.100
don't do anything so it does that by
00:20:01.380
default by default it just does a hard
00:20:03.179
check against the value itself but
00:20:06.120
because you have things like objects and
00:20:08.220
so forth that have references you might
00:20:10.740
want to actually create your own custom
00:20:12.660
way to check or there might be some
00:20:14.580
other logic where it's dependent on
00:20:16.500
something else whether it should
00:20:18.000
consider changed or not so no accessor
00:20:21.240
don't worry about this this is very
00:20:22.919
Advanced
00:20:24.179
um just keep it false on the default
00:20:26.720
reflect as I said what this does is that
00:20:29.460
if the property changes you can tell it
00:20:31.679
to actually change the attribute as well
00:20:34.320
don't set this to True unless there's a
00:20:37.320
reason why because as mentioned you know
00:20:40.200
it's false for a Reason by default and
00:20:42.720
that's because it does have a
00:20:44.160
performance implication so then State
00:20:46.500
and state is kind of what we're going to
00:20:48.120
use now for the most part and state is
00:20:51.360
effectively it's just internal State
00:20:53.460
it's an internal property you can't
00:20:56.400
influence it from outside so it
00:20:58.980
automatically sets attributes to false
00:21:01.260
and so forth so this is just internally
00:21:03.720
tracking state of something inside the
00:21:05.880
component without you being able to
00:21:07.679
access that state from outside because
00:21:09.720
obviously lit uses Shadow Dom and all
00:21:12.539
those things under the hood and the
00:21:14.340
other thing is attributes by default are
00:21:16.140
always strings when you pass them so you
00:21:18.240
can actually specify a type so if you
00:21:20.580
say it's a number it automatically
00:21:22.200
converts it for you to a number or a
00:21:24.360
Boolean or any of those stuff remember
00:21:25.919
remember we had to check previously
00:21:28.140
whether it is not null or whether it is
00:21:31.440
an empty string to determine if it's
00:21:33.539
true or false so it just does those type
00:21:35.700
of things for you automatically and so
00:21:38.039
for ehere it shows how to create state
00:21:40.020
with a decorator as mentioned we're just
00:21:42.600
going to ignore decorators for now so
00:21:44.220
here it shows how to do it without a
00:21:45.780
decorator and this is how we do it so
00:21:47.880
decorate is just abstract this away for
00:21:50.039
us so we still need to set the default
00:21:53.100
state in our Constructor when we declare
00:21:56.159
it in properties so it says here you
00:21:58.320
know State shouldn't be referenced from
00:22:00.059
outside the component this underscore
00:22:02.460
and this is only for typescript you
00:22:05.039
don't need to do this in plain
00:22:06.240
JavaScript so it does say here you
00:22:09.000
should indicate private properties like
00:22:10.799
this uh I'm not a fan I I don't do that
00:22:14.220
so it says it recommends using a
00:22:16.320
convention like this
00:22:18.179
um but I don't know like it's I'm not
00:22:20.220
necessarily a fan of this but you can do
00:22:22.860
it if you want and so it says
00:22:24.360
effectively the thing of state is the it
00:22:26.400
doesn't match an actual attribute or a
00:22:28.200
property so you can't access it from
00:22:29.640
outside and so here just goes into the
00:22:31.799
details like what actually happens if a
00:22:34.559
property changes and so forth and this
00:22:36.720
is where lit the actual framework comes
00:22:40.140
in because up until now we've used lit
00:22:42.299
HTML which gave us a way to render our
00:22:45.900
HTML declaratively express our view
00:22:48.179
declaratively but now there's another
00:22:50.460
question that's at a higher level of
00:22:52.559
abstraction than the clarity of
00:22:55.320
expression of Hashim Allen views and
00:22:57.480
that is when do you render so you'll see
00:23:00.299
the actual lit framework doesn't give us
00:23:02.220
the render function and the reason for
00:23:04.140
that is the framework itself figures out
00:23:06.299
when to render it takes that away from
00:23:09.360
you it moves that to the low level of
00:23:11.820
the abstraction because it doesn't see
00:23:13.380
that as the essence of creating apps you
00:23:16.559
shouldn't actually manually tell the UI
00:23:19.740
when to re-render you should just say
00:23:22.140
how it should render and then just write
00:23:24.240
your logic and the framework is self
00:23:26.400
should figure out when it re-renders so
00:23:28.740
this is the other key pillar of
00:23:30.780
Frameworks is that Frameworks also
00:23:32.880
handle for you not only a declarative
00:23:35.520
way to express how your app should read
00:23:37.740
how your app should render but it also
00:23:40.320
handles the internal logic based on
00:23:42.900
other things in the framework in terms
00:23:45.059
of when it should actually render when
00:23:46.980
should it up and the way that Lit does
00:23:49.860
it is whenever any of these things that
00:23:52.320
you declare here in properties changes
00:23:54.419
it's going to run the render function
00:23:57.120
again so then it's going to create those
00:23:58.919
two asts and compare them and if those
00:24:01.440
ASDS are exactly the same then it's not
00:24:04.020
going to update the HTML but that
00:24:06.059
process of comparing the asts obviously
00:24:09.000
takes computational resources so you
00:24:11.700
don't want to compare those to create a
00:24:13.860
new ASD and compare them if it's not
00:24:15.720
needed so once your app reaches a
00:24:17.640
certain size it's no longer enough just
00:24:20.400
actually not rewriting the entire HTML
00:24:23.940
every render but you also want to
00:24:25.679
announce start preventing unnecessary
00:24:28.500
evaluations in your app itself whether
00:24:31.620
it should render or not so once again
00:24:33.900
you know now we're moving into a higher
00:24:36.179
level of decision making and this is a
00:24:38.280
pattern that you'll find over and over
00:24:40.020
and over again as we get deeper into
00:24:42.419
abstractions the type of decisions we
00:24:45.419
make and the type of code we write
00:24:47.840
gradually become of a higher nature
00:24:50.820
because now we're dealing with should it
00:24:52.860
actually even determine whether it
00:24:54.720
should re-render or not but so we
00:24:56.580
gradually work our way up that
00:24:58.260
abstraction because if you're just
00:25:00.240
jumping into something like react
00:25:01.919
without understanding the Dom
00:25:03.659
understanding any of this you're going
00:25:05.880
to have a hard time understanding what
00:25:07.200
is the relationship between properties
00:25:09.179
AST or the virtual Dom and also why is
00:25:12.780
it even important to be able to
00:25:15.480
determine whether a property has changed
00:25:17.640
so we need to kind of build our
00:25:19.740
understanding of these abstractions up
00:25:21.480
incrementally for you to actually
00:25:23.700
understand why a certain things are
00:25:26.460
important this brings us back to that
00:25:28.380
conversation I had about just learning
00:25:30.299
the abstraction if you just learn the
00:25:31.980
abstraction if you just learn this is
00:25:33.539
how you do it and this is what you do
00:25:35.039
when weird things happen so for example
00:25:37.320
if your component so let's say you
00:25:39.360
accidentally set has changed to true now
00:25:42.120
all of a sudden your app is going to be
00:25:44.100
really really slow because it's always
00:25:46.200
going to check if it should re-render
00:25:48.179
and if you don't understand some of this
00:25:50.220
lower level logic you're not going to be
00:25:52.140
able to debug that you're not going to
00:25:53.700
know why the app is slow so we're
00:25:55.559
gradually working our way up that
00:25:57.240
abstraction so one way properties can
00:25:59.279
change is from outside so if the parent
00:26:01.740
changes what gets passed to a component
00:26:04.260
that component will re-render or it will
00:26:06.240
revaluate but another way is from inside
00:26:08.700
the component itself and that is by
00:26:10.620
means of event listeners we touched on
00:26:12.720
this super briefly when we looked at lit
00:26:15.480
HTML but effectively here's an example
00:26:18.120
so this add click so we can actually
00:26:21.179
write our event listeners in here and it
00:26:24.480
binds it for us and everything thing we
00:26:26.340
don't need to find the node we don't
00:26:28.020
need to attach it to a Dom node we can
00:26:30.960
actually write our event listener as a
00:26:33.900
method and then just attach it and so
00:26:36.120
what this does is it takes the count
00:26:38.520
value in here that we specify there and
00:26:41.400
it actually just updates it down here is
00:26:43.620
an example there we go and if this is
00:26:45.720
looking very strange ensure that it's
00:26:47.640
not set on typescript so up here you'll
00:26:49.679
see various and TS so on TS it's like
00:26:52.559
what language is this this doesn't look
00:26:54.659
like JavaScript and yeah rightfully so
00:26:57.539
um it isn't it's a different language so
00:26:59.340
just ensure it's set to JS otherwise
00:27:01.740
it's going to look a bit wacky all right
00:27:03.360
so here's our TD app and let's continue
00:27:06.659
working inside it so let us actually
00:27:09.480
create yet another abstraction and this
00:27:12.480
is going to contain all the logic that
00:27:15.900
handles the adding of tasks and let's
00:27:18.360
call it adding so let's just copy and
00:27:20.640
paste the code from here and just
00:27:23.460
extract the parts that related to the
00:27:25.740
adding and I think we have the button
00:27:28.140
and then just the hidden dialog below it
00:27:31.140
but so these two are bound together as a
00:27:33.960
single unit and let's call it adding and
00:27:36.360
TD adding and in our app let's remove
00:27:38.880
all of this put it over here as PD
00:27:42.720
adding so import compare opponent and TD
00:27:47.520
adding should show up there why is it
00:27:50.520
not let's just cancel log whoops
00:27:54.000
the debut wrote this is STD adding that
00:27:56.640
is definitely not what we want all right
00:27:59.480
editing so and let us actually create
00:28:04.200
the interface for that
00:28:06.179
so you can go static properties and that
00:28:10.260
just returns an object and so let's keep
00:28:12.720
all the properties just inside it for
00:28:14.880
now let's say open which is type Boolean
00:28:18.000
and also state is true oh sorry my bad
00:28:22.919
it's actually we specified actually as
00:28:25.740
an object like that so then in our
00:28:28.440
Constructor let's set that this open
00:28:31.320
equal starts as false and it's unhappy
00:28:34.500
because remember we need to call Super
00:28:36.299
so remember what it says is we shouldn't
00:28:38.880
do this like that so we shouldn't set it
00:28:41.460
like that we should set it in the
00:28:43.020
Constructor
00:28:44.460
um otherwise this is just the way let
00:28:46.200
works and because of weirdness in
00:28:49.020
JavaScript we need to do this so then
00:28:51.659
what we can do in our render let me just
00:28:54.120
cancel log it this open when we render
00:28:57.360
and so if I bring this in here you will
00:28:59.640
see it's false then we need to obviously
00:29:01.919
bind this and you know remember we want
00:29:04.679
to actually set the prop as follows so
00:29:07.320
this should be bound to this open let us
00:29:10.440
create a method for us in this component
00:29:12.720
that toggles with its open or closed so
00:29:15.240
let's just say toggle open that's just a
00:29:17.880
method and all it does is it takes this
00:29:20.520
open and it sets it to the opposite of
00:29:23.820
this open let's add an event listener on
00:29:27.179
this button so what we can do is we can
00:29:29.039
say add click in a lit you specify that
00:29:33.480
it should attach an event listener in
00:29:35.100
this manner and then what should that
00:29:36.960
call call this toggle open they're still
00:29:40.080
going to do all the things in terms of
00:29:41.580
passing the event and all of that but
00:29:44.039
it's just a more declarative way to
00:29:45.960
indicate actions instead of going and
00:29:48.899
imperatively adding the event listener
00:29:51.240
and looking at the event and so forth
00:29:54.000
cool works as easy as that but something
00:29:56.760
strange is happening here and you'll see
00:29:58.320
if we say add task and we close it and
00:30:01.440
we click add task again it doesn't open
00:30:03.600
it again so let's see what's going on so
00:30:06.059
console log what open is going to set to
00:30:09.299
when open toggles bring this in here
00:30:11.880
just ignore this okay so it's set to
00:30:14.460
true you click and that doesn't actually
00:30:16.740
update open and then if we click here it
00:30:18.899
sends it to false and only then to add I
00:30:21.480
said the reason is because this
00:30:22.679
component has its own State you know a
00:30:24.720
lot of times that is kind of one of the
00:30:27.600
things you need to manage because
00:30:30.260
unfortunately the reality is you can't
00:30:32.700
put everything in your Redux store
00:30:35.460
because otherwise your app will just get
00:30:37.679
too slow and I've seen people do this
00:30:40.320
type of thing and it always starts out
00:30:42.480
really nicely but it becomes very
00:30:44.520
unmaintainable I've literally seen
00:30:46.260
people go and every time someone puts a
00:30:49.380
character in an input they update the
00:30:51.840
entire store and that's usually when you
00:30:53.940
see apps where as you're typing it slows
00:30:57.059
down as you're typing and it lags a bit
00:30:59.820
that's usually when someone's doing
00:31:01.320
something crazy like that they're
00:31:03.120
updating the entire store with on every
00:31:06.360
key press so you do need to keep some
00:31:09.000
localized State and this is also where
00:31:10.919
that kind of container pattern comes in
00:31:12.659
so the containers are the points where
00:31:14.940
your components connect to the store but
00:31:18.480
your components themselves should also
00:31:20.279
have local state and honestly this is a
00:31:22.860
hard thing it's a hard architectural
00:31:24.539
thing figuring out where like whether
00:31:27.600
the state should be local or whether
00:31:29.100
should be in the global store the answer
00:31:31.140
isn't to make everything local or to
00:31:33.480
make everything part of the global store
00:31:35.340
that is unfortunately something that
00:31:37.559
with time as you gain more experience
00:31:39.240
you'll get a better feel for I also do
00:31:41.820
feel it's similar to abstraction and so
00:31:44.520
forth the only way to learn is to mess
00:31:46.440
it up and get it wrong but with time you
00:31:48.659
get a better sense for that and this is
00:31:50.399
also where State machines come in and
00:31:52.740
I'll talk about State machines in a
00:31:54.360
second and I'll illustrate how thinking
00:31:56.880
about components as state machines this
00:32:00.000
actually helps us make better decisions
00:32:02.460
in terms of where the state should lift