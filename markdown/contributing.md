<!-- .slide: data-background-image="images/jc.jpg" data-background-size="contain" -->

Note: Alright, back to my cute, beautiful patch.


<!-- .slide: data-background-image="images/patch_1_qrcode.jpg" data-background-size="contain" -->

Note: Though in reality it looks more like this.  (This is a link to the diff
on github.)


# 90 LOC!

Note: This was a **nine-ty-line** patch.  AND, it actually worked.  They're
gonna love me.


<!-- .slide: data-background-image="images/confident.svg" data-background-size="contain" -->

Note: So, in the beginning, I was feeling pretty good about myself.  I had
learned enough of the code to create a working patch, after all.  And it wasn't
just a one-liner, either.


## Pull Request

Note: And then I opened a Pull Request, or "PR".  It's not hard: you push your
change up to your own github repository, and press a button.


A little
## bureaucracy

Note:  And then, the first thing you learn is that you have to grant edX (the
organization) co-ownership of whatever you submit.  So you go through a little
legalese and sign it.  No big deal, as everything is AGPLv3 anyway.


## `open-source-contribution`

Note: A minor detour, once again.  You can tell the edX community is in its
beginings because of this tag on `edx-platform` on github.  While this could've
meant my patch would get more attention, it is a little disconcerting that it
merits special attention at all.

Once again, a comparison to OpenStack.  There is no such thing, there.  All
patches are supposedly equal.  The do newcomers the courtesy of hiding any
differences in "status" outside the internet.


Oh, right...
## Tests!

![Failing Checks](images/failing_checks.png) <!-- .element: class="fragment" -->

Note: The first "surprise" were the several red crosses at the bottom of my
Beautiful Baby.  "What do you mean, my Beautiful Golden Patch is failing 5 out
of 6 tests?  It doesn't even pass the dumb Quality one?  Who do they think they
are?"  And then reason kicks in and you thin, "Oh, wait, this must be old stuff
being retested - it's not my fault!"

So you go and learn how to test stuff in Devstack.  And after some time (a
significant amount of time, for acceptance tests)...


<!-- .slide: data-background-image="images/sad_trombone.svg" data-background-size="contain" -->

Note: Crestfallen, you discover that the latest master gets all greens.

Whaddya know?  Open edX is a serious project, after all.  And guess what... It
expects you to test your stuff.  **ALL** your stuff.


Of
## coffee
and
## cabbage

Note: This is where you learn about Coffeescript (and how some tests use it,
some don't), and the acceptance test Bok Choy (a Chinese cabbage, apparently).
You also learn how cabbage-testing a single suite (there are several) can take
10 minutes on your trusty old dev box.

Back to work, it is!


## "It builds character, man."

Note: This is what my high school history teacher, Mr. McFarland, used to say
when he asked you to rewrite your assignment.  (He was a Baby Boomer.  And now
that I think about, Ned Bat reminds me of him, a lot.)  And he did it two or
three times until he thought you got it right.  Or at least, right enough.  It
was a humbling experience, but it did, in fact build character - and it
certainly prepared me for a professional life in software, of all things.

Anyway, this is exactly what happened.  I had my pretty baby, and it was
(mostly) tested.  I got on Slack, and asked for some eyeballs - once again,
confident I would get "oohs" and "ahs".

Nope.  "Thanks, but I think it would be great if..."


<!-- .slide: data-background-image="images/confused.svg" data-background-size="contain" -->

Note: And so they asked me, quite politely and in a single deceptively simple
sentence, to instead of reinventing the wheel, to refactor the relevant code
out of the CMS into a common library.  But, but... But XBlock javascript
(tested in Coffeescript) can't use the utility library, because the latter uses
RequireJS, and not the former.

And so down the rabbit hole I went.


## 600 LOC

Note: This went on for a few iterations, and after a few such
character-building events, I was looking at a 600-line patch that touched on
places I never dreamed of.
