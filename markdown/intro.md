## Life as a new Open edX Contributor

[`adolfo.brandes@hastexo.com`](mailto:adolfo.brandes@hastexo.com)

[@arbrandes](https://twitter.com/arbrandes) | [@hastexo](https://twitter.com/hastexo)

*Use arrow keys to navigate, "ESC" for overview, or "s" for speaker notes.*


So, what is
# this
about?

Note: Last year I talked about our little OpenStack lab integration project.
Long story short, it worked.  But we soon discovered we didn't want students to
be able to take a lab unless they finished the previous one.  We found out
about an xmodule that provided the needed functionality...


<!-- .slide: data-background-image="images/sad_trombone.svg" data-background-size="contain" -->

Note: Except it didn't work with our XBlock.  (Because our XBlock loads custom
javascript, and the conditional xmodule wasn't originally written to load it.)

(This is the "Sad Trombone" in music notation - because they wouldn't let me
hook up the audio to the notebook.)


Open Source
# Power

Note: Well, what to do?  The source code is right there, so let's try fixing
it, shall we?  This is the story of how we went about it.


You should
# know a little edX

Note: Though I'm assuming some familiarity with Open edX, its features, and
codebase, this talk should be mostly accessible to everyone.

Oh, and you should also have a sense of humor.
