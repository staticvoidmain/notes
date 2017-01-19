
# Unlocking your Visual Studio potential

# Episode 0, Your Potential

(Leave It Alone)[./images/potential.jpg]

I think it's safe to say you can tap into a little bit of your potential. Don't be afraid, you can probably do it.

Credits to the amazing web series 'You Suck at Photoshop' for the inspiration for this. It's one of my favorites from the early days of youtube.

The unique blend of practical advice and sardonic dark humor is enormously entertaining, and I hope to achieve a similar motif here.

I won't be quite as mean as Donny; I won't openly berate you, but I think that generally people who use visual studio do so because they know it's the de-facto IDE for .Net and that's what they have to use, not because it's the best editor, or because they know it really well.

## Your Visual Studio license costs $6K

You're probably getting about $20 bucks worth. 

To put that in perspective, let's look at it visually.

[Wasted Dollars](./images/beer_money_vs_editor_money.png)

Now, to be fair, it's probably not really coming out of your pocket, so you don't really _have_ to care as much, but at least learn to leverage the investment to improve your quality of life.

It makes sense to invest in the best tools possible, but if you don't really understand how to exploit that value, you may as well spend 0.5% of the asking price on a personal copy of Sublime Text 3 or VSCode 

[1] You should always have a lightweight and competent text editor for making small quick changes. Change the default C# file assocation to use this editor instead of Visual Studio. 
[2] Notepad++ is terrible. Stop using it.

Disclaimer: I can't really make you a promise that you're going to unlock the FULL potential just by watching my videos, or that I even know all the ins and outs myself, but I'm gonna do what I can.

# Your tools matter

I shouldn't have to tell you this, but you spend a lot of time typing text into a computer. You have 

Your text editor should be an extension of your arms. It should bend to your will. 

Code should flow effortlessly from your brain to your fingertips to the keyboard to the screen with no barriers or distractions.

If you have to spend more time wrangling your tooling to get it to work right, either your tools suck, or you suck.

# Episode 1, The Defaults Suck

The stock-standard Visual Studio instance is not really a thing of beauty or productivity. Sure, you can file->New Project and get going right away, but the color scheme is an affront to the eye, and it doesn't really do much besides run msbuild for you.

You would honestly be better off with a nice console, the free MSBuild tools, and a copy of VSCode (also free). 

Edit code, build code, run app. There. I saved you some time and money.

We're gonna follow the same logic when customizing our environment as you might when optimizing code, which is focus on the "Hot Path". You should be impatient and demanding of your editor.

## Look at all these settings...

[Pretty Intimidating](./images/settings_window.png)

Well what if I told you there were some maaagical settings that would speed up your build, help visual studio launch quicker, and generally help you capture some of that 6-grand your company blew on it. Ross, you're crazy. What sane person wouldn't want that? If those settings existed they would be on by defau...hhhh crap.

### Environment

### General

* Dark Theme! Spare your eyes from the torture of black text on a white background.
* Ensure adjust visual for performance is on.

* Optimize Startup
- disable the start page.
- don't download content, ever.

### Build and Run

* Only 4 max parallel projects, let's make it 8! 
- (Some experimentation may be required. Your Mileage May Vary)

## Intellitrace
Have you ever actually used it? I didn't think so. Turn it off until you need it.

## XAML Designer
- Swap the default view to code-only. It's faster, and what you probably want to see anyway. 
- Also, WYSIWYG editors for markup languages are for cowards who can't code.

## Misc

If you're still laboring in WinForms land, firstly, my condolences. 

Right-click a Win Forms file, Open With... set the default editor to CSharp Code Editor. 

Sure, some people know that it's F7 to view code, but honestly, WHY would that be the hot path? 

How often do you step on this landmine only to be interrupted? My guess would be several times per day.

# Episode 2, The Keyboard And You

## The mouse is for n00bs

Anyone who has ever played World of Warcraft, or really any PC game knows that the worst thing you can be is a 'clicker'. 

I suppose there was also the keyboard-turner, but I think perhaps the two go hand-in-hand.

Essentially, being inefficient with your inputs is bad.

## Motha F***ing Code Snippets

```csharp
foreach (var foo in bar) { 
  // body
}
```


## Play the right chord

Make an effort to learn some of these, you will notice a difference. http://visualstudioshortcuts.com/2015/

### Ross's Greatest Hits:

- Ctrl+K, Ctrl+D: Format Document
- Ctrl+Shift+B: Build project, but don't run.
- Ctrl+K, Ctrl+R: Find all references
- Ctrl+R, Ctrl+M: extract method
- Ctrl+R, R: Rename without leaving the home row.
- Ctrl+R, A: Run ALL tests

[ With each note, you feel your productivity increasing. ]

# Episode 3, Finding Things

# Ctrl+Shift+Fuuuuuuuuuuuuuu

- Ctrl+comma: find anything, with type-ahead auto-complete goodness. 

YOU'RE WELCOME

## Bro, do you even Regex?

See that little icon over next to the 

## Next-Level Skills: ack / ag / ripgrep

Not totally related to visual studio, except to say that sometimes you need to find things that span multiple solutions, or multiple directories.

For such tasks, the old ways work best. Open up the command line, and use the right tool for the job.


# Episode 4, Extensions Galore!

## Re-Sharper


The cynics in the room How long before the editor just codes for you, you ask? The future is now!

Visual Code Assist:

https://marketplace.visualstudio.com/items?itemName=OneCodeTeam.DeveloperAssistant-13032

How much would you pay for this modern marvel? $100 / hour? NO it's yours for the low low price of a VS license.


Episode 5, The Debugger

* 





