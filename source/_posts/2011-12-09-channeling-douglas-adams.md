---
title: Channeling Douglas Adams
author: Nate
layout: post
permalink: /2011/12/channeling-douglas-adams/
categories:
  - From The Labs
tags:
  - cross-post
  - mac mini
  - OSX
  - Programming
---
# 

In [Last Chance To See][1] Douglas Adams talks about writing a program that is very sexy and has pull down menus and everything, and it’s entire purpose is to figure out the volume of the nests made by a certain kind of bird. In an article called “[Frank The Vandal][2]” he writes about a desire to be able to take just the parts of programs you want and paste them into a workflow so that you can do whatever it is you want to do without using six different programs. This is a mindset that resonates with me. If I can spend a few happy minutes[1][3] writing pointless software to solve a problem now instead of seconds taking care of it manually once a week I will definitely go for the pointless software. It was in this vein that I tackled the following

 [1]: http://en.wikipedia.org/wiki/Last_chance_to_see
 [2]: http://www.douglasadams.com/dna/980707-00-a.html
 [3]: #footnote_0_1144 "or hours"

### Extremely Small Problem:

I do a lot of what [Natalie Goldberg][4] calls “[practice writing][5]”. which is where you just block out some time and keep writing for that entire time. This writing can be directed, or not, but the goal is to keep moving forward, to keep putting words on the page, or, in my case, into the text document. This isn’t “real” writing that you plan to put in front of other people some day, this is just exercise, to keep those writing muscles in shape.

 [4]: http://en.wikipedia.org/wiki/Natalie_Goldberg
 [5]: http://en.wikipedia.org/wiki/Free_writing

When you exercise your muscles, you aren’t left with an artifact of your exercise. But when you do writing exercise, you have this document that you created, and have to do something with it. It’s possible that some part of it might be worth something to you in some context, so it seems wasteful to just delete it. Once again referring to Natalie Goldberg, these are like compost; they’re not really valuable by themselves, but if you keep piling them up there’s a chance that someday something good will grow out of them. Being the nerd that I am, I decided that I would keep all these useless little documents, and I would keep them all in one folder, so they would stay out the way.

So, on my home Mac I set up [Hazel][6] to just take those documents, rename them to today’s date (which gives me a good record of which days I did my writing practice and which days I didn’t) and shove them in a folder. All of this happens without me thinking about it, because Hazel is awesome. So, here comes the extremely small problem:

 [6]: http://www.noodlesoft.com/hazel.php

Sometimes I do my writing practice on my laptop, which is a PC.

Because I’m insane and picky and whatnot I use [FocusWriter][7] on the PC[2][8] and FocusWriter, by default, produces Rich Text files (rtf files). BUT I have WriteRoom set to produce plain text files (txt files). It’s possible that I could just set FocusWriter to save things as txt files by default, but that’s crazy talk. Simple solutions need not apply, thank you very much. And I still have the problem of getting my little documents[3][9] from my PC to my mac, and in the right folder.

 [7]: http://gottcode.org/focuswriter/
 [8]: #footnote_1_1144 "it most closely matches the functionality of WriteRoom, which is what I use on my mac"
 [9]: #footnote_2_1144 "which, you’ll remember, are pretty much worthless"

Now, I grant you, I could move these files myself, but part of being who I am is having a rock-solid conviction that I shouldn’t be thinking about things if I can make a computer think about them for me. My ultimate goal is to be able to write something mindlessly and forget about it, secure in the knowledge that when I look for it[4][10] it’ll be where I expect it to be.

 [10]: #footnote_3_1144 "which may nor may not ever happen, but that’s beside the point"

After a little bit of thinking and a little more tinkering, I came up with the following

### Gloriously Baroque Solution:

The moving parts involved here are (in order):

1.  [Dropbox][11]
2.  Hazel
3.  [Automator][12]
4.  [Word 2011 for Mac][13]
5.  Hazel again

 [11]: http://db.tt/WW19iU5
 [12]: http://www.apple.com/macosx/apps/all.html#automator
 [13]: http://www.microsoft.com/mac/word

Here’s how it goes:

I write my useless document, and save it to a particular folder in my Dropbox. It’s instantly beamed to all the other computers that are connected to my Dropbox account.[![Otto: the Automator icon][15]][15]

 []: http://crazyapplenews.com/wp-content/uploads/2011/12/Otto.jpg

On my mac, Hazel is monitoring that folder, and sees a new rtf file show up. It starts a rule[5][15] that renames the file and moves it into my “compost” folder. But the file is still an rtf instead of a txt file! Not to worry, this is where it calls Automator.

 [15]: #footnote_4_1144 "Hazel’s name for a set of actions that happen when a certain condition is met"

I’ve created an Automator workflow that takes the file, loads it into Word, converts it into a txt file and saves it.[6][16]  It then hands control back to Hazel. The Hazel rule completes, and colors the label of the original rtf file gray. This triggers a second Hazel rule that is watching the compost folder. This rule does one thing: if it finds an rtf file with a gray label it puts it in the trash. Since these files are only turned gray after the txt version is created I’m no longer worried about keeping the rtf file around.

 [16]: #footnote_5_1144 "and then closes Word. I don’t know why this is a separate step, but it is."

This all works perfectly, much to my surprise, and (even more surprisingly) usually takes less than five seconds to run, even with all the Word opening and closing stuff. And since it’s happening while I’m not at my mac it’s effectively happening instantly.

### Conclusion

Well, there isn’t one, really. All in all this took me about 20 minutes to set up, and will save me a few seconds of work a few times a week. But it’s work that I’m unlikely to do by myself, which would compromise the integrity of my compost folder. So, here’s to creative solutions to minuscule problems!

Note: This article was cross-posted here and at [Coals[2]Newcastle][17].

1.  or hours [[↩][18]]
2.  it most closely matches the functionality of [WriteRoom][19], which is what I use on my mac [[↩][20]]
3.  which, you’ll remember, are pretty much worthless [[↩][21]]
4.  which may nor may not ever happen, but that’s beside the point [[↩][22]]
5.  Hazel’s name for a set of actions that happen when a certain condition is met [[↩][23]]
6.  and then closes Word. I don’t know why this is a separate step, but it is. [[↩][24]]

 [17]: http://coals2newcastle.com
 [18]: #identifier_0_1144
 [19]: http://www.hogbaysoftware.com/products/writeroom
 [20]: #identifier_1_1144
 [21]: #identifier_2_1144
 [22]: #identifier_3_1144
 [23]: #identifier_4_1144
 [24]: #identifier_5_1144