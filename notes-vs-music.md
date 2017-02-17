# Hey, 'Backend Guys'

I'm gonna piss you off for a second. You're not the alpha nerds you think you are. Your code sucks and it's embarassing to look at. Not because it isn't functional or correct, but because it doesn't do anything anyone actually wants.

I came up with a lovely analogy, which I think works well to illustrate this point.

If you are a _programmer_ who does not understand _design_, you are a composer who understands music theory, but is **tone deaf**. The notes could be perfectly arranged, but they still sound like shit.

# Code is for Humans

In nerdy circles, when most people use the phrase "code is for humans", what they _mean_ is that you should care about the style and organization of your code so that future humans who come along can read and maintain it. That statement, while(true), is perhaps not the real message we should take away.

Code is ultimately **FOR** humans, to consume and enjoy. It is **for** our benefit that _any of this exists at all_. So, to belie the fact that humans are the ultimate consumers of our craft and focus only on shuffling registers around is perhaps doing ourselves and our customers a disservice.

So go learn some design.

- **Stop** learning about the Angular dependency injector and **start** learning about material design.
- **Stop** building architectural diagrams and **start** asking questions about your customers.

# No Excuses

There really aren't any convincing excuses as to **why** programmers are so allergic to design. I mean, unless you've actually got a clinical diagnosis of Asperger's Syndrome and your brain is incapable of processing human emotion, then I **still** think you could do it. Just get yourself a hug machine and study a labeled book of human faces like Temple Grandin. No excuses. If you want to be a great programmer, this is required.

if **this abomination** offends you:

```cs

private string StrLength(string s, int len, string repl){
    string result = string.Empty;
    result=s;
    while (result.Length < len){
        result = repl + result;
    }
    return result;
}
```

and **this piece of shit** doesn't:

[](./images/ugly-UI-v2.jpg)

You are only seeing half the sky.

# Follow your nose

We all know the acrid stench of smelly code, but we're much less likely to understand smelly design.

Smelly design is bad for exactly the same reasons as smelly code, it implies laziness, a lack of understanding, and leads to further abuses of good practice, but *the difference* is that your customers actually SEE your smelly designs. 

I've heard professional programmers *actually* complain: 

> Oh well, they don't care about my code, all they see is the UI. 

*No fucking shit, really?*

Get it together people. *Get* your *shit* together. Put it in a backpack. [Just get it together](https://youtu.be/jl17CYYSzUw?t=93).

Whew, rant over. 

*The good news* is I think once trained we can spot bad design just as effectively as we can bad code, after all, *it's just patterns*.

Smells include:

- poor alignment
- mismatched fonts/weignts
- inconsistent colors
- 