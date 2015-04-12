This command-line program allows the user to rapidly strip junk audio from the beginning and end of audio files.  It can be used, for example, to clean up files recorded with [Streamripper](http://streamripper.sourceforge.net) (_e.g._, `streamripper --xs_padding=5000:5000`).

Sonfilade is designed to be as effortless and fun as possible to use.  An entire edit session can be carried out using only three keys and sound feedback as the entire user interface.  (There is also text output, but it is non-essential.)

Each file is edited in four steps

  1. Choose the start point.
  1. Choose the end point.
  1. Adjust fade-in time.
  1. Adjust fade-out time.

A few seconds of audio is played after each adjustment to provide feedback on the current start or end of the clip, as appropriate.

In all cases, 'up arrow' means "more" and 'down arrow' means "less".  So, for example, when choosing the start time, if the clip is entirely good material, you can hit 'up' to extend the clip.  Alternatively, if you hear trash, hit 'down' to make the clip shorter.  [Binary search](http://en.wikipedia.org/wiki/Binary_search) is used to narrow in on the correct points--if you make an incorrect choice, you can hit 'r' to reset and start over.  When you're happy with what you hear, hit enter to proceed to the next step.

The program requires [Python](http://www.python.org/) 2.5 (or later) and [sox](http://sox.sourceforge.net/).  It was developed under Ubuntu Linux with sox 14.2.0, but will probably work with other flavors of Linux/BSD/etc.


---


Aside from its obvious use as an audio editor, this program also provides some practical insight into psychoacoustics and the binary search algorithm.