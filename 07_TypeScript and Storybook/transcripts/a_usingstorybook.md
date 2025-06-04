00:00:00.000
I am going to show you guys how I would
00:00:03.240
approach something similar to the actual
00:00:05.220
Capstone that you need to do what I have
00:00:07.980
done on my side is I have also created
00:00:11.160
something similar as your Capstone
00:00:13.679
project you will be using the this
00:00:15.780
podcast API if you don't know what an
00:00:17.760
API is if you don't know what https if
00:00:19.859
you don't know what the fetch API is any
00:00:21.420
of that stuff if you don't know what any
00:00:23.160
of this is don't worry for now just know
00:00:25.859
that the data that you're going to be
00:00:27.420
using live somewhere on a server and
00:00:30.119
what your app is going to have to do
00:00:31.320
your app is going to have to hit that
00:00:33.059
server and pull that information into
00:00:35.399
the app in the readme file it kind of
00:00:37.380
covers a bit about like how the
00:00:38.640
information is structured how it relates
00:00:40.440
to one another what are the endpoints
00:00:42.059
that you can hit and so forth I have a
00:00:44.280
much more reduced version of this which
00:00:46.680
is just like a collection of some movies
00:00:48.660
and stuff some of the information is
00:00:50.879
actual real information some of it is
00:00:53.340
just mock information because obviously
00:00:54.960
I didn't want to go all out and scrape
00:00:56.940
the entire web just for an example that
00:00:59.039
I'm going to show you guys we're going
00:01:00.780
to use this API and that's going to
00:01:02.640
return you a list of movies so some
00:01:04.860
basic information about movies so for
00:01:06.720
example you know the Dark Knight Lord of
00:01:09.060
the Rings Schindler's List Pulp Fiction
00:01:11.220
and so forth and also images associated
00:01:13.380
with those movies so this is completely
00:01:15.659
made up the amount of actors you
00:01:17.400
probably know that there isn't only a
00:01:19.439
single actor in The Dark Knight I'm not
00:01:21.299
good with actors ask me about JavaScript
00:01:23.400
you can do is then you can further go
00:01:25.380
into let's say eight to Pulp Fiction we
00:01:27.900
want more info about that we can go
00:01:29.340
forward slash IDE and eight then it
00:01:31.920
returns more info for us and we can also
00:01:34.500
get movies by genres so you'll see that
00:01:38.220
Pulp Fiction is genre three in terms of
00:01:41.220
the genres you can also see so I think
00:01:42.720
three is horror obviously Pulp Fiction
00:01:44.520
isn't horror but this is just for
00:01:46.619
illustration purposes so we can go genre
00:01:49.560
forward slash three you know and that
00:01:51.840
shows all the horror movies you know
00:01:54.060
like the the all-time big horror movie
00:01:56.640
called Forrest Gump in here I'm not
00:01:58.740
going to show you guys how to fetch this
00:02:00.540
from the server just here what I'm going
00:02:02.340
to show you is how we would build out
00:02:03.780
the app itself and what I generally do
00:02:06.060
is I start working from two sides so I
00:02:09.119
start working from the UI working my way
00:02:11.760
towards the middle of the app and then
00:02:13.860
also start from the API side and so what
00:02:16.560
I'm going to do now is I'm going to
00:02:17.700
figure out what the UI is going to be
00:02:19.560
like based on the information we have at
00:02:22.080
hand I find it useful to just do a
00:02:24.480
little bit of sketching once again this
00:02:25.980
isn't like uml charts or any of that
00:02:28.440
stuff this isn't formalized as I showed
00:02:30.480
in that other video that I did I do it
00:02:33.060
very roughly you know like almost think
00:02:34.680
about it like as like a piece of pen and
00:02:37.020
paper or like on the back of a napkin or
00:02:39.120
whatever the point is this shouldn't be
00:02:41.160
shown or given to anyone this is just
00:02:43.140
for yourself to start making sense
00:02:44.640
there's some really cool tools for this
00:02:46.920
type of thing you can do Json to
00:02:49.440
typescript you can just put it in here
00:02:51.360
and then so I can just copy all of this
00:02:53.340
put it in here and it actually gives me
00:02:55.800
some shapes for it in typescript so and
00:02:58.800
let's just call this pre view okay so
00:03:01.080
this is a movie preview and it does
00:03:03.060
interfaces I prefer to do types I'm
00:03:05.340
going to be using a lot of tools here
00:03:06.900
obviously using typescript I'm going to
00:03:08.580
be pulling in you are not obliged you
00:03:11.400
are not required to actually use any of
00:03:13.500
these you can do what you want you can
00:03:15.599
build this app how you want these are
00:03:17.940
just tools that I'm showing you that can
00:03:19.739
help you and if you want to play around
00:03:21.840
with them and so forth but in terms of
00:03:23.640
if you just want to build out this
00:03:25.019
entire app just with basic react with
00:03:27.360
the single use tape you're welcome to do
00:03:29.459
that if you also want to go like I don't
00:03:31.319
fully understand typescript I'm not
00:03:32.879
comfortable with typescript you're
00:03:34.260
welcome to not build it with typescript
00:03:35.760
okay but obviously the more stuff you
00:03:37.500
can display in your portfolio the better
00:03:39.239
in terms of your career prospects and
00:03:41.819
possibility of getting employed so
00:03:43.799
there's only a pretty view actual
00:03:45.900
full-on shape itself in terms of how do
00:03:48.840
you figure out what this what is the
00:03:50.640
shape of your data more often than not
00:03:52.920
you'll speak with like whoever like
00:03:55.140
creates the API or there will be some
00:03:57.060
documentation so you'll see for example
00:03:59.280
in the podcast what I've actually
00:04:00.720
documented like what are the shapes like
00:04:02.580
this is a string this is an array how do
00:04:05.040
they relate to one another and so forth
00:04:06.959
I know there's two things the one is
00:04:09.180
like a preview of a movie and then the
00:04:12.120
other one is the actual all the info
00:04:13.799
about the movie itself so let's just
00:04:15.959
call that type movie let's keep act as a
00:04:19.079
separate thing let's do type actor and
00:04:21.298
actor has ID first name last name and
00:04:23.880
and image and this is an array of actors
00:04:27.000
and the reason why I do this is just so
00:04:29.520
we know what is available to us when you
00:04:32.220
start doing a basic design of your app
00:04:34.139
like you obviously don't want to say oh
00:04:35.880
we're going to show you how what the
00:04:38.040
rating of the movie was or whatever but
00:04:40.020
you don't even have that information
00:04:41.100
available what do we want to do in our
00:04:43.440
app so we want to show list of movies
00:04:45.540
okay there's probably going to be some
00:04:47.759
preview component and then when you
00:04:49.800
click on it it should probably show like
00:04:51.840
the full movie info okay let's figure
00:04:53.880
out in the preview uh what is that going
00:04:56.040
to be like design wise so let's just
00:04:58.080
draw it up here so the ID we're just
00:05:00.660
going to use as the key the title let's
00:05:03.060
put the title up there and the release
00:05:05.460
date and obviously the image of the
00:05:07.320
movie itself let's put it here on the
00:05:09.060
side oh let's maybe put actors there as
00:05:11.280
well and we can maybe just have like a
00:05:13.080
little arrow like this that indicates
00:05:14.460
you can click on it so then when we are
00:05:16.139
here we have the image again similar to
00:05:18.900
how we did it with the book connect
00:05:20.220
thing where we kind of have it floating
00:05:21.960
here and then a background version of it
00:05:24.000
that's blurred over here then we have
00:05:25.919
the title of the movie down the release
00:05:28.380
the description and we can truncate that
00:05:31.680
you know if it's too long and then have
00:05:34.680
a show more button shows the rest let's
00:05:37.440
also put duration here genres actually
00:05:40.080
above the title over here then we would
00:05:42.419
list the actors down here so we just to
00:05:44.880
have an image first name and a last name
00:05:47.220
all right so here we have our app again
00:05:48.840
let's sketch out the phases that it can
00:05:51.240
be in we're not going to fetch the data
00:05:53.639
from the API right now but we want to
00:05:55.680
build our app in a way that it can
00:05:57.600
actually receive data so we're going to
00:05:59.820
mock that data for now and I'm going to
00:06:02.220
show you how you do this with something
00:06:03.300
like faker.js what are the phases that
00:06:05.880
the app can be in and this is where
00:06:07.199
State machines and those type of things
00:06:08.820
come in so there's obviously a loading
00:06:11.220
phase so obviously the podcast app has a
00:06:14.820
bit more complexity in it than what I'm
00:06:16.979
dealing with here because otherwise you
00:06:20.100
guys are just going to Loosely copy and
00:06:21.720
pick which isn't really useful to anyone
00:06:23.819
because then I could have given you guys
00:06:25.440
this is the very first assignment
00:06:26.940
without understanding any JavaScript you
00:06:28.740
just literally follow what I do you need
00:06:30.660
to solve some problems but that being
00:06:32.759
said so I'm going to cover like the
00:06:34.800
basics but then there is a lot of room
00:06:36.960
on top of that where you need to solve
00:06:39.060
problems yourself with all the knowledge
00:06:40.979
you've gained up until now basically if
00:06:43.620
you think about it most apps show a list
00:06:46.740
of information it allows you to navigate
00:06:48.539
that information that allows you to sort
00:06:50.280
that information some apps allow you to
00:06:52.500
actually edit the information delete it
00:06:54.240
and so forth you know think about
00:06:55.560
Netflix Netflix is the same principle uh
00:06:58.380
think about you know Facebook or Twitter
00:07:00.539
like you've you'd look at tweets you go
00:07:02.940
into tweets you can comment on Twitch
00:07:04.560
you can filter things or apps
00:07:06.840
effectively just allow you to Traverse
00:07:08.819
data bird watching it can be like a
00:07:11.819
directory of cars or stores or most apps
00:07:15.600
follow this blueprint so there's going
00:07:17.160
to be a loading phase where there isn't
00:07:18.720
any data yet look at the list then this
00:07:21.240
can be a phase where we're looking at a
00:07:22.979
single item so list loading can't do
00:07:25.860
anything list is this then single you're
00:07:28.680
looking at a single so you can go back
00:07:30.120
to list from there can you go there's
00:07:31.919
nowhere you can go from single loading
00:07:34.680
so the only place you can go from
00:07:36.419
loading is to list and when you're in
00:07:39.419
list you can go to one of two places you
00:07:43.020
can go to a single item or you can go to
00:07:46.139
the filter don't go to the filtering
00:07:47.699
from a single item all right so let's
00:07:49.380
just for now say the filtering is just
00:07:51.300
going to be pop up and let's just set up
00:07:53.520
here is you know like filter click that
00:07:55.620
it shows an overlay and in that overlay
00:07:57.960
what can you filter by plain text you
00:08:00.539
know just search genre amount of actors
00:08:03.539
uh release okay so that's probably
00:08:06.360
sufficient and then from there you can
00:08:08.460
only go back to list single you can only
00:08:10.740
go back to list so what I'm going to do
00:08:12.720
is I'm going to start by setting up a
00:08:15.060
react with Veet also setting up
00:08:17.580
storybook npm create beat at latest and
00:08:22.319
then it's going to ask us what we want
00:08:24.180
so let's just call it a movie app and
00:08:27.120
we're going to use react and we're going
00:08:29.039
to use just a regular typescript you can
00:08:31.080
just do the JavaScript if you want I'm
00:08:33.539
going to show you guys how to do Tasker
00:08:35.219
for those of you that want to and then
00:08:37.080
just the code dot so we open this in vs
00:08:39.719
code let's get started on storyboard so
00:08:42.679
storybook.js.org just going to say get
00:08:44.880
started and then I'm going to tell you
00:08:46.440
what Storybook is I did show it on some
00:08:49.440
occasions MPX storybook at latest and
00:08:52.500
Inlet npx storybook at the latest in
00:08:55.200
that storybook allows you to create your
00:08:57.779
components in isolation where you can
00:08:59.880
control you know what props they get and
00:09:03.120
so forth and you can build them out
00:09:04.620
without setting up all the logic like
00:09:07.140
where the data comes from and so forth
00:09:09.240
it's really cool I think they have an
00:09:10.980
example up so you know and then you can
00:09:12.480
see what all the props you can pass and
00:09:14.519
and whatever and you can see the
00:09:15.959
different components and how can you so
00:09:17.880
it's also self-documenting and you can
00:09:19.980
update the props and see what happens
00:09:22.080
with the components so it allows you to
00:09:23.760
play around with components testing it
00:09:25.740
out figuring out how components work
00:09:28.200
that someone else built and so forth and
00:09:29.940
this is really helpful especially when
00:09:32.640
you're building very complex things and
00:09:34.260
storybook might actually be a bit
00:09:35.940
overkill for what we're doing look at
00:09:37.860
this project so this project is pretty
00:09:40.140
big I think I showed it last time these
00:09:42.300
components kind of like the API and the
00:09:45.180
store and all that stuff here are all
00:09:47.820
the tests and so forth and you can drill
00:09:49.920
down into them so yeah mostly just going
00:09:52.140
to be covering the component stuff now
00:09:54.000
the next session we're going to be
00:09:55.260
looking at the model and so forth so
00:09:56.820
specifically what I want to show you
00:09:58.080
guys is kind of like the authentication
00:09:59.820
and so if you want to build out what
00:10:01.320
does it look like when someone's logged
00:10:02.700
in what does it look like when someone's
00:10:03.959
creating account resetting their
00:10:05.279
password and so forth you obviously want
00:10:07.320
to do that in an isolated instance you
00:10:10.380
don't want to go onto your real data and
00:10:12.660
every time reset an account see what it
00:10:14.940
looks like change the color of the
00:10:16.200
button go through that process again go
00:10:18.240
back to the database reset it again you
00:10:20.580
want to work against fake information so
00:10:22.920
you can toggle and see like fake the
00:10:25.200
state of it so you can work on how it
00:10:26.820
looks and so forth without having to
00:10:28.740
manually make changes in your your
00:10:30.420
actual real data and go through the
00:10:32.580
actual real processes not only that but
00:10:34.800
sometimes you might be working on
00:10:36.000
features that haven't been built out we
00:10:38.160
are now going to be working on like this
00:10:40.140
app although we haven't created a way to
00:10:42.480
actually fetch the information yet so
00:10:44.399
for example if we look over here we look
00:10:46.079
at the components so you can also write
00:10:48.060
your documentation in here so here's the
00:10:49.860
documentation in terms of how everything
00:10:52.019
works for this component and then this
00:10:54.180
is split up into three sub components so
00:10:56.700
this one is the actual authentication
00:10:58.740
model so it can be in one of Six States
00:11:03.120
it can be in login it can be in create
00:11:05.820
it can be in change notice or reset okay
00:11:10.200
so these are all the states that it can
00:11:12.600
be in so if you are in notice then
00:11:15.540
whatever is set so you'll see it updates
00:11:17.459
real time and it shows you what it would
00:11:19.440
look like if you pass a specific string
00:11:21.360
here if you don't pass anything to send
00:11:23.040
email this is what it looks like and
00:11:24.899
then likewise in connection so you can
00:11:26.880
see this is what it looks like none when
00:11:28.800
you're viewing your key when you're
00:11:30.720
adding a key when you when it's closed
00:11:32.880
when you edit you attempt to disconnect
00:11:35.040
it and then also you can toggle okay so
00:11:37.620
when you're viewing it a full account it
00:11:40.079
says active but you know if it's
00:11:42.000
disconnected this is what it shows if
00:11:43.680
it's invalid this is what it shows if
00:11:45.839
it's importing this is what it shows so
00:11:47.940
this is the phase and this is the actual
00:11:49.560
state of the data if it's a closed
00:11:51.779
phased during import this is what it
00:11:54.000
shows if it's the closed phase to be
00:11:55.860
invalid and so forth and so forth and so
00:11:58.260
forth you can also then write acceptance
00:12:00.839
tests I I didn't I don't know whether
00:12:03.180
we're going to get to that this is a bit
00:12:05.160
more complex but I'm going to show this
00:12:06.540
to you for example here you actually
00:12:08.940
don't even see it because it happens so
00:12:10.740
fast like it does like all these things
00:12:13.260
it runs through everything checks if
00:12:15.240
everything works so it's like literally
00:12:17.040
split seconds so you'll see you can just
00:12:19.079
go through it and you can see all the
00:12:20.459
tests actually pass you can actually do
00:12:22.800
a test runner in your terminal as well
00:12:24.899
let me show you super quickly npm run
00:12:27.360
test storybook I think is what the
00:12:29.880
screen group is called well so that
00:12:31.800
starts and it figures out what tests to
00:12:34.380
run okay and it's running all of them it
00:12:36.600
uses actual chromium we run them yeah
00:12:38.940
this pass pass pass and it passed cool
00:12:41.519
so all tests passed so what we do is we
00:12:43.620
have this as acceptance test you can't
00:12:45.420
actually push code to the reaper unless
00:12:47.579
all the test pass this avoids bugs
00:12:50.040
getting introduced and so forth like so
00:12:52.320
what these actually run is these things
00:12:54.180
but you can't step through it it checks
00:12:56.700
is it showing the password and that is
00:12:59.339
true so is it showing the password
00:13:01.139
screen right Next Step It selects
00:13:03.660
password and it tries to save and it
00:13:06.540
checks do you get this error Next Step
00:13:08.820
It enters something into the password it
00:13:10.560
tries to save you check do you get the
00:13:12.600
error that says your password is too
00:13:14.100
short next step it makes it long enough
00:13:16.320
tries again checks if it gets this error
00:13:18.959
Next Step next step and then it checks
00:13:21.360
like does it take you to account so all
00:13:23.760
of these pass yeah so it allows you to
00:13:25.680
set up these acceptance tests that and
00:13:27.779
obviously the more you write the more
00:13:29.760
stable your app Gates over time and
00:13:31.800
that's maybe a bit too advanced but I
00:13:33.959
just want to show you how far you can go
00:13:35.760
a storybook where my Mercy is going to
00:13:37.620
be focusing on the component side of
00:13:40.139
things so we have set up storybook now
00:13:42.240
so what we can do is should
00:13:43.920
automatically in our package add here
00:13:46.560
storybook so we should be able to just
00:13:48.300
run and run storybook there we go let's
00:13:51.240
click on that okay cool so this is just
00:13:52.740
like the base storybook setup it just
00:13:55.019
has like an introduction explaining to
00:13:56.760
you what is Storybook show some example
00:13:59.339
things that you can play around with and
00:14:01.019
so forth so we are going to delete all
00:14:03.060
of that and we're going to Let's
00:14:04.320
actually delete all the preset and place
00:14:07.139
all the stuff that comes to the feed
00:14:08.760
Comes The Storybook all of that this is
00:14:11.040
just a storybook configurations public
00:14:13.139
so let's get rid of this beat logo and
00:14:15.660
Source all right so what I would do is I
00:14:18.420
would just create components I would get
00:14:20.700
rid of assets keep the story stuff for
00:14:22.920
now and what I would do is I would
00:14:24.660
actually put my components in folders
00:14:27.360
let's just start with app and inside
00:14:29.459
that I have app.tsx I have a export it
00:14:34.860
just takes everything so export wildcard
00:14:37.260
from
00:14:38.540
app.tsx and they just X4 said so when
00:14:41.220
you hit this folder it automatically
00:14:43.260
takes whatever index is so you don't
00:14:45.600
need to go into the folder and extract
00:14:47.760
something and let's just in here just do
00:14:49.980
const app for now and just something
00:14:52.800
basic like return dev123 and it
00:14:56.279
automatically exports that and I would
00:14:58.320
also put my story here as well so I
00:15:00.180
would go app and stories dot TSX like it
00:15:03.779
sets It Up by default that it looks for
00:15:05.579
things that have dot stories okay I also
00:15:09.240
have a vs code icon extension that gives
00:15:11.760
me like the storybook icon
00:15:14.279
work so you would import your app in
00:15:16.980
here your component so let me just
00:15:18.600
import it here you need to do an export
00:15:20.639
default title let's just call this app
00:15:23.519
and generally I group my things
00:15:25.139
accordingly so I will just go like
00:15:27.180
components forward slash app in case I
00:15:29.279
have other things in storybook it's also
00:15:31.019
unhappy because I think it wants us to
00:15:33.260
assign this to an object you can't
00:15:36.779
directly export a default object uh yes
00:15:39.899
lent I think it wants you to do that and
00:15:42.540
this is unhappy because file should have
00:15:44.339
at least one story so export and let's
00:15:47.040
just do const basic is it this is and
00:15:49.740
basic just exports the app as is let's
00:15:52.560
get rid of index.css let's get rid of
00:15:55.459
app.tsx over here and this and so we
00:15:58.800
just keep main pull in our own app we go
00:16:01.920
components forward slash app and we get
00:16:04.079
rid of this and I usually just
00:16:06.360
destructure strict mode from here just
00:16:08.820
do it like that it's been up storybook
00:16:10.920
npm run storybook and it should have
00:16:13.380
that only this one single story this
00:16:16.199
basic one follow along with what I'm
00:16:18.180
doing here you can also check out the
00:16:21.060
storybook documentation if you want to
00:16:23.220
see like what all these things do
00:16:24.839
there's lots of videos and stuff I'm not
00:16:26.399
necessarily going to go into that in
00:16:28.260
depth here because I want to show you
00:16:29.760
guys how I would go about building this
00:16:31.740
app if you find storybook confusing and
00:16:33.660
you're like I I don't want to do
00:16:35.399
storybook that's 100 like you can just
00:16:37.320
dive straight into building out the app
00:16:39.360
in react with our storybook and here's a
00:16:41.699
basic version of it and that is all we
00:16:44.040
have so let's start adding some stuff to
00:16:46.440
that I'm going to pull in mui and just
00:16:49.560
copy that and I and I'm also going to
00:16:51.540
pull in material UI icons as well the
00:16:53.940
GLI icons icons material okay so that
00:16:57.300
one over there npm install let us just
00:17:00.660
go in our app here and let's pull in a
00:17:03.180
basic button just to see if it's working
00:17:04.859
so import from material and I'm gonna
00:17:09.540
pull in a button and what I'm also going
00:17:11.459
to do is I'm going to pull in dialed
00:17:14.280
from
00:17:15.439
emotion dialed button which is styled
00:17:18.780
and I just pass button to it and let's
00:17:21.059
just try giving it background red and
00:17:23.640
seeing if that works so let's just get
00:17:25.500
everything set up the style button and
00:17:27.900
let's just in here do the style button
00:17:29.940
it's start storybook there we go another
00:17:32.940
thing I want to pull in as well is Faker
00:17:34.980
JS that's just going to help us like
00:17:37.320
create some fake information to build
00:17:39.059
our UI against to get started and okay
00:17:42.299
so import at fake there we go and we can
00:17:46.740
then extract we need to extract Faker
00:17:50.100
from here because there's some other
00:17:51.480
things as well that you can use some
00:17:53.160
utility things along with it so we're
00:17:55.020
just going to use Faker and let's say
00:17:56.640
animal and give me a type of bear I just
00:17:59.700
want to see if it actually works
00:18:00.900
obviously this is nonsensical if there's
00:18:03.240
no reason you would want to do this I
00:18:05.039
just want to see if all the pieces of
00:18:07.020
all the stuff I'm pulling in works and
00:18:09.299
also remember what I said you know like
00:18:11.039
how do you organize your react app well
00:18:13.020
you start with one file and one is it's
00:18:15.299
getting too big you start splitting
00:18:16.559
stuff in a spectacle bear okay there you
00:18:19.200
go that's apparently a type of beer I
00:18:20.880
want to show you guys something great so
00:18:22.380
like I always have a good laugh at this
00:18:24.000
so if you go Faker and I think it's
00:18:26.100
Commerce product name I think some of
00:18:28.679
these things are ridiculous Sleek bronze
00:18:31.500
computer Oriental plastic bike recycled
00:18:34.860
Fresh Car Sleek concrete chair some of
00:18:38.100
the stuff is amazing so now we're
00:18:39.780
actually going to start building this
00:18:40.980
out so let's actually bring in this
00:18:43.740
typescript stuff that we mapped out over
00:18:46.740
here into this file type movie so let's
00:18:49.980
start with our previews first create
00:18:52.039
mock previews so what I'm going to do is
00:18:55.080
I'm gonna do you're gonna create a new
00:18:57.360
array that e and you're going to fill it
00:18:59.700
with undefined if you remember way way
00:19:02.520
back we spoke about how arrays are
00:19:04.620
actually just objects secretly under the
00:19:06.960
hood and how you can have an array that
00:19:09.720
has a length of 30 but has nothing in it
00:19:12.240
for this reason we need to actually fill
00:19:14.520
it with something that can be like one
00:19:16.559
undefined or whatever after we create
00:19:18.720
the links otherwise it's going to be a
00:19:20.520
length of 30 but there's not going to be
00:19:22.200
nothing in it okay so then we fill all
00:19:23.940
these 30 things with undefined and then
00:19:26.340
we just map over a degree Halo fake
00:19:28.440
things you know let's write it like this
00:19:30.660
for easier readability and what you can
00:19:33.360
also do is a prettier love if I go
00:19:35.340
control save bring everything into like
00:19:37.620
this um times I wanted like this for
00:19:39.960
readability so I would just go pretty uh
00:19:42.360
ignore just tell it like leave this
00:19:44.280
thing alone but I'm still going to get
00:19:46.260
all the other areas or whatever but it's
00:19:47.940
not going to try turn this into a single
00:19:50.280
big line in map I just wrap this in like
00:19:53.880
that so it's returning an object and
00:19:55.679
that object we can say that object needs
00:19:58.260
to be preview actors this is just we can
00:20:00.840
do Faker data type number what is it
00:20:04.140
except minimum and maximum so let's say
00:20:06.120
minimum of one active maximum of 12
00:20:09.179
actors so it creates a number for US
00:20:11.580
between that range we can get it to
00:20:13.860
create a fake UI ID for us so we can do
00:20:16.080
data type uuid I don't know why it says
00:20:18.720
these are deprecated okay they change
00:20:20.640
the API this was also really great about
00:20:22.799
is you can actually mock stuff as
00:20:24.539
deprecated I can actually go you know
00:20:26.760
jstock this isn't even typescript and
00:20:28.860
then whenever I use this it's going to
00:20:31.260
tell me listen with that strikethrough
00:20:33.179
this is deprecated can but you shouldn't
00:20:35.820
use this but this one fake a number int
00:20:38.160
okay so they changed the API at string
00:20:40.860
uuid oh it is actually a number it's not
00:20:43.140
a uui you can base this off the index so
00:20:45.780
let's instead underscore and index and
00:20:48.480
use the index plus one as the IDE Faker
00:20:51.660
has images image yeah pick some photos
00:20:54.419
yeah let's go pick some photos release
00:20:57.179
we can do Faker date uh past I'm
00:21:00.840
assuming like movies have been released
00:21:02.880
in the past we usually one is a one a
00:21:04.620
bit of variation in terms of how long
00:21:06.240
things are so I you generally just do a
00:21:08.700
faker get a Boolean and then you can use
00:21:11.220
a ternary so that it returns one of one
00:21:14.100
of two parts possible type like
00:21:16.580
lorem and words all words and then I
00:21:20.460
have another one that let's go something
00:21:21.900
like very like 11 words so it's it's
00:21:24.059
nice to have a bit of variation in your
00:21:25.799
fake data a release yeah let's just keep
00:21:28.679
it as a string through string first and
00:21:30.900
foremost let's actually just do a
00:21:32.700
unordered list and return all the
00:21:34.919
preview info and let's map over that the
00:21:37.559
structure and return the following
00:21:40.380
actors ID image release and title and
00:21:44.100
for each of these let's return An Li and
00:21:46.799
in that l i let's have another list with
00:21:49.080
the title release l i image source and
00:21:53.940
that image is probably going to be
00:21:55.320
pretty big so let's make it small so I
00:21:57.419
would also just image and I would go
00:21:59.100
styled IMG with Vibram and height
00:22:03.179
biogram because we're mapping we need to
00:22:05.820
set a key here and we can just use the
00:22:08.340
ID as the key let's just do Li actors my
00:22:12.240
storybook should still be running I all
00:22:15.539
right so here it created this based on
00:22:18.059
fake information it's an absolute mess
00:22:19.980
at the moment it's a good place to start
00:22:21.720
this you can also in storybook send it
00:22:23.580
to Small mobile so let's do that what I
00:22:25.740
might possibly even do is you might even
00:22:27.299
like pull this out into its own window I
00:22:29.640
know in material UI there's something
00:22:31.440
called paper another thing we need to do
00:22:34.320
as well I think there's like a CSS
00:22:35.880
Baseline so CSS Baseline just sets all
00:22:38.820
that border box margins on your body all
00:22:41.700
of that stuff for you as you get that
00:22:44.220
with mui let's just also Chuck it in
00:22:46.980
here so I use an empty fragment so I can
00:22:49.440
put it just above that and this just
00:22:51.120
sets all the basic SS for us so you'll
00:22:53.760
see it immediately even if I point that
00:22:55.380
out look at the font over here and then
00:22:57.299
when I do that look at the font over
00:22:58.860
there let's keep this as an unordered
00:23:00.900
list just for semantic reasons so let's
00:23:03.120
just say list styled
00:23:05.520
ul and we obviously just want to remove
00:23:07.140
the padding and we want to also say list
00:23:09.240
style none so we want to keep it for
00:23:11.100
semantic reasons for accessibility and
00:23:13.860
those type of things but but we don't
00:23:15.360
have the dots let us do const card and
00:23:19.559
we're going to use styled and we're
00:23:21.059
going to grab paper from Material UI I
00:23:23.580
think we're gonna have to put some
00:23:24.480
padding in it instead of Li let's do
00:23:26.940
card over there let me just comment this
00:23:28.799
out for now and let's say we want a H2 2
00:23:32.220
in there the H2 is just title you can do
00:23:35.460
this there's also a typography element
00:23:37.440
in material UI that we can use for our
00:23:40.260
text typography okay so let's set the
00:23:42.720
semantics of this a card component as
00:23:46.020
yeah as l i that should turn it into an
00:23:49.440
Li but we might need to type it up yes
00:23:51.780
okay it does but typescript doesn't know
00:23:54.000
about that so what we can do is we can
00:23:56.700
just go and we can add as and just let's
00:24:00.299
also set the background color all right
00:24:02.220
so you have Global we need to import
00:24:04.860
something called Global to set Global
00:24:06.960
style so we want to set the body because
00:24:09.059
obviously this ties are two actual
00:24:11.039
components okay so you can just do it
00:24:12.780
with the react on that it seems we need
00:24:14.940
to pull that from the react specific one
00:24:17.340
so I import from at emotion react oops
00:24:22.559
and so Global and CSS let's create our
00:24:25.919
Global Styles here constant let's just
00:24:28.080
say Global and CSS and what we want is
00:24:31.080
we want the body to has to be background
00:24:33.900
and let's just do something like that
00:24:35.940
for now we pass Global to this and
00:24:39.720
styles equals just that object that we
00:24:43.380
created I'm doing a lot of things here
00:24:45.659
and the goal here is for you guys to
00:24:47.880
show you guys how I would approach it
00:24:49.559
I'm not I don't think we have time for
00:24:51.360
me to go into everything learn more
00:24:53.760
about what I'm doing here with this
00:24:55.559
Global what I'm doing with the CSS
00:24:57.120
Baseline go read the documentation if
00:24:59.820
you don't understand it and you're okay
00:25:02.880
still using it even if you don't
00:25:04.380
understand what it does or how does it
00:25:07.020
more power to you if you're like I don't
00:25:09.240
know what this does I prefer to just do
00:25:11.039
it my own way and not do this way go for
00:25:13.140
it okay I'm just showing you guys that I
00:25:16.260
would use and you can decide whether you
00:25:18.720
want to do it the way I will do it or
00:25:20.400
not and whether you want to read up a
00:25:22.080
bit more about the way I did it okay so
00:25:23.880
this is maybe also but intense yeah
00:25:25.559
that's a bit on our cards as well let's
00:25:28.260
put a bit of margins at the top and the
00:25:30.059
bottom so margin one rim and no margins
00:25:33.539
on the side like I said at the very
00:25:34.620
least to separate these so we have the
00:25:36.779
typography let's see what we can do with
00:25:38.760
typography variant and what are the
00:25:41.220
variants the variants are body button
00:25:43.620
caption H1 H2 I think H2 is a bit
00:25:46.440
intense let's go H3 oh H3 is even worse
00:25:49.020
H4 by uh let's go six how much am I
00:25:54.240
zoomed in here okay I am zoomed in a ton
00:25:56.820
so math Six is fine okay so this is just
00:25:59.520
the styling of it but semantically we
00:26:02.820
probably want it to be an H2 so I think
00:26:05.580
you can go component H2 so then just
00:26:09.360
semantically so we want to keep our code
00:26:11.039
semantic even override it but if we want
00:26:13.320
so let's go to title because I would
00:26:14.760
like that to be a bit tighter so we can
00:26:16.799
do styled and typography really see if
00:26:19.260
it still works yeah that still works I
00:26:20.700
just want to bring in the line height a
00:26:22.200
little bit height and also we need to do
00:26:23.880
as now if you use style you need to do
00:26:26.279
as instead of component uh you just need
00:26:28.740
to tell typescript about it and line
00:26:31.020
height let's just C1 but intense let's
00:26:33.840
go like 1.1 okay these are some long
00:26:36.360
movie names we want an image next to
00:26:38.520
them so title we might need to tell our
00:26:41.340
card to be display Flex just to put some
00:26:45.120
next to one another flex and let's also
00:26:48.179
create something called info puts
00:26:50.279
everything next to the image so that's
00:26:51.900
just a div padding let's just do some
00:26:54.000
padding on the left side of it one rim
00:26:56.340
and we're going to wrap all our info in
00:26:58.740
that align items Center like these
00:27:02.820
titles are a bit intense I don't think
00:27:04.320
they'll actually movies of that long
00:27:05.880
title so let's just bring this in a
00:27:08.400
little bit let's just say two words up
00:27:11.279
to like seven words okay we want the
00:27:14.220
year it was released it's a string and
00:27:16.980
we're gonna have to turn it into a date
00:27:18.720
so that is fine also in did we put it
00:27:22.260
inside info yeah okay there's a problem
00:27:24.419
that's why if so let's put it in info
00:27:26.400
there we go okay so this isn't great we
00:27:28.200
just want to show the year so what we
00:27:30.059
can do is let's take that and I would
00:27:32.520
actually not in the jsx itself I would
00:27:35.039
go you know return and then I just put
00:27:37.320
it outside of the return in the map yes
00:27:39.900
oh okay it needs to be inside I see
00:27:41.880
right there we go nice so yeah yeah and
00:27:44.940
transform that before I put it in my jsx
00:27:47.340
so I would go new date I would take that
00:27:49.799
string turn it into a date release and
00:27:52.740
then just say get full yeah there's the
00:27:55.260
uh probably also want this to be in a
00:27:58.200
more semantic uh d l so DL is a
00:28:01.260
definition list so it's a key in value
00:28:03.179
challenging semantically is a key and
00:28:05.640
here's a value associated with that key
00:28:07.380
so it's almost like representing an
00:28:09.059
object with key and values and then your
00:28:11.400
DT would be the term release DD I think
00:28:15.299
yeah description the actual year with
00:28:18.179
that in a div I think as well so this is
00:28:20.460
all just HTML stuff this isn't react
00:28:22.799
stuff you don't have to write your HTML
00:28:24.659
the semantic if you want I don't know
00:28:26.700
it's up to you to decide if you have a
00:28:29.100
good understanding of HTML the more
00:28:30.539
semantic your HTML is for search engines
00:28:32.820
and accessibility and so forth the
00:28:34.799
better I also want to say you guys did
00:28:36.600
go over HTML very quickly like we're
00:28:39.299
mostly training you guys in JavaScript I
00:28:41.340
just want to like point out like HTML
00:28:42.840
and CSS goes deep um if you guys want to
00:28:45.419
like get more into it there's a lot of
00:28:46.919
Great Courses the one that I would
00:28:49.200
recommend if you have the money is a CSS
00:28:52.860
for JS devs this is phenomenal it's
00:28:56.460
amazing he also has a react course it is
00:28:59.340
it is quite expensive if you can get
00:29:01.380
your hands on it if you can get an
00:29:02.820
employer to pay for it
00:29:04.440
um Josh's stuff in general is just
00:29:06.480
amazing definitely follow him on Twitter
00:29:08.400
check out his blog and and so forth HML
00:29:11.220
CSS goes really deep you might not even
00:29:13.799
know about any of the stuff if you want
00:29:15.900
to get better at writing HTML there's
00:29:17.760
also another great book it's by Hayden
00:29:20.880
Pickering this inclusive components is a
00:29:23.279
phenomenal book There's an actual
00:29:25.020
website for it as well but this is he
00:29:26.760
really goes into HTML and writing
00:29:28.679
semantic HTML and so forth getting on a
00:29:30.720
tangent here but I just want to give you
00:29:31.860
as resources if you want to get into
00:29:33.899
like semantics around forms and so forth
00:29:36.600
so obviously we're just now looking at
00:29:38.220
representing data but like when it comes
00:29:40.140
to forms and inputs and radio buttons
00:29:42.120
and those things there's a really good
00:29:44.100
book called form design patterns by Adam
00:29:46.740
Adam Silver this is a great but yeah I
00:29:49.679
highly recommend it he is a senior
00:29:52.620
product designer at government.uk and
00:29:55.320
effectively they do all the UK
00:29:57.600
governments digital stuff and so