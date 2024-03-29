PFMud intends to provide an ORC License compatible implementation of a 
Pathfinder Compatible MUD. As of 2024 mymud.io will provide the reference 
hosted implementation of this Evennia-based MUD. Eventually, [backrooms.net](https://backrooms.net)'s 
mud will run off this engine.

# Welcome to PFMud!

Creating an ORC License and Pathfinder compatible MUD sets a lofty goal. As
this project progresses, I will likely ask for community support. Keep checking
back for change logs and progress reports!

Currently, my local DEV enviroment follows typical Evennia three-directory installation: 
**evennia** (using evennia's current codebase), **evenv** (for a virtual environment), 
and **mymud** (for pfmud project's code.)

## PFMud is an extension of Evennia MUD Engine

This is your game directory, set up to let you start with
your new game right away. An overview of this directory is found here:
https://github.com/evennia/evennia/wiki/Directory-Overview#the-game-directory

You can delete this readme file when you've read it and you can
re-arrange things in this game-directory to suit your own sense of
organisation (the only exception is the directory structure of the
`server/` directory, which Evennia expects). If you change the structure
you must however also edit/add to your settings file to tell Evennia
where to look for things.

Your game's main configuration file is found in
`server/conf/settings.py` (but you don't need to change it to get
started). If you just created this directory (which means you'll already
have a `virtualenv` running if you followed the default instructions),
`cd` to this directory then initialize a new database using

    evennia migrate

To start the server, stand in this directory and run

    evennia start

This will start the server, logging output to the console. Make
sure to create a superuser when asked. By default you can now connect
to your new game using a MUD client on `localhost`, port `4000`.  You can
also log into the web client by pointing a browser to
`http://localhost:4001`.

# Getting started

From here on you might want to look at one of the beginner tutorials:
http://github.com/evennia/evennia/wiki/Tutorials.

Evennia's documentation is here:
https://github.com/evennia/evennia/wiki.

## Upgrading to newest Evennia when developing

https://www.evennia.com/docs/latest/Setup/Updating-Evennia.html

## Reseting for failed upgrades

Use the Ubuntu environment. Windows is too buggy.

Delete the 'evennia' directory and the 'evenv'
directory.

<pre><code>
git clone https://github.com/evennia/evennia.git
python -m venv evenv
source evenv/bin/activate
cd evennia/
pip install --upgrade -e .
pip install --upgrade -e .[extra]

cd ../mymud
evennia start

</code></pre>

## gpt-engineer Configuration
To use gpt-engineer to work with a 'mymud' or any evennia MUD development, you'd want
to include 'evennia' as a library in the same environment. First get your gpt-engineer
venv running. It might be in something like:

/mnt/c/python_workspace/gpt-engineer

Then pip install the evennia project in your prefered way to give it access.
