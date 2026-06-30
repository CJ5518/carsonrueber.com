---
layout: default
---
# Outbreak Simulator

<img
src="https://polymorphiced.uidaho.edu/img/Flights.png"
alt="An image from Outbreak Simulator showing flight paths"
title="These lines show an infection spreading through air travel">

Outbreak Simulator was a project I worked on for basically all of my tenure at [Polymorphic Games](https://professorpolymorphic.github.io/PolymorphicWeb/). 

Their older website is [here](https://polymorphicgames.com)

Their website for this project specifically is [here](https://polymorphiced.uidaho.edu/index.html), made by [Kristen Martinet](https://kmartinet.github.io/index.html).

For a quick video overview of the history of Outbreak Simulator, click [here](https://www.youtube.com/watch?v=nbDYYguRZtE).

---

You can trawl through the two of those three that contain info on the project if you'd like, but here I'll give a brief history.

I started work on Outbreak Simulator in the summer of 2021, a couple weeks after I was hired at Polymorphic Games. I had never used the Unity game engine before, so the night after I was hired I quickly made a crappy version of snake in it. Then for the first couple of weeks I was given the other project that Polymorphic was working on at the time, which I legitimately cannot remember the name of. Like a lot of our projects, both of these would not see a true release. For the other one, I think they just lost interest in the idea, for Outbreak Simulator, well, we're getting there.

For the summer of 2021 I went back home, the University of Idaho is in Moscow, Idaho, and my parents lived in Coeur D Alene, Idaho and seeing as how I was 17 years old living in the dorms at the time (which made getting hired a real pain, I had to deal with a bunch of extra forms because I was a minor) I went back home for the summer. At this time I was sleeping in a treehouse.

<img
src="/images/treehouse.webp"
alt="A photo of a treehouse"
title="I miss living in this thing sometimes, mainly being able to pee off the deck. There's really nothing like peeing outside.">

And this is where I had my computer. I was closer to our rich neighbor's house (think richer, whatever number of houses you think they own, double it) than my parent's so I used the neighbor's internet (it was better anyway, they were rich). The only thing it didn't have was running water or AC. So when [the heatwave hit and it was getting to 100 degrees](https://www.krem.com/article/sports/ironman/coeur-dalene-ironman-athletes-battle-high-temperatures-during-1406-mile-race/293-b38a463e-1e8f-41c3-8a7d-8e44242407ad) I was just in the treehouse, developing Outbreak Simulator (then codenamed ZomSim), sweating buckets.

The very first version of Outbreak Simulator wasn't actually made by me, it was made by Landon, the [Studio Guy](https://www.youtube.com/watch?v=gzmpo02wxSY), who was the only non-student and non-professor to work there. Here's what he had whipped up:

<img
src="/images/OutbreakSimulator/landonsfirstversion.png"
alt="A photo of a map of the continental United States with some red splotches"
title="So this was really just a basic cellular automata, but Landon did it wrong! He didn't use two buffers, so he was reading and writing the same data! eeep! But, he's an artist primarily, you can't really blame him, especially because at this point it wasn't scientific, it was just a visual thing">

After I got my hands on it, I made some technical improvements and changes, and then, having no real direction from my boss [Barrie](https://www.uidaho.edu/people/brobison), which would come to be a theme during my time at Polymorphic Games, I made this:

<img
src="/images/OutbreakSimulator/myfirstversion.png"
alt="A photo of a map of the continental United States with some red splotches, and some green splotches!"
title="The green! I remember vaguely asking what to do on this, and somebody said add some green or something, so I did!">

Here the green had a sort of oppossite effect from the spreading red, but really I was just messing around trying to figure out what my Boss wanted from me! A lack of direction from the director of the studio was a problem for years, Barrie simply had a lot of other things on his plate! He had a class or two to teach, an institute to direct, and his co-director of the game studio, which for them was frankly a fun side project, was the new chair of the Computer Science department who found himself swamped! I've used a lot of exclamation points this paragraph!

Here's the first version of Outbreak Simulator with real data layers, which would come to be the coolest part of the project imo.

<img
src="/images/OutbreakSimulator/firstdatalayers.png"
alt="A photo of a map of the continental United States with some red splotches, and some population density! There are two lake michigans"
title="It was so hot this summer, and one time I attended a zoom meeting shirtless, just angled my camera up really high to hide it. Barrie said something like 'I can't seem to see Carson's face for some reason' in a sorta jovial manner, I guess deriding my choice of camera angle? Little did he know, there was a reason behind it all!">

You'll notice that on my fantasy map of the US here we have two lake Michigans, no Florida or Maine, and we're missing some other bits and bobs. This is because I did the map as an intersection of the thing Landon made, and what I grabbed from the data layers. Here's an improved version of the same idea, this time with the [compartment model](https://en.wikipedia.org/wiki/Compartmental_models_(epidemiology)) implemented.

<img
src="/images/OutbreakSimulator/betterdatalayers.png"
alt="A photo of a map of the continental United States with some green splotches, and some population density, and numbers!"
title="Do you notice the 2 shades of blue around the map? Yea, that would cause a lot of grief later as I tried to add more data layers to this. I was just using such a weird coordinate space.">

At this point we have the SIR model running on the simulation, multiple colors indicating infected, exposed, and recovered, all on a population map. Here's a photo from a version after other people got involved!

<img
src="/images/OutbreakSimulator/3dversion.png"
alt="Another photo of the project, this time with futuristic UI and graphs and such"
title="Fun fact, I used the panel on the left to adjust the variables until the very end, even when we re-designed the UI and it looked super out of place, I just had it bound to 'I' to appear and disappear.">

You can see we stuck with the Zombie idea for a while, until we got some complaints and pivoted to calling things influenza instead of zombie. I believe it was Lily and Landon who did the UI for this, and I remember talking to Landon once about how I had no idea how to use Unity when I started, and he said 'I know'. I can only imagine what he thought of some of my design decisions!

At some point, probably after the above screenshot, I added the [gillespie algorithm](https://en.wikipedia.org/wiki/Gillespie_algorithm) and [tau-leaping](https://en.wikipedia.org/wiki/Tau-leaping) which were very fun, if difficult, to figure out and implement.

There's a lot I'm skipping over for sure, like [running the project on a supercomputer](https://professorpolymorphic.github.io/PolymorphicWeb/DevBlog/posts/falconGUI/), going to conferences like the one pictured here:

<img
src="https://www.iids.uidaho.edu/img/Landon-Carson-AIED.jpg"
alt="A photo of Landon and I in Durham, a few computers set up with Outbreak Simulator running in the background"
title="This was legitimately the nicest shirt I owned at this point">

Landon (pictured on the left) and I (right) had a great time in Durham, in Britain no less! My first time travelling abroad since I was a small child and very briefly entered Canada with my parents. Our boss, Barrie, was not having a great time, he got Covid immediately and all he saw of Britain was a tapas place we went to (I think somebody recommended it?) and the inside of his hotel room.

Landon and I mostly spent our time wandering Durham, we went to the conference when we had to, and attended a few of the talks/presentations. But yea mostly just goofing off and exploring the cathedral, castle, river, etc. etc. all that touristy stuff.

We went to other conferences, one in Coeur D Alene, one near Lake Tahoe, and one in Burlington, Vermont. At some point we received Idaho's very first SEPA grant to the tune of 1.3 million dollars over 5 years, all based on work that I had done! I wish I could link to the original page for the grant, unfortunately there was a cancellation of the grant and therefore project in 2025 (what an odd way to word that). All I can find when googling our grant ID (R25GM150142) is [this](https://taggs.hhs.gov/Detail/AwardDetail?arg_AwardNum=R25GM150142&arg_ProgOfficeCode=127). Luckily, archive.org saves the day and [here](https://web.archive.org/web/20250123210545/https://nihsepa.org/project/eradicating-misconceptions-about-viruses-using-multimodal-trace-data-in-an-intelligent-game-based-environment-across-educational-contexts/) is the original page on the SEPA website. The money I believe was going to be used to partner with some other University and do a bunch of other research and work, but I don't really recall the specifics.

After I left in September of 2024 to go teach English in France, Justin picked the project up and did some work on it, but I'm not really sure how much he got done, or what he got done, when the grant was cancelled and the project put on eternal limbo from there on.

You can find the final source code of the project (from me, not including Justin's changes) [here](https://github.com/CJ5518/OutbreakSim/commits/master/).

## Closing thoughts

I'm incredibly grateful for the opportunity that Polymorphic Games gave me, to travel and meet smart people and learn and grow, it was really incredible. Thanks so much to Barrie, for taking a chance on hiring a Freshman, Landon, for wasting time with me, and Justin, for letting me waste his time. Thanks to Kristen for making an awesome website for the project, which I still show off to people to this day.

I had assumed that having 3 years of experience on my resume, a proven project, photographic evidence of me at conferences, etc, would be enough to get me a job pretty easily after college, but boy howdy, I was wrong on that front. But if the job market wasn't so bad, Polymorphic Games would have been the perfect springboard to gainful employment outside of the University of Idaho. 

I had a great time with Outbreak Simulator, my only real wish is that I could have actually finished it up and released it properly. But even though it wasn't finished, and it was clunky, and had loads of technical debt, and components from people who didn't know what they were doing (shoutouts Ryan and the 100 line switch statement), still, there goes the best damned project I ever worked on.

<img
src="/images/OutbreakSimulator/meme.jpeg"
alt="A frame from the simpsons, with bottom text similar to the above"
title="I might edit this to have a frame of Outbreak Simulator over Homer and Lisa at some point">
