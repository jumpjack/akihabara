Live demo [here](https://jumpjack.github.io/akihabara/test/runner.html).


Akihabara
=========

Akihabara is a set of libraries, tools and presets to create pixelated indie-style 8/16-bit era games in Javascript that runs in your browser without any Flash plugin, making use of a small small small subset of the HTML5 features, that are actually available on many modern browsers.

Notes about audio features
--------------------------

* Audio compatibility is *Work in progress*
* Firefox stable has little audio caching problem/slowdowns and sometime freezes - can't figure out if is plugin's fault. Seems fixed on nightly builds. Audio is not marked as experimental.
* For compatibility with Safari, every audio file used for games MUST be more than 1.5 seconds long. Add silence to reach the 1.5secs length.
* Safari is having troubles on downloading audio for unknown reasons. Seems fixed on nightly builds. For now AUDIO IS EXPERIMENTAL.

Notes for developers
--------------------

* For maximum compatibility make sure that you're using the ["name"] for when setting object properties with reserved names like "goto" and "data" (Discovered during patching for Wii)
* Also do not use the comma after the last element of an array or a property of an object. Still work on many browsers but is broken for Opera Wii. (and probably IE, when will be supported)
* For making sure that your sub-scripts are loaded, try to add an "alert" at the end. Opera for Wii silently fail when there are syntax errors like the one explained before.
* Opera Wii wants that canvas have to be blitted at least once before being used - or fails with a browser crash! The built-in gbox.createCanvas was already fixed. Is a good thing to use that method for spawning canvas.

### Running tests

Just run the runner.html on test directory.

### Generating Documentation

Just run `make doc` command. The documentation will be generated on the doc directory.

Mailing List
------------

* http://groups.google.com.br/group/akihabara-engine

Wiki
----

* For more informations follow our [Wiki](https://github.com/akihabara/akihabara/wiki)

Legal informations
------------------

The initial akihabara code was made by Fracesco Cottone (http://kesiev.com) as an open source project dual licensed by MIT and GPL.

Special Thanks
--------------

These guys deserves an special thanks:

* Carlos Benitez form EtnasSoft (http://www.etnassoft.com/) for all patches and helping on Akihabara development.
* Darren and Darius for the initial not finished documentation and the tutorials, it helped a lot on the for the first version.
* Rafael Masoni for helping on Akihabara website and game assets.
