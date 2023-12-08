# roger’s december adventure

2023-12-8

![mister1x4.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/02c03237-d8ef-4f9a-b5b1-3a0064ddccd8/bff911d9-45d2-4fc4-9d9d-55d2e4f26c47/mister1x4.png)

Trying [this](https://eli.li/december-adventure) out. Do a little bit every day towards a programming project.

Apologies at not having a proper website. You can reach me on Reddit,  where I go by mcsleepy.

I’m just a simple artist without a computer science degree. I’ve always been interested in Forth and minimalist coding, specifically in service of hobby game design, because it can be manipulated rapidly and get you to point B fast. I’ve released [a](https://store.steampowered.com/app/341060/The_Lady/) [few](https://inkajoo.itch.io/alright-were-gonna-walk-now) [games](https://inkajoo.itch.io/uncle-chunks-project-spin) and have many unfinished projects sitting in the dark, dank corners of my laptop. I also have heaps of gamedev-related bits written in various dialects. I joined decadv partially out of a desire to do better at showing my work, but also to get me to finish more stuff, which I expect the former to pressure me into doing. 

My aim is to explore game design, fueled by childhood memories of my relationship with classic PC and console gaming. As a starting place I will implement an [accelerated graphics window](https://liballeg.org/), a little library based on previous work, a REPL, and maybe a few tools. Then I will think about what to make.

I think the main reason I want to use Forth to do it is to make use of all the code I’ve already written as some of the tools I made have potential, and Forth, when used correctly, is just plain fun.

Milestones should be in the form of small games or interactive art pieces. Each sub-project will contain a unique version of the engine, combining iteration and customization, enabled by keeping things small and manageable.

I’m using [VFXForth](https://vfxforth.com/).

# 8

Made this webpage and spent some time filling it with text.

Looking back over the work done so far has given me a sense of how much goes into game development, even when it’s minimalist. It is so easy to get lost in thinking about “necessary features”. It’s key to keep things *dead-*simple and do as much as possible with as little pre-work as possible, embracing all the limitations. This’ll give me the side bonus of not writing too many things that depend on fixed-point because I might backpedal on that. The problem there is I need to get the newest VFXForth that supports SSE working because the current version I use only supports the 8-deep x87 float stack and the newest VFXForth cannot be recompiled to support more than 8MB dictionary because it isn’t code-signed and Windows 11 refuses to run the resulting executable. I might consider just working within 8MB (can always allocate more memory from the heap but doing things in the dictionary is more convenient).

I need to think about stuff to make next. I may have gotten just a little bit ahead of myself, as I don’t even know if I want to bother with tilemaps. But I might start with creating a level-editing tool, or use something readymade like [Tiled](https://www.mapeditor.org/) to just enjoy being creative and then put something into the engine.

Today I have to finish fixing a synth and put that and a few other pieces of gear up for sale since I got an Analog Rytm. (I also [make music](https://linktr.ee/topicalfruitsalad).) 

# 7

(Retrolog)

Added text support. 4 lines, 8x8 stock Allegro font, nothing exciting. I had to do some errands.

# 6

(Retrolog)

Found out about decadv. Probably added a few features and fixed some bugs.

# 5

(Retrolog)

![Screenshot 2023-12-08 120546.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/02c03237-d8ef-4f9a-b5b1-3a0064ddccd8/0d8eb85b-797f-4083-bce9-89ab5ecf28ce/Screenshot_2023-12-08_120546.png)

Finished laying the groundwork. 

I’ve got the bare minimum to get started.

- graphics window management
- keyboard & mouse (polling)
- basic graphics (rectangles, bitmaps)
- tilemaps w/ scrolling support
- fixed-point numbers (might backpedal on this)
- double-linked tree
- simplified file words
- game objects
- asynchronous timers

One important tenet I’m following is ******************NO TRADITIONAL OOP.****************** At least not for a long time. I’ve already tried to come up with my own Forth-y take on it several times and got in way over my head.

Instead components will be open and aware of each other as much as possible.

# 4

(Retrolog)

Made a Github for vfxland4 - should I keep everything in one repo? I’ll ask [a friend I made recently](https://rabbits.srht.site/decadv/) how they’ve handled this.

# 1 2 3

(Retrolog)

This is the period after around when I decided to revive my Forth work, going back to an old lineage where I treated Forth itself as the creative medium, not caring about a lot of typical programming wisdoms. It had the name TestPad at one point. Everything was open and direct, and trying ideas within the REPL (as well as compiling and testing code) was inspirational and productive.

The run-time model was to compile the game on-the-fly from source files (basically scripts, only they assemble to high-performance code before initiating execution), and I’m using that approach again here because it removes a lot of complexity.  You can’t just compile your data into your binary and use it on-demand when you’re using modern libraries based on OOP principles, so I’m sidestepping it.

Cleaned up the most previous codebase, vfxland3, making it more like TestPad by removing unnecessary features and simplifying some words. Calling it vfxland4 for now.

Here are a couple screenshots from around that aforementioned period.

![deadsimple.PNG](https://prod-files-secure.s3.us-west-2.amazonaws.com/02c03237-d8ef-4f9a-b5b1-3a0064ddccd8/5067a94e-4e52-4b1d-a856-54175d38aafb/deadsimple.png)

![darkblue january version.JPG](https://prod-files-secure.s3.us-west-2.amazonaws.com/02c03237-d8ef-4f9a-b5b1-3a0064ddccd8/c99e85c2-8d72-411f-b6c1-c2c22730bfdd/darkblue_january_version.jpg)