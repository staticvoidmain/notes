# Shit Bad Programmers Do

[Stupid Good](!/images/stupid_good_sign.png)

This post is brought to you by the incessant and increasingly aggressive reminders to post something from my friend Covington over at Stupid Good Coffee. If you're in Dallas and you want coffee, and a breakfast taco, check them out. If you're here because you saw the sign

## A long awaited return to nerdrage

So, I started this post a while ago when I did a lot more code reviews, and I think I was pretty pissed off. The tone is pretty agressive, but really, you aren't necessarily 'bad' unless you've been working in the industry for a while and you stil do these things. I suppose a more constructive title could have been, "Things beginner programmers do (and should unlearn in a hurry)". I actually don't care what level you are, or how long you've been programming, just please stop doing these silly things.

Some behaviors can be lumped into broad categories, like borrowing idioms from other (much older) languages and failing to adapt to newer environments, some are to do with inexperience, and some are just fucking dumb.

As programmers, a large portion of our lives is spent deciphering other people's code, and the least you can do is ease that burden slightly by not doing some weird shit that makes my eyes go cross. I shouldn't have to scratch my head and wonder how the hell this ever worked in the first place, in order to deal with whatever it is I'm actually tring to do. The polite way to state this is to use a style-guide, but that doesn't seem to resonate with people. This isn't even about "good taste", it's about me keeping my sanity.

So, here is a list of things not to do, in no particular order.

## Don't do silly things with bools that makes me think you don't understand them.

This really kills me.

``` java
// you almost had it...
if (expected == actual) {
    return true;   
} else {
    return false;
}

``` java
// OR this gem
if (x == null || x != null && x.y < 10) { }
```

The second bit is redundant. The fact that you made it to the other side of the || means that X isn't null, that's how || works.

``` java
// mega annoying
bool match = expected == actual ? true : false;
```

The expression _itself is boolean_, people. The local is equal to the result of the expression. That's it. You're done. Stop making it more complicated than it has to be.

# Don't comment out code

``` java
usable_code();

// this used to work at one point, and now I don't understand why
// some guy 10 years ago
// Do_All_The_Things(something, out stuff);

more_code();

```

If you see this, delete it. If this is you, I hate you.

To that end, signing and dating your comments is annoying, and makes me think you don't understand how version control works. Cut ito out.

## Don't Allocate then immediately overrwrite

``` java
Thing x = new Thing();
x = GetThing();
```

Just declare and initialize in one line please.

## Don't use Hungarian Notation

``` java
string strMessage = "You make me sick."
bool bolDoIHateYou = true;
```

