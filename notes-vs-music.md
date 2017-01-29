# Hey, 'Backend Guys'

I'm gonna piss you off for a second. You're not the alpha nerds you think you are. Your code sucks and it's embarassing to look at. Not because it isn't functional or correct, but because it doesn't do anything anyone actually wants.

I came up with a lovely analogy, which I think works well to illustrate this point.

If you are a _programmer_ who does not understand _design_, you are a composer who understands music theory, but is **tone deaf**. The notes could be perfectly arranged, but they still sound like shit.

# Code is for Humans

In nerdy circles, when most people use the phrase "code is for humans", what they _mean_ is that you should care about the style and organization of your code so that future humans who come along can read and maintain it. That statement, while(true), is perhaps not the real message we should take away.

Code is ultimately **FOR** humans, to consume and enjoy. It is **for** our benefit that _any of this exists at all_. So, to belie the fact that humans are the ultimate consumers of our craft and focus only on shuffling registers around is perhaps doing ourselves and our customers a disservice.

So go learn some design.

**Stop** learning about the Angular dependency injector and **start** learning about material design.

If **this** pisses you off:

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

and **this** doesn't:

[](./images/bad_design.png)

You are living a sad and lonely existance.