
# Unlocking your Visual Studio potential

- Twitter: @RossJennings
- Website: SmugDeveloper.com

#  Your Potential

<iframe width="854" height="480" src="https://www.youtube.com/embed/yNKoH84ioz0?start=50" frameborder="0" allowfullscreen></iframe>

# Mostly Kidding

I think it's safe to say you can tap into a little bit of your potential. Don't be afraid, you can probably do it.

# Inspiration

<iframe width="854" height="480" src="https://www.youtube.com/embed/YNfBF2xvhaE?start=82" frameborder="0" allowfullscreen></iframe>

<aside class="notes">
  Credits to the amazing web series 'You Suck at Photoshop' for the inspiration for this. It's one of my favorites from the early days of youtube.

  The unique blend of practical advice and sardonic dark humor is enormously entertaining, and I hope to achieve a similar motif here.

  I won't be quite as mean as Donny; I won't openly berate you, but I think that generally people who use visual studio do so because they know it's the de-facto IDE for .Net and that's what they have to use, not because it's the best editor, or because they know it really well.
</aside>

# Your Visual Studio license costs $6K

You're probably getting about $20 bucks worth. 

# Perspective
To put that in perspective, let's look at it visually.

[Wasted Dollars](./images/editor_money.gif)

<aside class="notes">

  Now, to be fair, it's probably not really coming out of your pocket, so you don't really _have_ to care as much, but at least learn to leverage the investment to improve your quality of life.

  It makes sense to invest in the best tools possible, but if you don't really understand how to exploit that value, you may as well spend 0.5% of the asking price on a personal copy of Sublime Text 3 or VSCode 

  [1] You should always have a lightweight and competent text editor for making small quick changes. Change the default C# file assocation to use this editor instead of Visual Studio. 
  [2] Notepad++ is terrible. Stop using it.
</aside>

# Disclaimer 

I can't really make you a promise that you're going to unlock the FULL potential just by watching my videos, or that I even know all the ins and outs myself, but I'm gonna do what I can.

# Your tools matter

I shouldn't have to tell you this, but you spend a lot of time typing text into a computer. You have 

* Your text editor should be an extension of you. 
* brain -> keyboard -> screen 
* If you spend most of your time wrangling your tooling to get it to work right, either your tools suck, or you suck.

# Thus ends the lesson

Next up, fixing the horrible defaults.

#  The Defaults Suck

- Twitter: @RossJennings
- Website: SmugDeveloper.com

# Bad defaults

Sane defaults are a big deal. Visual Studio is, getting better, but it's still not completely sane.

* Ugly
* Basic
* Bloated

Now it's just basic and bloated.

<aside>
  The stock-standard Visual Studio instance is not really a thing of beauty or productivity. Sure, you can file->New Project and get going right away, but the color scheme is an affront to the eye, and it doesn't really do much besides run msbuild for you.
</aside>

# YAGNI

Don't need a fully featured debugger, profiler, style checker, integrated source control provider, visual designer, or any one of a hundred other things that visual studio is taxing you for?

Don't use it.

# Taco-Bell Toolchain

* ConEmu
* Git
* MSBuild Tools
* VSCode

<aside class="notes">
  You would honestly be better off with a nice console, git, the free MSBuild tools, and a copy of VSCode, surprise, also free.
</aside>

# Taco-Bell Workflow

```bash
  code .
  build-and-run my.solution.sln
  git commit -a -m "Look at me mom!"
```

There. I saved you a boatload of time, energy, and money.

<aside class="notes">
  I cheated a bit. That's not a real command, but it could be!
</aside>

# Optimization

* Optimize the "Critical Path" first
* You do the thinking, let the software do the lifting.
* Be demanding, and never settle for a lazy editor.

<aside class="notes">
  We're gonna follow the same logic when customizing our environment as you might when optimizing code, which is focus on the "Hot Path". You should be impatient and demanding of your editor.
</aside>

# Look at all these settings...

What if I told you there was nother way...

<aside class="notes">
What if I told you there were some maaagical settings that would speed up your build, help visual studio launch quicker, and generally help you capture some of that 6-grand your company blew on it. 

Ross, you're crazy. What sane person wouldn't want that? If those settings existed they would be on by defau...hhhh crap.
</aside>

# Environment -> General

* Dark Theme! Spare your eyes from the torture of black text on a white background.
* Ensure adjust visual for performance is on.

* Optimize Startup
  - disable the start page.
  - don't download content, ever.

# Build and Run

* Only 4 max parallel projects, let's make it 8! 
- (Some experimentation may be required. Your Mileage May Vary)

# Intellitrace
- Have you ever actually used it? 
- I didn't think so. 
- Turn it off until you need it.

# XAML Designer
- Swap the default view to code-only.
- Also, WYSIWYG editors for markup languages are for cowards who can't code.

# Misc

- Right-Click Win Forms file
- Open With... CSharp Code Editor. 
- Set the default editor


<aside class="notes">
  If you're still laboring in WinForms land, firstly, my condolences. 

  Sure, some people know that it's F7 to view code, but honestly, WHY would that be the hot path? 

  How often do you step on this landmine only to be interrupted? My guess would be several times per day.

</aside>

# You feel enlightened

Continue on if ye be worthy.

#  The Keyboard And You

- Twitter: @RossJennings
- Website: SmugDeveloper.com

# The mouse is for n00bs


- Don't be a clicker

<aside class="notes">
  Anyone who has ever played World of Warcraft, or really any PC game knows that the worst thing you can be is a 'clicker'. 

  I suppose there was also the keyboard-turner, but I think perhaps the two go hand-in-hand.

  Essentially, being inefficient with your inputs is bad.
</aside>

# Motha F***ing Code Snippets

```csharp
foreach[Tab][Tab]
```

BOOM

```csharp
foreach (var item in collection) { 

}
```

# You can write your own

- bbo
- dirtyprop
- courier

Go nuts. Share with your friends.

# Play the right chord

Make an effort to learn some of these, you will notice a big difference. 

http://visualstudioshortcuts.com/2015/

# Ross's Greatest Hits:

- Ctrl+K, Ctrl+D: Format Document
- Ctrl+Shift+B: Build project, but don't run.
- Ctrl+K, Ctrl+R: Find all references
- Ctrl+R, Ctrl+M: extract method
- Ctrl+R, R: Rename without leaving the home row.
- Ctrl+R, A: Run ALL tests

# With each note, you feel your productivity increasing.

It feels good, the taste of power. Let's go on.

# Finding Things

- @RossJennings
- SmugDeveloper.com

TODO: is this even worth a whole video?

# Ctrl+Shift+Fuuuuuuuuuuuuuu

- Ctrl+comma: find anything, with type-ahead auto-complete goodness. 

[YOU'RE WELCOME](./images/nickburns.jpg)

# Bro, do you even Regex?

See that little icon over next to the 

# Next-Level Skills: ack / ag / ripgrep

> Sometimes, the best way to utilize a tool is to put it away. -Me, just now.

* Sometimes you need to find things that span multiple solutions, or multiple directories.
* For such tasks, the old ways work best. 
* Be a big boy (or girl)
* Open up the command line, and use the right tool for the job.

# Extensions Galore!
- Twitter: @RossJennings
- Website: SmugDeveloper.com

# Re-Sharper

You probably already have it. Again, these are probably settings you've never looked at.

# Web Essentials

Let's have an html typing contest.

I want you to write a snippet of valid html that 
* creates a div 
* a class of "content"
* and inside that put an unordered list with 3 elements.

# Ready?

# GO

# Oh hey look I won. 
```

div.content>ul>li*3

```

[magic happens]

```html
<div class="content">
  <ul>
    <li></li>
    <li></li>
    <li></li>
  </ul>
</div>
```

# But wait there's more!

I hear the cynics. I'm looking at you Brent.

> How long before the editor just codes for you.

The future is now!

# Visual Code Assist:

https://marketplace.visualstudio.com/items?itemName=OneCodeTeam.DeveloperAssistant-13032

How much would you pay for this modern marvel? $100 / hour plus benefits? NO it's yours for the low low price of a VS license.

Disclaimer: Please don't actually use this for production code.

#  The Debugger

* 





