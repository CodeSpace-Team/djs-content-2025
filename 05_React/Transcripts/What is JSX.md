00:00:00.000
would would we then if if we if we had
00:00:03.120
the time and we got around to doing
00:00:04.500
something like that would you go through
00:00:06.480
like react native to so that we could do
00:00:08.580
it into a mobile app kind of way well so
00:00:12.059
no so I think we can just do a web app
00:00:13.980
version of it so first and foremost I
00:00:15.839
think I think there's there's a bit of a
00:00:17.580
problem area here where by actually
00:00:19.920
rebuilding s-coms to push we're probably
00:00:22.320
breaking the the service agreement of
00:00:24.660
the API so sometimes apis have like
00:00:26.939
service agreements where it's like you
00:00:28.859
can't use the Netflix API or the Spotify
00:00:31.439
API to build a competitive version and
00:00:34.500
we can do react native so the reason why
00:00:36.780
I'm not covering react native apart from
00:00:38.940
this they're not being enough time is
00:00:41.160
like also it's it's a bit harder because
00:00:43.260
you need to spend a bit of money to
00:00:45.120
actually deploy native apps uh for
00:00:47.460
example on the iOS store I think it's
00:00:49.440
like a thousand Grand a month not a
00:00:51.420
month a year but which is still a
00:00:53.219
non-zero amount thousand round a year
00:00:55.260
just to be able to actually deploy to
00:00:58.140
the store so a thousand Rand a year just
00:00:59.940
to have an account and then there's
00:01:01.620
loads of other things it's very hard to
00:01:03.059
test and you need to submit it and it
00:01:04.860
needs to be reviewed I might maybe show
00:01:06.900
you guys a bit of react native show you
00:01:08.880
like how you can if you want to explore
00:01:10.560
that further but it's just like it's
00:01:12.180
very hard to kind of teach that because
00:01:14.340
once again you need to submit something
00:01:15.900
and then wait like a week for them to
00:01:17.580
review it and so forth whereas with the
00:01:19.439
web you just push to GitHub and it
00:01:21.720
updates automatically we can do a little
00:01:23.460
web app if we have time I was just
00:01:25.500
curious yeah I mean that's that's a
00:01:27.240
great idea actually it would be very
00:01:28.560
cool to like build our own version of it
00:01:30.540
just as a testing so you can to use apis
00:01:32.820
yeah yes and I might even show you guys
00:01:35.520
some service worker stuff I don't know
00:01:37.020
if anyone's heard about Progressive web
00:01:38.579
apps or service workers or those things
00:01:40.500
what you can do is then you can actually
00:01:42.479
install it as an app that is actually a
00:01:44.460
page let me show you an example so let
00:01:46.560
me quickly spin up Android studio and
00:01:48.600
let me quickly show this what's really
00:01:50.820
nice about Veet is Veet has a pwa plugin
00:01:53.880
pwa plug-in uh beat that you can
00:01:56.820
literally just plug into into your build
00:01:59.159
process and it turns is your your your
00:02:01.020
your react your felt your view whatever
00:02:04.200
uh project into a pwa it used to be a
00:02:07.740
lot harder to set up is this the one
00:02:09.720
that puts like a wrapper around your
00:02:11.099
site and then you're able to deploy
00:02:12.420
basically no so well so you're thinking
00:02:15.239
about something like Cordova or the new
00:02:18.720
the new versions kind of capacitor which
00:02:21.120
is kind of replaced Cordova no so it's
00:02:24.000
actually something that's built into the
00:02:25.620
specification itself so it actually
00:02:28.020
allows your your thing that you deploy
00:02:30.900
to interface with the operating system
00:02:33.000
itself without a play store or whatever
00:02:35.160
so so that's the caveat you can deploy
00:02:37.500
to some app stores I know like the
00:02:39.660
Microsoft one takes it I think in
00:02:41.819
Android you can I think uh Twitter Lite
00:02:45.480
Uber light all those like Facebook Lite
00:02:47.819
those are all pwas that have actually
00:02:49.860
just been deployed to the App Store so
00:02:52.920
you can like without actually even
00:02:54.660
needing to learn how to write native
00:02:57.000
apps you can take HTML CSS and
00:02:58.920
JavaScript and deploy it as an I might
00:03:00.840
touch on that as well but you know like
00:03:02.280
I I don't want to go too far beyond the
00:03:05.700
scope of what we want to cover but it is
00:03:07.680
it's important to just I think know that
00:03:10.260
those options exist and I will show you
00:03:12.599
guys how to do a pwa let's just think
00:03:15.420
it's so easy with feet excuse my
00:03:17.280
ignorance what does pwa mean Progressive
00:03:20.220
web apps so effectively you have
00:03:23.280
websites and you have apps the the the
00:03:25.860
the value of a website is that a website
00:03:29.340
is accessible from anything that has a
00:03:31.739
browser so if you have a fridge if you
00:03:33.900
have a Kindle if you have whatever and
00:03:35.940
it can run a browser you can look at a
00:03:38.040
website then you have apps which you
00:03:40.200
know have a lot more functionality like
00:03:41.879
like push notifications being able to
00:03:44.340
use them offline all of that stuff but
00:03:46.379
at the cost of the ubiquity of the reach
00:03:49.080
of the the web because now you need to
00:03:51.060
write it in flutter or Swift or Java or
00:03:54.540
whatever to actually integrate with the
00:03:56.099
operating system so pwas are a way that
00:03:59.340
looks at bridging that allowing you to
00:04:02.340
run actual HTML series and JavaScript as
00:04:05.459
actual apps um so the progressive web
00:04:07.980
apps so it's Progressive in other words
00:04:10.200
it steps up it builds forward so the
00:04:13.140
tally app that I'm going to re-bull or
00:04:15.060
you guys doesn't react
00:04:16.798
um so I the tallyapp
00:04:18.738
example.netified.app so if I go to that
00:04:21.478
it should prompt me at your home screen
00:04:24.479
if I click there I say install yes it's
00:04:27.000
adding it there you go so it should
00:04:29.520
install it as if it's an app I can even
00:04:31.860
show you like even on my operating
00:04:33.540
system so if I go for example the
00:04:35.639
netlify you'll see there's a little
00:04:37.320
prompt there that says installed at the
00:04:39.180
top and I can say install actually
00:04:40.800
running here at the bottom I can pin it
00:04:43.320
as actual software on its own so that I
00:04:45.600
can run it and it opens in its own
00:04:47.520
window that's really cool I've seen the
00:04:50.280
same thing with my girlfriend on her Mac
00:04:52.020
for her her work they've got she's got
00:04:54.000
ESP as an app on on like yeah I'm like
00:04:56.880
okay cool yeah yeah 100 so
00:05:01.020
um you can even search for it so I've
00:05:02.520
installed it now so I can just search
00:05:04.080
for you know tally and there it is and
00:05:06.060
it says app and I can you know if I go
00:05:08.280
in my program it should even appear here
00:05:10.979
as something that I can uninstall so you
00:05:14.400
can use push notification applications
00:05:15.780
you can use loads of cool other things
00:05:17.639
and you'll see it's actually running in
00:05:19.500
its own video if I do alt tab it
00:05:21.479
actually appears here as its own
00:05:23.280
software I don't know if you guys can
00:05:24.600
see my old tab yeah yeah it's it's
00:05:27.600
amazing it's it's because like I haven't
00:05:29.880
used this emulation in a while so I
00:05:32.580
think it's doing like software updates
00:05:34.139
yeah there we go fun times okay if I run
00:05:37.800
it kind of now opens it as actual
00:05:39.419
software and you can use it offline and
00:05:41.460
everything yeah you'll see it actually
00:05:42.900
runs separately as as actual app itself
00:05:46.320
um there's just one thing you need to do
00:05:47.940
in order to get rid of that little
00:05:50.699
Chrome thing in the icon but yeah so so
00:05:53.160
we can cover all of that stuff um
00:05:55.080
there's so much we can cover and I think
00:05:57.000
this is the value of learning the
00:05:58.740
foundations and the and the fundamental
00:06:00.840
principles first that now we can have a
00:06:03.060
discussion around these things and what
00:06:04.860
they actually do without every time
00:06:07.320
treating it as oh here's a new thing we
00:06:10.080
need to learn from scratch and oh
00:06:11.759
because we we understand the underlying
00:06:13.740
principles and we can just say okay this
00:06:15.000
is how it does reactivity this is how it
00:06:16.979
does encapsulation this is how it does
00:06:18.780
components you know and so forth and so
00:06:20.759
forth and we can just take our existing
00:06:22.560
understanding of what it does and just
00:06:25.020
see how these tools do it in different
00:06:26.880
ways what I would like to do in the
00:06:29.100
remainder of the session is get you guys
00:06:31.199
started on a little bit of react what I
00:06:33.600
want you guys to do as exercises along
00:06:35.699
with these sessions there is I don't
00:06:37.979
know if anyone knows about scrimba so it
00:06:40.139
scrimba's a bit like free code camp like
00:06:43.080
I would have under any other
00:06:44.340
circumstances have you guys done the
00:06:47.039
react exercises on free code camp and
00:06:50.639
you might be like what are they react
00:06:52.500
exercises on free program uh don't get
00:06:54.780
too excited they're really not that
00:06:56.340
great they're very outdated this is one
00:06:58.919
of the areas where I actually wouldn't
00:07:01.740
recommend someone to use free code camp
00:07:03.780
and it's also part of just kind of
00:07:05.819
teaching you the principle of
00:07:07.860
development front-end libraries so it
00:07:09.900
has like bird strap it even has jQuery
00:07:12.120
you know SAS react Redux you know and
00:07:15.600
you can check this out if you want but
00:07:17.639
honestly this is really due for a for a
00:07:20.580
rewrite and a refactor in terms of the
00:07:22.800
free card Camp team so I wouldn't like
00:07:25.319
this also uses the old component API as
00:07:28.139
well the recommended way to use react
00:07:30.360
nowadays is through hooks which this
00:07:32.940
doesn't even cover so yeah I I would and
00:07:35.580
it's also you'll see it's not very long
00:07:37.199
at three lessons or something but I want
00:07:39.419
you guys to work through this scrimba
00:07:42.300
one it's very similar to free code camp
00:07:45.060
and it's really great I've had previous
00:07:47.520
students work through it as well and
00:07:49.500
then it takes you through like react and
00:07:51.479
so forth you know like the you know what
00:07:53.699
is react you know and some practice
00:07:55.440
projects what is jsx how do you deploy a
00:07:58.500
reacting or netlify create root API
00:08:01.940
opponents custom components it even has
00:08:05.580
you know like how to set up react with
00:08:07.440
Veet as well so I kind of consider this
00:08:09.900
the best one at the moment in terms of
00:08:11.520
learning react so I want you guys to
00:08:13.919
work through these alongside the actual
00:08:16.979
lesson because as mentioned I what I
00:08:18.840
want us to do is to actually learn react
00:08:20.879
but I will touch on some of the other
00:08:22.319
Frameworks just on the side as well so
00:08:24.599
it's called what's the name of the
00:08:25.979
course exactly and it's just learn react
00:08:28.319
yeah just search for scrumba
00:08:30.380
[Music]
00:08:31.700
s-c-r-i-m-b-a I just react yeah
00:08:35.120
yeah there's a learner act one if you
00:08:37.679
even go on learn react on YouTube you
00:08:41.339
should get the free code Camp one so
00:08:43.020
this here uh this is actually ironically
00:08:46.800
enough this is actually the scrum course
00:08:49.140
which I don't know how that works so
00:08:51.000
they're not even using the actual
00:08:52.440
pre-code Camp one um and it's actually
00:08:54.720
the you'll see here's the link but so
00:08:56.760
that is how I would learn react in 2023
00:08:59.820
so I want you guys to work through that
00:09:01.620
on the side but then I will obviously
00:09:03.600
contextualize some of it for you a bit
00:09:05.880
more in terms of what those things are
00:09:07.620
if you have any questions while you're
00:09:09.360
working through it or you get stuck on
00:09:10.740
anything yeah please please do ask me
00:09:13.620
um we can chat about it here see the
00:09:15.000
guys let's say that stuff here on figma
00:09:17.279
as well they also have JavaScript stuff
00:09:19.140
as as well but I think the JavaScript
00:09:21.120
stuff is with the free codecamp the
00:09:23.580
JavaScript stuff is better though build
00:09:25.440
a meme generator yes please
00:09:27.620
like this is literally the Pinnacle of
00:09:30.779
all this evolution of JavaScript
00:09:32.880
Frameworks verged to give us like the
00:09:35.880
ultimate achievement of human
00:09:37.399
civilization building a meme generator
00:09:40.200
in a JavaScript framework you're kidding
00:09:42.420
but there's actually a lot of a lot of
00:09:45.540
the tutorials are like you know a dad
00:09:47.940
joke API or or whatever there's a ton of
00:09:51.120
them it's like I can has that joke and
00:09:54.300
you can call the API and every time you
00:09:56.940
call the API it gives you a new joke it
00:10:00.300
even has a it even has a graphql version
00:10:02.519
yeah so you can build it you can build a
00:10:04.920
dad joke app displays random dad jokes
00:10:07.140
that is so cool I like this yeah so like
00:10:09.480
I'll definitely show you guys this is
00:10:10.920
one of those things like once you know
00:10:12.720
how to use Frameworks you know how to
00:10:14.760
use Frameworks with actual remote apis
00:10:17.580
via Fetch and so forth you can build
00:10:19.620
almost anything you want you know
00:10:21.120
literally you can rebuild like escom to
00:10:23.399
push or you can rebuild like you can
00:10:25.260
build any app a weather app whatever so
00:10:27.959
it's really great for fleshing out your
00:10:29.820
portfolio and building really cool stuff
00:10:31.440
in your portfolio I'm happy to cover any
00:10:33.899
of those show like because the
00:10:35.580
principles are the same so you know if
00:10:37.140
you guys want to build like a weather
00:10:38.339
app or whatever we can do that I can use
00:10:40.380
that as a means too I want to start
00:10:42.120
digging into a bit of react but I'm not
00:10:45.480
going to start with any of kind of
00:10:48.959
setting up Veet and all of that I'm just
00:10:51.240
going to start with a very basic example
00:10:53.459
in codepen and and the reason being I
00:10:55.560
can actually then share that example
00:10:57.060
with you guys whereas you know if it's
00:10:59.279
on my local machine obviously I can't do
00:11:01.500
that let's look at the react
00:11:03.560
documentation uh I actually haven't like
00:11:06.959
spent much time with the new
00:11:08.760
documentation I just gave it a quick
00:11:10.800
glance because obviously like it's been
00:11:13.200
a while since I learned to react what
00:11:15.060
they do here is they just take you
00:11:17.100
through kind of how you like what is
00:11:19.200
react what is jsx what are all these
00:11:21.839
things and so maybe one of the first
00:11:23.459
things I want to do is I want to show
00:11:24.959
you guys what JS X is jsx is if you
00:11:28.500
remember in lit so we had that Lit HTML
00:11:32.399
which was effectively a function that we
00:11:35.339
would call a string template on okay so
00:11:37.920
we had you know like HTML and then we
00:11:41.339
would you know go like gov One Two Three
00:11:43.260
or whatever but so this is all just a
00:11:45.060
string and then this HTML for like
00:11:47.820
function turns it into like an object
00:11:49.680
with kind of like all the lead specific
00:11:51.720
stuff and then you know look render
00:11:53.820
consumes that object and checks like you
00:11:57.060
know like the correct Dom and so forth
00:11:58.980
and What needs to change jsx is a bit
00:12:01.440
different in order to kind of explain
00:12:03.120
jsx what I'm going to do I did mention
00:12:05.459
this in the videos super so there's
00:12:07.140
something called HTM uh bubbled Jason
00:12:10.260
Miller uh I actually have a couple of
00:12:12.360
pull requests to HTM itself except it's
00:12:15.660
really cool it's kind of like jsx in the
00:12:17.700
browser and we just pull in the CDN so I
00:12:20.700
can actually show you guys in here okay
00:12:23.700
so there we go so it works very similar
00:12:26.880
to to let HTML the only difference is
00:12:32.100
that Lit HTML assumes I guess it assumes
00:12:36.180
a page it assumes like HTML whereas HDM
00:12:40.320
doesn't so HTM is a lot closer to jsx so
00:12:44.040
jsx actually stands for JavaScript XML I
00:12:49.079
think but there's actually been
00:12:50.579
discussion to actually maybe bring jsx
00:12:54.180
natively into the browser weirdly enough
00:12:56.940
one of the biggest supporters of this is
00:12:59.220
actually a like senior project leads at
00:13:02.160
Google actually ironically enough and
00:13:04.260
you might think like oh that's weird
00:13:05.700
because jsx is a reacting jsx is
00:13:09.060
actually not a reacting and I think we
00:13:11.220
need to be clear about this because if
00:13:13.200
you think about jsx as reacts templating
00:13:16.980
you are going to be confused a lot of
00:13:19.620
people think about it as templating so
00:13:21.779
you know oh it's a way to write HTML and
00:13:24.420
react it's not what jss actually is jsx
00:13:27.420
actually Builds on top of a lot of other
00:13:29.399
things you know the first being
00:13:31.019
hyperscript and so forth and what these
00:13:33.959
do is they actually they actually allow
00:13:37.680
us to nest of functions in XML so what
00:13:41.579
XML is is XML is very similar to HTML
00:13:46.560
okay so XML is just kind of a more
00:13:50.399
generic version of HTML so it's it's
00:13:53.100
kind of the whole closing brackets and
00:13:55.260
stuff but for anything you know wouldn't
00:13:58.200
XML be in like your typical website like
00:14:00.360
your site map is your sitemap dot
00:14:02.220
exactly yes okay and 100 and actually
00:14:05.639
XML before Json used to be the way that
00:14:10.260
you would get stuff from endpoints so
00:14:12.480
here's an example of XML so but like XML
00:14:15.360
is an actual way for us to represent any
00:14:18.660
type of nested information you can think
00:14:21.000
about you know sitemap is nestable there
00:14:23.700
are pages that are children of other
00:14:25.740
pages and those pages so any type of
00:14:28.079
nested information for all intents and
00:14:30.300
purposes I can actually Express so
00:14:33.959
family in that family is you know or
00:14:38.160
let's say parents okay and in that is
00:14:41.100
you know sculpt and my wife section
00:14:43.440
there we go uh children and my daughters
00:14:46.800
I'm not going to write the second one
00:14:48.480
because we haven't solved the name yet
00:14:50.100
she's only due in two months so oh I was
00:14:52.980
gonna fall for that one like you guys
00:14:54.420
weren't going to be the first people to
00:14:55.860
learn the name my parents would have
00:14:57.360
been mortified if they learned that you
00:14:59.220
guys knew the name before them and then
00:15:01.260
you know like inside skulk I can have
00:15:03.600
you know like Hobbies I only have one
00:15:06.420
hobby obviously which is Javascript
00:15:08.760
turns out XML is actually a really great
00:15:11.820
way to express nestable functions as
00:15:14.760
well so so this is where hyperscript HTM
00:15:18.600
jsx all those things come in so plot
00:15:21.360
twist all that jsx does and you actually
00:15:24.660
find jsx and a ton of stuff so there's
00:15:26.579
also like stencil uh JS which I think I
00:15:29.220
touched on super briefly so stencil also
00:15:32.100
uses jsx you can use jsx in view you can
00:15:34.860
use it in angular
00:15:36.540
um in solid JS jsx is all over the place
00:15:39.660
you know so it's not a react specific
00:15:41.639
thing a lot of people write actually
00:15:43.440
their like view with jsx as well so what
00:15:46.680
jsx is is effectively it's a way to bind
00:15:50.399
like to a function call to a nested
00:15:53.760
structure so let me show that to you
00:15:55.380
guys so HTM bind so call this like
00:15:58.800
process or whatever you know uh okay
00:16:01.560
okay okay never mind I imported the
00:16:03.720
wrong thing didn't read the
00:16:05.040
documentation there you go sure that
00:16:06.600
happens so much where I'm just like if
00:16:08.220
that if you do that don't feel guilty
00:16:10.079
everyone does this you might feel like
00:16:11.940
you're the only person who doesn't
00:16:13.139
actually read documentation everyone is
00:16:15.240
like that seems like what I want I'll
00:16:18.120
just copy that without actually reading
00:16:19.620
what it is and paste and if it doesn't
00:16:21.180
work you just copy something else okay
00:16:23.180
so let me just check if this works now
00:16:26.339
uh console ah there we go all right so
00:16:29.040
what we do is then we actually bind it
00:16:31.260
to a function so let's just call this do
00:16:34.199
thing and we bind it to let's write our
00:16:37.019
own custom function here logger and all
00:16:39.779
that that does it just takes all the
00:16:41.459
arguments and it console logs them and
00:16:44.279
so we find that to HDM and so now what
00:16:48.839
we can do is if we now Express XML
00:16:53.160
information it's going to treat that
00:16:55.500
it's going to parse it through this
00:16:57.420
treating all each single nested level as
00:17:00.480
a function call let's see what it does
00:17:02.160
with this uh two thing yeah hey check
00:17:04.919
this out all right so actually I I so I
00:17:07.500
can do anything with it um it logs the
00:17:09.720
name to me and the children and so forth
00:17:11.640
so it actually on every level it
00:17:14.699
actually treats it as a function so what
00:17:17.760
it effectively does it's a different way
00:17:19.859
of expressing the following you know as
00:17:22.260
if these were functions you know so
00:17:23.939
family parents uh skulk Hobbies
00:17:27.540
JavaScript so this might seem very
00:17:30.720
strange and theoretical and whatever and
00:17:34.020
that's okay as well but like I just want
00:17:36.720
you to understand that jsx isn't a
00:17:40.020
templating language it doesn't take a
00:17:42.240
string and convert it into something jsx
00:17:44.940
is a way to express function calls
00:17:47.100
because if you understand that that's
00:17:49.679
going to level up your kind of react
00:17:51.720
game like so much effectively this is
00:17:55.260
what it does so it turns out if we have
00:17:58.380
a function that is create element and we
00:18:01.799
bind it to this it's going to create
00:18:04.260
these as elements for us okay so we can
00:18:07.500
effectively talk very Loosely what react
00:18:09.780
is based on you know so in the same way
00:18:11.340
that we can you know do document create
00:18:13.860
element or whatever and bind that to the
00:18:16.980
structure we can get those X to actually
00:18:19.380
compile HTML for us to Dom nodes we're
00:18:23.160
using react create element which creates
00:18:25.380
a virtual version of it you know like in
00:18:27.960
an actual Dom you would have you know
00:18:29.460
like tag you know H1 children whatever
00:18:32.100
it creates a virtual version for us that
00:18:34.980
we can store in memory let's just say
00:18:37.260
vdom very similar to the lit HTML stuff
00:18:40.559
that we did so we created a virtual
00:18:42.299
version of it and then anytime we can
00:18:44.340
just you know vdom1 compare it against
00:18:46.860
you know another version and by that
00:18:49.620
react can determine what to actually
00:18:51.720
update and that is the Crux of it but I
00:18:53.880
think it's important to understand that
00:18:55.559
the primary difference between jsx and a
00:18:58.980
templating language like HTML like the
00:19:01.260
lit HTML is that this actually takes
00:19:04.740
this and it you know does regex on it
00:19:07.200
it's an actual string and it goes over
00:19:09.780
the string and looks for things and so
00:19:11.700
forth what reactors it actually this is
00:19:14.580
actually function calls you know so for
00:19:16.740
all intents and purposes you should be
00:19:18.120
able to write something like this is not
00:19:21.299
valid jsx but you should be able you
00:19:23.640
know to write something like this but
00:19:25.860
what we do is we bind it to the the
00:19:29.039
actual create virtual Doms that creates
00:19:31.260
the spiritual Dom structures for us okay
00:19:33.299
so the reason why that's important
00:19:36.960
allows us to actually write loads of
00:19:39.179
other things declaratively in react
00:19:41.700
which is not part of HTML so in jsx you
00:19:44.640
can also do things like there is you
00:19:47.160
know react helmet which allows you to if
00:19:50.760
you want to set the title update the
00:19:53.039
title in your head on a specific page or
00:19:55.679
whatever and you can do that you can do
00:19:58.200
things like eternity so you can go or
00:20:01.260
you can go for example you know if
00:20:03.480
logged in then whatever whatever because
00:20:05.940
this is just a function call this means
00:20:08.100
that if this is false then nothing
00:20:10.200
happens if this is true then it
00:20:12.780
obviously goes to the next one and it
00:20:14.520
actually runs this as if it's a function
00:20:16.380
okay and this is one of the benefits of
00:20:18.780
react is that you get what's called lazy
00:20:21.120
evaluation because in react these things
00:20:24.600
are function calls in something like lit
00:20:27.000
all of this gets passed as actual string
00:20:29.580
and then it runs look goes over that
00:20:31.740
string looks for attributes looks for
00:20:33.240
whatever because
00:20:36.230
[Music]
00:20:38.940
runs react doesn't even know about it
00:20:41.460
because the conditions that trigger that
00:20:43.320
those functions quote unquote to be
00:20:45.059
called never actually runs so like this
00:20:47.100
allows you to do really really cool
00:20:48.539
stuff for you and then we'll get to some
00:20:50.460
of that later on but let's get to the
00:20:52.320
basics first okay one thing though jsx
00:20:55.200
isn't natively supported in browsers
00:20:57.480
okay there is some discussions about
00:20:59.520
perhaps including it in browsers at some
00:21:01.500
point for now you need something like
00:21:03.720
Babel to transform it into actual real
00:21:06.720
functions so let's say Babel jsx let me
00:21:09.480
just see if you can actually so if we
00:21:12.059
sets up all the Babel stuff for us for
00:21:14.220
us by default back in the day
00:21:16.860
um you had to do a lot of this manually
00:21:18.480
that's one of those skills that I
00:21:20.160
learned that is now completely
00:21:21.780
irrelevant because it's so easy to do
00:21:23.460
nowadays that and CSS floats you know it
00:21:26.039
took me like two years to learn it and
00:21:27.780
now it's useless okay so if I set it to
00:21:30.360
react it should include jsx by default
00:21:33.120
and we just see const let's test uh
00:21:36.419
let's do return the so once again keep
00:21:39.539
in mind this is jsx so this is actually
00:21:42.240
this is as if I'm calling a functions
00:21:45.240
inside one another
00:21:47.039
um and let's just do span and inside
00:21:50.100
that span like one two three or whatever
00:21:52.200
okay cool so you'll see here actually
00:21:54.679
turns it for us into let's do a bit
00:21:57.900
deeper let's go like on ordered this you
00:21:59.940
wouldn't do this type of thing but just
00:22:01.440
to show you it converts it for us into
00:22:04.080
like actual function calls cool so these
00:22:06.360
are just nested functions you can
00:22:08.460
actually write react like this you know
00:22:10.679
so I can go you know react create
00:22:12.900
element
00:22:13.740
what do I want to create I want to
00:22:15.600
create uh H1 what are the attributes on
00:22:18.720
it nothing what children does it have
00:22:20.640
and sometimes I actually teach students
00:22:22.860
this way of writing react first so they
00:22:25.440
can get an understanding you know and
00:22:27.120
they say class name you know test or
00:22:29.640
whatever you can actually write your
00:22:31.679
your actual react like this without jsx
00:22:34.260
there's actually some and so you might
00:22:36.960
hear people talking about you know react
00:22:40.320
as a library not a framework that is
00:22:42.780
true although I I don't know I just call
00:22:45.720
it a framework because people know what
00:22:48.120
I'm talking about but effectively
00:22:50.700
just the library because you and just
00:22:53.460
pull and react without like any doing
00:22:55.799
any node build steps or whatever I can
00:22:58.679
literally just write my react like this
00:23:00.419
if I pull in the the react
00:23:03.240
um actual from the CDN so the only part
00:23:05.580
that needs to happen in the Bold step is
00:23:07.860
like jsx so it's obviously a lot easier
00:23:11.340
to just write this actually composing
00:23:14.100
like react create element functions like
00:23:16.440
this it might seem to be like okay skulk
00:23:18.720
why are we going into all this Theory
00:23:20.580
all of this stuff I just want to know
00:23:22.020
how to create an app but I think the key
00:23:23.820
yes the fact that I'm able to explain
00:23:26.039
this to you is amazing like this shows
00:23:29.220
how close react is to the metal I I
00:23:32.100
can't explain to you how view works
00:23:33.960
because there's so much black magic that
00:23:36.360
happens from the bit of view that you
00:23:38.760
write to how it shows up in the browser
00:23:40.500
the same with angular all those things
00:23:42.000
react is so tiny of an abstraction that
00:23:45.600
like we've basically covered it you know
00:23:47.700
there are other things like in terms of
00:23:50.880
batching like State updates and
00:23:53.159
performance related things in terms of
00:23:54.960
event listeners and so forth but in
00:23:56.820
terms of the actual rendering this is it
00:23:58.559
this is react from top to bottom what
00:24:01.260
you're writing this is what happens with
00:24:02.940
that this is what you're writing this is
00:24:04.799
what it turns into so read includes
00:24:06.840
Babble it just transforms CSX that is
00:24:09.659
the extent of the framework
00:24:11.760
quote-unquote part of react the race is
00:24:14.340
just a JavaScript object that has
00:24:16.020
methods on it with that out of the way
00:24:18.000
let us actually pull and react and you
00:24:21.539
know like use it here um so I'm gonna
00:24:23.580
pull in the CDN as usual recommend
00:24:26.580
intended to not use cdn's performance
00:24:30.059
wise they're not that great I actually
00:24:31.919
don't know if the new documentation even
00:24:34.620
provides you with the means to if they
00:24:37.440
just completely removed it hectic so no
00:24:40.140
more CDN yeah because generally it's
00:24:42.179
really bad like you don't wanna because
00:24:44.400
you're pulling in a ton of stuff that
00:24:46.380
you don't want like with you and them
00:24:48.240
they also have like it's it's gen it's
00:24:50.220
just for like your development purpose
00:24:52.559
your testing phase I guess so if you
00:24:54.419
want to quickly test something without
00:24:55.919
having to do the whole but so it did
00:24:58.440
have it like I maybe I just don't know
00:25:00.600
the new documentation that well you
00:25:02.820
can't still search for CDN and react see
00:25:05.340
the old documentation it still has it
00:25:08.159
um so you can just Chuck pull that in
00:25:09.960
but so let's just put it here in our
00:25:12.059
HTML yeah like I don't think the new
00:25:14.280
documentation even like has a way for
00:25:16.860
you to do it okay let's just quickly
00:25:18.600
cancel log if uh react is actually there
00:25:21.740
I think I'm getting some Dwayne feedback
00:25:24.059
again let's have a look yes and this is
00:25:27.299
the amazing thing about react sorry like
00:25:29.700
I'm gonna I'm getting I think I'm gonna
00:25:32.039
get very excited about Frameworks I'm
00:25:33.720
very like excitable when it comes to
00:25:35.580
these things because I think I've been
00:25:37.020
doing JavaScript so long I know what
00:25:39.419
it's like writing JavaScript with jQuery
00:25:42.000
or even before jQuery like I know how it
00:25:45.779
was writing JavaScript before all of
00:25:47.700
this like this is oh you guys don't
00:25:49.140
understand like this is amazing you know
00:25:51.120
this is like almost I can imagine like
00:25:52.740
my grandma or whatever who grew up with
00:25:54.900
without cause and then like at some
00:25:57.179
point like the family got a car and it's
00:25:59.460
like you don't understand how amazing it
00:26:01.260
is to have a car
00:26:02.580
um or a smartphones you know I grew up
00:26:04.260
without smartphones all right let me not
00:26:06.179
uh give away my age cool but like this
00:26:08.640
is the react API this is what's so
00:26:10.440
amazing about react keep in mind free
00:26:12.539
act has been around for close to 20
00:26:14.820
years now this is the API I can't like
00:26:18.120
like there's a lot to be said about
00:26:19.860
things that are not that great about
00:26:21.480
react but the fact that this is the
00:26:23.820
extent of the react API after 20 years
00:26:27.419
is amazing like this is literally this
00:26:30.600
little API here is what powers the
00:26:32.700
majority of the web the Netflix Facebook
00:26:34.919
sure who's some other big like react
00:26:37.559
players uh Uber a B and B you know like
00:26:40.440
this little API here I also like that
00:26:42.900
there's a property in that called secret
00:26:44.460
internals do not use or you will be
00:26:46.799
fired that's the best property name ever
00:26:48.960
this is the thing about react and so I I
00:26:52.140
did mention we spoke about functional
00:26:54.059
programming one of the things about
00:26:55.980
functional programming is it's actually
00:26:58.320
very expressive and concise and reactive
00:27:01.260
property of all the Frameworks that
00:27:03.120
we're going to cover the one that leans
00:27:04.380
the most into functional programming
00:27:06.059
which means even if the react API itself
00:27:09.240
is super expressive
00:27:11.340
um like it's a super small API compared
00:27:13.500
to like let's look at for example The
00:27:15.000
View API you know and this isn't the
00:27:17.159
slam on view it's just like view has
00:27:18.779
different concerns you know look at all
00:27:21.120
these methods you know and this is just
00:27:23.039
like the common ones this isn't even if
00:27:25.320
you're you like like other edge cases
00:27:27.539
you know so this is just the ones that
00:27:29.460
are document you know that kind of
00:27:31.559
exposes to you this is like even
00:27:34.080
internally the extent of react all the
00:27:36.659
apis all the methods everything but
00:27:38.760
obviously there's a ton here that you
00:27:40.080
never use you know you never use
00:27:41.760
children you never use component you use
00:27:43.860
fragment you never use profiler you
00:27:45.720
never use pure so you probably only use
00:27:47.880
like eight or ten of these Okay and like
00:27:50.580
that is so amazing that 20 years down
00:27:52.679
the line we are what unlike react 18 now
00:27:55.980
I think um and it's still almost the
00:27:58.320
exact same API Justin you mentioned you
00:28:00.240
know kind of the switch from view two to
00:28:02.100
view three and it's like almost like a
00:28:03.840
completely different framework and it
00:28:05.760
speaks to react and the architecture of
00:28:09.419
react that we've never had like the
00:28:11.460
biggest is hooks but like hooks never
00:28:13.740
broke anything it just gave us a new way
00:28:15.779
to do something I cannot express you
00:28:18.720
guys how well of an API like in terms of
00:28:21.299
when we talk about abstraction and all
00:28:22.740
those things how great reactors it's
00:28:24.779
some of the smartest people in the world
00:28:26.580
that are behind us okay so create
00:28:29.580
element so this is effectively all that
00:28:31.799
jsx wraps it's a it's a method that
00:28:34.559
takes the type takes props and children
00:28:36.659
that's it this is all that jsx does it
00:28:39.240
just binds to create element